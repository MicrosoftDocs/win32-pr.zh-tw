---
title: 使用 GDI 函數搭配 WCS
description: 圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- 'Windows色彩系統 (WCS) 、圖形裝置介面 (GDI) '
- 'WCS (Windows 色彩系統) 、圖形裝置介面 (GDI) '
- '影像色彩管理、圖形裝置介面 (GDI) '
- '色彩管理、圖形裝置介面 (GDI) '
- '色彩、圖形裝置介面 (GDI) '
- " (GDI) 的圖形裝置介面"
- 'GDI (圖形裝置介面) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a104378ae46e6b9519d6f795d280d45c28c8fa3fdc7d1e34aae609bcdbd195d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444675"
---
# <a name="using-gdi-functions-with-wcs"></a>使用 GDI 函數搭配 WCS

圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。 有些會啟用以搭配 WCS 使用，有些則否。 下列 GDI 函數與 ICM 有關：

-   [使用 WCS 的裝置內容函式](#device-context-functions-with-wcs)
-   [使用 WCS 的畫筆和筆刷函數](#pen-and-brush-functions-with-wcs)
-   [使用 WCS 的文字輸出函數](#text-output-functions-with-wcs)
-   [具有 WCS 的 Bitmap 函數](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a>使用 WCS 的裝置內容函式



|    函式                |   描述                                                                                                                                                                                                                              |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateCompatibleDC | 如果已針對 ICM 啟用透過其 hdc 參數傳遞給此函式的裝置內容 (dc) ，則函式所建立的 dc 也會 ICM 啟用。 來源和目的色彩空間會在 DC 中指定。 |
| CreateDC           | 藉由將 pInitData 參數所指向的 DEVMODE 結構 dmICMMethod 成員設定為適當的值，就可以啟用 ICM。 如需詳細資訊，請參閱 DEVMODE 結構上 Platform SDK 中的檔。  |
| ResetDC            | 根據 lpInitData 參數所指定的 DEVMODE 結構中的資訊，將會重設 hdc 參數所指定之裝置內容的色彩設定檔。                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a>使用 WCS 的畫筆和筆刷函數



|    函式                |   描述                                                                                                                                                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| 筆刷函數 | 建立筆刷時，不會進行任何色彩管理。 不過，在將筆刷選取到已啟用 ICM 的 DC 中時，將會執行色彩管理。 |
| CreatePen       | 建立畫筆時，不會進行任何色彩管理。 不過，在將筆刷選取到已啟用 ICM 的 DC 中時，將會執行色彩管理。   |
| ExtCreatePen    | 建立畫筆時，不會進行任何色彩管理。 不過，在將筆刷選取到已啟用 ICM 的 DC 中時，將會執行色彩管理。   |
| SelectObject    | 如果選取的物件是筆刷或畫筆，則會執行色彩管理。                                                              |
| SetDCBrushColor | 如果啟用 WCS，則會執行色彩管理。                                                                                              |
| SetDCPenColor   | 如果啟用 WCS，則會執行色彩管理。                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a>使用 WCS 的文字輸出函數



|    函式                |   描述                                                                                                                                                                                                                              |
|--------------|--------------------------------------------------|
| SetBkColor   | 如果啟用 WCS，則會執行色彩管理。 |
| SetTextColor | 如果啟用 WCS，則會執行色彩管理。 |



 

## <a name="bitmap-functions-with-wcs"></a>具有 WCS 的 Bitmap 函數



|    函式                |   描述                                                                                                                                                                                                                              |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BitBlt            | 發生 blits 時，不會執行任何色彩管理。                                                                                                                                                                                                                                                                                                                                                                                             |
| CreateDIBitmap    | FuUsage 參數會指定 lpbmi 參數所指向之 BITMAPINFO 結構的 bmiColors 成員，或不包含色彩資訊。 如果沒有，則不會對此點陣圖執行色彩管理。 點陣圖必須使用第4版或第5版的 BITMAPINFO 結構，才能啟用色彩管理。 建立點陣圖之後，所產生點陣圖的內容不符合色彩。 |
| CreateDIBSection  | 如果透過 pbmi 參數傳遞的 BITMAPINFO 結構不是第4版或第5版，就不會進行任何色彩管理。 如果是第4版或第5版，則會啟用色彩管理，並將指定的色彩空間與點陣圖相關聯。                                                                                                                                                                                                   |
| MaskBlt           | 發生 blits 時，不會執行任何色彩管理。                                                                                                                                                                                                                                                                                                                                                                                             |
| SelectObject      | 如果物件是使用 CreateDIBSection 所建立的點陣圖，則會執行色彩管理。 點陣圖的色彩空間會用來做為目的色彩空間。                                                                                                                                                                                                                                                                                       |
| SetDIBits         | 色彩管理的執行。 如果指定的 BITMAPINFO 結構不是第4版或第5版，則會使用目前 DC 的色彩設定檔做為來源色彩空間設定檔。 如果沒有，則會使用 sRGB 空間。 如果指定的 BITMAPINFO 結構為第4版或第5版，則點陣圖標頭中指定的色彩空間設定檔會用來做為來源色彩空間設定檔。                                         |
| SetDIBitsToDevice | 色彩管理的執行。 如果指定的 BITMAPINFO 結構不是第4版或第5版，則會使用目前裝置內容的色彩設定檔做為來源色彩空間設定檔。 如果沒有的話，則會使用 sRGB 色彩空間。 如果指定的 BITMAPINFO 結構為第4版或第5版，則會使用與點陣圖相關聯的色彩空間設定檔做為來源色彩空間。                                    |
| SetDIBColorTable  | 未執行任何色彩管理。                                                                                                                                                                                                                                                                                                                                                                                                              |
| StretchBlt        | 發生 blits 時，不會執行任何色彩管理。                                                                                                                                                                                                                                                                                                                                                                                             |
| StretchDIBits     | 色彩管理的執行。 如果指定的 BITMAPINFO 結構不是第4版或第5版，則會使用目前 DC 的色彩設定檔做為來源色彩空間設定檔。 如果沒有，則會使用 sRGB 空間。 如果指定的 BITMAPINFO 結構為第4版或第5版，則點陣圖標頭中指定的色彩空間設定檔會用來做為來源色彩空間設定檔。                                         |



 

 

 




