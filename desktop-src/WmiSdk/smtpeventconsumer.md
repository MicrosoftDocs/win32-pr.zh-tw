---
description: SMTPEventConsumer 類別會在每次傳遞事件給它時，使用 Simple Mail Transfer Protocol (SMTP) 傳送電子郵件訊息。
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: SMTPEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195050"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="d045b-103">SMTPEventConsumer 類別</span><span class="sxs-lookup"><span data-stu-id="d045b-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="d045b-104">**SMTPEventConsumer** 類別會在每次傳遞事件給它時，使用 Simple Mail Transfer PROTOCOL (SMTP) 傳送電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="d045b-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="d045b-105">SMTP 伺服器必須存在於網路上。</span><span class="sxs-lookup"><span data-stu-id="d045b-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="d045b-106">SMTPEventConsumer 類別不支援附件。</span><span class="sxs-lookup"><span data-stu-id="d045b-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="d045b-107">電子郵件訊息的編碼必須是美國-ASCII。</span><span class="sxs-lookup"><span data-stu-id="d045b-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="d045b-108">此類別是 WMI 提供的其中一個標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="d045b-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="d045b-109">如需使用 **SMTPEventConsumer** 來建立取用者的範例，請參閱 [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="d045b-110">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="d045b-111">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d045b-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d045b-112">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="d045b-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d045b-113">語法</span><span class="sxs-lookup"><span data-stu-id="d045b-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="d045b-114">成員</span><span class="sxs-lookup"><span data-stu-id="d045b-114">Members</span></span>

<span data-ttu-id="d045b-115">**SMTPEventConsumer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d045b-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="d045b-116">屬性</span><span class="sxs-lookup"><span data-stu-id="d045b-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d045b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="d045b-117">Properties</span></span>

<span data-ttu-id="d045b-118">**SMTPEventConsumer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d045b-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d045b-119">**BccLine**</span><span class="sxs-lookup"><span data-stu-id="d045b-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-122">地址清單（以逗號或分號分隔），格式為要將訊息當作密件副本傳送的標準字串範本格式。</span><span class="sxs-lookup"><span data-stu-id="d045b-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="d045b-123">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="d045b-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-124">**CcLine**</span><span class="sxs-lookup"><span data-stu-id="d045b-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-127">地址清單（以逗號或分號分隔），採用標準字串範本的格式，訊息會以副本的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d045b-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="d045b-128">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="d045b-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-129">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="d045b-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-130">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="d045b-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d045b-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-132">安全識別碼 (SID) ，可唯一識別建立篩選的使用者。</span><span class="sxs-lookup"><span data-stu-id="d045b-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="d045b-133">根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="d045b-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="d045b-134">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="d045b-135">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d045b-136">**FromLine**</span><span class="sxs-lookup"><span data-stu-id="d045b-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-139">從電子郵件訊息的行，以標準字串範本的格式。</span><span class="sxs-lookup"><span data-stu-id="d045b-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="d045b-140">如果是 **Null**，就會以 "WinMgmt@*MachineName*" 的形式來構成 From 行。</span><span class="sxs-lookup"><span data-stu-id="d045b-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="d045b-141">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="d045b-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-142">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d045b-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d045b-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-144">插入電子郵件訊息的標頭欄位陣列，不含解讀。</span><span class="sxs-lookup"><span data-stu-id="d045b-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="d045b-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-148">Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="d045b-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="d045b-149">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d045b-150">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="d045b-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d045b-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-153">特定取用者的佇列上限，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="d045b-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="d045b-154">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d045b-155">**訊息**</span><span class="sxs-lookup"><span data-stu-id="d045b-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-158">包含電子郵件訊息主體的標準字串範本。</span><span class="sxs-lookup"><span data-stu-id="d045b-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-159">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d045b-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d045b-162">限定詞：索引 [**鍵**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d045b-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="d045b-163">事件取用者的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d045b-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-164">**ReplyToLine**</span><span class="sxs-lookup"><span data-stu-id="d045b-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-167">電子郵件訊息的回復行，格式為標準字串範本。</span><span class="sxs-lookup"><span data-stu-id="d045b-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="d045b-168">如果是 **Null**，則不會使用回復行。</span><span class="sxs-lookup"><span data-stu-id="d045b-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="d045b-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-172">傳送電子郵件的 SMTP 伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d045b-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="d045b-173">允許的名稱為 IP 位址或 DNS 或 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="d045b-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="d045b-174">這個屬性不能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d045b-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-175">**主旨**</span><span class="sxs-lookup"><span data-stu-id="d045b-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-178">標準字串範本，包含電子郵件訊息的主旨。</span><span class="sxs-lookup"><span data-stu-id="d045b-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="d045b-179">**ToLine**</span><span class="sxs-lookup"><span data-stu-id="d045b-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d045b-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d045b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d045b-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d045b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d045b-182">地址清單（以逗號或分號分隔），格式為識別要傳送訊息之位置的標準字串範本格式。</span><span class="sxs-lookup"><span data-stu-id="d045b-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="d045b-183">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="d045b-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d045b-184">備註</span><span class="sxs-lookup"><span data-stu-id="d045b-184">Remarks</span></span>

<span data-ttu-id="d045b-185">SMTPEventConsumer 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。</span><span class="sxs-lookup"><span data-stu-id="d045b-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="d045b-186">某些 **ToLine**、 **CcLine** 或 **BccLine** 屬性可以是 **Null**，但不能全部為 **null**。</span><span class="sxs-lookup"><span data-stu-id="d045b-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="d045b-187">從 SMTP 服務收到錯誤傳回碼會視為失敗。</span><span class="sxs-lookup"><span data-stu-id="d045b-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="d045b-188">範例</span><span class="sxs-lookup"><span data-stu-id="d045b-188">Examples</span></span>

<span data-ttu-id="d045b-189">如需使用 **SMTPEventConsumer** 來建立取用者的範例，請參閱 [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="d045b-190">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="d045b-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d045b-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="d045b-191">Requirements</span></span>



| <span data-ttu-id="d045b-192">需求</span><span class="sxs-lookup"><span data-stu-id="d045b-192">Requirement</span></span> | <span data-ttu-id="d045b-193">值</span><span class="sxs-lookup"><span data-stu-id="d045b-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d045b-194">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d045b-194">Minimum supported client</span></span><br/> | <span data-ttu-id="d045b-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d045b-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d045b-196">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d045b-196">Minimum supported server</span></span><br/> | <span data-ttu-id="d045b-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d045b-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d045b-198">命名空間</span><span class="sxs-lookup"><span data-stu-id="d045b-198">Namespace</span></span><br/>                | <span data-ttu-id="d045b-199">根 \\ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="d045b-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="d045b-200">MOF</span><span class="sxs-lookup"><span data-stu-id="d045b-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d045b-201"><dt>Smtpcons mof</dt></span><span class="sxs-lookup"><span data-stu-id="d045b-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="d045b-202">DLL</span><span class="sxs-lookup"><span data-stu-id="d045b-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d045b-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d045b-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d045b-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d045b-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d045b-205">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="d045b-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="d045b-206">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="d045b-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="d045b-207">根據事件傳送電子郵件</span><span class="sxs-lookup"><span data-stu-id="d045b-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="d045b-208">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="d045b-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="d045b-209">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="d045b-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 




