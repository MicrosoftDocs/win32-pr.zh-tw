---
description: 就像磚可以放在彼此旁以涵蓋樓層一樣，可以將矩形影像放在彼此旁，以填滿圖形) 的 (圖格。
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: 使用影像將圖形平平圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112945"
---
# <a name="tiling-a-shape-with-an-image"></a>使用影像將圖形平平圖

就像磚可以放在彼此旁以涵蓋樓層一樣，可以將矩形影像放在彼此旁，以填滿圖形) 的 (圖格。 若要並排顯示圖形的內部，請使用材質筆刷。 當您建立 [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) 物件時，您傳遞給函式的其中一個引數就是 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件的位址。 當您使用紋理筆刷繪製圖形的內部時，圖形會填入此影像的重複複本。

[**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)物件的 wrap 模式屬性會決定影像的導向方式，因為它會在矩形方格中重複。 您可以讓格線中的所有圖格都有相同的方向，也可以讓影像從一個格線位置切換至下一個。 翻轉可以是水準、垂直或兩者。 下列範例示範如何使用不同類型的翻轉進行平鋪。

## <a name="tiling-an-image"></a>平鋪影像

此範例使用下列75×75影像來磚出200×200矩形：

![此主題中做為其他圖例基底的圖例：在背景上的房屋和樹狀結構，並以矩形為中心](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



下圖顯示矩形如何與影像並排顯示。 請注意，所有圖格都有相同的方向;沒有任何翻轉。

![顯示在大型矩形中以水準和垂直方式重複的基底影像圖例](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a>在並排平邊時水準翻轉影像

此範例使用75×75影像來填滿200×200的矩形。 Wrap 模式設定為水準翻轉影像。


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



下圖顯示矩形如何與影像並排顯示。 請注意，當您在指定的資料列中，從一個圖格移至下一個磚時，影像會水準翻轉。

![此圖顯示水準重複的基底影像，但以水準方式反轉偶數的實例](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a>在並排平邊時垂直翻轉影像

此範例使用75×75影像來填滿200×200的矩形。 自動換行模式會設定為垂直翻轉影像。


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



下圖顯示矩形如何與影像並排顯示。 請注意，當您在指定的資料行中，從一個圖格移至下一個磚時，影像會垂直翻轉。

![圖例顯示以水準和垂直方式重複的基底影像，但偶數的資料列會垂直反轉](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a>在圖格時水準和垂直翻轉影像

此範例使用75×75影像來建立200×200矩形的磚。 Wrap 模式設定為水準和垂直翻轉影像。


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



下圖顯示矩形如何以影像並排顯示。 請注意，當您在指定的資料列中，從一個圖格移至下一個磚時，影像會水準翻轉，當您從某個圖格移至特定資料行中的下一個圖格時，影像會垂直翻轉。

![顯示每個資料列中基底影像之替代實例水準翻轉的圖例，以及垂直翻轉的替換資料列](images/tile5.png)

 

 



