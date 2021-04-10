---
title: SystemPropertiesType 複雜類型
description: 定義識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- SystemPropertiesType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686213"
---
# <a name="systempropertiestype-complex-type"></a><span data-ttu-id="6ee2c-104">SystemPropertiesType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="6ee2c-104">SystemPropertiesType Complex Type</span></span>

<span data-ttu-id="6ee2c-105">定義識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-105">Defines the information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6ee2c-106">子元素</span><span class="sxs-lookup"><span data-stu-id="6ee2c-106">Child elements</span></span>



| <span data-ttu-id="6ee2c-107">元素</span><span class="sxs-lookup"><span data-stu-id="6ee2c-107">Element</span></span>                                                                         | <span data-ttu-id="6ee2c-108">類型</span><span class="sxs-lookup"><span data-stu-id="6ee2c-108">Type</span></span>                                                        | <span data-ttu-id="6ee2c-109">Description</span><span class="sxs-lookup"><span data-stu-id="6ee2c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ee2c-110">**通路**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-110">**Channel**</span></span>](eventschema-channel-systempropertiestype-element.md)             | <span data-ttu-id="6ee2c-111">anyURI</span><span class="sxs-lookup"><span data-stu-id="6ee2c-111">anyURI</span></span>                                                      | <span data-ttu-id="6ee2c-112">要記錄事件的通道。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-112">The channel to which the event was logged.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="6ee2c-113">**電腦**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-113">**Computer**</span></span>](eventschema-computer-systempropertiestype-element.md)           | <span data-ttu-id="6ee2c-114">字串</span><span class="sxs-lookup"><span data-stu-id="6ee2c-114">string</span></span>                                                      | <span data-ttu-id="6ee2c-115">發生事件之電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-115">The name of the computer on which the event occurred.</span></span><br/>                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="6ee2c-116">**相關**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-116">**Correlation**</span></span>](eventschema-correlation-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="6ee2c-117">取用者可用來將相關事件群組在一起的活動識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-117">The activity identifiers that consumers can use to group related events together.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="6ee2c-118">**EventID**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-118">**EventID**</span></span>](eventschema-eventid-systempropertiestype-element.md)             |                                                             | <span data-ttu-id="6ee2c-119">提供者用來識別事件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-119">The identifier that the provider used to identify the event.</span></span><br/>                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="6ee2c-120">**EventRecordID**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-120">**EventRecordID**</span></span>](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | <span data-ttu-id="6ee2c-121">記錄時指派給事件的記錄號碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-121">The record number assigned to the event when it was logged.</span></span><br/>                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="6ee2c-122">**執行**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-122">**Execution**</span></span>](eventschema-execution-systempropertiestype-element.md)         |                                                             | <span data-ttu-id="6ee2c-123">包含記錄事件之進程和執行緒的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-123">Contains information about the process and thread that logged the event.</span></span><br/>                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="6ee2c-124">**關鍵字**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-124">**Keywords**</span></span>](eventschema-keywords-systempropertiestype-element.md)           | [<span data-ttu-id="6ee2c-125">**HexInt64Type**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-125">**HexInt64Type**</span></span>](eventschema-hexint64type-simpletype.md) | <span data-ttu-id="6ee2c-126">事件中所定義關鍵字的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-126">A bitmask of the keywords defined in the event.</span></span> <span data-ttu-id="6ee2c-127">關鍵字是用來分類事件種類 (例如，與讀取資料) 相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-127">Keywords are used to classify types of events (for example, events associated with reading data).</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="6ee2c-128">**水準**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-128">**Level**</span></span>](eventschema-level-systempropertiestype-element.md)                 | <span data-ttu-id="6ee2c-129">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6ee2c-129">unsignedByte</span></span>                                                | <span data-ttu-id="6ee2c-130">事件中定義的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-130">The severity level defined in the event.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="6ee2c-131">**OpCode**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-131">**Opcode**</span></span>](eventschema-opcode-systempropertiestype-element.md)               | <span data-ttu-id="6ee2c-132">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6ee2c-132">unsignedByte</span></span>                                                | <span data-ttu-id="6ee2c-133">事件中定義的操作碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-133">The opcode defined in the event.</span></span> <span data-ttu-id="6ee2c-134">工作和 opcode 的 typcially 是用來識別應用程式中記錄事件的位置。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-134">Task and opcode are typcially used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="6ee2c-135">**提供者**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-135">**Provider**</span></span>](eventschema-provider-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="6ee2c-136">識別記錄事件的提供者。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-136">Identifies the provider that logged the event.</span></span> <span data-ttu-id="6ee2c-137">如果提供者使用檢測資訊清單來定義其事件，則會包含 **Name** 和 **Guid** 屬性;否則，如果舊版事件提供者 (使用 [事件記錄](/windows/desktop/EventLog/event-logging)API) 記錄事件，則會包含 **EventSourceName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-137">The **Name** and **Guid** attributes are included if the provider used an instrumentation manifest to define its events; otherwise, the **EventSourceName** attribute is included if a legacy event provider (using the [Event Logging](/windows/desktop/EventLog/event-logging) API) logged the event.</span></span><br/> |
| [<span data-ttu-id="6ee2c-138">**安全性**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-138">**Security**</span></span>](eventschema-security-systempropertiestype-element.md)           |                                                             | <span data-ttu-id="6ee2c-139">識別記錄事件的使用者。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-139">Identifies the user that logged the event.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="6ee2c-140">**Task**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-140">**Task**</span></span>](eventschema-task-systempropertiestype-element.md)                   | <span data-ttu-id="6ee2c-141">unsignedShort</span><span class="sxs-lookup"><span data-stu-id="6ee2c-141">unsignedShort</span></span>                                               | <span data-ttu-id="6ee2c-142">事件中定義的工作。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-142">The task defined in the event.</span></span> <span data-ttu-id="6ee2c-143">工作和 opcode 通常用來識別應用程式中記錄事件的位置。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-143">Task and opcode are typically used to identify the location in the application from where the event was logged.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="6ee2c-144">**TimeCreated**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-144">**TimeCreated**</span></span>](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | <span data-ttu-id="6ee2c-145">識別事件記錄時間的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-145">The time stamp that identifies when the event was logged.</span></span> <span data-ttu-id="6ee2c-146">時間戳記會包含 **SystemTime** 屬性或 **RawTime** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-146">The time stamp will include either the **SystemTime** attribute or the **RawTime** attribute.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="6ee2c-147">**版本**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-147">**Version**</span></span>](schema-version-systempropertiestype-element.md)                  | <span data-ttu-id="6ee2c-148">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6ee2c-148">unsignedByte</span></span>                                                | <span data-ttu-id="6ee2c-149">事件定義的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-149">The version number of the event's definition.</span></span><br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a><span data-ttu-id="6ee2c-150">屬性</span><span class="sxs-lookup"><span data-stu-id="6ee2c-150">Attributes</span></span>



| <span data-ttu-id="6ee2c-151">名稱</span><span class="sxs-lookup"><span data-stu-id="6ee2c-151">Name</span></span>              | <span data-ttu-id="6ee2c-152">類型</span><span class="sxs-lookup"><span data-stu-id="6ee2c-152">Type</span></span>                                                | <span data-ttu-id="6ee2c-153">Description</span><span class="sxs-lookup"><span data-stu-id="6ee2c-153">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee2c-154">ActivityID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-154">ActivityID</span></span>        | [<span data-ttu-id="6ee2c-155">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-155">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="6ee2c-156">識別目前活動的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-156">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="6ee2c-157">以此識別碼發佈的事件是相同活動的一部分。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-157">The events that are published with this identifier are part of the same activity.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="6ee2c-158">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="6ee2c-158">EventSourceName</span></span>   | <span data-ttu-id="6ee2c-159">字串</span><span class="sxs-lookup"><span data-stu-id="6ee2c-159">string</span></span>                                              | <span data-ttu-id="6ee2c-160">如果事件來源來自舊版 [事件記錄](/windows/desktop/EventLog/event-logging) API) ，則發佈事件 (事件來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-160">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/>                                                                                                                                                      |
| <span data-ttu-id="6ee2c-161">Guid</span><span class="sxs-lookup"><span data-stu-id="6ee2c-161">Guid</span></span>              | [<span data-ttu-id="6ee2c-162">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-162">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="6ee2c-163">可唯一識別提供者的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-163">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="6ee2c-164">KernelTime</span><span class="sxs-lookup"><span data-stu-id="6ee2c-164">KernelTime</span></span>        | <span data-ttu-id="6ee2c-165">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ee2c-165">unsignedInt</span></span>                                         | <span data-ttu-id="6ee2c-166">核心模式指令的已耗用執行時間，以 CPU 時間單位表示。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-166">Elapsed execution time for kernel-mode instructions, in CPU time units.</span></span> <span data-ttu-id="6ee2c-167">如果您使用的是 ETW 私用會話，請改用 ProcessorTime 成員中的值。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-167">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="6ee2c-168">僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-168">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                               |
| <span data-ttu-id="6ee2c-169">Name</span><span class="sxs-lookup"><span data-stu-id="6ee2c-169">Name</span></span>              | <span data-ttu-id="6ee2c-170">anyURI</span><span class="sxs-lookup"><span data-stu-id="6ee2c-170">anyURI</span></span>                                              | <span data-ttu-id="6ee2c-171">提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-171">The name of the provider.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6ee2c-172">ProcessID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-172">ProcessID</span></span>         | <span data-ttu-id="6ee2c-173">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ee2c-173">unsignedInt</span></span>                                         | <span data-ttu-id="6ee2c-174">識別已產生事件的處理序。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-174">Identifies the process that generated the event.</span></span><br/>                                                                                                                                                                                                                                             |
| <span data-ttu-id="6ee2c-175">ProcessorID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-175">ProcessorID</span></span>       | <span data-ttu-id="6ee2c-176">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="6ee2c-176">unsignedByte</span></span>                                        | <span data-ttu-id="6ee2c-177">處理事件之處理器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-177">The identification number for the processor that processed the event.</span></span> <span data-ttu-id="6ee2c-178">僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-178">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="6ee2c-179">ProcessorTime</span><span class="sxs-lookup"><span data-stu-id="6ee2c-179">ProcessorTime</span></span>     | <span data-ttu-id="6ee2c-180">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ee2c-180">unsignedInt</span></span>                                         | <span data-ttu-id="6ee2c-181">針對 ETW 私用會話，使用者模式指示的經過執行時間，以 CPU 滴答為單位。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-181">For ETW private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.</span></span> <span data-ttu-id="6ee2c-182">僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-182">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                    |
| <span data-ttu-id="6ee2c-183">限定詞</span><span class="sxs-lookup"><span data-stu-id="6ee2c-183">Qualifiers</span></span>        | <span data-ttu-id="6ee2c-184">**unsignedShort**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-184">**unsignedShort**</span></span>                                   | <span data-ttu-id="6ee2c-185">舊版提供者會使用32位的數位來識別其事件。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-185">A legacy provider uses a 32-bit number to identify its events.</span></span> <span data-ttu-id="6ee2c-186">如果舊版提供者記錄此事件， **EventID** 元素的值會包含事件識別碼的低序位16位，且 **限定詞** 屬性包含事件識別碼的高序位16位。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-186">If the event is logged by a legacy provider, the value of **EventID** element contains the low-order 16 bits of the event identifier and the **Qualifier** attribute contains the high-order 16 bits of the event identifier.</span></span><br/> |
| <span data-ttu-id="6ee2c-187">RawTime</span><span class="sxs-lookup"><span data-stu-id="6ee2c-187">RawTime</span></span>           | <span data-ttu-id="6ee2c-188">unsignedLong</span><span class="sxs-lookup"><span data-stu-id="6ee2c-188">unsignedLong</span></span>                                        | <span data-ttu-id="6ee2c-189">原始時間戳記值;時間戳記的格式取決於用來收集追蹤的時間來源。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-189">The raw time stamp value; the format of the time stamp depends on the time source used to collect the trace.</span></span> <span data-ttu-id="6ee2c-190">未經處理的時間戳記提供比系統時間更高的精確度。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-190">The raw time stamp offers higher precision than system time.</span></span> <span data-ttu-id="6ee2c-191">如果您搭配-rts 參數使用 TraceRpt.exe，轉譯的事件輸出只會包含原始時間。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-191">The rendered event output will only contain raw time if you use TraceRpt.exe with the -rts switch.</span></span><br/>                 |
| <span data-ttu-id="6ee2c-192">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-192">RelatedActivityID</span></span> | [<span data-ttu-id="6ee2c-193">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-193">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="6ee2c-194">全域唯一識別碼，用來識別要將控制項傳送至其中的活動。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-194">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="6ee2c-195">相關事件接著會有此識別碼作為其 ActivityID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-195">The related events would then have this identifier as their ActivityID identifier.</span></span><br/>                                                                                                            |
| <span data-ttu-id="6ee2c-196">SessionID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-196">SessionID</span></span>         | <span data-ttu-id="6ee2c-197">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ee2c-197">unsignedInt</span></span>                                         | <span data-ttu-id="6ee2c-198">發生事件之終端機伺服器工作階段的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-198">The identification number for the terminal server session in which the event occurred.</span></span> <span data-ttu-id="6ee2c-199">僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-199">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                                                                                            |
| <span data-ttu-id="6ee2c-200">SystemTime</span><span class="sxs-lookup"><span data-stu-id="6ee2c-200">SystemTime</span></span>        | <span data-ttu-id="6ee2c-201">dateTime</span><span class="sxs-lookup"><span data-stu-id="6ee2c-201">dateTime</span></span>                                            | <span data-ttu-id="6ee2c-202">記錄事件的系統時間。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-202">The system time of when the event was logged.</span></span><br/>                                                                                                                                                                                                                                                |
| <span data-ttu-id="6ee2c-203">ThreadID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-203">ThreadID</span></span>          | <span data-ttu-id="6ee2c-204">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ee2c-204">unsignedInt</span></span>                                         | <span data-ttu-id="6ee2c-205">識別已產生事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-205">Identifies the thread that generated the event.</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="6ee2c-206">UserID</span><span class="sxs-lookup"><span data-stu-id="6ee2c-206">UserID</span></span>            | <span data-ttu-id="6ee2c-207">字串</span><span class="sxs-lookup"><span data-stu-id="6ee2c-207">string</span></span>                                              | <span data-ttu-id="6ee2c-208">以字串形式 (SID) 使用者的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-208">The security identifier (SID) of the user in string form.</span></span><br/>                                                                                                                                                                                                                                    |
| <span data-ttu-id="6ee2c-209">UserTime</span><span class="sxs-lookup"><span data-stu-id="6ee2c-209">UserTime</span></span>          | <span data-ttu-id="6ee2c-210">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6ee2c-210">unsignedInt</span></span>                                         | <span data-ttu-id="6ee2c-211">使用者模式指示的經過執行時間，以 CPU 時間單位表示。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-211">Elapsed execution time for user-mode instructions, in CPU time units.</span></span> <span data-ttu-id="6ee2c-212">如果您使用的是 ETW 私用會話，請改用 ProcessorTime 成員中的值。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-212">If you are using an ETW private session, use the value in the ProcessorTime member instead.</span></span> <span data-ttu-id="6ee2c-213">僅適用于記錄至事件追蹤記錄檔的事件，)  ( etl 檔。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-213">Only available for events logged to an event tracing log file (.etl file).</span></span><br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="6ee2c-214">備註</span><span class="sxs-lookup"><span data-stu-id="6ee2c-214">Remarks</span></span>

<span data-ttu-id="6ee2c-215">根據預設，事件會包含電腦 (FQDN) 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-215">By default, the event contains the fully qualified domain name (FQDN) of a computer.</span></span> <span data-ttu-id="6ee2c-216">若要使用 NETBIOS 名稱而不是 FQDN，您必須在下列登錄機碼底下建立名為 CompatFlags 的 DWORD 登錄值，並將 CompatFlags 的值設定為0x2。</span><span class="sxs-lookup"><span data-stu-id="6ee2c-216">To use the NETBIOS name rather than the FQDN, you must create a DWORD registry value named CompatFlags under the following registry key, and set the value of CompatFlags to 0x2.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a><span data-ttu-id="6ee2c-217">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ee2c-217">Requirements</span></span>



| <span data-ttu-id="6ee2c-218">需求</span><span class="sxs-lookup"><span data-stu-id="6ee2c-218">Requirement</span></span> | <span data-ttu-id="6ee2c-219">值</span><span class="sxs-lookup"><span data-stu-id="6ee2c-219">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6ee2c-220">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ee2c-220">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee2c-221">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ee2c-221">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6ee2c-222">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ee2c-222">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee2c-223">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ee2c-223">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

