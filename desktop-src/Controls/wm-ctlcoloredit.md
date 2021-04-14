---
title: 'WM_CTLCOLOREDIT 訊息 (Winuser .h) '
description: 不是唯讀或停用的編輯控制項，會在 \_ 即將繪製控制項時，將 WM CTLCOLOREDIT 訊息傳送至其父視窗。
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT message Windows 控制項
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464237"
---
# <a name="wm_ctlcoloredit-message"></a><span data-ttu-id="69215-104">WM \_ CTLCOLOREDIT 訊息</span><span class="sxs-lookup"><span data-stu-id="69215-104">WM\_CTLCOLOREDIT message</span></span>

<span data-ttu-id="69215-105">不是唯讀或停用的編輯控制項，會在即將繪製控制項時，將 **WM \_ CTLCOLOREDIT** 訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="69215-105">An edit control that is not read-only or disabled sends the **WM\_CTLCOLOREDIT** message to its parent window when the control is about to be drawn.</span></span> <span data-ttu-id="69215-106">藉由回應此訊息，父視窗可使用指定的裝置內容控制碼來設定編輯控制項的文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="69215-106">By responding to this message, the parent window can use the specified device context handle to set the text and background colors of the edit control.</span></span>


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="69215-107">參數</span><span class="sxs-lookup"><span data-stu-id="69215-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69215-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69215-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69215-109">編輯控制項視窗的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="69215-109">A handle to the device context for the edit control window.</span></span>

</dd> <dt>

<span data-ttu-id="69215-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69215-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69215-111">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="69215-111">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69215-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="69215-112">Return value</span></span>

<span data-ttu-id="69215-113">如果應用程式處理此訊息，則必須傳回筆刷的控制碼。</span><span class="sxs-lookup"><span data-stu-id="69215-113">If an application processes this message, it must return the handle of a brush.</span></span> <span data-ttu-id="69215-114">系統會使用筆刷來繪製編輯控制項的背景。</span><span class="sxs-lookup"><span data-stu-id="69215-114">The system uses the brush to paint the background of the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="69215-115">備註</span><span class="sxs-lookup"><span data-stu-id="69215-115">Remarks</span></span>

<span data-ttu-id="69215-116">如果應用程式傳回所建立的筆刷 (例如，藉由使用 [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) 或 [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) 函數) ，應用程式必須釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="69215-116">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="69215-117">如果應用程式傳回的系統筆刷 (例如， [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) 或 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 函式所抓取的) ，則應用程式不需要釋放筆刷。</span><span class="sxs-lookup"><span data-stu-id="69215-117">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="69215-118">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會選取編輯控制項的預設系統色彩。</span><span class="sxs-lookup"><span data-stu-id="69215-118">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the edit control.</span></span>

<span data-ttu-id="69215-119">唯讀或停用的編輯控制項不會傳送 **wm \_ CTLCOLOREDIT** 訊息，而是會傳送 [**wm \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="69215-119">Read-only or disabled edit controls do not send the **WM\_CTLCOLOREDIT** message; instead, they send the [**WM\_CTLCOLORSTATIC**](wm-ctlcolorstatic.md) message.</span></span>

<span data-ttu-id="69215-120">線上程之間永遠不會傳送 **WM \_ CTLCOLOREDIT** 訊息，它只會在相同的執行緒中傳送。</span><span class="sxs-lookup"><span data-stu-id="69215-120">The **WM\_CTLCOLOREDIT** message is never sent between threads, it is only sent within the same thread.</span></span>

<span data-ttu-id="69215-121">如果對話方塊程式處理此訊息，則應該將所需的傳回值轉換成 **INT \_ PTR** 並直接傳回值。</span><span class="sxs-lookup"><span data-stu-id="69215-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="69215-122">如果對話方塊程式傳回 **FALSE**，則會執行預設訊息處理。</span><span class="sxs-lookup"><span data-stu-id="69215-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="69215-123">\_ [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數所設定的 DWL MSGRESULT 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="69215-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="69215-124">**Rich Edit：** 不支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="69215-124">**Rich Edit:** This message is not supported.</span></span> <span data-ttu-id="69215-125">若要設定 rich edit 控制項的背景色彩，請使用 [**EM \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="69215-125">To set the background color for a rich edit control, use the [**EM\_SETBKGNDCOLOR**](em-setbkgndcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="69215-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="69215-126">Requirements</span></span>



| <span data-ttu-id="69215-127">需求</span><span class="sxs-lookup"><span data-stu-id="69215-127">Requirement</span></span> | <span data-ttu-id="69215-128">值</span><span class="sxs-lookup"><span data-stu-id="69215-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69215-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69215-129">Minimum supported client</span></span><br/> | <span data-ttu-id="69215-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69215-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69215-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69215-131">Minimum supported server</span></span><br/> | <span data-ttu-id="69215-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69215-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69215-133">標頭</span><span class="sxs-lookup"><span data-stu-id="69215-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="69215-134"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="69215-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69215-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69215-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="69215-136">**參考**</span><span class="sxs-lookup"><span data-stu-id="69215-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69215-137">**EM \_ SETBKGNDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="69215-137">**EM\_SETBKGNDCOLOR**</span></span>](em-setbkgndcolor.md)
</dt> <dt>

[<span data-ttu-id="69215-138">**WM \_ CTLCOLORSTATIC**</span><span class="sxs-lookup"><span data-stu-id="69215-138">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="69215-139">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="69215-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="69215-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="69215-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="69215-141">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="69215-141">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="69215-142">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="69215-142">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

