---
Description: 在視窗大小變更之後傳送至視窗。
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: 'WM_SIZE 訊息 (Winuser .h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996320"
---
# <a name="wm_size-message"></a><span data-ttu-id="7e823-103">WM \_ 大小訊息</span><span class="sxs-lookup"><span data-stu-id="7e823-103">WM\_SIZE message</span></span>

<span data-ttu-id="7e823-104">在視窗大小變更之後傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="7e823-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="7e823-105">視窗會透過其 [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="7e823-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="7e823-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e823-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e823-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e823-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e823-108">要求的調整大小類型。</span><span class="sxs-lookup"><span data-stu-id="7e823-108">The type of resizing requested.</span></span> <span data-ttu-id="7e823-109">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7e823-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7e823-110">值</span><span class="sxs-lookup"><span data-stu-id="7e823-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="7e823-111">意義</span><span class="sxs-lookup"><span data-stu-id="7e823-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="7e823-112"><dt>**大小 \_MAXHIDE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7e823-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="7e823-113">當某個其他視窗最大化時，訊息會傳送至所有快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="7e823-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="7e823-114"><dt>**大小 \_最大化**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7e823-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="7e823-115">視窗已經最大化。</span><span class="sxs-lookup"><span data-stu-id="7e823-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="7e823-116"><dt>**大小 \_MAXSHOW**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7e823-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="7e823-117">當某個其他視窗還原成先前的大小時，訊息會傳送至所有快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="7e823-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="7e823-118"><dt>**大小 \_最小化**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7e823-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="7e823-119">視窗已經過最小化。</span><span class="sxs-lookup"><span data-stu-id="7e823-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="7e823-120"><dt>**大小 \_還原**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e823-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="7e823-121">視窗已調整大小，但不會套用 **大小 \_ 最小化** 或 **大小 \_ 最大化** 的值。</span><span class="sxs-lookup"><span data-stu-id="7e823-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7e823-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e823-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e823-123">*LParam* 的低序位字組指定工作區的新寬度。</span><span class="sxs-lookup"><span data-stu-id="7e823-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="7e823-124">*LParam* 的高序位字指定了工作區的新高度。</span><span class="sxs-lookup"><span data-stu-id="7e823-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e823-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e823-125">Return value</span></span>

<span data-ttu-id="7e823-126">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7e823-126">Type: **LRESULT**</span></span>

<span data-ttu-id="7e823-127">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="7e823-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="7e823-128">範例</span><span class="sxs-lookup"><span data-stu-id="7e823-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="7e823-129">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="7e823-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e823-130">備註</span><span class="sxs-lookup"><span data-stu-id="7e823-130">Remarks</span></span>

<span data-ttu-id="7e823-131">如果針對子視窗呼叫 [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) 或 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式作為 **WM \_ 大小** 訊息的結果，則 *bRedraw* 或 *bRepaint* 參數應為非零，以使視窗重新繪製。</span><span class="sxs-lookup"><span data-stu-id="7e823-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="7e823-132">雖然視窗的寬度和高度是32位的值，但 *lParam* 參數只會包含每個值的低序位16位。</span><span class="sxs-lookup"><span data-stu-id="7e823-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="7e823-133">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會在處理 [**wm \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)訊息時，傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。</span><span class="sxs-lookup"><span data-stu-id="7e823-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="7e823-134">如果應用程式在不呼叫 **DefWindowProc** 的情況下處理 **wm \_ WINDOWPOSCHANGED** 訊息，則不會傳送 **wm \_ 大小** 和 **wm \_ 移動** 訊息。</span><span class="sxs-lookup"><span data-stu-id="7e823-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e823-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e823-135">Requirements</span></span>



| <span data-ttu-id="7e823-136">需求</span><span class="sxs-lookup"><span data-stu-id="7e823-136">Requirement</span></span> | <span data-ttu-id="7e823-137">值</span><span class="sxs-lookup"><span data-stu-id="7e823-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e823-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e823-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7e823-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e823-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e823-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e823-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7e823-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e823-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e823-142">標頭</span><span class="sxs-lookup"><span data-stu-id="7e823-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e823-143"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="7e823-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e823-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e823-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e823-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="7e823-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="7e823-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e823-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7e823-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e823-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7e823-148">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="7e823-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="7e823-149">**WM \_ WINDOWPOSCHANGED**</span><span class="sxs-lookup"><span data-stu-id="7e823-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="7e823-150">**概念**</span><span class="sxs-lookup"><span data-stu-id="7e823-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7e823-151">Windows</span><span class="sxs-lookup"><span data-stu-id="7e823-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="7e823-152">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="7e823-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7e823-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="7e823-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 
