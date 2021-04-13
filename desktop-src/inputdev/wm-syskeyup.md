---
title: 'WM_SYSKEYUP 訊息 (Winuser .h) '
description: 當使用者放開按住 ALT 鍵時所按下的按鍵時，以鍵盤焦點張貼至視窗。
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321799"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="e871e-104">WM \_ SYSKEYUP 訊息</span><span class="sxs-lookup"><span data-stu-id="e871e-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="e871e-105">當使用者放開按住 ALT 鍵時所按下的按鍵時，以鍵盤焦點張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="e871e-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="e871e-106">當目前沒有任何視窗具有鍵盤焦點時，也會發生此問題。在此情況下，會將 **WM \_ SYSKEYUP** 訊息傳送至使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="e871e-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="e871e-107">接收訊息的視窗可以藉由檢查 *lParam* 參數中的內容程式碼來區分這兩個內容。</span><span class="sxs-lookup"><span data-stu-id="e871e-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="e871e-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="e871e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="e871e-109">參數</span><span class="sxs-lookup"><span data-stu-id="e871e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e871e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e871e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e871e-111">要釋放之金鑰的虛擬金鑰碼。</span><span class="sxs-lookup"><span data-stu-id="e871e-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="e871e-112">請參閱 [**虛擬金鑰代碼**](virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e871e-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="e871e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e871e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e871e-114">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="e871e-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="e871e-115">Bits</span><span class="sxs-lookup"><span data-stu-id="e871e-115">Bits</span></span>  | <span data-ttu-id="e871e-116">意義</span><span class="sxs-lookup"><span data-stu-id="e871e-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e871e-117">0-15</span><span class="sxs-lookup"><span data-stu-id="e871e-117">0-15</span></span>  | <span data-ttu-id="e871e-118">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="e871e-118">The repeat count for the current message.</span></span> <span data-ttu-id="e871e-119">值是當使用者按住按鍵時，按鍵 autorepeated 的次數。</span><span class="sxs-lookup"><span data-stu-id="e871e-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="e871e-120">針對 **WM \_ SYSKEYUP** 訊息，重複計數一律是一個。</span><span class="sxs-lookup"><span data-stu-id="e871e-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="e871e-121">16-23</span><span class="sxs-lookup"><span data-stu-id="e871e-121">16-23</span></span> | <span data-ttu-id="e871e-122">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="e871e-122">The scan code.</span></span> <span data-ttu-id="e871e-123">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="e871e-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="e871e-124">24</span><span class="sxs-lookup"><span data-stu-id="e871e-124">24</span></span>    | <span data-ttu-id="e871e-125">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="e871e-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="e871e-126">如果它是擴充索引鍵，則此值為 1;否則，它是零。</span><span class="sxs-lookup"><span data-stu-id="e871e-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="e871e-127">25-28</span><span class="sxs-lookup"><span data-stu-id="e871e-127">25-28</span></span> | <span data-ttu-id="e871e-128">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e871e-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="e871e-129">29</span><span class="sxs-lookup"><span data-stu-id="e871e-129">29</span></span>    | <span data-ttu-id="e871e-130">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="e871e-130">The context code.</span></span> <span data-ttu-id="e871e-131">如果在釋放金鑰時，ALT 鍵已關閉，則此值為 1;如果將 **WM \_ SYSKEYUP** 訊息張貼至使用中視窗，因為沒有視窗具有鍵盤焦點，則為零。</span><span class="sxs-lookup"><span data-stu-id="e871e-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="e871e-132">30</span><span class="sxs-lookup"><span data-stu-id="e871e-132">30</span></span>    | <span data-ttu-id="e871e-133">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="e871e-133">The previous key state.</span></span> <span data-ttu-id="e871e-134">**WM \_ SYSKEYUP** 訊息的值一律為1。</span><span class="sxs-lookup"><span data-stu-id="e871e-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="e871e-135">31</span><span class="sxs-lookup"><span data-stu-id="e871e-135">31</span></span>    | <span data-ttu-id="e871e-136">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="e871e-136">The transition state.</span></span> <span data-ttu-id="e871e-137">**WM \_ SYSKEYUP** 訊息的值一律為1。</span><span class="sxs-lookup"><span data-stu-id="e871e-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="e871e-138">如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="e871e-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e871e-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="e871e-139">Return value</span></span>

<span data-ttu-id="e871e-140">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="e871e-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e871e-141">備註</span><span class="sxs-lookup"><span data-stu-id="e871e-141">Remarks</span></span>

<span data-ttu-id="e871e-142">如果放開了 F10 鍵或 ALT 鍵， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="e871e-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="e871e-143">訊息的 *wParam* 參數設定為 **SC \_ KEYMENU**。</span><span class="sxs-lookup"><span data-stu-id="e871e-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="e871e-144">當內容程式碼為零時，訊息可以傳遞至 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 函式，它會處理它，就像是一般的索引鍵訊息，而非字元索引鍵訊息一樣。</span><span class="sxs-lookup"><span data-stu-id="e871e-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="e871e-145">這可讓快速鍵與使用中視窗搭配使用，即使使用中視窗沒有鍵盤焦點也一樣。</span><span class="sxs-lookup"><span data-stu-id="e871e-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="e871e-146">針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="e871e-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="e871e-147">其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="e871e-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="e871e-148">適用于非 U. S。增強的 102-按鍵鍵盤，右邊的 ALT 鍵會以 CTRL + ALT 鍵的形式處理。</span><span class="sxs-lookup"><span data-stu-id="e871e-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="e871e-149">下表顯示當使用者按下並釋放此索引鍵時，所產生的訊息順序。</span><span class="sxs-lookup"><span data-stu-id="e871e-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="e871e-150">訊息</span><span class="sxs-lookup"><span data-stu-id="e871e-150">Message</span></span>                           | <span data-ttu-id="e871e-151">虛擬金鑰碼</span><span class="sxs-lookup"><span data-stu-id="e871e-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="e871e-152">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="e871e-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="e871e-153">**VK \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="e871e-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="e871e-154">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="e871e-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="e871e-155">**VK \_ 功能表**</span><span class="sxs-lookup"><span data-stu-id="e871e-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="e871e-156">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="e871e-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="e871e-157">**VK \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="e871e-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="e871e-158">**WM \_ SYSKEYUP**</span><span class="sxs-lookup"><span data-stu-id="e871e-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="e871e-159">**VK \_ 功能表**</span><span class="sxs-lookup"><span data-stu-id="e871e-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="e871e-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="e871e-160">Requirements</span></span>



| <span data-ttu-id="e871e-161">需求</span><span class="sxs-lookup"><span data-stu-id="e871e-161">Requirement</span></span> | <span data-ttu-id="e871e-162">值</span><span class="sxs-lookup"><span data-stu-id="e871e-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e871e-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e871e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="e871e-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e871e-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e871e-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e871e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="e871e-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e871e-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e871e-167">標頭</span><span class="sxs-lookup"><span data-stu-id="e871e-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="e871e-168"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e871e-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e871e-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e871e-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="e871e-170">**參考**</span><span class="sxs-lookup"><span data-stu-id="e871e-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e871e-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e871e-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e871e-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="e871e-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="e871e-173">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="e871e-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="e871e-174">**WM \_ SYSKEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="e871e-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="e871e-175">**概念**</span><span class="sxs-lookup"><span data-stu-id="e871e-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e871e-176">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="e871e-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

