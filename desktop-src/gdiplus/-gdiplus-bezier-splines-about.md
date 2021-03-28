---
description: B&\# 233; zier 曲線是由四個點指定的曲線：兩個端點 (p1 和 p2) ，以及 (C1 和 c2) 的兩個控制點。
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: 貝茲曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115269"
---
# <a name="bezier-splines"></a>貝茲曲線

貝茲曲線是由四個點指定的曲線：兩個端點 (p1 和 p2) ，以及 (C1 和 c2) 的兩個控制點。 曲線開始于 p1，結束于 p2。 曲線不會通過控制點，但是控制點的作用就像磁鐵一樣，以特定方向拉出曲線，並影響曲線的彎曲方式。 下圖顯示貝茲曲線以及其端點和控制點。

![圖例顯示具有兩個端點和兩個控制點的貝茲曲線](images/aboutgdip02-art11a.png)

請注意，曲線會從 p1 開始，並移至控制項點 c1。 在 p1 的曲線的正切線條是從 p1 到 c1 繪製的線條。 另請注意，端點 p2 的正切線條是從 c2 到 p2 繪製的線條。

若要繪製貝茲曲線，您需要 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件。 **Graphics** 物件提供 [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint))方法，而 **Pen** 物件會儲存曲線的屬性，例如線條寬度和色彩。 **畫筆** 物件的位址會做為 DrawBezier 方法的其中一個引數傳遞。 傳遞至 DrawBezier 方法的其餘引數為端點和控制點。 下列範例會繪製一個具有起點的貝茲曲線 (0、0) 、控制點 (40、20) 和 (80、150) 和結束點 (100，10) 。


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



下圖顯示曲線、控制點和兩條正切線條。

![圖例顯示具有兩個端點的貝茲曲線、兩個控制點，以及兩個正切線條](images/aboutgdip02-art12.png)

貝茲曲線最初是由在汽車產業中設計的聖皮爾貝茲曲線所開發。 他們已證明在許多電腦輔助設計類型中都很有用，而且也用來定義字型的大綱。 貝茲曲線可以產生各種不同的圖形，如下圖所示。

![顯示三個貝茲曲線的圖例](images/aboutgdip02-art13.png)

 

 



