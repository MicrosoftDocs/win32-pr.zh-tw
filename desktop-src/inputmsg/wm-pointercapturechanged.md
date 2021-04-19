---
title: WM_POINTERCAPTURECHANGED 訊息
description: 傳送至遺失輸入指標之捕捉的視窗。
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966337"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="8be78-104">WM_POINTERCAPTURECHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="8be78-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="8be78-105">傳送至遺失輸入指標之捕捉的視窗。</span><span class="sxs-lookup"><span data-stu-id="8be78-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="8be78-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="8be78-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="8be78-107">參數</span><span class="sxs-lookup"><span data-stu-id="8be78-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be78-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8be78-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8be78-109">包含遺失之輸入指標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8be78-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="8be78-110">使用 [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) 取得指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="8be78-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="8be78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8be78-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8be78-112">包含正在捕捉輸入指標的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="8be78-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="8be78-113">如果該指標不再由視窗所捕捉，則這個值可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="8be78-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="8be78-114">如果此訊息是從內部處理產生的，則此值可以是接收訊息的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="8be78-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be78-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8be78-115">Return value</span></span>

<span data-ttu-id="8be78-116">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8be78-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="8be78-117">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="8be78-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="8be78-118">備註</span><span class="sxs-lookup"><span data-stu-id="8be78-118">Remarks</span></span>

<span data-ttu-id="8be78-119">視窗應該使用此通知來停止處理後續的訊息，並起始指標遺失所需的任何清除。</span><span class="sxs-lookup"><span data-stu-id="8be78-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="8be78-120">與指標相關聯的手勢的處理也應終止 (例如，呼叫 [**StopInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) 和剩餘的連絡人重新與視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="8be78-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="8be78-121">一般來說，如果視窗收到 **WM_POINTERCAPTURECHANGED** 通知，就不會收到與輸入指標相關的後續通知。</span><span class="sxs-lookup"><span data-stu-id="8be78-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="8be78-122">因此，請不要依賴成對的通知，例如 [**WM_POINTERENTER**](wm-pointerenter.md) 和 [**WM_POINTERLEAVE**](wm-pointerleave.md)。</span><span class="sxs-lookup"><span data-stu-id="8be78-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="8be78-123">**WM_POINTERCAPTURECHANGED** 不包含 [**POINTER_INFO**](/previous-versions/windows/desktop/api) 的資料。</span><span class="sxs-lookup"><span data-stu-id="8be78-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="8be78-124">除了設定的 [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) 旗標以外， [**GetPointerInfo**](/previous-versions/windows/desktop/api) (或任何變異) 所傳回的資料，與通知之前傳回的資料相同。</span><span class="sxs-lookup"><span data-stu-id="8be78-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="8be78-125">如果應用程式未處理此通知， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會產生一或多個 [**WM_GESTURE**](../wintouch/wm-gesture.md) 訊息，或者，如果無法辨識手勢， **DefWindowProc** 可能會產生滑鼠輸入。</span><span class="sxs-lookup"><span data-stu-id="8be78-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="8be78-126">如果應用程式選擇性地取用一些指標輸入，並將 rest 傳遞給 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)，則產生的行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8be78-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be78-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8be78-127">Requirements</span></span>



| <span data-ttu-id="8be78-128">需求</span><span class="sxs-lookup"><span data-stu-id="8be78-128">Requirement</span></span> | <span data-ttu-id="8be78-129">值</span><span class="sxs-lookup"><span data-stu-id="8be78-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be78-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8be78-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8be78-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8be78-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="8be78-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8be78-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8be78-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8be78-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8be78-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8be78-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8be78-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8be78-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be78-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8be78-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be78-137">訊息</span><span class="sxs-lookup"><span data-stu-id="8be78-137">Messages</span></span>](messages.md)
</dt> </dl>

 

