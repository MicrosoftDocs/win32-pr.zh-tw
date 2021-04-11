---
description: NTEventLogEventConsumer 類別會在事件傳遞給它時，將特定訊息記錄到作業系統事件記錄檔中。
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: NTEventLogEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848393"
---
# <a name="nteventlogeventconsumer-class"></a><span data-ttu-id="088bd-103">NTEventLogEventConsumer 類別</span><span class="sxs-lookup"><span data-stu-id="088bd-103">NTEventLogEventConsumer class</span></span>

<span data-ttu-id="088bd-104">**NTEventLogEventConsumer** 類別會在事件傳遞給它時，將特定訊息記錄到作業系統事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="088bd-104">The **NTEventLogEventConsumer** class logs a specific message to the operating system event log when an event is delivered to it.</span></span> <span data-ttu-id="088bd-105">此類別是 WMI 提供的其中一個標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="088bd-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="088bd-106">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="088bd-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="088bd-107">語法</span><span class="sxs-lookup"><span data-stu-id="088bd-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a><span data-ttu-id="088bd-108">成員</span><span class="sxs-lookup"><span data-stu-id="088bd-108">Members</span></span>

<span data-ttu-id="088bd-109">**NTEventLogEventConsumer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="088bd-109">The **NTEventLogEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="088bd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="088bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="088bd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="088bd-111">Properties</span></span>

