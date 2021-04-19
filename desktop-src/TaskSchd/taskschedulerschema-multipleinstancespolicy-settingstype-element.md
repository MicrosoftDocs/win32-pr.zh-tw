---
title: MultipleInstancesPolicy (settingsType) 元素
description: 指定原則，定義工作排程器處理工作之多個實例的方式。
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- MultipleInstancesPolicy 元素工作排程器
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965915"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="c9003-104">MultipleInstancesPolicy (settingsType) 元素</span><span class="sxs-lookup"><span data-stu-id="c9003-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="c9003-105">指定原則，定義工作排程器處理工作之多個實例的方式。</span><span class="sxs-lookup"><span data-stu-id="c9003-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="c9003-106">**MultipleInstancesPolicy** 元素是由 [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple 型別定義。</span><span class="sxs-lookup"><span data-stu-id="c9003-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c9003-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c9003-107">Parent element</span></span>



| <span data-ttu-id="c9003-108">元素</span><span class="sxs-lookup"><span data-stu-id="c9003-108">Element</span></span>                                                           | <span data-ttu-id="c9003-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c9003-109">Derived from</span></span>                                                         | <span data-ttu-id="c9003-110">Description</span><span class="sxs-lookup"><span data-stu-id="c9003-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9003-111">**設定**</span><span class="sxs-lookup"><span data-stu-id="c9003-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="c9003-112">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="c9003-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="c9003-113">包含工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="c9003-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c9003-114">備註</span><span class="sxs-lookup"><span data-stu-id="c9003-114">Remarks</span></span>

<span data-ttu-id="c9003-115">針對 c + + 開發，請參閱 [**ITaskSettings 的 MultipleInstances 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances)。</span><span class="sxs-lookup"><span data-stu-id="c9003-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="c9003-116">如需腳本開發，請參閱 [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md)。</span><span class="sxs-lookup"><span data-stu-id="c9003-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="c9003-117">限制的值</span><span class="sxs-lookup"><span data-stu-id="c9003-117">Restricted Values</span></span>

<span data-ttu-id="c9003-118">這個元素會限制為下列值。</span><span class="sxs-lookup"><span data-stu-id="c9003-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="c9003-119">Parallel：當現有的實例正在執行時，啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="c9003-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="c9003-120">Queue：在工作的所有其他實例完成之後，啟動新的工作實例。</span><span class="sxs-lookup"><span data-stu-id="c9003-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="c9003-121">IgnoreNew：預設值。</span><span class="sxs-lookup"><span data-stu-id="c9003-121">IgnoreNew: Default.</span></span> <span data-ttu-id="c9003-122">如果工作的現有實例正在執行，則不會啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="c9003-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="c9003-123">StopExisting：停止工作的現有實例，然後啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="c9003-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="c9003-124">範例</span><span class="sxs-lookup"><span data-stu-id="c9003-124">Examples</span></span>

<span data-ttu-id="c9003-125">下列 XML 會定義允許多個工作實例平行執行的設定元素。</span><span class="sxs-lookup"><span data-stu-id="c9003-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="c9003-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9003-126">Requirements</span></span>



| <span data-ttu-id="c9003-127">需求</span><span class="sxs-lookup"><span data-stu-id="c9003-127">Requirement</span></span> | <span data-ttu-id="c9003-128">值</span><span class="sxs-lookup"><span data-stu-id="c9003-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9003-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9003-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9003-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9003-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9003-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9003-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9003-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9003-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9003-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9003-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9003-134">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c9003-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





