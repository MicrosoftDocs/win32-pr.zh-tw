---
UID: ''
title: LowLevelKeyboardProc 回呼函式
description: 每次有新的鍵盤輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函式。
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "104023198"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="54fcb-103">LowLevelKeyboardProc 函式</span><span class="sxs-lookup"><span data-stu-id="54fcb-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="54fcb-104">Description</span><span class="sxs-lookup"><span data-stu-id="54fcb-104">Description</span></span>

<span data-ttu-id="54fcb-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="54fcb-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="54fcb-106">每次有新的鍵盤輸入事件張貼到執行緒輸入佇列時，系統就會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="54fcb-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="54fcb-107">**注意：**  當呼叫此回呼函式以回應索引鍵的狀態變更時，會先呼叫回呼函式，然後再更新索引鍵的非同步狀態。</span><span class="sxs-lookup"><span data-stu-id="54fcb-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="54fcb-108">因此，無法從回呼函式中呼叫 [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) 來判斷索引鍵的非同步狀態。</span><span class="sxs-lookup"><span data-stu-id="54fcb-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="54fcb-109">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="54fcb-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="54fcb-110">**LowLevelKeyboardProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="54fcb-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="54fcb-111">參數</span><span class="sxs-lookup"><span data-stu-id="54fcb-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="54fcb-112">程式碼 [in]</span><span class="sxs-lookup"><span data-stu-id="54fcb-112">code [in]</span></span>

<span data-ttu-id="54fcb-113">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="54fcb-113">Type: **int**</span></span>

<span data-ttu-id="54fcb-114">攔截程式用來判斷如何處理訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="54fcb-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="54fcb-115">如果 *nCode* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="54fcb-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="54fcb-116">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="54fcb-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="54fcb-117">值</span><span class="sxs-lookup"><span data-stu-id="54fcb-117">Value</span></span> | <span data-ttu-id="54fcb-118">意義</span><span class="sxs-lookup"><span data-stu-id="54fcb-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="54fcb-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="54fcb-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="54fcb-120">*WParam* 和 *lParam* 參數包含鍵盤訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="54fcb-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="54fcb-121">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="54fcb-121">wParam [in]</span></span>

<span data-ttu-id="54fcb-122">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="54fcb-122">Type: **WPARAM**</span></span>

<span data-ttu-id="54fcb-123">鍵盤訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54fcb-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="54fcb-124">這個參數可以是下列其中一個訊息： [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)、 [WM_KEYUP](/windows/desktop/inputdev/wm-keyup)、 [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)或 [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup)。</span><span class="sxs-lookup"><span data-stu-id="54fcb-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="54fcb-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="54fcb-125">lParam [in]</span></span>

<span data-ttu-id="54fcb-126">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="54fcb-126">Type: **LPARAM**</span></span>

<span data-ttu-id="54fcb-127">[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="54fcb-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="54fcb-128">傳回</span><span class="sxs-lookup"><span data-stu-id="54fcb-128">Returns</span></span>

<span data-ttu-id="54fcb-129">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="54fcb-129">Type: **LRESULT**</span></span>

<span data-ttu-id="54fcb-130">如果 *nCode* 小於零，則攔截程式必須傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="54fcb-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="54fcb-131">如果 *nCode* 大於或等於零，且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_KEYBOARD_LL](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="54fcb-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="54fcb-132">如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至其餘的攔截鏈或目標視窗程式。</span><span class="sxs-lookup"><span data-stu-id="54fcb-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="54fcb-133">備註</span><span class="sxs-lookup"><span data-stu-id="54fcb-133">Remarks</span></span>

<span data-ttu-id="54fcb-134">應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_KEYBOARD_LL** 攔截類型和攔截程式指標，以安裝攔截程式。</span><span class="sxs-lookup"><span data-stu-id="54fcb-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="54fcb-135">此攔截器會在其安裝所在的執行緒內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="54fcb-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="54fcb-136">呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。</span><span class="sxs-lookup"><span data-stu-id="54fcb-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="54fcb-137">因此，安裝攔截的執行緒必須有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="54fcb-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="54fcb-138">鍵盤輸入可以來自本機鍵盤驅動程式，或來自 [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) 函式的呼叫。</span><span class="sxs-lookup"><span data-stu-id="54fcb-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="54fcb-139">如果輸入來自 **keybd_event** 的呼叫，則輸入為「已插入」。</span><span class="sxs-lookup"><span data-stu-id="54fcb-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="54fcb-140">不過，WH_KEYBOARD_LL 的勾點不會插入另一個進程。</span><span class="sxs-lookup"><span data-stu-id="54fcb-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="54fcb-141">相反地，內容會切換回已安裝攔截的進程，並在其原始內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="54fcb-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="54fcb-142">然後，內容會切換回產生事件的應用程式。</span><span class="sxs-lookup"><span data-stu-id="54fcb-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="54fcb-143">攔截程式應處理訊息的時間，比下列登錄機碼中 **LowLevelHooksTimeout** 值指定的資料輸入少： **HKEY_CURRENT_USER\Control Panel\Desktop**。</span><span class="sxs-lookup"><span data-stu-id="54fcb-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="54fcb-144">值會以毫秒來表示。</span><span class="sxs-lookup"><span data-stu-id="54fcb-144">The value is in milliseconds.</span></span>
<span data-ttu-id="54fcb-145">如果攔截程式超時，系統會將訊息傳遞至下一個攔截。</span><span class="sxs-lookup"><span data-stu-id="54fcb-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="54fcb-146">不過，在 Windows 7 和更新版本上，會以無訊息方式移除攔截，而不會被呼叫。</span><span class="sxs-lookup"><span data-stu-id="54fcb-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="54fcb-147">應用程式沒有辦法知道是否已移除攔截。</span><span class="sxs-lookup"><span data-stu-id="54fcb-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="54fcb-148">注意：偵錯工具攔截無法追蹤這種類型的低層級鍵盤攔截。</span><span class="sxs-lookup"><span data-stu-id="54fcb-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="54fcb-149">如果應用程式必須使用低層級的勾點，則應該在將工作關閉到工作者執行緒的專用線程上執行勾點，然後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="54fcb-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="54fcb-150">在大部分的情況下，應用程式必須使用低層級的勾點，而改為監視原始輸入。</span><span class="sxs-lookup"><span data-stu-id="54fcb-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="54fcb-151">這是因為原始輸入可以更有效率地監視以其他執行緒為目標的滑鼠和鍵盤訊息，而非低層級的勾點。</span><span class="sxs-lookup"><span data-stu-id="54fcb-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="54fcb-152">如需原始輸入的詳細資訊，請參閱 [原始輸入](/windows/desktop/inputdev/raw-input)。</span><span class="sxs-lookup"><span data-stu-id="54fcb-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="54fcb-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54fcb-153">See also</span></span>

[<span data-ttu-id="54fcb-154">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="54fcb-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="54fcb-155">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="54fcb-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="54fcb-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="54fcb-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="54fcb-157">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="54fcb-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="54fcb-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="54fcb-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="54fcb-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="54fcb-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="54fcb-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="54fcb-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="54fcb-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="54fcb-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="54fcb-162">鉤</span><span class="sxs-lookup"><span data-stu-id="54fcb-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="54fcb-163">關於勾點</span><span class="sxs-lookup"><span data-stu-id="54fcb-163">About Hooks</span></span>](about-hooks.md)
