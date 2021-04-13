---
title: Action 物件
description: 腳本物件，提供所有動作物件所繼承的通用屬性。
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- 動作物件工作排程器
- 動作物件工作排程器，說明
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508883"
---
# <a name="action-object"></a><span data-ttu-id="96004-105">Action 物件</span><span class="sxs-lookup"><span data-stu-id="96004-105">Action object</span></span>

<span data-ttu-id="96004-106">腳本物件，提供所有動作物件所繼承的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="96004-106">Scripting object that provides the common properties that are inherited by all action objects.</span></span> <span data-ttu-id="96004-107">動作物件是由 [**actioncollection 動作**](actioncollection-create.md) 建立的方法所建立。</span><span class="sxs-lookup"><span data-stu-id="96004-107">An action object is created by the [**ActionCollection.Create**](actioncollection-create.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="96004-108">成員</span><span class="sxs-lookup"><span data-stu-id="96004-108">Members</span></span>

<span data-ttu-id="96004-109">**Action** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="96004-109">The **Action** object has these types of members:</span></span>

-   [<span data-ttu-id="96004-110">屬性</span><span class="sxs-lookup"><span data-stu-id="96004-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96004-111">屬性</span><span class="sxs-lookup"><span data-stu-id="96004-111">Properties</span></span>

<span data-ttu-id="96004-112">**動作** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="96004-112">The **Action** object has these properties.</span></span>



| <span data-ttu-id="96004-113">屬性</span><span class="sxs-lookup"><span data-stu-id="96004-113">Property</span></span>                               | <span data-ttu-id="96004-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="96004-114">Access type</span></span>           | <span data-ttu-id="96004-115">Description</span><span class="sxs-lookup"><span data-stu-id="96004-115">Description</span></span>                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [<span data-ttu-id="96004-116">**Id**</span><span class="sxs-lookup"><span data-stu-id="96004-116">**Id**</span></span>](action-id.md)<br/>     | <span data-ttu-id="96004-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="96004-117">Read/write</span></span><br/> | <span data-ttu-id="96004-118">取得或設定動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96004-118">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="96004-119">**類型**</span><span class="sxs-lookup"><span data-stu-id="96004-119">**Type**</span></span>](action-type.md)<br/> | <span data-ttu-id="96004-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="96004-120">Read-only</span></span><br/>  | <span data-ttu-id="96004-121">取得動作的類型。</span><span class="sxs-lookup"><span data-stu-id="96004-121">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="96004-122">備註</span><span class="sxs-lookup"><span data-stu-id="96004-122">Remarks</span></span>

<span data-ttu-id="96004-123">如需動作和工作如何一起運作的詳細資訊，請參閱工作 [動作](task-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="96004-123">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span> <span data-ttu-id="96004-124">下表包含腳本物件，代表可以執行的動作：</span><span class="sxs-lookup"><span data-stu-id="96004-124">The following table contains the scripting objects that represent the actions that can be performed:</span></span>



| <span data-ttu-id="96004-125">API</span><span class="sxs-lookup"><span data-stu-id="96004-125">API</span></span>                                            | <span data-ttu-id="96004-126">描述</span><span class="sxs-lookup"><span data-stu-id="96004-126">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="96004-127">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="96004-127">**ComHandlerAction**</span></span>](comhandleraction.md)   | <span data-ttu-id="96004-128">表示引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="96004-128">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="96004-129">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="96004-129">**ExecAction**</span></span>](execaction.md)               | <span data-ttu-id="96004-130">表示執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="96004-130">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="96004-131">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="96004-131">**EmailAction**</span></span>](emailaction.md)             | <span data-ttu-id="96004-132">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="96004-132">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="96004-133">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="96004-133">**ShowMessageAction**</span></span>](showmessageaction.md) | <span data-ttu-id="96004-134">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="96004-134">Represents an action that shows a message box.</span></span>               |



 

<span data-ttu-id="96004-135">讀取或寫入 XML 時，會在工作排程器架構的 [**actions**](taskschedulerschema-actions-tasktype-element.md) 元素中指定工作的動作。</span><span class="sxs-lookup"><span data-stu-id="96004-135">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="96004-136">範例</span><span class="sxs-lookup"><span data-stu-id="96004-136">Examples</span></span>

<span data-ttu-id="96004-137">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md) 、 [事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、 [每日觸發程式範例 (腳本 ](daily-trigger-example--scripting-.md)) 、 [註冊觸發 ](registration-trigger-example--scripting-.md)程式範例 (腳本) 、 [的觸發程式 ](weekly-trigger-example--scripting-.md)範例、 [登入觸發 ](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或啟動觸發程式範例 [ (腳本) ](boot-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="96004-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96004-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="96004-138">Requirements</span></span>



| <span data-ttu-id="96004-139">需求</span><span class="sxs-lookup"><span data-stu-id="96004-139">Requirement</span></span> | <span data-ttu-id="96004-140">值</span><span class="sxs-lookup"><span data-stu-id="96004-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96004-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96004-141">Minimum supported client</span></span><br/> | <span data-ttu-id="96004-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96004-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="96004-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96004-143">Minimum supported server</span></span><br/> | <span data-ttu-id="96004-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96004-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96004-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="96004-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="96004-146"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="96004-146"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="96004-147">DLL</span><span class="sxs-lookup"><span data-stu-id="96004-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96004-148"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96004-148"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96004-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96004-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96004-150">工作排程器腳本物件</span><span class="sxs-lookup"><span data-stu-id="96004-150">Task Scheduler Scripting Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="96004-151">工作排程器</span><span class="sxs-lookup"><span data-stu-id="96004-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





