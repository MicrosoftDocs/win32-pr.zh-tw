---
title: 關於多媒體計時器
description: 關於多媒體計時器
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows 多媒體，計時器
- 多媒體、計時器
- 多媒體輸入，計時器
- 多媒體計時器，關於
- 計時器，關於
- 多媒體計時器，排程事件
- 計時器，排程事件
- 排程計時器事件
- 高解析度計時
- SetTimer 函式
- CreateWaitableTimer 函式
- WM_TIMER 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023413"
---
# <a name="about-multimedia-timers"></a><span data-ttu-id="f604d-115">關於多媒體計時器</span><span class="sxs-lookup"><span data-stu-id="f604d-115">About Multimedia Timers</span></span>

<span data-ttu-id="f604d-116">多媒體計時器服務可讓應用程式以最高解析度 (或硬體平臺的精確度) 來排程計時器事件。</span><span class="sxs-lookup"><span data-stu-id="f604d-116">Multimedia timer services allow applications to schedule timer events with the greatest resolution (or accuracy) possible for the hardware platform.</span></span> <span data-ttu-id="f604d-117">這些多媒體計時器服務可讓您以比其他計時器服務更高的解析度來排程計時器事件。</span><span class="sxs-lookup"><span data-stu-id="f604d-117">These multimedia timer services allow you to schedule timer events at a higher resolution than other timer services.</span></span>

<span data-ttu-id="f604d-118">這些計時器服務適用于需要高解析度時間的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f604d-118">These timer services are useful for applications that demand high-resolution timing.</span></span> <span data-ttu-id="f604d-119">例如，MIDI sequencer 需要高解析度計時器，因為它必須維持在1毫秒的解決範圍內之 MIDI 事件的步調。</span><span class="sxs-lookup"><span data-stu-id="f604d-119">For example, a MIDI sequencer requires a high-resolution timer because it must maintain the pace of MIDI events within a resolution of 1 millisecond.</span></span>

<span data-ttu-id="f604d-120">未使用高解析度時間的應用程式應該使用 [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) 函式，而不是多媒體計時器服務。</span><span class="sxs-lookup"><span data-stu-id="f604d-120">Applications that do not use high-resolution timing should use the [SetTimer](/windows/win32/api/winuser/nf-winuser-settimer) function instead of multimedia timer services.</span></span> <span data-ttu-id="f604d-121">**SetTimer** 提供的計時器服務會將 [WM \_ 計時器](../winmsg/wm-timer.md)訊息張貼到訊息佇列，而多媒體計時器服務會呼叫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f604d-121">The timer services provided by **SetTimer** post [WM\_TIMER](../winmsg/wm-timer.md) messages to a message queue, while the multimedia timer services call a callback function.</span></span> <span data-ttu-id="f604d-122">需要可等候計時器的應用程式應該使用 [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) 函數。</span><span class="sxs-lookup"><span data-stu-id="f604d-122">Applications that want a waitable timer should use the [CreateWaitableTimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function.</span></span>

 

 