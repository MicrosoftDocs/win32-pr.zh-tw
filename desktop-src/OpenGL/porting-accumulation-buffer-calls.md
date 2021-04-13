---
title: 移植累積的緩衝區呼叫
description: 您必須向 OpenGL auxInitDisplayMode 或 ChoosePixelFormat 函數要求適當的像素格式，以配置累積緩衝區。
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- 鳶尾花 GL 移植，累積緩衝區
- 從鳶尾花 GL 進行移植，累積緩衝區
- 從鳶尾花 GL 移植至 OpenGL，累積緩衝區
- 鳶尾花 GL 的 OpenGL 移植，累積緩衝區
- 累積緩衝區 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184157"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="71801-108">移植累積的緩衝區呼叫</span><span class="sxs-lookup"><span data-stu-id="71801-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="71801-109">您必須向 OpenGL **auxInitDisplayMode** 或 [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) 函數要求適當的像素格式，以配置累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="71801-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="71801-110">下表列出會影響累積緩衝區的鳶尾花 GL 函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="71801-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="71801-111">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="71801-111">IRIS GL function</span></span>       | <span data-ttu-id="71801-112">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="71801-112">OpenGL function</span></span>                                       | <span data-ttu-id="71801-113">意義</span><span class="sxs-lookup"><span data-stu-id="71801-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="71801-114">**acsize**</span><span class="sxs-lookup"><span data-stu-id="71801-114">**acsize**</span></span>             | <span data-ttu-id="71801-115">**auxInitDisplayMode** 或 **ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="71801-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="71801-116">指定累積緩衝區中每個色彩元件的 bitplanes 數目。</span><span class="sxs-lookup"><span data-stu-id="71801-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="71801-117">**acbuf**</span><span class="sxs-lookup"><span data-stu-id="71801-117">**acbuf**</span></span>              | [<span data-ttu-id="71801-118">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="71801-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="71801-119">在累積緩衝區上運作。</span><span class="sxs-lookup"><span data-stu-id="71801-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="71801-120">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="71801-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="71801-121">設定累積緩衝區的明確值。</span><span class="sxs-lookup"><span data-stu-id="71801-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="71801-122">**acbuf** ( AC \_ CLEAR ) </span><span class="sxs-lookup"><span data-stu-id="71801-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="71801-123">[**glClear**](glclear.md) ( GL \_ ACCUM \_ 緩衝區 \_ 位 ) </span><span class="sxs-lookup"><span data-stu-id="71801-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="71801-124">清除累積緩衝區。</span><span class="sxs-lookup"><span data-stu-id="71801-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="71801-125">下表列出鳶尾花 GL **acbuf** 參數，以及相等的 OpenGL [**glAccum**](glaccum.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="71801-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="71801-126">鳶尾花 GL 參數</span><span class="sxs-lookup"><span data-stu-id="71801-126">IRIS GL parameter</span></span>     | <span data-ttu-id="71801-127">OpenGL 參數</span><span class="sxs-lookup"><span data-stu-id="71801-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="71801-128">AC \_ 累積</span><span class="sxs-lookup"><span data-stu-id="71801-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="71801-129">GL \_ ACCUM</span><span class="sxs-lookup"><span data-stu-id="71801-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="71801-130">AC \_ CLEAR \_ 累積</span><span class="sxs-lookup"><span data-stu-id="71801-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="71801-131">GL \_ 負載</span><span class="sxs-lookup"><span data-stu-id="71801-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="71801-132">AC \_ 退回</span><span class="sxs-lookup"><span data-stu-id="71801-132">AC\_RETURN</span></span>            | <span data-ttu-id="71801-133">GL \_ 退貨</span><span class="sxs-lookup"><span data-stu-id="71801-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="71801-134">AC \_ MULT</span><span class="sxs-lookup"><span data-stu-id="71801-134">AC\_MULT</span></span>              | <span data-ttu-id="71801-135">GL \_ MULT</span><span class="sxs-lookup"><span data-stu-id="71801-135">GL\_MULT</span></span>         |
| <span data-ttu-id="71801-136">AC \_ 新增</span><span class="sxs-lookup"><span data-stu-id="71801-136">AC\_ADD</span></span>               | <span data-ttu-id="71801-137">GL \_ 新增</span><span class="sxs-lookup"><span data-stu-id="71801-137">GL\_ADD</span></span>          |



 

 

 




