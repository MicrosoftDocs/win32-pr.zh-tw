---
title: 重複工作
description: 工作排程器可以在引發觸發程式之後，任意次數執行一次工作。
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- 重複模式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301492"
---
# <a name="repeating-a-task"></a><span data-ttu-id="983ad-104">重複工作</span><span class="sxs-lookup"><span data-stu-id="983ad-104">Repeating A Task</span></span>

<span data-ttu-id="983ad-105">工作排程器可以在引發觸發程式之後，任意次數執行一次工作。</span><span class="sxs-lookup"><span data-stu-id="983ad-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="983ad-106">若要這樣做，此觸發程式會定義重複模式，告知工作排程器它應該繼續重複工作的時間，以及每個工作重複之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="983ad-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="983ad-107">重複模式</span><span class="sxs-lookup"><span data-stu-id="983ad-107">Repetition Pattern</span></span>

<span data-ttu-id="983ad-108">下圖顯示持續時間為60分鐘的重複模式，以及25分鐘的間隔。</span><span class="sxs-lookup"><span data-stu-id="983ad-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="983ad-109">請注意，在此情況下，工作排程器會在觸發程式引發時執行工作，它會在25分鐘之後再次執行工作，然後根據 IRepetitionPattern () [**RepetitionPattern**](repetitionpattern-stopatdurationend.md)的 [**StopAtDurationEnd 屬性**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend)設定，在50分鐘後再執行一次此工作。</span><span class="sxs-lookup"><span data-stu-id="983ad-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="983ad-110">如果 [ **StopAtDurationEnd** ] 屬性設定為 [True]，工作排程器在60分鐘後仍在執行時，停止工作的最後一個實例。</span><span class="sxs-lookup"><span data-stu-id="983ad-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="983ad-111">如果 **StopAtDurationEnd** 屬性設定為 False，就會執行工作的最後一個實例，而不管持續時間。</span><span class="sxs-lookup"><span data-stu-id="983ad-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![觸發重複模式](images/repetition-pattern.png)

<span data-ttu-id="983ad-113">如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動五次。</span><span class="sxs-lookup"><span data-stu-id="983ad-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="983ad-114">您可以使用下列模式來定義五次重複：</span><span class="sxs-lookup"><span data-stu-id="983ad-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="983ad-115">工作會在第一分鐘的開頭開始。</span><span class="sxs-lookup"><span data-stu-id="983ad-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="983ad-116">下一項工作會在第一分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="983ad-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="983ad-117">下一項工作會在第二分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="983ad-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="983ad-118">下一項工作會從第三分鐘的結尾開始。</span><span class="sxs-lookup"><span data-stu-id="983ad-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="983ad-119">下一項工作會在第四分鐘結束時啟動。</span><span class="sxs-lookup"><span data-stu-id="983ad-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="983ad-120">**Windows Server 2003、WINDOWS XP 和 windows 2000：** 如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動四次。</span><span class="sxs-lookup"><span data-stu-id="983ad-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="983ad-121">物件、介面和 XML 元素</span><span class="sxs-lookup"><span data-stu-id="983ad-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="983ad-122">針對開發腳本，會使用 [**RepetitionPattern**](repetitionpattern.md) 物件來定義重複模式。</span><span class="sxs-lookup"><span data-stu-id="983ad-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="983ad-123">針對 c + + 開發，重複模式是由 [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) 介面所定義。</span><span class="sxs-lookup"><span data-stu-id="983ad-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="983ad-124">讀取或寫入工作的 XML 時，重複的模式是在 [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) 專案中指定。</span><span class="sxs-lookup"><span data-stu-id="983ad-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="983ad-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="983ad-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="983ad-126">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="983ad-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




