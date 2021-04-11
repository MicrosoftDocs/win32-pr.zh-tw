---
title: 使用視窗訊息來管理 Waveform-Audio 播放
description: 使用視窗訊息來管理 Waveform-Audio 播放
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- 波形音訊，使用訊息管理播放
- 波形-音訊介面，使用訊息管理播放
- 播放波形-音訊檔案，使用訊息管理播放
- 波形音訊，訊息
- 波形-音訊介面，訊息
- 播放波形-音訊檔案，訊息
- MM_WOM_CLOSE 訊息
- MM_WOM_DONE 訊息
- MM_WOM_OPEN 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314854"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a><span data-ttu-id="0413a-112">使用視窗訊息來管理 Waveform-Audio 播放</span><span class="sxs-lookup"><span data-stu-id="0413a-112">Using Window Messages to Manage Waveform-Audio Playback</span></span>

<span data-ttu-id="0413a-113">您可以將下列訊息傳送至視窗程式函式，以管理波形音訊播放。</span><span class="sxs-lookup"><span data-stu-id="0413a-113">The following messages can be sent to a window procedure function for managing waveform-audio playback.</span></span>



| <span data-ttu-id="0413a-114">訊息</span><span class="sxs-lookup"><span data-stu-id="0413a-114">Message</span></span>                                | <span data-ttu-id="0413a-115">描述</span><span class="sxs-lookup"><span data-stu-id="0413a-115">Description</span></span>                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0413a-116">**MM \_ WOM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="0413a-116">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md) | <span data-ttu-id="0413a-117">在使用 [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) 函式關閉裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="0413a-117">Sent when the device is closed by using the [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) function.</span></span>                                 |
| [<span data-ttu-id="0413a-118">**MM \_ WOM \_ 完成**</span><span class="sxs-lookup"><span data-stu-id="0413a-118">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)   | <span data-ttu-id="0413a-119">當設備磁碟機使用 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) 函數傳送的資料區塊完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="0413a-119">Sent when the device driver is finished with a data block sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> |
| [<span data-ttu-id="0413a-120">**MM \_ WOM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="0413a-120">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)   | <span data-ttu-id="0413a-121">在使用 [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) 函式開啟裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="0413a-121">Sent when the device is opened by using the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>                                   |



 

<span data-ttu-id="0413a-122">*WParam* 和 *lParam* 參數與每個訊息相關聯。</span><span class="sxs-lookup"><span data-stu-id="0413a-122">A *wParam* and *lParam* parameter is associated with each of these messages.</span></span> <span data-ttu-id="0413a-123">*WParam* 參數一律會指定開啟波形音訊裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0413a-123">The *wParam* parameter always specifies a handle of the open waveform-audio device.</span></span> <span data-ttu-id="0413a-124">在 [**MM \_ WOM \_ 完成**](mm-wom-done.md) 訊息中， *lParam* 會指定 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) 結構的指標，以識別已完成的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="0413a-124">For the [**MM\_WOM\_DONE**](mm-wom-done.md) message, *lParam* specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the completed data block.</span></span> <span data-ttu-id="0413a-125">*LParam* 參數未用於 [**MM \_ WOM \_ CLOSE**](mm-wom-close.md)和 [**mm \_ WOM \_ 開啟**](mm-wom-open.md)的訊息。</span><span class="sxs-lookup"><span data-stu-id="0413a-125">The *lParam* parameter is unused for the [**MM\_WOM\_CLOSE**](mm-wom-close.md) and [**MM\_WOM\_OPEN**](mm-wom-open.md) messages.</span></span>

<span data-ttu-id="0413a-126">最有用的訊息可能是 \_ WOM \_ 完成。</span><span class="sxs-lookup"><span data-stu-id="0413a-126">The most useful message is probably MM\_WOM\_DONE.</span></span> <span data-ttu-id="0413a-127">當此訊息表示資料區塊的播放已完成時，您可以清除並釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="0413a-127">When this message signals that playback of a data block is complete, you can clean up and free the data block.</span></span> <span data-ttu-id="0413a-128">除非您需要配置記憶體或初始化變數，否則您可能不需要處理 MM \_ WOM \_ OPEN 和 mm \_ WOM \_ CLOSE 訊息。</span><span class="sxs-lookup"><span data-stu-id="0413a-128">Unless you need to allocate memory or initialize variables, you probably do not need to process the MM\_WOM\_OPEN and MM\_WOM\_CLOSE messages.</span></span>

<span data-ttu-id="0413a-129">波形音訊輸出裝置的回呼函式是由應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="0413a-129">The callback function for waveform-audio output devices is supplied by the application.</span></span> <span data-ttu-id="0413a-130">如需此回呼函數的詳細資訊，請參閱 [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) 函式。</span><span class="sxs-lookup"><span data-stu-id="0413a-130">For information about this callback function, see the [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) function.</span></span>

 

 