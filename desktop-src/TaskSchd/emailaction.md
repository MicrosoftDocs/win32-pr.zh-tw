---
title: EmailAction 物件
description: 代表傳送電子郵件訊息之動作的腳本物件。
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- EmailAction 物件工作排程器
- EmailAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844156"
---
# <a name="emailaction-object"></a><span data-ttu-id="cae54-105">EmailAction 物件</span><span class="sxs-lookup"><span data-stu-id="cae54-105">EmailAction object</span></span>

<span data-ttu-id="cae54-106">\[不再支援此物件。</span><span class="sxs-lookup"><span data-stu-id="cae54-106">\[This object is no longer supported.</span></span> <span data-ttu-id="cae54-107">請使用 IExecAction 搭配 powershell [**傳送 send-mailmessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) Cmdlet 作為因應措施。\]</span><span class="sxs-lookup"><span data-stu-id="cae54-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="cae54-108">代表傳送電子郵件訊息之動作的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="cae54-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="cae54-109">成員</span><span class="sxs-lookup"><span data-stu-id="cae54-109">Members</span></span>

<span data-ttu-id="cae54-110">**EmailAction** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cae54-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="cae54-111">屬性</span><span class="sxs-lookup"><span data-stu-id="cae54-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cae54-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cae54-112">Properties</span></span>

<span data-ttu-id="cae54-113">**EmailAction** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cae54-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="cae54-114">屬性</span><span class="sxs-lookup"><span data-stu-id="cae54-114">Property</span></span>                                                    | <span data-ttu-id="cae54-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="cae54-115">Access type</span></span>           | <span data-ttu-id="cae54-116">Description</span><span class="sxs-lookup"><span data-stu-id="cae54-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cae54-117">**附件**</span><span class="sxs-lookup"><span data-stu-id="cae54-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="cae54-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-118">Read/write</span></span><br/> | <span data-ttu-id="cae54-119">取得或設定與電子郵件訊息一起傳送的附件陣列。</span><span class="sxs-lookup"><span data-stu-id="cae54-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="cae54-120">**密件副本**</span><span class="sxs-lookup"><span data-stu-id="cae54-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="cae54-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-121">Read/write</span></span><br/> | <span data-ttu-id="cae54-122">取得或設定要在電子郵件訊息中密件副本的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cae54-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="cae54-123">**主體**</span><span class="sxs-lookup"><span data-stu-id="cae54-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="cae54-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-124">Read/write</span></span><br/> | <span data-ttu-id="cae54-125">取得或設定包含電子郵件訊息的電子郵件內文。</span><span class="sxs-lookup"><span data-stu-id="cae54-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="cae54-126">**Cc**</span><span class="sxs-lookup"><span data-stu-id="cae54-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="cae54-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-127">Read/write</span></span><br/> | <span data-ttu-id="cae54-128">取得或設定要在電子郵件訊息中抄送的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cae54-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="cae54-129">**寄件者**</span><span class="sxs-lookup"><span data-stu-id="cae54-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="cae54-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-130">Read/write</span></span><br/> | <span data-ttu-id="cae54-131">取得或設定要傳送電子郵件的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cae54-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="cae54-132">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="cae54-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="cae54-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-133">Read/write</span></span><br/> | <span data-ttu-id="cae54-134">取得或設定要傳送的電子郵件中的標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="cae54-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="cae54-135">**Id**</span><span class="sxs-lookup"><span data-stu-id="cae54-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="cae54-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-136">Read/write</span></span><br/> | <span data-ttu-id="cae54-137">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="cae54-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="cae54-138">取得或設定動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cae54-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="cae54-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="cae54-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="cae54-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-140">Read/write</span></span><br/> | <span data-ttu-id="cae54-141">取得或設定要回復的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cae54-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="cae54-142">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="cae54-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="cae54-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-143">Read/write</span></span><br/> | <span data-ttu-id="cae54-144">取得或設定用來傳送電子郵件的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cae54-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="cae54-145">**主體**</span><span class="sxs-lookup"><span data-stu-id="cae54-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="cae54-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-146">Read/write</span></span><br/> | <span data-ttu-id="cae54-147">取得或設定電子郵件訊息的主旨。</span><span class="sxs-lookup"><span data-stu-id="cae54-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="cae54-148">**自**</span><span class="sxs-lookup"><span data-stu-id="cae54-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="cae54-149">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cae54-149">Read/write</span></span><br/> | <span data-ttu-id="cae54-150">取得或設定要傳送電子郵件的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="cae54-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="cae54-151">**類型**</span><span class="sxs-lookup"><span data-stu-id="cae54-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="cae54-152">唯讀</span><span class="sxs-lookup"><span data-stu-id="cae54-152">Read-only</span></span><br/>  | <span data-ttu-id="cae54-153">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="cae54-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="cae54-154">取得動作的類型。</span><span class="sxs-lookup"><span data-stu-id="cae54-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="cae54-155">備註</span><span class="sxs-lookup"><span data-stu-id="cae54-155">Remarks</span></span>

<span data-ttu-id="cae54-156">電子郵件動作必須具有 [[**伺服器**](emailaction-server.md)]、[[**寄件者**](emailaction-from.md)]、[收件者] 或 [副本 [**] 屬性的**](emailaction-cc.md)有效值 [**，才能讓**](emailaction-to.md)工作正確註冊並執行。</span><span class="sxs-lookup"><span data-stu-id="cae54-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="cae54-157">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) 元素來指定電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="cae54-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="cae54-158">範例</span><span class="sxs-lookup"><span data-stu-id="cae54-158">Examples</span></span>

<span data-ttu-id="cae54-159">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [事件觸發程式範例 (腳本) ](/previous-versions//aa446887(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cae54-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="cae54-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="cae54-160">Requirements</span></span>



| <span data-ttu-id="cae54-161">需求</span><span class="sxs-lookup"><span data-stu-id="cae54-161">Requirement</span></span> | <span data-ttu-id="cae54-162">值</span><span class="sxs-lookup"><span data-stu-id="cae54-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cae54-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cae54-163">Minimum supported client</span></span><br/> | <span data-ttu-id="cae54-164">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cae54-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cae54-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cae54-165">Minimum supported server</span></span><br/> | <span data-ttu-id="cae54-166">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cae54-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cae54-167">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cae54-167">End of client support</span></span><br/>    | <span data-ttu-id="cae54-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cae54-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="cae54-169">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cae54-169">End of server support</span></span><br/>    | <span data-ttu-id="cae54-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cae54-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="cae54-171">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="cae54-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="cae54-172"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cae54-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cae54-173">DLL</span><span class="sxs-lookup"><span data-stu-id="cae54-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae54-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae54-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

