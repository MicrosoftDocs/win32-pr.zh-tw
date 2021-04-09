---
title: 'EN_KILLFOCUS (Winuser 的通知碼) '
description: 當編輯控制項失去鍵盤焦點時傳送。 編輯控制項的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: c31f4b6c-afed-4506-b98a-65c902b0f63a
keywords:
- EN_KILLFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c30c037d985647f50b93402667832b18b3897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843156"
---
# <a name="en_killfocus-notification-code"></a><span data-ttu-id="4de03-105">EN \_ KILLFOCUS 通知碼</span><span class="sxs-lookup"><span data-stu-id="4de03-105">EN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="4de03-106">當編輯控制項失去鍵盤焦點時傳送。</span><span class="sxs-lookup"><span data-stu-id="4de03-106">Sent when an edit control loses the keyboard focus.</span></span> <span data-ttu-id="4de03-107">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="4de03-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4de03-108">參數</span><span class="sxs-lookup"><span data-stu-id="4de03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4de03-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4de03-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4de03-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4de03-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="4de03-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="4de03-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="4de03-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4de03-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4de03-113">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4de03-113">Handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4de03-114">備註</span><span class="sxs-lookup"><span data-stu-id="4de03-114">Remarks</span></span>

<span data-ttu-id="4de03-115">父視窗一律會收到此事件的 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息，不需要以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)傳送通知遮罩。</span><span class="sxs-lookup"><span data-stu-id="4de03-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="4de03-116">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="4de03-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4de03-117">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="4de03-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4de03-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4de03-118">Requirements</span></span>



| <span data-ttu-id="4de03-119">需求</span><span class="sxs-lookup"><span data-stu-id="4de03-119">Requirement</span></span> | <span data-ttu-id="4de03-120">值</span><span class="sxs-lookup"><span data-stu-id="4de03-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de03-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4de03-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4de03-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4de03-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4de03-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4de03-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4de03-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4de03-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4de03-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4de03-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de03-126"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4de03-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de03-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4de03-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4de03-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="4de03-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4de03-129">**EN \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="4de03-129">**EN\_SETFOCUS**</span></span>](en-setfocus.md)
</dt> <dt>

<span data-ttu-id="4de03-130">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="4de03-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4de03-131">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="4de03-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

