---
title: 'WM_KEYDOWN 訊息 (Winuser .h) '
description: 當按下非系統鍵時，將鍵盤焦點張貼至視窗。 非系統機碼是未按下 ALT 鍵時所按下的按鍵。
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996065"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="8b411-105">WM \_ KEYDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="8b411-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="8b411-106">當按下非系統鍵時，將鍵盤焦點張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="8b411-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="8b411-107">非系統機碼是未按下 ALT 鍵時所按下的按鍵。</span><span class="sxs-lookup"><span data-stu-id="8b411-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="8b411-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b411-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b411-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b411-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b411-110">非系統索引鍵的虛擬機器碼程式碼。</span><span class="sxs-lookup"><span data-stu-id="8b411-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="8b411-111">請參閱 [虛擬金鑰代碼](virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="8b411-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b411-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b411-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b411-113">重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標和轉換狀態旗標，如下所示。</span><span class="sxs-lookup"><span data-stu-id="8b411-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="8b411-114">Bits</span><span class="sxs-lookup"><span data-stu-id="8b411-114">Bits</span></span>  | <span data-ttu-id="8b411-115">意義</span><span class="sxs-lookup"><span data-stu-id="8b411-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b411-116">0-15</span><span class="sxs-lookup"><span data-stu-id="8b411-116">0-15</span></span>  | <span data-ttu-id="8b411-117">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="8b411-117">The repeat count for the current message.</span></span> <span data-ttu-id="8b411-118">值是當使用者按住按鍵時，按鍵 autorepeated 的次數。</span><span class="sxs-lookup"><span data-stu-id="8b411-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="8b411-119">如果按鍵夠長，則會傳送多則訊息。</span><span class="sxs-lookup"><span data-stu-id="8b411-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="8b411-120">不過，重複計數不是累計的。</span><span class="sxs-lookup"><span data-stu-id="8b411-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="8b411-121">16-23</span><span class="sxs-lookup"><span data-stu-id="8b411-121">16-23</span></span> | <span data-ttu-id="8b411-122">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="8b411-122">The scan code.</span></span> <span data-ttu-id="8b411-123">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="8b411-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="8b411-124">24</span><span class="sxs-lookup"><span data-stu-id="8b411-124">24</span></span>    | <span data-ttu-id="8b411-125">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="8b411-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="8b411-126">如果它是擴充索引鍵，則此值為 1;否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="8b411-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="8b411-127">25-28</span><span class="sxs-lookup"><span data-stu-id="8b411-127">25-28</span></span> | <span data-ttu-id="8b411-128">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="8b411-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8b411-129">29</span><span class="sxs-lookup"><span data-stu-id="8b411-129">29</span></span>    | <span data-ttu-id="8b411-130">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="8b411-130">The context code.</span></span> <span data-ttu-id="8b411-131">若為 **WM 的 \_ KEYDOWN** 訊息，此值一律為0。</span><span class="sxs-lookup"><span data-stu-id="8b411-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="8b411-132">30</span><span class="sxs-lookup"><span data-stu-id="8b411-132">30</span></span>    | <span data-ttu-id="8b411-133">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="8b411-133">The previous key state.</span></span> <span data-ttu-id="8b411-134">如果在傳送訊息之前，金鑰已關閉，則值為1，如果索引鍵已啟動，則為零。</span><span class="sxs-lookup"><span data-stu-id="8b411-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="8b411-135">31</span><span class="sxs-lookup"><span data-stu-id="8b411-135">31</span></span>    | <span data-ttu-id="8b411-136">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="8b411-136">The transition state.</span></span> <span data-ttu-id="8b411-137">若為 **WM 的 \_ KEYDOWN** 訊息，此值一律為0。</span><span class="sxs-lookup"><span data-stu-id="8b411-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="8b411-138">如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="8b411-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b411-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b411-139">Return value</span></span>

<span data-ttu-id="8b411-140">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="8b411-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="8b411-141">範例</span><span class="sxs-lookup"><span data-stu-id="8b411-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="8b411-142">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="8b411-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="8b411-143">備註</span><span class="sxs-lookup"><span data-stu-id="8b411-143">Remarks</span></span>

<span data-ttu-id="8b411-144">如果按下 F10 鍵， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會設定內部旗標。</span><span class="sxs-lookup"><span data-stu-id="8b411-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="8b411-145">當 **DefWindowProc** 收到 [**WM \_ KEYUP**](wm-keyup.md) 訊息時，此函式會檢查是否已設定內部旗標，如果是，則會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="8b411-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="8b411-146">訊息的 **WM \_ SYSCOMMAND** 參數設定為 SC \_ KEYMENU。</span><span class="sxs-lookup"><span data-stu-id="8b411-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="8b411-147">由於 autorepeat 功能的不同，在發送 [**wm \_ KEYUP**](wm-keyup.md)訊息之前，可能會公佈一個以上的 **wm \_ KEYDOWN** 訊息。</span><span class="sxs-lookup"><span data-stu-id="8b411-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="8b411-148">先前的金鑰狀態 (位 30) 可用來判斷 **WM \_ KEYDOWN** 訊息是否表示第一個向下轉換或重複的轉換。</span><span class="sxs-lookup"><span data-stu-id="8b411-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="8b411-149">針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="8b411-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="8b411-150">其他鍵盤可能會在 *lParam* 參數中支援擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="8b411-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="8b411-151">應用程式必須將 *wParam* 傳遞至 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ，而不需要加以變更。</span><span class="sxs-lookup"><span data-stu-id="8b411-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b411-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b411-152">Requirements</span></span>



| <span data-ttu-id="8b411-153">需求</span><span class="sxs-lookup"><span data-stu-id="8b411-153">Requirement</span></span> | <span data-ttu-id="8b411-154">值</span><span class="sxs-lookup"><span data-stu-id="8b411-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b411-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b411-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8b411-156">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b411-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8b411-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b411-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8b411-158">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b411-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b411-159">標頭</span><span class="sxs-lookup"><span data-stu-id="8b411-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b411-160"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8b411-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b411-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b411-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b411-162">**參考**</span><span class="sxs-lookup"><span data-stu-id="8b411-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8b411-163">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8b411-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8b411-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="8b411-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="8b411-165">**WM \_ 字元**</span><span class="sxs-lookup"><span data-stu-id="8b411-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="8b411-166">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="8b411-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="8b411-167">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="8b411-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="8b411-168">**概念**</span><span class="sxs-lookup"><span data-stu-id="8b411-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8b411-169">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="8b411-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

