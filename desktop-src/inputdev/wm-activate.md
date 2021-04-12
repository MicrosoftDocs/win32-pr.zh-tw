---
title: 'WM_ACTI加值稅E 訊息 (Winuser .h) '
description: 傳送至正在啟動的視窗和停用的視窗。
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- WM_ACTI加值稅E 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094356"
---
# <a name="wm_activate-message"></a><span data-ttu-id="b4317-104">WM \_ 啟用訊息</span><span class="sxs-lookup"><span data-stu-id="b4317-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="b4317-105">傳送至正在啟動的視窗和停用的視窗。</span><span class="sxs-lookup"><span data-stu-id="b4317-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="b4317-106">如果 windows 使用相同的輸入佇列，則會以同步方式將訊息傳送至即將停用之最上層視窗的視窗程式，然後再傳送至即將啟動之最上層視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="b4317-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="b4317-107">如果 windows 使用不同的輸入佇列，則會以非同步方式傳送訊息，因此會立即啟用視窗。</span><span class="sxs-lookup"><span data-stu-id="b4317-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="b4317-108">參數</span><span class="sxs-lookup"><span data-stu-id="b4317-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4317-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4317-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4317-110">低序位字組可指定視窗是否正在啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="b4317-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="b4317-111">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b4317-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="b4317-112">高序位單字指定要啟動或停用視窗的最小化狀態。</span><span class="sxs-lookup"><span data-stu-id="b4317-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="b4317-113">非零值表示視窗最小化。</span><span class="sxs-lookup"><span data-stu-id="b4317-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="b4317-114">值</span><span class="sxs-lookup"><span data-stu-id="b4317-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="b4317-115">意義</span><span class="sxs-lookup"><span data-stu-id="b4317-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="b4317-116"><dt>**WA \_主動**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b4317-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="b4317-117">由滑鼠點以外的某個方法啟用 (例如，透過呼叫 [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) 函式，或使用鍵盤介面選取視窗) 。</span><span class="sxs-lookup"><span data-stu-id="b4317-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="b4317-118"><dt>**WA \_CLICKACTIVE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b4317-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b4317-119">由滑鼠按一下來啟用。</span><span class="sxs-lookup"><span data-stu-id="b4317-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="b4317-120"><dt>**WA \_非**</dt>作用中 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b4317-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="b4317-121">關閉。</span><span class="sxs-lookup"><span data-stu-id="b4317-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="b4317-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4317-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4317-123">要啟用或停用的視窗控制碼（視 *wParam* 參數的值而定）。</span><span class="sxs-lookup"><span data-stu-id="b4317-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="b4317-124">如果 *wParam* 的低序位字是 **WA \_ 非** 使用中，則 *lParam* 是正在啟動之視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b4317-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="b4317-125">如果 *wParam* 的低序位字是 **Wa \_ ACTIVE** 或 **wa \_ CLICKACTIVE**， *lParam* 就是停用視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b4317-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="b4317-126">這個控制碼可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4317-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4317-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4317-127">Return value</span></span>

<span data-ttu-id="b4317-128">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b4317-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4317-129">備註</span><span class="sxs-lookup"><span data-stu-id="b4317-129">Remarks</span></span>

<span data-ttu-id="b4317-130">如果視窗正在啟動且未最小化， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將鍵盤焦點設定為視窗。</span><span class="sxs-lookup"><span data-stu-id="b4317-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="b4317-131">如果視窗是由滑鼠按一下來啟動，它也會收到 [**WM \_ MOUSEACTI加值稅E**](wm-mouseactivate.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b4317-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4317-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4317-132">Requirements</span></span>



| <span data-ttu-id="b4317-133">需求</span><span class="sxs-lookup"><span data-stu-id="b4317-133">Requirement</span></span> | <span data-ttu-id="b4317-134">值</span><span class="sxs-lookup"><span data-stu-id="b4317-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4317-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4317-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b4317-136">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4317-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b4317-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4317-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b4317-138">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4317-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4317-139">標頭</span><span class="sxs-lookup"><span data-stu-id="b4317-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4317-140"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="b4317-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4317-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4317-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4317-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="b4317-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4317-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b4317-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b4317-144">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="b4317-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="b4317-145">**WM \_ MOUSEACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="b4317-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="b4317-146">**WM \_ NCACTI加值稅E**</span><span class="sxs-lookup"><span data-stu-id="b4317-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="b4317-147">**概念**</span><span class="sxs-lookup"><span data-stu-id="b4317-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b4317-148">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="b4317-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

