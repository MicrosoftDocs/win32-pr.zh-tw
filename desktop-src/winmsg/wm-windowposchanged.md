---
description: 當呼叫 SetWindowPos 函式或另一個視窗管理函式時，傳送至 Z 順序的大小、位置或位置的視窗已變更。
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: 'WM_WINDOWPOSCHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112841"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="674b1-103">WM \_ WINDOWPOSCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="674b1-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="674b1-104">當呼叫 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) 函式或另一個視窗管理函式時，傳送至 Z 順序的大小、位置或位置的視窗已變更。</span><span class="sxs-lookup"><span data-stu-id="674b1-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="674b1-105">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="674b1-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="674b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="674b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="674b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="674b1-108">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="674b1-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="674b1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="674b1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="674b1-110">[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)結構的指標，其中包含視窗新大小和位置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="674b1-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="674b1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="674b1-111">Return value</span></span>

<span data-ttu-id="674b1-112">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="674b1-112">Type: **LRESULT**</span></span>

<span data-ttu-id="674b1-113">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="674b1-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="674b1-114">備註</span><span class="sxs-lookup"><span data-stu-id="674b1-114">Remarks</span></span>

<span data-ttu-id="674b1-115">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會傳送 [**Wm \_ 大小**](wm-size.md) 和 [**WM \_ 將訊息移**](wm-move.md) 至視窗。</span><span class="sxs-lookup"><span data-stu-id="674b1-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="674b1-116">如果應用程式在不呼叫 **DefWindowProc** 的情況下處理 **wm \_ WINDOWPOSCHANGED** 訊息，則不會傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。</span><span class="sxs-lookup"><span data-stu-id="674b1-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="674b1-117">在不呼叫 **DefWindowProc** 的情況下，于 **WM \_ WINDOWPOSCHANGED** 訊息中執行任何移動或大小變更處理會更有效率。</span><span class="sxs-lookup"><span data-stu-id="674b1-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="674b1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="674b1-118">Requirements</span></span>



| <span data-ttu-id="674b1-119">需求</span><span class="sxs-lookup"><span data-stu-id="674b1-119">Requirement</span></span> | <span data-ttu-id="674b1-120">值</span><span class="sxs-lookup"><span data-stu-id="674b1-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="674b1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="674b1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="674b1-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="674b1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="674b1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="674b1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="674b1-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="674b1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="674b1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="674b1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="674b1-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="674b1-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674b1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="674b1-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="674b1-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="674b1-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="674b1-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="674b1-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="674b1-130">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="674b1-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="674b1-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="674b1-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="674b1-132">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="674b1-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="674b1-133">**WM \_ 移動**</span><span class="sxs-lookup"><span data-stu-id="674b1-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="674b1-134">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="674b1-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="674b1-135">**WM \_ WINDOWPOSCHANGING**</span><span class="sxs-lookup"><span data-stu-id="674b1-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="674b1-136">**概念**</span><span class="sxs-lookup"><span data-stu-id="674b1-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="674b1-137">Windows</span><span class="sxs-lookup"><span data-stu-id="674b1-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
