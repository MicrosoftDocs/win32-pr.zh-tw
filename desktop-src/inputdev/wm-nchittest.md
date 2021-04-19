---
title: 'WM_NCHITTEST 訊息 (Winuser .h) '
description: 傳送至視窗，以判斷視窗的哪個部分對應至特定的螢幕座標。
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106983310"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="d6679-104">WM \_ NCHITTEST 訊息</span><span class="sxs-lookup"><span data-stu-id="d6679-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="d6679-105">傳送至視窗，以判斷視窗的哪個部分對應至特定的螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="d6679-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="d6679-106">例如，當游標移動時、按下或放開滑鼠按鍵時，或為了回應函式（例如 [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint)）的呼叫時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d6679-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="d6679-107">如果未捕捉到滑鼠，則會將訊息傳送至游標下的視窗。</span><span class="sxs-lookup"><span data-stu-id="d6679-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="d6679-108">否則，訊息會傳送至已捕捉滑鼠的視窗。</span><span class="sxs-lookup"><span data-stu-id="d6679-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="d6679-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="d6679-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="d6679-110">參數</span><span class="sxs-lookup"><span data-stu-id="d6679-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6679-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6679-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6679-112">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="d6679-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d6679-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6679-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6679-114">低序位字組指定游標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="d6679-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="d6679-115">座標相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="d6679-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="d6679-116">高序位字組指定游標的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="d6679-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="d6679-117">座標相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="d6679-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6679-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6679-118">Return value</span></span>

<span data-ttu-id="d6679-119">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式的傳回值是下列其中一個值，表示游標作用點的位置。</span><span class="sxs-lookup"><span data-stu-id="d6679-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="d6679-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d6679-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="d6679-121">Description</span><span class="sxs-lookup"><span data-stu-id="d6679-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6679-122"><dt>**HTBORDER**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="d6679-123">在沒有調整大小框線的視窗框線中。</span><span class="sxs-lookup"><span data-stu-id="d6679-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="d6679-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="d6679-125">在可調整大小之視窗的水準框線 (使用者可以按一下滑鼠，以垂直方式調整視窗的大小) 。</span><span class="sxs-lookup"><span data-stu-id="d6679-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="d6679-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="d6679-127">在可調整大小之視窗框線的左下角 (使用者可以按一下滑鼠，以對角線方式調整視窗的大小) 。</span><span class="sxs-lookup"><span data-stu-id="d6679-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="d6679-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="d6679-129">在可調整大小之視窗框線的右下角 (使用者可以按一下滑鼠，以對角線方式調整視窗的大小) 。</span><span class="sxs-lookup"><span data-stu-id="d6679-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d6679-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="d6679-131">在標題列中。</span><span class="sxs-lookup"><span data-stu-id="d6679-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d6679-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="d6679-133">在工作區中。</span><span class="sxs-lookup"><span data-stu-id="d6679-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d6679-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="d6679-135">在 [ **關閉** ] 按鈕中。</span><span class="sxs-lookup"><span data-stu-id="d6679-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="d6679-136"><dt>**HTERROR**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="d6679-137">在螢幕背景上或 windows (與 **HTNOWHERE** 相同的分隔線上，不同之處在于 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會產生系統嗶聲，指出) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d6679-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="d6679-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="d6679-139">在 [大小] 方塊中 (與 **HTSIZE**) 相同。</span><span class="sxs-lookup"><span data-stu-id="d6679-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="d6679-140"><dt>**HTHELP**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="d6679-141">**在 [說明] 按鈕中**。</span><span class="sxs-lookup"><span data-stu-id="d6679-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="d6679-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="d6679-143">水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="d6679-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="d6679-144"><dt>**HTLEFT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="d6679-145">在可調整大小之視窗的左邊框線中 (使用者可以按一下滑鼠，以水準方式調整視窗的大小) 。</span><span class="sxs-lookup"><span data-stu-id="d6679-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d6679-146"><dt>**HTMENU**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="d6679-147">在功能表中。</span><span class="sxs-lookup"><span data-stu-id="d6679-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d6679-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="d6679-149">在 [ **最大化** ] 按鈕中。</span><span class="sxs-lookup"><span data-stu-id="d6679-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d6679-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="d6679-151">在 [ **最小化** ] 按鈕中。</span><span class="sxs-lookup"><span data-stu-id="d6679-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d6679-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="d6679-153">在螢幕背景或視窗之間的分隔線上。</span><span class="sxs-lookup"><span data-stu-id="d6679-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="d6679-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="d6679-155">在 [ **最小化** ] 按鈕中。</span><span class="sxs-lookup"><span data-stu-id="d6679-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d6679-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="d6679-157">在可調整大小之視窗的右框線中 (使用者可以按一下滑鼠，以水準方式調整視窗的大小) 。</span><span class="sxs-lookup"><span data-stu-id="d6679-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d6679-158"><dt>**HTSIZE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="d6679-159">在 [大小] 方塊中 (與 **HTGROWBOX**) 相同。</span><span class="sxs-lookup"><span data-stu-id="d6679-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="d6679-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="d6679-161">在 [視窗] 功能表或子視窗的 [ **關閉** ] 按鈕中。</span><span class="sxs-lookup"><span data-stu-id="d6679-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="d6679-162"><dt>**HTTOP**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="d6679-163">在視窗的上水準框線中。</span><span class="sxs-lookup"><span data-stu-id="d6679-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="d6679-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="d6679-165">在視窗框線的左上角。</span><span class="sxs-lookup"><span data-stu-id="d6679-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="d6679-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="d6679-167">在視窗框線的右上角。</span><span class="sxs-lookup"><span data-stu-id="d6679-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="d6679-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="d6679-169">在目前由相同執行緒中的另一個視窗所涵蓋的視窗中 (會將訊息傳送至相同執行緒中的基礎視窗，直到其中一個傳回未 **HTTRANSPARENT**) 的程式碼為止。</span><span class="sxs-lookup"><span data-stu-id="d6679-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="d6679-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="d6679-171">在垂直捲動條中。</span><span class="sxs-lookup"><span data-stu-id="d6679-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="d6679-172"><dt>**HTZOOM**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d6679-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="d6679-173">在 [ **最大化** ] 按鈕中。</span><span class="sxs-lookup"><span data-stu-id="d6679-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d6679-174">備註</span><span class="sxs-lookup"><span data-stu-id="d6679-174">Remarks</span></span>

