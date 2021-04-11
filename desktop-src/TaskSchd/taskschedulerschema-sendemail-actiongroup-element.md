---
title: SendEmail (actionGroup) 元素
description: 表示傳送電子郵件訊息的動作。
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- SendEmail 元素工作排程器
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934828"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="f4c22-104">SendEmail (actionGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="f4c22-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="f4c22-105">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="f4c22-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="f4c22-106">**SendEmail** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="f4c22-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f4c22-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f4c22-107">Parent element</span></span>



| <span data-ttu-id="f4c22-108">元素</span><span class="sxs-lookup"><span data-stu-id="f4c22-108">Element</span></span>                                                         | <span data-ttu-id="f4c22-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="f4c22-109">Derived from</span></span>                                                       | <span data-ttu-id="f4c22-110">Description</span><span class="sxs-lookup"><span data-stu-id="f4c22-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f4c22-111">**行動**</span><span class="sxs-lookup"><span data-stu-id="f4c22-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="f4c22-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="f4c22-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="f4c22-113">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="f4c22-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f4c22-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f4c22-114">Child elements</span></span>



| <span data-ttu-id="f4c22-115">元素</span><span class="sxs-lookup"><span data-stu-id="f4c22-115">Element</span></span>                                                                        | <span data-ttu-id="f4c22-116">類型</span><span class="sxs-lookup"><span data-stu-id="f4c22-116">Type</span></span>                                                                         | <span data-ttu-id="f4c22-117">Description</span><span class="sxs-lookup"><span data-stu-id="f4c22-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c22-118">**附件**</span><span class="sxs-lookup"><span data-stu-id="f4c22-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="f4c22-119">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="f4c22-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="f4c22-120">指定電子郵件訊息中的附件清單。</span><span class="sxs-lookup"><span data-stu-id="f4c22-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="f4c22-121">**密件副本**</span><span class="sxs-lookup"><span data-stu-id="f4c22-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="f4c22-122">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-122">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-123">指定電子郵件訊息的 [密件副本] 行上使用的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f4c22-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="f4c22-124">**主體**</span><span class="sxs-lookup"><span data-stu-id="f4c22-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="f4c22-125">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-125">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-126">指定電子郵件訊息主體中的文字。</span><span class="sxs-lookup"><span data-stu-id="f4c22-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="f4c22-127">**Cc**</span><span class="sxs-lookup"><span data-stu-id="f4c22-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="f4c22-128">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-128">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-129">指定電子郵件訊息之 Cc 行上使用的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f4c22-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="f4c22-130">**寄件者**</span><span class="sxs-lookup"><span data-stu-id="f4c22-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="f4c22-131">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-131">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-132">指定寄件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f4c22-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="f4c22-133">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="f4c22-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="f4c22-134">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="f4c22-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="f4c22-135">指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。</span><span class="sxs-lookup"><span data-stu-id="f4c22-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="f4c22-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="f4c22-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="f4c22-137">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-137">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-138">指定電子郵件訊息中要回復的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f4c22-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="f4c22-139">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="f4c22-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="f4c22-140">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="f4c22-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="f4c22-141">指定用來傳送電子郵件訊息的電子郵件伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4c22-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="f4c22-142">**主體**</span><span class="sxs-lookup"><span data-stu-id="f4c22-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="f4c22-143">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-143">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-144">指定電子郵件訊息的主旨。</span><span class="sxs-lookup"><span data-stu-id="f4c22-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="f4c22-145">**自**</span><span class="sxs-lookup"><span data-stu-id="f4c22-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="f4c22-146">**string**</span><span class="sxs-lookup"><span data-stu-id="f4c22-146">**string**</span></span>                                                                   | <span data-ttu-id="f4c22-147">指定電子郵件將傳送至其中的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f4c22-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="f4c22-148">備註</span><span class="sxs-lookup"><span data-stu-id="f4c22-148">Remarks</span></span>

<span data-ttu-id="f4c22-149">針對 c + + 開發，請參閱 [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) 介面。</span><span class="sxs-lookup"><span data-stu-id="f4c22-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="f4c22-150">如需腳本開發，請參閱 [**EmailAction**](emailaction.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f4c22-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="f4c22-151">**Windows 8 和 Windows Server 2012：** 已移除這個元素。</span><span class="sxs-lookup"><span data-stu-id="f4c22-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="f4c22-152">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。</span><span class="sxs-lookup"><span data-stu-id="f4c22-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="f4c22-153">範例</span><span class="sxs-lookup"><span data-stu-id="f4c22-153">Examples</span></span>

<span data-ttu-id="f4c22-154">如需指定電子郵件動作之工作的 XML 完整範例，請參閱 [事件觸發程式範例 (xml) ](/previous-versions//aa446889(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="f4c22-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c22-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4c22-155">Requirements</span></span>



| <span data-ttu-id="f4c22-156">需求</span><span class="sxs-lookup"><span data-stu-id="f4c22-156">Requirement</span></span> | <span data-ttu-id="f4c22-157">值</span><span class="sxs-lookup"><span data-stu-id="f4c22-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4c22-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4c22-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c22-159">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4c22-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4c22-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4c22-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c22-161">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4c22-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f4c22-162">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f4c22-162">End of client support</span></span><br/>    | <span data-ttu-id="f4c22-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4c22-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="f4c22-164">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f4c22-164">End of server support</span></span><br/>    | <span data-ttu-id="f4c22-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4c22-165">Windows Server 2008 R2</span></span><br/>                    |



 

