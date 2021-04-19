---
title: ChannelPublishingType 複雜類型
description: 為通道所使用的會話定義記錄屬性。 |ChannelPublishingType 複雜類型
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- ChannelPublishingType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997231"
---
# <a name="channelpublishingtype-complex-type"></a><span data-ttu-id="57d08-105">ChannelPublishingType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="57d08-105">ChannelPublishingType Complex Type</span></span>

<span data-ttu-id="57d08-106">為通道所使用的會話定義記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="57d08-106">Defines the logging properties for the session that the channel uses.</span></span>

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
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

## <a name="child-elements"></a><span data-ttu-id="57d08-107">子元素</span><span class="sxs-lookup"><span data-stu-id="57d08-107">Child elements</span></span>



| <span data-ttu-id="57d08-108">元素</span><span class="sxs-lookup"><span data-stu-id="57d08-108">Element</span></span>                                                                              | <span data-ttu-id="57d08-109">類型</span><span class="sxs-lookup"><span data-stu-id="57d08-109">Type</span></span>                                                              | <span data-ttu-id="57d08-110">Description</span><span class="sxs-lookup"><span data-stu-id="57d08-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57d08-111">**bufferSize**</span><span class="sxs-lookup"><span data-stu-id="57d08-111">**bufferSize**</span></span>](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [<span data-ttu-id="57d08-112">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-112">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="57d08-113">針對每個緩衝區配置的記憶體數量（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="57d08-113">The amount of memory, in kilobytes, to allocate for each buffer.</span></span> <span data-ttu-id="57d08-114">如果您預期較低的事件速率，緩衝區大小應該設定為記憶體頁面大小。</span><span class="sxs-lookup"><span data-stu-id="57d08-114">If you expect a relatively low event rate, the buffer size should be set to the memory page size.</span></span> <span data-ttu-id="57d08-115">如果事件速率預期會相當高，您應該指定較大的緩衝區大小並增加緩衝區的最大數目。</span><span class="sxs-lookup"><span data-stu-id="57d08-115">If the event rate is expected to be relatively high, you should specify a larger buffer size and increase the maximum number of buffers.</span></span><br/> <span data-ttu-id="57d08-116">緩衝區大小會影響緩衝區填滿和必須排清的速率。</span><span class="sxs-lookup"><span data-stu-id="57d08-116">The buffer size affects the rate at which buffers fill and must be flushed.</span></span> <span data-ttu-id="57d08-117">雖然小型緩衝區大小需要較少的記憶體，但它會增加緩衝區必須排清的速率。</span><span class="sxs-lookup"><span data-stu-id="57d08-117">Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed.</span></span><br/> <span data-ttu-id="57d08-118">分析和偵測通道的預設緩衝區大小為 4 KB，而系統管理員和運作方式為 64 KB。</span><span class="sxs-lookup"><span data-stu-id="57d08-118">The default buffer size for Analytic and Debug channels is 4 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="57d08-119">**clockType**</span><span class="sxs-lookup"><span data-stu-id="57d08-119">**clockType**</span></span>](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | <span data-ttu-id="57d08-120">記錄每個事件的時間戳記時，所要使用的時鐘解析。</span><span class="sxs-lookup"><span data-stu-id="57d08-120">The clock resolution to use when logging the time stamp for each event.</span></span> <span data-ttu-id="57d08-121">您可以指定 SystemTime 或 QPC。</span><span class="sxs-lookup"><span data-stu-id="57d08-121">You can specify SystemTime or QPC.</span></span> <span data-ttu-id="57d08-122">SystemTime 提供低解析度 (10 毫秒) 時間戳記，但要取得的成本相對較低。</span><span class="sxs-lookup"><span data-stu-id="57d08-122">SystemTime provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve.</span></span> <span data-ttu-id="57d08-123">預設值為 SystemTime。</span><span class="sxs-lookup"><span data-stu-id="57d08-123">The default is SystemTime.</span></span> <br/> <span data-ttu-id="57d08-124">Query 效能計數器 (QPC) 提供高解析度的 (100 納秒) 時間戳記，但耗用的成本會相對較高。</span><span class="sxs-lookup"><span data-stu-id="57d08-124">Query performance counter (QPC) provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve.</span></span> <span data-ttu-id="57d08-125">如果您有高事件率，或取用者合併來自不同緩衝區的事件，您應該 QPC。</span><span class="sxs-lookup"><span data-stu-id="57d08-125">You should QPC if you have high event rates or if the consumer merges events from different buffers.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="57d08-126">**controlGuid**</span><span class="sxs-lookup"><span data-stu-id="57d08-126">**controlGuid**</span></span>](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [<span data-ttu-id="57d08-127">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="57d08-127">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="57d08-128">識別包含 WPP 事件之 ETW 會話的會話 GUID。</span><span class="sxs-lookup"><span data-stu-id="57d08-128">Identifies the session GUID for an ETW session that contains WPP events.</span></span> <span data-ttu-id="57d08-129">這項設定只允許用於 Debug 類型的通道。</span><span class="sxs-lookup"><span data-stu-id="57d08-129">This setting is only allowed for channels of type Debug.</span></span> <span data-ttu-id="57d08-130">這些通道無法完全啟用，關鍵字設定為零 (0x0000000000000000) 。</span><span class="sxs-lookup"><span data-stu-id="57d08-130">These channels cannot be fully enabled with keywords set to zero (0x0000000000000000).</span></span> <span data-ttu-id="57d08-131">它們必須啟用，並將關鍵字設為0xffffffffffffffff。</span><span class="sxs-lookup"><span data-stu-id="57d08-131">They must be enabled with keywords set to 0xffffffffffffffff.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="57d08-132">**fileMax**</span><span class="sxs-lookup"><span data-stu-id="57d08-132">**fileMax**</span></span>                                                                          | [<span data-ttu-id="57d08-133">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-133">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="57d08-134">啟用通道時，您要讓服務建立新記錄檔的最大次數 (包括重新開機電腦) 。</span><span class="sxs-lookup"><span data-stu-id="57d08-134">The maximum number of times that you want the service to create a new log file when the channel is enabled (includes when the computer is restarted).</span></span> <span data-ttu-id="57d08-135">如果值為0或1，則服務會在每次啟用通道時覆寫記錄檔，而且會遺失先前的事件。</span><span class="sxs-lookup"><span data-stu-id="57d08-135">If the value is 0 or 1, the service will overwrite the log file each time the channel is enabled and the previous events will be lost.</span></span> <span data-ttu-id="57d08-136">如果值大於1，則服務會在每次啟用通道時建立新的記錄檔，以便保留事件。</span><span class="sxs-lookup"><span data-stu-id="57d08-136">If the value is greater than 1, the service will create a new log file each time the channel is enabled in order to preserve the events.</span></span> <span data-ttu-id="57d08-137">預設值為1，而且您可以指定的最大值為16。</span><span class="sxs-lookup"><span data-stu-id="57d08-137">The default is 1 and the maximum that you can specify is 16.</span></span><br/> <span data-ttu-id="57d08-138">服務會將三位數的十進位數附加至每個檔案名，介於0和 fileMax 1 之間。</span><span class="sxs-lookup"><span data-stu-id="57d08-138">The service appends a three digit decimal number between 0 and fileMax 1 to each file name.</span></span> <span data-ttu-id="57d08-139">例如，etl.xxx，其中 xxx 是三位數的十進位 *數。*</span><span class="sxs-lookup"><span data-stu-id="57d08-139">For example, *filename*.etl.xxx, where xxx is the three digit decimal number.</span></span> <span data-ttu-id="57d08-140">這些檔案位於% windir% \\ System32 \\ \system32\winevt\logs\application.evtx 記錄檔中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="57d08-140">The files are located in %windir%\\System32\\winevt\\Logs.</span></span><br/> |
| [<span data-ttu-id="57d08-141">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="57d08-141">**keywords**</span></span>](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [<span data-ttu-id="57d08-142">**UInt64Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-142">**UInt64Type**</span></span>](eventmanifestschema-hexint64type-simpletype.md) | <span data-ttu-id="57d08-143">位元遮罩，可決定寫入通道的事件分類。</span><span class="sxs-lookup"><span data-stu-id="57d08-143">A bitmask that determines the category of events that are written to the channel.</span></span> <span data-ttu-id="57d08-144">如果 **關鍵字** 屬性的值為0，則提供者寫入的所有事件都會寫入至通道;否則，只有定義了 **關鍵字** 位元遮罩之關鍵字的事件會寫入至通道。</span><span class="sxs-lookup"><span data-stu-id="57d08-144">If the value of **keywords** attribute is 0, all events that the provider writes are written to the channel; otherwise only events that have defined a keyword that is included in the **keywords** bitmask are written to the channel.</span></span> <span data-ttu-id="57d08-145">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="57d08-145">The default is 0.</span></span><br/> <span data-ttu-id="57d08-146">具有 controlGuid 屬性集的 Debug 通道必須將 **關鍵字** 屬性設定為0xFFFFFFFFFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="57d08-146">Debug channels that have the controlGuid attribute set must set the **keywords** attribute to 0xFFFFFFFFFFFFFFFF.</span></span><br/> <span data-ttu-id="57d08-147">會話啟用提供者時，會將關鍵字值傳遞給提供者。</span><span class="sxs-lookup"><span data-stu-id="57d08-147">The session passes the keywords value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="57d08-148">**延遲**</span><span class="sxs-lookup"><span data-stu-id="57d08-148">**latency**</span></span>](eventmanifestschema-latency-channelpublishingtype-element.md)         | [<span data-ttu-id="57d08-149">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-149">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="57d08-150">清除緩衝區之前等候的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="57d08-150">The time to wait before flushing the buffers, in milliseconds.</span></span> <span data-ttu-id="57d08-151">如果為零，ETW 會在緩衝區填滿時立即將其清除。</span><span class="sxs-lookup"><span data-stu-id="57d08-151">If zero, ETW flushes the buffers as soon as they become full.</span></span> <span data-ttu-id="57d08-152">如果是非零值，ETW 會根據值（即使緩衝區未滿）來排清包含事件的所有緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57d08-152">If nonzero, ETW flushes all buffers that contain events based on the value even if the buffer is not full.</span></span> <span data-ttu-id="57d08-153">一般來說，您只想要在緩衝區填滿時排清緩衝區。</span><span class="sxs-lookup"><span data-stu-id="57d08-153">Typically, you want to flush buffers only when they become full.</span></span> <span data-ttu-id="57d08-154">強制緩衝區排清可以增加具有未填滿緩衝區空間的記錄檔大小。</span><span class="sxs-lookup"><span data-stu-id="57d08-154">Forcing the buffers to flush can increase the file size of the log file with unfilled buffer space.</span></span> <span data-ttu-id="57d08-155">系統管理員和作業記錄的預設值為1秒，分析和偵錯工具記錄檔的預設值為5秒。</span><span class="sxs-lookup"><span data-stu-id="57d08-155">The default value is 1 second for Admin and Operational logs and 5 seconds for Analytic and Debug logs.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="57d08-156">**等級**</span><span class="sxs-lookup"><span data-stu-id="57d08-156">**level**</span></span>](eventmanifestschema-level-channelpublishingtype-element.md)             | [<span data-ttu-id="57d08-157">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-157">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="57d08-158">要寫入通道之事件的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="57d08-158">The severity level of the events to write to the channel.</span></span> <span data-ttu-id="57d08-159">服務會將事件寫入至層級值小於或等於指定值的通道。</span><span class="sxs-lookup"><span data-stu-id="57d08-159">The service writes events to the channel that have a level value that is less than or equal to the specified value.</span></span> <span data-ttu-id="57d08-160">預設值為0，這表示要記錄具有任何層級值的事件。</span><span class="sxs-lookup"><span data-stu-id="57d08-160">The default is 0, which means to log events with any level value.</span></span><br/> <span data-ttu-id="57d08-161">會話啟用提供者時，會將層級值傳遞給提供者。</span><span class="sxs-lookup"><span data-stu-id="57d08-161">The session passes the level value to the provider when it enables the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="57d08-162">**maxBuffers**</span><span class="sxs-lookup"><span data-stu-id="57d08-162">**maxBuffers**</span></span>](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="57d08-163">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-163">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="57d08-164">要配置給會話的緩衝區數目上限。</span><span class="sxs-lookup"><span data-stu-id="57d08-164">The maximum number of buffers to allocate for the session.</span></span> <span data-ttu-id="57d08-165">一般來說，此值是緩衝區數目下限加上二十。</span><span class="sxs-lookup"><span data-stu-id="57d08-165">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="57d08-166">此值必須大於或等於針對 minBuffers 指定的值。</span><span class="sxs-lookup"><span data-stu-id="57d08-166">This value must be greater than or equal to the value specified for minBuffers.</span></span><br/> <span data-ttu-id="57d08-167">分析和偵測通道的預設緩衝區數目上限為 10 KB，而系統管理員和運作方式為 64 KB。</span><span class="sxs-lookup"><span data-stu-id="57d08-167">The default maximum number of buffers for Analytic and Debug channels is 10 KB and for Admin and Operational it is 64 KB.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="57d08-168">**minBuffers**</span><span class="sxs-lookup"><span data-stu-id="57d08-168">**minBuffers**</span></span>](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [<span data-ttu-id="57d08-169">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="57d08-169">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="57d08-170">要配置給會話的緩衝區數目下限。</span><span class="sxs-lookup"><span data-stu-id="57d08-170">The minimum number of buffers to allocate for the session.</span></span> <span data-ttu-id="57d08-171">預設值是零。</span><span class="sxs-lookup"><span data-stu-id="57d08-171">The default is zero.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="57d08-172">**sidType**</span><span class="sxs-lookup"><span data-stu-id="57d08-172">**sidType**</span></span>](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | <span data-ttu-id="57d08-173">決定是否要包含主體的安全識別碼 (SID) ，並將每個事件寫入通道。</span><span class="sxs-lookup"><span data-stu-id="57d08-173">Determines whether to include a security identifier (SID) of the principal with each event written to the channel.</span></span> <span data-ttu-id="57d08-174">若要將 SID 包含在事件中，請將此屬性設定為「發佈」。</span><span class="sxs-lookup"><span data-stu-id="57d08-174">To include the SID with the event, set this attribute to "Publishing".</span></span> <span data-ttu-id="57d08-175">SID 會根據寫入事件時的執行緒識別來設定。</span><span class="sxs-lookup"><span data-stu-id="57d08-175">The SID is set based on the thread identity at the time the event is written.</span></span> <span data-ttu-id="57d08-176">如果您不想要在事件中包含 SID，請將此屬性設定為「無」。</span><span class="sxs-lookup"><span data-stu-id="57d08-176">If you do not want to include the SID with the event, set this attribute to "None".</span></span> <span data-ttu-id="57d08-177">預設值為「發佈」。</span><span class="sxs-lookup"><span data-stu-id="57d08-177">The default is "Publishing".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="57d08-178">備註</span><span class="sxs-lookup"><span data-stu-id="57d08-178">Remarks</span></span>

<span data-ttu-id="57d08-179">您可以針對分析和偵測通道類型或指定自訂隔離的任何通道指定此發行資訊。</span><span class="sxs-lookup"><span data-stu-id="57d08-179">You can specify this publishing information for Analytic and Debug channel types or for any channel that specifies Custom isolation.</span></span>

<span data-ttu-id="57d08-180">雖然您可以指定層級和關鍵字，但您應該考慮這些將是您將從該通道的提供者接收的唯一事件。</span><span class="sxs-lookup"><span data-stu-id="57d08-180">Although you can specify level and keywords, you should consider that these will be the only events that you will receive from the provider for that channel.</span></span>

<span data-ttu-id="57d08-181">當緩衝區已滿時，ETW 會將緩衝區排清到記錄檔。</span><span class="sxs-lookup"><span data-stu-id="57d08-181">When a buffer is full, ETW flushes the buffer to the log file.</span></span> <span data-ttu-id="57d08-182">如果緩衝區的填滿速度超過可以排清的緩衝區，則會配置新的緩衝區，並將其新增至會話的緩衝集區，最多可達指定的最大數目。</span><span class="sxs-lookup"><span data-stu-id="57d08-182">If the buffers are filled faster than they can be flushed, new buffers are allocated and added to the session's buffer pool, up to the maximum number specified.</span></span> <span data-ttu-id="57d08-183">超過此限制，會話會捨棄傳入事件，直到緩衝區變成可用為止。</span><span class="sxs-lookup"><span data-stu-id="57d08-183">Beyond this limit, the session discards incoming events until a buffer becomes available.</span></span>

## <a name="requirements"></a><span data-ttu-id="57d08-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="57d08-184">Requirements</span></span>



| <span data-ttu-id="57d08-185">需求</span><span class="sxs-lookup"><span data-stu-id="57d08-185">Requirement</span></span> | <span data-ttu-id="57d08-186">值</span><span class="sxs-lookup"><span data-stu-id="57d08-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57d08-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57d08-187">Minimum supported client</span></span><br/> | <span data-ttu-id="57d08-188">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57d08-188">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57d08-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57d08-189">Minimum supported server</span></span><br/> | <span data-ttu-id="57d08-190">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57d08-190">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





