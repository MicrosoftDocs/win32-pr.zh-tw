---
title: Trigger。重複屬性
description: 針對腳本，取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- 重複屬性工作排程器
- 重複屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，重複屬性
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969767"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="d58c3-106">Trigger。重複屬性</span><span class="sxs-lookup"><span data-stu-id="d58c3-106">Trigger.Repetition property</span></span>

<span data-ttu-id="d58c3-107">針對腳本，取得或設定值，這個值會指出工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="d58c3-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="d58c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58c3-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="d58c3-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d58c3-109">Property value</span></span>

<span data-ttu-id="d58c3-110">[**RepetitionPattern**](repetitionpattern.md)物件，定義工作的執行頻率，以及在工作啟動之後重複模式重複的時間長度。</span><span class="sxs-lookup"><span data-stu-id="d58c3-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="d58c3-111">備註</span><span class="sxs-lookup"><span data-stu-id="d58c3-111">Remarks</span></span>

<span data-ttu-id="d58c3-112">針對工作讀取或撰寫您自己的 XML 時，會在工作排程器架構的 [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) 元素中指定觸發程式的重複模式。</span><span class="sxs-lookup"><span data-stu-id="d58c3-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d58c3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d58c3-113">Requirements</span></span>



| <span data-ttu-id="d58c3-114">需求</span><span class="sxs-lookup"><span data-stu-id="d58c3-114">Requirement</span></span> | <span data-ttu-id="d58c3-115">值</span><span class="sxs-lookup"><span data-stu-id="d58c3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d58c3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d58c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d58c3-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d58c3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d58c3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d58c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d58c3-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d58c3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d58c3-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d58c3-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d58c3-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d58c3-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d58c3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d58c3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d58c3-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d58c3-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d58c3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d58c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d58c3-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="d58c3-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d58c3-126">**RepetitionPattern**</span><span class="sxs-lookup"><span data-stu-id="d58c3-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





