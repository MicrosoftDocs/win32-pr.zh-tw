---
title: 點陣化
description: 進行圖形化是指將基本型別轉換為二維影像的進程。
ms.assetid: 8d4e3033-2afe-4526-8862-799c45ea9a6a
keywords:
- OpenGL 處理管線，點陣化
- 將 OpenGL 進行點陣化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f0d8e7ece3bead408b8d056356593879edc638c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507152"
---
# <a name="rasterizing"></a>點陣化

*進行圖形化是指將* 基本型別轉換為二維影像的進程。 此影像的每個點都包含色彩、深度和材質資料等資訊。 點及其相關聯的資訊稱為 *片段*。 目前的點陣位置（如 [**glRasterPos \***](glrasterpos-functions.md)所指定）在這個階段中用於繪製圖元和點陣圖的各種方式。 柵格點、線段和多邊形時，會發生不同的問題。 此外，圖元矩形和點陣圖也需要進行柵格化。

使用 OpenGL，您可以使用下列函式來控制光柵：

-   原。 使用判斷維度和 stipple 模式的函式來控制如何將基本專案進行柵格化： [**glPointSize**](glpointsize.md)、 [**glLineWidth**](gllinewidth.md)、 [**glLineStipple**](gllinestipple.md)和 [**glPolygonStipple**](glpolygonstipple.md)。 使用 [**glCullFace**](glcullface.md)、 [**glFrontFace**](glfrontface.md)和 [**glPolygonMode**](glpolygonmode.md)來控制多邊形的前後臉部如何進行柵格化。
-   圖元。 有幾個函式會控制圖元的儲存和傳輸模式。 函數 [**\* glPixelStore**](glpixelstore-functions.md)可控制用戶端記憶體中的圖元編碼，以及 [**glPixelTransfer \***](glpixeltransfer.md)和 [**glPixelMap \***](glpixelmap.md)控制在放置於畫面格緩衝區之前如何處理圖元。 使用 [**glDrawPixels**](gldrawpixels.md)指定圖元矩形;使用 [**glPixelZoom**](glpixelzoom.md)控制其點陣化。
-   點陣圖。 點陣圖是零的矩形，也是指定要產生之片段的特定模式。 每個片段都有相同的關聯資料。 [**GlBitmap**](glbitmap.md)函數會指定點陣圖。
-   材質記憶體。 當啟用紋理時，紋理會將指定之材質影像的一部分對應到每個基本類型。 這項對應的完成方式是在片段的材質座標所指示的位置使用材質影像的色彩，以修改片段的 RGBA 色彩。 使用 [**glTexImage2D**](glteximage2d.md) 或 [**glTexImage1D**](glteximage1d.md)指定材質影像。 [**GlTexParameter \***](gltexparameter-functions.md)和 [**glTexEnv \***](gltexenv-functions.md)函式會控制如何解讀材質值並套用至片段。
-   霧。 若要以柵格化片段的後續紋理色彩來 blend 霧化色彩，請使用根據 eyepoint 與片段之間距離的混合因數。 使用 [**glFog \***](glfog.md)來指定 [霧色] 和 [混色因數]。

 

 




