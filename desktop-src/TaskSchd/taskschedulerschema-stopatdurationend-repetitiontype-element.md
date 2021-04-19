---
title: StopAtDurationEnd (repetitionType) 元素
description: 指定在重複模式期間結束時停止執行中的工作實例。
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- StopAtDurationEnd 元素工作排程器
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967569"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="fa1d1-104">StopAtDurationEnd (repetitionType) 元素</span><span class="sxs-lookup"><span data-stu-id="fa1d1-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="fa1d1-105">指定在重複模式期間結束時停止執行中的工作實例。</span><span class="sxs-lookup"><span data-stu-id="fa1d1-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="fa1d1-106">這僅適用于已設定重複的情況。</span><span class="sxs-lookup"><span data-stu-id="fa1d1-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="fa1d1-107">**StopAtDurationEnd** 元素是由 [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="fa1d1-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fa1d1-108">父元素</span><span class="sxs-lookup"><span data-stu-id="fa1d1-108">Parent element</span></span>

| <span data-ttu-id="fa1d1-109">元素</span><span class="sxs-lookup"><span data-stu-id="fa1d1-109">Element</span></span> | <span data-ttu-id="fa1d1-110">衍生自</span><span class="sxs-lookup"><span data-stu-id="fa1d1-110">Derived from</span></span> | <span data-ttu-id="fa1d1-111">Description</span><span class="sxs-lookup"><span data-stu-id="fa1d1-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="fa1d1-112">**重複**</span><span class="sxs-lookup"><span data-stu-id="fa1d1-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="fa1d1-113">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="fa1d1-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="fa1d1-114">指定執行工作的頻率，以及啟動工作之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="fa1d1-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="fa1d1-115">備註</span><span class="sxs-lookup"><span data-stu-id="fa1d1-115">Remarks</span></span>

<span data-ttu-id="fa1d1-116">針對腳本開發，此設定會使用 [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="fa1d1-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="fa1d1-117">針對 c + + 開發，此設定會使用 [**IRepetitionPattern：： StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) 屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="fa1d1-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa1d1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa1d1-118">Requirements</span></span>

| <span data-ttu-id="fa1d1-119">需求</span><span class="sxs-lookup"><span data-stu-id="fa1d1-119">Requirement</span></span> | <span data-ttu-id="fa1d1-120">值</span><span class="sxs-lookup"><span data-stu-id="fa1d1-120">Value</span></span> |
|-|-|
| <span data-ttu-id="fa1d1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa1d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fa1d1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa1d1-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fa1d1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa1d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fa1d1-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa1d1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="fa1d1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa1d1-125">See also</span></span>

[<span data-ttu-id="fa1d1-126">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="fa1d1-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="fa1d1-127">工作排程器</span><span class="sxs-lookup"><span data-stu-id="fa1d1-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
