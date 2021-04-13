---
title: 圖元擁有權測試
description: 圖元擁有權測試會判斷目前的 OpenGL 內容是否擁有畫面格緩衝區中對應至特定片段的圖元。
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- OpenGL 處理管線，圖元擁有權測試
- 圖元擁有權測試 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301175"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="8819f-105">圖元擁有權測試</span><span class="sxs-lookup"><span data-stu-id="8819f-105">Pixel Ownership Test</span></span>

<span data-ttu-id="8819f-106">圖元擁有權測試會判斷目前的 OpenGL 內容是否擁有畫面格緩衝區中對應至特定片段的圖元。</span><span class="sxs-lookup"><span data-stu-id="8819f-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="8819f-107">如果是，則片段會繼續進行下一個測試。</span><span class="sxs-lookup"><span data-stu-id="8819f-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="8819f-108">如果不是，則視窗系統會決定是否要捨棄片段，或是否要使用該片段來執行任何進一步的片段作業。</span><span class="sxs-lookup"><span data-stu-id="8819f-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="8819f-109">在這項測試中，當 OpenGL 視窗遮蔽時，視窗系統會控制行為。</span><span class="sxs-lookup"><span data-stu-id="8819f-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




