---
description: 若要改善轉譯效能，您可以挑選出 (，或從相機中移除) 的基本物件。
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: " (Direct3D 9) 的挑選狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111009"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="c8831-103"> (Direct3D 9) 的挑選狀態</span><span class="sxs-lookup"><span data-stu-id="c8831-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="c8831-104">若要改善轉譯效能，您可以挑選出 (，或從相機中移除) 的基本物件。</span><span class="sxs-lookup"><span data-stu-id="c8831-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="c8831-105">若是單面基本專案，這會節省轉譯時間，因為看不見背面的臉部。</span><span class="sxs-lookup"><span data-stu-id="c8831-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="c8831-106">若要啟用剔除，您需要知道頂點的纏繞順序 (通常會逆時針地) 。</span><span class="sxs-lookup"><span data-stu-id="c8831-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="c8831-107">此範例將會移除背面臉部朝前 (的任何基本型別) 的逆時針繞組順序：</span><span class="sxs-lookup"><span data-stu-id="c8831-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="c8831-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8831-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8831-109">轉譯狀態</span><span class="sxs-lookup"><span data-stu-id="c8831-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