<span data-ttu-id="088bd-112">**NTEventLogEventConsumer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="088bd-112">The **NTEventLogEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="088bd-113">**類別**</span><span class="sxs-lookup"><span data-stu-id="088bd-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="088bd-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-116">事件類別目錄。</span><span class="sxs-lookup"><span data-stu-id="088bd-116">Event category.</span></span> <span data-ttu-id="088bd-117">這是來源特定的資訊，而且可以具有任何值。</span><span class="sxs-lookup"><span data-stu-id="088bd-117">This is source-specific information and can have any value.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-118">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="088bd-118">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-119">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="088bd-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="088bd-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-121">安全識別碼 (SID) ，可唯一識別建立篩選的使用者。</span><span class="sxs-lookup"><span data-stu-id="088bd-121">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="088bd-122">根據作業系統而定，WMI 會儲存建立 [**\_ \_ EventConsumer**](--eventconsumer.md)實例或系統管理員 SID 之使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="088bd-122">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="088bd-123">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="088bd-123">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="088bd-124">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="088bd-124">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="088bd-125">**EventID**</span><span class="sxs-lookup"><span data-stu-id="088bd-125">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="088bd-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-128">訊息 DLL 中的事件訊息。</span><span class="sxs-lookup"><span data-stu-id="088bd-128">Event message in the message DLL.</span></span> <span data-ttu-id="088bd-129">這個屬性不能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="088bd-129">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-130">**EventType**</span><span class="sxs-lookup"><span data-stu-id="088bd-130">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="088bd-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-133">事件的類型。</span><span class="sxs-lookup"><span data-stu-id="088bd-133">Type of event.</span></span> <span data-ttu-id="088bd-134">這個參數可以有下列清單中所列的其中一個值，這些值定義于 Winnt 中。</span><span class="sxs-lookup"><span data-stu-id="088bd-134">This parameter can have one of the values listed in the following list, which are defined in Winnt.h.</span></span>

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span data-ttu-id="088bd-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG \_SUCCESS** (0 (0x0) ) </span><span class="sxs-lookup"><span data-stu-id="088bd-135"><span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**EVENTLOG\_SUCCESS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="088bd-136">成功的事件</span><span class="sxs-lookup"><span data-stu-id="088bd-136">Successful event</span></span>

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span data-ttu-id="088bd-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG \_\_TPYE** (1 (0X1) ) 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="088bd-137"><span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**EVENTLOG\_ERROR\_TPYE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="088bd-138">錯誤事件</span><span class="sxs-lookup"><span data-stu-id="088bd-138">Error event</span></span>

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span data-ttu-id="088bd-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG \_警告 \_ 類型** (2 (0x2) ) </span><span class="sxs-lookup"><span data-stu-id="088bd-139"><span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**EVENTLOG\_WARNING\_TYPE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="088bd-140">警告事件</span><span class="sxs-lookup"><span data-stu-id="088bd-140">Warning event</span></span>

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span data-ttu-id="088bd-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG \_資訊 \_ 類型** (4 (0x4) ) </span><span class="sxs-lookup"><span data-stu-id="088bd-141"><span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**EVENTLOG\_INFORMATION\_TYPE** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="088bd-142">資訊事件</span><span class="sxs-lookup"><span data-stu-id="088bd-142">Information event</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span data-ttu-id="088bd-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG \_AUDIT \_ SUCCESS** (8 (0x8) ) </span><span class="sxs-lookup"><span data-stu-id="088bd-143"><span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**EVENTLOG\_AUDIT\_SUCCESS** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="088bd-144">成功審核類型</span><span class="sxs-lookup"><span data-stu-id="088bd-144">Success audit type</span></span>

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span data-ttu-id="088bd-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG \_AUDIT \_ 失敗** (16 (0x10) ) </span><span class="sxs-lookup"><span data-stu-id="088bd-145"><span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**EVENTLOG\_AUDIT\_FAILURE** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="088bd-146">失敗審核類型</span><span class="sxs-lookup"><span data-stu-id="088bd-146">Failure audit type</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="088bd-147">**InsertionStringTemplates**</span><span class="sxs-lookup"><span data-stu-id="088bd-147">**InsertionStringTemplates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-148">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="088bd-148">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="088bd-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-150">標準字串範本的陣列，用來做為事件記錄檔記錄的插入字串。</span><span class="sxs-lookup"><span data-stu-id="088bd-150">Array of standard string templates that is used as the insertion string for an event log record.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-151">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="088bd-151">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="088bd-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-154">Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="088bd-154">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="088bd-155">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="088bd-155">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="088bd-156">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="088bd-156">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="088bd-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-159">特定取用者的佇列上限，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="088bd-159">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="088bd-160">這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="088bd-160">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="088bd-161">**名稱**</span><span class="sxs-lookup"><span data-stu-id="088bd-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="088bd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="088bd-164">限定詞：索引 [**鍵**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="088bd-164">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="088bd-165">取用者的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="088bd-165">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-166">**NameOfRawDataProperty**</span><span class="sxs-lookup"><span data-stu-id="088bd-166">**NameOfRawDataProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="088bd-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-169">事件屬性的名稱，其中包含要傳遞給 [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) 函數 *lpRawData* 參數的資料。</span><span class="sxs-lookup"><span data-stu-id="088bd-169">Name of the event property that contains data to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpRawData* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-170">**NameOfUserSidProperty**</span><span class="sxs-lookup"><span data-stu-id="088bd-170">**NameOfUserSidProperty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="088bd-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-173">事件屬性的名稱，其中包含要傳遞至 [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) 函式 *LPUSERSID* 參數 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="088bd-173">Name of the event property that contains a security identifier (SID) to be passed to the [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) function *lpUserSid* parameter.</span></span> <span data-ttu-id="088bd-174">屬性必須是位元組陣列 (**uint8**) 或字串。</span><span class="sxs-lookup"><span data-stu-id="088bd-174">The property must be either an array of bytes (**uint8**) or a string.</span></span> <span data-ttu-id="088bd-175">如果是位元組陣列，則會假設為 SID。</span><span class="sxs-lookup"><span data-stu-id="088bd-175">If it is an array of bytes, it is assumed to be a SID.</span></span> <span data-ttu-id="088bd-176">如果是字串，它就是轉換成 SID 的字串 SID。</span><span class="sxs-lookup"><span data-stu-id="088bd-176">If it is a string, it is a string SID that is converted into a SID.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-177">**NumberOfInsertionStrings**</span><span class="sxs-lookup"><span data-stu-id="088bd-177">**NumberOfInsertionStrings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-178">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="088bd-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-180">**InsertionStringTemplates** 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="088bd-180">Number of elements in the **InsertionStringTemplates** array.</span></span>

</dd> <dt>

