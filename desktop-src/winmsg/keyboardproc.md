---
UID: ''
title: KeyboardProc 回呼函式
description: 系統呼叫這個函式會取得訊息函式，且會有要處理的鍵盤訊息。
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
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/11/2020
ms.locfileid: "106968689"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="9bea9-103">KeyboardProc 函式</span><span class="sxs-lookup"><span data-stu-id="9bea9-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="9bea9-104">Description</span><span class="sxs-lookup"><span data-stu-id="9bea9-104">Description</span></span>

<span data-ttu-id="9bea9-105">搭配 [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) 函式使用的應用程式定義或程式庫定義的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="9bea9-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="9bea9-106">每當應用程式呼叫 [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) 或 [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) 函式時，系統就會呼叫這個函式，而 ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) 或 [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) 處理的鍵盤訊息。</span><span class="sxs-lookup"><span data-stu-id="9bea9-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="9bea9-107">**HOOKPROC** 型別定義此回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="9bea9-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="9bea9-108">**KeyboardProc** 是應用程式定義或程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="9bea9-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="9bea9-109">參數</span><span class="sxs-lookup"><span data-stu-id="9bea9-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="9bea9-110">程式碼 [in]</span><span class="sxs-lookup"><span data-stu-id="9bea9-110">code [in]</span></span>

<span data-ttu-id="9bea9-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="9bea9-111">Type: **int**</span></span>

<span data-ttu-id="9bea9-112">攔截程式用來判斷如何處理訊息的程式碼。</span><span class="sxs-lookup"><span data-stu-id="9bea9-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="9bea9-113">如果程式 *代碼* 小於零，則攔截程式必須將訊息傳遞至 [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) 函式，而不需要進一步處理，並且應該傳回 **CallNextHookEx** 所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="9bea9-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="9bea9-114">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="9bea9-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="9bea9-115">值</span><span class="sxs-lookup"><span data-stu-id="9bea9-115">Value</span></span> | <span data-ttu-id="9bea9-116">意義</span><span class="sxs-lookup"><span data-stu-id="9bea9-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="9bea9-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="9bea9-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="9bea9-118">*WParam* 和 *lParam* 參數包含按鍵訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9bea9-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="9bea9-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="9bea9-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="9bea9-120">*WParam* 和 *lParam* 參數包含按鍵訊息的相關資訊，而且尚未從訊息佇列中移除按鍵訊息。</span><span class="sxs-lookup"><span data-stu-id="9bea9-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="9bea9-121"> (名為 **PeekMessage** 函式的應用程式，並指定 **PM_NOREMOVE** 旗標。 ) </span><span class="sxs-lookup"><span data-stu-id="9bea9-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="9bea9-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="9bea9-122">wParam [in]</span></span>

<span data-ttu-id="9bea9-123">類型： **WPARAM**</span><span class="sxs-lookup"><span data-stu-id="9bea9-123">Type: **WPARAM**</span></span>

<span data-ttu-id="9bea9-124">產生擊鍵訊息的索引鍵的 [虛擬金鑰程式碼](/windows/desktop/inputdev/virtual-key-codes) 。</span><span class="sxs-lookup"><span data-stu-id="9bea9-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="9bea9-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="9bea9-125">lParam [in]</span></span>

<span data-ttu-id="9bea9-126">類型： **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="9bea9-126">Type: **LPARAM**</span></span>

