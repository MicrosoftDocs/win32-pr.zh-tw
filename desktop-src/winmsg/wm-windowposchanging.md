---
description: 傳送至 Z 順序中大小、位置或位置的視窗，即將因呼叫 SetWindowPos 函式或其他視窗管理函式而變更。
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: 'WM_WINDOWPOSCHANGING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694283"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="bc47f-103">WM \_ WINDOWPOSCHANGING 訊息</span><span class="sxs-lookup"><span data-stu-id="bc47f-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="bc47f-104">傳送至 Z 順序中大小、位置或位置的視窗，即將因呼叫 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 函式或其他視窗管理函式而變更。</span><span class="sxs-lookup"><span data-stu-id="bc47f-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="bc47f-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="bc47f-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="bc47f-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc47f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc47f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc47f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc47f-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="bc47f-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc47f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc47f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc47f-110">[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)結構的指標，其中包含視窗新大小和位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc47f-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc47f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc47f-111">Return value</span></span>

<span data-ttu-id="bc47f-112">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc47f-112">Type: **LRESULT**</span></span>

<span data-ttu-id="bc47f-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="bc47f-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc47f-114">備註</span><span class="sxs-lookup"><span data-stu-id="bc47f-114">Remarks</span></span>

<span data-ttu-id="bc47f-115">若為具有 Ws 重 [**迭 \_**](window-styles.md) 或 **ws \_ THICKFRAME** 樣式的視窗， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將 [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="bc47f-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="bc47f-116">這樣做的目的是要驗證視窗的新大小和位置，以及強制執行 [cs \_ BYTEALIGNCLIENT](about-window-classes.md) 和 cs \_ BYTEALIGNWINDOW 用戶端樣式。</span><span class="sxs-lookup"><span data-stu-id="bc47f-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="bc47f-117">藉由不將 **WM \_ WINDOWPOSCHANGING** 訊息傳遞給 **DefWindowProc** 函數，應用程式可以覆寫這些預設值。</span><span class="sxs-lookup"><span data-stu-id="bc47f-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="bc47f-118">在處理此訊息時，修改 [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) 中的任何值會影響視窗的新大小、位置或位置（以 Z 順序表示）。</span><span class="sxs-lookup"><span data-stu-id="bc47f-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="bc47f-119">應用程式可以藉由設定或清除 **WINDOWPOS\*\*\*\*旗標** 成員中的適當位，來防止視窗的變更。</span><span class="sxs-lookup"><span data-stu-id="bc47f-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc47f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc47f-120">Requirements</span></span>



| <span data-ttu-id="bc47f-121">需求</span><span class="sxs-lookup"><span data-stu-id="bc47f-121">Requirement</span></span> | <span data-ttu-id="bc47f-122">值</span><span class="sxs-lookup"><span data-stu-id="bc47f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc47f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc47f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bc47f-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc47f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bc47f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc47f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bc47f-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc47f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc47f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="bc47f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc47f-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="bc47f-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc47f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc47f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc47f-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="bc47f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc47f-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bc47f-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bc47f-132">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="bc47f-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="bc47f-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="bc47f-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="bc47f-134">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="bc47f-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="bc47f-135">**WM \_ GETMINMAXINFO**</span><span class="sxs-lookup"><span data-stu-id="bc47f-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="bc47f-136">**WM \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="bc47f-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="bc47f-137">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="bc47f-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="bc47f-138">**WM \_ WINDOWPOSCHANGED**</span><span class="sxs-lookup"><span data-stu-id="bc47f-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="bc47f-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="bc47f-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc47f-140">Windows</span><span class="sxs-lookup"><span data-stu-id="bc47f-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
