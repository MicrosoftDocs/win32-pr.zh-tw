---
title: 'WM_SYSCHAR 訊息 (Winuser .h) '
description: 當 TranslateMessage 函數轉譯了 WM SYSKEYDOWN 訊息時，以鍵盤焦點張貼至視窗 \_ 。
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509461"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="fae07-104">WM \_ SYSCHAR 訊息</span><span class="sxs-lookup"><span data-stu-id="fae07-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="fae07-105">當 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數轉譯了 [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)訊息時，以鍵盤焦點張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="fae07-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="fae07-106">它會指定系統字元索引鍵的字元碼，也就是在 ALT 鍵關閉時按下的字元按鍵。</span><span class="sxs-lookup"><span data-stu-id="fae07-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="fae07-107">參數</span><span class="sxs-lookup"><span data-stu-id="fae07-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae07-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fae07-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fae07-109">視窗功能表鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="fae07-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="fae07-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fae07-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fae07-111">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fae07-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="fae07-112">Bits</span><span class="sxs-lookup"><span data-stu-id="fae07-112">Bits</span></span>                                                                             | <span data-ttu-id="fae07-113">意義</span><span class="sxs-lookup"><span data-stu-id="fae07-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fae07-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="fae07-115">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="fae07-115">The repeat count for the current message.</span></span> <span data-ttu-id="fae07-116">值是當使用者按住索引鍵時，自動重複擊鍵的次數。</span><span class="sxs-lookup"><span data-stu-id="fae07-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="fae07-117">如果按鍵夠長，則會傳送多則訊息。</span><span class="sxs-lookup"><span data-stu-id="fae07-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="fae07-118">不過，重複計數不是累計的。</span><span class="sxs-lookup"><span data-stu-id="fae07-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="fae07-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="fae07-120">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="fae07-120">The scan code.</span></span> <span data-ttu-id="fae07-121">此值取決於原始設備製造商 (OEM) 。</span><span class="sxs-lookup"><span data-stu-id="fae07-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="fae07-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="fae07-123">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="fae07-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="fae07-124">如果它是擴充索引鍵，則此值為 1;否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="fae07-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="fae07-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="fae07-126">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="fae07-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="fae07-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="fae07-128">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="fae07-128">The context code.</span></span> <span data-ttu-id="fae07-129">如果按下按鍵時按住 ALT 鍵，則此值為 1;否則，此值為0。</span><span class="sxs-lookup"><span data-stu-id="fae07-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="fae07-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="fae07-131">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="fae07-131">The previous key state.</span></span> <span data-ttu-id="fae07-132">如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。</span><span class="sxs-lookup"><span data-stu-id="fae07-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="fae07-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="fae07-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="fae07-134">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="fae07-134">The transition state.</span></span> <span data-ttu-id="fae07-135">如果正在釋放金鑰，則值為1，如果正在按下索引鍵，則為0。</span><span class="sxs-lookup"><span data-stu-id="fae07-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="fae07-136">如需詳細資訊，請參閱 [按鍵訊息旗標](../inputdev/about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="fae07-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae07-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="fae07-137">Return value</span></span>

<span data-ttu-id="fae07-138">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="fae07-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae07-139">備註</span><span class="sxs-lookup"><span data-stu-id="fae07-139">Remarks</span></span>

<span data-ttu-id="fae07-140">當內容程式碼為零時，訊息可以傳遞至 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函式，此函式會處理它，就好像它是標準的索引鍵訊息，而不是系統字元金鑰訊息一樣。</span><span class="sxs-lookup"><span data-stu-id="fae07-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="fae07-141">這可讓快速鍵與使用中視窗搭配使用，即使使用中視窗沒有鍵盤焦點也一樣。</span><span class="sxs-lookup"><span data-stu-id="fae07-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="fae07-142">針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;PRINT SCRN 鍵;BREAK 鍵;數位鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="fae07-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="fae07-143">其他鍵盤可能會支援參數中的擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="fae07-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fae07-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="fae07-144">Requirements</span></span>



| <span data-ttu-id="fae07-145">需求</span><span class="sxs-lookup"><span data-stu-id="fae07-145">Requirement</span></span> | <span data-ttu-id="fae07-146">值</span><span class="sxs-lookup"><span data-stu-id="fae07-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae07-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fae07-147">Minimum supported client</span></span><br/> | <span data-ttu-id="fae07-148">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fae07-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fae07-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fae07-149">Minimum supported server</span></span><br/> | <span data-ttu-id="fae07-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fae07-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fae07-151">標頭</span><span class="sxs-lookup"><span data-stu-id="fae07-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae07-152"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fae07-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fae07-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fae07-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="fae07-154">**參考**</span><span class="sxs-lookup"><span data-stu-id="fae07-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fae07-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="fae07-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="fae07-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="fae07-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="fae07-157">**WM \_ SYSKEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="fae07-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="fae07-158">**概念**</span><span class="sxs-lookup"><span data-stu-id="fae07-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fae07-159">鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="fae07-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

