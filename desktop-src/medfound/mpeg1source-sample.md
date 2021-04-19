---
description: MPEG1Source 範例
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: MPEG1Source 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987429"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="d805a-103">MPEG1Source 範例</span><span class="sxs-lookup"><span data-stu-id="d805a-103">MPEG1Source Sample</span></span>

<span data-ttu-id="d805a-104">顯示如何在 Microsoft 媒體基礎中撰寫自訂媒體來源。</span><span class="sxs-lookup"><span data-stu-id="d805a-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="d805a-105">此範例會執行可剖析 MPEG-2 系統層串流的媒體來源，並產生包含 MPEG-2 承載的範例。</span><span class="sxs-lookup"><span data-stu-id="d805a-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="d805a-106">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="d805a-106">APIs Demonstrated</span></span>

<span data-ttu-id="d805a-107">這個範例會示範下列媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="d805a-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="d805a-108">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="d805a-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="d805a-109">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="d805a-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="d805a-110">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="d805a-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="d805a-111">在檢查這個範例之前，您可能會想要先複習 [WavSource 範例](wavsource-sample.md)，以提供更簡單的媒體來源執行。</span><span class="sxs-lookup"><span data-stu-id="d805a-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="d805a-112">MPEG1Source 範例會新增一些功能，這些功能可在大部分真實世界的媒體來源執行中找到：</span><span class="sxs-lookup"><span data-stu-id="d805a-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="d805a-113">多個資料流</span><span class="sxs-lookup"><span data-stu-id="d805a-113">Multiple streams</span></span>
-   <span data-ttu-id="d805a-114">非同步方法</span><span class="sxs-lookup"><span data-stu-id="d805a-114">Asynchronous methods</span></span>
-   <span data-ttu-id="d805a-115">非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="d805a-115">Asynchronous I/O</span></span>

<span data-ttu-id="d805a-116">在 Windows Server 2008 的 Windows SDK 中，此範例也包含範例 MPEG-2 視頻解碼器，可顯示每個影片畫面的時間代碼。</span><span class="sxs-lookup"><span data-stu-id="d805a-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="d805a-117"> (它實際上並不會解碼 MPEG-2 位流。 ) </span><span class="sxs-lookup"><span data-stu-id="d805a-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="d805a-118">從 Windows 7 的 Windows SDK 開始，已將此解碼器移至個別的範例。</span><span class="sxs-lookup"><span data-stu-id="d805a-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="d805a-119">請參閱 [解碼器範例](decoder-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="d805a-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d805a-120">使用方式</span><span class="sxs-lookup"><span data-stu-id="d805a-120">Usage</span></span>

<span data-ttu-id="d805a-121">MPEG1Source 範例會建立一個 DLL，它是媒體來源、媒體來源位元組資料流程處理常式和解碼器 MFT 的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d805a-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="d805a-122">使用媒體來源之前，您必須先註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="d805a-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="d805a-123">若要使用媒體來源，您可以執行 [BasicPlayback 範例](/previous-versions//bb970475(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d805a-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="d805a-124">如果您選取要播放的 MPEG-2 檔案，來源解析程式會自動載入媒體來源。</span><span class="sxs-lookup"><span data-stu-id="d805a-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="d805a-125"> (如果發生錯誤，請確定您已成功註冊 MPEG1Source DLL。 ) </span><span class="sxs-lookup"><span data-stu-id="d805a-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="d805a-126">您也可以使用 TopoEdit 工具來建立包含媒體來源的播放拓撲。</span><span class="sxs-lookup"><span data-stu-id="d805a-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="d805a-127">如需 TopoEdit 的詳細資訊，請參閱 [TopoEdit](topoedit.md)。</span><span class="sxs-lookup"><span data-stu-id="d805a-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d805a-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d805a-128">Requirements</span></span>



| <span data-ttu-id="d805a-129">產品</span><span class="sxs-lookup"><span data-stu-id="d805a-129">Product</span></span>                                                        | <span data-ttu-id="d805a-130">版本</span><span class="sxs-lookup"><span data-stu-id="d805a-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d805a-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d805a-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d805a-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d805a-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d805a-133">下載範例</span><span class="sxs-lookup"><span data-stu-id="d805a-133">Downloading the Sample</span></span>

<span data-ttu-id="d805a-134">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source)中取得。</span><span class="sxs-lookup"><span data-stu-id="d805a-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d805a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d805a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d805a-136">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="d805a-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="d805a-137">媒體來源</span><span class="sxs-lookup"><span data-stu-id="d805a-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="d805a-138">配置處理常式和 Byte-Stream 處理常式</span><span class="sxs-lookup"><span data-stu-id="d805a-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="d805a-139">教學課程：撰寫自訂媒體來源</span><span class="sxs-lookup"><span data-stu-id="d805a-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="d805a-140">WavSource 範例</span><span class="sxs-lookup"><span data-stu-id="d805a-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
