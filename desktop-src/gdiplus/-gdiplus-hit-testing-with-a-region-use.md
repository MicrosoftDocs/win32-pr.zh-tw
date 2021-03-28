---
description: 點擊測試的目的是要判斷資料指標是否在指定的物件上，例如圖示或按鈕。
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: 使用區域進行點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24913d8d890e3e1ded87eb48e2d52f1726663a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991331"
---
# <a name="hit-testing-with-a-region"></a>使用區域進行點擊測試

點擊測試的目的是要判斷資料指標是否在指定的物件上，例如圖示或按鈕。 下列範例會建立兩個矩形區域的聯集，藉以建立一個形狀區域。 假設變數 **點** 保存最近按一下的位置。 程式碼會檢查 **點** 是否位於加號區域中。 如果 **point** 位於 (點擊) 的區域內，則會以不透明的紅色筆刷填滿區域。 否則，區域會填入半透明的紅色筆刷。


```
Point point(60, 10);
// Assume that the variable "point" contains the location
// of the most recent click.
// To simulate a hit, assign (60, 10) to point.
// To simulate a miss, assign (0, 0) to point.
SolidBrush solidBrush(Color());
Region region1(Rect(50, 0, 50, 150));
Region region2(Rect(0, 50, 150, 50));
// Create a plus-shaped region by forming the union of region1 and region2.
// The union replaces region1.
region1.Union(&region2);
if(region1.IsVisible(point, &graphics))
{
   // The point is in the region. Use an opaque brush.
   solidBrush.SetColor(Color(255, 255, 0, 0));
}
else
{
   // The point is not in the region. Use a semitransparent brush.
   solidBrush.SetColor(Color(64, 255, 0, 0));
}
graphics.FillRegion(&solidBrush, &region1);
```



 

 



