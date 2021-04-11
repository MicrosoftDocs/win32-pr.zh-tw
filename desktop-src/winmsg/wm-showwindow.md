---
description: 當視窗即將隱藏或顯示時，傳送至視窗。
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: 'WM_SHOWWINDOW 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319204"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="e103d-103">WM \_ SHOWWINDOW 訊息</span><span class="sxs-lookup"><span data-stu-id="e103d-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="e103d-104">當視窗即將隱藏或顯示時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="e103d-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e103d-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="e103d-106">參數</span><span class="sxs-lookup"><span data-stu-id="e103d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e103d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e103d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e103d-108">指出是否顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="e103d-109">如果 *wParam* 為 **TRUE**，則會顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="e103d-110">如果 *wParam* 為 **FALSE**，則會隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="e103d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e103d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e103d-112">所顯示視窗的狀態。</span><span class="sxs-lookup"><span data-stu-id="e103d-112">The status of the window being shown.</span></span> <span data-ttu-id="e103d-113">如果 *lParam* 為零，則會因為呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函數而傳送訊息;否則， *lParam* 是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e103d-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="e103d-114">值</span><span class="sxs-lookup"><span data-stu-id="e103d-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="e103d-115">意義</span><span class="sxs-lookup"><span data-stu-id="e103d-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="e103d-116"><dt>**SW \_OTHERUNZOOM**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e103d-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="e103d-117">因為已還原或最小化視窗，所以正在發現視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="e103d-118"><dt>**SW \_OTHERZOOM**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e103d-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="e103d-119">視窗正由另一個已最大化的視窗所涵蓋。</span><span class="sxs-lookup"><span data-stu-id="e103d-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="e103d-120"><dt>**SW \_PARENTCLOSING**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e103d-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e103d-121">視窗的擁有者視窗會最小化。</span><span class="sxs-lookup"><span data-stu-id="e103d-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="e103d-122"><dt>**SW \_PARENTOPENING**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e103d-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e103d-123">正在還原視窗的擁有者視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e103d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="e103d-124">Return value</span></span>

<span data-ttu-id="e103d-125">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e103d-125">Type: **LRESULT**</span></span>

<span data-ttu-id="e103d-126">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e103d-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e103d-127">備註</span><span class="sxs-lookup"><span data-stu-id="e103d-127">Remarks</span></span>

<span data-ttu-id="e103d-128">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會依訊息的指定，隱藏或顯示視窗。</span><span class="sxs-lookup"><span data-stu-id="e103d-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="e103d-129">如果視窗在建立時有 [**WS \_ 可見**](window-styles.md) 的樣式，則視窗會在建立之後，但在顯示之前接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e103d-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="e103d-130">當 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 或 [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) 函式變更其可見度狀態時，視窗也會收到此訊息。</span><span class="sxs-lookup"><span data-stu-id="e103d-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="e103d-131">在下列情況下，不會傳送 **WM \_ SHOWWINDOW** 訊息：</span><span class="sxs-lookup"><span data-stu-id="e103d-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="e103d-132">使用 [**ws \_ 最大化**](window-styles.md) 或 **ws \_ 最小化** 樣式建立最上層的重迭視窗時。</span><span class="sxs-lookup"><span data-stu-id="e103d-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="e103d-133">在 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)函數的呼叫中指定 **SW \_ SHOWNORMAL** 旗標時。</span><span class="sxs-lookup"><span data-stu-id="e103d-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e103d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e103d-134">Requirements</span></span>



| <span data-ttu-id="e103d-135">需求</span><span class="sxs-lookup"><span data-stu-id="e103d-135">Requirement</span></span> | <span data-ttu-id="e103d-136">值</span><span class="sxs-lookup"><span data-stu-id="e103d-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e103d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e103d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e103d-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e103d-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e103d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e103d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e103d-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e103d-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e103d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="e103d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e103d-142"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e103d-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e103d-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e103d-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="e103d-144">**參考**</span><span class="sxs-lookup"><span data-stu-id="e103d-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e103d-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e103d-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e103d-146">**ShowOwnedPopups**</span><span class="sxs-lookup"><span data-stu-id="e103d-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="e103d-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="e103d-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="e103d-148">**概念**</span><span class="sxs-lookup"><span data-stu-id="e103d-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e103d-149">Windows</span><span class="sxs-lookup"><span data-stu-id="e103d-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
