---
title: 特殊鳶尾花 GL 移植問題
description: 特殊鳶尾花 GL 移植問題
ms.assetid: dcf7967a-2867-4443-a1c8-8335c6fe016a
keywords:
- Windows 上的 OpenGL，鳶尾花 GL 移植
- 移植至 OpenGL、鳶尾花 GL
- OpenGL 移植，鳶尾花 GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1273a873f3a39a5d237f9a5845a72f87156e001c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969672"
---
# <a name="special-iris-gl-porting-issues"></a><span data-ttu-id="5e1e9-106">特殊鳶尾花 GL 移植問題</span><span class="sxs-lookup"><span data-stu-id="5e1e9-106">Special IRIS GL Porting Issues</span></span>

<span data-ttu-id="5e1e9-107">下列主題說明將鳶尾花 GL 程式碼的特定部分移植至 OpenGL 程式碼的技巧。</span><span class="sxs-lookup"><span data-stu-id="5e1e9-107">The following topics describe techniques for porting specific parts of your IRIS GL code to OpenGL code.</span></span>

-   [<span data-ttu-id="5e1e9-108">移植 greset</span><span class="sxs-lookup"><span data-stu-id="5e1e9-108">Porting greset</span></span>](porting-greset.md)
-   [<span data-ttu-id="5e1e9-109">移植鳶尾花 GL "Get" 函式</span><span class="sxs-lookup"><span data-stu-id="5e1e9-109">Porting IRIS GL "Get" Functions</span></span>](porting-iris-gl-get-functions.md)
-   [<span data-ttu-id="5e1e9-110">移植需要目前圖形位置的程式碼</span><span class="sxs-lookup"><span data-stu-id="5e1e9-110">Porting Code that Requires a Current Graphics Position</span></span>](porting-code-that-requires-a-current-graphics-position.md)
-   [<span data-ttu-id="5e1e9-111">移植繪圖函數</span><span class="sxs-lookup"><span data-stu-id="5e1e9-111">Porting Drawing Functions</span></span>](porting-drawing-functions.md)
-   [<span data-ttu-id="5e1e9-112">移植色彩、陰影和 Writemask 程式碼</span><span class="sxs-lookup"><span data-stu-id="5e1e9-112">Porting Color, Shading, and Writemask Code</span></span>](porting-color--shading--and-writemask-code.md)
-   [<span data-ttu-id="5e1e9-113">移植圖元作業</span><span class="sxs-lookup"><span data-stu-id="5e1e9-113">Porting Pixel Operations</span></span>](porting-pixel-operations.md)
-   [<span data-ttu-id="5e1e9-114">移植深度提示和霧化命令</span><span class="sxs-lookup"><span data-stu-id="5e1e9-114">Porting Depth Cueing and Fog Commands</span></span>](porting-depth-cueing-and-fog-commands.md)
-   [<span data-ttu-id="5e1e9-115">移植曲線和介面函式</span><span class="sxs-lookup"><span data-stu-id="5e1e9-115">Porting Curve and Surface Functions</span></span>](porting-curve-and-surface-functions.md)
-   [<span data-ttu-id="5e1e9-116">移植消除鋸齒功能</span><span class="sxs-lookup"><span data-stu-id="5e1e9-116">Porting Antialiasing Functions</span></span>](porting-antialiasing-functions.md)
-   [<span data-ttu-id="5e1e9-117">移植累積的緩衝區呼叫</span><span class="sxs-lookup"><span data-stu-id="5e1e9-117">Porting Accumulation Buffer Calls</span></span>](porting-accumulation-buffer-calls.md)
-   [<span data-ttu-id="5e1e9-118">移植樣板平面呼叫</span><span class="sxs-lookup"><span data-stu-id="5e1e9-118">Porting Stencil Plane Calls</span></span>](porting-stencil-plane-calls.md)
-   [<span data-ttu-id="5e1e9-119">移植顯示清單</span><span class="sxs-lookup"><span data-stu-id="5e1e9-119">Porting Display Lists</span></span>](porting-display-lists.md)
-   [<span data-ttu-id="5e1e9-120">移植 Defs、系結和集合</span><span class="sxs-lookup"><span data-stu-id="5e1e9-120">Porting Defs, Binds, and Sets</span></span>](porting-defs--binds--and-sets.md)
-   [<span data-ttu-id="5e1e9-121">移植光源和材質函數</span><span class="sxs-lookup"><span data-stu-id="5e1e9-121">Porting Lighting and Materials Functions</span></span>](porting-lighting-and-materials-functions.md)
-   [<span data-ttu-id="5e1e9-122">移植材質函數</span><span class="sxs-lookup"><span data-stu-id="5e1e9-122">Porting Texture Functions</span></span>](porting-texture-functions.md)
-   [<span data-ttu-id="5e1e9-123">移植挑選函數</span><span class="sxs-lookup"><span data-stu-id="5e1e9-123">Porting Picking Functions</span></span>](porting-picking-functions.md)
-   [<span data-ttu-id="5e1e9-124">移植意見函數</span><span class="sxs-lookup"><span data-stu-id="5e1e9-124">Porting Feedback Functions</span></span>](porting-feedback-functions.md)

 

 




