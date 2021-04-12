---
description: 當視窗啟用時，傳送至應用程式。 視窗會透過其 WindowProc 函數接收此訊息。
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: 'WM_IME_SETCONTEXT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191379"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="2d316-104">WM \_ 輸入法 \_ SETCONTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="2d316-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="2d316-105">當視窗啟用時，傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="2d316-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="2d316-106">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="2d316-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="2d316-107">參數</span><span class="sxs-lookup"><span data-stu-id="2d316-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d316-108">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="2d316-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2d316-109">視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2d316-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="2d316-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d316-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d316-111">如果視窗為使用中，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="2d316-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="2d316-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d316-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d316-113">顯示選項。</span><span class="sxs-lookup"><span data-stu-id="2d316-113">Display options.</span></span> <span data-ttu-id="2d316-114">這個參數可以有下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="2d316-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="2d316-115">值</span><span class="sxs-lookup"><span data-stu-id="2d316-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="2d316-116">意義</span><span class="sxs-lookup"><span data-stu-id="2d316-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="2d316-117"><dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="2d316-118">依使用者介面視窗顯示撰寫視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="2d316-119"><dt>**ISC \_ SHOWUIGUIDWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="2d316-120">依使用者介面視窗顯示 [節目表] 視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="2d316-121"><dt>**ISC \_ SHOWUISOFTKBD**</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="2d316-122">依使用者介面視窗顯示 [螢幕小鍵盤]。</span><span class="sxs-lookup"><span data-stu-id="2d316-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="2d316-123"><dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="2d316-124">依使用者介面視窗顯示索引0的候選視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="2d316-125"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="2d316-126">依使用者介面視窗顯示索引1的候選視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="2d316-127"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="2d316-128">依使用者介面視窗顯示索引2的候選視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="2d316-129"><dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt></span><span class="sxs-lookup"><span data-stu-id="2d316-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="2d316-130">依使用者介面視窗顯示索引3的候選視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d316-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d316-131">Return value</span></span>

<span data-ttu-id="2d316-132">傳回 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 或 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="2d316-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d316-133">備註</span><span class="sxs-lookup"><span data-stu-id="2d316-133">Remarks</span></span>

<span data-ttu-id="2d316-134">如果應用程式已建立 IME 視窗，則應該呼叫 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)。</span><span class="sxs-lookup"><span data-stu-id="2d316-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="2d316-135">否則，它應該會將此訊息傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="2d316-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="2d316-136">如果應用程式繪製組合視窗，預設的 IME 視窗就不需要顯示其撰寫視窗。</span><span class="sxs-lookup"><span data-stu-id="2d316-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="2d316-137">在此情況下，應用程式必須先從 *lParam* 參數清除 **ISC \_ SHOWUICOMPOSITIONWINDOW** 值，然後再將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)或 [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)。</span><span class="sxs-lookup"><span data-stu-id="2d316-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="2d316-138">若要顯示特定的使用者介面視窗，應用程式應該移除對應的值，使 IME 不會顯示該值。</span><span class="sxs-lookup"><span data-stu-id="2d316-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d316-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d316-139">Requirements</span></span>



| <span data-ttu-id="2d316-140">需求</span><span class="sxs-lookup"><span data-stu-id="2d316-140">Requirement</span></span> | <span data-ttu-id="2d316-141">值</span><span class="sxs-lookup"><span data-stu-id="2d316-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d316-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d316-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2d316-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d316-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="2d316-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d316-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2d316-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d316-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="2d316-146">標頭</span><span class="sxs-lookup"><span data-stu-id="2d316-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d316-147"><dt>Winuser (包含 Windows .h) ;</dt><dt>Imm (包括 Windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2d316-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d316-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d316-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d316-149">輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="2d316-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="2d316-150">輸入方法管理員訊息</span><span class="sxs-lookup"><span data-stu-id="2d316-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="2d316-151">**ImmIsUIMessage**</span><span class="sxs-lookup"><span data-stu-id="2d316-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
