---
title: 'WM_CHAR 訊息 (Winuser .h) '
description: 在 TranslateMessage 函式轉譯了 WM KEYDOWN 訊息時，以鍵盤焦點張貼至視窗 \_ 。 WM \_ 字元訊息包含已按下之按鍵的字元碼。
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977724"
---
# <a name="wm_char-message"></a><span data-ttu-id="00eb9-105">WM \_ 字元訊息</span><span class="sxs-lookup"><span data-stu-id="00eb9-105">WM\_CHAR message</span></span>

<span data-ttu-id="00eb9-106">在 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函式轉譯了 [**WM \_ KEYDOWN**](wm-keydown.md)訊息時，以鍵盤焦點張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="00eb9-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="00eb9-107">**WM \_ 字元** 訊息包含已按下之按鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="00eb9-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="00eb9-108">參數</span><span class="sxs-lookup"><span data-stu-id="00eb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00eb9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00eb9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00eb9-110">按鍵的字元碼。</span><span class="sxs-lookup"><span data-stu-id="00eb9-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="00eb9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00eb9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00eb9-112">[重複計數]、[掃描程式碼]、[擴充按鍵旗標]、[內容程式碼]、先前的索引鍵狀態旗標和轉換狀態旗標，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="00eb9-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="00eb9-113">Bits</span><span class="sxs-lookup"><span data-stu-id="00eb9-113">Bits</span></span>  | <span data-ttu-id="00eb9-114">意義</span><span class="sxs-lookup"><span data-stu-id="00eb9-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00eb9-115">0-15</span><span class="sxs-lookup"><span data-stu-id="00eb9-115">0-15</span></span>  | <span data-ttu-id="00eb9-116">目前訊息的重複計數。</span><span class="sxs-lookup"><span data-stu-id="00eb9-116">The repeat count for the current message.</span></span> <span data-ttu-id="00eb9-117">值是當使用者按住按鍵時，按鍵 autorepeated 的次數。</span><span class="sxs-lookup"><span data-stu-id="00eb9-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="00eb9-118">如果按鍵夠長，則會傳送多則訊息。</span><span class="sxs-lookup"><span data-stu-id="00eb9-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="00eb9-119">不過，重複計數不是累計的。</span><span class="sxs-lookup"><span data-stu-id="00eb9-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="00eb9-120">16-23</span><span class="sxs-lookup"><span data-stu-id="00eb9-120">16-23</span></span> | <span data-ttu-id="00eb9-121">掃描程式碼。</span><span class="sxs-lookup"><span data-stu-id="00eb9-121">The scan code.</span></span> <span data-ttu-id="00eb9-122">此值取決於 OEM。</span><span class="sxs-lookup"><span data-stu-id="00eb9-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="00eb9-123">24</span><span class="sxs-lookup"><span data-stu-id="00eb9-123">24</span></span>    | <span data-ttu-id="00eb9-124">指出機碼是否為擴充的索引鍵，例如出現在增強型101或102按鍵鍵盤上的右手 ALT 和 CTRL 鍵。</span><span class="sxs-lookup"><span data-stu-id="00eb9-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="00eb9-125">如果它是擴充索引鍵，則此值為 1;否則，它是0。</span><span class="sxs-lookup"><span data-stu-id="00eb9-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="00eb9-126">25-28</span><span class="sxs-lookup"><span data-stu-id="00eb9-126">25-28</span></span> | <span data-ttu-id="00eb9-127">保護請勿使用。</span><span class="sxs-lookup"><span data-stu-id="00eb9-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="00eb9-128">29</span><span class="sxs-lookup"><span data-stu-id="00eb9-128">29</span></span>    | <span data-ttu-id="00eb9-129">內容程式碼。</span><span class="sxs-lookup"><span data-stu-id="00eb9-129">The context code.</span></span> <span data-ttu-id="00eb9-130">如果按下按鍵時按住 ALT 鍵，則此值為 1;否則，此值為0。</span><span class="sxs-lookup"><span data-stu-id="00eb9-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="00eb9-131">30</span><span class="sxs-lookup"><span data-stu-id="00eb9-131">30</span></span>    | <span data-ttu-id="00eb9-132">先前的金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="00eb9-132">The previous key state.</span></span> <span data-ttu-id="00eb9-133">如果在傳送訊息之前，金鑰已關閉，則此值為 1; 如果金鑰已啟動，則為0。</span><span class="sxs-lookup"><span data-stu-id="00eb9-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="00eb9-134">31</span><span class="sxs-lookup"><span data-stu-id="00eb9-134">31</span></span>    | <span data-ttu-id="00eb9-135">轉換狀態。</span><span class="sxs-lookup"><span data-stu-id="00eb9-135">The transition state.</span></span> <span data-ttu-id="00eb9-136">如果正在釋放金鑰，則值為1，如果正在按下索引鍵，則為0。</span><span class="sxs-lookup"><span data-stu-id="00eb9-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="00eb9-137">如需詳細資訊，請參閱 [按鍵訊息旗標](about-keyboard-input.md#keystroke-message-flags)。</span><span class="sxs-lookup"><span data-stu-id="00eb9-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00eb9-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="00eb9-138">Return value</span></span>

<span data-ttu-id="00eb9-139">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="00eb9-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="00eb9-140">範例</span><span class="sxs-lookup"><span data-stu-id="00eb9-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="00eb9-141">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="00eb9-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="00eb9-142">備註</span><span class="sxs-lookup"><span data-stu-id="00eb9-142">Remarks</span></span>

<span data-ttu-id="00eb9-143">**WM \_ 字元** 訊息使用 Unicode 轉換格式 (utf-16) -16。</span><span class="sxs-lookup"><span data-stu-id="00eb9-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="00eb9-144">在按下的按鍵和產生的字元訊息之間不一定會有一對一的對應，因此 *lParam* 參數的高序位字中的資訊通常對應用程式而言並不有用。</span><span class="sxs-lookup"><span data-stu-id="00eb9-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="00eb9-145">高序位字組中的資訊僅適用于在 **wm \_ 字元** 訊息張貼之前的最新 [**wm \_ KEYDOWN**](wm-keydown.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="00eb9-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="00eb9-146">針對增強的101和102鍵鍵盤，擴充的按鍵是鍵盤主要區段上的右 ALT 和右 CTRL 鍵;位於數位鍵台左邊的叢集中的 INS、DEL、HOME、END、PAGE UP、PAGE DOWN 和方向鍵;並將 (/) ，然後在數位鍵台中輸入按鍵。</span><span class="sxs-lookup"><span data-stu-id="00eb9-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="00eb9-147">有些其他鍵盤可能會支援 *lParam* 參數中的擴充金鑰位。</span><span class="sxs-lookup"><span data-stu-id="00eb9-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="00eb9-148">[**Wm \_ 則 unichar 會**](wm-unichar.md)訊息與 **wm \_ CHAR** 相同，但它使用 32 utf-16。</span><span class="sxs-lookup"><span data-stu-id="00eb9-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="00eb9-149">其設計目的是要將 Unicode 字元傳送或張貼至 ANSI 視窗，並且可以處理 Unicode 補充平面字元。</span><span class="sxs-lookup"><span data-stu-id="00eb9-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="00eb9-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="00eb9-150">Requirements</span></span>



| <span data-ttu-id="00eb9-151">需求</span><span class="sxs-lookup"><span data-stu-id="00eb9-151">Requirement</span></span> | <span data-ttu-id="00eb9-152">值</span><span class="sxs-lookup"><span data-stu-id="00eb9-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00eb9-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00eb9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="00eb9-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00eb9-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="00eb9-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00eb9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="00eb9-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00eb9-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="00eb9-157">標頭</span><span class="sxs-lookup"><span data-stu-id="00eb9-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="00eb9-158"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="00eb9-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00eb9-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00eb9-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="00eb9-160">**參考**</span><span class="sxs-lookup"><span data-stu-id="00eb9-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="00eb9-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="00eb9-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="00eb9-162">**WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="00eb9-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="00eb9-163">**WM \_ 則 UNICHAR 會**</span><span class="sxs-lookup"><span data-stu-id="00eb9-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="00eb9-164">**概念**</span><span class="sxs-lookup"><span data-stu-id="00eb9-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00eb9-165">鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="00eb9-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

