---
title: Task 項目
description: 定義工作排程器服務所執行的工作。
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Task 元素工作排程器
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843256"
---
# <a name="task-element"></a><span data-ttu-id="5390f-104">Task 項目</span><span class="sxs-lookup"><span data-stu-id="5390f-104">Task Element</span></span>

<span data-ttu-id="5390f-105">定義工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="5390f-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="5390f-106">子元素</span><span class="sxs-lookup"><span data-stu-id="5390f-106">Child elements</span></span>



| <span data-ttu-id="5390f-107">元素</span><span class="sxs-lookup"><span data-stu-id="5390f-107">Element</span></span>                                                                           | <span data-ttu-id="5390f-108">類型</span><span class="sxs-lookup"><span data-stu-id="5390f-108">Type</span></span>                                                                                 | <span data-ttu-id="5390f-109">Description</span><span class="sxs-lookup"><span data-stu-id="5390f-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5390f-110">**行動**</span><span class="sxs-lookup"><span data-stu-id="5390f-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="5390f-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="5390f-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="5390f-112">指定工作執行的動作。</span><span class="sxs-lookup"><span data-stu-id="5390f-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="5390f-113">**資料**</span><span class="sxs-lookup"><span data-stu-id="5390f-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="5390f-114">**dataType**</span><span class="sxs-lookup"><span data-stu-id="5390f-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="5390f-115">指定與工作相關聯的額外資料，但工作排程器服務未使用。</span><span class="sxs-lookup"><span data-stu-id="5390f-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="5390f-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="5390f-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="5390f-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="5390f-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="5390f-118">指定可以用來執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="5390f-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="5390f-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="5390f-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="5390f-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="5390f-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="5390f-121">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="5390f-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="5390f-122">**設定**</span><span class="sxs-lookup"><span data-stu-id="5390f-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="5390f-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="5390f-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="5390f-124">指定工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="5390f-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="5390f-125">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="5390f-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="5390f-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="5390f-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="5390f-127">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="5390f-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="5390f-128">備註</span><span class="sxs-lookup"><span data-stu-id="5390f-128">Remarks</span></span>

<span data-ttu-id="5390f-129">針對 c + + 開發，請參閱 [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)。</span><span class="sxs-lookup"><span data-stu-id="5390f-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="5390f-130">如需腳本開發，請參閱 [**TaskDefinition**](taskdefinition.md)。</span><span class="sxs-lookup"><span data-stu-id="5390f-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5390f-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5390f-131">Requirements</span></span>



| <span data-ttu-id="5390f-132">需求</span><span class="sxs-lookup"><span data-stu-id="5390f-132">Requirement</span></span> | <span data-ttu-id="5390f-133">值</span><span class="sxs-lookup"><span data-stu-id="5390f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5390f-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5390f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5390f-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5390f-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5390f-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5390f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5390f-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5390f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





