---
description: 大部分的 CAD 和繪圖應用程式都會提供可調整使用者所建立之輸出的功能。
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: 調整大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf8cb7293be4083c08de1d104bb8349b3cd5003a0abddf77d41922cfb294cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965238"
---
# <a name="scaling"></a>調整大小

大部分的 CAD 和繪圖應用程式都會提供可調整使用者所建立之輸出的功能。 包含調整 (或縮放) 功能的應用程式會呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將適當的世界空間設定為頁面空間轉換。 此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。 XFORM 的 eM11 和 eM22 成員分別指定水準和垂直縮放比例元件。

進行 *調整* 時，會根據 X 軸或 y 軸來延展或壓縮組成物件的垂直和水平線條 (或向量) 。 下圖顯示從全局座標空間複製到頁面座標空間時，垂直縮放至其原始高度的兩倍的 20 x 20 單位矩形。

![圖例顯示世界空間中的小矩形，以及頁面空間中的高度](images/cstrn-10.png)

在上圖中，定義原始矩形的側邊量值20個單位的垂直線，而定義縮放矩形側邊量值40單位的垂直線則是垂直線條。

垂直調整可透過下列演算法來表示。

``` syntax
y' = y * Dy 
```

其中 y ' 是新的長度，y 是原始長度，而 Dy 是垂直縮放比例。

水準調整可透過下列演算法來表示。

``` syntax
x' = x * Dx 
```

其中 x 是新的長度，x 是原始長度，而 Dx 是水準縮放因數。

垂直和水準縮放轉換可以使用2乘2矩陣合併為單一作業。

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

產生縮放轉換的2到2個矩陣包含下列值。

``` syntax
|1    0| 
|0    2| 
```

 

 



