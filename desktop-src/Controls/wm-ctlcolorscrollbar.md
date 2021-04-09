---
title: 'WM_CTLCOLORSCROLLBAR 訊息 (Winuser .h) '
description: '\_當控制項即將繪製時，會將 WM CTLCOLORSCROLLBAR 訊息傳送到捲軸控制項的父視窗。'
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- WM_CTLCOLORSCROLLBAR message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934312"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="8c04f-104">WM \_ CTLCOLORSCROLLBAR 訊息</span><span class="sxs-lookup"><span data-stu-id="8c04f-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="8c04f-105">當控制項即將繪製時，會將 **WM \_ CTLCOLORSCROLLBAR** 訊息傳送到捲軸控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="8c04f-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="8c04f-106">藉由回應此訊息，父視窗可以使用顯示內容控制碼來設定捲軸控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="8c04f-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="8c04f-107">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="8c04f-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8c04f-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c04f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c04f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c04f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c04f-110">捲軸控制項的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c04f-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="8c04f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c04f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c04f-112">捲軸的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8c04f-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c04f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c04f-113">Return value</span></span>

<span data-ttu-id="8c04f-114">如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。</span><span class="sxs-lookup"><span data-stu-id="8c04f-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="8c04f-115">系統會使用筆刷來繪製捲軸控制項的背景。</span><span class="sxs-lookup"><span data-stu-id="8c04f-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c04f-116">備註</span><span class="sxs-lookup"><span data-stu-id="8c04f-116">Remarks</span></span>

<span data-ttu-id="8c04f-117">如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="8c04f-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="8c04f-118">如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="8c04f-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="8c04f-119">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取捲軸控制項的預設系統色彩。</span><span class="sxs-lookup"><span data-stu-id="8c04f-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="8c04f-120">線上程之間永遠不會傳送 **WM \_ CTLCOLORSCROLLBAR** 訊息，它只會在相同的執行緒內傳送。</span><span class="sxs-lookup"><span data-stu-id="8c04f-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="8c04f-121">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="8c04f-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="8c04f-122">如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。</span><span class="sxs-lookup"><span data-stu-id="8c04f-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="8c04f-123">\_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="8c04f-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="8c04f-124">只有子捲軸控制項才會使用 **WM \_ CTLCOLORSCROLLBAR** 訊息。</span><span class="sxs-lookup"><span data-stu-id="8c04f-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="8c04f-125">附加至視窗 (WS \_ SCROLL 和 WS \_ VSCROLL) 不會產生此訊息的捲軸。</span><span class="sxs-lookup"><span data-stu-id="8c04f-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="8c04f-126">若要自訂附加至視窗之捲軸的外觀，請使用一般捲軸函數。</span><span class="sxs-lookup"><span data-stu-id="8c04f-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c04f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c04f-127">Requirements</span></span>



| <span data-ttu-id="8c04f-128">需求</span><span class="sxs-lookup"><span data-stu-id="8c04f-128">Requirement</span></span> | <span data-ttu-id="8c04f-129">值</span><span class="sxs-lookup"><span data-stu-id="8c04f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c04f-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c04f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8c04f-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c04f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c04f-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c04f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8c04f-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c04f-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c04f-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8c04f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c04f-135"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8c04f-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c04f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c04f-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c04f-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="8c04f-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c04f-138">**WM \_ CTLCOLORBTN**</span><span class="sxs-lookup"><span data-stu-id="8c04f-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="8c04f-139">**WM \_ CTLCOLOREDIT**</span><span class="sxs-lookup"><span data-stu-id="8c04f-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="8c04f-140">**WM \_ CTLCOLORLISTBOX**</span><span class="sxs-lookup"><span data-stu-id="8c04f-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="8c04f-141">**WM \_ CTLCOLORSTATIC**</span><span class="sxs-lookup"><span data-stu-id="8c04f-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="8c04f-142">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="8c04f-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8c04f-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8c04f-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8c04f-144">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="8c04f-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="8c04f-145">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="8c04f-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="8c04f-146">**WM \_ CTLCOLORDLG**</span><span class="sxs-lookup"><span data-stu-id="8c04f-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

