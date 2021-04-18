---
title: 輸入資料
description: OpenGL 管線需要您輸入數種類型的資料
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- OpenGL 處理管線，輸入資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968835"
---
# <a name="input-data"></a>輸入資料

OpenGL 管線會要求您輸入數種類型的資料：

-   **頂點**。 頂點描述所需幾何物件的形狀。 若要指定頂點，請使用 [**\* glVertex**](glvertex-functions.md)函數搭配 [**glBegin**](glbegin.md)和 [**glEnd**](glend.md)來建立點、線條或多邊形。 您也可以使用 [**glRect**](glrect-functions.md) 來一次描述整個矩形。
-   **邊緣旗** 標。 依預設，多邊形的所有邊緣都是邊界邊緣。 使用 [**glEdgeFlag \***](gledgeflag-functions.md)明確設定 edge 旗標。
-   **目前的點陣定位**。 使用 [**glRasterPos \***](glrasterpos-functions.md)指定時，目前的點陣位置會用來決定圖元和點陣圖繪圖作業的點陣座標。
-   **目前的一般**。 與特定頂點相關聯的一般向量會決定該頂點上的介面如何在三維空間中導向;接著，這會影響特定頂點接收的光線量。 使用 [**glNormal \***](glnormal-functions.md)來指定一般向量。
-   **目前的色彩**。 頂點的色彩與光源條件，會決定最終的亮色。 如果在 RGBA 模式中，則以 [**glColor \***](glcolor-functions.md)指定色彩，或是在色彩索引模式下使用 [**glIndex \***](glindex-functions.md) 。
-   **目前的材質座標**。 以 [**glTexCoord \***](gltexcoord-functions.md)指定的材質座標可決定材質地圖中與物件頂點關聯的位置。

> [!Note]  
> 當 **呼叫 \* glVertex** 時，產生的頂點會繼承目前的邊緣旗標、正常、色彩和材質座標。 因此，必須在 **glVertex \*** 之前呼叫 **glEdgeFlag \***、 **glNormal \***、 **\* glColor** 和 **glTexCoord \*** ，以影響產生的頂點。

 

 

 




