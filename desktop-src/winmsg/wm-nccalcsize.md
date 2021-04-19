---
description: 當必須計算視窗工作區的大小和位置時傳送。 藉由處理這個訊息，應用程式可以在視窗的大小或位置變更時，控制視窗工作區的內容。
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: 'WM_NCCALCSIZE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7d63fea3ad0a80bba686d8d86aa5354f0bb45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978978"
---
# <a name="wm_nccalcsize-message"></a><span data-ttu-id="d1699-104">WM \_ NCCALCSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="d1699-104">WM\_NCCALCSIZE message</span></span>

<span data-ttu-id="d1699-105">當必須計算視窗工作區的大小和位置時傳送。</span><span class="sxs-lookup"><span data-stu-id="d1699-105">Sent when the size and position of a window's client area must be calculated.</span></span> <span data-ttu-id="d1699-106">藉由處理這個訊息，應用程式可以在視窗的大小或位置變更時，控制視窗工作區的內容。</span><span class="sxs-lookup"><span data-stu-id="d1699-106">By processing this message, an application can control the content of the window's client area when the size or position of the window changes.</span></span>

<span data-ttu-id="d1699-107">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d1699-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a><span data-ttu-id="d1699-108">參數</span><span class="sxs-lookup"><span data-stu-id="d1699-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1699-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1699-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1699-110">如果 *wParam* 為 **TRUE**，它會指定應用程式應該指出工作區的哪個部分包含有效的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1699-110">If *wParam* is **TRUE**, it specifies that the application should indicate which part of the client area contains valid information.</span></span> <span data-ttu-id="d1699-111">系統會將有效的資訊複製到新工作區中的指定區域。</span><span class="sxs-lookup"><span data-stu-id="d1699-111">The system copies the valid information to the specified area within the new client area.</span></span>

<span data-ttu-id="d1699-112">如果 *wParam* 為 **FALSE**，則應用程式不需要表示工作區的有效部分。</span><span class="sxs-lookup"><span data-stu-id="d1699-112">If *wParam* is **FALSE**, the application does not need to indicate the valid part of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d1699-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1699-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1699-114">如果 *wParam* 為 **TRUE**， *lParam* 會指向 [**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) 結構，其中包含應用程式可用來計算用戶端矩形新大小和位置的資訊。</span><span class="sxs-lookup"><span data-stu-id="d1699-114">If *wParam* is **TRUE**, *lParam* points to an [**NCCALCSIZE\_PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) structure that contains information an application can use to calculate the new size and position of the client rectangle.</span></span>

<span data-ttu-id="d1699-115">如果 *wParam* 為 **FALSE**，則 *lParam* 會指向 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="d1699-115">If *wParam* is **FALSE**, *lParam* points to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="d1699-116">當輸入時，結構會包含視窗的建議視窗矩形。</span><span class="sxs-lookup"><span data-stu-id="d1699-116">On entry, the structure contains the proposed window rectangle for the window.</span></span> <span data-ttu-id="d1699-117">在結束時，結構應包含對應之視窗工作區的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="d1699-117">On exit, the structure should contain the screen coordinates of the corresponding window client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1699-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1699-118">Return value</span></span>

<span data-ttu-id="d1699-119">類型： **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d1699-119">Type: **LRESULT**</span></span>

<span data-ttu-id="d1699-120">如果 *wParam* 參數為 **FALSE**，則應用程式應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="d1699-120">If the *wParam* parameter is **FALSE**, the application should return zero.</span></span>

<span data-ttu-id="d1699-121">如果 *wParam* 為 **TRUE**，則應用程式應該傳回零或下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="d1699-121">If *wParam* is **TRUE**, the application should return zero or a combination of the following values.</span></span>

<span data-ttu-id="d1699-122">如果 *wParam* 為 **TRUE** ，且應用程式傳回零，則會保留舊的工作區，並與新工作區的左上角對齊。</span><span class="sxs-lookup"><span data-stu-id="d1699-122">If *wParam* is **TRUE** and an application returns zero, the old client area is preserved and is aligned with the upper-left corner of the new client area.</span></span>



