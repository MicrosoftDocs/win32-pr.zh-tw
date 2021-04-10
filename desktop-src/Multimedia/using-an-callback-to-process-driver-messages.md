---
title: 使用事件回呼處理驅動程式訊息
description: 使用事件回呼處理驅動程式訊息
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- 波形音訊、事件回呼
- 音訊資料區塊，事件回呼
- 波形音訊，處理驅動程式訊息
- 音訊資料區塊，處理驅動程式訊息
- 處理驅動程式訊息
- CreateEvent 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681886"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="ebec1-109">使用事件回呼處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="ebec1-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="ebec1-110">若要使用事件回呼，請使用 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) 函數建立手動重設事件。</span><span class="sxs-lookup"><span data-stu-id="ebec1-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="ebec1-111">在 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)函數的呼叫中，指定 *FdwOpen* 參數的 **回呼 \_ 事件**。</span><span class="sxs-lookup"><span data-stu-id="ebec1-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="ebec1-112">在您呼叫 [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) 函式，但在將波形音訊資料傳送至裝置之前，請呼叫 [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) 函式，將事件放入未收到信號狀態。</span><span class="sxs-lookup"><span data-stu-id="ebec1-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="ebec1-113">然後，在檢查 **WHDR \_ DONE** 旗標是否在 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwFlags** 成員中設定的迴圈內，呼叫 [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)函數，並將事件處理常式和超時值指定為參數。</span><span class="sxs-lookup"><span data-stu-id="ebec1-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="ebec1-114">由於事件回呼不會收到特定的關閉、完成或開啟的通知，因此應用程式可能必須檢查它在事件發生之後所等待的進程狀態。</span><span class="sxs-lookup"><span data-stu-id="ebec1-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="ebec1-115">[**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)傳回的時間可能已完成許多工具。</span><span class="sxs-lookup"><span data-stu-id="ebec1-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebec1-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebec1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebec1-117">音訊資料區塊</span><span class="sxs-lookup"><span data-stu-id="ebec1-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 