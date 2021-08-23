---
title: 基本 OpenGL 操作
description: 基本 OpenGL 操作
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL，基本作業
- OpenGL，資料處理
- OpenGL，處理階段
- OpenGL、顯示清單
- 顯示清單 OpenGL
- OpenGL，評估工具
- 評估 OpenGL
- OpenGL、每個頂點作業
- 每個頂點的作業 OpenGL
- OpenGL、基本元件
- 基本元件 OpenGL
- OpenGL、點陣化
- 點陣化 OpenGL
- OpenGL、每個片段的作業
- 每個片段的作業 OpenGL
- framebuffers，基本作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72f6abed7d06a93985b798e72efbf4d6ec0901e7ad9fb4614f5bf81590cefcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554711"
---
# <a name="basic-opengl-operation"></a>基本 OpenGL 操作

下圖說明 OpenGL 如何處理資料。 如所示，命令會從左邊進入，然後繼續處理管線。 有些命令會指定要繪製的幾何物件，而其他則會控制在不同處理階段處理物件的方式。

![顯示 OpenGL 資料處理管線階段的圖表。](images/basic01.png)

基本 OpenGL 操作中的處理階段如下所示：

-   **顯示清單** 您可以選擇在顯示清單中累積某些命令，以供稍後處理，而不是讓所有的命令立即透過管線進行。
-   **評估** 工具處理的評估階段可透過評估輸入值的多項式命令，提供更有效率的方式來接近曲線和表面幾何。
-   **每個頂點的作業和基本元件** OpenGL 會處理幾何 primitivespoints、線段線段，以及由頂點描述的 polygonsall。 頂點會轉換並亮掉，而且會將基本專案裁剪至區，以準備進行點陣化。
-   **光柵** 化柵格化階段會使用點、線段或多邊形的二維描述，產生一系列的框架緩衝區位址和相關聯的值。 產生的每個片段都會送入最後一個階段，也就是每個片段的作業。
-   **每個片段的作業** 這些是在資料儲存為畫面格緩衝區中的圖元之前，對資料執行的最後一項作業。

    每個片段的作業包含畫面格緩衝區的條件式更新，會根據內送和先前儲存的 z 值 (z 緩衝) 和混合內送圖元色彩與儲存的色彩，以及遮罩和其他圖元值的邏輯運算。

資料可以輸入像素格式，而不是頂點。 像素格式的資料（例如，可能會描述用於材質對應的影像），會略過上述處理的第一個階段，並改為在圖元作業階段中處理為圖元。 以下是圖元運算，圖元資料是：

-   儲存為材質記憶體，以在點陣化階段中使用。
-   柵格化，並將產生的片段合併到畫面格緩衝區，就像是從幾何資料產生的片段一樣。

 

 




