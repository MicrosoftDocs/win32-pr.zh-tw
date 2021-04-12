---
title: 移植 MSINGLE 模式程式碼
description: OpenGL 對 MSINGLE、單一矩陣模式沒有對等專案。
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- 鳶尾花 GL 移植，MSINGLE 模式
- 從鳶尾花 GL （MSINGLE 模式）移植
- 從鳶尾花 GL （MSINGLE 模式）移植至 OpenGL
- 鳶尾花 GL，MSINGLE 模式的 OpenGL 移植
- MSINGLE 模式
- 鳶尾花 GL 移植，單一矩陣模式
- 從鳶尾花 GL （單一矩陣模式）移植
- 從鳶尾花 GL （單一矩陣模式）移植至 OpenGL
- 從鳶尾花 GL （單一矩陣模式）移植的 OpenGL
- 單一矩陣模式
- 雙矩陣模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372367"
---
# <a name="porting-msingle-mode-code"></a><span data-ttu-id="0aca5-114">移植 MSINGLE 模式程式碼</span><span class="sxs-lookup"><span data-stu-id="0aca5-114">Porting MSINGLE Mode Code</span></span>

<span data-ttu-id="0aca5-115">OpenGL 對 **MSINGLE**、單一矩陣模式沒有對等專案。</span><span class="sxs-lookup"><span data-stu-id="0aca5-115">OpenGL has no equivalent for **MSINGLE**, single-matrix mode.</span></span> <span data-ttu-id="0aca5-116">雖然不建議使用此模式，但這是鳶尾花 GL 的預設值。</span><span class="sxs-lookup"><span data-stu-id="0aca5-116">Though use of this mode has been discouraged, it is the default for IRIS GL.</span></span> <span data-ttu-id="0aca5-117">如果您的鳶尾花 GL 程式使用單一矩陣模式，您必須將它重寫為只使用雙矩陣模式。</span><span class="sxs-lookup"><span data-stu-id="0aca5-117">If your IRIS GL program uses the single-matrix mode, you need to rewrite it to use double-matrix mode only.</span></span> <span data-ttu-id="0aca5-118">OpenGL 一律採用雙矩陣模式，且一開始是 GL \_ 模型模式。</span><span class="sxs-lookup"><span data-stu-id="0aca5-118">OpenGL is always in double-matrix mode, and is initially in GL\_MODELVIEW mode.</span></span>

<span data-ttu-id="0aca5-119">MSINGLE 模式中大部分的鳶尾花 GL 程式碼看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="0aca5-119">Most IRIS GL code in MSINGLE mode looks like this:</span></span>

``` syntax
projectionmatrix();
```

<span data-ttu-id="0aca5-120">其中 *projectionmatrix* 是下列其中一個： **ortho**、 **ortho2**、 **透視圖** 或 **window**。</span><span class="sxs-lookup"><span data-stu-id="0aca5-120">where *projectionmatrix* is one of: **ortho**, **ortho2**, **perspective**, or **window**.</span></span> <span data-ttu-id="0aca5-121">若要移植至 OpenGL，請將 **MSINGLE** 模式的 *projectionmatrix* 函式取代為：</span><span class="sxs-lookup"><span data-stu-id="0aca5-121">To port to OpenGL, replace the **MSINGLE** -mode *projectionmatrix* function with:</span></span>


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




