---
title: 'WM_KEYUP 訊息 (Winuser .h) '
description: 當系統釋放非系統機碼時，以鍵盤焦點張貼至視窗。 非系統索引鍵是未按下 ALT 鍵時所按下的按鍵，或是當視窗具有鍵盤焦點時按下的鍵盤按鍵。
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384418"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="f3aa0-105">WM \_ KEYUP 訊息</span><span class="sxs-lookup"><span data-stu-id="f3aa0-105">WM\_KEYUP message</span></span>

<span data-ttu-id="f3aa0-106">當系統釋放非系統機碼時，以鍵盤焦點張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="f3aa0-107">非系統索引鍵是 *未* 按下 ALT 鍵時所按下的按鍵，或是當視窗具有鍵盤焦點時按下的鍵盤按鍵。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="f3aa0-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3aa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3aa0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3aa0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3aa0-110">非系統索引鍵的虛擬機器碼程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="f3aa0-111">請參閱 [虛擬金鑰代碼](virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3aa0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3aa0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3aa0-113">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="f3aa0-114">Bits</span><span class="sxs-lookup"><span data-stu-id="f3aa0-114">Bits</span></span>  | <span data-ttu-id="f3aa0-115">意義</span><span class="sxs-lookup"><span data-stu-id="f3aa0-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3aa0-116">0-15</span><span class="sxs-lookup"><span data-stu-id="f3aa0-116">0-15</span></span>  | <span data-ttu-id="f3aa0-117">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-117">The repeat count for the current message.</span></span> <span data-ttu-id="f3aa0-118">值是當使用者按住按鍵時，按鍵 autorepeated 的次數。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="f3aa0-119">針對 **WM \_ KEYUP** 訊息，重複計數一律為1。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="f3aa0-120">16-23</span><span class="sxs-lookup"><span data-stu-id="f3aa0-120">16-23</span></span> | <span data-ttu-id="f3aa0-121">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-121">The scan code.</span></span> <span data-ttu-id="f3aa0-122">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f3aa0-123">24</span><span class="sxs-lookup"><span data-stu-id="f3aa0-123">24</span></span>    | <span data-ttu-id="f3aa0-124">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="f3aa0-125">如果它是擴充索引鍵，則此值為 1;否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="f3aa0-126">25-28</span><span class="sxs-lookup"><span data-stu-id="f3aa0-126">25-28</span></span> | <span data-ttu-id="f3aa0-127">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="f3aa0-128">29</span><span class="sxs-lookup"><span data-stu-id="f3aa0-128">29</span></span>    | <span data-ttu-id="f3aa0-129">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-129">The context code.</span></span> <span data-ttu-id="f3aa0-130">**WM 的 \_ KEYUP** 訊息的值一律為0。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="f3aa0-131">30</span><span class="sxs-lookup"><span data-stu-id="f3aa0-131">30</span></span>    | <span data-ttu-id="f3aa0-132">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-132">The previous key state.</span></span> <span data-ttu-id="f3aa0-133">若為 **WM 的 \_ KEYUP** 訊息，此值一律為1。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="f3aa0-134">31</span><span class="sxs-lookup"><span data-stu-id="f3aa0-134">31</span></span>    | <span data-ttu-id="f3aa0-135">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-135">The transition state.</span></span> <span data-ttu-id="f3aa0-136">若為 **WM 的 \_ KEYUP** 訊息，此值一律為1。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="f3aa0-137">如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3aa0-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3aa0-138">Return value</span></span>

<span data-ttu-id="f3aa0-139">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3aa0-140">備註</span><span class="sxs-lookup"><span data-stu-id="f3aa0-140">Remarks</span></span>

<span data-ttu-id="f3aa0-141">如果放開了 F10 鍵或 ALT 鍵， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="f3aa0-142">訊息的 *wParam* 參數設定為 SC \_ KEYMENU。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="f3aa0-143">針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="f3aa0-144">其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="f3aa0-145">應用程式必須將 *wParam* 傳遞至 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ，而不需要加以變更。</span><span class="sxs-lookup"><span data-stu-id="f3aa0-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3aa0-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3aa0-146">Requirements</span></span>



| <span data-ttu-id="f3aa0-147">需求</span><span class="sxs-lookup"><span data-stu-id="f3aa0-147">Requirement</span></span> | <span data-ttu-id="f3aa0-148">值</span><span class="sxs-lookup"><span data-stu-id="f3aa0-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3aa0-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3aa0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f3aa0-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3aa0-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f3aa0-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3aa0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f3aa0-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3aa0-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f3aa0-153">標頭</span><span class="sxs-lookup"><span data-stu-id="f3aa0-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3aa0-154"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f3aa0-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3aa0-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3aa0-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3aa0-156">**參考**</span><span class="sxs-lookup"><span data-stu-id="f3aa0-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f3aa0-157">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f3aa0-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f3aa0-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="f3aa0-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="f3aa0-159">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="f3aa0-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="f3aa0-160">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="f3aa0-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="f3aa0-161">**概念**</span><span class="sxs-lookup"><span data-stu-id="f3aa0-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f3aa0-162">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="f3aa0-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

