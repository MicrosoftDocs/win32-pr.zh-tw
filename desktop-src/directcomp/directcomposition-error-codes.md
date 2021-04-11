---
title: 'DirectComposition 錯誤碼 (Dcomp) '
description: 本節說明 DirectComposition 特有的錯誤碼。
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104892"
---
# <a name="directcomposition-error-codes"></a><span data-ttu-id="bf2f7-103">DirectComposition 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bf2f7-103">DirectComposition error codes</span></span>

<span data-ttu-id="bf2f7-104">如果發生錯誤，Microsoft DirectComposition 會以 **HRESULT** 值傳回程序代碼。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-104">If an error occurs, Microsoft DirectComposition returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="bf2f7-105">本節說明 DirectComposition 特有的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-105">This section describes the error codes that are specific to DirectComposition.</span></span> <span data-ttu-id="bf2f7-106">如需 (COM) 錯誤碼的一般元件物件模型清單，請參閱 [Com 錯誤碼](/windows/desktop/com/com-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-106">For a list of general Component Object Model (COM) error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bf2f7-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_ \_ 拒絕存取 DCOMPOSITION \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-107"><span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**DCOMPOSITION\_ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="bf2f7-108"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bf2f7-108"><dt>


</dt> <dt></span></span>



<span data-ttu-id="bf2f7-109">在 [**IDCompositionDevice：： CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) 方法的呼叫中指定的視窗控制碼，屬於建立裝置物件的不同處理常式。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-109">The window handle that was specified in a call to the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method belongs to a different process from the one that created the device object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf2f7-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-110"><span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="bf2f7-111"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bf2f7-111"><dt>


</dt> <dt></span></span>



<span data-ttu-id="bf2f7-112">當應用程式呼叫 [**IDCompositionSurface：： BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)、 [**IDCompositionSurface：： SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)或 [**IDCompositionSurface：： ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) 方法時，介面已經呈現。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-112">The surface was already being rendered when the application called the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), or [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) method.</span></span> <span data-ttu-id="bf2f7-113">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-113">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf2f7-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_ \_ \_ 未 \_ \_ 呈現 DCOMPOSITION 錯誤介面**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-114"><span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="bf2f7-115"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bf2f7-115"><dt>


</dt> <dt></span></span>



<span data-ttu-id="bf2f7-116">應用程式針對未轉譯的介面呼叫 [**IDCompositionSurface：： SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)、 [**IDCompositionSurface：： ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)或 [**IDCompositionSurface：： EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 方法。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-116">The application called the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw), or [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) method for a surface that is not being rendered.</span></span> <span data-ttu-id="bf2f7-117">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-117">For more information, see Remarks.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bf2f7-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION \_ 錯誤 \_ 視窗 \_ 已 \_ 組成**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-118"><span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**DCOMPOSITION\_ERROR\_WINDOW\_ALREADY\_COMPOSED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="bf2f7-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bf2f7-119"><dt>


</dt> <dt></span></span>



<span data-ttu-id="bf2f7-120">[**IDCompositionDevice：： CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd)方法是使用 *hwnd* 和 *最上層* 的參數（視覺化樹狀結構已存在）來呼叫。</span><span class="sxs-lookup"><span data-stu-id="bf2f7-120">The [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method was called with *hwnd* and *topmost* parameters for which a visual tree already exists.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf2f7-121">備註</span><span class="sxs-lookup"><span data-stu-id="bf2f7-121">Remarks</span></span>

<span data-ttu-id="bf2f7-122">如果 [**IDCompositionSurface：： BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) 的呼叫是最新的動作：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-122">If a call to the [**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) was the most recent action:</span></span>



| <span data-ttu-id="bf2f7-123">呼叫這個方法：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-123">Calling this method:</span></span>                                    | <span data-ttu-id="bf2f7-124">傳回此值：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-124">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="bf2f7-125">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-125">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="bf2f7-126">**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-126">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="bf2f7-127">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-127">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="bf2f7-128">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-128">S\_OK</span></span>                                             |
| [<span data-ttu-id="bf2f7-129">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-129">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="bf2f7-130">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-130">S\_OK</span></span>                                             |
| [<span data-ttu-id="bf2f7-131">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-131">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="bf2f7-132">**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-132">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |



 

<span data-ttu-id="bf2f7-133">如果 [**IDCompositionSurface：： SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) 的呼叫是最新的動作：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-133">If a call to the [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) was the most recent action:</span></span>



| <span data-ttu-id="bf2f7-134">呼叫這個方法：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-134">Calling this method:</span></span>                                    | <span data-ttu-id="bf2f7-135">傳回此值：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-135">Returns this value:</span></span>                               |
|---------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="bf2f7-136">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-136">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="bf2f7-137">**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-137">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="bf2f7-138">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-138">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="bf2f7-139">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-139">S\_OK</span></span>                                             |
| [<span data-ttu-id="bf2f7-140">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-140">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="bf2f7-141">**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-141">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span> |
| [<span data-ttu-id="bf2f7-142">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-142">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="bf2f7-143">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-143">S\_OK</span></span>                                             |



 

<span data-ttu-id="bf2f7-144">如果 [**IDCompositionSurface：： ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) 的呼叫是最新的動作：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-144">If a call to the [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) was the most recent action:</span></span>



| <span data-ttu-id="bf2f7-145">呼叫這個方法：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-145">Calling this method:</span></span>                                    | <span data-ttu-id="bf2f7-146">傳回此值：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-146">Returns this value:</span></span>                                |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bf2f7-147">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-147">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="bf2f7-148">**\_正在轉譯的 DCOMPOSITION 錯誤 \_ 介面 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-148">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED**</span></span>  |
| [<span data-ttu-id="bf2f7-149">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-149">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="bf2f7-150">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-150">S\_OK</span></span>                                              |
| [<span data-ttu-id="bf2f7-151">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-151">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="bf2f7-152">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-152">S\_OK</span></span>                                              |
| [<span data-ttu-id="bf2f7-153">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-153">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="bf2f7-154">**\_ \_ 正在呈現 DCOMPOSITION 錯誤介面 \_ \_ 。**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-154">**DCOMPOSITION\_ERROR\_SURFACE\_BEING\_RENDERED.**</span></span> |



 

<span data-ttu-id="bf2f7-155">如果 [**IDCompositionSurface：： EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 的呼叫是最新的動作：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-155">If a call to the [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) was the most recent action:</span></span>



| <span data-ttu-id="bf2f7-156">呼叫這個方法：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-156">Calling this method:</span></span>                                    | <span data-ttu-id="bf2f7-157">傳回此值：</span><span class="sxs-lookup"><span data-stu-id="bf2f7-157">Returns this value:</span></span>                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="bf2f7-158">**BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-158">**BeginDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | <span data-ttu-id="bf2f7-159">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="bf2f7-159">S\_OK</span></span>                                                   |
| [<span data-ttu-id="bf2f7-160">**EndDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-160">**EndDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | <span data-ttu-id="bf2f7-161">**DCOMPOSITION \_ 錯誤 \_ 介面 \_ 未 \_ \_ 呈現。**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-161">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="bf2f7-162">**SuspendDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-162">**SuspendDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | <span data-ttu-id="bf2f7-163">**DCOMPOSITION \_ 錯誤 \_ 介面 \_ 未 \_ \_ 呈現。**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-163">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |
| [<span data-ttu-id="bf2f7-164">**ResumeDraw**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-164">**ResumeDraw**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | <span data-ttu-id="bf2f7-165">**DCOMPOSITION \_ 錯誤 \_ 介面 \_ 未 \_ \_ 呈現。**</span><span class="sxs-lookup"><span data-stu-id="bf2f7-165">**DCOMPOSITION\_ERROR\_SURFACE\_NOT\_BEING\_RENDERED.**</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bf2f7-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf2f7-166">Requirements</span></span>



| <span data-ttu-id="bf2f7-167">需求</span><span class="sxs-lookup"><span data-stu-id="bf2f7-167">Requirement</span></span> | <span data-ttu-id="bf2f7-168">值</span><span class="sxs-lookup"><span data-stu-id="bf2f7-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2f7-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf2f7-169">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2f7-170">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf2f7-170">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bf2f7-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf2f7-171">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2f7-172">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf2f7-172">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bf2f7-173">標頭</span><span class="sxs-lookup"><span data-stu-id="bf2f7-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2f7-174"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2f7-174"><dt>Dcomp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2f7-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf2f7-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2f7-176">DirectComposition 參考</span><span class="sxs-lookup"><span data-stu-id="bf2f7-176">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