<span data-ttu-id="088bd-181">**SourceName**</span><span class="sxs-lookup"><span data-stu-id="088bd-181">**SourceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="088bd-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-184">訊息所在的來源名稱。</span><span class="sxs-lookup"><span data-stu-id="088bd-184">Source name where a message is located.</span></span> <span data-ttu-id="088bd-185">假設客戶已使用必要的訊息註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="088bd-185">The customer is assumed to have registered a DLL with the necessary messages.</span></span>

> [!Note]  
> <span data-ttu-id="088bd-186">此參數的值不能包含冒號 (： ) 字元。</span><span class="sxs-lookup"><span data-stu-id="088bd-186">The value of this parameter must not include a colon (:) character.</span></span>

 

</dd> <dt>

<span data-ttu-id="088bd-187">**UNCServerName**</span><span class="sxs-lookup"><span data-stu-id="088bd-187">**UNCServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="088bd-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="088bd-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="088bd-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="088bd-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="088bd-190">要記錄事件的電腦名稱稱，如果事件是在本機伺服器上登入，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="088bd-190">Name of the computer on which to log an event, or **NULL** if the event is to be logged on a local server.</span></span>

<span data-ttu-id="088bd-191">依預設，已驗證的使用者不能將事件記錄到遠端電腦上的應用程式記錄檔。</span><span class="sxs-lookup"><span data-stu-id="088bd-191">Authenticated users cannot, by default, log events to the Application log on a remote computer.</span></span> <span data-ttu-id="088bd-192">因此，使用此屬性指定遠端電腦將無法運作。</span><span class="sxs-lookup"><span data-stu-id="088bd-192">As a result, using this property to specify a remote computer will not work.</span></span> <span data-ttu-id="088bd-193">若要瞭解如何變更事件記錄檔安全性，請參閱這 [篇知識庫文章](https://support.microsoft.com/kb/323076)。</span><span class="sxs-lookup"><span data-stu-id="088bd-193">To learn how to change event log security, consult this [KB article](https://support.microsoft.com/kb/323076).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="088bd-194">備註</span><span class="sxs-lookup"><span data-stu-id="088bd-194">Remarks</span></span>

<span data-ttu-id="088bd-195">**NTEventLogEventConsumer** 類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。</span><span class="sxs-lookup"><span data-stu-id="088bd-195">The **NTEventLogEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

## <a name="examples"></a><span data-ttu-id="088bd-196">範例</span><span class="sxs-lookup"><span data-stu-id="088bd-196">Examples</span></span>

<span data-ttu-id="088bd-197">如需使用 **NTEventLogEventConsumer** 來建立取用者的範例，請參閱 [根據事件記錄至 NT 事件記錄](logging-to-nt-event-log-based-on-an-event.md)檔。</span><span class="sxs-lookup"><span data-stu-id="088bd-197">For an example of using **NTEventLogEventConsumer** to create a consumer, see [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="088bd-198">規格需求</span><span class="sxs-lookup"><span data-stu-id="088bd-198">Requirements</span></span>



| <span data-ttu-id="088bd-199">需求</span><span class="sxs-lookup"><span data-stu-id="088bd-199">Requirement</span></span> | <span data-ttu-id="088bd-200">值</span><span class="sxs-lookup"><span data-stu-id="088bd-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="088bd-201">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="088bd-201">Minimum supported client</span></span><br/> | <span data-ttu-id="088bd-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="088bd-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="088bd-203">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="088bd-203">Minimum supported server</span></span><br/> | <span data-ttu-id="088bd-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="088bd-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="088bd-205">命名空間</span><span class="sxs-lookup"><span data-stu-id="088bd-205">Namespace</span></span><br/>                | <span data-ttu-id="088bd-206">根 \\ 訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="088bd-206">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="088bd-207">MOF</span><span class="sxs-lookup"><span data-stu-id="088bd-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="088bd-208"><dt>Wbemcons mof</dt></span><span class="sxs-lookup"><span data-stu-id="088bd-208"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="088bd-209">DLL</span><span class="sxs-lookup"><span data-stu-id="088bd-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="088bd-210"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088bd-210"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088bd-211">另請參閱</span><span class="sxs-lookup"><span data-stu-id="088bd-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088bd-212">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="088bd-212">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="088bd-213">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="088bd-213">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="088bd-214">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="088bd-214">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="088bd-215">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="088bd-215">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

