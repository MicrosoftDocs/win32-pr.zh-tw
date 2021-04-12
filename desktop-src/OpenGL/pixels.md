---
title: 阻擋的
description: 片段會轉換成畫面格緩衝區中的圖元。
ms.assetid: 1925b455-ae6e-4f95-899c-4bcac641f549
keywords:
- OpenGL、圖元
- OpenGL 處理管線，圖元
- 圖元 OpenGL
- framebuffers，將片段轉換成圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6660452930683943da780fad3aeb001e531711
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372614"
---
# <a name="pixels"></a><span data-ttu-id="28d4a-107">阻擋的</span><span class="sxs-lookup"><span data-stu-id="28d4a-107">Pixels</span></span>

<span data-ttu-id="28d4a-108">片段會轉換成畫面格緩衝區中的圖元。</span><span class="sxs-lookup"><span data-stu-id="28d4a-108">Fragments are converted to pixels in the framebuffer.</span></span> <span data-ttu-id="28d4a-109">畫面格緩衝區會組織成一組邏輯緩衝的色彩、深度、樣板和累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="28d4a-109">The framebuffer is organized into a set of logical buffers the color, depth, stencil, and accumulation buffers.</span></span> <span data-ttu-id="28d4a-110">色彩緩衝區本身是由 front left、right、back、back、back 和某些數目的輔助緩衝區所組成。</span><span class="sxs-lookup"><span data-stu-id="28d4a-110">The color buffer itself consists of a front left, front right, back left, back right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="28d4a-111">您可以發出函式來控制這些緩衝區，並直接讀取或複製它們的圖元。</span><span class="sxs-lookup"><span data-stu-id="28d4a-111">You can issue functions to control these buffers, and directly read or copy pixels from them.</span></span> <span data-ttu-id="28d4a-112"> (請注意，您所使用的特定 OpenGL 內容可能不會提供所有這些緩衝區。 ) </span><span class="sxs-lookup"><span data-stu-id="28d4a-112">(Note that the particular OpenGL context you're using may not provide all these buffers.)</span></span>

-   [<span data-ttu-id="28d4a-113">畫面格緩衝區作業</span><span class="sxs-lookup"><span data-stu-id="28d4a-113">Framebuffer Operations</span></span>](framebuffer-operations.md)
-   [<span data-ttu-id="28d4a-114">讀取或複製圖元</span><span class="sxs-lookup"><span data-stu-id="28d4a-114">Reading or Copying Pixels</span></span>](reading-or-copying-pixels.md)
-   [<span data-ttu-id="28d4a-115">圖元參考</span><span class="sxs-lookup"><span data-stu-id="28d4a-115">Pixels Reference</span></span>](pixels-reference.md)

 

 




