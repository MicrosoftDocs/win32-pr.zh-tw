---
title: 移植樣板平面呼叫
description: 在 OpenGL 中，您可以使用 OpenGL auxInitDisplayMode 或 ChoosePixelFormat 要求適當的像素格式來配置樣板平面。
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- 鳶尾花 GL 移植，樣板平面
- 從鳶尾花 GL、樣板平面移植
- 從鳶尾花 GL、樣板平面移植至 OpenGL
- 從鳶尾花 GL、樣板平面移植的 OpenGL
- 樣板平面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301379"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="d03ec-108">移植樣板平面呼叫</span><span class="sxs-lookup"><span data-stu-id="d03ec-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="d03ec-109">在 OpenGL 中，您可以使用 OpenGL **auxInitDisplayMode** 或 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)要求適當的像素格式來配置樣板平面。</span><span class="sxs-lookup"><span data-stu-id="d03ec-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="d03ec-110">功能。</span><span class="sxs-lookup"><span data-stu-id="d03ec-110">functions.</span></span> <span data-ttu-id="d03ec-111">下表列出會影響樣板平面及其對等 OpenGL 函式的鳶尾花 GL 函數。</span><span class="sxs-lookup"><span data-stu-id="d03ec-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d03ec-112">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="d03ec-112">IRIS GL function</span></span>             | <span data-ttu-id="d03ec-113">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="d03ec-113">OpenGL function</span></span>                                         | <span data-ttu-id="d03ec-114">意義</span><span class="sxs-lookup"><span data-stu-id="d03ec-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="d03ec-115">**stensize**</span><span class="sxs-lookup"><span data-stu-id="d03ec-115">**stensize**</span></span>                 | <span data-ttu-id="d03ec-116">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="d03ec-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="d03ec-117">樣板 ( **TRUE**，... ) </span><span class="sxs-lookup"><span data-stu-id="d03ec-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="d03ec-118">[**glEnable**](glenable.md) ( GL \_ 樣板 \_ 測試 ) </span><span class="sxs-lookup"><span data-stu-id="d03ec-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="d03ec-119">啟用樣板測試。</span><span class="sxs-lookup"><span data-stu-id="d03ec-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="d03ec-120">**模具**</span><span class="sxs-lookup"><span data-stu-id="d03ec-120">**stencil**</span></span>                  | [<span data-ttu-id="d03ec-121">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="d03ec-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="d03ec-122">設定樣板測試動作。</span><span class="sxs-lookup"><span data-stu-id="d03ec-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="d03ec-123">樣板 **( ...** func、... ) </span><span class="sxs-lookup"><span data-stu-id="d03ec-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="d03ec-124">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="d03ec-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="d03ec-125">設定樣板測試的函數和參考值。</span><span class="sxs-lookup"><span data-stu-id="d03ec-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="d03ec-126">**swritemask**</span><span class="sxs-lookup"><span data-stu-id="d03ec-126">**swritemask**</span></span>               | [<span data-ttu-id="d03ec-127">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="d03ec-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="d03ec-128">指定可寫入的範本位。</span><span class="sxs-lookup"><span data-stu-id="d03ec-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="d03ec-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="d03ec-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="d03ec-130">指定樣板緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="d03ec-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="d03ec-131">**sclear**</span><span class="sxs-lookup"><span data-stu-id="d03ec-131">**sclear**</span></span>                   | <span data-ttu-id="d03ec-132">[**glClear**](glclear.md) ( GL \_ 樣板 \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="d03ec-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="d03ec-133">樣板-比較函式和樣板通過/失敗作業在 OpenGL 和鳶尾花 GL 中幾乎相等。</span><span class="sxs-lookup"><span data-stu-id="d03ec-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="d03ec-134">鳶尾花 GL 樣板函式旗標前面會加上 SF;具有 GL 的 OpenGL 旗標。</span><span class="sxs-lookup"><span data-stu-id="d03ec-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="d03ec-135">鳶尾花 GL 通過/失敗作業旗標的開頭為 ST;具有 GL 的 OpenGL 旗標。</span><span class="sxs-lookup"><span data-stu-id="d03ec-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




