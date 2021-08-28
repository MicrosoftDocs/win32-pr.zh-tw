---
title: 輸入資料
description: OpenGL 管線需要您輸入數種類型的資料
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- OpenGL 處理管線，輸入資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a588e60991ad068653890659e236f8a7a96e62cad524b13ea72bfd38fb5bba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937425"
---
# <a name="input-data"></a>輸入資料

OpenGL 管線會要求您輸入數種類型的資料：

-   **頂點**。 頂點描述所需幾何物件的形狀。 若要指定頂點，請使用 [ * *\* glVertex* _](glvertex-functions.md)函數搭配 [_ *glBegin* *](glbegin.md)和 [**glEnd**](glend.md) ，以建立點、線條或多邊形。 您也可以使用 [**glRect**](glrect-functions.md) 來一次描述整個矩形。
-   **邊緣旗** 標。 依預設，多邊形的所有邊緣都是邊界邊緣。 使用 [**glEdgeFlag \***](gledgeflag-functions.md)明確設定 edge 旗標。
-   **目前的點陣定位**。 使用 [**glRasterPos \***](glrasterpos-functions.md)指定時，目前的點陣位置會用來決定圖元和點陣圖繪圖作業的點陣座標。
-   **目前的一般**。 與特定頂點相關聯的一般向量會決定該頂點上的介面如何在三維空間中導向;接著，這會影響特定頂點接收的光線量。 使用 [**glNormal \***](glnormal-functions.md)來指定一般向量。
-   **目前的色彩**。 頂點的色彩與光源條件，會決定最終的亮色。 如果是在 RGBA 模式中，則會使用 [ * *glColor \** _](glcolor-functions.md)來指定色彩，或在色彩索引模式中使用 [_ *\* glIndex* *](glindex-functions.md)來指定色彩。
-   **目前的材質座標**。 以 [**glTexCoord \***](gltexcoord-functions.md)指定的材質座標可決定材質地圖中與物件頂點關聯的位置。

> [!Note]  
> **呼叫 glVertex \* *_ 時，產生的頂點會繼承目前的邊緣旗標、正常、色彩和材質座標。因此，* _ glEdgeFlag \* *_、_* glNormal \* *_、_* glColor \* *_ 和 _* glTexCoord \* *_ 必須在 _* glVertex \* 之前呼叫**，如果它們會影響產生的頂點。

 

 

 




