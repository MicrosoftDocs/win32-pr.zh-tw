---
description: 在應用程式建立顯示器或印表機 DC 之後，它就可以在相關聯的裝置上開始繪圖，或者，如果是記憶體 DC，則可以開始在儲存在記憶體中的點陣圖上進行繪製。
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: 繪圖物件上的作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ae7467e04f53196c839b6daa72482ab73845c3185208eb3cb886cb0ce6a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965618"
---
# <a name="operations-on-graphic-objects"></a>繪圖物件上的作業

在應用程式建立顯示器或印表機 DC 之後，它就可以在相關聯的裝置上開始繪圖，或者，如果是記憶體 DC，則可以開始在儲存在記憶體中的點陣圖上進行繪製。 不過，在開始繪製之前，有時候繪圖正在進行中時，通常需要將預設物件取代為新的物件。

應用程式可以藉由呼叫 [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) 和 [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) 函數來檢查預設物件的屬性。 **GetCurrentObject** 函式會傳回識別目前畫筆、筆刷、調色板、點陣圖或字型的控制碼，而 **GetObject** 函式會將包含該物件之屬性的結構初始化。

某些印表機會提供可用來改善應用程式繪圖速度的內建畫筆、筆刷和字型。 您可以使用兩個函數來列舉這些物件： [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) 和 [**>enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)。 如果應用程式必須列舉常駐畫筆或筆刷，則可以呼叫 **EnumObjects** 函數來檢查對應的屬性。 如果應用程式必須列舉常駐字型，則可以呼叫 **>enumfontfamilies** 函式 (也可以) 的 GDI 字型。

一旦應用程式判斷出預設物件需要取代之後，它會呼叫下列其中一項建立函式來建立新的物件。



| 繪圖物件 | 函數                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 點陣圖         | [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)、 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)、 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)、 [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)、 [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| 筆刷          | [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)、 [**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)、 [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt)、 [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)、 [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)、 [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| 調色盤  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| 字型           | [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)、 [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| 手寫筆            | [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)、 [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| 區域         | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)、 [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)、 [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)、 [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)、 [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)、 [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)、 [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

這些函式每一個都會傳回識別新物件的控制碼。 在應用程式抓取控制碼之後，它必須呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式來取代預設的物件。 但是，應用程式應該儲存識別預設物件的控制碼，並在不再需要時，使用這個控制碼來取代新的物件。 當應用程式使用新的物件完成繪圖時，必須藉由呼叫 **SelectObject** 函式來還原預設物件，然後藉由呼叫 [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) 函數來刪除新的物件。 無法刪除物件會導致嚴重的效能問題。

 

 