| <span data-ttu-id="d1699-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d1699-123">Return code/value</span></span>                                                                                                                                           | <span data-ttu-id="d1699-124">Description</span><span class="sxs-lookup"><span data-stu-id="d1699-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1699-125"><dt>**WVR \_ALIGNTOP**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-125"><dt>**WVR\_ALIGNTOP**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="d1699-126">指定要保留視窗的工作區，並與視窗新位置的頂端對齊。</span><span class="sxs-lookup"><span data-stu-id="d1699-126">Specifies that the client area of the window is to be preserved and aligned with the top of the new position of the window.</span></span> <span data-ttu-id="d1699-127">例如，若要將工作區對齊左上角，請傳回 WVR \_ ALIGNTOP 和 **WVR \_ ALIGNLEFT** 值。</span><span class="sxs-lookup"><span data-stu-id="d1699-127">For example, to align the client area to the upper-left corner, return the WVR\_ALIGNTOP and **WVR\_ALIGNLEFT** values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="d1699-128"><dt>**WVR \_ALIGNRIGHT**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-128"><dt>**WVR\_ALIGNRIGHT**</dt> <dt>0x0080</dt></span></span> </dl>  | <span data-ttu-id="d1699-129">指定要保留視窗的工作區，並與視窗新位置的右邊對齊。</span><span class="sxs-lookup"><span data-stu-id="d1699-129">Specifies that the client area of the window is to be preserved and aligned with the right side of the new position of the window.</span></span> <span data-ttu-id="d1699-130">例如，若要將工作區對齊右下角，請傳回 **WVR \_ ALIGNRIGHT** 和 WVR \_ ALIGNBOTTOM 值。</span><span class="sxs-lookup"><span data-stu-id="d1699-130">For example, to align the client area to the lower-right corner, return the **WVR\_ALIGNRIGHT** and WVR\_ALIGNBOTTOM values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d1699-131"><dt>**WVR \_ALIGNLEFT**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-131"><dt>**WVR\_ALIGNLEFT**</dt> <dt>0x0020</dt></span></span> </dl>   | <span data-ttu-id="d1699-132">指定要保留視窗的工作區，並與視窗新位置的左邊對齊。</span><span class="sxs-lookup"><span data-stu-id="d1699-132">Specifies that the client area of the window is to be preserved and aligned with the left side of the new position of the window.</span></span> <span data-ttu-id="d1699-133">例如，若要將工作區對齊左下角，請傳回 **WVR \_ ALIGNLEFT** 和 **WVR \_ ALIGNBOTTOM** 值。</span><span class="sxs-lookup"><span data-stu-id="d1699-133">For example, to align the client area to the lower-left corner, return the **WVR\_ALIGNLEFT** and **WVR\_ALIGNBOTTOM** values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="d1699-134"><dt>**WVR \_ALIGNBOTTOM**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-134"><dt>**WVR\_ALIGNBOTTOM**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="d1699-135">指定要保留視窗的工作區，並與視窗新位置的底部對齊。</span><span class="sxs-lookup"><span data-stu-id="d1699-135">Specifies that the client area of the window is to be preserved and aligned with the bottom of the new position of the window.</span></span> <span data-ttu-id="d1699-136">例如，若要將工作區對齊左上角，請傳回 WVR \_ ALIGNTOP 和 **WVR \_ ALIGNLEFT** 值。</span><span class="sxs-lookup"><span data-stu-id="d1699-136">For example, to align the client area to the top-left corner, return the WVR\_ALIGNTOP and **WVR\_ALIGNLEFT** values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d1699-137"><dt>**WVR \_HREDRAW**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-137"><dt>**WVR\_HREDRAW**</dt> <dt>0x0100</dt></span></span> </dl>     | <span data-ttu-id="d1699-138">與任何其他值搭配使用（除了 **WVR \_ VALIDRECTS** 以外）時，如果用戶端矩形以水準方式變更大小，就會讓視窗完全重繪。</span><span class="sxs-lookup"><span data-stu-id="d1699-138">Used in combination with any other values, except **WVR\_VALIDRECTS**, causes the window to be completely redrawn if the client rectangle changes size horizontally.</span></span> <span data-ttu-id="d1699-139">此值類似于 [CS \_ HREDRAW](about-window-classes.md) 類別樣式</span><span class="sxs-lookup"><span data-stu-id="d1699-139">This value is similar to [CS\_HREDRAW](about-window-classes.md) class style</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="d1699-140"><dt>**WVR \_VREDRAW**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-140"><dt>**WVR\_VREDRAW**</dt> <dt>0x0200</dt></span></span> </dl>     | <span data-ttu-id="d1699-141">與任何其他值搭配使用（除了 **WVR \_ VALIDRECTS**）時，如果用戶端矩形的大小垂直變更，則會讓視窗完全重繪。</span><span class="sxs-lookup"><span data-stu-id="d1699-141">Used in combination with any other values, except **WVR\_VALIDRECTS**, causes the window to be completely redrawn if the client rectangle changes size vertically.</span></span> <span data-ttu-id="d1699-142">此值類似于 [CS \_ VREDRAW](about-window-classes.md) 類別樣式</span><span class="sxs-lookup"><span data-stu-id="d1699-142">This value is similar to [CS\_VREDRAW](about-window-classes.md) class style</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="d1699-143"><dt>**WVR \_重繪**</dt> <dt>0x0300</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-143"><dt>**WVR\_REDRAW**</dt> <dt>0x0300</dt></span></span> </dl>      | <span data-ttu-id="d1699-144">此值會重新繪製整個視窗。</span><span class="sxs-lookup"><span data-stu-id="d1699-144">This value causes the entire window to be redrawn.</span></span> <span data-ttu-id="d1699-145">它是 **WVR \_ HREDRAW** 和 **WVR \_ VREDRAW** 值的組合。</span><span class="sxs-lookup"><span data-stu-id="d1699-145">It is a combination of **WVR\_HREDRAW** and **WVR\_VREDRAW** values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="d1699-146"><dt>**WVR \_VALIDRECTS**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="d1699-146"><dt>**WVR\_VALIDRECTS**</dt> <dt>0x0400</dt></span></span> </dl>  | <span data-ttu-id="d1699-147">這個值表示，在從 [**WM \_ NCCALCSIZE**](wm-nccalcsize.md)傳回時，  \[ NCCALCSIZE PARAMS 結構的 rgrc 1 和 rgrc 2 成員所指定的矩形會 \]  \[ \] 分別包含有效的目的地和來源區域矩形。 [**\_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)</span><span class="sxs-lookup"><span data-stu-id="d1699-147">This value indicates that, upon return from [**WM\_NCCALCSIZE**](wm-nccalcsize.md), the rectangles specified by the **rgrc**\[1\] and **rgrc**\[2\] members of the [**NCCALCSIZE\_PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) structure contain valid destination and source area rectangles, respectively.</span></span> <span data-ttu-id="d1699-148">系統會合並這些矩形，以計算要保留的視窗區域。</span><span class="sxs-lookup"><span data-stu-id="d1699-148">The system combines these rectangles to calculate the area of the window to be preserved.</span></span> <span data-ttu-id="d1699-149">系統會複製來源矩形內視窗影像的任何部分，並將影像裁剪至目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="d1699-149">The system copies any part of the window image that is within the source rectangle and clips the image to the destination rectangle.</span></span> <span data-ttu-id="d1699-150">這兩個矩形都在父相對或螢幕相對座標中。</span><span class="sxs-lookup"><span data-stu-id="d1699-150">Both rectangles are in parent-relative or screen-relative coordinates.</span></span> <span data-ttu-id="d1699-151">此旗標無法與任何其他旗標合併。</span><span class="sxs-lookup"><span data-stu-id="d1699-151">This flag cannot be combined with any other flags.</span></span> <br/> <span data-ttu-id="d1699-152">此傳回值可讓應用程式執行更詳盡的用戶端區域保留原則，例如，將工作區的子集集中或保留。</span><span class="sxs-lookup"><span data-stu-id="d1699-152">This return value allows an application to implement more elaborate client-area preservation strategies, such as centering or preserving a subset of the client area.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1699-153">備註</span><span class="sxs-lookup"><span data-stu-id="d1699-153">Remarks</span></span>

