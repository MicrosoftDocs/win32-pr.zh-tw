---
title: opcode (TaskEventDefinitionType) 元素
description: 包含事件的工作特定作業碼。 所有的 opcode 定義都假設為包含事件定義之工作的特定工作。
ms.assetid: c7192772-401b-4602-918d-0e0bc4b65ca7
keywords:
- opcode 元素 EventLog
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9f3b58353163e1ee5b9abeb04007a4a9d449e5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968994"
---
# <a name="opcode-taskeventdefinitiontype-element"></a><span data-ttu-id="c8630-105">opcode (TaskEventDefinitionType) 元素</span><span class="sxs-lookup"><span data-stu-id="c8630-105">opcode (TaskEventDefinitionType) Element</span></span>

<span data-ttu-id="c8630-106">\[從 Windows 7 版 Windows SDK 隨附的訊息編譯器開始，此專案已無法再使用。\]</span><span class="sxs-lookup"><span data-stu-id="c8630-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="c8630-107">包含事件的工作特定作業碼。</span><span class="sxs-lookup"><span data-stu-id="c8630-107">Contains a task-specific opcode for an event.</span></span> <span data-ttu-id="c8630-108">所有的 opcode 定義都假設為包含事件定義之工作的特定工作。</span><span class="sxs-lookup"><span data-stu-id="c8630-108">All of the opcode definitions are assumed to be task-specific for the task that contains the event definitions.</span></span>

``` syntax
<xs:element name="opcode">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="event"
                type="EventDefinitionType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
        <xs:attribute name="name"
            type="QName"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="c8630-109">**Opcode** 元素是由 [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c8630-109">The **opcode** element is defined by the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c8630-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c8630-110">Child elements</span></span>



| <span data-ttu-id="c8630-111">元素</span><span class="sxs-lookup"><span data-stu-id="c8630-111">Element</span></span>                                                   | <span data-ttu-id="c8630-112">類型</span><span class="sxs-lookup"><span data-stu-id="c8630-112">Type</span></span>                                                                               | <span data-ttu-id="c8630-113">Description</span><span class="sxs-lookup"><span data-stu-id="c8630-113">Description</span></span>                                        |
|-----------------------------------------------------------|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c8630-114">**事件**</span><span class="sxs-lookup"><span data-stu-id="c8630-114">**event**</span></span>](eventmanifestschema-event-opcode-element.md) | [<span data-ttu-id="c8630-115">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="c8630-115">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="c8630-116">與工作一起發行的事件。</span><span class="sxs-lookup"><span data-stu-id="c8630-116">An event that is published with a task.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="c8630-117">屬性</span><span class="sxs-lookup"><span data-stu-id="c8630-117">Attributes</span></span>



| <span data-ttu-id="c8630-118">名稱</span><span class="sxs-lookup"><span data-stu-id="c8630-118">Name</span></span> | <span data-ttu-id="c8630-119">類型</span><span class="sxs-lookup"><span data-stu-id="c8630-119">Type</span></span>      | <span data-ttu-id="c8630-120">描述</span><span class="sxs-lookup"><span data-stu-id="c8630-120">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="c8630-121">NAME</span><span class="sxs-lookup"><span data-stu-id="c8630-121">name</span></span> | <span data-ttu-id="c8630-122">**QName**</span><span class="sxs-lookup"><span data-stu-id="c8630-122">**QName**</span></span> | <span data-ttu-id="c8630-123">工作特定作業碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8630-123">The name of the task-specific opcode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c8630-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8630-124">Requirements</span></span>



| <span data-ttu-id="c8630-125">需求</span><span class="sxs-lookup"><span data-stu-id="c8630-125">Requirement</span></span> | <span data-ttu-id="c8630-126">值</span><span class="sxs-lookup"><span data-stu-id="c8630-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8630-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8630-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8630-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8630-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c8630-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8630-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8630-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8630-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8630-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8630-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8630-132">**父元素**</span><span class="sxs-lookup"><span data-stu-id="c8630-132">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="c8630-133">**task (DefinitionType)**</span><span class="sxs-lookup"><span data-stu-id="c8630-133">**task (DefinitionType)**</span></span>](eventmanifestschema-task-definitiontype-element.md)
</dt> </dl>

 

 





