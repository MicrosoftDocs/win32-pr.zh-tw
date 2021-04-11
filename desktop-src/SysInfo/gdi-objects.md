---
description: GDI 物件只支援每個物件一個控制碼。 GDI 物件的控制碼對進程而言是私用的。 也就是說，只有建立 GDI 物件的進程可以使用物件控制碼。
ms.assetid: 699de25c-083d-4be3-a997-67418b7173e1
title: GDI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d57d4a1cfa99c392783dec23a090e7ccf09eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027594"
---
# <a name="gdi-objects"></a>GDI 物件

GDI 物件只支援每個物件一個控制碼。 GDI 物件的控制碼對進程而言是私用的。 也就是說，只有建立 GDI 物件的進程可以使用物件控制碼。

每個會話都有65536個 GDI 控制碼的理論限制。 不過，每個會話可以開啟的最大 GDI 控制碼數目通常較低，因為它會受到可用記憶體的影響。

**Windows 2000：** 每個會話有16384個 GDI 控制碼的限制。

另外還有 GDI 控制碼的預設每一進程限制。 若要變更此限制，請設定下列登錄值：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows** \\ **GDIProcessHandleQuota**

這個值可以設定為介於256到65536之間的數位。

**Windows 2000：** 這個值可以設定為介於256到16384之間的數位。

## <a name="managing-gdi-objects"></a>管理 GDI 物件

下表列出 GDI 物件，以及每個物件的建立者和 destroyer 函數。 建立者函式會建立物件和物件控制碼，或只傳回現有的物件控制碼。 Destroyer 函式會從記憶體中移除物件，這樣會使物件控制碼失效。



| GDI 物件           | Creator 函數                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Destroyer 函式                                           |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| 點陣圖               | [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap)、 [**CreateBitmapIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbitmapindirect)、 [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap)、 [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)、 [**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)、 [**CreateDiscardableBitmap**](/windows/desktop/api/wingdi/nf-wingdi-creatediscardablebitmap)                                                                                                                                                                                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                         |
| 筆刷                | [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect)、 [**CreateDIBPatternBrush**](/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush)、 [**CreateDIBPatternBrushPt**](/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt)、 [**CreateHatchBrush**](/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush)、 [**CreatePatternBrush**](/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush)、 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush)                                                                                                                                                                     | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                         |
| DC                   | [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc)、 [ **ReleaseDC**](/windows/desktop/api/winuser/nf-winuser-releasedc) |
| 增強的中繼檔    | [**CreateEnhMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea)                                                                                                                                                                                                                                                                                                                                                                                                                                           | [**DeleteEnhMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile)               |
| 增強型中繼檔 DC | [**CreateEnhMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-createenhmetafilea)                                                                                                                                                                                                                                                                                                                                                                                                                                           | [**CloseEnhMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-closeenhmetafile)                 |
| 字型                 | [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta)、 [ **CreateFontIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                                                                                                                                       | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                         |
| 記憶體 DC            | [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc)                                                                                                                                                                                                                                                                                                                                                                                                                                         | [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc)                                 |
|  中繼檔             | [**CreateMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-createmetafilea)                                                                                                                                                                                                                                                                                                                                                                                                                                                 | [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile)                     |
| 中繼檔 DC          | [**CreateMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-createmetafilea)                                                                                                                                                                                                                                                                                                                                                                                                                                                 | [**CloseMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-closemetafile)                       |
| 調色盤              | [**CreatePalette**](/windows/desktop/api/wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                                                                                                                                                   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                         |
| 畫筆和延伸畫筆 | [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen)、 [**CreatePenIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createpenindirect)、 [**ExtCreatePen**](/windows/desktop/api/wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                                                                                                                                     | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                         |
| 區域               | [**CombineRgn**](/windows/desktop/api/wingdi/nf-wingdi-combinergn)、 [**CreateEllipticRgn**](/windows/desktop/api/wingdi/nf-wingdi-createellipticrgn)、 [**CreateEllipticRgnIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createellipticrgnindirect)、 [**CreatePolygonRgn**](/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn)、 [**CreatePolyPolygonRgn**](/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn)、 [**CreateRectRgn**](/windows/desktop/api/wingdi/nf-wingdi-createrectrgn)、 [**CreateRectRgnIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect)、 [**CreateRoundRectRgn**](/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn)、 [**ExtCreateRegion**](/windows/desktop/api/wingdi/nf-wingdi-extcreateregion)、 [**PathToRegion**](/windows/desktop/api/wingdi/nf-wingdi-pathtoregion) | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                         |



 

 

 
