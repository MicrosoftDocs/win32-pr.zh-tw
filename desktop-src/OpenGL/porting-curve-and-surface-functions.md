---
title: 移植曲線和介面函式
description: 移植曲線和介面函式
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- 鳶尾花 GL 移植，曲線
- 從鳶尾花 GL、曲線移植
- 從鳶尾花 GL （曲線）移植至 OpenGL
- 從鳶尾花 GL、曲線移植的 OpenGL
- 鳶尾花 GL 移植，surface 修補程式
- 從鳶尾花 GL、surface 修補程式移植
- 從鳶尾花 GL 移植至 OpenGL，surface 修補程式
- 從鳶尾花 GL 的 OpenGL 移植，surface 修補程式
- 曲線
- 介面修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300292"
---
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="72e32-113">移植曲線和介面函式</span><span class="sxs-lookup"><span data-stu-id="72e32-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="72e32-114">OpenGL 不支援對曲線和 surface 修補程式的鳶尾花 GL 函數進行對等。</span><span class="sxs-lookup"><span data-stu-id="72e32-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="72e32-115">如果您的程式碼包含下列任何呼叫，就必須重寫程式碼：</span><span class="sxs-lookup"><span data-stu-id="72e32-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="72e32-116">**defbasis**</span><span class="sxs-lookup"><span data-stu-id="72e32-116">**defbasis**</span></span>
-   <span data-ttu-id="72e32-117">**curvebasis**、 **curveprecision**、 **crv**、 **crvn**、 **rcrv**、 **rcrvn** 和 **curveit**</span><span class="sxs-lookup"><span data-stu-id="72e32-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="72e32-118">**patchbasis**、 **patchcurves**、 **patchprecision**、 **patch** 和 **rpatch**</span><span class="sxs-lookup"><span data-stu-id="72e32-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="72e32-119">本主題包含下列各項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72e32-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="72e32-120">移植 NURBS 物件</span><span class="sxs-lookup"><span data-stu-id="72e32-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="72e32-121">移植 NURBS 曲線</span><span class="sxs-lookup"><span data-stu-id="72e32-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="72e32-122">移植修剪曲線</span><span class="sxs-lookup"><span data-stu-id="72e32-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="72e32-123">移植 NURBS 表面</span><span class="sxs-lookup"><span data-stu-id="72e32-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 