<span data-ttu-id="d1699-154">視是否指定 [cs \_ HREDRAW](about-window-classes.md) 或 cs \_ VREDRAW 類別樣式而定，可能會重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="d1699-154">The window may be redrawn, depending on whether the [CS\_HREDRAW](about-window-classes.md) or CS\_VREDRAW class style is specified.</span></span> <span data-ttu-id="d1699-155">這是 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式 (的預設回溯相容性處理，除了上表中所述的一般用戶端矩形計算) 之外。</span><span class="sxs-lookup"><span data-stu-id="d1699-155">This is the default, backward-compatible processing of this message by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function (in addition to the usual client rectangle calculation described in the preceding table).</span></span>

<span data-ttu-id="d1699-156">當 *wParam* 為 **TRUE** 時，只要在未處理 [**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) 矩形的情況下傳回0，就會使工作區大小調整為視窗的大小，包括視窗框架。</span><span class="sxs-lookup"><span data-stu-id="d1699-156">When *wParam* is **TRUE**, simply returning 0 without processing the [**NCCALCSIZE\_PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) rectangles will cause the client area to resize to the size of the window, including the window frame.</span></span> <span data-ttu-id="d1699-157">這會從您的視窗中移除視窗框架和標題專案，只留下顯示的工作區。</span><span class="sxs-lookup"><span data-stu-id="d1699-157">This will remove the window frame and caption items from your window, leaving only the client area displayed.</span></span>

