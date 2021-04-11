---
title: 'EN_CHANGE (rich edit) 通知碼 (Winuser) '
description: 通知無視窗、rich edit 控制項的主視窗已發生變更。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE (rich edit) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934205"
---
# <a name="en_change-rich-edit-notification-code"></a><span data-ttu-id="2464a-105">EN \_ 變更 (rich edit) 通知碼</span><span class="sxs-lookup"><span data-stu-id="2464a-105">EN\_CHANGE (rich edit) notification code</span></span>

<span data-ttu-id="2464a-106">通知無視窗、rich edit 控制項的主視窗已發生變更。</span><span class="sxs-lookup"><span data-stu-id="2464a-106">Notifies a windowless rich edit control's host window that a change has occurred.</span></span> <span data-ttu-id="2464a-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="2464a-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2464a-108">參數</span><span class="sxs-lookup"><span data-stu-id="2464a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2464a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2464a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2464a-110">[**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify)結構，指定所做的變更。</span><span class="sxs-lookup"><span data-stu-id="2464a-110">A [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) structure specifying the change that was made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2464a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2464a-111">Return value</span></span>

<span data-ttu-id="2464a-112">此通知碼不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2464a-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2464a-113">備註</span><span class="sxs-lookup"><span data-stu-id="2464a-113">Remarks</span></span>

<span data-ttu-id="2464a-114">若要接收 EN-US \_ 變更通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ 變更**](rich-edit-control-event-mask-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="2464a-114">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2464a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2464a-115">Requirements</span></span>



| <span data-ttu-id="2464a-116">需求</span><span class="sxs-lookup"><span data-stu-id="2464a-116">Requirement</span></span> | <span data-ttu-id="2464a-117">值</span><span class="sxs-lookup"><span data-stu-id="2464a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2464a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2464a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2464a-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2464a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2464a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2464a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2464a-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2464a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2464a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2464a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2464a-123"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="2464a-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2464a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2464a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2464a-125">**TxNotify**</span><span class="sxs-lookup"><span data-stu-id="2464a-125">**TxNotify**</span></span>](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





