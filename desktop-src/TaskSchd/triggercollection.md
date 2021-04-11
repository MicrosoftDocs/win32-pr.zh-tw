---
title: 'TriggerCollection 物件 (]) '
description: 腳本物件，用來新增、移除及取出工作的觸發程式。
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- 觸發程式工作排程器，觸發程式集合物件
- TriggerCollection 物件工作排程器
- TriggerCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094223"
---
# <a name="triggercollection-object"></a><span data-ttu-id="2ab6b-106">TriggerCollection 物件</span><span class="sxs-lookup"><span data-stu-id="2ab6b-106">TriggerCollection object</span></span>

<span data-ttu-id="2ab6b-107">腳本物件，用來新增、移除及取出工作的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-107">Scripting object that is used to add to, remove from, and retrieve the triggers of a task.</span></span>

## <a name="members"></a><span data-ttu-id="2ab6b-108">成員</span><span class="sxs-lookup"><span data-stu-id="2ab6b-108">Members</span></span>

<span data-ttu-id="2ab6b-109">**TriggerCollection** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2ab6b-109">The **TriggerCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="2ab6b-110">方法</span><span class="sxs-lookup"><span data-stu-id="2ab6b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ab6b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2ab6b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ab6b-112">方法</span><span class="sxs-lookup"><span data-stu-id="2ab6b-112">Methods</span></span>

<span data-ttu-id="2ab6b-113">**TriggerCollection** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-113">The **TriggerCollection** object has these methods.</span></span>



| <span data-ttu-id="2ab6b-114">方法</span><span class="sxs-lookup"><span data-stu-id="2ab6b-114">Method</span></span>                                     | <span data-ttu-id="2ab6b-115">描述</span><span class="sxs-lookup"><span data-stu-id="2ab6b-115">Description</span></span>                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ab6b-116">**清楚**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-116">**Clear**</span></span>](triggercollection-clear.md)   | <span data-ttu-id="2ab6b-117">清除集合中的所有觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-117">Clears all triggers from the collection.</span></span><br/>                                        |
| [<span data-ttu-id="2ab6b-118">**建立**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-118">**Create**</span></span>](triggercollection-create.md) | <span data-ttu-id="2ab6b-119">為工作建立新的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-119">Creates a new trigger for the task.</span></span><br/>                                             |
| [<span data-ttu-id="2ab6b-120">**移除**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-120">**Remove**</span></span>](triggercollection-remove.md) | <span data-ttu-id="2ab6b-121">從工作所用的觸發程式集合中移除指定的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-121">Removes the specified trigger from the collection of triggers used by the task.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2ab6b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="2ab6b-122">Properties</span></span>

<span data-ttu-id="2ab6b-123">**TriggerCollection** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-123">The **TriggerCollection** object has these properties.</span></span>



| <span data-ttu-id="2ab6b-124">屬性</span><span class="sxs-lookup"><span data-stu-id="2ab6b-124">Property</span></span>                                            | <span data-ttu-id="2ab6b-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="2ab6b-125">Access type</span></span>          | <span data-ttu-id="2ab6b-126">Description</span><span class="sxs-lookup"><span data-stu-id="2ab6b-126">Description</span></span>                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="2ab6b-127">**計數**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-127">**Count**</span></span>](triggercollection-count.md)<br/> | <span data-ttu-id="2ab6b-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="2ab6b-128">Read-only</span></span><br/> | <span data-ttu-id="2ab6b-129">取得集合中的觸發程式數目。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-129">Gets the number of triggers in the collection.</span></span><br/>  |
| [<span data-ttu-id="2ab6b-130">**項目**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-130">**Item**</span></span>](triggercollection-item.md)<br/>   | <span data-ttu-id="2ab6b-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="2ab6b-131">Read-only</span></span><br/> | <span data-ttu-id="2ab6b-132">從集合中取得指定的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-132">Gets the specified trigger from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ab6b-133">備註</span><span class="sxs-lookup"><span data-stu-id="2ab6b-133">Remarks</span></span>

<span data-ttu-id="2ab6b-134">讀取或寫入工作的 XML 時，工作的觸發程式會在工作排程器架構的 [**觸發**](taskschedulerschema-triggers-tasktype-element.md) 程式元素中指定。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-134">When reading or writing XML for a task, the triggers for the task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="2ab6b-135">如需每個觸發程式類型的詳細資訊，請參閱 [觸發程式類型](trigger-types.md)。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-135">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2ab6b-136">範例</span><span class="sxs-lookup"><span data-stu-id="2ab6b-136">Examples</span></span>

<span data-ttu-id="2ab6b-137">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="2ab6b-137">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab6b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ab6b-138">Requirements</span></span>



| <span data-ttu-id="2ab6b-139">需求</span><span class="sxs-lookup"><span data-stu-id="2ab6b-139">Requirement</span></span> | <span data-ttu-id="2ab6b-140">值</span><span class="sxs-lookup"><span data-stu-id="2ab6b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab6b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ab6b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab6b-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ab6b-142">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2ab6b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ab6b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab6b-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ab6b-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2ab6b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="2ab6b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ab6b-146"><dt>App.xaml.。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ab6b-146"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="2ab6b-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2ab6b-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ab6b-148"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ab6b-148"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="2ab6b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="2ab6b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ab6b-150"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ab6b-150"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="2ab6b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ab6b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab6b-152">**觸發**</span><span class="sxs-lookup"><span data-stu-id="2ab6b-152">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





