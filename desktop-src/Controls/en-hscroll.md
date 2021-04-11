---
title: 'EN_HSCROLL (Winuser 的通知碼) '
description: 當使用者按一下編輯控制項的水準捲軸時傳送。 編輯控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。 在畫面更新之前，父視窗會收到通知。
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843799"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="cb27a-106">EN \_ HSCROLL 通知碼</span><span class="sxs-lookup"><span data-stu-id="cb27a-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="cb27a-107">當使用者按一下編輯控制項的水準捲軸時傳送。</span><span class="sxs-lookup"><span data-stu-id="cb27a-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="cb27a-108">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="cb27a-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="cb27a-109">在畫面更新之前，父視窗會收到通知。</span><span class="sxs-lookup"><span data-stu-id="cb27a-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="cb27a-110">參數</span><span class="sxs-lookup"><span data-stu-id="cb27a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb27a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb27a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb27a-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb27a-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="cb27a-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="cb27a-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="cb27a-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb27a-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb27a-115">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cb27a-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb27a-116">備註</span><span class="sxs-lookup"><span data-stu-id="cb27a-116">Remarks</span></span>

<span data-ttu-id="cb27a-117">此通知碼會針對水準捲軸上的下列滑鼠事件傳送：按一下任一箭號按鈕，或在箭號按鈕與 thumb 之間按一下。</span><span class="sxs-lookup"><span data-stu-id="cb27a-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="cb27a-118">不過，在按一下捲軸捲軸時，不會傳送通知碼。</span><span class="sxs-lookup"><span data-stu-id="cb27a-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="cb27a-119">當鍵盤事件在編輯控制項的視圖區域中造成變更時（例如，按下 HOME、END、向左鍵或向右箭號），也會傳送通知碼。</span><span class="sxs-lookup"><span data-stu-id="cb27a-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="cb27a-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="cb27a-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="cb27a-121">若要接收 **EN \_ HSCROLL** 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="cb27a-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="cb27a-122">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="cb27a-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb27a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb27a-123">Requirements</span></span>



| <span data-ttu-id="cb27a-124">需求</span><span class="sxs-lookup"><span data-stu-id="cb27a-124">Requirement</span></span> | <span data-ttu-id="cb27a-125">值</span><span class="sxs-lookup"><span data-stu-id="cb27a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb27a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb27a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cb27a-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb27a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb27a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb27a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cb27a-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb27a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb27a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cb27a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb27a-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="cb27a-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb27a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb27a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb27a-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="cb27a-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb27a-134">EN \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="cb27a-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="cb27a-135">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="cb27a-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cb27a-136">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="cb27a-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

