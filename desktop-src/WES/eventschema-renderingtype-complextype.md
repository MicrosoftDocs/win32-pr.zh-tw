---
title: RenderingInfoType 複雜類型
description: 定義事件的呈現訊息。
ms.assetid: 85a4cfc6-6277-4af8-af4e-cae3bd3aac13
keywords:
- RenderingInfoType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- RenderingInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d0e4224ec9b90e84cbacbf5ede852763edd8e4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466692"
---
# <a name="renderinginfotype-complex-type"></a><span data-ttu-id="96452-104">RenderingInfoType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="96452-104">RenderingInfoType Complex Type</span></span>

<span data-ttu-id="96452-105">定義事件的呈現訊息。</span><span class="sxs-lookup"><span data-stu-id="96452-105">Defines the rendered messages for the event.</span></span>

``` syntax
<xs:complexType name="RenderingInfoType">
    <xs:sequence>
        <xs:element name="Message"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Channel"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Provider"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="Keyword"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="Culture"
        type="language"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="96452-106">子元素</span><span class="sxs-lookup"><span data-stu-id="96452-106">Child elements</span></span>



| <span data-ttu-id="96452-107">元素</span><span class="sxs-lookup"><span data-stu-id="96452-107">Element</span></span>                                                             | <span data-ttu-id="96452-108">類型</span><span class="sxs-lookup"><span data-stu-id="96452-108">Type</span></span>   | <span data-ttu-id="96452-109">Description</span><span class="sxs-lookup"><span data-stu-id="96452-109">Description</span></span>                                                                   |
|---------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="96452-110">**通路**</span><span class="sxs-lookup"><span data-stu-id="96452-110">**Channel**</span></span>](eventschema-task-renderingtype-element.md)           | <span data-ttu-id="96452-111">字串</span><span class="sxs-lookup"><span data-stu-id="96452-111">string</span></span> | <span data-ttu-id="96452-112">事件中指定之通道的呈現訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-112">The rendered message string of the channel specified in the event.</span></span><br/> |
| [<span data-ttu-id="96452-113">**關鍵字**</span><span class="sxs-lookup"><span data-stu-id="96452-113">**Keyword**</span></span>](eventschema-keyword-keywords-element.md)             | <span data-ttu-id="96452-114">字串</span><span class="sxs-lookup"><span data-stu-id="96452-114">string</span></span> | <span data-ttu-id="96452-115">事件中指定之關鍵字的轉譯訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-115">The rendered message string of a keyword specified in the event.</span></span><br/>   |
| [<span data-ttu-id="96452-116">**關鍵字**</span><span class="sxs-lookup"><span data-stu-id="96452-116">**Keywords**</span></span>](eventschema-keywords-renderingtype-element.md)      |        | <span data-ttu-id="96452-117">已轉譯關鍵字的清單。</span><span class="sxs-lookup"><span data-stu-id="96452-117">A list of rendered keywords.</span></span><br/>                                       |
| [<span data-ttu-id="96452-118">**水準**</span><span class="sxs-lookup"><span data-stu-id="96452-118">**Level**</span></span>](eventschema-level-renderingtype-element.md)            | <span data-ttu-id="96452-119">字串</span><span class="sxs-lookup"><span data-stu-id="96452-119">string</span></span> | <span data-ttu-id="96452-120">事件中指定之層級的轉譯訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-120">The rendered message string of the level specified in the event.</span></span><br/>   |
| [<span data-ttu-id="96452-121">**消息**</span><span class="sxs-lookup"><span data-stu-id="96452-121">**Message**</span></span>](eventschema-message-renderingtype-element.md)        | <span data-ttu-id="96452-122">字串</span><span class="sxs-lookup"><span data-stu-id="96452-122">string</span></span> | <span data-ttu-id="96452-123">事件的呈現訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-123">The rendered message string of the event.</span></span><br/>                          |
| [<span data-ttu-id="96452-124">**OpCode**</span><span class="sxs-lookup"><span data-stu-id="96452-124">**Opcode**</span></span>](eventschema-opcode-renderingtype-element.md)          | <span data-ttu-id="96452-125">字串</span><span class="sxs-lookup"><span data-stu-id="96452-125">string</span></span> | <span data-ttu-id="96452-126">事件中指定之 opcode 的轉譯訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-126">The rendered message string of the opcode specified in the event.</span></span><br/>  |
| [<span data-ttu-id="96452-127">**提供者**</span><span class="sxs-lookup"><span data-stu-id="96452-127">**Provider**</span></span>](eventschema-publisher-renderinginfotype-element.md) | <span data-ttu-id="96452-128">字串</span><span class="sxs-lookup"><span data-stu-id="96452-128">string</span></span> | <span data-ttu-id="96452-129">提供者的呈現訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-129">The rendered message string for the provider.</span></span><br/>                      |
| [<span data-ttu-id="96452-130">**Task**</span><span class="sxs-lookup"><span data-stu-id="96452-130">**Task**</span></span>](eventschema-task-renderingtype-element.md)              | <span data-ttu-id="96452-131">字串</span><span class="sxs-lookup"><span data-stu-id="96452-131">string</span></span> | <span data-ttu-id="96452-132">事件中指定之工作的轉譯訊息字串。</span><span class="sxs-lookup"><span data-stu-id="96452-132">The rendered message string of the task specified in the event.</span></span><br/>    |



## <a name="attributes"></a><span data-ttu-id="96452-133">屬性</span><span class="sxs-lookup"><span data-stu-id="96452-133">Attributes</span></span>



| <span data-ttu-id="96452-134">名稱</span><span class="sxs-lookup"><span data-stu-id="96452-134">Name</span></span>    | <span data-ttu-id="96452-135">類型</span><span class="sxs-lookup"><span data-stu-id="96452-135">Type</span></span>     | <span data-ttu-id="96452-136">Description</span><span class="sxs-lookup"><span data-stu-id="96452-136">Description</span></span>                                                                                                      |
|---------|----------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96452-137">文化特性</span><span class="sxs-lookup"><span data-stu-id="96452-137">Culture</span></span> | <span data-ttu-id="96452-138">語言</span><span class="sxs-lookup"><span data-stu-id="96452-138">language</span></span> | <span data-ttu-id="96452-139"> (的語言名稱，例如，用來識別用來呈現訊息字串之地區設定的 en-us) 。</span><span class="sxs-lookup"><span data-stu-id="96452-139">The language name (for example, en-US) that identifies the locale used to render the message strings.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96452-140">備註</span><span class="sxs-lookup"><span data-stu-id="96452-140">Remarks</span></span>

<span data-ttu-id="96452-141">只有使用 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector) 服務所收集的事件才會包含此區段。</span><span class="sxs-lookup"><span data-stu-id="96452-141">Only events that have been collected using the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service will contain this section.</span></span>

## <a name="requirements"></a><span data-ttu-id="96452-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="96452-142">Requirements</span></span>



| <span data-ttu-id="96452-143">需求</span><span class="sxs-lookup"><span data-stu-id="96452-143">Requirement</span></span> | <span data-ttu-id="96452-144">值</span><span class="sxs-lookup"><span data-stu-id="96452-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96452-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96452-145">Minimum supported client</span></span><br/> | <span data-ttu-id="96452-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96452-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96452-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96452-147">Minimum supported server</span></span><br/> | <span data-ttu-id="96452-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96452-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

