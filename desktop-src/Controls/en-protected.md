---
title: 'EN_PROTECTED (Richedit 的通知碼) '
description: 通知 rich edit 控制項的父視窗，讓使用者採取動作來變更受保護的文字範圍。 Rich edit 控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465481"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="5b6ce-105">EN \_ 受保護的通知碼</span><span class="sxs-lookup"><span data-stu-id="5b6ce-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="5b6ce-106">通知 rich edit 控制項的父視窗，讓使用者採取動作來變更受保護的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="5b6ce-107">Rich edit 控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5b6ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b6ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b6ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b6ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b6ce-110">[**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected)結構，其中包含觸發通知碼之訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b6ce-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b6ce-111">Return value</span></span>

<span data-ttu-id="5b6ce-112">傳回零以允許操作。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="5b6ce-113">傳回非零值以防止作業。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b6ce-114">備註</span><span class="sxs-lookup"><span data-stu-id="5b6ce-114">Remarks</span></span>

<span data-ttu-id="5b6ce-115">如果傳回零，且 [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected)結構的 **msg**、 **wParam** 和 **lParam** 成員有所變更，控制項會處理修改過的訊息，而不是原始訊息。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="5b6ce-116">若要接收 EN-US \_ 受保護的通知碼，請在以 [**EM \_ SETEVENTMASK**](em-seteventmask.md)訊息傳送的遮罩中指定 [**ENM \_ PROTECTED**](rich-edit-control-event-mask-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="5b6ce-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b6ce-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b6ce-117">Requirements</span></span>



| <span data-ttu-id="5b6ce-118">需求</span><span class="sxs-lookup"><span data-stu-id="5b6ce-118">Requirement</span></span> | <span data-ttu-id="5b6ce-119">值</span><span class="sxs-lookup"><span data-stu-id="5b6ce-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6ce-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b6ce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5b6ce-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b6ce-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b6ce-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b6ce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5b6ce-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b6ce-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b6ce-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5b6ce-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b6ce-125"><dt>Richedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ce-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b6ce-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b6ce-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b6ce-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="5b6ce-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5b6ce-128">**ENPROTECTED**</span><span class="sxs-lookup"><span data-stu-id="5b6ce-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="5b6ce-129">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="5b6ce-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