<span data-ttu-id="9bea9-127">重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標，以及轉換狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="9bea9-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="9bea9-128">如需 *lParam* 參數的詳細資訊，請參閱 [按鍵訊息旗標](/windows/desktop/inputdev/about-keyboard-input)。</span><span class="sxs-lookup"><span data-stu-id="9bea9-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="9bea9-129">下表描述此值的位。</span><span class="sxs-lookup"><span data-stu-id="9bea9-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="9bea9-130">Bits</span><span class="sxs-lookup"><span data-stu-id="9bea9-130">Bits</span></span> | <span data-ttu-id="9bea9-131">Description</span><span class="sxs-lookup"><span data-stu-id="9bea9-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="9bea9-132">0-15</span><span class="sxs-lookup"><span data-stu-id="9bea9-132">0-15</span></span> | <span data-ttu-id="9bea9-133">重複計數。</span><span class="sxs-lookup"><span data-stu-id="9bea9-133">The repeat count.</span></span> <span data-ttu-id="9bea9-134">值是當使用者按住按鍵時，按鍵重複出現的次數。</span><span class="sxs-lookup"><span data-stu-id="9bea9-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="9bea9-135">16-23</span><span class="sxs-lookup"><span data-stu-id="9bea9-135">16-23</span></span> | <span data-ttu-id="9bea9-136">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="9bea9-136">The scan code.</span></span> <span data-ttu-id="9bea9-137">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="9bea9-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="9bea9-138">24</span><span class="sxs-lookup"><span data-stu-id="9bea9-138">24</span></span> | <span data-ttu-id="9bea9-139">指出金鑰是否為擴充金鑰，例如，函式金鑰或數位鍵臺上的按鍵。</span><span class="sxs-lookup"><span data-stu-id="9bea9-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="9bea9-140">如果金鑰是擴充索引鍵，則值為1。否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="9bea9-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="9bea9-141">25-28</span><span class="sxs-lookup"><span data-stu-id="9bea9-141">25-28</span></span> | <span data-ttu-id="9bea9-142">保留的。</span><span class="sxs-lookup"><span data-stu-id="9bea9-142">Reserved.</span></span> |
| <span data-ttu-id="9bea9-143">29</span><span class="sxs-lookup"><span data-stu-id="9bea9-143">29</span></span> | <span data-ttu-id="9bea9-144">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="9bea9-144">The context code.</span></span> <span data-ttu-id="9bea9-145">如果 ALT 鍵已關閉，則此值為1。否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="9bea9-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="9bea9-146">30</span><span class="sxs-lookup"><span data-stu-id="9bea9-146">30</span></span> | <span data-ttu-id="9bea9-147">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="9bea9-147">The previous key state.</span></span> <span data-ttu-id="9bea9-148">如果在傳送訊息之前，金鑰已關閉，則此值為 1;如果金鑰已啟動，則為0。</span><span class="sxs-lookup"><span data-stu-id="9bea9-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="9bea9-149">31</span><span class="sxs-lookup"><span data-stu-id="9bea9-149">31</span></span> | <span data-ttu-id="9bea9-150">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="9bea9-150">The transition state.</span></span> <span data-ttu-id="9bea9-151">如果正在按下索引鍵，則值為0，如果正在釋放，則為1。</span><span class="sxs-lookup"><span data-stu-id="9bea9-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="9bea9-152">傳回</span><span class="sxs-lookup"><span data-stu-id="9bea9-152">Returns</span></span>

<span data-ttu-id="9bea9-153">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9bea9-153">Type: **LRESULT**</span></span>

<span data-ttu-id="9bea9-154">如果程式 *代碼* 小於零，則攔截程式必須傳回 **CallNextHookEx** 傳回的值。</span><span class="sxs-lookup"><span data-stu-id="9bea9-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="9bea9-155">如果程式 *代碼* 大於或等於零，而且攔截程式未處理訊息，強烈建議您呼叫 **CallNextHookEx** 並傳回傳回的值;否則，已安裝 [WH_KEYBOARD](about-hooks.md) 勾點的其他應用程式將不會收到攔截通知，而且可能會導致不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="9bea9-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="9bea9-156">如果攔截程式處理訊息，它可能會傳回非零值，以防止系統將訊息傳遞至其餘的攔截鏈或目標視窗程式。</span><span class="sxs-lookup"><span data-stu-id="9bea9-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bea9-157">備註</span><span class="sxs-lookup"><span data-stu-id="9bea9-157">Remarks</span></span>

<span data-ttu-id="9bea9-158">應用程式會在 **SetWindowsHookEx** 函式的呼叫中指定 **WH_KEYBOARD** 攔截類型和攔截程式指標，以安裝攔截程式。</span><span class="sxs-lookup"><span data-stu-id="9bea9-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="9bea9-159">此攔截可能會在其安裝所在的執行緒內容中呼叫。</span><span class="sxs-lookup"><span data-stu-id="9bea9-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="9bea9-160">呼叫是藉由將訊息傳送至已安裝攔截器的執行緒進行。</span><span class="sxs-lookup"><span data-stu-id="9bea9-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="9bea9-161">因此，安裝攔截的執行緒必須有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="9bea9-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bea9-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9bea9-162">See also</span></span>

[<span data-ttu-id="9bea9-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="9bea9-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="9bea9-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="9bea9-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="9bea9-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="9bea9-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="9bea9-166">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="9bea9-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="9bea9-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="9bea9-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="9bea9-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="9bea9-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="9bea9-169">鉤</span><span class="sxs-lookup"><span data-stu-id="9bea9-169">Hooks</span></span>](hooks.md)
