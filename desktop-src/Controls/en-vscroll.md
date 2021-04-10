---
title: 'EN_VSCROLL (Winuser 的通知碼) '
description: 當使用者按一下編輯控制項的垂直捲動條，或當使用者將滑鼠滾輪滾動至編輯控制項時傳送。
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844343"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="de3ea-104">EN \_ VSCROLL 通知碼</span><span class="sxs-lookup"><span data-stu-id="de3ea-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="de3ea-105">當使用者按一下編輯控制項的垂直捲動條，或當使用者將滑鼠滾輪滾動至編輯控制項時傳送。</span><span class="sxs-lookup"><span data-stu-id="de3ea-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="de3ea-106">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="de3ea-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="de3ea-107">在畫面更新之前，父視窗會收到通知。</span><span class="sxs-lookup"><span data-stu-id="de3ea-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="de3ea-108">參數</span><span class="sxs-lookup"><span data-stu-id="de3ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de3ea-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de3ea-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="de3ea-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="de3ea-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="de3ea-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="de3ea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de3ea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de3ea-113">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="de3ea-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de3ea-114">備註</span><span class="sxs-lookup"><span data-stu-id="de3ea-114">Remarks</span></span>

<span data-ttu-id="de3ea-115">這則訊息會針對垂直捲動條上的下列滑鼠事件傳送：按一下任一箭號按鈕，或在箭號按鈕與 thumb 之間按一下。</span><span class="sxs-lookup"><span data-stu-id="de3ea-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="de3ea-116">但是，當您按一下捲軸滑鼠本身時，不會傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="de3ea-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="de3ea-117">當鍵盤事件在編輯控制項的視圖區域中造成變更時（例如，按下 HOME、END、PAGE UP、PAGE DOWN、UP 箭號或向下箭號），也會傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="de3ea-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="de3ea-118">滑鼠滾輪是具有滾動滾輪的滑鼠。</span><span class="sxs-lookup"><span data-stu-id="de3ea-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="de3ea-119">如需詳細資訊，請參閱 [關於滑鼠輸入](/windows/desktop/inputdev/about-mouse-input)的「滑鼠滾輪」。</span><span class="sxs-lookup"><span data-stu-id="de3ea-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="de3ea-120">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="de3ea-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="de3ea-121">若要接收 EN \_ VSCROLL 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="de3ea-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="de3ea-122">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="de3ea-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de3ea-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="de3ea-123">Requirements</span></span>



| <span data-ttu-id="de3ea-124">需求</span><span class="sxs-lookup"><span data-stu-id="de3ea-124">Requirement</span></span> | <span data-ttu-id="de3ea-125">值</span><span class="sxs-lookup"><span data-stu-id="de3ea-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ea-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="de3ea-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de3ea-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de3ea-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="de3ea-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="de3ea-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de3ea-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="de3ea-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de3ea-130">標頭</span><span class="sxs-lookup"><span data-stu-id="de3ea-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="de3ea-131"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="de3ea-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3ea-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de3ea-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="de3ea-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="de3ea-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="de3ea-134">EN \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="de3ea-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="de3ea-135">**概念**</span><span class="sxs-lookup"><span data-stu-id="de3ea-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de3ea-136">使用編輯控制項</span><span class="sxs-lookup"><span data-stu-id="de3ea-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="de3ea-137">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="de3ea-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="de3ea-138">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="de3ea-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

