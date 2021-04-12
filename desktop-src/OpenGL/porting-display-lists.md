---
title: 移植顯示清單
description: 顯示清單的 OpenGL 執行類似于鳶尾花 GL 的執行，在 OpenGL 中有兩個例外狀況：當您建立顯示清單並無法從顯示清單中呼叫函式時，就無法編輯顯示清單。
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- 鳶尾花 GL 移植，顯示清單
- 從鳶尾花 GL 進行移植，顯示清單
- 從鳶尾花 GL 移植至 OpenGL，顯示清單
- 從鳶尾花 GL 的 OpenGL 移植，顯示清單
- 顯示清單，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300288"
---
# <a name="porting-display-lists"></a><span data-ttu-id="33f6c-108">移植顯示清單</span><span class="sxs-lookup"><span data-stu-id="33f6c-108">Porting Display Lists</span></span>

<span data-ttu-id="33f6c-109">顯示清單的 OpenGL 執行類似于鳶尾花 GL 的執行，但有兩個例外：在 OpenGL 中，您無法在建立後編輯顯示清單，也無法從顯示清單中呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="33f6c-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="33f6c-110">因為您無法在顯示清單內編輯或呼叫函式，所以這些鳶尾花 GL 函式在 OpenGL 中沒有對等專案：</span><span class="sxs-lookup"><span data-stu-id="33f6c-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="33f6c-111">**editobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-111">**editobj**</span></span>
-   <span data-ttu-id="33f6c-112">**objdelete**、 **objinsert** 和 **objreplace**</span><span class="sxs-lookup"><span data-stu-id="33f6c-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="33f6c-113">**maketag**、 **gentag**、 **istag** 和 **deltag**</span><span class="sxs-lookup"><span data-stu-id="33f6c-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="33f6c-114">**callfunc**</span><span class="sxs-lookup"><span data-stu-id="33f6c-114">**callfunc**</span></span>

<span data-ttu-id="33f6c-115">在鳶尾花 GL 中，您可以使用 **makeobj** 和 **closeobj** 函數來建立顯示清單。</span><span class="sxs-lookup"><span data-stu-id="33f6c-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="33f6c-116">在 OpenGL 中，您會使用 [**glNewList**](glnewlist.md) 和 [**glEndList**](glendlist.md)。</span><span class="sxs-lookup"><span data-stu-id="33f6c-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="33f6c-117">下表列出鳶尾花 GL 顯示清單函式與其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="33f6c-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="33f6c-118">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="33f6c-118">IRIS GL function</span></span> | <span data-ttu-id="33f6c-119">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="33f6c-119">OpenGL function</span></span>                                                      | <span data-ttu-id="33f6c-120">意義</span><span class="sxs-lookup"><span data-stu-id="33f6c-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="33f6c-121">**makeobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-121">**makeobj**</span></span>      | <span data-ttu-id="33f6c-122">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="33f6c-122">**glNewList**</span></span>                                                        | <span data-ttu-id="33f6c-123">建立新的顯示清單。</span><span class="sxs-lookup"><span data-stu-id="33f6c-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="33f6c-124">**closeobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-124">**closeobj**</span></span>     | <span data-ttu-id="33f6c-125">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="33f6c-125">**glEndList**</span></span>                                                        | <span data-ttu-id="33f6c-126">信號顯示清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="33f6c-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="33f6c-127">**callobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-127">**callobj**</span></span>      | <span data-ttu-id="33f6c-128">[**glCallList**](glcalllist.md)、 [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="33f6c-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="33f6c-129">執行顯示清單或清單。</span><span class="sxs-lookup"><span data-stu-id="33f6c-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="33f6c-130">**isobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-130">**isobj**</span></span>        | [<span data-ttu-id="33f6c-131">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="33f6c-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="33f6c-132">顯示清單存在的測試。</span><span class="sxs-lookup"><span data-stu-id="33f6c-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="33f6c-133">**delobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-133">**delobj**</span></span>       | [<span data-ttu-id="33f6c-134">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="33f6c-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="33f6c-135">刪除連續的顯示清單群組。</span><span class="sxs-lookup"><span data-stu-id="33f6c-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="33f6c-136">**genobj**</span><span class="sxs-lookup"><span data-stu-id="33f6c-136">**genobj**</span></span>       | [<span data-ttu-id="33f6c-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="33f6c-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="33f6c-138">產生指定數目的連續空白顯示清單。</span><span class="sxs-lookup"><span data-stu-id="33f6c-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="33f6c-139">本主題包含下列各項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33f6c-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="33f6c-140">移植 bbox2 函式</span><span class="sxs-lookup"><span data-stu-id="33f6c-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="33f6c-141">移植已編輯的顯示清單</span><span class="sxs-lookup"><span data-stu-id="33f6c-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="33f6c-142">顯示清單的範例埠</span><span class="sxs-lookup"><span data-stu-id="33f6c-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 




