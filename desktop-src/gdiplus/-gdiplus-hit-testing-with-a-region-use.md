---
description: 點擊測試的目的是要判斷資料指標是否在指定的物件上，例如圖示或按鈕。
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: 使用區域進行點擊測試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0673466bc368c9288765b1c7e6f460716d8d40674802a0977690a7ef79b58b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885396"
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



 

 



