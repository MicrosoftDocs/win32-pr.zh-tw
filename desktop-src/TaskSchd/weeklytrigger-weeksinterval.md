---
title: WeeklyTrigger. WeeksInterval 屬性
description: 針對腳本，取得或設定排程中周之間的間隔。
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- WeeksInterval 屬性工作排程器
- WeeksInterval 屬性工作排程器，WeeklyTrigger 物件
- WeeklyTrigger 物件工作排程器、WeeksInterval 屬性
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965700"
---
# <a name="weeklytriggerweeksinterval-property"></a><span data-ttu-id="2f65a-106">WeeklyTrigger. WeeksInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="2f65a-106">WeeklyTrigger.WeeksInterval property</span></span>

<span data-ttu-id="2f65a-107">針對腳本，取得或設定排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="2f65a-107">For scripting, gets or sets the interval between the weeks in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f65a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f65a-108">Syntax</span></span>


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a><span data-ttu-id="2f65a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="2f65a-109">Property value</span></span>

<span data-ttu-id="2f65a-110">排程中周之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="2f65a-110">The interval between the weeks in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f65a-111">備註</span><span class="sxs-lookup"><span data-stu-id="2f65a-111">Remarks</span></span>

<span data-ttu-id="2f65a-112">間隔1會產生每週排程。</span><span class="sxs-lookup"><span data-stu-id="2f65a-112">An interval of 1 produces a weekly schedule.</span></span> <span data-ttu-id="2f65a-113">間隔2會產生每隔一周的排程。</span><span class="sxs-lookup"><span data-stu-id="2f65a-113">An interval of 2 produces an every-other week schedule.</span></span>

<span data-ttu-id="2f65a-114">針對工作讀取或撰寫您自己的 XML 時，每週排程的間隔是使用工作排程器架構的 [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) 元素來指定。</span><span class="sxs-lookup"><span data-stu-id="2f65a-114">When reading or writing your own XML for a task, the interval for a weekly schedule is specified using the [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f65a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f65a-115">Requirements</span></span>



| <span data-ttu-id="2f65a-116">需求</span><span class="sxs-lookup"><span data-stu-id="2f65a-116">Requirement</span></span> | <span data-ttu-id="2f65a-117">值</span><span class="sxs-lookup"><span data-stu-id="2f65a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f65a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f65a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f65a-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f65a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f65a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f65a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f65a-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f65a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f65a-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2f65a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f65a-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2f65a-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2f65a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2f65a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f65a-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f65a-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f65a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f65a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f65a-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="2f65a-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





