---
title: 'WM_CTLCOLORBTN 訊息 (Winuser .h) '
description: 在 \_ 繪製按鈕之前，會將 WM CTLCOLORBTN 訊息傳送至按鈕的父視窗。 父視窗可以變更按鈕的文字和背景色彩。 不過，只有主控描繪的按鈕會回應父視窗處理此訊息。
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- WM_CTLCOLORBTN message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfdaed4682cbd87bfd86d7829f7c828494ec46fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933905"
---
# <a name="wm_ctlcolorbtn-message"></a><span data-ttu-id="73111-106">WM \_ CTLCOLORBTN 訊息</span><span class="sxs-lookup"><span data-stu-id="73111-106">WM\_CTLCOLORBTN message</span></span>

<span data-ttu-id="73111-107">在繪製按鈕之前，會將 **WM \_ CTLCOLORBTN** 訊息傳送至按鈕的父視窗。</span><span class="sxs-lookup"><span data-stu-id="73111-107">The **WM\_CTLCOLORBTN** message is sent to the parent window of a button before drawing the button.</span></span> <span data-ttu-id="73111-108">父視窗可以變更按鈕的文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="73111-108">The parent window can change the button's text and background colors.</span></span> <span data-ttu-id="73111-109">不過，只有主控描繪的按鈕會回應父視窗處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="73111-109">However, only owner-drawn buttons respond to the parent window processing this message.</span></span>


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="73111-110">參數</span><span class="sxs-lookup"><span data-stu-id="73111-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73111-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73111-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73111-112">指定按鈕的顯示內容之控制碼的 **HDC** 。</span><span class="sxs-lookup"><span data-stu-id="73111-112">An **HDC** that specifies the handle to the display context for the button.</span></span>

</dd> <dt>

<span data-ttu-id="73111-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73111-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73111-114">指定按鈕之控制碼的 **HWND** 。</span><span class="sxs-lookup"><span data-stu-id="73111-114">An **HWND** that specifies the handle to the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73111-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="73111-115">Return value</span></span>

<span data-ttu-id="73111-116">如果應用程式處理此訊息，則必須將控制碼傳回給筆刷。</span><span class="sxs-lookup"><span data-stu-id="73111-116">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="73111-117">系統會使用筆刷來繪製按鈕的背景。</span><span class="sxs-lookup"><span data-stu-id="73111-117">The system uses the brush to paint the background of the button.</span></span>

## <a name="remarks"></a><span data-ttu-id="73111-118">備註</span><span class="sxs-lookup"><span data-stu-id="73111-118">Remarks</span></span>

<span data-ttu-id="73111-119">如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="73111-119">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="73111-120">如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="73111-120">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="73111-121">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取按鈕的預設系統色彩。</span><span class="sxs-lookup"><span data-stu-id="73111-121">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the button.</span></span> <span data-ttu-id="73111-122">具有 [**BS \_**](button-styles.md)按鈕、 [**BS \_ DEFPUSHBUTTON**](button-styles.md)或 [**BS \_ PUSHLIKE**](button-styles.md) 樣式的按鈕不會使用傳回的筆刷。</span><span class="sxs-lookup"><span data-stu-id="73111-122">Buttons with the [**BS\_PUSHBUTTON**](button-styles.md), [**BS\_DEFPUSHBUTTON**](button-styles.md), or [**BS\_PUSHLIKE**](button-styles.md) styles do not use the returned brush.</span></span> <span data-ttu-id="73111-123">具有這些樣式的按鈕一律會以預設的系統色彩繪製。</span><span class="sxs-lookup"><span data-stu-id="73111-123">Buttons with these styles are always drawn with the default system colors.</span></span> <span data-ttu-id="73111-124">繪圖推播按鈕需要數種不同的筆刷-臉部、反白顯示和陰影，但是 **WM \_ CTLCOLORBTN** 訊息只允許傳回一個筆刷。</span><span class="sxs-lookup"><span data-stu-id="73111-124">Drawing push buttons requires several different brushes-face, highlight, and shadow-but the **WM\_CTLCOLORBTN** message allows only one brush to be returned.</span></span> <span data-ttu-id="73111-125">若要為推播按鈕提供自訂外觀，請使用主控描繪按鈕。</span><span class="sxs-lookup"><span data-stu-id="73111-125">To provide a custom appearance for push buttons, use an owner-drawn button.</span></span> <span data-ttu-id="73111-126">如需詳細資訊，請參閱 [建立 Owner-Drawn 控制項](user-controls-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="73111-126">For more information, see [Creating Owner-Drawn Controls](user-controls-intro.md).</span></span>

<span data-ttu-id="73111-127">線上程之間永遠不會傳送 **WM \_ CTLCOLORBTN** 訊息。</span><span class="sxs-lookup"><span data-stu-id="73111-127">The **WM\_CTLCOLORBTN** message is never sent between threads.</span></span> <span data-ttu-id="73111-128">它只會在一個執行緒內傳送。</span><span class="sxs-lookup"><span data-stu-id="73111-128">It is sent only within one thread.</span></span>

<span data-ttu-id="73111-129">核取方塊或選項按鈕的文字色彩會套用至方塊或按鈕、其核取記號和文字。</span><span class="sxs-lookup"><span data-stu-id="73111-129">The text color of a check box or radio button applies to the box or button, its check mark, and the text.</span></span> <span data-ttu-id="73111-130">這些按鈕的焦點矩形會維持系統預設色彩 (通常是黑色) 。</span><span class="sxs-lookup"><span data-stu-id="73111-130">The focus rectangle for these buttons remains the system default color (typically black).</span></span> <span data-ttu-id="73111-131">群組方塊的文字色彩會套用至文字，但不會套用至定義方塊的線條。</span><span class="sxs-lookup"><span data-stu-id="73111-131">The text color of a group box applies to the text but not to the line that defines the box.</span></span> <span data-ttu-id="73111-132">按下按鈕的文字色彩只適用于其焦點矩形;它不會影響文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="73111-132">The text color of a push button applies only to its focus rectangle; it does not affect the color of the text.</span></span>

<span data-ttu-id="73111-133">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="73111-133">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="73111-134">如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。</span><span class="sxs-lookup"><span data-stu-id="73111-134">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="73111-135">\_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="73111-135">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="73111-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="73111-136">Requirements</span></span>



| <span data-ttu-id="73111-137">需求</span><span class="sxs-lookup"><span data-stu-id="73111-137">Requirement</span></span> | <span data-ttu-id="73111-138">值</span><span class="sxs-lookup"><span data-stu-id="73111-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73111-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73111-139">Minimum supported client</span></span><br/> | <span data-ttu-id="73111-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73111-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="73111-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73111-141">Minimum supported server</span></span><br/> | <span data-ttu-id="73111-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73111-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="73111-143">標頭</span><span class="sxs-lookup"><span data-stu-id="73111-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="73111-144"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="73111-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73111-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73111-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="73111-146">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="73111-146">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="73111-147">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="73111-147">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="73111-148">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="73111-148">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

