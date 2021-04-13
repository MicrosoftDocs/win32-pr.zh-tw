---
title: TaskListType 複雜類型
description: 定義用來識別應用程式元件的工作清單。
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- TaskListType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383806"
---
# <a name="tasklisttype-complex-type"></a><span data-ttu-id="36fb4-104">TaskListType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="36fb4-104">TaskListType Complex Type</span></span>

<span data-ttu-id="36fb4-105">定義用來識別應用程式元件的工作清單。</span><span class="sxs-lookup"><span data-stu-id="36fb4-105">Defines a list of tasks that are used to identify the components of an application.</span></span>

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="36fb4-106">子元素</span><span class="sxs-lookup"><span data-stu-id="36fb4-106">Child elements</span></span>



| <span data-ttu-id="36fb4-107">元素</span><span class="sxs-lookup"><span data-stu-id="36fb4-107">Element</span></span>                                                       | <span data-ttu-id="36fb4-108">類型</span><span class="sxs-lookup"><span data-stu-id="36fb4-108">Type</span></span>                                                         | <span data-ttu-id="36fb4-109">Description</span><span class="sxs-lookup"><span data-stu-id="36fb4-109">Description</span></span>                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="36fb4-110">**任務**</span><span class="sxs-lookup"><span data-stu-id="36fb4-110">**task**</span></span>](eventmanifestschema-task-tasklisttype-element.md) | [<span data-ttu-id="36fb4-111">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="36fb4-111">**TaskType**</span></span>](eventmanifestschema-tasktype-complextype.md) | <span data-ttu-id="36fb4-112">定義應用程式的元件或子元件。</span><span class="sxs-lookup"><span data-stu-id="36fb4-112">Defines a component or subcomponent of an application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="36fb4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="36fb4-113">Requirements</span></span>



| <span data-ttu-id="36fb4-114">需求</span><span class="sxs-lookup"><span data-stu-id="36fb4-114">Requirement</span></span> | <span data-ttu-id="36fb4-115">值</span><span class="sxs-lookup"><span data-stu-id="36fb4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36fb4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36fb4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36fb4-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36fb4-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36fb4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36fb4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36fb4-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36fb4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





