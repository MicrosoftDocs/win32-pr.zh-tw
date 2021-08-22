---
description: 若要建立點陣圖，請使用 CreateBitmap、CreateBitmapIndirect 或 CreateCompatibleBitmap 函數、CreateDIBitmap 和 CreateDiscardableBitmap。
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: 點陣圖建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038256"
---
# <a name="bitmap-creation"></a>點陣圖建立

若要建立點陣圖，請使用 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)、 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)或 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 函數、 [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)和 [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)。

這些函數可讓您指定點陣圖的寬度和高度（以圖元為單位）。 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)和 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)函式也可讓您指定色彩平面的數目，以及用來識別色彩所需的位數。 另一方面， [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 和 [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) 函式會使用指定的裝置內容，來取得色彩平面的數目和識別色彩所需的位數。

[**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)函式會從與裝置無關的點陣圖建立裝置相依點陣圖。 它包含描述圖元值如何對應至 RGB 色彩值的色彩表。 如需詳細資訊，請參閱 [裝置相關點陣圖](device-dependent-bitmaps.md) 和與 [裝置無關的點陣圖](device-independent-bitmaps.md)。

建立點陣圖之後，您就無法變更其大小、色彩平面的數目或識別色彩所需的位數。

當您不再需要點陣圖時，請呼叫 [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) 函數來刪除它。

 

 



