---
title: 'WM_UNICHAR 訊息 (Winuser .h) '
description: '\_應用程式可以使用 WM 則 unichar 會訊息，將輸入張貼到其他視窗。'
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- WM_UNICHAR 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965302"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="acde4-104">WM \_ 則 unichar 會訊息</span><span class="sxs-lookup"><span data-stu-id="acde4-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="acde4-105">應用程式可以使用 **WM \_ 則 unichar 會** 訊息，將輸入張貼到其他視窗。</span><span class="sxs-lookup"><span data-stu-id="acde4-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="acde4-106">此訊息包含已按下之按鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="acde4-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="acde4-107"> (測試目標應用程式是否能藉由傳送 *wParam* 設定為 **UNICODE \_ NOCHAR** 的訊息，來處理 **WM \_ 則 unichar 會** 訊息。 ) </span><span class="sxs-lookup"><span data-stu-id="acde4-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="acde4-108">參數</span><span class="sxs-lookup"><span data-stu-id="acde4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acde4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acde4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acde4-110">按鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="acde4-110">The character code of the key.</span></span>

<span data-ttu-id="acde4-111">如果 *wParam* 是 **UNICODE \_ NOCHAR** ，而且應用程式會處理此訊息，則傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="acde4-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="acde4-112">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會傳回 **FALSE** (預設) 。</span><span class="sxs-lookup"><span data-stu-id="acde4-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="acde4-113">如果 *wParam* 不是 **UNICODE \_ NOCHAR**，則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="acde4-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="acde4-114">Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會使用相同的參數張貼 [**WM \_ 字元**](wm-char.md) 訊息，而 ANSI **DefWindowProc** 函式會使用對應的 ANSI 字元 (s) 來張貼一或兩個 **wm \_ 字元** 訊息。</span><span class="sxs-lookup"><span data-stu-id="acde4-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="acde4-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acde4-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acde4-116">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="acde4-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="acde4-117">Bits</span><span class="sxs-lookup"><span data-stu-id="acde4-117">Bits</span></span>  | <span data-ttu-id="acde4-118">意義</span><span class="sxs-lookup"><span data-stu-id="acde4-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acde4-119">0-15</span><span class="sxs-lookup"><span data-stu-id="acde4-119">0-15</span></span>  | <span data-ttu-id="acde4-120">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="acde4-120">The repeat count for the current message.</span></span> <span data-ttu-id="acde4-121">值是當使用者按住按鍵時，按鍵 autorepeated 的次數。</span><span class="sxs-lookup"><span data-stu-id="acde4-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="acde4-122">如果按鍵夠長，則會傳送多則訊息。</span><span class="sxs-lookup"><span data-stu-id="acde4-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="acde4-123">不過，重複計數不是累計的。</span><span class="sxs-lookup"><span data-stu-id="acde4-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="acde4-124">16-23</span><span class="sxs-lookup"><span data-stu-id="acde4-124">16-23</span></span> | <span data-ttu-id="acde4-125">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="acde4-125">The scan code.</span></span> <span data-ttu-id="acde4-126">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="acde4-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="acde4-127">24</span><span class="sxs-lookup"><span data-stu-id="acde4-127">24</span></span>    | <span data-ttu-id="acde4-128">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="acde4-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="acde4-129">如果它是擴充索引鍵，則此值為 1;否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="acde4-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="acde4-130">25-28</span><span class="sxs-lookup"><span data-stu-id="acde4-130">25-28</span></span> | <span data-ttu-id="acde4-131">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="acde4-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="acde4-132">29</span><span class="sxs-lookup"><span data-stu-id="acde4-132">29</span></span>    | <span data-ttu-id="acde4-133">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="acde4-133">The context code.</span></span> <span data-ttu-id="acde4-134">如果按下按鍵時按住 ALT 鍵，則此值為 1;否則，此值為0。</span><span class="sxs-lookup"><span data-stu-id="acde4-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="acde4-135">30</span><span class="sxs-lookup"><span data-stu-id="acde4-135">30</span></span>    | <span data-ttu-id="acde4-136">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="acde4-136">The previous key state.</span></span> <span data-ttu-id="acde4-137">如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。</span><span class="sxs-lookup"><span data-stu-id="acde4-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="acde4-138">31</span><span class="sxs-lookup"><span data-stu-id="acde4-138">31</span></span>    | <span data-ttu-id="acde4-139">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="acde4-139">The transition state.</span></span> <span data-ttu-id="acde4-140">如果正在釋放金鑰，則值為1，如果正在按下索引鍵，則為0。</span><span class="sxs-lookup"><span data-stu-id="acde4-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="acde4-141">如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="acde4-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acde4-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="acde4-142">Return value</span></span>

<span data-ttu-id="acde4-143">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="acde4-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="acde4-144">備註</span><span class="sxs-lookup"><span data-stu-id="acde4-144">Remarks</span></span>

<span data-ttu-id="acde4-145">**Wm \_ 則 unichar 會** 訊息類似于 [**wm \_ 字元**](wm-char.md)，但它使用 Unicode 轉換格式 (Utf-16) -32，而 **WM \_ 字元** 使用 utf-16。</span><span class="sxs-lookup"><span data-stu-id="acde4-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="acde4-146">此訊息的設計目的是要將 Unicode 字元傳送或張貼至 ANSI 視窗，並且可以處理 Unicode 補充平面字元。</span><span class="sxs-lookup"><span data-stu-id="acde4-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="acde4-147">因為所按下的按鍵和產生的字元訊息之間不一定要有一對一的對應，所以 *lParam* 參數的高序位字中的資訊通常對應用程式而言並不有用。</span><span class="sxs-lookup"><span data-stu-id="acde4-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="acde4-148">高序位字組中的資訊只適用于在 **\_ 則 unichar 會** 訊息張貼之前的最新 wm 的一則的 [**wm \_**](wm-keydown.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="acde4-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="acde4-149">針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和右 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="acde4-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="acde4-150">有些其他鍵盤可能會支援 *lParam* 參數中的擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="acde4-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="acde4-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="acde4-151">Requirements</span></span>



| <span data-ttu-id="acde4-152">需求</span><span class="sxs-lookup"><span data-stu-id="acde4-152">Requirement</span></span> | <span data-ttu-id="acde4-153">值</span><span class="sxs-lookup"><span data-stu-id="acde4-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acde4-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acde4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="acde4-155">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acde4-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="acde4-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acde4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="acde4-157">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="acde4-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="acde4-158">標頭</span><span class="sxs-lookup"><span data-stu-id="acde4-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="acde4-159"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="acde4-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acde4-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acde4-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="acde4-161">**參考**</span><span class="sxs-lookup"><span data-stu-id="acde4-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="acde4-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="acde4-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="acde4-163">**WM \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="acde4-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="acde4-164">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="acde4-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="acde4-165">**概念**</span><span class="sxs-lookup"><span data-stu-id="acde4-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="acde4-166">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="acde4-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

