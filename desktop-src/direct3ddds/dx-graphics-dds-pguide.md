---
title: DDS 程式設計指南
description: Direct3D 會實行用來儲存未壓縮或壓縮 (DXTn) 材質的 DDS 檔案格式。
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc1f8b9b84c2dc1f9236c79c320ae75848834ef2183db55b189f6b9d340d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796718"
---
# <a name="programming-guide-for-dds"></a>DDS 程式設計指南

Direct3D 會實行用來儲存未壓縮或壓縮 (DXTn) 材質的 DDS 檔案格式。 檔案格式會執行幾個稍微不同的類型，其設計目的是為了儲存不同類型的資料，並支援在 Direct3D 10/11) 中 (單一層紋理、具有 mipmap 的材質、cube 地圖、磁片區地圖和材質陣列。 本節說明 DDS 檔案的版面配置。

如需在 Direct3D 11 中建立材質的說明，請參閱 [如何：建立材質](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create)。 如需 Direct3D 9 的說明，請參閱 [D3DX (Direct3D 9) 中的材質支援 ](/windows/desktop/direct3d9/texture-support-in-d3dx)。

-   [DDS 檔案版面配置](#dds-file-layout)
-   [DDS 變數](#dds-variants)
-   [使用 Direct3D 10/11 中的材質陣列](#using-texture-arrays-in-direct3d-1011)
-   [常見的 DDS 檔案資源格式和相關聯的標頭內容](#common-dds-file-resource-formats-and-associated-header-content)
-   [相關主題](#related-topics)

## <a name="dds-file-layout"></a>DDS 檔案版面配置

DDS 檔案是包含下列資訊的二進位檔案：

-   包含四個字元的代碼值 'DDS ' (0x20534444) 的 DWORD (魔術數字)。

-   檔案中的資料描述。

    資料是以使用 [**dds \_ 標頭**](dds-header.md)的標頭描述來描述，而像素格式則是使用 [**dds \_ PIXELFORMAT**](dds-pixelformat.md)來定義。 請注意， **dds \_ 標頭** 和 **dds \_ PIXELFORMAT** 結構會取代已被取代的 DDSURFACEDESC2、DDSCAPS2 和 DDPIXELFORMAT DirectDraw 7 結構。 **DDS \_標頭** 是 DDSURFACEDESC2 和 DDSCAPS2 的二進位對等專案。 **DDS \_PIXELFORMAT** 是 DDPIXELFORMAT 的二進位對等專案。

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    如果 [DDS \_ PIXELFORMAT dwFlags] 設定為 [DDPF \_ FOURCC]，而 [dwFourCC] 設定為 "DX10"，則會出現額外的 [**DDS \_ 標頭 \_ DXT10**](dds-header-dxt10.md) 結構，以容納無法以 RGB 像素格式表示的材質陣列或 DXGI 格式，例如浮點數格式、sRGB 格式等等。當 **DDS \_ 標頭 \_ DXT10** 結構存在時，整個資料描述看起來會像這樣。

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   包含主要表面資料的位元組陣列指標。
    ```
    BYTE bdata[]
    ```

    

-   包含其餘的表面 (如 Mipmap 層級、立方體貼圖中的面及容積紋理中的深度) 的位元組陣列指標。 請點選下列連結，以了解下列的 DDS 檔案配置相關資訊：[紋理](dds-file-layout-for-textures.md)、[立方體貼圖](dds-file-layout-for-cubic-environment-maps.md)或[容積紋理](dds-file-layout-for-volume-textures.md)。

    ```
    BYTE bdata2[]
    ```

    

如需廣泛的硬體支援，建議您使用 [**dxgi \_ 格式 \_ R8G8B8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、 [**dxgi \_ format \_ R8G8B8A8 \_ UNORM \_ SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、 [**dxgi \_ format \_ R8G8B8A8 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、 [**dxgi \_ format \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、 [**dxgi \_ format \_ R16G16 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、 [**dxgi \_ format \_ R8G8 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、dxgi format R8 [**\_ \_ \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)、dxgi format BC1 UNORM、dxgi format BC1 UNORM、dxgi format BC2 UNORM、dxgi format BC2 UNORM、dxgi format BC3 UNORM、dxgi format BC3 UNORM 或 [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**dxgi \_ format \_ \_ \_ srgb**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)格式。 [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

如需有關壓縮材質格式的詳細資訊，請參閱 [direct3d 11 中的材質區塊壓縮](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) 和 [ (Direct3D 10) 的區塊壓縮 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)。

D3DX 程式庫 (例如 D3DX11 .lib) 和其他類似的程式庫 unreliably 或不一致地提供 [**DDS \_ 標頭**](dds-header.md)結構 **dwPitchOrLinearSize** 成員中的音調值。 因此，當您讀取和寫入 DDS 檔案時，建議您以下列其中一種方式來計算指定格式的音調：

-   針對區塊壓縮格式，請將音調計算為：

    最大 ( 1、 ( (寬度 + 3) /4) ) \* 區塊大小

    區塊大小為8個位元組，適用于 DXT1、BC1 和 BC4 格式，以及16個位元組適用于其他區塊壓縮格式。

-   若為 R8G8 \_ B8G8、G8R8 \_ G8B8、舊版 UYVY 封裝和舊版 YUY2 封裝格式，請將此音調計算為：

     ( (寬度 + 1)  >> 1) \* 4

-   針對其他格式，請以下列方式計算推銷：

     ( 寬度 \* 位-每圖元 + 7 ) /8

    您可以除以8以進行位元組對齊。

> [!Note]  
> 您計算的音調值不一定等於執行時間所提供的音調，這在某些情況下為 DWORD 對齊，而在其他情況下則為位元組對齊。 因此，建議您一次複製一段掃描行，而不是嘗試將整個影像複製到一個複本。

 

## <a name="dds-variants"></a>DDS 變數

有許多工具可建立和取用 DDS 檔案，但它們在標頭中所需內容的詳細資料中可能會有所不同。 寫入器應該盡可能地填入標頭，而讀取器應該檢查最大的值，以獲得最大的相容性。 若要驗證 DDS 檔案，讀取器應確定檔案的長度至少為128個位元組，以容納魔術值和基本標頭、魔術值為 0x20534444 ( "DDS" ) 、DDS \_ 標頭大小為124，而 \_ 標頭大小中的 DDS PIXELFORMAT 為32。 如果 [DDS \_ PIXELFORMAT dwFlags] 設定為 [DDPF FOURCC]， \_ 而 dwFourCC 設定為 "DX10"，則檔案大小總計必須至少為148個位元組。

有一些常用的變化，其中的像素格式設定為 DDPF \_ FOURCC 程式碼，其中 dwFourCC 設定為 D3DFORMAT 或 DXGI \_ 格式的列舉值。 沒有任何方法可分辨列舉值是否為 D3DFORMAT 或 DXGI \_ 格式，因此強烈建議您改為使用 "DX10" 擴充功能和 DDS \_ 標頭 \_ DXT10 標頭，以在基本的 DDS \_ PIXELFORMAT 無法表示格式時儲存 dxgiFormat。

標準的 DDS \_ PIXELFORMAT 最好要有最大的相容性，以儲存 RGB 未壓縮資料和 DXT1-5 資料，因為並非所有的 DDS 工具都支援 DX10 延伸模組。

## <a name="using-texture-arrays-in-direct3d-1011"></a>使用 Direct3D 10/11 中的材質陣列

在 Direct3D 10/11 中 ([**dds \_ 標頭**](dds-header.md) 和 [**dds \_ 標頭 \_ DXT10**](dds-header-dxt10.md)) 的新 dds 結構會擴充 DDS 檔案格式，以支援材質的陣列，這是 direct3d 10/11 中的新資源類型。 以下是一些範例程式碼，示範如何使用新的標頭來存取材質陣列中不同的 mipmap 層級。


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>常見的 DDS 檔案資源格式和相關聯的標頭內容



| 資源格式                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | DDS \_ RGBA      | 32            | 0xff       | 0xff00     | 0xff0000   | 0xff000000 |
| DXGI \_ 格式 \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGBA      | 32            | 0xffff     | 0xffff0000 |            |            |
| \*\*<br/> DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | DDS \_ RGBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| DXGI \_ 格式 \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGB       | 32            | 0xffff     | 0xffff0000 |            |            |
| DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | DDS \_ RGBA      | 16            | 0x7c00     | 0x3e0      | 0x1f       | 0x8000     |
| DXGI \_ 格式 \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RGB       | 16            | 0xf800     | 0x7e0      | 0x1f       |            |
| DXGI \_ A8 \_ UNORM<br/> D3DFMT \_ A8<br/>                                           | DDS \_ ALPHA     | 8             |            |            |            | 0xff       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | DDS \_ RGBA      | 32            | 0xff0000   | 0xff00     | 0xff       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RGB       | 32            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RGB       | 32            | 0xff       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | DDS \_ RGBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RGB       | 24            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1f       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | DDS \_ RGBA      | 16            | 0xf00      | 0xf0       | 0xf        | 0xf000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RGB       | 16            | 0xf00      | 0xf0       | 0xf        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | DDS \_ RGBA      | 16            | 0xe0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | DDS \_ 亮度 | 16            | 0xff       |            |            | 0xff00     |
| D3DFMT \_ l16 也<br/>                                                                     | DDS \_ 亮度 | 16            | 0xffff     |            |            |            |
| D3DFMT 的 \_ L8<br/>                                                                      | DDS \_ 亮度 | 8             | 0xff       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | DDS \_ 亮度 | 8             | 0xf        |            |            | 0xf0       |



 



| 資源格式                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| DXGI \_ 格式 \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | DDS \_ FOURCC | DXT1   |
| DXGI \_ 格式 \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | DDS \_ FOURCC | "DXT3"   |
| DXGI \_ 格式 \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | DDS \_ FOURCC | DXT5   |
| \*<br/> DXGI \_ 格式 \_ BC4 \_ UNORM<br/>                                           | DDS \_ FOURCC | "BC4U"   |
| \*<br/> DXGI \_ 格式 \_ BC4 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC4S"   |
| \*<br/> DXGI \_ 格式 \_ BC5 \_ UNORM<br/>                                           | DDS \_ FOURCC | "ATI2"   |
| \*<br/> DXGI \_ 格式 \_ BC5 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC5S"   |
| DXGI \_ 格式 \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FOURCC | "RGBG"   |
| DXGI \_ 格式 \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FOURCC | "GRGB"   |
| \*<br/> DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FOURCC | 36       |
| \*<br/> DXGI \_ 格式 \_ R16G16B16A16 \_ SNORM<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FOURCC | 110      |
| \*<br/> DXGI \_ 格式 \_ R16 \_ FLOAT<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FOURCC | 111      |
| \*<br/> DXGI \_ 格式 \_ R16G16 \_ FLOAT<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FOURCC | 112      |
| \*<br/> DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FOURCC | 113      |
| \*<br/> DXGI \_ 格式 \_ R32 \_ FLOAT<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FOURCC | 114      |
| \*<br/> DXGI \_ 格式 \_ R32G32 \_ FLOAT<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FOURCC | 115      |
| \*<br/> DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FOURCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FOURCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FOURCC | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | DDS \_ FOURCC | UYVY   |
| D3DFMT \_ YUY2<br/>                                                                     | DDS \_ FOURCC | YUY2   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FOURCC | 117      |
| 任何 DXGI 格式                                                                             | DDS \_ FOURCC | DX10   |



 

\* = 穩固的 DDS 讀取器必須能夠處理這些舊版的格式代碼。 不過，這類 DDS 讀取器在寫入這些格式代碼時，應該偏好使用 "DX10" 標頭延伸模組，以避免混淆。

\*\* = 由於通常會在 DDS 讀取器和寫入器的常見實值中出現一些長期問題，因此寫出10:10:10:2 型別資料的最穩固方式是使用 "DX10" 標頭延伸模組搭配 [**dxgi \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 代碼 "24" (也就是 dxgi \_ format \_ R10G10B10A2 \_ UNORM 值) 。 D3DFMT \_ A2R10G10B10 資料應轉換成10:10:10:2 類型的資料，再以 DXGI \_ 格式寫入 \_ R10G10B10A2 \_ UNORM 格式的 DDS 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DDS](dx-graphics-dds.md)
</dt> </dl>

 

