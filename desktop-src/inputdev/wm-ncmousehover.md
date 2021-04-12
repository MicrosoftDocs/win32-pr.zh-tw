---
title: 'WM_NCMOUSEHOVER 訊息 (Winuser .h) '
description: 當游標停留在視窗的非工作區時，在先前呼叫 TrackMouseEvent 所指定的期間內，將滑鼠停留在視窗的非工作區上。
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- WM_NCMOUSEHOVER 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025410"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="64d3c-104">WM \_ NCMOUSEHOVER 訊息</span><span class="sxs-lookup"><span data-stu-id="64d3c-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="64d3c-105">當游標停留在視窗的非工作區時，在先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定的期間內，將滑鼠停留在視窗的非工作區上。</span><span class="sxs-lookup"><span data-stu-id="64d3c-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="64d3c-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="64d3c-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="64d3c-107">參數</span><span class="sxs-lookup"><span data-stu-id="64d3c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d3c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64d3c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d3c-109">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式所傳回的點擊測試值，做為處理 [**WM \_ NCHITTEST**](wm-nchittest.md)訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="64d3c-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="64d3c-110">如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。</span><span class="sxs-lookup"><span data-stu-id="64d3c-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="64d3c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64d3c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64d3c-112">[**點**](/previous-versions//dd162808(v=vs.85))結構，包含資料指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="64d3c-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="64d3c-113">座標是相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="64d3c-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d3c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="64d3c-114">Return value</span></span>

<span data-ttu-id="64d3c-115">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="64d3c-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d3c-116">備註</span><span class="sxs-lookup"><span data-stu-id="64d3c-116">Remarks</span></span>

<span data-ttu-id="64d3c-117">當產生此訊息時，會停止停留追蹤。</span><span class="sxs-lookup"><span data-stu-id="64d3c-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="64d3c-118">如果應用程式需要進一步追蹤滑鼠停留行為，則必須再次呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 。</span><span class="sxs-lookup"><span data-stu-id="64d3c-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="64d3c-119">您也可以使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 和 [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，從 *LPARAM* 中解壓縮 X 和 Y 座標的值。</span><span class="sxs-lookup"><span data-stu-id="64d3c-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="64d3c-120">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="64d3c-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="64d3c-121">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="64d3c-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64d3c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="64d3c-122">Requirements</span></span>



| <span data-ttu-id="64d3c-123">需求</span><span class="sxs-lookup"><span data-stu-id="64d3c-123">Requirement</span></span> | <span data-ttu-id="64d3c-124">值</span><span class="sxs-lookup"><span data-stu-id="64d3c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d3c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64d3c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="64d3c-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64d3c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="64d3c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64d3c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="64d3c-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64d3c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="64d3c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="64d3c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d3c-130"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="64d3c-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d3c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64d3c-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="64d3c-132">**參考**</span><span class="sxs-lookup"><span data-stu-id="64d3c-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64d3c-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="64d3c-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="64d3c-134">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="64d3c-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="64d3c-135">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="64d3c-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="64d3c-136">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="64d3c-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="64d3c-137">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="64d3c-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="64d3c-138">**WM \_ NCHITTEST**</span><span class="sxs-lookup"><span data-stu-id="64d3c-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="64d3c-139">**WM \_ MOUSEHOVER**</span><span class="sxs-lookup"><span data-stu-id="64d3c-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="64d3c-140">**概念**</span><span class="sxs-lookup"><span data-stu-id="64d3c-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="64d3c-141">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="64d3c-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="64d3c-142">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="64d3c-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="64d3c-143">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="64d3c-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="64d3c-144">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64d3c-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

