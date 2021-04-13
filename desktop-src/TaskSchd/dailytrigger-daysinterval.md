---
title: DailyTrigger. DaysInterval 屬性
description: 針對腳本，取得或設定排程中天數之間的間隔。
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- DaysInterval 屬性工作排程器
- DaysInterval 屬性工作排程器，DailyTrigger 物件
- DailyTrigger 物件工作排程器、DaysInterval 屬性
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6499f3b900fe10b2a2527c2e2ee675cca3151204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508667"
---
# <a name="dailytriggerdaysinterval-property"></a><span data-ttu-id="12e00-106">DailyTrigger. DaysInterval 屬性</span><span class="sxs-lookup"><span data-stu-id="12e00-106">DailyTrigger.DaysInterval property</span></span>

<span data-ttu-id="12e00-107">針對腳本，取得或設定排程中天數之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="12e00-107">For scripting, gets or sets the interval between the days in the schedule.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e00-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e00-108">Syntax</span></span>


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a><span data-ttu-id="12e00-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="12e00-109">Property value</span></span>

<span data-ttu-id="12e00-110">排程中天數之間的間隔。</span><span class="sxs-lookup"><span data-stu-id="12e00-110">The interval between the days in the schedule.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e00-111">備註</span><span class="sxs-lookup"><span data-stu-id="12e00-111">Remarks</span></span>

<span data-ttu-id="12e00-112">間隔1會產生每日排程。</span><span class="sxs-lookup"><span data-stu-id="12e00-112">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="12e00-113">間隔2會產生每隔一天的排程。</span><span class="sxs-lookup"><span data-stu-id="12e00-113">An interval of 2 produces an every-other day schedule.</span></span>

<span data-ttu-id="12e00-114">針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) 元素來指定每日排程的間隔。</span><span class="sxs-lookup"><span data-stu-id="12e00-114">When reading or writing your own XML for a task, the interval for a daily schedule is specified using the [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="12e00-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="12e00-115">Requirements</span></span>



| <span data-ttu-id="12e00-116">需求</span><span class="sxs-lookup"><span data-stu-id="12e00-116">Requirement</span></span> | <span data-ttu-id="12e00-117">值</span><span class="sxs-lookup"><span data-stu-id="12e00-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12e00-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12e00-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12e00-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12e00-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12e00-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12e00-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12e00-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12e00-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12e00-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="12e00-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="12e00-123"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12e00-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12e00-124">DLL</span><span class="sxs-lookup"><span data-stu-id="12e00-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e00-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e00-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e00-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e00-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="12e00-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="12e00-128">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="12e00-128">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> </dl>

 

 





