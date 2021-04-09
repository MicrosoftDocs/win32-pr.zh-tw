---
UID: ''
title: LowLevelMouseProc 回呼函式
description: 每次有新的滑鼠輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函數。
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2020
ms.locfileid: "104024279"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="cdd2f-103">LowLevelMouseProc 函式</span><span class="sxs-lookup"><span data-stu-id="cdd2f-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="cdd2f-104">Description</span><span class="sxs-lookup"><span data-stu-id="cdd2f-104">Description</span></span>

<span data-ttu-id="cdd2f-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="cdd2f-106">每次有新的滑鼠輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="cdd2f-107">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="cdd2f-108">**LowLevelMouseProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="cdd2f-109">參數</span><span class="sxs-lookup"><span data-stu-id="cdd2f-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="cdd2f-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="cdd2f-110">nCode [in]</span></span>

<span data-ttu-id="cdd2f-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="cdd2f-111">Type: **int**</span></span>

<span data-ttu-id="cdd2f-112">攔截程式用來判斷如何處理訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="cdd2f-113">如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="cdd2f-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="cdd2f-115">值</span><span class="sxs-lookup"><span data-stu-id="cdd2f-115">Value</span></span> | <span data-ttu-id="cdd2f-116">意義</span><span class="sxs-lookup"><span data-stu-id="cdd2f-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="cdd2f-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="cdd2f-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="cdd2f-118">*WParam* 和 *lParam* 參數包含滑鼠訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="cdd2f-119">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="cdd2f-119">wParam [in]</span></span>

<span data-ttu-id="cdd2f-120">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="cdd2f-120">Type: **WPARAM**</span></span>

<span data-ttu-id="cdd2f-121">滑鼠訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="cdd2f-122">這個參數可以是下列其中一個訊息： [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)、 [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)、 [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)、 [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)、 [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) 或 [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="cdd2f-123">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="cdd2f-123">lParam [in]</span></span>

<span data-ttu-id="cdd2f-124">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="cdd2f-124">Type: **LPARAM**</span></span>

<span data-ttu-id="cdd2f-125">[MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="cdd2f-126">傳回</span><span class="sxs-lookup"><span data-stu-id="cdd2f-126">Returns</span></span>

<span data-ttu-id="cdd2f-127">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="cdd2f-127">Type: **LRESULT**</span></span>

<span data-ttu-id="cdd2f-128">如果 *nCode* 小於零，則攔截程式必須傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="cdd2f-129">如果 *nCode* 大於或等於零，且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_MOUSE_LL](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="cdd2f-130">如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至其餘的攔截鏈或目標視窗程式。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd2f-131">備註</span><span class="sxs-lookup"><span data-stu-id="cdd2f-131">Remarks</span></span>

<span data-ttu-id="cdd2f-132">應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_MOUSE_LL** 攔截類型和攔截程式指標，以安裝攔截程式。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="cdd2f-133">此攔截器會在其安裝所在的執行緒內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="cdd2f-134">呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="cdd2f-135">因此，安裝攔截的執行緒必須有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="cdd2f-136">滑鼠輸入可以來自本機滑鼠驅動程式，或是來自 [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) 函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="cdd2f-137">如果輸入來自 **mouse_event** 的呼叫，則輸入為「已插入」。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="cdd2f-138">不過， **WH_MOUSE_LL** 的勾點不會插入另一個進程。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="cdd2f-139">相反地，內容會切換回已安裝攔截的進程，並在其原始內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="cdd2f-140">然後，內容會切換回產生事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="cdd2f-141">攔截程式應處理訊息的時間，比下列登錄機碼中 **LowLevelHooksTimeout** 值指定的資料輸入少： **HKEY_CURRENT_USER\Control Panel\Desktop**。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="cdd2f-142">值會以毫秒來表示。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-142">The value is in milliseconds.</span></span>
<span data-ttu-id="cdd2f-143">如果攔截程式超時，系統會將訊息傳遞至下一個攔截。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="cdd2f-144">不過，在 Windows 7 和更新版本上，會以無訊息方式移除攔截，而不會被呼叫。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="cdd2f-145">應用程式沒有辦法知道是否已移除攔截。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="cdd2f-146">**注意：**  偵錯工具攔截無法追蹤這種類型的低層級滑鼠掛勾。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="cdd2f-147">如果應用程式必須使用低層級的勾點，則應該在將工作關閉到工作者執行緒的專用線程上執行勾點，然後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="cdd2f-148">在大部分的情況下，應用程式必須使用低層級的勾點，而改為監視原始輸入。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="cdd2f-149">這是因為原始輸入可以更有效率地監視以其他執行緒為目標的滑鼠和鍵盤訊息，而非低層級的勾點。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="cdd2f-150">如需原始輸入的詳細資訊，請參閱 [原始輸入](/windows/desktop/inputdev/raw-input)。</span><span class="sxs-lookup"><span data-stu-id="cdd2f-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="cdd2f-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cdd2f-151">See also</span></span>

[<span data-ttu-id="cdd2f-152">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="cdd2f-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="cdd2f-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="cdd2f-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="cdd2f-154">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="cdd2f-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="cdd2f-155">MSLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="cdd2f-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="cdd2f-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="cdd2f-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="cdd2f-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="cdd2f-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="cdd2f-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="cdd2f-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="cdd2f-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="cdd2f-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="cdd2f-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="cdd2f-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="cdd2f-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="cdd2f-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="cdd2f-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="cdd2f-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="cdd2f-163">鉤</span><span class="sxs-lookup"><span data-stu-id="cdd2f-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="cdd2f-164">關於勾點</span><span class="sxs-lookup"><span data-stu-id="cdd2f-164">About Hooks</span></span>](about-hooks.md)