<span data-ttu-id="d1699-158">從 Windows Vista 開始，只要在 *wParam* 為 **TRUE** 時傳回0，就不會影響使用 [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 函式延伸至工作區的框架，藉以移除標準框架。</span><span class="sxs-lookup"><span data-stu-id="d1699-158">Starting with Windows Vista, removing the standard frame by simply returning 0 when the *wParam* is **TRUE** does not affect frames that are extended into the client area using the [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span> <span data-ttu-id="d1699-159">只會移除標準框架。</span><span class="sxs-lookup"><span data-stu-id="d1699-159">Only the standard frame will be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1699-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1699-160">Requirements</span></span>



| <span data-ttu-id="d1699-161">需求</span><span class="sxs-lookup"><span data-stu-id="d1699-161">Requirement</span></span> | <span data-ttu-id="d1699-162">值</span><span class="sxs-lookup"><span data-stu-id="d1699-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1699-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1699-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d1699-164">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1699-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d1699-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1699-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d1699-166">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1699-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1699-167">標頭</span><span class="sxs-lookup"><span data-stu-id="d1699-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1699-168"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d1699-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1699-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1699-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1699-170">**參考**</span><span class="sxs-lookup"><span data-stu-id="d1699-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1699-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d1699-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d1699-172">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="d1699-172">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="d1699-173">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="d1699-173">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="d1699-174">**NCCALCSIZE \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="d1699-174">**NCCALCSIZE\_PARAMS**</span></span>](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

<span data-ttu-id="d1699-175">**概念**</span><span class="sxs-lookup"><span data-stu-id="d1699-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1699-176">Windows</span><span class="sxs-lookup"><span data-stu-id="d1699-176">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="d1699-177">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="d1699-177">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d1699-178">[**矩形**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1699-178">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
