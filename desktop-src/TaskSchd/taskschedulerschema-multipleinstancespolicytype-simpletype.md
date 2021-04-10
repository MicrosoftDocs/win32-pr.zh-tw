---
title: multipleInstancesPolicyType 簡單類型
description: 定義 MultipleInstancesPolicy (settingsType) 元素的實例原則常數。
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- multipleInstancesPolicyType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934591"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="57de9-104">multipleInstancesPolicyType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="57de9-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="57de9-105">定義 [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) 元素的實例原則常數。</span><span class="sxs-lookup"><span data-stu-id="57de9-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="57de9-106">列舉值</span><span class="sxs-lookup"><span data-stu-id="57de9-106">Enumeration values</span></span>

<span data-ttu-id="57de9-107">**MultipleInstancesPolicyType** 簡單類型會定義下列值。</span><span class="sxs-lookup"><span data-stu-id="57de9-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="57de9-108">值</span><span class="sxs-lookup"><span data-stu-id="57de9-108">Value</span></span>        | <span data-ttu-id="57de9-109">描述</span><span class="sxs-lookup"><span data-stu-id="57de9-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57de9-110">平行</span><span class="sxs-lookup"><span data-stu-id="57de9-110">Parallel</span></span>     | <span data-ttu-id="57de9-111">當現有的實例正在執行時，啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="57de9-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="57de9-112">佇列</span><span class="sxs-lookup"><span data-stu-id="57de9-112">Queue</span></span>        | <span data-ttu-id="57de9-113">在工作的所有其他實例完成後，啟動新的工作實例。</span><span class="sxs-lookup"><span data-stu-id="57de9-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="57de9-114">IgnoreNew</span><span class="sxs-lookup"><span data-stu-id="57de9-114">IgnoreNew</span></span>    | <span data-ttu-id="57de9-115">預設值。</span><span class="sxs-lookup"><span data-stu-id="57de9-115">Default.</span></span> <span data-ttu-id="57de9-116">如果工作的現有實例正在執行，則不會啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="57de9-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="57de9-117">StopExisting</span><span class="sxs-lookup"><span data-stu-id="57de9-117">StopExisting</span></span> | <span data-ttu-id="57de9-118">停止工作的現有實例，然後再啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="57de9-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="57de9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="57de9-119">Requirements</span></span>



| <span data-ttu-id="57de9-120">需求</span><span class="sxs-lookup"><span data-stu-id="57de9-120">Requirement</span></span> | <span data-ttu-id="57de9-121">值</span><span class="sxs-lookup"><span data-stu-id="57de9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="57de9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57de9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57de9-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57de9-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="57de9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57de9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57de9-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57de9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57de9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57de9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57de9-127">工作排程器架構簡單類型</span><span class="sxs-lookup"><span data-stu-id="57de9-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="57de9-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="57de9-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





