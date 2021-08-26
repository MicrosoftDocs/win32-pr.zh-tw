---
description: 影線圖樣的建立方式有兩種：一個用於背景，另一個用於在背景上形成模式的線條。
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: 以影線圖樣填滿形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b571ab09dc91c037e0cc89a2b107c2f8d253b832b593bb32a169bc970295d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015098"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>以影線圖樣填滿形狀

影線圖樣的建立方式有兩種：一個用於背景，另一個用於在背景上形成模式的線條。 若要填滿具有影線圖樣的封閉圖形，請使用 [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) 物件。 下列範例示範如何使用影線圖樣填滿橢圓形：


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



下圖顯示已填滿的橢圓形。

![在純色背景上，以水平線條的影線圖樣填滿的橢圓形圖例](images/hatch1.png)

[**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush)的函式會採用三個引數：影線樣式、影線線的色彩，以及背景的色彩。 影線樣式引數可以是 [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) 列舉的任何元素。 **HatchStyle** 列舉中有超過50個元素;下列清單中會顯示其中一些元素：

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



