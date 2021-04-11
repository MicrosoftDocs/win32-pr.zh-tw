---
title: 'EN_MSGFILTER (Richedit 的通知碼) '
description: 在控制項中通知 rich edit 控制項的鍵盤或滑鼠事件的父視窗。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103931"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="cf5a1-105">EN \_ MSGFILTER 通知碼</span><span class="sxs-lookup"><span data-stu-id="cf5a1-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="cf5a1-106">在控制項中通知 rich edit 控制項的鍵盤或滑鼠事件的父視窗。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="cf5a1-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cf5a1-108">參數</span><span class="sxs-lookup"><span data-stu-id="cf5a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf5a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf5a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf5a1-110">[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)結構，其中包含鍵盤或滑鼠訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="cf5a1-111">如果父視窗修改此結構並傳回非零值，則會處理修改過的訊息，而不是原始的訊息。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf5a1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf5a1-112">Return value</span></span>

<span data-ttu-id="cf5a1-113">如果控制項應該處理鍵盤或滑鼠事件，則傳回零。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="cf5a1-114">如果控制項應該忽略鍵盤或滑鼠事件，則傳回非零。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf5a1-115">備註</span><span class="sxs-lookup"><span data-stu-id="cf5a1-115">Remarks</span></span>

<span data-ttu-id="cf5a1-116">若要接收 \_ 事件的 EN MSGFILTER 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md) 訊息傳送的遮罩中指定下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="cf5a1-117">旗標</span><span class="sxs-lookup"><span data-stu-id="cf5a1-117">Flag</span></span>                                                                             | <span data-ttu-id="cf5a1-118">意義</span><span class="sxs-lookup"><span data-stu-id="cf5a1-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="cf5a1-119">**ENM \_ KEYEVENTS**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="cf5a1-120">接收鍵盤事件的通知碼。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="cf5a1-121">**ENM \_ MOUSEEVENTS**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="cf5a1-122">接收滑鼠事件的通知碼。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="cf5a1-123">**ENM \_ SCROLLEVENTS**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="cf5a1-124">接收滑鼠滾輪事件的通知碼。</span><span class="sxs-lookup"><span data-stu-id="cf5a1-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="cf5a1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf5a1-125">Requirements</span></span>



| <span data-ttu-id="cf5a1-126">需求</span><span class="sxs-lookup"><span data-stu-id="cf5a1-126">Requirement</span></span> | <span data-ttu-id="cf5a1-127">值</span><span class="sxs-lookup"><span data-stu-id="cf5a1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5a1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf5a1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf5a1-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf5a1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf5a1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf5a1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf5a1-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf5a1-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf5a1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="cf5a1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf5a1-133"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf5a1-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf5a1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf5a1-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf5a1-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf5a1-136">**MSGFILTER**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="cf5a1-137">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="cf5a1-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





