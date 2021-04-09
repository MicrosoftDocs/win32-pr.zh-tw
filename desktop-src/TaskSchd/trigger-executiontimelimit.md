---
title: Trigger.ExecutionTimeLimit 屬性
description: 針對腳本，取得或設定允許執行觸發程式之工作的最大時間量。
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- ExecutionTimeLimit 屬性工作排程器
- ExecutionTimeLimit 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，ExecutionTimeLimit 屬性
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934135"
---
# <a name="triggerexecutiontimelimit-property"></a><span data-ttu-id="5cee5-106">Trigger.ExecutionTimeLimit 屬性</span><span class="sxs-lookup"><span data-stu-id="5cee5-106">Trigger.ExecutionTimeLimit property</span></span>

<span data-ttu-id="5cee5-107">針對腳本，取得或設定允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="5cee5-107">For scripting, gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cee5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cee5-108">Syntax</span></span>


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="5cee5-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="5cee5-109">Property value</span></span>

<span data-ttu-id="5cee5-110">允許執行觸發程式之工作的最大時間量。</span><span class="sxs-lookup"><span data-stu-id="5cee5-110">The maximum amount of time that the task launched by the trigger is allowed to run.</span></span> <span data-ttu-id="5cee5-111">此字串的格式為 PnYnMnDTnHnMnS，其中 nY 是年數，nM 是月數，nD 是天數、t ' 是日期/時間分隔符號、nH 是時數、nM 為分鐘數，而 nS 是以秒為單位的秒數，例如，PT5M 指定 (5 分鐘，P1M4DT2H5M 指定一個月、四天、兩小時和五分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="5cee5-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cee5-112">備註</span><span class="sxs-lookup"><span data-stu-id="5cee5-112">Remarks</span></span>

<span data-ttu-id="5cee5-113">讀取或寫入工作的 XML 時，會在工作排程器架構的 [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) 元素中指定執行時間限制。</span><span class="sxs-lookup"><span data-stu-id="5cee5-113">When reading or writing XML for a task, the execution time limit is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cee5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cee5-114">Requirements</span></span>



| <span data-ttu-id="5cee5-115">需求</span><span class="sxs-lookup"><span data-stu-id="5cee5-115">Requirement</span></span> | <span data-ttu-id="5cee5-116">值</span><span class="sxs-lookup"><span data-stu-id="5cee5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cee5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cee5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5cee5-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cee5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5cee5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cee5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5cee5-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cee5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5cee5-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5cee5-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="5cee5-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5cee5-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5cee5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5cee5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cee5-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cee5-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cee5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cee5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cee5-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="5cee5-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





