---
description: 下列子類型會定義無 Alpha 通道的未壓縮 RGB 格式。
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: '未壓縮的 RGB 影片子類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e04237a61fa91f4fe648dcb7743c893604adbe7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991159"
---
# <a name="uncompressed-rgb-video-subtypes"></a>未壓縮的 RGB 影片子類型

下列子類型會定義無 Alpha 通道的未壓縮 RGB 格式。



| 常數                                                                                                                                                                        | 描述                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RGB，每圖元1位 (bpp) ，調色盤<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RGB、4 bpp、調色盤<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RGB、8 bpp、調色盤<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555、16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565、16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ RGB24**</dt> </dl>    | RGB，24 bpp<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB、32 bpp<br/>                            |



下列子類型會定義使用 Alpha 色板的未壓縮 RGB 格式。



| 常數                                                                                                                                                                                       | 描述                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | 具有 Alpha 通道的 RGB 555<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | 具有 Alpha 通道的 RGB 32<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | 具有 Alpha 通道的16位 RGB;每個通道4個位<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | 使用 Alpha 通道的32位 RGB;每個 RGB 通道10個位加上 Alpha 的2位。<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | 使用 Alpha 通道的32位 BGR;每個 BGR 通道10個位加上 Alpha 的2位。<br/> |



## <a name="remarks"></a>備註

針對調色盤格式，會將每個圖元的色彩指定為調色板中的索引。 在 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構後面的格式區塊中必須包含此調色板。 若為非調色盤格式，則會直接指定每個圖元的色彩;記憶體配置取決於位深度：

-   RGB 555 使用下列記憶體配置：
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   RGB 565 使用下列記憶體配置：
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   針對 RGB 24，每個圖元都是 [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple)。 每個色彩都是一個位元組，其值介於0到255（含）之間。 記憶體配置為： 

    |       |      |       |     |
    |-------|------|-------|-----|
    | Byte  | 0    | 1     | 2   |
    | 值 | 藍色 | 綠色 | 紅色 |

    

     

-   針對 RGB 32，每個圖元都是 **RGBQUAD**。 每個色彩都是一個位元組，其值介於0到255（含）之間。 記憶體配置為： 

    |       |      |       |     |                     |
    |-------|------|-------|-----|---------------------|
    | Byte  | 0    | 1     | 2   | 3                   |
    | 值 | 藍色 | 綠色 | 紅色 | Alpha 或不在意 |

    

     

    如果子類型為 MEDIASUBTYPE \_ ARGB32，則 byte 3 會包含 Alpha 色板的值。 如果子類型為 MEDIASUBTYPE \_ RGB32，則應忽略 byte 3。

-   A2R10G10B10 會使用下列配置： 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | 值 | 藍色  | 綠色   | 紅色     | Alpha   |

    

     

-   A2B10G10R10 會使用下列配置： 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | 值 | 紅色   | 綠色   | 藍色    | Alpha   |

    

     

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片子類型](video-subtypes.md)
</dt> <dt>

[使用影片畫面](working-with-video-frames.md)
</dt> </dl>

 

 
