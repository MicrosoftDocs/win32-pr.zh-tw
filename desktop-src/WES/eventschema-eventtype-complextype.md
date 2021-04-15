---
title: 事件種類複雜類型
description: 定義事件架構的根節點。
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- 事件種類複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1103570b6c1d9f51a8cbe8fe5628460690fb32cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384006"
---
# <a name="eventtype-complex-type"></a><span data-ttu-id="647f0-104">事件種類複雜類型</span><span class="sxs-lookup"><span data-stu-id="647f0-104">EventType Complex Type</span></span>

<span data-ttu-id="647f0-105">定義事件架構的根節點。</span><span class="sxs-lookup"><span data-stu-id="647f0-105">Defines the root node of the Event schema.</span></span>

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="647f0-106">子元素</span><span class="sxs-lookup"><span data-stu-id="647f0-106">Child elements</span></span>



| <span data-ttu-id="647f0-107">元素</span><span class="sxs-lookup"><span data-stu-id="647f0-107">Element</span></span>                                                                          | <span data-ttu-id="647f0-108">類型</span><span class="sxs-lookup"><span data-stu-id="647f0-108">Type</span></span>                                                                               | <span data-ttu-id="647f0-109">Description</span><span class="sxs-lookup"><span data-stu-id="647f0-109">Description</span></span>                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="647f0-110">**BinaryEventData**</span><span class="sxs-lookup"><span data-stu-id="647f0-110">**BinaryEventData**</span></span>](eventschema-binaryeventdata-eventtype-element.md)         | <span data-ttu-id="647f0-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="647f0-111">hexBinary</span></span>                                                                          | <span data-ttu-id="647f0-112">以二進位 blob 的形式包含事件資料。</span><span class="sxs-lookup"><span data-stu-id="647f0-112">Contains the event data as a binary blob.</span></span> <span data-ttu-id="647f0-113">如果轉譯函數找不到用來解碼事件的中繼資料，則會將事件資料轉譯成二進位 blob。</span><span class="sxs-lookup"><span data-stu-id="647f0-113">The event data is rendered as a binary blob if the rendering function cannot find the metadata used to decode the event.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="647f0-114">**DebugData**</span><span class="sxs-lookup"><span data-stu-id="647f0-114">**DebugData**</span></span>](eventschema-debugdata-eventtype-element.md)                     | [<span data-ttu-id="647f0-115">**DebugDataType**</span><span class="sxs-lookup"><span data-stu-id="647f0-115">**DebugDataType**</span></span>](eventschema-debugdatatype-complextype.md)                     | <span data-ttu-id="647f0-116">包含可針對 Windows 軟體追蹤預處理器 (WPP) 事件記錄的資料。</span><span class="sxs-lookup"><span data-stu-id="647f0-116">Contains the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="647f0-117">**EventData**</span><span class="sxs-lookup"><span data-stu-id="647f0-117">**EventData**</span></span>](eventschema-eventdata-eventtype-element.md)                     | [<span data-ttu-id="647f0-118">**EventDataType**</span><span class="sxs-lookup"><span data-stu-id="647f0-118">**EventDataType**</span></span>](eventschema-eventdatatype-complextype.md)                     | <span data-ttu-id="647f0-119">包含事件資料。</span><span class="sxs-lookup"><span data-stu-id="647f0-119">Contains the event data.</span></span> <span data-ttu-id="647f0-120">範本中資料項目的順序會決定事件資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="647f0-120">The order of the data items in the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="647f0-121">**ProcessingErrorData**</span><span class="sxs-lookup"><span data-stu-id="647f0-121">**ProcessingErrorData**</span></span>](eventschema-processingerrordata-eventtype-element.md) | [<span data-ttu-id="647f0-122">**ProcessingErrorDataType**</span><span class="sxs-lookup"><span data-stu-id="647f0-122">**ProcessingErrorDataType**</span></span>](eventschema-processingerrordatatype-complextype.md) | <span data-ttu-id="647f0-123">包含嘗試呈現事件時所發生之錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="647f0-123">Contains details of the error that occurred while trying to render the event.</span></span> <span data-ttu-id="647f0-124">如果事件資料與資訊清單中的事件資料定義不符，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="647f0-124">This can occur if the event data does not match the event data definition in the manifest.</span></span> <span data-ttu-id="647f0-125">事件資料會以二進位 blob 的形式包含。</span><span class="sxs-lookup"><span data-stu-id="647f0-125">The event data is included as a binary blob.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="647f0-126">**RenderingInfo**</span><span class="sxs-lookup"><span data-stu-id="647f0-126">**RenderingInfo**</span></span>](eventschema-renderinginfo-eventtype-element.md)             | [<span data-ttu-id="647f0-127">**RenderingInfoType**</span><span class="sxs-lookup"><span data-stu-id="647f0-127">**RenderingInfoType**</span></span>](eventschema-renderingtype-complextype.md)                 | <span data-ttu-id="647f0-128">包含事件的已轉譯訊息字串 (包含事件的訊息字串，以及任何事件屬性的訊息字串，例如層級、工作和 opcode) 。</span><span class="sxs-lookup"><span data-stu-id="647f0-128">Contains the rendered message strings for the event (includes the event's message string and the message strings for any of the event's properties such as level, task, and opcode).</span></span> <span data-ttu-id="647f0-129">只有使用 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector) 服務所收集的事件才會包含此區段。</span><span class="sxs-lookup"><span data-stu-id="647f0-129">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span><br/> |
| [<span data-ttu-id="647f0-130">**系統**</span><span class="sxs-lookup"><span data-stu-id="647f0-130">**System**</span></span>](eventschema-system-eventtype-element.md)                           | [<span data-ttu-id="647f0-131">**SystemPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="647f0-131">**SystemPropertiesType**</span></span>](eventschema-systempropertiestype-complextype.md)       | <span data-ttu-id="647f0-132">包含識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="647f0-132">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="647f0-133">**UserData**</span><span class="sxs-lookup"><span data-stu-id="647f0-133">**UserData**</span></span>](eventschema-userdata-eventtype-element.md)                       | [<span data-ttu-id="647f0-134">**UserDataType**</span><span class="sxs-lookup"><span data-stu-id="647f0-134">**UserDataType**</span></span>](eventschema-userdatatype-complextype.md)                       | <span data-ttu-id="647f0-135">包含事件資料。</span><span class="sxs-lookup"><span data-stu-id="647f0-135">Contains the event data.</span></span> <span data-ttu-id="647f0-136">範本的 [使用者資料] 區段會決定事件資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="647f0-136">The user data section of the template determines the layout of the event data.</span></span><br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="647f0-137">備註</span><span class="sxs-lookup"><span data-stu-id="647f0-137">Remarks</span></span>

<span data-ttu-id="647f0-138">此區段通常會包含 **EventData** 或 **UserData** 區段。</span><span class="sxs-lookup"><span data-stu-id="647f0-138">Typically, this section will contain with the **EventData** or **UserData** section.</span></span> <span data-ttu-id="647f0-139">如果範本未包含 **UserData** 區段，則會使用 **EventData** 區段。</span><span class="sxs-lookup"><span data-stu-id="647f0-139">The **EventData** section is used if the template does not contain a **UserData** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="647f0-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="647f0-140">Requirements</span></span>



| <span data-ttu-id="647f0-141">需求</span><span class="sxs-lookup"><span data-stu-id="647f0-141">Requirement</span></span> | <span data-ttu-id="647f0-142">值</span><span class="sxs-lookup"><span data-stu-id="647f0-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="647f0-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="647f0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="647f0-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="647f0-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="647f0-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="647f0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="647f0-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="647f0-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

