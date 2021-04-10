---
title: 影片調整大小
description: 影片調整大小
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK，調整大小的影片
- Windows Media Format SDK，調整大小影片
- Advanced Systems Format (ASF) 、影片大小調整
- ASF (Advanced Systems Format) 、影片大小調整
- Advanced Systems Format (ASF) ，調整大小影片
- ASF (Advanced Systems Format) ，調整大小影片
- 影片調整大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183283"
---
# <a name="video-resizing"></a><span data-ttu-id="89d12-110">影片調整大小</span><span class="sxs-lookup"><span data-stu-id="89d12-110">Video Resizing</span></span>

<span data-ttu-id="89d12-111">當您定義影片資料流程的設定時，您必須指定影片框架的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="89d12-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="89d12-112">此影片大小會決定在檔案的 [資料] 區段中編碼的影片框架大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="89d12-113">不過，設定檔中的影片大小不會決定或限制您傳遞給寫入器的輸入媒體大小，或是您從讀取器收到的輸出媒體大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="89d12-114">寫入器可以調整影片畫面的大小，以符合您應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="89d12-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="89d12-115">影片影像大小可視為三個階段：輸入影片大小、串流影片大小和輸出影片大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="89d12-116">輸入影片大小是您以範例形式傳遞至寫入器物件的框架大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="89d12-117">您可以將此大小定義為其中一個必要的影片輸入屬性。</span><span class="sxs-lookup"><span data-stu-id="89d12-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="89d12-118">如需輸入屬性的詳細資訊，請參閱 [列舉輸入格式](to-enumerate-input-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="89d12-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="89d12-119">串流影片大小是 ASF 檔案的 [資料] 區段中的框架大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="89d12-120">您可以將此大小定義為設定檔中的其中一個必要的串流設定。</span><span class="sxs-lookup"><span data-stu-id="89d12-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="89d12-121">如果您要寫入檔案，且輸入影片大小與串流影片大小不同，則寫入器會在編碼時調整框架大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="89d12-122">如需影片串流屬性的詳細資訊，請參閱設定 [影片串流](configuring-video-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="89d12-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="89d12-123">輸出影片大小是由讀取器或同步讀取器所提供的框架大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="89d12-124">您可以將此大小定義為其中一個必要的影片輸出屬性。</span><span class="sxs-lookup"><span data-stu-id="89d12-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="89d12-125">如果您要讀取檔案，而且輸出影片大小與串流影片大小不同，則讀取器會在解碼時調整畫面的大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="89d12-126">您無法將 stream 影片大小設定為奇數圖元寬的數位。</span><span class="sxs-lookup"><span data-stu-id="89d12-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="89d12-127">如果您將影片資料流程的寬度設定為奇數值，寫入器將不會接受該設定檔，否則產生的影片將會以一側的黑色線條向下編碼來構成差異。</span><span class="sxs-lookup"><span data-stu-id="89d12-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="89d12-128">調整影片大小時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="89d12-128">You should take care when resizing video.</span></span> <span data-ttu-id="89d12-129">影像通常會以原始解析度查看其最佳效果。</span><span class="sxs-lookup"><span data-stu-id="89d12-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="89d12-130">調整影像大小通常會造成失真，並讓文字難以辨識。</span><span class="sxs-lookup"><span data-stu-id="89d12-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="89d12-131">如果您要將影片壓縮成低位速率，您也會發現調整大小扭曲可能會導致嚴重的壓縮成品。</span><span class="sxs-lookup"><span data-stu-id="89d12-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="89d12-132">Windows Media 視訊9螢幕編解碼器不支援調整大小。</span><span class="sxs-lookup"><span data-stu-id="89d12-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d12-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="89d12-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d12-134">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="89d12-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="89d12-135">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="89d12-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="89d12-136">**使用輸出**</span><span class="sxs-lookup"><span data-stu-id="89d12-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




