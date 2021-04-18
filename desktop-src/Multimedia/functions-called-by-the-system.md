---
title: 系統呼叫的函式
description: 系統呼叫的函式
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- 多媒體音訊、正常運作
- 音訊、等式函數
- 音訊壓縮管理員 (的功能) 、函式
- " (音訊壓縮管理員) 、函式、功能"
- 進行的函數
- 回呼函式
- 音訊壓縮管理員 (的功能) 、回呼函式
- " (的音訊壓縮管理員) 、回呼函式"
- 攔截程式
- 驅動程式程式
- 音訊壓縮管理員 (的) 、攔截程式
- " (的音效壓縮管理員) 、攔截程式"
- 音訊壓縮管理員 (等量) ，驅動程式程式
- " (音訊壓縮管理員) 的驅動程式程式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968695"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="528c5-117">系統呼叫的函式</span><span class="sxs-lookup"><span data-stu-id="528c5-117">Functions Called by the System</span></span>

<span data-ttu-id="528c5-118">系統會呼叫三種不同類型的應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="528c5-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="528c5-119">回呼函式是您應用程式中的函式，系統會呼叫此函式以回應應用程式所提出的要求。</span><span class="sxs-lookup"><span data-stu-id="528c5-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="528c5-120">攔截程式可協助應用程式處理對話方塊的自訂。</span><span class="sxs-lookup"><span data-stu-id="528c5-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="528c5-121">驅動程式是應用程式本身的編解碼器、轉換器或篩選器的實作為。</span><span class="sxs-lookup"><span data-stu-id="528c5-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="528c5-122">回呼函數具有下列名稱：</span><span class="sxs-lookup"><span data-stu-id="528c5-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="528c5-123">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="528c5-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="528c5-124">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="528c5-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="528c5-125">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="528c5-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="528c5-126">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="528c5-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="528c5-127">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="528c5-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="528c5-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="528c5-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="528c5-129">使用中的大部分列舉函數都會使用回呼函數。</span><span class="sxs-lookup"><span data-stu-id="528c5-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="528c5-130">例如，當您呼叫列舉函式時，會透過回呼函數重複呼叫應用程式來列舉專案。</span><span class="sxs-lookup"><span data-stu-id="528c5-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="528c5-131">某些函式無法從這些回呼函數中呼叫。</span><span class="sxs-lookup"><span data-stu-id="528c5-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="528c5-132">無法呼叫的函式會操控列舉函式所使用的內部的型式結構。</span><span class="sxs-lookup"><span data-stu-id="528c5-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="528c5-133">下列函式不應該從回呼函數中呼叫：</span><span class="sxs-lookup"><span data-stu-id="528c5-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="528c5-134">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="528c5-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="528c5-135">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="528c5-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="528c5-136">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="528c5-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="528c5-137">系統會呼叫下列函數來協助應用程式處理對話方塊的自訂：</span><span class="sxs-lookup"><span data-stu-id="528c5-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="528c5-138">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="528c5-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="528c5-139">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="528c5-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="528c5-140">下列函式會指定為可讓應用程式使用自訂編解碼器、轉換器或篩選準則的原型。</span><span class="sxs-lookup"><span data-stu-id="528c5-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="528c5-141">符合這個原型的函式可能會做為引數傳遞至 [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) 函數。</span><span class="sxs-lookup"><span data-stu-id="528c5-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="528c5-142">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="528c5-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 