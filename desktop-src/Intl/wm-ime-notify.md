---
description: 傳送至應用程式，以通知它對 IME 視窗的變更。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: 'WM_IME_NOTIFY 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971221"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="6c2de-104">WM_IME_NOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="6c2de-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="6c2de-105">傳送至應用程式，以通知它對 IME 視窗的變更。</span><span class="sxs-lookup"><span data-stu-id="6c2de-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="6c2de-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="6c2de-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="6c2de-107">參數</span><span class="sxs-lookup"><span data-stu-id="6c2de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c2de-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="6c2de-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2de-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6c2de-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="6c2de-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c2de-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2de-111">命令。</span><span class="sxs-lookup"><span data-stu-id="6c2de-111">The command.</span></span> <span data-ttu-id="6c2de-112">這個參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6c2de-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="6c2de-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="6c2de-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="6c2de-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="6c2de-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c2de-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2de-127">命令特有的資料，其格式取決於 *wParam* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="6c2de-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="6c2de-128">如需詳細資訊，請參閱每個命令的說明文件。</span><span class="sxs-lookup"><span data-stu-id="6c2de-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c2de-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c2de-129">Return value</span></span>

<span data-ttu-id="6c2de-130">傳回值取決於傳送的命令。</span><span class="sxs-lookup"><span data-stu-id="6c2de-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2de-131">備註</span><span class="sxs-lookup"><span data-stu-id="6c2de-131">Remarks</span></span>

<span data-ttu-id="6c2de-132">如果應用程式負責管理 IME 視窗，則會處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="6c2de-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2de-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c2de-133">Requirements</span></span>



| <span data-ttu-id="6c2de-134">需求</span><span class="sxs-lookup"><span data-stu-id="6c2de-134">Requirement</span></span> | <span data-ttu-id="6c2de-135">值</span><span class="sxs-lookup"><span data-stu-id="6c2de-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2de-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c2de-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2de-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c2de-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="6c2de-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c2de-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2de-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c2de-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="6c2de-140">標頭</span><span class="sxs-lookup"><span data-stu-id="6c2de-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c2de-141"><dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6c2de-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2de-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c2de-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2de-143">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="6c2de-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6c2de-144">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="6c2de-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="6c2de-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="6c2de-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="6c2de-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="6c2de-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="6c2de-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="6c2de-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="6c2de-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="6c2de-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="6c2de-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="6c2de-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="6c2de-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="6c2de-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="6c2de-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="6c2de-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="6c2de-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="6c2de-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="6c2de-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="6c2de-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="6c2de-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="6c2de-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="6c2de-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="6c2de-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="6c2de-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="6c2de-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="6c2de-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="6c2de-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
