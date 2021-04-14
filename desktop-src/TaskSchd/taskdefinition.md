---
title: TaskDefinition 物件
description: 腳本物件，定義工作的所有元件，例如工作設定、觸發程式、動作和註冊資訊。
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- TaskDefinition 物件工作排程器
- TaskDefinition 物件工作排程器，說明
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508775"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="b5dd0-105">TaskDefinition 物件</span><span class="sxs-lookup"><span data-stu-id="b5dd0-105">TaskDefinition object</span></span>

<span data-ttu-id="b5dd0-106">腳本物件，定義工作的所有元件，例如工作設定、觸發程式、動作和註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="b5dd0-107">成員</span><span class="sxs-lookup"><span data-stu-id="b5dd0-107">Members</span></span>

<span data-ttu-id="b5dd0-108">**TaskDefinition** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5dd0-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="b5dd0-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b5dd0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5dd0-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b5dd0-110">Properties</span></span>

<span data-ttu-id="b5dd0-111">**TaskDefinition** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="b5dd0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b5dd0-112">Property</span></span>                                                               | <span data-ttu-id="b5dd0-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="b5dd0-113">Access type</span></span>           | <span data-ttu-id="b5dd0-114">Description</span><span class="sxs-lookup"><span data-stu-id="b5dd0-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5dd0-115">**行動**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="b5dd0-116">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-116">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-117">取得或設定工作所執行的動作集合。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="b5dd0-118">**資料**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="b5dd0-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-119">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-120">取得或設定與工作相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="b5dd0-121">工作排程器的服務會忽略這項資料，但想要擴充工作格式的協力廠商會使用此資料。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="b5dd0-122">**主要**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="b5dd0-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-123">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-124">取得或設定工作的主體，此工作會提供工作的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="b5dd0-125">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="b5dd0-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-126">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-127">取得或設定用來描述工作的註冊資訊，例如工作的描述、工作的作者，以及工作的註冊日期。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="b5dd0-128">**設定**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="b5dd0-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-129">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-130">取得或設定定義工作排程器服務如何執行工作的設定。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="b5dd0-131">**觸發程序**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="b5dd0-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-132">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-133">取得或設定用來啟動工作的觸發程式集合。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="b5dd0-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="b5dd0-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="b5dd0-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b5dd0-135">Read/write</span></span><br/> | <span data-ttu-id="b5dd0-136">取得或設定工作的 XML 格式化定義。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b5dd0-137">備註</span><span class="sxs-lookup"><span data-stu-id="b5dd0-137">Remarks</span></span>

<span data-ttu-id="b5dd0-138">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**task**](taskschedulerschema-task-element.md) 元素來指定工作定義。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b5dd0-139">範例</span><span class="sxs-lookup"><span data-stu-id="b5dd0-139">Examples</span></span>

<span data-ttu-id="b5dd0-140">如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md) 、 [事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、 [每日觸發程式範例 (腳本 ](daily-trigger-example--scripting-.md)) 、 [註冊觸發 ](registration-trigger-example--scripting-.md)程式範例 (腳本) 、 [的觸發程式 ](weekly-trigger-example--scripting-.md)範例、 [登入觸發 ](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或啟動觸發程式範例 [ (腳本) ](boot-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="b5dd0-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5dd0-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5dd0-141">Requirements</span></span>



| <span data-ttu-id="b5dd0-142">需求</span><span class="sxs-lookup"><span data-stu-id="b5dd0-142">Requirement</span></span> | <span data-ttu-id="b5dd0-143">值</span><span class="sxs-lookup"><span data-stu-id="b5dd0-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5dd0-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5dd0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b5dd0-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5dd0-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5dd0-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5dd0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b5dd0-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5dd0-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5dd0-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b5dd0-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5dd0-149"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5dd0-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5dd0-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b5dd0-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5dd0-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5dd0-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





