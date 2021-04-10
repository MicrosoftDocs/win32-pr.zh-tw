---
title: 'EN_CHANGE (Winuser 的通知碼) '
description: 當使用者採取的動作可能已更改編輯控制項中的文字時傳送。
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843356"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="457bd-104">EN \_ 變更通知碼</span><span class="sxs-lookup"><span data-stu-id="457bd-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="457bd-105">當使用者採取的動作可能已更改編輯控制項中的文字時傳送。</span><span class="sxs-lookup"><span data-stu-id="457bd-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="457bd-106">不同于 [EN \_ 更新](en-update.md) 通知碼，系統會在系統更新畫面之後傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="457bd-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="457bd-107">編輯控制項的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="457bd-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="457bd-108">參數</span><span class="sxs-lookup"><span data-stu-id="457bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="457bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="457bd-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含編輯控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="457bd-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="457bd-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="457bd-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="457bd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="457bd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="457bd-113">編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="457bd-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="457bd-114">備註</span><span class="sxs-lookup"><span data-stu-id="457bd-114">Remarks</span></span>

<span data-ttu-id="457bd-115">**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。</span><span class="sxs-lookup"><span data-stu-id="457bd-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="457bd-116">若要接收 EN-US \_ 變更通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ 變更**](rich-edit-control-event-mask-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="457bd-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="457bd-117">如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="457bd-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="457bd-118">\_使用 [**ES \_ 多行**](edit-control-styles.md)樣式，並透過 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)傳送文字時，不會傳送 EN 變更通知碼。</span><span class="sxs-lookup"><span data-stu-id="457bd-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="457bd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="457bd-119">Requirements</span></span>



| <span data-ttu-id="457bd-120">需求</span><span class="sxs-lookup"><span data-stu-id="457bd-120">Requirement</span></span> | <span data-ttu-id="457bd-121">值</span><span class="sxs-lookup"><span data-stu-id="457bd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="457bd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="457bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="457bd-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="457bd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="457bd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="457bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="457bd-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="457bd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="457bd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="457bd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="457bd-127"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="457bd-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="457bd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="457bd-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="457bd-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="457bd-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="457bd-130">EN \_ 更新</span><span class="sxs-lookup"><span data-stu-id="457bd-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="457bd-131">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="457bd-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="457bd-132">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="457bd-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

