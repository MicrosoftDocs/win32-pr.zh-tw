---
description: 有些應用程式會提供一些功能，以反映在工作區中繪製的 (或鏡像) 物件。
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: 反射
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03d872273e7d0b9f23d9ffb31c6304c8b59b59eda80c7181802120f89c0d764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092698"
---
# <a name="reflection"></a>反射

有些應用程式會提供一些功能，以反映在工作區中繪製的 (或鏡像) 物件。 包含反映功能的應用程式會使用 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將世界空間中的適當值設定為頁面空間轉換。 此函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。 XFORM 的 eM11 和 eM22 成員分別指定水準和垂直反映元件。

*反映轉換* 會建立物件的鏡像影像（相對於 X 軸或 y 軸）。 簡單來說，反映只是負面調整。 若要產生水準反映，x 座標會乘以1。 若要產生垂直反映，y 座標會乘以1。

水準反映可透過下列演算法來表示：

``` syntax
x' = -x 
```

其中 x 是 x 座標，x 是反映的結果。

產生水準反映的2到2個矩陣包含下列值：

``` syntax
|-1    0| 
|0     1| 
```

垂直反映可透過下列演算法來表示：

``` syntax
y' = -y 
```

其中 y 是 y 座標，y 是反映的結果。

產生垂直反映的2到2個矩陣包含下列值：

``` syntax
|1    0| 
|0   -1| 
```

您可以使用下列2乘2矩陣，將水準反映和垂直反映作業合併為單一作業：

``` syntax
|-1    0| 
|0    -1| 
```

 

 



