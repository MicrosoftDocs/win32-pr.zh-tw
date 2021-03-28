---
description: 您可以用數個圖形的其中一種來繪製線條的開頭或結尾，稱為行帽。 Windows GDI + 支援數行帽，例如 round、正方形、菱形和箭頭。
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: 使用行帽繪製線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988147"
---
# <a name="drawing-a-line-with-line-caps"></a>使用行帽繪製線條

您可以用數個圖形的其中一種來繪製線條的開頭或結尾，稱為行帽。 Windows GDI + 支援數行帽，例如 round、正方形、菱形和箭頭。

您可以指定行首的行帽 (開始上限) 、行尾 (結束帽) ，或虛線 (虛線端點) 的虛線。

下列範例會繪製一端有箭頭的線條，以及另一端的圓端點：


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



下圖顯示產生的行。

![圖例顯示水平線，其中的箭號位於左邊端，而一個圓形在右端](images/pens4.png)

**LineCapArrowAnchor** 和 **LineCapRoundAnchor** 是 [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) 列舉的元素。

 

 



