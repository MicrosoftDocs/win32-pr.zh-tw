---
description: 本主題說明 DirectXMath 程式庫的內部設計。
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: 程式庫內部
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7c1843a83a81e7acac241c66dd18ff26217569
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827232"
---
# <a name="library-internals"></a>程式庫內部

本主題說明 DirectXMath 程式庫的內部設計。

-   [呼叫慣例](#calling-conventions)
-   [圖形程式庫類型等價](#graphics-library-type-equivalence)
-   [DirectXMath 程式庫中的全域常數](#global-constants-in-the-directxmath-library)
-   [Windows SSE 與 SSE2](#windows-sse-versus-sse2)
-   [常式變數](#routine-variants)
-   [平臺不一致](#platform-inconsistencies)
-   [平臺特定的擴充功能](#platform-specific-extensions)
-   [相關主題](#related-topics)

## <a name="calling-conventions"></a>呼叫慣例

若要增強可攜性並將資料版面配置優化，您必須針對 DirectXMath 程式庫所支援的每個平臺使用適當的呼叫慣例。 具體而言，當您傳遞 [**XMVECTOR**](xmvector-data-type.md) 物件做為參數（定義為在16位元組界限上對齊）時，會有不同的呼叫需求集合，視目標平臺而定：

**適用于32位 Windows**

針對32位的 Windows，有兩個呼叫慣例可用來有效率地傳遞 [ \_ \_ m128](/cpp/cpp/m128)值， (可在該平臺) 上執行 [**XMVECTOR**](xmvector-data-type.md) 。 標準是 [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall)，它可以傳遞前三個 [ \_ \_ m128](/cpp/cpp/m128)值 (**XMVECTOR** 實例，) 為 *SSE/SSE2* 登錄中函式的引數。 [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall)會透過堆疊傳遞其餘的引數。

較新的 Microsoft Visual Studio 編譯器支援新的呼叫慣例 \_ \_ vectorcall，最多可傳遞六個 [ \_ \_ m128](/cpp/cpp/m128)值 ([**XMVECTOR**](xmvector-data-type.md)實例) 為 *SSE/SSE2* 暫存器中函式的引數。 如果有足夠的空間，也可以透過 *SSE/SSE2* 暫存器，傳遞異類向量匯總 (也稱為 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) 。

**適用于 Windows 的64位版本**

針對64位的 Windows，有兩個呼叫慣例可用來有效率地傳遞[ \_ \_ m128](/cpp/cpp/m128)值。 標準是[ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall)，它會傳遞堆疊上的所有[ \_ \_ m128](/cpp/cpp/m128)值。

較新的 Visual Studio 編譯器支援 \_ \_ vectorcall 呼叫慣例，其最多可傳遞六個 [ \_ \_ m128](/cpp/cpp/m128)值 ([**XMVECTOR**](xmvector-data-type.md)實例) 為 *SSE/SSE2* 登錄中函式的引數。 如果有足夠的空間，也可以透過 *SSE/SSE2* 暫存器，傳遞異類向量匯總 (也稱為 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) 。

**適用于 ARM 上的 Windows**

ARM 上的 Windows & ARM64 支援將前四個 \_ \_ n128 值傳遞 ([**XMVECTOR**](xmvector-data-type.md)實例) 在註冊中。

**DirectXMath 解決方案**

**FXMVECTOR**、 **GXMVECTOR**、 **HXMVECTOR** 和 **CXMVECTOR** 別名都支援下列慣例：

-   使用 **FXMVECTOR** 別名最多可傳遞給 [**XMVECTOR**](xmvector-data-type.md) 的前三個實例，做為函式的引數。
-   使用 **GXMVECTOR** 別名，將做為引數之 [**XMVECTOR**](xmvector-data-type.md) 的第四個實例傳遞至函式。
-   使用 **HXMVECTOR** 別名來傳遞 [**XMVECTOR**](xmvector-data-type.md) 的第5和第6個實例，做為函數的引數。 如需其他考慮的詳細資訊，請參閱 \_ \_ vectorcall 檔。
-   使用 **CXMVECTOR** 別名來傳遞任何進一步的 [**XMVECTOR**](xmvector-data-type.md) 實例，做為引數使用。

> [!Note]  
> 針對輸出參數，請一律使用 XMVECTOR \* 或 XMVECTOR&，並根據先前的輸入參數規則來忽略它們。

 

由於 vectorcall 的限制 \_ \_ ，我們建議您不要針對 c + + 函式使用 **GXMVECTOR** 或 **HXMVECTOR** 。 您只需針對前三個 [**XMVECTOR**](xmvector-data-type.md)值使用 **FXMVECTOR** ，然後將 **CXMVECTOR** 用於其餘部分。

**FXMMATRIX** 和 **CXMMATRIX** 別名有助於支援利用 vectorcall 傳遞的 HVA 引數 \_ \_ 。

-   使用 **FXMMATRIX** 別名，將第一個 [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) 做為引數傳遞至函式。 這假設您沒有兩個以上的 **FXMVECTOR** 引數，或兩個以上的 float、Double 或 **FXMVECTOR** 引數指向矩陣的 ' right '。 如需其他考慮的詳細資訊，請參閱 \_ \_ vectorcall 檔。
-   請使用 **CXMMATRIX** 別名，否則為。

由於 vectorcall 的限制 \_ \_ ，我們建議您不要針對 c + + 函式使用 **FXMMATRIX** 。 只需使用 **CXMMATRIX**。

除了類型別名，您也必須使用 XM CALLCONV 注釋，以確定函式會根據 \_ 您的編譯器和架構，使用適當的呼叫慣例 (\_ \_ fastcall 和 \_ \_ vectorcall) 。 由於 vectorcall 的限制 \_ \_ ，我們建議您不要 \_ 針對 c + + 函式使用 XM CALLCONV。

以下是說明此慣例的範例聲明：


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



為了支援這些呼叫慣例，這些類型的別名定義如下 (參數必須以傳值方式傳遞給編譯器，以將其視為內建的傳遞) ：

**適用于32位 Windows 應用程式**

當您使用 \_ \_ fastcall 時：


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



當您使用 \_ \_ vectorcall 時：


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**適用于64位原生 Windows 應用程式**

當您使用 \_ \_ fastcall 時：


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



當您使用 \_ \_ vectorcall 時：


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**ARM 上的 Windows**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> 雖然所有的函式都是以內嵌方式宣告，而且在許多情況下，編譯器不需要使用這些函式的呼叫慣例，但在某些情況下，編譯器可能會決定不內嵌函式，而在這些情況下，我們希望每個平臺都能有最佳的呼叫慣例。

 

## <a name="graphics-library-type-equivalence"></a>圖形程式庫類型等價

為了支援使用 DirectXMath 程式庫，許多 DirectXMath 程式庫類型和結構都相當於 **D3DDECLTYPE** 和 **D3DFORMAT** 類型的 Windows 實作為，以及 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 類型。

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | DXGI \_ 格式                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | DXGI \_ 格式 \_ R8G8 \_ 聖                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (僅限 Xbox)                                                         | D3DFMT \_ x8x8x8x8                                              | DXGI \_ 格式 \_ x8x8x8x8 \_ 聖                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | DXGI \_ 格式 \_ R8G8 \_ SNORM                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (僅限 Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | DXGI \_ 格式 \_ x8x8x8x8 \_ SNORM                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM (DXGI 1.1 +)                                                                                                                                                                |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (僅限 Xbox)                                                          | D3DDECLTYPE \_ DEC3 (僅限 Xbox)                                  |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (僅限 Xbox)                                                         | D3DDECLTYPE \_ DEC3N (僅限 Xbox)                                 |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ 格式 \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ 格式 \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ 格式 \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ 格式 \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | DXGI \_ 格式 \_ R11G11B10 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | DXGI \_ 格式 \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | DXGI \_ 格式 \_ R16G16 \_ FLOAT                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | DXGI \_ 格式 \_ R32G32 \_ 聖                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | DXGI \_ 格式 \_ R32G32B32 \_ 聖                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | DXGI \_ 格式 \_ R32G32B32A32 \_ 聖                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | DXGI \_ 格式 \_ R16G16 \_ 聖                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | DXGI \_ 格式 \_ R16G16 \_ SNORM                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | DXGI \_ 格式 \_ R16G16B16A16 \_ 聖                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | DXGI \_ 格式 \_ R8G8 \_ UINT                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8、D3DFMT \_ A8L8                                    | DXGI \_ 格式 \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | DXGI \_ 格式 \_ R32G32 \_ UINT                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | DXGI \_ 格式 \_ R32G32B32 \_ UINT                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | DXGI \_ 格式 \_ R32G32B32A32 \_ UINT                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5、D3DFMT \_ A1R5G5B5                            | DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | DXGI \_ 格式 \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI \_ 格式 \_ x8x8x8x8 \_ UINT                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI \_ 格式 \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM (使用 [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) 和 [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)。 ) <br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (僅限 Xbox) <br/> D3DDECLTYPE \_ UDEC3 (僅限 Xbox) <br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ 格式 \_ R10G10B10A2 \_ UINT                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (僅限 Xbox) <br/> D3DDECLTYPE \_ UDEC3N (僅限 Xbox) <br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4、D3DFMT \_ X4R4G4B4                            | DXGI \_ 格式 \_ B4G4R4A4 \_ UNORM (DXGI 1.2 +)                                                                                                                                                                |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | DXGI \_ 格式 \_ R16G16 \_ UINT                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI \_ 格式 \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (僅限 Xbox)                                                       | D3DFMT \_ x16x16x16x16                                          | DXGI \_ 格式 \_ R16G16B16A16 \_ UINT                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>DirectXMath 程式庫中的全域常數

為了減少資料區段的大小，DirectXMath 程式庫會使用 [XMGLOBALCONST](xmglobalconst.md) 宏來利用其實值中的一些全域內部常數。 依照慣例，這類內部全域常數前面會加上 **g \_ XM**。 一般而言，它們是下列其中一種類型： [**XMVECTORU32**](xmvectoru32-data-type.md)、 [**XMVECTORF32**](xmvectorf32-data-type.md)或 **XMVECTORI32**。

這些內部全域常數可能會在未來的 DirectXMath 程式庫修訂中變更。 使用可封裝常數的公用函式（可能的話），而不是直接使用 **g \_ XM** 全域值。 您也可以使用 [XMGLOBALCONST](xmglobalconst.md)宣告您自己的全域常數。

## <a name="windows-sse-versus-sse2"></a>Windows SSE 與 SSE2

SSE 指令集僅提供單精確度浮點向量的支援。 DirectXMath 必須利用 SSE2 指令集來提供整數向量支援。 自 Pentium 4、所有 AMD K8 和更新版本的處理器，以及所有 x64 支援的處理器推出之後，所有 Intel 處理器都支援 SSE2。

> [!Note]  
> X86 或更新版本的 Windows 8 需要支援 SSE2。 所有版本的 Windows x64 都需要 SSE2 的支援。 ARM/ARM64 上的 Windows 需要 ARM \_ 霓虹燈。

 

## <a name="routine-variants"></a>常式變數

有數種 DirectXMath 函式可讓您更輕鬆地執行您的工作：

-   比較函式，根據較少量的向量比較作業來建立複雜的條件式分支。 這些函式的名稱會以 "R" 結尾，例如 XMVector3InBoundsR。 函數會以 UINT 傳回值或 UINT out 參數傳回比較記錄。 您可以使用 **XMComparision \*** 宏來測試值。
-   在較大型向量陣列上執行批次樣式作業的批次函數。 這些函式的名稱會以 "Stream" 結尾，例如 [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)。 這些函式會在輸入的陣列上操作，而且會產生輸出的陣列。 通常，它們會採用輸入和輸出 stride。
-   評估函式，以執行更快的估計，而不是較慢且更精確的結果。 這些函式的名稱結尾是 "Est"，例如 [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)。 使用估計的品質和效能影響會因平臺而異，但我們建議您針對效能相關的程式碼使用估計變異。

## <a name="platform-inconsistencies"></a>平臺不一致

DirectXMath 程式庫是要用於效能相關的圖形應用程式和遊戲中。 因此，其設計目的是為了在所有支援的平臺上進行正常處理的最佳速度。 界限條件的結果，尤其是產生浮點數特殊的結果，可能會因目標而異。 此行為也將取決於其他執行時間設定，例如 Windows 32 位的非內建函式目標的 x87 控制字組，或 Windows 32 位和64位的 SSE 控制字組。 此外，不同 CPU 廠商之間的界限條件之間會有差異。

請勿在科學或其他應用程式中使用 DirectXMath，其中數位精確度是最重要的。 此外，這項限制會反映在缺少雙或其他延伸精確度計算的支援。

> [!Note]  
> 如果沒有任何內建純量純量 \_ \_ \_ \_ 程式碼路徑，通常會針對合規性撰寫，而不是效能。 它們的界限條件結果也會不同。

 

## <a name="platform-specific-extensions"></a>平臺特定的擴充功能

DirectXMath 程式庫旨在簡化 c + + SIMD 程式設計，為 x86、x64 和 Windows RT 平臺提供絕佳的支援，其使用廣泛支援的內建指示 (SSE2 和 ARM-霓虹燈) 。

不過，在某些情況下，平臺特定的指示可能會有所説明。 由於 DirectXMath 的實現方式，在許多情況下，直接在標準編譯器支援的內建語句中使用 DirectXMath 類型，以及使用 DirectXMath 作為不支援擴充指令之平臺的回溯路徑是很簡單的。

例如，以下是利用 SSE 4.1 點產品指令的簡化範例。 請注意，您必須明確防護程式碼路徑，以避免在執行時間產生不正確指令例外狀況。 確定程式碼路徑有足夠的工作，以證明分支的額外成本、維護多個程式碼路徑的複雜性等等。


```
#include <Windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ...

   return 0;
}
```



如需平臺特定擴充功能的詳細資訊，請參閱：

<dl>

[DirectXMath： SSE、SSE2 和 ARM-霓虹燈](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath： SSE3 和 SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath： SSE 4.1 和 SSE 4。2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath： AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath： F16C 和 FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath： AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath： ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計指南](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
