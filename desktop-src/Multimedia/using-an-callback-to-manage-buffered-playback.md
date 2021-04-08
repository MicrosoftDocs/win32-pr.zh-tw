---
title: 使用事件回呼來管理緩衝的播放
description: 使用事件回呼來管理緩衝的播放
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- 音樂檢測數位介面 (MIDI) 、緩衝播放
- MIDI (的音樂檢測數位介面) ，經過緩衝的播放
- 播放 MIDI 檔案，緩衝播放
- 緩衝播放
- CreateEvent 函數
- 音樂檢測數位介面 (MIDI) 、事件回呼
- MIDI (的音樂檢測數位介面) 、事件回呼
- 播放 MIDI 檔案，事件回呼
- 事件回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681887"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a><span data-ttu-id="47a67-112">使用事件回呼來管理緩衝的播放</span><span class="sxs-lookup"><span data-stu-id="47a67-112">Using an Event Callback to Manage Buffered Playback</span></span>

<span data-ttu-id="47a67-113">若要使用事件回呼，請使用 [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數來取出事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="47a67-113">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event.</span></span> <span data-ttu-id="47a67-114">在 [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) 函數的呼叫中，指定 \_ *dwFlags* 參數的回呼事件。</span><span class="sxs-lookup"><span data-stu-id="47a67-114">In a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function, specify CALLBACK\_EVENT for the *dwFlags* parameter.</span></span> <span data-ttu-id="47a67-115">在使用 [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) 函式之後，但在將 MIDI 事件傳送到裝置之前，請藉由呼叫 [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) 函式來建立未收到訊號事件，以指定 **CreateEvent** 抓取的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="47a67-115">After using the [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function but before sending MIDI events to the device, create a nonsignaled event by calling the [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) function, specifying the event handle retrieved by **CreateEvent**.</span></span> <span data-ttu-id="47a67-116">然後，在檢查是否在 \_ [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)結構的 **DWFLAGS** 成員中設定 MHDR 完成位的迴圈內，請使用 [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)函數，指定事件控制碼，並將超時值指定為無限的參數。</span><span class="sxs-lookup"><span data-stu-id="47a67-116">Then, inside a loop that checks whether the MHDR\_DONE bit is set in the **dwFlags** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure, use the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying the event handle and a time-out value of INFINITE as parameters.</span></span>

<span data-ttu-id="47a67-117">事件回呼是由任何可能導致函式回呼的專案所設定。</span><span class="sxs-lookup"><span data-stu-id="47a67-117">An event callback is set by anything that might cause a function callback.</span></span>

<span data-ttu-id="47a67-118">由於事件回呼不會收到特定的關閉、完成或開啟通知，因此應用程式可能需要在事件發生之後，檢查其正在等候的進程狀態。</span><span class="sxs-lookup"><span data-stu-id="47a67-118">Because event callbacks do not receive specific close, done, or open notifications, an application may need to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="47a67-119">可能會在 **WaitForSingleObject** 傳回時完成許多工。</span><span class="sxs-lookup"><span data-stu-id="47a67-119">It is possible that a number of tasks could be completed by the time **WaitForSingleObject** returns.</span></span>

 

 