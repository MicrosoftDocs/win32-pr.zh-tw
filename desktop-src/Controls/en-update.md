---
title: 'EN_UPDATE (Winuser 的通知碼) '
description: 當編輯控制項即將重新繪製時傳送。
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105551"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="5548b-104">EN \_ 更新通知碼</span><span class="sxs-lookup"><span data-stu-id="5548b-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="5548b-105">當編輯控制項即將重新繪製時傳送。</span><span class="sxs-lookup"><span data-stu-id="5548b-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="5548b-106">此通知碼會在控制項格式化文字之後，但在顯示文字之前傳送。</span><span class="sxs-lookup"><span data-stu-id="5548b-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="5548b-107">如此一來，就可以視需要調整編輯控制項視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="5548b-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="5548b-108">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="5548b-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="5548b-109">參數</span><span class="sxs-lookup"><span data-stu-id="5548b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5548b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5548b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5548b-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5548b-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="5548b-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="5548b-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5548b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5548b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5548b-114">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5548b-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5548b-115">備註</span><span class="sxs-lookup"><span data-stu-id="5548b-115">Remarks</span></span>

<span data-ttu-id="5548b-116">**Rich Edit 1.0：** 若要接收 EN \_ 更新通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="5548b-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="5548b-117">**Rich Edit 2.0 和更新版本：** 已忽略 [**ENM \_ 更新**](rich-edit-control-event-mask-flags.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="5548b-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="5548b-118">\_一律會收到 EN 更新通知代碼。</span><span class="sxs-lookup"><span data-stu-id="5548b-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="5548b-119">不過，當 Microsoft Rich Edit 3.0 模擬 Microsoft Rich Edit 1.0 時，若要接收 EN-US \_ 更新通知碼，您必須在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 **ENM \_ UPDATE** 。</span><span class="sxs-lookup"><span data-stu-id="5548b-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="5548b-120">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="5548b-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5548b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5548b-121">Requirements</span></span>



| <span data-ttu-id="5548b-122">需求</span><span class="sxs-lookup"><span data-stu-id="5548b-122">Requirement</span></span> | <span data-ttu-id="5548b-123">值</span><span class="sxs-lookup"><span data-stu-id="5548b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5548b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5548b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5548b-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5548b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5548b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5548b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5548b-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5548b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5548b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5548b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5548b-129"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="5548b-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5548b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5548b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5548b-131">**參考**</span><span class="sxs-lookup"><span data-stu-id="5548b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5548b-132">EN \_ 變更</span><span class="sxs-lookup"><span data-stu-id="5548b-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="5548b-133">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="5548b-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5548b-134">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="5548b-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

