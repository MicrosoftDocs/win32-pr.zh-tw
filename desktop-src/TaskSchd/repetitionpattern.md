---
title: RepetitionPattern 物件
description: 腳本物件，定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- 觸發程式工作排程器，重複模式物件
- 重複模式工作排程器，物件
- RepetitionPattern 物件工作排程器
- RepetitionPattern 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464813"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="74bf0-107">RepetitionPattern 物件</span><span class="sxs-lookup"><span data-stu-id="74bf0-107">RepetitionPattern object</span></span>

<span data-ttu-id="74bf0-108">腳本物件，定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="74bf0-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="74bf0-109">成員</span><span class="sxs-lookup"><span data-stu-id="74bf0-109">Members</span></span>

<span data-ttu-id="74bf0-110">**RepetitionPattern** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="74bf0-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="74bf0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="74bf0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74bf0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="74bf0-112">Properties</span></span>

<span data-ttu-id="74bf0-113">**RepetitionPattern** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="74bf0-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="74bf0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="74bf0-114">Property</span></span>                                                                    | <span data-ttu-id="74bf0-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="74bf0-115">Access type</span></span>           | <span data-ttu-id="74bf0-116">Description</span><span class="sxs-lookup"><span data-stu-id="74bf0-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74bf0-117">**持續時間**</span><span class="sxs-lookup"><span data-stu-id="74bf0-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="74bf0-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="74bf0-118">Read/write</span></span><br/> | <span data-ttu-id="74bf0-119">取得或設定重複模式的時間長度。</span><span class="sxs-lookup"><span data-stu-id="74bf0-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="74bf0-120">**間隔**</span><span class="sxs-lookup"><span data-stu-id="74bf0-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="74bf0-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="74bf0-121">Read/write</span></span><br/> | <span data-ttu-id="74bf0-122">取得或設定每次重新開機工作之間的時間量。</span><span class="sxs-lookup"><span data-stu-id="74bf0-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="74bf0-123">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="74bf0-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="74bf0-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="74bf0-124">Read/write</span></span><br/> | <span data-ttu-id="74bf0-125">取得或設定布林值，這個值表示是否在重複模式期間結束時停止正在執行的工作實例。</span><span class="sxs-lookup"><span data-stu-id="74bf0-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74bf0-126">備註</span><span class="sxs-lookup"><span data-stu-id="74bf0-126">Remarks</span></span>

<span data-ttu-id="74bf0-127">如果您指定工作的重複持續時間，您也必須指定重複間隔。</span><span class="sxs-lookup"><span data-stu-id="74bf0-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="74bf0-128">如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動五次。</span><span class="sxs-lookup"><span data-stu-id="74bf0-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="74bf0-129">您可以使用下列模式來定義五次重複。</span><span class="sxs-lookup"><span data-stu-id="74bf0-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="74bf0-130">工作會在第一分鐘的開頭開始。</span><span class="sxs-lookup"><span data-stu-id="74bf0-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="74bf0-131">下一項工作會在第一分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="74bf0-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="74bf0-132">下一項工作會在第二分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="74bf0-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="74bf0-133">下一項工作會從第三分鐘的結尾開始。</span><span class="sxs-lookup"><span data-stu-id="74bf0-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="74bf0-134">下一項工作會在第四分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="74bf0-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="74bf0-135">**Windows Server 2003、WINDOWS XP 和 windows 2000：** 如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動四次。</span><span class="sxs-lookup"><span data-stu-id="74bf0-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="74bf0-136">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) 專案來指定重複模式。</span><span class="sxs-lookup"><span data-stu-id="74bf0-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="74bf0-137">範例</span><span class="sxs-lookup"><span data-stu-id="74bf0-137">Examples</span></span>

<span data-ttu-id="74bf0-138">如需此屬性的詳細資訊和範例程式碼，請參閱 [ (腳本) 的每日觸發程式範例 ](daily-trigger-example--scripting-.md)。</span><span class="sxs-lookup"><span data-stu-id="74bf0-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74bf0-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="74bf0-139">Requirements</span></span>



| <span data-ttu-id="74bf0-140">需求</span><span class="sxs-lookup"><span data-stu-id="74bf0-140">Requirement</span></span> | <span data-ttu-id="74bf0-141">值</span><span class="sxs-lookup"><span data-stu-id="74bf0-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74bf0-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74bf0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="74bf0-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74bf0-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="74bf0-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74bf0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="74bf0-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74bf0-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74bf0-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="74bf0-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="74bf0-147"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74bf0-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74bf0-148">DLL</span><span class="sxs-lookup"><span data-stu-id="74bf0-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74bf0-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74bf0-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74bf0-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74bf0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74bf0-151">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="74bf0-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="74bf0-152">工作排程器</span><span class="sxs-lookup"><span data-stu-id="74bf0-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





