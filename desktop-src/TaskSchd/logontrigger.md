---
title: LogonTrigger 物件
description: 代表觸發程式的腳本物件，此觸發程式會在使用者登入時啟動工作。
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- 登入觸發程式工作排程器，物件
- LogonTrigger 物件工作排程器
- LogonTrigger 物件工作排程器，說明
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934674"
---
# <a name="logontrigger-object"></a><span data-ttu-id="4fa03-106">LogonTrigger 物件</span><span class="sxs-lookup"><span data-stu-id="4fa03-106">LogonTrigger object</span></span>

<span data-ttu-id="4fa03-107">代表觸發程式的腳本物件，此觸發程式會在使用者登入時啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4fa03-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="4fa03-108">當工作排程器服務啟動時，系統會列舉所有登入的使用者，並執行與登入的使用者相符之登入觸發程式所註冊的任何工作。</span><span class="sxs-lookup"><span data-stu-id="4fa03-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="4fa03-109">成員</span><span class="sxs-lookup"><span data-stu-id="4fa03-109">Members</span></span>

<span data-ttu-id="4fa03-110">**LogonTrigger** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4fa03-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="4fa03-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4fa03-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fa03-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4fa03-112">Properties</span></span>

<span data-ttu-id="4fa03-113">**LogonTrigger** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa03-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="4fa03-114">屬性</span><span class="sxs-lookup"><span data-stu-id="4fa03-114">Property</span></span>                                                            | <span data-ttu-id="4fa03-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="4fa03-115">Access type</span></span>           | <span data-ttu-id="4fa03-116">Description</span><span class="sxs-lookup"><span data-stu-id="4fa03-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fa03-117">**延遲**</span><span class="sxs-lookup"><span data-stu-id="4fa03-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="4fa03-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-118">Read/write</span></span><br/> | <span data-ttu-id="4fa03-119">取得或設定值，這個值表示使用者登入和工作啟動時間之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="4fa03-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="4fa03-120">**啟用**</span><span class="sxs-lookup"><span data-stu-id="4fa03-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="4fa03-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-121">Read/write</span></span><br/> | <span data-ttu-id="4fa03-122">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-123">取得或設定布林值，這個值會指出是否已啟用觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4fa03-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="4fa03-124">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="4fa03-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="4fa03-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-125">Read/write</span></span><br/> | <span data-ttu-id="4fa03-126">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-127">取得或設定停用觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4fa03-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="4fa03-128">觸發程式在停用之後無法啟動工作。</span><span class="sxs-lookup"><span data-stu-id="4fa03-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="4fa03-129">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="4fa03-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="4fa03-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-130">Read/write</span></span><br/> | <span data-ttu-id="4fa03-131">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-132">取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="4fa03-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="4fa03-133">**Id**</span><span class="sxs-lookup"><span data-stu-id="4fa03-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="4fa03-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-134">Read/write</span></span><br/> | <span data-ttu-id="4fa03-135">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-136">取得或設定觸發程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fa03-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="4fa03-137">**重複**</span><span class="sxs-lookup"><span data-stu-id="4fa03-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="4fa03-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-138">Read/write</span></span><br/> | <span data-ttu-id="4fa03-139">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-140">取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="4fa03-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="4fa03-141">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="4fa03-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="4fa03-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-142">Read/write</span></span><br/> | <span data-ttu-id="4fa03-143">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-144">取得或設定啟動觸發程式的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4fa03-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="4fa03-145">**類型**</span><span class="sxs-lookup"><span data-stu-id="4fa03-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="4fa03-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="4fa03-146">Read-only</span></span><br/>  | <span data-ttu-id="4fa03-147">繼承自 [**觸發**](trigger.md) 程式物件。</span><span class="sxs-lookup"><span data-stu-id="4fa03-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="4fa03-148">取得觸發程式的類型。</span><span class="sxs-lookup"><span data-stu-id="4fa03-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="4fa03-149">**UserId**</span><span class="sxs-lookup"><span data-stu-id="4fa03-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="4fa03-150">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4fa03-150">Read/write</span></span><br/> | <span data-ttu-id="4fa03-151">取得或設定使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4fa03-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="4fa03-152">備註</span><span class="sxs-lookup"><span data-stu-id="4fa03-152">Remarks</span></span>

<span data-ttu-id="4fa03-153">如果您想要在群組的任何成員登入電腦而非特定使用者登入時觸發工作，則不要將值指派給 [**LogonTrigger。 UserId**](logontrigger-userid.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4fa03-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="4fa03-154">相反地，請使用 **LogonTrigger 的 UserId** 屬性建立登入觸發程式，並使用 [**principal**](principal-groupid.md) 屬性將值指派給工作的主體。</span><span class="sxs-lookup"><span data-stu-id="4fa03-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="4fa03-155">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) 元素來指定登入觸發程式。</span><span class="sxs-lookup"><span data-stu-id="4fa03-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="4fa03-156">範例</span><span class="sxs-lookup"><span data-stu-id="4fa03-156">Examples</span></span>

<span data-ttu-id="4fa03-157">如需此腳本物件的詳細資訊和程式碼範例，請參閱 [登入觸發程式範例 (腳本) ](logon-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="4fa03-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa03-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fa03-158">Requirements</span></span>



| <span data-ttu-id="4fa03-159">需求</span><span class="sxs-lookup"><span data-stu-id="4fa03-159">Requirement</span></span> | <span data-ttu-id="4fa03-160">值</span><span class="sxs-lookup"><span data-stu-id="4fa03-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa03-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fa03-161">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa03-162">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fa03-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4fa03-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fa03-163">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa03-164">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fa03-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fa03-165">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4fa03-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fa03-166"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4fa03-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4fa03-167">DLL</span><span class="sxs-lookup"><span data-stu-id="4fa03-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fa03-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fa03-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa03-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fa03-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa03-170">**觸發**</span><span class="sxs-lookup"><span data-stu-id="4fa03-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





