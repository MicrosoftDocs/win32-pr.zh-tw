---
title: 片段
description: 片段
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL、片段
- OpenGL 處理管線，片段
- 段 OpenGL
- framebuffers，修改圖元的片段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984930"
---
# <a name="fragments"></a><span data-ttu-id="18dcd-107">片段</span><span class="sxs-lookup"><span data-stu-id="18dcd-107">Fragments</span></span>

<span data-ttu-id="18dcd-108">只有當它通過下列測試時，才會在畫面格緩衝區中修改對應的圖元：</span><span class="sxs-lookup"><span data-stu-id="18dcd-108">A fragment produced by rasterization modifies the corresponding pixel in the framebuffer only if it passes the following tests:</span></span>

-   [<span data-ttu-id="18dcd-109">圖元擁有權測試</span><span class="sxs-lookup"><span data-stu-id="18dcd-109">Pixel ownership test</span></span>](pixel-ownership-test.md)
-   [<span data-ttu-id="18dcd-110">剪式測試</span><span class="sxs-lookup"><span data-stu-id="18dcd-110">Scissor test</span></span>](scissor-test.md)
-   [<span data-ttu-id="18dcd-111">Alpha 測試</span><span class="sxs-lookup"><span data-stu-id="18dcd-111">Alpha test</span></span>](alpha-test.md)
-   [<span data-ttu-id="18dcd-112">樣板測試</span><span class="sxs-lookup"><span data-stu-id="18dcd-112">Stencil test</span></span>](stencil-test.md)
-   [<span data-ttu-id="18dcd-113">深度緩衝區測試</span><span class="sxs-lookup"><span data-stu-id="18dcd-113">Depth-buffer test</span></span>](depth-buffer-test.md)

<span data-ttu-id="18dcd-114">如果通過，片段的資料可以取代現有的畫面格緩衝區值，或者您可以將它與畫面格緩衝區中現有的資料結合，視特定模式的狀態而定。</span><span class="sxs-lookup"><span data-stu-id="18dcd-114">If it passes, the fragment's data can replace the existing framebuffer values, or you can combine it with existing data in the framebuffer, depending on the state of certain modes.</span></span> <span data-ttu-id="18dcd-115">您可以透過下列方式將片段與畫面格緩衝區中的資料結合：</span><span class="sxs-lookup"><span data-stu-id="18dcd-115">You can combine the fragment with data in the framebuffer by:</span></span>

-   [<span data-ttu-id="18dcd-116">混合</span><span class="sxs-lookup"><span data-stu-id="18dcd-116">Blending</span></span>](blending.md)
-   [<span data-ttu-id="18dcd-117">抖動</span><span class="sxs-lookup"><span data-stu-id="18dcd-117">Dithering</span></span>](dithering.md)
-   [<span data-ttu-id="18dcd-118">邏輯作業</span><span class="sxs-lookup"><span data-stu-id="18dcd-118">Logical operations</span></span>](logical-operations.md)

 

 




