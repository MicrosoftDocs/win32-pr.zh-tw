---
title: 'taskType 複雜類型 (工作排程器) '
description: 定義工作專案的子項目和排序資訊。
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- taskType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466013"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="59ca9-104">taskType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="59ca9-104">taskType Complex Type</span></span>

<span data-ttu-id="59ca9-105">定義 [**工作專案**](taskschedulerschema-task-element.md) 的子項目和排序資訊。</span><span class="sxs-lookup"><span data-stu-id="59ca9-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="59ca9-106">子元素</span><span class="sxs-lookup"><span data-stu-id="59ca9-106">Child elements</span></span>



| <span data-ttu-id="59ca9-107">元素</span><span class="sxs-lookup"><span data-stu-id="59ca9-107">Element</span></span>                                                                           | <span data-ttu-id="59ca9-108">類型</span><span class="sxs-lookup"><span data-stu-id="59ca9-108">Type</span></span>                                                                                 | <span data-ttu-id="59ca9-109">Description</span><span class="sxs-lookup"><span data-stu-id="59ca9-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59ca9-110">**行動**</span><span class="sxs-lookup"><span data-stu-id="59ca9-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="59ca9-111">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="59ca9-112">指定工作執行的動作。</span><span class="sxs-lookup"><span data-stu-id="59ca9-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="59ca9-113">**資料**</span><span class="sxs-lookup"><span data-stu-id="59ca9-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="59ca9-114">**dataType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="59ca9-115">指定與工作相關聯的額外資料，但工作排程器服務未使用。</span><span class="sxs-lookup"><span data-stu-id="59ca9-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="59ca9-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="59ca9-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="59ca9-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="59ca9-118">指定可以用來執行工作的安全性內容。</span><span class="sxs-lookup"><span data-stu-id="59ca9-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="59ca9-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="59ca9-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="59ca9-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="59ca9-121">指定工作的系統管理資訊，例如工作的作者以及註冊工作的日期。</span><span class="sxs-lookup"><span data-stu-id="59ca9-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="59ca9-122">**設定**</span><span class="sxs-lookup"><span data-stu-id="59ca9-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="59ca9-123">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="59ca9-124">指定工作排程器用來執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="59ca9-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="59ca9-125">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="59ca9-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="59ca9-126">**triggersType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="59ca9-127">指定啟動工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="59ca9-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="59ca9-128">屬性</span><span class="sxs-lookup"><span data-stu-id="59ca9-128">Attributes</span></span>



| <span data-ttu-id="59ca9-129">名稱</span><span class="sxs-lookup"><span data-stu-id="59ca9-129">Name</span></span>    | <span data-ttu-id="59ca9-130">類型</span><span class="sxs-lookup"><span data-stu-id="59ca9-130">Type</span></span>                                                              | <span data-ttu-id="59ca9-131">描述</span><span class="sxs-lookup"><span data-stu-id="59ca9-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="59ca9-132">version</span><span class="sxs-lookup"><span data-stu-id="59ca9-132">version</span></span> | [<span data-ttu-id="59ca9-133">**versionType**</span><span class="sxs-lookup"><span data-stu-id="59ca9-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="59ca9-134">指定工作的版本。</span><span class="sxs-lookup"><span data-stu-id="59ca9-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="59ca9-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="59ca9-135">Requirements</span></span>



| <span data-ttu-id="59ca9-136">需求</span><span class="sxs-lookup"><span data-stu-id="59ca9-136">Requirement</span></span> | <span data-ttu-id="59ca9-137">值</span><span class="sxs-lookup"><span data-stu-id="59ca9-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59ca9-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59ca9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="59ca9-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59ca9-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59ca9-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59ca9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="59ca9-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59ca9-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59ca9-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59ca9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ca9-143">工作排程器架構複雜類型</span><span class="sxs-lookup"><span data-stu-id="59ca9-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="59ca9-144">工作排程器</span><span class="sxs-lookup"><span data-stu-id="59ca9-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





