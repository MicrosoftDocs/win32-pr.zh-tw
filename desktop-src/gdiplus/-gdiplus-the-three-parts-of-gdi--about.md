---
description: Windows GDI+ 的服務屬於下列三個廣泛的類別：
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: GDI+ 的三個部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5547702ca98cce86ace0f672b7aeed2dc8fc0ecee63534aaa15fac05bdcb024b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014648"
---
# <a name="the-three-parts-of-gdi"></a>GDI+ 的三個部分

Windows GDI+ 的服務屬於下列三個廣泛的類別：

-   [2D 向量圖形](#2-d-vector-graphics)
-   [建立映像](#imaging)
-   [印刷樣式](#typography)

## <a name="2-d-vector-graphics"></a>2D 向量圖形

向量圖形包含繪製基本 (，例如線條、曲線和圖形，) 由座標系統上的點集所指定。 例如，直線可以由它的兩個端點來指定，並可指定矩形的點，提供其左上角的位置，以及提供其寬度和高度的數位配對。 簡單路徑可由點陣列指定，以直線連接。 貝茲曲線是由四個控制點所指定的複雜曲線。

GDI+ 提供的類別會儲存基本型別的相關資訊、儲存基本專案相關資訊的類別，以及實際進行繪製的類別。 例如， **Rect** 類別會儲存矩形的位置和大小; **Pen** 類別會儲存線條色彩、線條寬度和線條樣式的相關資訊;和 **圖形** 類別具有繪製線條、矩形、路徑和其他圖形的方法。 另外還有數個 **筆刷** 類別，可儲存有關如何以色彩或模式填滿封閉的圖形和路徑的資訊。

## <a name="imaging"></a>建立映像

使用向量圖形的技巧很難或無法顯示特定類型的圖片。 例如，工具列按鈕上的圖片和顯示為圖示的圖片，都很難指定為線條和曲線的集合。 更難使用向量技術來建立擁擠棒球體育場的高解析度數位相片。 此類型的影像會儲存為點陣圖、數位陣列，代表螢幕上的個別點色彩。 儲存點陣圖相關資訊的資料結構，通常比向量圖形所需的更為複雜，因此 GDI+ 中有幾個類別專門用於此用途。 這類類別的範例是 **CachedBitmap**，它是用來將點陣圖儲存在記憶體中，以供快速存取和顯示。

## <a name="typography"></a>印刷樣式

印刷樣式與各種字型、大小和樣式的文字顯示相關。 GDI+ 為這項複雜的工作提供令人印象深刻的支援。 GDI+ 的其中一項新功能是子圖元消除鋸齒，可讓螢幕上呈現的文字變得更平滑。

 

 



