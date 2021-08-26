---
description: 下列函式會搭配色彩使用。
ms.assetid: 9dd32d4a-30bd-406f-a934-bb71ad4ca2cb
title: 色彩函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef9e233e5376718ac983982fd3f06e9fcd6c6fc5843d4a32d685fe64bbc1af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966308"
---
# <a name="color-functions"></a>色彩函數

下列函式會搭配色彩使用。



| 函式                                                   | 描述                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette)                   | 取代指定之邏輯調色板中的專案。                                                                                                    |
| [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette)     | 為指定的裝置內容建立半色調調色板， (DC) 。                                                                                     |
| [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                     | 建立邏輯調色板。                                                                                                                            |
| [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment)           | 抓取指定之 DC 的色彩調整值。                                                                                           |
| [**GetNearestColor**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestcolor)                 | 從系統選擇區中，抓取用來識別色彩的色彩值，該色彩會在使用指定的色彩值時顯示。                    |
| [**GetNearestPaletteIndex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex)   | 抓取指定的邏輯調色板中，專案的索引，最符合指定的色彩值。                                     |
| [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries)             | 從指定的邏輯調色板抓取指定的元件專案範圍。                                                                        |
| [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) | 從與指定的 DC 相關聯的系統選擇區中，抓取元件專案的範圍。                                                |
| [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse)         | 針對指定的 DC，抓取系統 (實體) 元件的目前狀態。                                                                    |
| [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette)                   | 從目前的邏輯選擇區，將調色板專案地圖到系統調色板。                                                                          |
| [**ResizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette)                     | 根據指定值來增加或減少邏輯調色盤 (Palette) 的大小。                                                                    |
| [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette)                     | 在裝置內容中選取指定的邏輯調色板。                                                                                          |
| [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment)           | 使用指定的值，設定 DC 的色彩調整值。                                                                                 |
| [**SetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries)             | 將 RGB (紅色、綠色、藍色) 色彩值，以及邏輯調色板中某個專案範圍內的旗標。                                                        |
| [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse)         | 允許應用程式指定系統調色板是否包含2或20個靜態色彩。                                                           |
| [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject)                 | 重設筆刷的原點，或重設邏輯調色板。                                                                                             |
| [**UpdateColors**](/windows/desktop/api/Wingdi/nf-wingdi-updatecolors)                       | 藉由將工作區中目前的色彩重新對應到目前實現的邏輯調色板，以更新指定之裝置內容的工作區。 |



 

 

 



