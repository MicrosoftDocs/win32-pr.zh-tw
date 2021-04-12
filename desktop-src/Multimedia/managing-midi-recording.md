---
title: 管理 MIDI 錄製
description: 管理 MIDI 錄製
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- 音樂檢測數位介面 (MIDI) ，錄製
- MIDI (的音樂檢測數位介面) ，錄製
- 錄製 MIDI 音訊，管理
- MIDI 記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462973"
---
# <a name="managing-midi-recording"></a><span data-ttu-id="5c187-107">管理 MIDI 錄製</span><span class="sxs-lookup"><span data-stu-id="5c187-107">Managing MIDI Recording</span></span>

<span data-ttu-id="5c187-108">開啟 MIDI 裝置之後，您就可以開始錄製 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="5c187-108">After you open a MIDI device, you can begin recording MIDI data.</span></span> <span data-ttu-id="5c187-109">Windows 提供下列功能來管理 MIDI 錄音。</span><span class="sxs-lookup"><span data-stu-id="5c187-109">Windows provides the following functions for managing MIDI recording.</span></span>



| <span data-ttu-id="5c187-110">值</span><span class="sxs-lookup"><span data-stu-id="5c187-110">Value</span></span>                                      | <span data-ttu-id="5c187-111">意義</span><span class="sxs-lookup"><span data-stu-id="5c187-111">Meaning</span></span>                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c187-112">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="5c187-112">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | <span data-ttu-id="5c187-113">將緩衝區傳送到設備磁碟機，讓它可以填滿已記錄的系統專屬 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="5c187-113">Sends a buffer to the device driver so it can be filled with recorded system-exclusive MIDI data.</span></span> |
| [<span data-ttu-id="5c187-114">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="5c187-114">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | <span data-ttu-id="5c187-115">停止 MIDI 記錄，並將所有暫止的緩衝區標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="5c187-115">Stops MIDI recording and marks all pending buffers as done.</span></span>                                       |
| [<span data-ttu-id="5c187-116">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="5c187-116">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | <span data-ttu-id="5c187-117">啟動 MIDI 記錄，並將時間戳記重設為零。</span><span class="sxs-lookup"><span data-stu-id="5c187-117">Starts MIDI recording and resets the time stamp to zero.</span></span>                                          |
| [<span data-ttu-id="5c187-118">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="5c187-118">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | <span data-ttu-id="5c187-119">停止 MIDI 錄音。</span><span class="sxs-lookup"><span data-stu-id="5c187-119">Stops MIDI recording.</span></span>                                                                             |



 

<span data-ttu-id="5c187-120">若要將緩衝區傳送到設備磁碟機以記錄系統專屬的訊息，請使用 [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)。</span><span class="sxs-lookup"><span data-stu-id="5c187-120">To send buffers to the device driver for recording system-exclusive messages, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer).</span></span> <span data-ttu-id="5c187-121">當緩衝區填入系統專屬記錄資料時，就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="5c187-121">The application is notified as the buffers are filled with system-exclusive recorded data.</span></span> <span data-ttu-id="5c187-122">如需有關通知技術的詳細資訊，請參閱 [管理 MIDI 資料區塊](managing-midi-data-blocks.md)。</span><span class="sxs-lookup"><span data-stu-id="5c187-122">For more information about the notification techniques, see [Managing MIDI Data Blocks](managing-midi-data-blocks.md).</span></span>

<span data-ttu-id="5c187-123">[**MidiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)函式會開始錄製進程。</span><span class="sxs-lookup"><span data-stu-id="5c187-123">The [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) function begins the recording process.</span></span> <span data-ttu-id="5c187-124">記錄系統專屬的訊息時，請在開始錄製之前將至少一個緩衝區傳送至驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5c187-124">When recording system-exclusive messages, send at least one buffer to the driver before starting recording.</span></span> <span data-ttu-id="5c187-125">若要停止錄製，請使用 [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)。</span><span class="sxs-lookup"><span data-stu-id="5c187-125">To stop recording, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop).</span></span> <span data-ttu-id="5c187-126">使用 [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) 函式來關閉裝置之前，請先呼叫 [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)，將任何擱置中的資料區塊標示為已完成。</span><span class="sxs-lookup"><span data-stu-id="5c187-126">Before closing the device by using the [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) function, mark any pending data blocks as being done by calling [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).</span></span>

<span data-ttu-id="5c187-127">需要時間戳記資料的應用程式會使用回呼函數來接收 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="5c187-127">Applications that require time-stamped data use a callback function to receive MIDI data.</span></span> <span data-ttu-id="5c187-128">如果您的時間需求不是嚴格的，您可以使用視窗或執行緒回呼。</span><span class="sxs-lookup"><span data-stu-id="5c187-128">If your timing requirements are not strict, you can use a window or thread callback.</span></span> <span data-ttu-id="5c187-129">不過，您無法使用事件回呼來接收 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="5c187-129">However, you cannot use an event callback to receive MIDI data.</span></span>

<span data-ttu-id="5c187-130">若要使用不使用串流緩衝區的應用程式來記錄系統專屬的訊息，您必須以緩衝區提供設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5c187-130">To record system-exclusive messages with applications that do not use stream buffers, you must supply the device driver with buffers.</span></span> <span data-ttu-id="5c187-131">您可以使用 [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) 結構來指定這些緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5c187-131">These buffers are specified by using a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c187-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c187-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c187-133">錄製 MIDI 音訊</span><span class="sxs-lookup"><span data-stu-id="5c187-133">Recording MIDI Audio</span></span>](recording-midi-audio.md)
</dt> </dl>

 

 