---
title: 使用回呼函式來處理驅動程式訊息
description: 使用回呼函式來處理驅動程式訊息
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- 波形音訊，回呼函數
- 音訊資料區塊，回呼函數
- 波形音訊，處理驅動程式訊息
- 音訊資料區塊，處理驅動程式訊息
- 處理驅動程式訊息
- waveInOpen 函式
- waveOutOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969704"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="83745-110">使用回呼函式來處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="83745-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="83745-111">您可以撰寫自己的回呼函式來處理設備磁碟機所傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="83745-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="83745-112">若要使用回呼函式，請在 \_ *fdwOpen* 參數中指定回呼函數旗標，並在 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)或 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)函數的 *dwCallback* 參數中指定回呼的位址。</span><span class="sxs-lookup"><span data-stu-id="83745-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="83745-113">傳送至回呼函式的訊息類似于傳送至視窗的訊息，但它們有兩個 **DWORD** 參數，而不是 **UINT** 和 **DWORD** 參數。</span><span class="sxs-lookup"><span data-stu-id="83745-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="83745-114">如需這些訊息的詳細資訊，請參閱 [播放 Waveform-Audio](playing-waveform-audio-files.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="83745-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="83745-115">若要將實例資料從應用程式傳遞給回呼函式，請使用下列其中一種技術：</span><span class="sxs-lookup"><span data-stu-id="83745-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="83745-116">使用開啟設備磁碟機的函式的 *dwInstance* 參數傳遞實例資料。</span><span class="sxs-lookup"><span data-stu-id="83745-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="83745-117">使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwUser** 成員（識別要傳送到設備磁碟機的音訊資料區塊）來傳遞實例資料。</span><span class="sxs-lookup"><span data-stu-id="83745-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="83745-118">如果您需要超過32個位的實例資料，請將指標傳遞至包含其他資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="83745-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 