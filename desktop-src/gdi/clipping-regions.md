---
description: 裁剪區域是應用程式可在裝置內容 (DC) 中選取的其中一個繪圖物件。
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: 裁剪區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a830e05b2a9ce709183f23fad66f937c8c512acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114713"
---
# <a name="clipping-regions"></a>裁剪區域

裁剪區域是應用程式可在裝置內容 (DC) 中選取的其中一個繪圖物件。 它通常是矩形。 某些裝置內容提供預先定義或預設的裁剪區域，其他則否。 例如，如果您從 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式取得裝置內容控制碼，DC 就會包含預先定義的矩形裁剪區域，該區域會對應至需要重新繪製的無效矩形。 但是，當您藉由呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 函式（使用 **Null**_HWnd_ 參數）或呼叫 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) 函式來取得裝置內容控制碼時，DC 不會包含預設的裁剪區域。 如需 **BeginPaint** 函式所傳回之裝置內容的詳細資訊，請參閱 [繪製和繪製](painting-and-drawing.md) 。 如需 **CreateDC** 和 **GetDC** 函數所傳回之裝置內容的詳細資訊，請參閱 [裝置](device-contexts.md)內容。

應用程式可以在裁剪區域上執行各種作業。 其中有些作業需要識別區域的控制碼，有些則否。 例如，應用程式可以直接在裝置內容的裁剪區域上執行下列作業。

-   藉由將對應的線條、弧線、點陣圖、文字或填滿圖形的座標傳遞給 [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) 函式，來判斷圖形輸出是否出現在區域的框線內。
-   藉由呼叫 [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) 函數，判斷用戶端區域的一部分是否與區域相交。
-   藉由呼叫 [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) 函數，以指定的位移來移動現有的區域。
-   藉由呼叫 [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) 函式，從目前的裁剪區域中排除工作區的矩形部分。
-   藉由呼叫 [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) 函式，將工作區的矩形部分與目前的裁剪區域結合在一起。

取得識別裁剪區域的控制碼之後，應用程式就可以執行與區域共通的任何作業，例如：

-   藉由呼叫 [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) 函數，結合目前裁剪區域的複本與第二個區域。
-   藉由呼叫 [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) 函數，比較目前裁剪區域的複本與第二個區域。
-   藉由呼叫 [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) 函式，判斷某個點是否位在目前裁剪區域的複本內部。

 

 



