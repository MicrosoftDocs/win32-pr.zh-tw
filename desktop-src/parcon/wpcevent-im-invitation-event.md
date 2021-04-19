---
description: 提供的每個使用者事件，可供立即訊息用戶端用來記錄對話的起始。
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: 'WPCEVENT_IM_INVITATION (Wpcevent 的事件) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87c9d7e90eaa901b5e18a072e03e3112ee8c2934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978085"
---
# <a name="wpcevent_im_invitation-event"></a><span data-ttu-id="3bc97-103">WPCEVENT \_ IM \_ 邀請事件</span><span class="sxs-lookup"><span data-stu-id="3bc97-103">WPCEVENT\_IM\_INVITATION event</span></span>

<span data-ttu-id="3bc97-104">提供的每個使用者事件，可供立即訊息用戶端用來記錄對話的起始。</span><span class="sxs-lookup"><span data-stu-id="3bc97-104">Per-user event provided for logging initiation of conversations by Instant Messaging clients.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="3bc97-105">參數</span><span class="sxs-lookup"><span data-stu-id="3bc97-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc97-106">*AppName*</span><span class="sxs-lookup"><span data-stu-id="3bc97-106">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-107">產生事件的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="3bc97-107">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-108">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="3bc97-108">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-109">產生事件之應用程式的版本字串。</span><span class="sxs-lookup"><span data-stu-id="3bc97-109">The version string for the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-110">*AccountName*</span><span class="sxs-lookup"><span data-stu-id="3bc97-110">*AccountName*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-111">立即訊息帳戶識別字串。</span><span class="sxs-lookup"><span data-stu-id="3bc97-111">The instant messaging account identity string.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-112">*ConvID*</span><span class="sxs-lookup"><span data-stu-id="3bc97-112">*ConvID*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-113">交談的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bc97-113">The identifier for the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-114">*RequestingIP*</span><span class="sxs-lookup"><span data-stu-id="3bc97-114">*RequestingIP*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-115">字串，其中包含正在傳送邀請的電腦 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3bc97-115">A string that contains the IP address of the computer that is sending the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-116">*傳送者*</span><span class="sxs-lookup"><span data-stu-id="3bc97-116">*Sender*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-117">發出邀請之帳戶的立即訊息帳戶識別字串。</span><span class="sxs-lookup"><span data-stu-id="3bc97-117">The instant messaging account identity string for the account that is issuing the invitation.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-118">*原因*</span><span class="sxs-lookup"><span data-stu-id="3bc97-118">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-119">[**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked)列舉值，這個值會指出哪些事件遭到封鎖而無法使用的資訊，以及已有哪些控制項。</span><span class="sxs-lookup"><span data-stu-id="3bc97-119">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-120">*RecipCount*</span><span class="sxs-lookup"><span data-stu-id="3bc97-120">*RecipCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-121">接收邀請的收件者計數，以及收件者欄位中定義的身分識別。</span><span class="sxs-lookup"><span data-stu-id="3bc97-121">The count of recipients who are receiving the invitation and who have identities defined in the recipient field.</span></span>

</dd> <dt>

<span data-ttu-id="3bc97-122">*收件者*</span><span class="sxs-lookup"><span data-stu-id="3bc97-122">*Recipient*</span></span> 
</dt> <dd>

<span data-ttu-id="3bc97-123">包含邀請收件者之立即訊息帳戶識別字串的分隔字串。</span><span class="sxs-lookup"><span data-stu-id="3bc97-123">A delimited string that contains instant messaging account identity strings for the recipients of the invitation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bc97-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bc97-124">Requirements</span></span>



| <span data-ttu-id="3bc97-125">需求</span><span class="sxs-lookup"><span data-stu-id="3bc97-125">Requirement</span></span> | <span data-ttu-id="3bc97-126">值</span><span class="sxs-lookup"><span data-stu-id="3bc97-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc97-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bc97-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc97-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bc97-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3bc97-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bc97-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc97-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="3bc97-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="3bc97-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3bc97-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc97-132"><dt>Wpcevent。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc97-132"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc97-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bc97-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc97-134">使用適用于家長監護的記錄 Api</span><span class="sxs-lookup"><span data-stu-id="3bc97-134">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="3bc97-135">**WPC 的 \_ ARGS \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="3bc97-135">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




