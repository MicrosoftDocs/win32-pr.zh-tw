---
description: 本教學課程說明如何使用 Media Session 物件播放媒體檔案。
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: 如何使用媒體基礎播放媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104560230"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="a2766-103">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="a2766-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="a2766-104">本教學課程說明如何使用 [Media Session](media-session.md) 物件播放媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="a2766-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a2766-105">必要條件</span><span class="sxs-lookup"><span data-stu-id="a2766-105">Prerequisites</span></span>

<span data-ttu-id="a2766-106">閱讀本主題之前，您應該先熟悉下列媒體基礎概念：</span><span class="sxs-lookup"><span data-stu-id="a2766-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="a2766-107">媒體會話</span><span class="sxs-lookup"><span data-stu-id="a2766-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="a2766-108">來源解析程式</span><span class="sxs-lookup"><span data-stu-id="a2766-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="a2766-109">拓撲</span><span class="sxs-lookup"><span data-stu-id="a2766-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="a2766-110">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="a2766-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="a2766-111">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="a2766-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="a2766-112">本主題不會說明如何播放受到數位版權管理 (DRM) 保護的檔案。</span><span class="sxs-lookup"><span data-stu-id="a2766-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="a2766-113">如需 Microsoft 媒體基礎中 DRM 的詳細資訊，請參閱 [如何播放受保護的媒體](how-to-play-protected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="a2766-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="a2766-114">概觀</span><span class="sxs-lookup"><span data-stu-id="a2766-114">Overview</span></span>

<span data-ttu-id="a2766-115">下列物件是用來播放媒體檔案和媒體會話：</span><span class="sxs-lookup"><span data-stu-id="a2766-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="a2766-116">*媒體來源* 是剖析媒體檔案或其他媒體資料來源的物件。</span><span class="sxs-lookup"><span data-stu-id="a2766-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="a2766-117">媒體來源會為檔案中的每個音訊或影片串流建立 *資料流程* 物件。</span><span class="sxs-lookup"><span data-stu-id="a2766-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="a2766-118">*解碼器* 會將編碼的媒體資料轉換成未壓縮的影片和音訊。</span><span class="sxs-lookup"><span data-stu-id="a2766-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="a2766-119">*來源解析程式* 會從 URL 建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="a2766-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="a2766-120">[增強型影片](enhanced-video-renderer.md)轉譯器 (EVR) 將影片轉譯至螢幕。</span><span class="sxs-lookup"><span data-stu-id="a2766-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="a2766-121">[串流音訊](streaming-audio-renderer.md)轉譯器 (SAR) 將音訊轉譯成喇叭或其他音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="a2766-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="a2766-122">*拓撲* 會定義從媒體來源到 EVR 和 SAR 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a2766-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="a2766-123">*媒體會話* 可控制資料流程並將狀態事件傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="a2766-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="a2766-124">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="a2766-124">The following diagram illustrates this process.</span></span>

![顯示使用媒體會話播放的圖表](images/session-playback.gif)

<span data-ttu-id="a2766-126">以下是使用媒體會話播放媒體檔案時所需步驟的一般大綱：</span><span class="sxs-lookup"><span data-stu-id="a2766-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="a2766-127">呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函式來初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="a2766-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="a2766-128">呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立媒體會話的新實例。</span><span class="sxs-lookup"><span data-stu-id="a2766-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="a2766-129">使用來源解析程式來建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="a2766-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="a2766-130">如需詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="a2766-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="a2766-131">建立將媒體來源連接至 EVR 和 SAR 的拓撲。</span><span class="sxs-lookup"><span data-stu-id="a2766-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="a2766-132">在這個步驟中，應用程式會建立不包含該解碼器的 *部分* 拓撲。</span><span class="sxs-lookup"><span data-stu-id="a2766-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="a2766-133">如需詳細資訊，請參閱 [建立播放拓撲](creating-playback-topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="a2766-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="a2766-134">呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定媒體會話上的拓撲。</span><span class="sxs-lookup"><span data-stu-id="a2766-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="a2766-135">使用 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面從媒體會話取得事件。</span><span class="sxs-lookup"><span data-stu-id="a2766-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="a2766-136">呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 以開始播放。</span><span class="sxs-lookup"><span data-stu-id="a2766-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="a2766-137">播放開始之後，您可以藉由呼叫 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)來暫停它，或呼叫 [**IMFMediaSession：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)來停止它。</span><span class="sxs-lookup"><span data-stu-id="a2766-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="a2766-138">當應用程式結束時，釋放資源：</span><span class="sxs-lookup"><span data-stu-id="a2766-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="a2766-139">呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="a2766-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="a2766-140">這個方法是非同步方法。</span><span class="sxs-lookup"><span data-stu-id="a2766-140">This method is asynchronous.</span></span> <span data-ttu-id="a2766-141">完成時，媒體會話會傳送 [MESessionClosed](mesessionclosed.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a2766-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="a2766-142">然後可以安全地執行其餘步驟。</span><span class="sxs-lookup"><span data-stu-id="a2766-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="a2766-143">呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 以關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="a2766-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="a2766-144">呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) 以關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="a2766-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="a2766-145">呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 以關閉媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="a2766-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="a2766-146">下列各節顯示完整的程式碼範例：</span><span class="sxs-lookup"><span data-stu-id="a2766-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="a2766-147">步驟1：宣告 CPlayer 類別</span><span class="sxs-lookup"><span data-stu-id="a2766-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="a2766-148">步驟2：建立 CPlayer 物件</span><span class="sxs-lookup"><span data-stu-id="a2766-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="a2766-149">步驟3：開啟媒體檔案</span><span class="sxs-lookup"><span data-stu-id="a2766-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="a2766-150">步驟4：建立媒體會話</span><span class="sxs-lookup"><span data-stu-id="a2766-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="a2766-151">步驟5：處理媒體會話事件</span><span class="sxs-lookup"><span data-stu-id="a2766-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="a2766-152">步驟6：控制播放</span><span class="sxs-lookup"><span data-stu-id="a2766-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="a2766-153">步驟7：關機媒體會話</span><span class="sxs-lookup"><span data-stu-id="a2766-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="a2766-154">媒體會話播放範例</span><span class="sxs-lookup"><span data-stu-id="a2766-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="a2766-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2766-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2766-156">媒體會話</span><span class="sxs-lookup"><span data-stu-id="a2766-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="a2766-157">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="a2766-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



