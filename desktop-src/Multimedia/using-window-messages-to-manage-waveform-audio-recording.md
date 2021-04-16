---
title: 使用視窗訊息來管理 Waveform-Audio 記錄
description: 使用視窗訊息來管理 Waveform-Audio 記錄
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- 波形音訊，使用訊息管理錄製
- 波形-音訊介面，使用訊息管理錄製
- 錄製波形音訊，使用訊息管理錄製
- 波形音訊，訊息
- 波形-音訊介面，訊息
- 錄製波形音訊，訊息
- MM_WIM_CLOSE 訊息
- MM_WIM_DATA 訊息
- MM_WIM_OPEN 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463004"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a><span data-ttu-id="8c70a-112">使用視窗訊息來管理 Waveform-Audio 記錄</span><span class="sxs-lookup"><span data-stu-id="8c70a-112">Using Window Messages to Manage Waveform-Audio Recording</span></span>

<span data-ttu-id="8c70a-113">您可以將下列訊息傳送至視窗程式函式，以管理波形音訊錄製。</span><span class="sxs-lookup"><span data-stu-id="8c70a-113">The following messages can be sent to a window procedure function for managing waveform-audio recording.</span></span>



| <span data-ttu-id="8c70a-114">訊息</span><span class="sxs-lookup"><span data-stu-id="8c70a-114">Message</span></span>                                | <span data-ttu-id="8c70a-115">描述</span><span class="sxs-lookup"><span data-stu-id="8c70a-115">Description</span></span>                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c70a-116">**MM \_ WIM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="8c70a-116">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md) | <span data-ttu-id="8c70a-117">在使用 [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) 函式關閉裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="8c70a-117">Sent when the device is closed by using the [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) function.</span></span>                                     |
| [<span data-ttu-id="8c70a-118">**MM \_ WIM \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="8c70a-118">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)   | <span data-ttu-id="8c70a-119">當設備磁碟機使用 [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) 函式傳送的緩衝區完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="8c70a-119">Sent when the device driver is finished with a buffer sent by using the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function.</span></span> |
| [<span data-ttu-id="8c70a-120">**MM \_ WIM \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="8c70a-120">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)   | <span data-ttu-id="8c70a-121">在使用 [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) 函式開啟裝置時傳送。</span><span class="sxs-lookup"><span data-stu-id="8c70a-121">Sent when the device is opened by using the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function.</span></span>                                       |



 

<span data-ttu-id="8c70a-122">[**MM \_ WIM \_ 資料**](mm-wim-data.md)的 *lParam* 參數會指定識別緩衝區之 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8c70a-122">The *lParam* parameter of [**MM\_WIM\_DATA**](mm-wim-data.md) specifies a pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer.</span></span> <span data-ttu-id="8c70a-123">此緩衝區可能不會完全以波形-音訊資料填滿;記錄可能會在緩衝區填滿之前停止。</span><span class="sxs-lookup"><span data-stu-id="8c70a-123">This buffer might not be completely filled with waveform-audio data; recording can stop before the buffer is filled.</span></span> <span data-ttu-id="8c70a-124">您可以使用 **WAVEHDR** 結構的 **dwBytesRecorded** 成員，判斷存在於緩衝區中的有效資料量。</span><span class="sxs-lookup"><span data-stu-id="8c70a-124">Use the **dwBytesRecorded** member of the **WAVEHDR** structure to determine the amount of valid data present in the buffer.</span></span>

<span data-ttu-id="8c70a-125">最有用的訊息可能是 [**以 \_ WIM \_ 資料為 MM**](mm-wim-data.md)。</span><span class="sxs-lookup"><span data-stu-id="8c70a-125">The most useful message is probably [**MM\_WIM\_DATA**](mm-wim-data.md).</span></span> <span data-ttu-id="8c70a-126">當您的應用程式使用設備磁碟機所傳送的資料區塊完成時，您可以清除並釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="8c70a-126">When your application finishes using the data block sent by the device driver, you can clean up and free the data block.</span></span> <span data-ttu-id="8c70a-127">除非您需要配置記憶體或初始化變數，否則您可能不需要使用 [**mm \_ wim \_ 開啟**](mm-wim-open.md) 和 [**mm \_ wim \_ 關閉**](mm-wim-close.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="8c70a-127">Unless you need to allocate memory or initialize variables, you probably do not need to use the [**MM\_WIM\_OPEN**](mm-wim-open.md) and [**MM\_WIM\_CLOSE**](mm-wim-close.md) messages.</span></span>

<span data-ttu-id="8c70a-128">波形音訊輸入裝置的回呼函式是由應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="8c70a-128">The callback function for waveform-audio input devices is supplied by the application.</span></span> <span data-ttu-id="8c70a-129">如需此回呼函數的詳細資訊，請參閱 [**waveInProc**](/previous-versions//dd743849(v=vs.85)) 函式。</span><span class="sxs-lookup"><span data-stu-id="8c70a-129">For information about this callback function, see the [**waveInProc**](/previous-versions//dd743849(v=vs.85)) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c70a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c70a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c70a-131">錄製波形音訊</span><span class="sxs-lookup"><span data-stu-id="8c70a-131">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 