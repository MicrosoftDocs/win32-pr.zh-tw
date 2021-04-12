---
title: Actioncollection 動作物件
description: 包含工作所執行之動作的腳本物件。
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- 動作工作排程器，集合物件
- Actioncollection 動作物件工作排程器
- Actioncollection 動作物件工作排程器，說明
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509448"
---
# <a name="actioncollection-object"></a><span data-ttu-id="da2c9-106">Actioncollection 動作物件</span><span class="sxs-lookup"><span data-stu-id="da2c9-106">ActionCollection object</span></span>

<span data-ttu-id="da2c9-107">包含工作所執行之動作的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="da2c9-107">Scripting object that contains the actions performed by the task.</span></span>

## <a name="members"></a><span data-ttu-id="da2c9-108">成員</span><span class="sxs-lookup"><span data-stu-id="da2c9-108">Members</span></span>

<span data-ttu-id="da2c9-109">**Actioncollection 動作** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="da2c9-109">The **ActionCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="da2c9-110">方法</span><span class="sxs-lookup"><span data-stu-id="da2c9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="da2c9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="da2c9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da2c9-112">方法</span><span class="sxs-lookup"><span data-stu-id="da2c9-112">Methods</span></span>

<span data-ttu-id="da2c9-113">**Actioncollection 動作** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="da2c9-113">The **ActionCollection** object has these methods.</span></span>



| <span data-ttu-id="da2c9-114">方法</span><span class="sxs-lookup"><span data-stu-id="da2c9-114">Method</span></span>                                    | <span data-ttu-id="da2c9-115">描述</span><span class="sxs-lookup"><span data-stu-id="da2c9-115">Description</span></span>                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="da2c9-116">**清楚**</span><span class="sxs-lookup"><span data-stu-id="da2c9-116">**Clear**</span></span>](actioncollection-clear.md)   | <span data-ttu-id="da2c9-117">清除集合中的所有動作。</span><span class="sxs-lookup"><span data-stu-id="da2c9-117">Clears all the actions from the collection.</span></span><br/>      |
| [<span data-ttu-id="da2c9-118">**建立**</span><span class="sxs-lookup"><span data-stu-id="da2c9-118">**Create**</span></span>](actioncollection-create.md) | <span data-ttu-id="da2c9-119">建立新的動作，並將其加入至集合。</span><span class="sxs-lookup"><span data-stu-id="da2c9-119">Creates and adds a new action to the collection.</span></span><br/> |
| [<span data-ttu-id="da2c9-120">**移除**</span><span class="sxs-lookup"><span data-stu-id="da2c9-120">**Remove**</span></span>](actioncollection-remove.md) | <span data-ttu-id="da2c9-121">從集合中移除指定的動作。</span><span class="sxs-lookup"><span data-stu-id="da2c9-121">Removes a specified action from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="da2c9-122">屬性</span><span class="sxs-lookup"><span data-stu-id="da2c9-122">Properties</span></span>

<span data-ttu-id="da2c9-123">**Actioncollection 動作** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="da2c9-123">The **ActionCollection** object has these properties.</span></span>



| <span data-ttu-id="da2c9-124">屬性</span><span class="sxs-lookup"><span data-stu-id="da2c9-124">Property</span></span>                                               | <span data-ttu-id="da2c9-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="da2c9-125">Access type</span></span>           | <span data-ttu-id="da2c9-126">Description</span><span class="sxs-lookup"><span data-stu-id="da2c9-126">Description</span></span>                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="da2c9-127">**Context**</span><span class="sxs-lookup"><span data-stu-id="da2c9-127">**Context**</span></span>](actioncollection-context.md)<br/> | <span data-ttu-id="da2c9-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="da2c9-128">Read/write</span></span><br/> | <span data-ttu-id="da2c9-129">取得或設定工作主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="da2c9-129">Gets or sets the identifier of the principal for the task.</span></span><br/> |
| [<span data-ttu-id="da2c9-130">**計數**</span><span class="sxs-lookup"><span data-stu-id="da2c9-130">**Count**</span></span>](actioncollection-count.md)<br/>     | <span data-ttu-id="da2c9-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="da2c9-131">Read-only</span></span><br/>  | <span data-ttu-id="da2c9-132">取得集合中的動作數目。</span><span class="sxs-lookup"><span data-stu-id="da2c9-132">Gets the number of actions in the collection.</span></span><br/>              |
| [<span data-ttu-id="da2c9-133">**項目**</span><span class="sxs-lookup"><span data-stu-id="da2c9-133">**Item**</span></span>](actioncollection-item.md)<br/>       | <span data-ttu-id="da2c9-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="da2c9-134">Read-only</span></span><br/>  | <span data-ttu-id="da2c9-135">從集合中取得指定的動作。</span><span class="sxs-lookup"><span data-stu-id="da2c9-135">Gets a specified action from the collection.</span></span><br/>               |
| [<span data-ttu-id="da2c9-136">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="da2c9-136">**XmlText**</span></span>](actioncollection-xmltext.md)<br/> | <span data-ttu-id="da2c9-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="da2c9-137">Read/write</span></span><br/> | <span data-ttu-id="da2c9-138">取得或設定集合的 XML 格式版本。</span><span class="sxs-lookup"><span data-stu-id="da2c9-138">Gets or sets an XML-formatted version of the collection.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="da2c9-139">備註</span><span class="sxs-lookup"><span data-stu-id="da2c9-139">Remarks</span></span>

<span data-ttu-id="da2c9-140">讀取或寫入 XML 時，會在工作排程器架構的 [**actions**](taskschedulerschema-actions-tasktype-element.md) 元素中指定工作的動作。</span><span class="sxs-lookup"><span data-stu-id="da2c9-140">When reading or writing XML, the actions of a task are specified in the [**Actions**](taskschedulerschema-actions-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="da2c9-141">範例</span><span class="sxs-lookup"><span data-stu-id="da2c9-141">Examples</span></span>

<span data-ttu-id="da2c9-142">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)、 [事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、 [每日觸發程式範例 (腳本 ](daily-trigger-example--scripting-.md)) 、 [註冊觸發 ](registration-trigger-example--scripting-.md)程式範例 (腳本) 、 [的觸發程式 ](weekly-trigger-example--scripting-.md)範例、 [登入觸發 ](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或啟動觸發程式範例 [ (腳本) ](boot-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="da2c9-142">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md), [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da2c9-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="da2c9-143">Requirements</span></span>



| <span data-ttu-id="da2c9-144">需求</span><span class="sxs-lookup"><span data-stu-id="da2c9-144">Requirement</span></span> | <span data-ttu-id="da2c9-145">值</span><span class="sxs-lookup"><span data-stu-id="da2c9-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da2c9-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da2c9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="da2c9-147">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da2c9-147">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="da2c9-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da2c9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="da2c9-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da2c9-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da2c9-150">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="da2c9-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="da2c9-151"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da2c9-151"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da2c9-152">DLL</span><span class="sxs-lookup"><span data-stu-id="da2c9-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da2c9-153"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da2c9-153"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





