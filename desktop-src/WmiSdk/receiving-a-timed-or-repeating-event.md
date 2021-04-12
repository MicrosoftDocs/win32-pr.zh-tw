---
description: 計時或重複事件是在某個特定時間和日期發生的事件，或定期重複發生的事件。 例如，事件可能會在2015年12月2日的午夜發生，或在星期二下午2:31 點發生一次。
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: 接收計時或重複事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192087"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="4023f-104">接收計時或重複事件</span><span class="sxs-lookup"><span data-stu-id="4023f-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="4023f-105">計時或重複事件是在某個特定時間和日期發生的事件，或定期重複發生的事件。</span><span class="sxs-lookup"><span data-stu-id="4023f-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="4023f-106">例如，事件可能會在2015年12月2日的午夜發生，或在星期二下午2:31 點發生一次。</span><span class="sxs-lookup"><span data-stu-id="4023f-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="4023f-107">下表列出用來建立計時或重複事件的不同類別。</span><span class="sxs-lookup"><span data-stu-id="4023f-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="4023f-108">類別</span><span class="sxs-lookup"><span data-stu-id="4023f-108">Class</span></span>                                                                                            | <span data-ttu-id="4023f-109">描述</span><span class="sxs-lookup"><span data-stu-id="4023f-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4023f-110">[**Win32 \_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)或 [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="4023f-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="4023f-111">標準 Microsoft 事件模型。</span><span class="sxs-lookup"><span data-stu-id="4023f-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="4023f-112">如需詳細資訊，請參閱 [使用 win32 \_ LocalTime 或 Win32 \_ UTCTime 建立計時器事件](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)。</span><span class="sxs-lookup"><span data-stu-id="4023f-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="4023f-113">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="4023f-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="4023f-114">舊版技術。</span><span class="sxs-lookup"><span data-stu-id="4023f-114">Legacy technique.</span></span><br/> <span data-ttu-id="4023f-115">如需詳細資訊，請參閱 [使用 \_ TimerInstruction 建立計時器事件](creating-a-timer-event-with---timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="4023f-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="4023f-116">如果您想要將工作或工作排程在特定時間或重複執行，請使用 [**Win32 \_ register-scheduledjob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) 類別和其方法。</span><span class="sxs-lookup"><span data-stu-id="4023f-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="4023f-117">此類別代表在命令視窗中使用 AT 命令建立的作業，從 **開始** 然後 **執行**，或從 **主控台** 中的 **排程** 工作。</span><span class="sxs-lookup"><span data-stu-id="4023f-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

