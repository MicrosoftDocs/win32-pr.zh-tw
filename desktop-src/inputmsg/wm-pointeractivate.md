---
title: WM_POINTERACTI加值稅E 訊息
description: 當主要指標在視窗上產生 WM_POINTERDOWN 時，傳送至非使用中的視窗。
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTI加值稅E 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001300"
---
# <a name="wm_pointeractivate-message"></a><span data-ttu-id="d3d2e-104">WM_POINTERACTI加值稅E 訊息</span><span class="sxs-lookup"><span data-stu-id="d3d2e-104">WM_POINTERACTIVATE message</span></span>

<span data-ttu-id="d3d2e-105">當主要指標在視窗上產生 [**WM_POINTERDOWN**](wm-pointerdown.md) 時，傳送至非使用中的視窗。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-105">Sent to an inactive window when a primary pointer generates a [**WM_POINTERDOWN**](wm-pointerdown.md) over the window.</span></span> <span data-ttu-id="d3d2e-106">只要訊息保持未處理狀態，它就會向上移動父視窗鏈，直到到達最上層視窗為止。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-106">As long as the message remains unhandled, it travels up the parent window chain until it is reaches the top-level window.</span></span> <span data-ttu-id="d3d2e-107">應用程式可以回應此訊息，以指定是否要啟用它們。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-107">Applications can respond to this message to specify whether they wish to be activated.</span></span>

<span data-ttu-id="d3d2e-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a><span data-ttu-id="d3d2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="d3d2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d2e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3d2e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d2e-111">包含指標識別碼和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-111">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="d3d2e-112">使用下列宏來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-112">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="d3d2e-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼</span><span class="sxs-lookup"><span data-stu-id="d3d2e-113">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="d3d2e-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (wParam) ：處理 [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) 訊息時所傳回的點擊測試值。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="d3d2e-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3d2e-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d2e-116">包含要啟動之視窗最上層視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-116">Contains the handle to the top-level window of the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d2e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3d2e-117">Return value</span></span>

<span data-ttu-id="d3d2e-118">如果應用程式處理此訊息，它應該會傳回 [備註] 區段中所述的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-118">If an application processes this message, it should return one of the values described in the Remarks section.</span></span>

<span data-ttu-id="d3d2e-119">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-119">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d2e-120">備註</span><span class="sxs-lookup"><span data-stu-id="d3d2e-120">Remarks</span></span>

<span data-ttu-id="d3d2e-121">應用程式可以處理這則訊息，並傳回下列其中一個值，以判斷系統如何處理啟用和啟用輸入：</span><span class="sxs-lookup"><span data-stu-id="d3d2e-121">An application can handle this message and return one of the following values to determine how the system processes the activation and the activating input:</span></span>

-   <span data-ttu-id="d3d2e-122">PA_ACTI加值稅E</span><span class="sxs-lookup"><span data-stu-id="d3d2e-122">PA_ACTIVATE</span></span>
-   <span data-ttu-id="d3d2e-123">PA_NOACTI加值稅E</span><span class="sxs-lookup"><span data-stu-id="d3d2e-123">PA_NOACTIVATE</span></span>

<span data-ttu-id="d3d2e-124">請務必注意，當使用者與具有多個同時指標的系統互動時， **WM_POINTERACTI加值稅E** 訊息代表的啟動機會僅適用于這些指標的第一個。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-124">It is important to note that, when the user is interacting with the system with multiple simultaneous pointers, the activation opportunity that the **WM_POINTERACTIVATE** message represents is available to applications only for the first of those pointers.</span></span> <span data-ttu-id="d3d2e-125">因此，應用程式應留意到它們在非使用中時，仍會收到指標的輸入。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-125">Applications should, therefore, be aware that they may still receive input from pointers while they are inactive.</span></span>

<span data-ttu-id="d3d2e-126">如果應用程式未處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 會將訊息傳遞至父視窗。</span><span class="sxs-lookup"><span data-stu-id="d3d2e-126">If the application does not handle this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) passes the message to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d2e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3d2e-127">Requirements</span></span>



| <span data-ttu-id="d3d2e-128">需求</span><span class="sxs-lookup"><span data-stu-id="d3d2e-128">Requirement</span></span> | <span data-ttu-id="d3d2e-129">值</span><span class="sxs-lookup"><span data-stu-id="d3d2e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d2e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3d2e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d2e-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3d2e-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d3d2e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3d2e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d2e-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3d2e-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3d2e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d3d2e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d2e-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d3d2e-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d2e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3d2e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d2e-137">訊息</span><span class="sxs-lookup"><span data-stu-id="d3d2e-137">Messages</span></span>](messages.md)
</dt> </dl>

 

