---
title: 'WM_SYSKEYDOWN 訊息 (Winuser .h) '
description: 當使用者按下 F10 (鍵時，以鍵盤焦點張貼至視窗) 或按住 ALT 鍵，然後按下另一個按鍵。
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967538"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="a4f71-104">WM \_ SYSKEYDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="a4f71-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="a4f71-105">當使用者按下 F10 (鍵時，以鍵盤焦點張貼至視窗) 或按住 ALT 鍵，然後按下另一個按鍵。</span><span class="sxs-lookup"><span data-stu-id="a4f71-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="a4f71-106">當目前沒有任何視窗具有鍵盤焦點時，也會發生此問題。在此情況下，會將 **WM \_ SYSKEYDOWN** 訊息傳送至使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="a4f71-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="a4f71-107">接收訊息的視窗可以藉由檢查 *lParam* 參數中的內容程式碼來區分這兩個內容。</span><span class="sxs-lookup"><span data-stu-id="a4f71-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="a4f71-108">參數</span><span class="sxs-lookup"><span data-stu-id="a4f71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4f71-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f71-110">所按下之按鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="a4f71-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="a4f71-111">請參閱 [**虛擬金鑰代碼**](virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a4f71-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="a4f71-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4f71-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f71-113">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="a4f71-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="a4f71-114">Bits</span><span class="sxs-lookup"><span data-stu-id="a4f71-114">Bits</span></span>  | <span data-ttu-id="a4f71-115">意義</span><span class="sxs-lookup"><span data-stu-id="a4f71-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f71-116">0-15</span><span class="sxs-lookup"><span data-stu-id="a4f71-116">0-15</span></span>  | <span data-ttu-id="a4f71-117">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="a4f71-117">The repeat count for the current message.</span></span> <span data-ttu-id="a4f71-118">值是當使用者按住按鍵時，按鍵 autorepeated 的次數。</span><span class="sxs-lookup"><span data-stu-id="a4f71-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="a4f71-119">如果按鍵夠長，則會傳送多則訊息。</span><span class="sxs-lookup"><span data-stu-id="a4f71-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="a4f71-120">不過，重複計數不是累計的。</span><span class="sxs-lookup"><span data-stu-id="a4f71-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="a4f71-121">16-23</span><span class="sxs-lookup"><span data-stu-id="a4f71-121">16-23</span></span> | <span data-ttu-id="a4f71-122">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="a4f71-122">The scan code.</span></span> <span data-ttu-id="a4f71-123">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="a4f71-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="a4f71-124">24</span><span class="sxs-lookup"><span data-stu-id="a4f71-124">24</span></span>    | <span data-ttu-id="a4f71-125">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="a4f71-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="a4f71-126">如果它是擴充索引鍵，則此值為 1;否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="a4f71-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="a4f71-127">25-28</span><span class="sxs-lookup"><span data-stu-id="a4f71-127">25-28</span></span> | <span data-ttu-id="a4f71-128">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="a4f71-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a4f71-129">29</span><span class="sxs-lookup"><span data-stu-id="a4f71-129">29</span></span>    | <span data-ttu-id="a4f71-130">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="a4f71-130">The context code.</span></span> <span data-ttu-id="a4f71-131">如果在按下按鍵時，ALT 鍵已關閉，則此值為 1;如果將 **WM \_ SYSKEYDOWN** 訊息張貼至使用中視窗，因為沒有視窗具有鍵盤焦點，則為0。</span><span class="sxs-lookup"><span data-stu-id="a4f71-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="a4f71-132">30</span><span class="sxs-lookup"><span data-stu-id="a4f71-132">30</span></span>    | <span data-ttu-id="a4f71-133">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f71-133">The previous key state.</span></span> <span data-ttu-id="a4f71-134">如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。</span><span class="sxs-lookup"><span data-stu-id="a4f71-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="a4f71-135">31</span><span class="sxs-lookup"><span data-stu-id="a4f71-135">31</span></span>    | <span data-ttu-id="a4f71-136">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="a4f71-136">The transition state.</span></span> <span data-ttu-id="a4f71-137">**WM \_ SYSKEYDOWN** 訊息的值一律為0。</span><span class="sxs-lookup"><span data-stu-id="a4f71-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="a4f71-138">如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="a4f71-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f71-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4f71-139">Return value</span></span>

<span data-ttu-id="a4f71-140">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="a4f71-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f71-141">備註</span><span class="sxs-lookup"><span data-stu-id="a4f71-141">Remarks</span></span>

<span data-ttu-id="a4f71-142">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會檢查指定的索引鍵，並在索引鍵為 TAB 或 ENTER 時產生 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)訊息。</span><span class="sxs-lookup"><span data-stu-id="a4f71-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="a4f71-143">當內容程式碼為零時，訊息可以傳遞至 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 函式，它會處理它，就像是一般的索引鍵訊息，而非字元索引鍵訊息一樣。</span><span class="sxs-lookup"><span data-stu-id="a4f71-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="a4f71-144">這可讓快速鍵與使用中視窗搭配使用，即使使用中視窗沒有鍵盤焦點也一樣。</span><span class="sxs-lookup"><span data-stu-id="a4f71-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="a4f71-145">因為會自動重複，所以在傳送 [**wm \_ SYSKEYUP**](wm-syskeyup.md)訊息之前可能會發生一個以上的 **WM \_ SYSKEYDOWN** 訊息。</span><span class="sxs-lookup"><span data-stu-id="a4f71-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="a4f71-146">先前的金鑰狀態 (位 30) 可用來判斷 **WM \_ SYSKEYDOWN** 訊息是否表示第一個向下轉換或重複的轉換。</span><span class="sxs-lookup"><span data-stu-id="a4f71-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="a4f71-147">針對增強的101和102鍵鍵盤，增強型按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="a4f71-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="a4f71-148">其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="a4f71-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="a4f71-149">當使用者按下 F10 鍵而沒有 ALT 鍵時，也會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a4f71-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f71-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4f71-150">Requirements</span></span>



| <span data-ttu-id="a4f71-151">需求</span><span class="sxs-lookup"><span data-stu-id="a4f71-151">Requirement</span></span> | <span data-ttu-id="a4f71-152">值</span><span class="sxs-lookup"><span data-stu-id="a4f71-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f71-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4f71-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f71-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4f71-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a4f71-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4f71-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f71-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4f71-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a4f71-157">標頭</span><span class="sxs-lookup"><span data-stu-id="a4f71-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f71-158"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a4f71-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f71-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4f71-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4f71-160">**參考**</span><span class="sxs-lookup"><span data-stu-id="a4f71-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a4f71-161">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a4f71-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a4f71-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="a4f71-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="a4f71-163">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="a4f71-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="a4f71-164">**WM \_ SYSKEYUP**</span><span class="sxs-lookup"><span data-stu-id="a4f71-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="a4f71-165">**概念**</span><span class="sxs-lookup"><span data-stu-id="a4f71-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a4f71-166">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="a4f71-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

