---
description: 有些應用程式會提供在工作區中繪製物件的扭曲功能。
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: 剪切
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193791"
---
# <a name="shear"></a>剪切

有些應用程式會提供在工作區中繪製物件的扭曲功能。 使用切變功能的應用程式會使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將世界空間中的適當值設定為頁面空間轉換。 此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。 XFORM 的 eM12 和 eM21 成員分別指定水準和垂直 proportionality 常數。

*切變轉換* 有兩個元件。 第一個改變物件中的垂直線;第二個改變水平線條。 下圖顯示從世界空間複製到頁面空間時，水準切變的 20 x 單位矩形。

![圖例顯示世界空間中的矩形和頁面空間中的 trapeziod](images/cstrn-13.png)

水準切變可透過下列演算法來表示：

``` syntax
x' = x + (Sx * y) 
```

其中 x 是原始 x 座標，Sx 是 proportionality 常數，而 x 是切變轉換的結果。

垂直切變可透過下列演算法來表示：

``` syntax
y' = y + (Sy * x) 
```

其中 y 是原始的 y 座標，Sy 是 proportionality 常數，y ' 是切變轉換的結果。

您可以使用2乘2矩陣，將水準切變和垂直切變轉換合併成單一作業。

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

產生切變的 2 x 2 矩陣包含下列值：

``` syntax
|1    1| 
|0    1| 
```

 

 



