---
description: CImageDisplay 類別是 GDI 影片轉譯器的 helper 類別，可管理顯示格式。
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: 'CImageDisplay 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 551650e7c8b6b0f830a84aee37bf671bbc300224c9e300a3f6f841ef503a504d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428940"
---
# <a name="cimagedisplay-class"></a>CImageDisplay 類別

![cimagedisplayclasshierarchy](images/wutil06.png)

`CImageDisplay`類別是 GDI 影片轉譯器的 helper 類別，可管理顯示格式。 物件會儲存描述目前顯示模式的 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構，此模式是在物件的「函式」方法中初始化。 物件的 **CheckMediaType** 方法會檢查建議的媒體類型是否可以使用 GDI 有效率地呈現。



| 受保護的成員變數                                       | 描述                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ 顯示**](cimagedisplay-m-display.md)                    | 描述目前顯示格式的 **VIDEOINFO** 結構。                     |
| 保護方法                                                | 描述                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | 驗證 **VIDEOINFO** 結構中的色遮罩。                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | 計算指定位欄位開頭的零位位數。              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | 傳回在指定位欄位中設定為1的位數目。                          |
| 公用方法                                                   | 描述                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | 驗證 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | 判斷建議的媒體類型是否與顯示格式相容。        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | 驗證 **VIDEOINFO** 結構中的調色板專案。                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | 檢查指定的 **VIDEOINFO** 格式是否與顯示格式相容。 |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | 函式方法。                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | 抓取指定 **VIDEOINFO** 格式的色彩遮罩。                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | 抓取目前顯示格式的色彩遮罩。                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | 抓取目前顯示模式的位深度。                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | 抓取描述目前顯示模式的影片格式。                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Retermines，指出目前的顯示格式是否為調色盤。                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | 更新物件的影片格式以符合指定的顯示                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




