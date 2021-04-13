---
title: MonthlyDOWTrigger. WeeksOfMonth 屬性
description: 針對腳本，取得或設定工作執行的月份周數。
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- WeeksOfMonth 屬性工作排程器
- WeeksOfMonth 屬性工作排程器，MonthlyDOWTrigger 物件
- MonthlyDOWTrigger 物件工作排程器、WeeksOfMonth 屬性
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464701"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a><span data-ttu-id="8289a-106">MonthlyDOWTrigger. WeeksOfMonth 屬性</span><span class="sxs-lookup"><span data-stu-id="8289a-106">MonthlyDOWTrigger.WeeksOfMonth property</span></span>

<span data-ttu-id="8289a-107">針對腳本，取得或設定工作執行的月份周數。</span><span class="sxs-lookup"><span data-stu-id="8289a-107">For scripting, gets or sets the weeks of the month during which the task runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="8289a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8289a-108">Syntax</span></span>


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a><span data-ttu-id="8289a-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8289a-109">Property value</span></span>

<span data-ttu-id="8289a-110">位元遮罩，表示工作在一周中的哪幾天執行。</span><span class="sxs-lookup"><span data-stu-id="8289a-110">A bitwise mask that indicates the days of the week during which the task runs.</span></span>

## <a name="remarks"></a><span data-ttu-id="8289a-111">備註</span><span class="sxs-lookup"><span data-stu-id="8289a-111">Remarks</span></span>

<span data-ttu-id="8289a-112">下表顯示這個屬性所使用之位元遮罩的對應。</span><span class="sxs-lookup"><span data-stu-id="8289a-112">The following table shows the mapping of the bitwise mask used by this property.</span></span>



| <span data-ttu-id="8289a-113">週</span><span class="sxs-lookup"><span data-stu-id="8289a-113">Week</span></span>                     | <span data-ttu-id="8289a-114">十六進位值</span><span class="sxs-lookup"><span data-stu-id="8289a-114">Hex Value</span></span> | <span data-ttu-id="8289a-115">十進位值</span><span class="sxs-lookup"><span data-stu-id="8289a-115">Decimal Value</span></span> |
|--------------------------|-----------|---------------|
| <span data-ttu-id="8289a-116">每月第一周</span><span class="sxs-lookup"><span data-stu-id="8289a-116">First week of the month</span></span>  | <span data-ttu-id="8289a-117">0X01</span><span class="sxs-lookup"><span data-stu-id="8289a-117">0X01</span></span>      | <span data-ttu-id="8289a-118">1</span><span class="sxs-lookup"><span data-stu-id="8289a-118">1</span></span>             |
| <span data-ttu-id="8289a-119">當月的第二周</span><span class="sxs-lookup"><span data-stu-id="8289a-119">Second week of the month</span></span> | <span data-ttu-id="8289a-120">0x02</span><span class="sxs-lookup"><span data-stu-id="8289a-120">0x02</span></span>      | <span data-ttu-id="8289a-121">2</span><span class="sxs-lookup"><span data-stu-id="8289a-121">2</span></span>             |
| <span data-ttu-id="8289a-122">當月的第三周</span><span class="sxs-lookup"><span data-stu-id="8289a-122">Third week of the month</span></span>  | <span data-ttu-id="8289a-123">0X04</span><span class="sxs-lookup"><span data-stu-id="8289a-123">0X04</span></span>      | <span data-ttu-id="8289a-124">4</span><span class="sxs-lookup"><span data-stu-id="8289a-124">4</span></span>             |
| <span data-ttu-id="8289a-125">每月第四周</span><span class="sxs-lookup"><span data-stu-id="8289a-125">Fourth week of the month</span></span> | <span data-ttu-id="8289a-126">0X08</span><span class="sxs-lookup"><span data-stu-id="8289a-126">0X08</span></span>      | <span data-ttu-id="8289a-127">8</span><span class="sxs-lookup"><span data-stu-id="8289a-127">8</span></span>             |



 

<span data-ttu-id="8289a-128">讀取或寫入工作的 XML 時，每週的每月星期幾日曆中的天數是由 [**week 元素所**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) 指定。</span><span class="sxs-lookup"><span data-stu-id="8289a-128">When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the [**Weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8289a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8289a-129">Requirements</span></span>



| <span data-ttu-id="8289a-130">需求</span><span class="sxs-lookup"><span data-stu-id="8289a-130">Requirement</span></span> | <span data-ttu-id="8289a-131">值</span><span class="sxs-lookup"><span data-stu-id="8289a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8289a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8289a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8289a-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8289a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8289a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8289a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8289a-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8289a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8289a-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8289a-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="8289a-137"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8289a-137"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8289a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8289a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8289a-139"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8289a-139"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8289a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8289a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8289a-141">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="8289a-141">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> <dt>

[<span data-ttu-id="8289a-142">工作排程器</span><span class="sxs-lookup"><span data-stu-id="8289a-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





