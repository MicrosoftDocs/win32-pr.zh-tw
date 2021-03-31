---
description: SetRect 函式會建立矩形，CopyRect 函式會建立指定矩形的複本，而 SetRectEmpty 函式會建立空的矩形。
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: 矩形作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318832"
---
# <a name="rectangle-operations"></a>矩形作業

[**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect)函式會建立矩形， [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect)函式會建立指定矩形的複本，而 [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty)函式會建立空的矩形。 空的矩形是任何寬度為零的矩形、零高度或兩者。 [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty)函式會判斷指定的矩形是否為空白。 [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect)函式會判斷兩個矩形是否相同，也就是它們是否具有相同的座標。

[**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect)函式會增加或減少矩形的寬度或高度，或兩者。 它可以新增或移除矩形兩端的寬度;它可以新增或移除矩形頂端和底部的高度。

[**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect)函式會以指定的數量移動矩形。 它會藉由將指定的 x 數量、y 金額或 x 和 y 數量新增至邊角座標來移動矩形。

[**>ptinrect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect)函式會判斷指定的點是否位於指定的矩形內。 如果該點位於左邊或上方，或完全在矩形內，則該點位於矩形內。 如果這個點位於右邊或底部，則不在矩形中。

[**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect)函數會建立新的矩形，這是兩個現有矩形的交集，如下圖所示。

![顯示兩個重迭矩形的圖例，以較深的陰影來指出交集 ](images/csrec-01.png)

[**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect)函式會建立一個新的矩形，其為兩個現有矩形的聯集，如下圖所示。

![兩個重迭矩形的圖例，以較深的陰影表示等位內的區域，但不在任一矩形內](images/csrec-02.png)

如需繪製橢圓形和多邊形之函式的詳細資訊，請參閱 [填滿的圖形](filled-shapes.md)。

 

 



