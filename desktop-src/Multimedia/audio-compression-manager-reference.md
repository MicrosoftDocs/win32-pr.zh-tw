---
title: 音訊壓縮管理員參考
description: 音訊壓縮管理員參考
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows 多媒體、進行中的參考
- 多媒體、進行中的參考
- 多媒體音訊、進行中的參考
- '音訊、進行中的參考) '
- 音訊壓縮管理員 (的) ，參考
- " (音效壓縮管理員) ，參考"
- 資訊相關參考，關於
- 對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d365b0a69ecd94a07811b24762aa4bffdc8c9f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507871"
---
# <a name="audio-compression-manager-reference"></a><span data-ttu-id="39492-111">音訊壓縮管理員參考</span><span class="sxs-lookup"><span data-stu-id="39492-111">Audio Compression Manager Reference</span></span>

<span data-ttu-id="39492-112">本章節描述與此架構相關聯的函式、結構和訊息。</span><span class="sxs-lookup"><span data-stu-id="39492-112">This section describes the functions, structures, and messages associated with the ACM.</span></span> <span data-ttu-id="39492-113">這些元素的分組方式如下。</span><span class="sxs-lookup"><span data-stu-id="39492-113">These elements are grouped as follows.</span></span>

## <a name="drivers"></a><span data-ttu-id="39492-114">驅動程式</span><span class="sxs-lookup"><span data-stu-id="39492-114">Drivers</span></span>

