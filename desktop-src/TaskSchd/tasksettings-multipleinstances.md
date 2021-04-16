---
title: TaskSettings. MultipleInstances 屬性
description: 針對腳本，取得或設定原則，以定義工作排程器處理工作之多個實例的方式。
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- MultipleInstances 屬性工作排程器
- MultipleInstances 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、MultipleInstances 屬性
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508368"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="e93a1-106">TaskSettings. MultipleInstances 屬性</span><span class="sxs-lookup"><span data-stu-id="e93a1-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="e93a1-107">針對腳本，取得或設定原則，以定義工作排程器處理工作之多個實例的方式。</span><span class="sxs-lookup"><span data-stu-id="e93a1-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="e93a1-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e93a1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93a1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e93a1-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="e93a1-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e93a1-110">Property value</span></span>

<span data-ttu-id="e93a1-111">[**工作 \_實例 \_ 原則**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) 常數。</span><span class="sxs-lookup"><span data-stu-id="e93a1-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="e93a1-112">值</span><span class="sxs-lookup"><span data-stu-id="e93a1-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="e93a1-113">意義</span><span class="sxs-lookup"><span data-stu-id="e93a1-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="e93a1-114"><dt>**工作 \_實例 \_ 平行**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e93a1-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="e93a1-115">當工作的現有實例正在執行時，啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="e93a1-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="e93a1-116"><dt>**工作 \_實例 \_ 佇列**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e93a1-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="e93a1-117">在工作的所有其他實例完成之後，啟動工作的新實例。</span><span class="sxs-lookup"><span data-stu-id="e93a1-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="e93a1-118"><dt>**工作 \_實例 \_ 忽略 \_ 新**</dt>的 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e93a1-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="e93a1-119">如果工作的現有實例正在執行，則不會啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="e93a1-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="e93a1-120"><dt>**工作 \_實例 \_ 停止 \_ 現有**</dt>的 <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e93a1-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e93a1-121">停止工作的現有實例，然後再啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="e93a1-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="e93a1-122">備註</span><span class="sxs-lookup"><span data-stu-id="e93a1-122">Remarks</span></span>

<span data-ttu-id="e93a1-123">讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="e93a1-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e93a1-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e93a1-124">Requirements</span></span>



| <span data-ttu-id="e93a1-125">需求</span><span class="sxs-lookup"><span data-stu-id="e93a1-125">Requirement</span></span> | <span data-ttu-id="e93a1-126">值</span><span class="sxs-lookup"><span data-stu-id="e93a1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e93a1-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e93a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e93a1-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e93a1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e93a1-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e93a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e93a1-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e93a1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e93a1-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e93a1-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="e93a1-132"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e93a1-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e93a1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e93a1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e93a1-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e93a1-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e93a1-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e93a1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93a1-136">**工作 \_ 實例 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="e93a1-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="e93a1-137">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e93a1-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





