---
title: 'EN_REQUESTRESIZE (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，控制項的內容小於控制項的視窗大小。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104496"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="f008c-105">EN \_ REQUESTRESIZE 通知碼</span><span class="sxs-lookup"><span data-stu-id="f008c-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="f008c-106">通知 rich edit 控制項的父視窗，控制項的內容小於控制項的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="f008c-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="f008c-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="f008c-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f008c-108">參數</span><span class="sxs-lookup"><span data-stu-id="f008c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f008c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f008c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f008c-110">接收所要求大小的 [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) 結構。</span><span class="sxs-lookup"><span data-stu-id="f008c-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f008c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f008c-111">Return value</span></span>

<span data-ttu-id="f008c-112">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f008c-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f008c-113">備註</span><span class="sxs-lookup"><span data-stu-id="f008c-113">Remarks</span></span>

<span data-ttu-id="f008c-114">若要支援 rich edit 控制項的無底邊行為，父視窗必須在收到此通知碼時調整控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="f008c-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="f008c-115">若要接收 EN \_ REQUESTRESIZE 通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="f008c-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f008c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f008c-116">Requirements</span></span>



| <span data-ttu-id="f008c-117">需求</span><span class="sxs-lookup"><span data-stu-id="f008c-117">Requirement</span></span> | <span data-ttu-id="f008c-118">值</span><span class="sxs-lookup"><span data-stu-id="f008c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f008c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f008c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f008c-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f008c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f008c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f008c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f008c-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f008c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f008c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f008c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f008c-124"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="f008c-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f008c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f008c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f008c-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="f008c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f008c-127">**REQRESIZE**</span><span class="sxs-lookup"><span data-stu-id="f008c-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="f008c-128">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="f008c-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





