---
title: Day (daysOfMonthType) 元素
description: 指定執行工作的月份日期。
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Day 元素工作排程器
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024824"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="701ec-104">Day (daysOfMonthType) 元素</span><span class="sxs-lookup"><span data-stu-id="701ec-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="701ec-105">指定執行工作的月份日期。</span><span class="sxs-lookup"><span data-stu-id="701ec-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="701ec-106">**Day** 元素是由 [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="701ec-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="701ec-107">父元素</span><span class="sxs-lookup"><span data-stu-id="701ec-107">Parent element</span></span>



| <span data-ttu-id="701ec-108">元素</span><span class="sxs-lookup"><span data-stu-id="701ec-108">Element</span></span>                                                                            | <span data-ttu-id="701ec-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="701ec-109">Derived from</span></span>                                                               | <span data-ttu-id="701ec-110">Description</span><span class="sxs-lookup"><span data-stu-id="701ec-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="701ec-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="701ec-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="701ec-112">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="701ec-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="701ec-113">指定工作執行的當月天數。</span><span class="sxs-lookup"><span data-stu-id="701ec-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="701ec-114">範例</span><span class="sxs-lookup"><span data-stu-id="701ec-114">Examples</span></span>

<span data-ttu-id="701ec-115">下列 XML 會定義每月日曆的日部分，其會在該月的1日和15日執行工作。</span><span class="sxs-lookup"><span data-stu-id="701ec-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="701ec-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="701ec-116">Requirements</span></span>



| <span data-ttu-id="701ec-117">需求</span><span class="sxs-lookup"><span data-stu-id="701ec-117">Requirement</span></span> | <span data-ttu-id="701ec-118">值</span><span class="sxs-lookup"><span data-stu-id="701ec-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="701ec-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="701ec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="701ec-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="701ec-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="701ec-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="701ec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="701ec-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="701ec-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="701ec-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="701ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701ec-124">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="701ec-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





