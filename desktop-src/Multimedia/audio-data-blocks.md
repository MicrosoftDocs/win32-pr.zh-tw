---
title: 音訊資料區塊
description: 音訊資料區塊
ms.assetid: 9646e18c-294b-4532-bd5e-709d66ad31f4
keywords:
- 多媒體音訊，資料區塊
- 音訊、資料區塊
- 波形音訊、資料區塊
- 音訊資料區塊，關於
- WAVEHDR 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a81a5a29ec9718e7c11306b6bafc1aa20369e5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933125"
---
# <a name="audio-data-blocks"></a><span data-ttu-id="46e96-108">音訊資料區塊</span><span class="sxs-lookup"><span data-stu-id="46e96-108">Audio Data Blocks</span></span>

<span data-ttu-id="46e96-109">[**WaveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)和 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)函式需要應用程式佈建資料區塊，以傳遞至設備磁碟機以供錄製或播放之用。</span><span class="sxs-lookup"><span data-stu-id="46e96-109">The [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) and [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) functions require applications to allocate data blocks to pass to the device drivers for recording or playback purposes.</span></span> <span data-ttu-id="46e96-110">這兩個函數都會使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構來描述其資料區塊。</span><span class="sxs-lookup"><span data-stu-id="46e96-110">Both of these functions use the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to describe its data block.</span></span>

<span data-ttu-id="46e96-111">使用這些函式的其中一個來將資料區塊傳遞給設備磁碟機之前，您必須為數據區塊和描述資料區塊的標頭結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="46e96-111">Before using one of these functions to pass a data block to a device driver, you must allocate memory for the data block and the header structure that describes the data block.</span></span> <span data-ttu-id="46e96-112">您可以使用下列功能來備妥和取消準備標頭。</span><span class="sxs-lookup"><span data-stu-id="46e96-112">The headers can be prepared and unprepared by using the following functions.</span></span>



| <span data-ttu-id="46e96-113">函式</span><span class="sxs-lookup"><span data-stu-id="46e96-113">Function</span></span>                                                 | <span data-ttu-id="46e96-114">描述</span><span class="sxs-lookup"><span data-stu-id="46e96-114">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="46e96-115">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="46e96-115">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)       | <span data-ttu-id="46e96-116">準備波形-音訊輸入資料區塊。</span><span class="sxs-lookup"><span data-stu-id="46e96-116">Prepares a waveform-audio input data block.</span></span>                      |
| [<span data-ttu-id="46e96-117">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="46e96-117">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)   | <span data-ttu-id="46e96-118">清除波形音訊輸入資料區塊的準備工作。</span><span class="sxs-lookup"><span data-stu-id="46e96-118">Cleans up the preparation on a waveform-audio input data block.</span></span>  |
| [<span data-ttu-id="46e96-119">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="46e96-119">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)     | <span data-ttu-id="46e96-120">準備波形音訊輸出資料區塊。</span><span class="sxs-lookup"><span data-stu-id="46e96-120">Prepares a waveform-audio output data block.</span></span>                     |
| [<span data-ttu-id="46e96-121">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="46e96-121">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) | <span data-ttu-id="46e96-122">清除波形音訊輸出資料區塊的準備工作。</span><span class="sxs-lookup"><span data-stu-id="46e96-122">Cleans up the preparation on a waveform-audio output data block.</span></span> |



 

<span data-ttu-id="46e96-123">將音訊資料區塊傳遞到設備磁碟機之前，您必須先將資料區塊傳遞給 [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) 或 [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)，以準備資料區塊。</span><span class="sxs-lookup"><span data-stu-id="46e96-123">Before you pass an audio data block to a device driver, you must prepare the data block by passing it to either [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader) or [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader).</span></span> <span data-ttu-id="46e96-124">當設備磁碟機完成資料區塊並傳回它時，您必須先將資料區塊傳遞至 [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) 或 [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) ，然後再釋放任何配置的記憶體，以清除此準備工作。</span><span class="sxs-lookup"><span data-stu-id="46e96-124">When the device driver is finished with the data block and returns it, you must clean up this preparation by passing the data block to either [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader) or [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) before any allocated memory can be freed.</span></span>

