---
description: 您可以建立一個計時器事件，方法是 \_ \_ 在任何 WMI 命名空間中建立衍生自 TimerInstruction 類別的類別實例。
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: 使用 __TimerInstruction 建立計時器事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e502678525569dae272edb7b03c0916db25edfd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194708"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a><span data-ttu-id="550fc-103">使用 TimerInstruction 建立計時器事件 \_ \_</span><span class="sxs-lookup"><span data-stu-id="550fc-103">Creating a Timer Event with \_\_TimerInstruction</span></span>

<span data-ttu-id="550fc-104">您可以建立一個計時器事件，方法是在任何 WMI 命名空間中建立衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)類別的類別實例。</span><span class="sxs-lookup"><span data-stu-id="550fc-104">You create a timer event by creating an instance of classes derived from the [**\_\_TimerInstruction**](--timerinstruction.md) class in any WMI namespace.</span></span> <span data-ttu-id="550fc-105">WMI 接著會在適當的時間產生計時器事件。</span><span class="sxs-lookup"><span data-stu-id="550fc-105">WMI then generates the timer event at the appropriate time.</span></span> <span data-ttu-id="550fc-106">如果您因為電腦停機而錯過了計時器事件，WMI 會通知您遺漏的事件。</span><span class="sxs-lookup"><span data-stu-id="550fc-106">If you miss a timer event due to computer downtime, WMI notifies you about the missed event.</span></span> <span data-ttu-id="550fc-107">WMI 支援計時器事件以提供回溯相容性，以及適用于您必須知道自從上一個傳遞事件以來已錯過多少事件的情況。</span><span class="sxs-lookup"><span data-stu-id="550fc-107">WMI supports timer events for backward compatibility and for scenarios where you must know how many events you have missed since the last delivered event.</span></span> <span data-ttu-id="550fc-108">但是針對大部分的計時器事件，您應該建立 [**win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) 或 [**win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)的事件篩選。</span><span class="sxs-lookup"><span data-stu-id="550fc-108">For most timer events, however, you should create an event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime).</span></span> <span data-ttu-id="550fc-109">如需詳細資訊，請參閱 [使用 win32 \_ LocalTime 或 Win32 \_ UTCTime 建立計時器事件](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)。</span><span class="sxs-lookup"><span data-stu-id="550fc-109">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span>

<span data-ttu-id="550fc-110">下列程式描述如何使用 TimerInstruction 建立及接收計時器事件 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="550fc-110">The following procedure describes how to create and receive a timer event with \_\_TimerInstruction.</span></span>

<span data-ttu-id="550fc-111">**使用 TimerInstruction 建立和接收計時器事件 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="550fc-111">**To create and receive a timer event with \_\_TimerInstruction**</span></span>

1.  <span data-ttu-id="550fc-112">建立 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)或 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="550fc-112">Create an instance of the [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md) or [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md) classes.</span></span>

    <span data-ttu-id="550fc-113">[**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)和 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)類別衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)類別，該類別包含唯一的開發人員指派的字串，可識別計時器事件的類型。</span><span class="sxs-lookup"><span data-stu-id="550fc-113">The [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md) and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md) classes are derived from the [**\_\_TimerInstruction**](--timerinstruction.md) class, which contains a unique developer-assigned string that identifies the type of timer event.</span></span> <span data-ttu-id="550fc-114">**\_ \_ TimerInstruction** 類別也包含一個值，這個值會指定當 wmi 無法使用時，wmi 是否應該傳送 belated 通知。</span><span class="sxs-lookup"><span data-stu-id="550fc-114">The **\_\_TimerInstruction** class also contains a value that specifies whether WMI should send a belated notification if the timer event occurs when WMI is unavailable.</span></span>

    <span data-ttu-id="550fc-115">使用 [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md)來傳送絕對計時器事件，此事件會在特定時間于特定日期發生。</span><span class="sxs-lookup"><span data-stu-id="550fc-115">Use [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md) to send absolute timer events, which occur on a specific date at a specific time.</span></span> <span data-ttu-id="550fc-116">使用 [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md)傳送間隔計時器事件，這會定期發生。</span><span class="sxs-lookup"><span data-stu-id="550fc-116">Use [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md) to send interval timer events, which occur on a regular basis.</span></span>

2.  <span data-ttu-id="550fc-117">設定您的應用程式以接收 [**\_ \_ TimerEvent**](--timerevent.md)實例。</span><span class="sxs-lookup"><span data-stu-id="550fc-117">Set your application to receive a [**\_\_TimerEvent**](--timerevent.md) instance.</span></span>

    <span data-ttu-id="550fc-118">為了產生事件，WMI 會建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例，並將實例轉送至您的取用者。</span><span class="sxs-lookup"><span data-stu-id="550fc-118">To generate an event, WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class and forwards the instance to your consumer.</span></span> <span data-ttu-id="550fc-119">**\_ \_ TimerEvent** 實例包含取用者的計時器指令識別碼。</span><span class="sxs-lookup"><span data-stu-id="550fc-119">The **\_\_TimerEvent** instance contains the timer instruction identifier from the consumer.</span></span> <span data-ttu-id="550fc-120">此實例也包含值，指定 wmi 無法觸達取用者時，WMI 應該在任何間隔期間傳送計時器事件通知的次數。</span><span class="sxs-lookup"><span data-stu-id="550fc-120">The instance also contains a value that specifies how many times WMI should send the timer event notification during any interval when WMI cannot reach the consumer.</span></span>

 

 
