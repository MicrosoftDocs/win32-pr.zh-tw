---
title: 'EN_MAXTEXT (Winuser 的通知碼) '
description: 當目前的文字插入超過編輯控制項的指定字元數時傳送。
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509163"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="eb05d-104">EN \_ MAXTEXT 通知碼</span><span class="sxs-lookup"><span data-stu-id="eb05d-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="eb05d-105">當目前的文字插入超過編輯控制項的指定字元數時傳送。</span><span class="sxs-lookup"><span data-stu-id="eb05d-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="eb05d-106">文字插入已被截斷。</span><span class="sxs-lookup"><span data-stu-id="eb05d-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="eb05d-107">當編輯控制項沒有 [**ES \_ AUTOHSCROLL**](edit-control-styles.md) 樣式，而且要插入的字元數超過編輯控制項的寬度時，也會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="eb05d-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="eb05d-108">當編輯控制項沒有 [**ES \_ AUTOVSCROLL**](edit-control-styles.md) 樣式，而且文字插入所產生的行總數超過編輯控制項的高度時，也會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="eb05d-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="eb05d-109">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="eb05d-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="eb05d-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb05d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb05d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb05d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb05d-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb05d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="eb05d-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="eb05d-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="eb05d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb05d-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb05d-115">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb05d-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb05d-116">備註</span><span class="sxs-lookup"><span data-stu-id="eb05d-116">Remarks</span></span>

<span data-ttu-id="eb05d-117">父視窗一律會收到此事件的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。</span><span class="sxs-lookup"><span data-stu-id="eb05d-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="eb05d-118">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="eb05d-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="eb05d-119">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="eb05d-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb05d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb05d-120">Requirements</span></span>



| <span data-ttu-id="eb05d-121">需求</span><span class="sxs-lookup"><span data-stu-id="eb05d-121">Requirement</span></span> | <span data-ttu-id="eb05d-122">值</span><span class="sxs-lookup"><span data-stu-id="eb05d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb05d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb05d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="eb05d-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb05d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eb05d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb05d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="eb05d-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb05d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eb05d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="eb05d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb05d-128"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="eb05d-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb05d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb05d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb05d-130">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="eb05d-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

