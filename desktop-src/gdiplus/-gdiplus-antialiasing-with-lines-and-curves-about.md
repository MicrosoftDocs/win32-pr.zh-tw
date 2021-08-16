---
description: 當您使用 Windows GDI+ 來繪製線條時，可以提供線條的起點和結束點，但不需要提供該行上個別圖元的任何相關資訊。
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: 線條和曲線的反鋸齒功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6fd1df9c8dca6bb600c723fa61cf14b99e53a51670768a7323ca33e12b9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117697107"
---
# <a name="antialiasing-with-lines-and-curves"></a>線條和曲線的反鋸齒功能

當您使用 Windows GDI+ 來繪製線條時，可以提供線條的起點和結束點，但不需要提供該行上個別圖元的任何相關資訊。 GDI+ 與顯示器驅動程式軟體一起運作，以判斷要開啟哪些圖元來顯示特定顯示裝置上的線條。

請考慮從點 (4，2) 到 (16，10) 的點的紅線。 假設座標系統的原點位於左上角，而量值的單位是圖元。 也假設 X 軸指向右邊，y 軸則指向向下。 下圖顯示在彩色背景上繪製的紅線放大視圖。

![圖例顯示彩色彩色背景上的純色紅色圖元](images/aboutgdip02-art33.png)

請注意，用來呈現線條的紅色圖元不是透明的。 沒有部分透明的圖元可顯示線條。 這種類型的線條轉譯讓線條具有不規則外觀，而線條看起來有點像樓梯。 這項技術代表具有樓梯的線，稱為別名;樓梯是理論線的別名。

更精密的轉譯線條技巧牽涉到使用部分透明的圖元以及純紅色圖元。 圖元會設定為純紅色或某些混合的紅色和背景色彩，視它們與線條的接近程度而定。 這種類型的轉譯稱為消除鋸齒，並導致人類眼睛感覺更平滑的線條。 下圖顯示特定圖元如何與背景混合，以產生反鋸齒線條。

![圖例顯示在相同背景的紅色圖元](images/aboutgdip02-art34.png)

 (平滑) 的消除鋸齒也可以套用至曲線。 下圖顯示平滑橢圓形的放大視圖。

![在白色背景上由不同的藍色圖元陰影組成的橢圓形圖例](images/aboutgdip02-art35.png)

下圖顯示實際大小的相同橢圓形，一次沒有消除鋸齒，一次是消除鋸齒。

![兩個省略號的螢幕擷取畫面：具有消除鋸齒功能的 noticably 會更平滑](images/aboutgdip02-art36.png)

若要繪製使用消除鋸齒的線條和曲線，請建立 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件，並將 *SmoothingModeAntiAlias* 傳遞至其 [**graphics：： SetSmoothingMode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) 方法。 然後，呼叫相同 **圖形** 物件的其中一個繪圖方法。


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** 是 [**SmoothingMode**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) 列舉的元素。

 

 



