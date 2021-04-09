---
title: 'WM_CTLCOLORSTATIC 訊息 (Winuser .h) '
description: 靜態控制項，或是唯讀或停用的編輯控制項， \_ 會在即將繪製控制項時，將 WM CTLCOLORSTATIC 訊息傳送至其父視窗。
ms.assetid: a171a1e8-6845-4a8e-8394-44cea99d2b0d
keywords:
- WM_CTLCOLORSTATIC message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORSTATIC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851879eeb65a00f95f8cb81cef1b6c23ece8028d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685874"
---
# <a name="wm_ctlcolorstatic-message"></a><span data-ttu-id="1632d-104">WM \_ CTLCOLORSTATIC 訊息</span><span class="sxs-lookup"><span data-stu-id="1632d-104">WM\_CTLCOLORSTATIC message</span></span>

<span data-ttu-id="1632d-105">靜態控制項，或是唯讀或停用的編輯控制項，會在即將繪製控制項時，將 **WM \_ CTLCOLORSTATIC** 訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="1632d-105">A static control, or an edit control that is read-only or disabled, sends the **WM\_CTLCOLORSTATIC** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="1632d-106">藉由回應此訊息，父視窗可使用指定的裝置內容控制碼來設定靜態控制項的文字前景和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="1632d-106">By responding to this message, the parent window can use the specified device context handle to set the text foreground and background colors of the static control.</span></span>

<span data-ttu-id="1632d-107">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="1632d-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSTATIC

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1632d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1632d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1632d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1632d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1632d-110">靜態控制項視窗的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="1632d-110">Handle to the device context for the static control window.</span></span>

</dd> <dt>

<span data-ttu-id="1632d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1632d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1632d-112">靜態控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1632d-112">Handle to the static control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1632d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1632d-113">Return value</span></span>

<span data-ttu-id="1632d-114">如果應用程式處理此訊息，則傳回值會是系統用來繪製靜態控制項背景之筆刷的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1632d-114">If an application processes this message, the return value is a handle to a brush that the system uses to paint the background of the static control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1632d-115">備註</span><span class="sxs-lookup"><span data-stu-id="1632d-115">Remarks</span></span>

<span data-ttu-id="1632d-116">如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="1632d-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="1632d-117">如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="1632d-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="1632d-118">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取靜態控制項的預設系統色彩。</span><span class="sxs-lookup"><span data-stu-id="1632d-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the static control.</span></span>

<span data-ttu-id="1632d-119">您可以設定已停用編輯控制項的文字背景色彩，但無法設定文字前景色彩。</span><span class="sxs-lookup"><span data-stu-id="1632d-119">You can set the text background color of a disabled edit control, but you cannot set the text foreground color.</span></span> <span data-ttu-id="1632d-120">系統一律會使用色彩 \_ GRAYTEXT。</span><span class="sxs-lookup"><span data-stu-id="1632d-120">The system always uses COLOR\_GRAYTEXT.</span></span>

<span data-ttu-id="1632d-121">編輯非唯讀或停用的控制項不會傳送 **wm \_ CTLCOLORSTATIC** 訊息，而是會傳送 [**wm \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="1632d-121">Edit controls that are not read-only or disabled do not send the **WM\_CTLCOLORSTATIC** message; instead, they send the [**WM\_CTLCOLOREDIT**](wm-ctlcoloredit.md) message.</span></span>

<span data-ttu-id="1632d-122">線上程之間永遠不會傳送 **WM \_ CTLCOLORSTATIC** 訊息; 它只會在同一個執行緒內傳送。</span><span class="sxs-lookup"><span data-stu-id="1632d-122">The **WM\_CTLCOLORSTATIC** message is never sent between threads; it is sent only within the same thread.</span></span>

<span data-ttu-id="1632d-123">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="1632d-123">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="1632d-124">如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。</span><span class="sxs-lookup"><span data-stu-id="1632d-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="1632d-125">\_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="1632d-125">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="1632d-126">範例</span><span class="sxs-lookup"><span data-stu-id="1632d-126">Examples</span></span>

<span data-ttu-id="1632d-127">下列 c + + 範例顯示如何設定靜態控制項的文字前景和背景色彩，以回應 **WM \_ CTLCOLORSTATIC** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1632d-127">The following C++ example shows how to set the text foreground and background colors of a static control in response to the **WM\_CTLCOLORSTATIC** message.</span></span> <span data-ttu-id="1632d-128">`hbrBkgnd`變數是靜態 **HBRUSH** 變數，它會初始化為 Null，並在對 **WM \_ CTLCOLORSTATIC** 的呼叫之間儲存背景筆刷。</span><span class="sxs-lookup"><span data-stu-id="1632d-128">The `hbrBkgnd` variable is a static **HBRUSH** variable that is initialized to NULL, and stores the background brush between calls to **WM\_CTLCOLORSTATIC**.</span></span> <span data-ttu-id="1632d-129">當不再需要時，您必須呼叫 [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) 函式來終結筆刷，通常是在相關聯的對話方塊終結時。</span><span class="sxs-lookup"><span data-stu-id="1632d-129">The brush must be destroyed by a call to the [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) function when it is no longer needed, typically when the associated dialog box is destroyed.</span></span>


```C++
   case WM_CTLCOLORSTATIC:
        {
        HDC hdcStatic = (HDC) wParam;
        SetTextColor(hdcStatic, RGB(255,255,255));
        SetBkColor(hdcStatic, RGB(0,0,0));

        if (hbrBkgnd == NULL)
        {
            hbrBkgnd = CreateSolidBrush(RGB(0,0,0));
        }
        return (INT_PTR)hbrBkgnd;
        }
```



## <a name="requirements"></a><span data-ttu-id="1632d-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1632d-130">Requirements</span></span>



| <span data-ttu-id="1632d-131">需求</span><span class="sxs-lookup"><span data-stu-id="1632d-131">Requirement</span></span> | <span data-ttu-id="1632d-132">值</span><span class="sxs-lookup"><span data-stu-id="1632d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1632d-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1632d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1632d-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1632d-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1632d-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1632d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1632d-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1632d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1632d-137">標頭</span><span class="sxs-lookup"><span data-stu-id="1632d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1632d-138"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="1632d-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1632d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1632d-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="1632d-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="1632d-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1632d-141">**WM \_ CTLCOLORBTN**</span><span class="sxs-lookup"><span data-stu-id="1632d-141">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="1632d-142">**WM \_ CTLCOLOREDIT**</span><span class="sxs-lookup"><span data-stu-id="1632d-142">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="1632d-143">**WM \_ CTLCOLORLISTBOX**</span><span class="sxs-lookup"><span data-stu-id="1632d-143">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="1632d-144">**WM \_ CTLCOLORSCROLLBAR**</span><span class="sxs-lookup"><span data-stu-id="1632d-144">**WM\_CTLCOLORSCROLLBAR**</span></span>](wm-ctlcolorscrollbar.md)
</dt> <dt>

<span data-ttu-id="1632d-145">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="1632d-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1632d-146">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1632d-146">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1632d-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="1632d-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="1632d-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="1632d-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="1632d-149">**WM \_ CTLCOLORDLG**</span><span class="sxs-lookup"><span data-stu-id="1632d-149">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

