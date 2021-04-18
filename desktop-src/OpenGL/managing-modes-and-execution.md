---
title: 管理模式和執行
description: 管理模式和執行
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL、模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965975"
---
# <a name="managing-modes-and-execution"></a><span data-ttu-id="d3d83-104">管理模式和執行</span><span class="sxs-lookup"><span data-stu-id="d3d83-104">Managing Modes and Execution</span></span>

<span data-ttu-id="d3d83-105">許多 OpenGL 函數的作用取決於特定模式是否有效。</span><span class="sxs-lookup"><span data-stu-id="d3d83-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="d3d83-106">[**GlEnable**](glenable.md)和 [**glDisable**](gldisable.md)函數會設定這類模式;[**glIsEnabled**](glisenabled.md)會判斷是否已設定特定模式。</span><span class="sxs-lookup"><span data-stu-id="d3d83-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="d3d83-107">您可以使用 [**glFinish**](glfinish.md)來控制先前發行之 OpenGL 函式的執行，這會強制所有這類函式完成或 [**glFlush**](glflush.md)，以確保所有這類函式會在有限的時間內完成。</span><span class="sxs-lookup"><span data-stu-id="d3d83-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="d3d83-108">在特定的 OpenGL 執行中，您可以使用 [**glHint**](glhint.md)來控制提示的特定行為。</span><span class="sxs-lookup"><span data-stu-id="d3d83-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="d3d83-109">這類行為是色彩和材質座標插補的品質;霧化計算的精確度;以及反鋸齒點、線條或多邊形的取樣品質。</span><span class="sxs-lookup"><span data-stu-id="d3d83-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3d83-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3d83-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3d83-111">模式和執行參考</span><span class="sxs-lookup"><span data-stu-id="d3d83-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 




