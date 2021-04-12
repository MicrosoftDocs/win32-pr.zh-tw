---
title: 'WM_MOUSEACTI加值稅E 訊息 (Winuser .h) '
description: 當游標在非作用中視窗，且使用者按下滑鼠按鍵時傳送。 只有當子視窗將它傳遞給 DefWindowProc 函數時，父視窗才會接收此訊息。
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- WM_MOUSEACTI加值稅E 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094351"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="73381-105">WM \_ MOUSEACTI加值稅E 訊息</span><span class="sxs-lookup"><span data-stu-id="73381-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="73381-106">當游標在非作用中視窗，且使用者按下滑鼠按鍵時傳送。</span><span class="sxs-lookup"><span data-stu-id="73381-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="73381-107">只有當子視窗將它傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數時，父視窗才會接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="73381-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="73381-109">參數</span><span class="sxs-lookup"><span data-stu-id="73381-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73381-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73381-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73381-111">正在啟動之視窗最上層父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="73381-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="73381-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73381-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73381-113">低序位單字會指定 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式所傳回的點擊測試值，作為處理 [**WM \_ NCHITTEST**](wm-nchittest.md) 訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="73381-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="73381-114">如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。</span><span class="sxs-lookup"><span data-stu-id="73381-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="73381-115">高序位單字指定當使用者按下滑鼠按鍵時所產生之滑鼠訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73381-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="73381-116">滑鼠訊息會被捨棄或張貼至視窗，視傳回值而定。</span><span class="sxs-lookup"><span data-stu-id="73381-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73381-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="73381-117">Return value</span></span>

<span data-ttu-id="73381-118">傳回值會指定是否應啟用視窗，以及是否應捨棄滑鼠訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="73381-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="73381-119">它必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="73381-119">It must be one of the following values.</span></span>



| <span data-ttu-id="73381-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="73381-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="73381-121">Description</span><span class="sxs-lookup"><span data-stu-id="73381-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73381-122"><dt>**MA \_啟動**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="73381-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="73381-123">啟動視窗，不捨棄滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="73381-124"><dt>**MA \_ACTI加值稅EANDEAT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="73381-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="73381-125">啟用視窗，並捨棄滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="73381-126"><dt>**MA \_NOACTI加值稅E**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="73381-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="73381-127">不會啟動視窗，也不會捨棄滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="73381-128"><dt>**MA \_NOACTI加值稅EANDEAT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="73381-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="73381-129">不會啟動視窗，但會捨棄滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="73381-130">備註</span><span class="sxs-lookup"><span data-stu-id="73381-130">Remarks</span></span>

<span data-ttu-id="73381-131">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會先將訊息傳遞給子視窗的父視窗，然後再進行任何處理。</span><span class="sxs-lookup"><span data-stu-id="73381-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="73381-132">父視窗會決定是否要啟動子視窗。</span><span class="sxs-lookup"><span data-stu-id="73381-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="73381-133">如果它啟用子視窗，父視窗應該會傳回 **ma \_ NOACTI加值稅E** 或 **ma \_ NOACTI加值稅EANDEAT** ，以防止系統進一步處理訊息。</span><span class="sxs-lookup"><span data-stu-id="73381-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="73381-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="73381-134">Requirements</span></span>



| <span data-ttu-id="73381-135">需求</span><span class="sxs-lookup"><span data-stu-id="73381-135">Requirement</span></span> | <span data-ttu-id="73381-136">值</span><span class="sxs-lookup"><span data-stu-id="73381-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73381-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73381-137">Minimum supported client</span></span><br/> | <span data-ttu-id="73381-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73381-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="73381-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73381-139">Minimum supported server</span></span><br/> | <span data-ttu-id="73381-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73381-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="73381-141">標頭</span><span class="sxs-lookup"><span data-stu-id="73381-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="73381-142"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="73381-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73381-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73381-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="73381-144">**參考**</span><span class="sxs-lookup"><span data-stu-id="73381-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73381-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="73381-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="73381-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73381-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="73381-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73381-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="73381-148">**WM \_ NCHITTEST**</span><span class="sxs-lookup"><span data-stu-id="73381-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="73381-149">**概念**</span><span class="sxs-lookup"><span data-stu-id="73381-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73381-150">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="73381-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

