---
title: TaskType) 元素 (動作
description: 包含工作所執行的動作。
ms.assetid: 0a48fbd6-8a6f-4bad-9b28-0631dce15748
keywords:
- 動作 (taskType) 元素工作排程器
- 動作工作排程器、XML
- Actions 元素工作排程器
topic_type:
- apiref
api_name:
- Actions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21af0f8a06faa9cdc61917dcb3b3b0672c47e0e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384225"
---
# <a name="actions-tasktype-element"></a><span data-ttu-id="93670-106">TaskType) 元素 (動作</span><span class="sxs-lookup"><span data-stu-id="93670-106">Actions (taskType) Element</span></span>

<span data-ttu-id="93670-107">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="93670-107">Contains the actions performed by the task.</span></span>

``` syntax
<xs:element name="Actions"
    type="actionsType"
 />
```

<span data-ttu-id="93670-108">**Actions** 元素是由 [**taskType**](taskschedulerschema-tasktype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="93670-108">The **Actions** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="93670-109">父元素</span><span class="sxs-lookup"><span data-stu-id="93670-109">Parent element</span></span>



| <span data-ttu-id="93670-110">元素</span><span class="sxs-lookup"><span data-stu-id="93670-110">Element</span></span>                                          | <span data-ttu-id="93670-111">衍生自</span><span class="sxs-lookup"><span data-stu-id="93670-111">Derived from</span></span>                                                 | <span data-ttu-id="93670-112">Description</span><span class="sxs-lookup"><span data-stu-id="93670-112">Description</span></span>                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="93670-113">**Task**</span><span class="sxs-lookup"><span data-stu-id="93670-113">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="93670-114">**taskType**</span><span class="sxs-lookup"><span data-stu-id="93670-114">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="93670-115">描述工作排程器服務所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="93670-115">Describes the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="93670-116">子元素</span><span class="sxs-lookup"><span data-stu-id="93670-116">Child elements</span></span>



| <span data-ttu-id="93670-117">元素</span><span class="sxs-lookup"><span data-stu-id="93670-117">Element</span></span>                                                                    | <span data-ttu-id="93670-118">類型</span><span class="sxs-lookup"><span data-stu-id="93670-118">Type</span></span>                                                                       | <span data-ttu-id="93670-119">Description</span><span class="sxs-lookup"><span data-stu-id="93670-119">Description</span></span>                                                            |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="93670-120">**ComHandler**</span><span class="sxs-lookup"><span data-stu-id="93670-120">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | [<span data-ttu-id="93670-121">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="93670-121">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md)   | <span data-ttu-id="93670-122">指定引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="93670-122">Specifies an action that fires a handler.</span></span><br/>                   |
| [<span data-ttu-id="93670-123">**Exec**</span><span class="sxs-lookup"><span data-stu-id="93670-123">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | [<span data-ttu-id="93670-124">**execType**</span><span class="sxs-lookup"><span data-stu-id="93670-124">**execType**</span></span>](taskschedulerschema-exectype-complextype.md)               | <span data-ttu-id="93670-125">指定執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="93670-125">Specifies an action that executes a command-line operation.</span></span><br/> |
| [<span data-ttu-id="93670-126">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="93670-126">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | [<span data-ttu-id="93670-127">**sendEmailType**</span><span class="sxs-lookup"><span data-stu-id="93670-127">**sendEmailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md)     | <span data-ttu-id="93670-128">指定傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="93670-128">Specifies an action that sends an email message.</span></span><br/>            |
| [<span data-ttu-id="93670-129">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="93670-129">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="93670-130">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="93670-130">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="93670-131">指定顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="93670-131">Specifies an action that shows a message box.</span></span><br/>               |



## <a name="attributes"></a><span data-ttu-id="93670-132">屬性</span><span class="sxs-lookup"><span data-stu-id="93670-132">Attributes</span></span>



| <span data-ttu-id="93670-133">名稱</span><span class="sxs-lookup"><span data-stu-id="93670-133">Name</span></span>    | <span data-ttu-id="93670-134">類型</span><span class="sxs-lookup"><span data-stu-id="93670-134">Type</span></span> | <span data-ttu-id="93670-135">描述</span><span class="sxs-lookup"><span data-stu-id="93670-135">Description</span></span>                                                                                          |
|---------|------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93670-136">Context</span><span class="sxs-lookup"><span data-stu-id="93670-136">Context</span></span> |      | <span data-ttu-id="93670-137">做為工作動作之安全性內容之使用者的主體識別碼。</span><span class="sxs-lookup"><span data-stu-id="93670-137">Principal identifier of the user who is the security context for the actions of the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="93670-138">備註</span><span class="sxs-lookup"><span data-stu-id="93670-138">Remarks</span></span>

<span data-ttu-id="93670-139">先前所列的子項目 (最大的 32) 是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md) 群組定義。</span><span class="sxs-lookup"><span data-stu-id="93670-139">The child elements listed previously (maximum 32) are defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) group.</span></span> <span data-ttu-id="93670-140">您可以依任何順序加入這些元素。</span><span class="sxs-lookup"><span data-stu-id="93670-140">These elements can be added in any order.</span></span>

<span data-ttu-id="93670-141">針對 c + + 開發，工作的動作會定義在 [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) 介面中。</span><span class="sxs-lookup"><span data-stu-id="93670-141">For C++ development, the actions of a task are defined in the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface.</span></span>

<span data-ttu-id="93670-142">針對腳本開發，工作的動作會定義在 [**actioncollection 動作**](actioncollection.md) 物件中。</span><span class="sxs-lookup"><span data-stu-id="93670-142">For script development, the actions of a task are defined in the [**ActionCollection**](actioncollection.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="93670-143">範例</span><span class="sxs-lookup"><span data-stu-id="93670-143">Examples</span></span>

<span data-ttu-id="93670-144">如需包含單一執行動作之工作的 XML 詳細資訊和完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="93670-144">For more information and a complete example of the XML for a task that contains a single execution action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93670-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="93670-145">Requirements</span></span>



| <span data-ttu-id="93670-146">需求</span><span class="sxs-lookup"><span data-stu-id="93670-146">Requirement</span></span> | <span data-ttu-id="93670-147">值</span><span class="sxs-lookup"><span data-stu-id="93670-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93670-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93670-148">Minimum supported client</span></span><br/> | <span data-ttu-id="93670-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93670-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93670-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93670-150">Minimum supported server</span></span><br/> | <span data-ttu-id="93670-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93670-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93670-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93670-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93670-153">**taskType**</span><span class="sxs-lookup"><span data-stu-id="93670-153">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md)
</dt> <dt>

[<span data-ttu-id="93670-154">**actionGroup**</span><span class="sxs-lookup"><span data-stu-id="93670-154">**actionGroup**</span></span>](taskschedulerschema-actiongroup-group.md)
</dt> <dt>

[<span data-ttu-id="93670-155">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="93670-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="93670-156">工作排程器</span><span class="sxs-lookup"><span data-stu-id="93670-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





