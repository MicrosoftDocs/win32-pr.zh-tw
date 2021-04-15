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
# <a name="framebuffer-operations"></a><span data-ttu-id="751c3-105">畫面格緩衝區作業</span><span class="sxs-lookup"><span data-stu-id="751c3-105">Framebuffer Operations</span></span>

<span data-ttu-id="751c3-106">若要選取要在其中寫入色彩值的緩衝區，請使用 [**glDrawBuffer**](gldrawbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="751c3-106">To select the buffer into which color values are written, use [**glDrawBuffer**](gldrawbuffer.md).</span></span> <span data-ttu-id="751c3-107">您可以使用四個不同的函式，在執行所有的每個片段作業之後，針對每個邏輯 framebuffers 遮罩寫入位數：</span><span class="sxs-lookup"><span data-stu-id="751c3-107">You use four different functions to mask the writing of bits to each of the logical framebuffers after all per-fragment operations have been performed:</span></span>

-   [<span data-ttu-id="751c3-108">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="751c3-108">**glIndexMask**</span></span>](glindexmask.md)
-   [<span data-ttu-id="751c3-109">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="751c3-109">**glColorMask**</span></span>](glcolormask.md)
-   [<span data-ttu-id="751c3-110">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="751c3-110">**glDepthMask**</span></span>](gldepthmask.md)
-   [<span data-ttu-id="751c3-111">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="751c3-111">**glStencilMask**</span></span>](glstencilmask.md)

<span data-ttu-id="751c3-112">[**GlAccum**](glaccum.md)函數控制累積緩衝區的作業。</span><span class="sxs-lookup"><span data-stu-id="751c3-112">The [**glAccum**](glaccum.md) function controls the operation of the accumulation buffer.</span></span> <span data-ttu-id="751c3-113">最後， [**glClear**](glclear.md) 會將指定之緩衝區子集中的每個圖元設定為 [**glClearColor**](glclearcolor.md)、 [**glClearIndex**](glclearindex.md)、 [**glClearDepth**](glcleardepth.md)、 [**glClearStencil**](glclearstencil.md)或 [**glClearAccum**](glclearaccum.md)指定的值。</span><span class="sxs-lookup"><span data-stu-id="751c3-113">Finally, [**glClear**](glclear.md) sets every pixel in a specified subset of the buffers to the value specified with [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), or [**glClearAccum**](glclearaccum.md).</span></span>

 

 