-   [<span data-ttu-id="39492-115">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="39492-115">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="39492-116">**acmDriverClose**</span><span class="sxs-lookup"><span data-stu-id="39492-116">**acmDriverClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [<span data-ttu-id="39492-117">**ACMDRIVERDETAILS**</span><span class="sxs-lookup"><span data-stu-id="39492-117">**ACMDRIVERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [<span data-ttu-id="39492-118">**acmDriverEnum**</span><span class="sxs-lookup"><span data-stu-id="39492-118">**acmDriverEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [<span data-ttu-id="39492-119">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="39492-119">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="39492-120">**acmDriverID**</span><span class="sxs-lookup"><span data-stu-id="39492-120">**acmDriverID**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [<span data-ttu-id="39492-121">**acmDriverMessage**</span><span class="sxs-lookup"><span data-stu-id="39492-121">**acmDriverMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [<span data-ttu-id="39492-122">**acmDriverOpen**</span><span class="sxs-lookup"><span data-stu-id="39492-122">**acmDriverOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [<span data-ttu-id="39492-123">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="39492-123">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="39492-124">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="39492-124">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [<span data-ttu-id="39492-125">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="39492-125">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a><span data-ttu-id="39492-126">篩選器</span><span class="sxs-lookup"><span data-stu-id="39492-126">Filters</span></span>

-   [<span data-ttu-id="39492-127">**ACMFILTERCHOOSE**</span><span class="sxs-lookup"><span data-stu-id="39492-127">**ACMFILTERCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [<span data-ttu-id="39492-128">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="39492-128">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="39492-129">**ACMFILTERDETAILS**</span><span class="sxs-lookup"><span data-stu-id="39492-129">**ACMFILTERDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [<span data-ttu-id="39492-130">**acmFilterEnum**</span><span class="sxs-lookup"><span data-stu-id="39492-130">**acmFilterEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [<span data-ttu-id="39492-131">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="39492-131">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="39492-132">**ACMFILTERTAGDETAILS**</span><span class="sxs-lookup"><span data-stu-id="39492-132">**ACMFILTERTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [<span data-ttu-id="39492-133">**acmFilterTagEnum**</span><span class="sxs-lookup"><span data-stu-id="39492-133">**acmFilterTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [<span data-ttu-id="39492-134">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="39492-134">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a><span data-ttu-id="39492-135">格式</span><span class="sxs-lookup"><span data-stu-id="39492-135">Formats</span></span>

-   [<span data-ttu-id="39492-136">**ACMFORMATCHOOSE**</span><span class="sxs-lookup"><span data-stu-id="39492-136">**ACMFORMATCHOOSE**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [<span data-ttu-id="39492-137">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="39492-137">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [<span data-ttu-id="39492-138">**ACMFORMATDETAILS**</span><span class="sxs-lookup"><span data-stu-id="39492-138">**ACMFORMATDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [<span data-ttu-id="39492-139">**acmFormatEnum**</span><span class="sxs-lookup"><span data-stu-id="39492-139">**acmFormatEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [<span data-ttu-id="39492-140">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="39492-140">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="39492-141">**acmFormatSuggest**</span><span class="sxs-lookup"><span data-stu-id="39492-141">**acmFormatSuggest**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [<span data-ttu-id="39492-142">**ACMFORMATTAGDETAILS**</span><span class="sxs-lookup"><span data-stu-id="39492-142">**ACMFORMATTAGDETAILS**</span></span>](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [<span data-ttu-id="39492-143">**acmFormatTagEnum**</span><span class="sxs-lookup"><span data-stu-id="39492-143">**acmFormatTagEnum**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [<span data-ttu-id="39492-144">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="39492-144">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a><span data-ttu-id="39492-145">訊息</span><span class="sxs-lookup"><span data-stu-id="39492-145">Messages</span></span>

-   [<span data-ttu-id="39492-146">**MM \_ \_ FILTERCHOOSE**</span><span class="sxs-lookup"><span data-stu-id="39492-146">**MM\_ACM\_FILTERCHOOSE**</span></span>](mm-acm-filterchoose.md)
-   [<span data-ttu-id="39492-147">**MM \_ \_ FORMATCHOOSE**</span><span class="sxs-lookup"><span data-stu-id="39492-147">**MM\_ACM\_FORMATCHOOSE**</span></span>](mm-acm-formatchoose.md)

## <a name="streams"></a><span data-ttu-id="39492-148">串流</span><span class="sxs-lookup"><span data-stu-id="39492-148">Streams</span></span>

-   [<span data-ttu-id="39492-149">**acmStreamClose**</span><span class="sxs-lookup"><span data-stu-id="39492-149">**acmStreamClose**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [<span data-ttu-id="39492-150">**acmStreamConvert**</span><span class="sxs-lookup"><span data-stu-id="39492-150">**acmStreamConvert**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   <span data-ttu-id="39492-151">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="39492-151">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>
-   [<span data-ttu-id="39492-152">**ACMSTREAMHEADER**</span><span class="sxs-lookup"><span data-stu-id="39492-152">**ACMSTREAMHEADER**</span></span>](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [<span data-ttu-id="39492-153">**acmStreamMessage**</span><span class="sxs-lookup"><span data-stu-id="39492-153">**acmStreamMessage**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [<span data-ttu-id="39492-154">**acmStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="39492-154">**acmStreamOpen**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [<span data-ttu-id="39492-155">**acmStreamPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="39492-155">**acmStreamPrepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [<span data-ttu-id="39492-156">**acmStreamReset**</span><span class="sxs-lookup"><span data-stu-id="39492-156">**acmStreamReset**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [<span data-ttu-id="39492-157">**acmStreamSize**</span><span class="sxs-lookup"><span data-stu-id="39492-157">**acmStreamSize**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [<span data-ttu-id="39492-158">**acmStreamUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="39492-158">**acmStreamUnprepareHeader**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a><span data-ttu-id="39492-159">其他</span><span class="sxs-lookup"><span data-stu-id="39492-159">Miscellaneous</span></span>

-   [<span data-ttu-id="39492-160">**acmGetVersion**</span><span class="sxs-lookup"><span data-stu-id="39492-160">**acmGetVersion**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [<span data-ttu-id="39492-161">**acmMetrics**</span><span class="sxs-lookup"><span data-stu-id="39492-161">**acmMetrics**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a><span data-ttu-id="39492-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="39492-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39492-163">音訊壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="39492-163">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> </dl>

 

 