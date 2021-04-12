---
title: TaskSettings. DeleteExpiredTaskAfter 屬性
description: 針對腳本，取得或設定在工作到期之後，工作排程器將等待的時間量。
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- DeleteExpiredTaskAfter 屬性工作排程器
- DeleteExpiredTaskAfter 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、DeleteExpiredTaskAfter 屬性
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464801"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="e08f1-106">TaskSettings. DeleteExpiredTaskAfter 屬性</span><span class="sxs-lookup"><span data-stu-id="e08f1-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="e08f1-107">針對腳本，取得或設定在工作到期之後，工作排程器將等待的時間量。</span><span class="sxs-lookup"><span data-stu-id="e08f1-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="e08f1-108">如果未指定這個屬性的值，工作排程器服務將不會刪除該工作。</span><span class="sxs-lookup"><span data-stu-id="e08f1-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="e08f1-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e08f1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08f1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e08f1-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="e08f1-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="e08f1-111">Property value</span></span>

<span data-ttu-id="e08f1-112">字串，這個字串會取得或設定工作排程器在工作到期之後刪除工作的等待時間量。</span><span class="sxs-lookup"><span data-stu-id="e08f1-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="e08f1-113">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="e08f1-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="e08f1-114">備註</span><span class="sxs-lookup"><span data-stu-id="e08f1-114">Remarks</span></span>

<span data-ttu-id="e08f1-115">當所有與工作相關聯的觸發程式都超過結束界限之後，工作就會過期。</span><span class="sxs-lookup"><span data-stu-id="e08f1-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="e08f1-116">觸發程式的結束界限是由所有觸發程式物件所繼承的 [EndBoundary](trigger-endboundary.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="e08f1-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="e08f1-117">讀取或寫入工作的 XML 時，此設定會指定在工作排程器架構的 [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) 元素中。</span><span class="sxs-lookup"><span data-stu-id="e08f1-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08f1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e08f1-118">Requirements</span></span>



| <span data-ttu-id="e08f1-119">需求</span><span class="sxs-lookup"><span data-stu-id="e08f1-119">Requirement</span></span> | <span data-ttu-id="e08f1-120">值</span><span class="sxs-lookup"><span data-stu-id="e08f1-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e08f1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e08f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e08f1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e08f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e08f1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e08f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e08f1-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e08f1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e08f1-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e08f1-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e08f1-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e08f1-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e08f1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e08f1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08f1-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08f1-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08f1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e08f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08f1-130">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e08f1-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





