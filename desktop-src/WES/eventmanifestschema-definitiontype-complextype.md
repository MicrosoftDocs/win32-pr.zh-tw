---
title: DefinitionType 複雜類型
description: 定義提供者可記錄的事件清單。
ms.assetid: 6d401ced-be1a-409a-8f4d-2d977a33ff8d
keywords:
- DefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- DefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82fbf7ec7db6f64f1bac9776376fa8fe89659d9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965899"
---
# <a name="definitiontype-complex-type"></a><span data-ttu-id="1c99b-104">DefinitionType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="1c99b-104">DefinitionType Complex Type</span></span>

<span data-ttu-id="1c99b-105">定義提供者可記錄的事件清單。</span><span class="sxs-lookup"><span data-stu-id="1c99b-105">Defines a list of events that your provider can log.</span></span>

``` syntax
<xs:complexType name="DefinitionType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="event"
            type="EventDefinitionType"
         />
        <xs:element name="task"
            type="TaskEventDefinitionType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1c99b-106">子元素</span><span class="sxs-lookup"><span data-stu-id="1c99b-106">Child elements</span></span>



| <span data-ttu-id="1c99b-107">元素</span><span class="sxs-lookup"><span data-stu-id="1c99b-107">Element</span></span>                                                           | <span data-ttu-id="1c99b-108">類型</span><span class="sxs-lookup"><span data-stu-id="1c99b-108">Type</span></span>                                                                                       | <span data-ttu-id="1c99b-109">Description</span><span class="sxs-lookup"><span data-stu-id="1c99b-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c99b-110">**事件**</span><span class="sxs-lookup"><span data-stu-id="1c99b-110">**event**</span></span>](eventmanifestschema-event-definitiontype-element.md) | [<span data-ttu-id="1c99b-111">**EventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="1c99b-111">**EventDefinitionType**</span></span>](eventmanifestschema-eventdefinitiontype-complextype.md)         | <span data-ttu-id="1c99b-112">定義您的提供者可以記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="1c99b-112">Defines an event that your provider can log.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="1c99b-113">**任務**</span><span class="sxs-lookup"><span data-stu-id="1c99b-113">**task**</span></span>](eventmanifestschema-task-definitiontype-element.md)   | [<span data-ttu-id="1c99b-114">**TaskEventDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="1c99b-114">**TaskEventDefinitionType**</span></span>](eventmanifestschema-taskeventdefinitiontype-complextype.md) | <span data-ttu-id="1c99b-115">不支援。</span><span class="sxs-lookup"><span data-stu-id="1c99b-115">Not supported.</span></span><br/> <span data-ttu-id="1c99b-116">**Windows Server 2008 和 Windows Vista：** 定義您的提供者可以記錄的工作特定事件。</span><span class="sxs-lookup"><span data-stu-id="1c99b-116">**Windows Server 2008 and Windows Vista:** Defines a task-specific event that your provider can log.</span></span> <span data-ttu-id="1c99b-117"> (從 Windows SDK 的 Windows 7 版本隨附的訊息編譯器開始，不再支援工作特定事件。 ) </span><span class="sxs-lookup"><span data-stu-id="1c99b-117">(Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, task-specific events are no longer supported.)</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1c99b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c99b-118">Requirements</span></span>



| <span data-ttu-id="1c99b-119">需求</span><span class="sxs-lookup"><span data-stu-id="1c99b-119">Requirement</span></span> | <span data-ttu-id="1c99b-120">值</span><span class="sxs-lookup"><span data-stu-id="1c99b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c99b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c99b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c99b-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c99b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c99b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c99b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c99b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c99b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





