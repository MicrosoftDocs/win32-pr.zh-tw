---
description: WavSource 範例
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: WavSource 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848693"
---
# <a name="wavsource-sample"></a><span data-ttu-id="634e5-103">WavSource 範例</span><span class="sxs-lookup"><span data-stu-id="634e5-103">WavSource Sample</span></span>

<span data-ttu-id="634e5-104">顯示如何在 Microsoft 媒體基礎中建立自訂媒體來源。</span><span class="sxs-lookup"><span data-stu-id="634e5-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="634e5-105">此範例會執行分析 wav 音訊檔案的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="634e5-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="634e5-106">此範例是媒體來源的相對簡單範例：</span><span class="sxs-lookup"><span data-stu-id="634e5-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="634e5-107">只有一個資料流程，因此沒有可執行資料流程選取的程式碼。</span><span class="sxs-lookup"><span data-stu-id="634e5-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="634e5-108">媒體來源不會執行速率控制 (也就是向前快轉或反向播放) 。</span><span class="sxs-lookup"><span data-stu-id="634e5-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="634e5-109">所有來源和資料流程方法都會實作為同步方法。</span><span class="sxs-lookup"><span data-stu-id="634e5-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="634e5-110">由於 .wav 檔案的資料部分是未壓縮 PCM 音訊的單一區塊，因此媒體來源不需要讀取封包標頭，或在播放期間剖析串流，而非讀取初始 [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 標頭。</span><span class="sxs-lookup"><span data-stu-id="634e5-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="634e5-111">如需更先進的媒體來源範例，請參閱 [MPEG1Source 範例](mpeg1source-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="634e5-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="634e5-112">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="634e5-112">APIs Demonstrated</span></span>

<span data-ttu-id="634e5-113">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="634e5-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="634e5-114">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="634e5-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="634e5-115">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="634e5-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="634e5-116">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="634e5-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="634e5-117">使用方式</span><span class="sxs-lookup"><span data-stu-id="634e5-117">Usage</span></span>

<span data-ttu-id="634e5-118">WavSource 範例會建立一個 DLL，它是媒體來源和媒體來源位元組資料流程處理常式的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="634e5-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="634e5-119">使用媒體來源之前，您必須先註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="634e5-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="634e5-120">若要使用媒體來源，您可以執行 [BasicPlayback](/previous-versions//bb970475(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="634e5-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="634e5-121">如果您選取 .wav 檔案來播放，來源解析程式會自動載入媒體來源。</span><span class="sxs-lookup"><span data-stu-id="634e5-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="634e5-122"> (如果發生錯誤，請確定您已成功註冊 WavSource DLL。 ) </span><span class="sxs-lookup"><span data-stu-id="634e5-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="634e5-123">您也可以使用 TopoEdit 工具來建立包含媒體來源的播放拓撲。</span><span class="sxs-lookup"><span data-stu-id="634e5-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="634e5-124">如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="634e5-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="634e5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="634e5-125">Requirements</span></span>



| <span data-ttu-id="634e5-126">產品</span><span class="sxs-lookup"><span data-stu-id="634e5-126">Product</span></span>                                                        | <span data-ttu-id="634e5-127">版本</span><span class="sxs-lookup"><span data-stu-id="634e5-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="634e5-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="634e5-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="634e5-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="634e5-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="634e5-130">下載範例</span><span class="sxs-lookup"><span data-stu-id="634e5-130">Downloading the Sample</span></span>

<span data-ttu-id="634e5-131">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)中取得。</span><span class="sxs-lookup"><span data-stu-id="634e5-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="634e5-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="634e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="634e5-133">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="634e5-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="634e5-134">媒體來源</span><span class="sxs-lookup"><span data-stu-id="634e5-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="634e5-135">MPEG1Source 範例</span><span class="sxs-lookup"><span data-stu-id="634e5-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="634e5-136">配置處理常式和 Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="634e5-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="634e5-137">撰寫自訂媒體來源</span><span class="sxs-lookup"><span data-stu-id="634e5-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
