---
title: 資料 (taskType) 元素
description: 定義與工作相關聯的加法資料，但工作排程器服務未使用。
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- 工作排程器的資料元素
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685739"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="c394f-104">資料 (taskType) 元素</span><span class="sxs-lookup"><span data-stu-id="c394f-104">Data (taskType) Element</span></span>

<span data-ttu-id="c394f-105">定義與工作相關聯的加法資料，但工作排程器服務未使用。</span><span class="sxs-lookup"><span data-stu-id="c394f-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="c394f-106">**資料** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c394f-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c394f-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c394f-107">Parent element</span></span>



| <span data-ttu-id="c394f-108">元素</span><span class="sxs-lookup"><span data-stu-id="c394f-108">Element</span></span>                                          | <span data-ttu-id="c394f-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c394f-109">Derived from</span></span>                                                 | <span data-ttu-id="c394f-110">Description</span><span class="sxs-lookup"><span data-stu-id="c394f-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="c394f-111">**Task**</span><span class="sxs-lookup"><span data-stu-id="c394f-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="c394f-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="c394f-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="c394f-113">定義工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="c394f-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c394f-114">備註</span><span class="sxs-lookup"><span data-stu-id="c394f-114">Remarks</span></span>

<span data-ttu-id="c394f-115">作為這類資料的範例，效能記錄檔及警示服務會使用這個屬性做為與工作相關聯之效能計數器查詢的儲存體容器。</span><span class="sxs-lookup"><span data-stu-id="c394f-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="c394f-116">針對 c + + 開發，會使用 [**ITaskDefinition 的資料屬性**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data)來指定工作的資料。</span><span class="sxs-lookup"><span data-stu-id="c394f-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="c394f-117">在腳本開發中，會使用 [**TaskDefinition**](taskdefinition-data.md) 屬性來指定工作的資料。</span><span class="sxs-lookup"><span data-stu-id="c394f-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c394f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c394f-118">Requirements</span></span>



| <span data-ttu-id="c394f-119">需求</span><span class="sxs-lookup"><span data-stu-id="c394f-119">Requirement</span></span> | <span data-ttu-id="c394f-120">值</span><span class="sxs-lookup"><span data-stu-id="c394f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c394f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c394f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c394f-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c394f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c394f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c394f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c394f-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c394f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c394f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c394f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c394f-126">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="c394f-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c394f-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c394f-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





