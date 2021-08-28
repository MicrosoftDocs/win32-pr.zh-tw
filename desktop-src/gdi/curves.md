---
description: 一般曲線是一組在點陣顯示器上反白顯示的圖元 (或列印頁面上的點) ，定義圓周 (或圓錐區段的周邊) 部分。
ms.assetid: b7a1b544-8b50-45ba-918c-17472c46c8b8
title: 曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed6b7c0f6ad03a9ebe16dcffe85694397f6127ff15c2d9d3a9e68f79257a0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452238"
---
# <a name="curves"></a>曲線

一般曲線是一組在點陣顯示器上反白顯示的圖元 (或列印頁面上的點) ，定義圓周 (或圓錐區段的周邊) 部分。 不規則曲線是一組圖元，用來定義不符合圓錐區段周邊的曲線。 結束點會從曲線中排除，就如同從一行排除一樣。

當應用程式呼叫其中一個曲線繪圖函式時，GDI 會將曲線分成數個極小、離散的線段。 在判斷端點 (開始點和結束點) 每個這些線段時，GDI 會透過套用其 DDA 來決定) 定義每一行的圖元 (或點。

應用程式可以藉由呼叫 [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) 函數來繪製橢圓形或橢圓形的一部分。 此函式會在不可見矩形的周邊（稱為周框矩形）中繪製曲線。 橢圓形的大小是由兩個不可見的 radials 所指定，從矩形的中心延伸至矩形的側邊。 下圖顯示的弧形 (部分) 使用 **arc** 函數繪製的橢圓形。

![顯示代表完整圓形三季的弧線的圖表](images/cslcv-03.png)

呼叫 [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc) 函式時，應用程式會指定周框和 radials 的座標。 上圖顯示以虛線繪製的矩形和 radials，而使用實線繪製實際的弧形。

繪製另一個物件的弧線時，應用程式可以呼叫 [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) 和 [**GetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) 函式，以控制繪製物件時 (順時針或逆時針) 方向。 繪製弧形和其他物件的預設方向是以逆時針表示。

除了繪製省略號或橢圓形的部分，應用程式也可以繪製稱為貝茲曲線的不規則曲線。 *貝茲曲線* 是一種不規則曲線，其曲率是由四個控制點所定義 (p1、p2、p3 和 p4) 。 控制點 p1 和 p4 會定義曲線的開始和結束點，而控制點 p2 和 p3 會藉由標示曲線反轉方向的點來定義曲線的形狀，如下圖所示。

![顯示兩個貝茲曲線的圖，每個曲線都介於起始點和結束點之間，而每個曲線都有兩個控制點](images/cslcv-04.png)

應用程式可以藉由呼叫 [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier) 函式來繪製不規則曲線，以提供適當的控制點。

 

 



