---
title: 管理 Waveform-Audio 記錄
description: 管理 Waveform-Audio 記錄
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- 波形音訊，錄製
- 波形-音訊介面，錄製
- 錄製波形音訊，關於
- WAVEHDR 結構
- waveInAddBuffer 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314773"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="23616-108">管理 Waveform-Audio 記錄</span><span class="sxs-lookup"><span data-stu-id="23616-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="23616-109">開啟波形音訊輸入裝置之後，您就可以開始錄製波形音訊資料。</span><span class="sxs-lookup"><span data-stu-id="23616-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="23616-110">波形-音訊資料會記錄到 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構所指定的應用程式提供的緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="23616-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="23616-111">這些資料區塊必須在使用之前先備妥;如需詳細資訊，請參閱 [音訊資料區塊](audio-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="23616-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="23616-112">Windows 提供下列功能來管理波形音訊錄製。</span><span class="sxs-lookup"><span data-stu-id="23616-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="23616-113">函式</span><span class="sxs-lookup"><span data-stu-id="23616-113">Function</span></span>                                   | <span data-ttu-id="23616-114">描述</span><span class="sxs-lookup"><span data-stu-id="23616-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23616-115">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="23616-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="23616-116">將緩衝區傳送到設備磁碟機，讓它可以填滿錄製的波形音訊資料。</span><span class="sxs-lookup"><span data-stu-id="23616-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="23616-117">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="23616-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="23616-118">停止波形-音訊錄製，並將所有暫止的緩衝區標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="23616-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="23616-119">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="23616-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="23616-120">開始波形-音訊錄製。</span><span class="sxs-lookup"><span data-stu-id="23616-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="23616-121">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="23616-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="23616-122">停止波形-音訊錄製。</span><span class="sxs-lookup"><span data-stu-id="23616-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="23616-123">使用 [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) 函式將緩衝區傳送到設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="23616-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="23616-124">當緩衝區填滿錄製的波形音訊資料時，會根據開啟裝置時所指定的旗標，以視窗訊息、回呼訊息、執行緒訊息或事件來通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="23616-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="23616-125">使用 [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)開始錄製之前，您應該至少將一個緩衝區傳送至驅動程式，否則可能會遺失傳入的資料。</span><span class="sxs-lookup"><span data-stu-id="23616-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="23616-126">使用 [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)來關閉裝置之前，請先呼叫 [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) ，將任何擱置中的資料區塊標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="23616-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23616-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="23616-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23616-128">錄製波形音訊</span><span class="sxs-lookup"><span data-stu-id="23616-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 