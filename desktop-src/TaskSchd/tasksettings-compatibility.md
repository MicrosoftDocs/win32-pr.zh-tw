---
title: TaskSettings 相容性屬性
description: 若為腳本，取得或設定整數值，這個值表示與工作相容的工作排程器版本。
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- 相容性屬性工作排程器
- 相容性屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器，相容性屬性
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685736"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="2601f-106">TaskSettings 相容性屬性</span><span class="sxs-lookup"><span data-stu-id="2601f-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="2601f-107">若為腳本，取得或設定整數值，這個值表示與工作相容的工作排程器版本。</span><span class="sxs-lookup"><span data-stu-id="2601f-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="2601f-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2601f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2601f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2601f-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="2601f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2601f-110">Property value</span></span>



| <span data-ttu-id="2601f-111">值</span><span class="sxs-lookup"><span data-stu-id="2601f-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="2601f-112">意義</span><span class="sxs-lookup"><span data-stu-id="2601f-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="2601f-113"><dt>**工作 \_相容 \_ 性**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="2601f-114">工作與 AT 命令相容。</span><span class="sxs-lookup"><span data-stu-id="2601f-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="2601f-115"><dt>**工作 \_相容性 \_ V1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2601f-116">工作與工作排程器1.0 相容。</span><span class="sxs-lookup"><span data-stu-id="2601f-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="2601f-117"><dt>**工作 \_相容性 \_ V2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="2601f-118">工作與工作排程器2.0 相容。</span><span class="sxs-lookup"><span data-stu-id="2601f-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2601f-119">備註</span><span class="sxs-lookup"><span data-stu-id="2601f-119">Remarks</span></span>

<span data-ttu-id="2601f-120">只有在[](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) \_ \_ 需要從 Windows XP、Windows Server 2003 或 windows 2000 電腦存取或修改工作時，才應該將工作相容性（透過 [相容性] 屬性設定）設定為 [工作相容性 V1]。</span><span class="sxs-lookup"><span data-stu-id="2601f-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="2601f-121">否則，建議使用工作排程器2.0 相容性，因為工作將會有更多功能。</span><span class="sxs-lookup"><span data-stu-id="2601f-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="2601f-122">與 AT 命令相容的工作只能有一個時間觸發程式。</span><span class="sxs-lookup"><span data-stu-id="2601f-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="2601f-123">與工作排程器1.0 相容的工作只能有時間觸發程式、登入觸發程式或開機觸發程式，且工作只能有可執行檔動作。</span><span class="sxs-lookup"><span data-stu-id="2601f-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="2601f-124">如需工作相容性的詳細資訊，請參閱工作排程器[和工作](tasks.md)[的新功能](what-s-new-in-task-scheduler.md)。</span><span class="sxs-lookup"><span data-stu-id="2601f-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2601f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2601f-125">Requirements</span></span>



| <span data-ttu-id="2601f-126">需求</span><span class="sxs-lookup"><span data-stu-id="2601f-126">Requirement</span></span> | <span data-ttu-id="2601f-127">值</span><span class="sxs-lookup"><span data-stu-id="2601f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2601f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2601f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2601f-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2601f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2601f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2601f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2601f-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2601f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2601f-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2601f-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="2601f-133"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2601f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2601f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2601f-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2601f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2601f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2601f-137">**工作 \_ 相容性**</span><span class="sxs-lookup"><span data-stu-id="2601f-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="2601f-138">工作排程器</span><span class="sxs-lookup"><span data-stu-id="2601f-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