<span data-ttu-id="46e96-125">除非波形-音訊輸入和輸出資料小到足以包含在單一資料區塊中，否則應用程式必須持續提供設備磁碟機與資料區塊，直到播放或錄製完成為止。</span><span class="sxs-lookup"><span data-stu-id="46e96-125">Unless the waveform-audio input and output data is small enough to be contained in a single data block, applications must continually supply the device driver with data blocks until playback or recording is complete.</span></span>

<span data-ttu-id="46e96-126">即使使用單一資料區塊，應用程式也必須能夠判斷設備磁碟機何時完成資料區塊，讓應用程式可以釋放與資料區塊和標頭結構相關聯的記憶體。</span><span class="sxs-lookup"><span data-stu-id="46e96-126">Even if a single data block is used, an application must be able to determine when a device driver is finished with the data block so the application can free the memory associated with the data block and header structure.</span></span> <span data-ttu-id="46e96-127">有幾種方式可判斷設備磁碟機何時完成資料區塊：</span><span class="sxs-lookup"><span data-stu-id="46e96-127">There are several ways to determine when a device driver is finished with a data block:</span></span>

-   <span data-ttu-id="46e96-128">藉由指定回呼函式，以在使用資料區塊完成時接收驅動程式所傳送的訊息</span><span class="sxs-lookup"><span data-stu-id="46e96-128">By specifying a callback function to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="46e96-129">使用事件回呼</span><span class="sxs-lookup"><span data-stu-id="46e96-129">By using an event callback</span></span>
-   <span data-ttu-id="46e96-130">藉由指定視窗或執行緒，以接收驅動程式完成使用資料區塊時所傳送的訊息</span><span class="sxs-lookup"><span data-stu-id="46e96-130">By specifying a window or thread to receive a message sent by the driver when it is finished with a data block</span></span>
-   <span data-ttu-id="46e96-131">藉由 \_ 在每個資料區塊所傳送之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **DWFLAGS** 成員中輪詢 WHDR 完成位</span><span class="sxs-lookup"><span data-stu-id="46e96-131">By polling the WHDR\_DONE bit in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure sent with each data block</span></span>

<span data-ttu-id="46e96-132">如果應用程式在需要時無法取得設備磁碟機的資料區塊，則播放可能會有可能出現的間隙或遺失傳入記錄的資訊。</span><span class="sxs-lookup"><span data-stu-id="46e96-132">If an application does not get a data block to the device driver when needed, there can be an audible gap in playback or a loss of incoming recorded information.</span></span> <span data-ttu-id="46e96-133">這至少需要雙重緩衝配置，至少要在設備磁碟機之前保持至少一個資料區塊。</span><span class="sxs-lookup"><span data-stu-id="46e96-133">This requires at least a double-buffering scheme — staying at least one data block ahead of the device driver.</span></span>

<span data-ttu-id="46e96-134">下列主題描述使用資料區塊完成設備磁碟機的判斷方式：</span><span class="sxs-lookup"><span data-stu-id="46e96-134">The following topics describe ways to determine when a device driver is finished with a data block:</span></span>

<span data-ttu-id="46e96-135">使用回呼函式來處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="46e96-135">Using a Callback Function to Process Driver Messages</span></span>

-   [<span data-ttu-id="46e96-136">使用回呼函式來處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="46e96-136">Using a Callback Function to Process Driver Messages</span></span>](using-a-callback-function-to-process-driver-messages.md)
-   [<span data-ttu-id="46e96-137">使用事件回呼處理驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="46e96-137">Using an Event Callback to Process Driver Messages</span></span>](using-an-callback-to-process-driver-messages.md)
-   [<span data-ttu-id="46e96-138">使用視窗或執行緒驅動程式訊息</span><span class="sxs-lookup"><span data-stu-id="46e96-138">Using a Window or Thread to Process Driver Messages</span></span>](using-a-window-or-thread-to-process-driver-messages.md)
-   [<span data-ttu-id="46e96-139">藉由輪詢管理資料區塊</span><span class="sxs-lookup"><span data-stu-id="46e96-139">Managing Data Blocks by Polling</span></span>](managing-data-blocks-by-polling.md)

 

 