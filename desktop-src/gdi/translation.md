---
description: 某些應用程式會轉譯在工作區中繪製 (或移位) 物件。
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: 翻譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987817"
---
# <a name="translation"></a>翻譯

某些應用程式會轉譯在工作區中繪製 (或移位) 物件。 藉由呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 函式，將適當的世界空間設定為頁面空間轉換。 SetWorldTransform 函式會接收 [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) 結構的指標，其中包含適當的值。 XFORM 的 eDx 和 eDy 成員會分別指定水準和垂直轉譯元件。

進行 *轉譯* 時，物件中的每個點都會依指定的量垂直、水準或同時移動。 下圖顯示從全局座標空間複製到頁面座標空間時，由10個單位轉譯為右邊的 20 x 單位矩形。

![圖例顯示在世界空間的某個位置，以及在頁面空間中不同位置的矩形](images/cstrn-09.png)

在上圖中，矩形中每個點的 x 座標是大於原始 x 座標的10個單位。

水準轉譯可以用下列演算法來表示。

``` syntax
x' = x + Dx 
```

其中 x 是新的 x 座標，x 是原始 x 座標，而 Dx 是移動的水準距離。

垂直轉譯可以用下列演算法來表示。

``` syntax
y' = y + Dy 
```

其中 y ' 是新的 y 座標，y 是原始的 y 座標，而 Dy 是移動的垂直距離。

水準和垂直轉譯轉換可以使用三乘3的矩陣合併成單一作業。

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

 (矩陣乘法狀態的規則，其中一個矩陣的資料列數目必須等於另一個矩陣中的資料行數目。 矩陣 x y 1 中的整數 1 \| \| 是為了符合此需求而加入的預留位置。 ) 

產生圖例轉譯轉換的三向3個矩陣包含下列值。

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



