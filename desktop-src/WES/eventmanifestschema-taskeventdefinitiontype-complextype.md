---
title: TaskEventDefinitionType 複雜類型
description: 定義您的提供者可以記錄的工作特定事件。 |TaskEventDefinitionType 複雜類型
ms.assetid: f0329728-e7b5-4161-a30f-78b81a7b6812
keywords:
- TaskEventDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TaskEventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ebf752dbaf97ceced84b6bd9698faf7b191c07e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997352"
---
# <a name="taskeventdefinitiontype-complex-type"></a><span data-ttu-id="ebc14-105">TaskEventDefinitionType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="ebc14-105">TaskEventDefinitionType Complex Type</span></span>

<span data-ttu-id="ebc14-106">\[從 Windows 7 版 Windows SDK 隨附的訊息編譯器開始，就無法再使用 TaskEventDefinitionType 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="ebc14-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, the TaskEventDefinitionType complex type is no longer available.</span></span> <span data-ttu-id="ebc14-107">相反地，請使用工作特定的作業碼來提供相同的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ebc14-107">Instead use task-specific opcodes to provide the same functionality.\]</span></span>

<span data-ttu-id="ebc14-108">定義您的提供者可以記錄的工作特定事件。</span><span class="sxs-lookup"><span data-stu-id="ebc14-108">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:complexType name="TaskEventDefinitionType">
    <xs:sequence>
        <xs:element name="opcode"
            maxOccurs="unbounded"
        >
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ebc14-109">子元素</span><span class="sxs-lookup"><span data-stu-id="ebc14-109">Child elements</span></span>



| <span data-ttu-id="ebc14-110">元素</span><span class="sxs-lookup"><span data-stu-id="ebc14-110">Element</span></span>                                                                      | <span data-ttu-id="ebc14-111">類型</span><span class="sxs-lookup"><span data-stu-id="ebc14-111">Type</span></span>                                                                               | <span data-ttu-id="ebc14-112">Description</span><span class="sxs-lookup"><span data-stu-id="ebc14-112">Description</span></span>                                             |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ebc14-113">**event**</span><span class="sxs-lookup"><span data-stu-id="ebc14-113">**event**</span></span>                                                                    | [<span data-ttu-id="ebc14-114">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="ebc14-114">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md) | <span data-ttu-id="ebc14-115">以工作發佈的工作特定事件。</span><span class="sxs-lookup"><span data-stu-id="ebc14-115">A task-specific event published with a task.</span></span><br/> |
| [<span data-ttu-id="ebc14-116">**opcode**</span><span class="sxs-lookup"><span data-stu-id="ebc14-116">**opcode**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) |                                                                                    | <span data-ttu-id="ebc14-117">適用于事件的工作特定作業碼。</span><span class="sxs-lookup"><span data-stu-id="ebc14-117">A task-specific opcode that for an event.</span></span> <br/>   |



## <a name="attributes"></a><span data-ttu-id="ebc14-118">屬性</span><span class="sxs-lookup"><span data-stu-id="ebc14-118">Attributes</span></span>



| <span data-ttu-id="ebc14-119">名稱</span><span class="sxs-lookup"><span data-stu-id="ebc14-119">Name</span></span> | <span data-ttu-id="ebc14-120">類型</span><span class="sxs-lookup"><span data-stu-id="ebc14-120">Type</span></span>      | <span data-ttu-id="ebc14-121">描述</span><span class="sxs-lookup"><span data-stu-id="ebc14-121">Description</span></span>                                      |
|------|-----------|--------------------------------------------------|
| <span data-ttu-id="ebc14-122">NAME</span><span class="sxs-lookup"><span data-stu-id="ebc14-122">name</span></span> | <span data-ttu-id="ebc14-123">**QName**</span><span class="sxs-lookup"><span data-stu-id="ebc14-123">**QName**</span></span> | <span data-ttu-id="ebc14-124">工作特定作業碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc14-124">The name of the task-specific opcode.</span></span><br/> |
| <span data-ttu-id="ebc14-125">NAME</span><span class="sxs-lookup"><span data-stu-id="ebc14-125">name</span></span> | <span data-ttu-id="ebc14-126">anyURI</span><span class="sxs-lookup"><span data-stu-id="ebc14-126">anyURI</span></span>    | <span data-ttu-id="ebc14-127">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebc14-127">The name of the task.</span></span><br/>                 |



## <a name="requirements"></a><span data-ttu-id="ebc14-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebc14-128">Requirements</span></span>



| <span data-ttu-id="ebc14-129">需求</span><span class="sxs-lookup"><span data-stu-id="ebc14-129">Requirement</span></span> | <span data-ttu-id="ebc14-130">值</span><span class="sxs-lookup"><span data-stu-id="ebc14-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebc14-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebc14-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc14-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebc14-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ebc14-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebc14-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc14-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebc14-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





