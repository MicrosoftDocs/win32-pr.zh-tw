---
title: 畫面格緩衝區作業
description: 若要選取要在其中寫入色彩值的緩衝區，請使用 glDrawBuffer。
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- OpenGL 處理管線，畫面格緩衝區作業
- framebuffers，作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082328"
---
# <a name="framebuffer-operations"></a>畫面格緩衝區作業

若要選取要在其中寫入色彩值的緩衝區，請使用 [**glDrawBuffer**](gldrawbuffer.md)。 您可以使用四個不同的函式，在執行所有的每個片段作業之後，針對每個邏輯 framebuffers 遮罩寫入位數：

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

[**GlAccum**](glaccum.md)函數控制累積緩衝區的作業。 最後， [**glClear**](glclear.md) 會將指定之緩衝區子集中的每個圖元設定為 [**glClearColor**](glclearcolor.md)、 [**glClearIndex**](glclearindex.md)、 [**glClearDepth**](glcleardepth.md)、 [**glClearStencil**](glclearstencil.md)或 [**glClearAccum**](glclearaccum.md)指定的值。

 

 




