---
title: '我 (工作排程器) '
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508228"
---
# <a name="i-task-scheduler"></a><span data-ttu-id="23bd4-103">我 (工作排程器) </span><span class="sxs-lookup"><span data-stu-id="23bd4-103">I (Task Scheduler)</span></span>

<span data-ttu-id="23bd4-104">B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="23bd4-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="23bd4-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**閒置條件**</span><span class="sxs-lookup"><span data-stu-id="23bd4-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="23bd4-106">電腦上沒有使用者輸入的一段時間。</span><span class="sxs-lookup"><span data-stu-id="23bd4-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="23bd4-107">閒置條件與工作的排程開始時間相關聯。</span><span class="sxs-lookup"><span data-stu-id="23bd4-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="23bd4-108">這些條件是透過呼叫 [**IScheduledWorkItem：： SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags)來設定。</span><span class="sxs-lookup"><span data-stu-id="23bd4-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="23bd4-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**閒置觸發程式**</span><span class="sxs-lookup"><span data-stu-id="23bd4-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="23bd4-110">以事件為基礎的觸發程式，當電腦閒置一段特定的時間時就會引發。</span><span class="sxs-lookup"><span data-stu-id="23bd4-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="23bd4-111">閒置觸發程式的建立方式，是將 \_ 工作觸發程式結構的工作觸發程式 \_ 類型成員設定為 [**\_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) \_ \_ 閒置時的 task 事件觸發程式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="23bd4-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="23bd4-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**閒置等候時間**</span><span class="sxs-lookup"><span data-stu-id="23bd4-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="23bd4-113">閒置觸發程式或閒置條件所使用的時間間隔 (分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="23bd4-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="23bd4-114">閒置觸發程式是以事件為基礎的觸發程式，不會與排程的時間相關聯。</span><span class="sxs-lookup"><span data-stu-id="23bd4-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="23bd4-115">閒置條件與工作的排程開始時間相關聯。</span><span class="sxs-lookup"><span data-stu-id="23bd4-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="23bd4-116">閒置時間是透過呼叫 [**IScheduledWorkItem：： SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait)來設定。</span><span class="sxs-lookup"><span data-stu-id="23bd4-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




