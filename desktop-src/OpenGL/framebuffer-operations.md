---
title: 畫面格緩衝區作業
description: 若要選取要在其中寫入色彩值的緩衝區，請使用 glDrawBuffer。
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- OpenGL 處理管線，畫面格緩衝區作業
- framebuffers，作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507121"
---
# <a name="framebuffer-operations"></a>畫面格緩衝區作業

若要選取要在其中寫入色彩值的緩衝區，請使用 [**glDrawBuffer**](gldrawbuffer.md)。 您可以使用四個不同的函式，在執行所有的每個片段作業之後，針對每個邏輯 framebuffers 遮罩寫入位數：

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

[**GlAccum**](glaccum.md)函數控制累積緩衝區的作業。 最後， [**glClear**](glclear.md) 會將指定之緩衝區子集中的每個圖元設定為 [**glClearColor**](glclearcolor.md)、 [**glClearIndex**](glclearindex.md)、 [**glClearDepth**](glcleardepth.md)、 [**glClearStencil**](glclearstencil.md)或 [**glClearAccum**](glclearaccum.md)指定的值。

 

 




