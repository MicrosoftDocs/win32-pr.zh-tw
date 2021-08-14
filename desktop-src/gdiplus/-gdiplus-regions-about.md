---
description: 區域是顯示介面的一部分。
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: 區域 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd15a7a25b341556b312c540f6fa4caf870da75aa4973be1d7c1e8102511e6ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885014"
---
# <a name="regions-gdi"></a>區域 (GDI+)

區域是顯示介面的一部分。 區域可以是簡單 (單一矩形) 或複雜 (多邊形和封閉曲線) 的組合。 下圖顯示兩個區域：一個是從矩形建立的，另一個則是從路徑所建立。

![顯示與不透明曲線圖形重迭的透明矩形區域圖例](images/aboutgdip02-art27.png)

區域通常用於裁剪和點擊測試。 裁剪牽涉到將繪圖限制為螢幕的特定區域，通常是需要更新的螢幕部分。 點擊測試牽涉到在按下滑鼠按鍵時，檢查游標是否在畫面的特定區域中。

您可以從矩形或從路徑來建立區域。 您也可以藉由合併現有區域來建立複雜的區域。 [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)類別提供下列方法來結合區域： [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion))、 [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion))、 [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_))、 [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))和 [**Region：：補數**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath))。

兩個區域的交集是屬於這兩個區域的所有點的集合。 聯集是所有屬於一或多個區域的所有點的集合。 區域的補數是不在區域中的所有點的集合。 下圖顯示上圖中兩個區域的交集和聯集。

![顯示上圖中區域交集及其交集的圖例](images/aboutgdip02-art28.png)

套用至一組區域的 [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) 方法會產生一個區域，其中包含屬於一個區域或另一個區域的所有點，但不能同時包含兩者。 適用于一組區域的 [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) 方法會產生一個區域，其中包含第一個區域中不在第二個區域的所有點。 下圖顯示將 Xor 和 Exclude 方法套用至本主題開頭所顯示的兩個區域所產生的區域。

![顯示兩個區域中的元件，而不是兩者都有的圖例，以及未與曲線區域重迭的矩形部分](images/aboutgdip02-art29.png)

若要填滿區域，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件和 [**區域**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) 物件。 **Graphics** 物件提供 [**Graphics：： FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion)方法，而 **筆刷** 物件會儲存填滿的屬性，例如色彩或模式。 下列範例會以純色填滿區域。


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