<span data-ttu-id="d6679-175">使用下列程式碼來取得水準和垂直位置：</span><span class="sxs-lookup"><span data-stu-id="d6679-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="d6679-176">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="d6679-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="d6679-177">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="d6679-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="d6679-178">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="d6679-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6679-179">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="d6679-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="d6679-180">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="d6679-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="d6679-181">**Windows Vista：** 建立包含標準標題按鈕的自訂框架時，應先將此訊息傳遞至 [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) 函式。</span><span class="sxs-lookup"><span data-stu-id="d6679-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="d6679-182">這可讓桌面視窗管理員 (DWM) 提供標題按鈕的點擊測試。</span><span class="sxs-lookup"><span data-stu-id="d6679-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="d6679-183">如果 **DwmDefWindowProc** 未處理訊息，可能需要進一步處理 **WM \_ NCHITTEST** 。</span><span class="sxs-lookup"><span data-stu-id="d6679-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6679-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6679-184">Requirements</span></span>



| <span data-ttu-id="d6679-185">需求</span><span class="sxs-lookup"><span data-stu-id="d6679-185">Requirement</span></span> | <span data-ttu-id="d6679-186">值</span><span class="sxs-lookup"><span data-stu-id="d6679-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6679-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6679-187">Minimum supported client</span></span><br/> | <span data-ttu-id="d6679-188">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6679-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d6679-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6679-189">Minimum supported server</span></span><br/> | <span data-ttu-id="d6679-190">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6679-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d6679-191">標頭</span><span class="sxs-lookup"><span data-stu-id="d6679-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6679-192"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="d6679-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6679-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6679-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6679-194">**參考**</span><span class="sxs-lookup"><span data-stu-id="d6679-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d6679-195">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d6679-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d6679-196">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="d6679-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="d6679-197">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="d6679-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="d6679-198">**概念**</span><span class="sxs-lookup"><span data-stu-id="d6679-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d6679-199">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="d6679-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="d6679-200">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="d6679-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d6679-201">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="d6679-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="d6679-202">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6679-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

