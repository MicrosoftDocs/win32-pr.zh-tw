---
title: 'D3DX11CreateTextureFromResource 函式 (D3DX11) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用資源函式，然後這些 DirectXTK 程式庫 (runtime) 、CreateXXXTextureFromMemory (其中 XXX 是 DDS 或 WIC) DirectXTex 程式庫 (工具) 、LoadFromXXXMemory (，其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲的常見藝術來源格式) 然後 CreateTexture 從另一個資源建立紋理。
ms.assetid: 2b62239a-c19b-4d4f-9fd2-afcd87ba0fac
keywords:
- D3DX11CreateTextureFromResource 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bea89fe4f8bf6632ada9461b048195335c72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196372"
---
# <a name="d3dx11createtexturefromresource-function"></a>D3DX11CreateTextureFromResource 函式

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

> [!Note]  
> 我們建議您不要使用此函式，而是使用 [資源](/windows/desktop/menurc/resources-functions)函式，如下所示：
>
> -   [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 (runtime) 、 **CreateXXXTextureFromMemory** (，其中 XXX 是 DDS 或 WIC) 
> -   [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 **CreateTexture**

 

建立另一個資源的材質。

## <a name="syntax"></a>語法


```C++
HRESULT D3DX11CreateTextureFromResource(
  _In_  ID3D11Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevice* \[在\]
</dt> <dd>

類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

裝置的指標 (查看將使用該資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 。

</dd> <dt>

*hSrcModule* \[在\]
</dt> <dd>

類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**

來源資源的控制碼。 您可以使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。

</dd> <dt>

*pSrcResource* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

包含來源資源名稱的字串。 如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。 否則，資料型別會解析為 LPCSTR。

</dd> <dt>

*pLoadInfo* \[在\]
</dt> <dd>

類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***

選擇性。 識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。

</dd> <dt>

*pPump* \[在\]
</dt> <dd>

類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。 如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。

</dd> <dt>

*ppTexture* \[擴展\]
</dt> <dd>

類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***

材質資源指標的位址 (參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)) 。

</dd> <dt>

*pHResult* \[擴展\]
</dt> <dd>

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

傳回值的指標。 可能是 **Null**。 如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX11。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX11 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 函式](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

