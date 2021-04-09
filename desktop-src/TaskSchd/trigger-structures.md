---
title: 工作排程器1.0 的觸發程式結構
description: 工作排程器1.0 會使用數個結構來定義觸發程式的準則。
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021580"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="a145c-103">工作排程器1.0 的觸發程式結構</span><span class="sxs-lookup"><span data-stu-id="a145c-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="a145c-104">工作排程器1.0 會使用數個結構來定義觸發程式的準則。</span><span class="sxs-lookup"><span data-stu-id="a145c-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="a145c-105">如需工作排程器2.0 觸發程式的詳細資訊，請參閱 [觸發程式介面](trigger-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="a145c-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="a145c-106">工作排程器1.0 結構</span><span class="sxs-lookup"><span data-stu-id="a145c-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="a145c-107">下圖顯示工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。</span><span class="sxs-lookup"><span data-stu-id="a145c-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="a145c-108">它有三個必要的成員 (在建立新的觸發程式時必須設定的 **wBeginYear**、 **wBeginMonth** 和 **wBeginDay**) 。</span><span class="sxs-lookup"><span data-stu-id="a145c-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="a145c-109"> (跳到此結構的參考頁面，請按一下圖例中的結構名稱。 ) </span><span class="sxs-lookup"><span data-stu-id="a145c-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![工作觸發程式結構](images/tsktri1.png)

<span data-ttu-id="a145c-111">請注意， **TriggerType** 成員使用工作 [**觸發程式 \_ \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 列舉，而 **類型** 成員使用工作觸發程式聯 **\_ \_ 集** 結構。</span><span class="sxs-lookup"><span data-stu-id="a145c-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="a145c-112">工作 **\_ 觸發程式 \_ 類型** 列舉是用來指定觸發程式的類型 (事件和以時間為基礎的觸發程式類型) 。</span><span class="sxs-lookup"><span data-stu-id="a145c-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="a145c-113">[**觸發程式 \_ 類型聯 \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union)結構是用來合併 [**每日**](/windows/desktop/api/Mstask/ns-mstask-daily)、[**每週**](/windows/desktop/api/Mstask/ns-mstask-weekly)、 [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (日的月份) ，以及 [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (星期幾) 結構，用來指定何時會引發以時間為基礎的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="a145c-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="a145c-114">如果 **TriggerType** 指定以時間為基礎的觸發程式或以事件為基礎的觸發程式，則會忽略 **類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="a145c-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="a145c-115">只有當 **TriggerType** 成員指定每日、每週、每月或每週的時間型觸發程式時，才會使用 [**觸發型別聯 \_ \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union)結構。</span><span class="sxs-lookup"><span data-stu-id="a145c-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="a145c-116">此外， **類型** 成員的設定會指出要使用的 [**觸發程式類型聯 \_ \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="a145c-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="a145c-117">下圖顯示工作 [**\_ 觸發程式 \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 列舉值與 **觸發程式 \_ 類型 \_ 結構** 結構的成員之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="a145c-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="a145c-118"> (跳至這些結構的參考頁面，請按一下圖例中的結構名稱。 ) </span><span class="sxs-lookup"><span data-stu-id="a145c-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![工作觸發程式類型列舉值與觸發程式類型結構結構成員之間的關聯性](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="a145c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="a145c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a145c-121">工作觸發程式</span><span class="sxs-lookup"><span data-stu-id="a145c-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="a145c-122">觸發程式類型</span><span class="sxs-lookup"><span data-stu-id="a145c-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="a145c-123">觸發程式介面</span><span class="sxs-lookup"><span data-stu-id="a145c-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




