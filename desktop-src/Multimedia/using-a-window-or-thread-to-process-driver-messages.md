---
title: 使用視窗或執行緒驅動程式訊息
description: 使用視窗或執行緒驅動程式訊息
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- 波形音訊、視窗回呼
- 音訊資料區塊，視窗回呼
- 波形音訊，執行緒回呼
- 音訊資料區塊，執行緒回呼
- 波形音訊，處理驅動程式訊息
- 音訊資料區塊，處理驅動程式訊息
- 處理驅動程式訊息
- waveInOpen 函式
- waveOutOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933233"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a><span data-ttu-id="6d2b5-112">使用視窗或執行緒驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="6d2b5-112">Using a Window or Thread to Process Driver Messages</span></span>

<span data-ttu-id="6d2b5-113">若要使用視窗回呼函式，請在 \_ *fdwOpen* 參數中指定回呼視窗旗標，並在 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)或 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)函式之 *dwCallback* 參數的低序位單字中指定視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d2b5-113">To use a window callback function, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the low-order word of the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span> <span data-ttu-id="6d2b5-114">驅動程式訊息將會傳送至 *dwCallback* 中的控制碼所識別之視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="6d2b5-114">Driver messages will be sent to the window procedure for the window identified by the handle in *dwCallback*.</span></span>

<span data-ttu-id="6d2b5-115">同樣地，若要使用執行緒回呼，請 \_ 在 **WaveInOpen** 或 **waveOutOpen** 的呼叫中指定回呼執行緒和執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d2b5-115">Similarly, to use a thread callback, specify CALLBACK\_THREAD and a thread handle in the call to **waveInOpen** or **waveOutOpen**.</span></span> <span data-ttu-id="6d2b5-116">在此情況下，會將訊息張貼到指定的執行緒，而不是傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="6d2b5-116">In this case, messages are posted to the specified thread instead of to a window.</span></span>

<span data-ttu-id="6d2b5-117">傳送至視窗或執行緒回呼的訊息，專屬於所使用的音訊裝置類型而異。</span><span class="sxs-lookup"><span data-stu-id="6d2b5-117">Messages sent to the window or thread callback are specific to the audio device type used.</span></span> <span data-ttu-id="6d2b5-118">如需這些訊息的詳細資訊，請參閱 [播放 Waveform-Audio](playing-waveform-audio-files.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="6d2b5-118">For more information about these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

 

 