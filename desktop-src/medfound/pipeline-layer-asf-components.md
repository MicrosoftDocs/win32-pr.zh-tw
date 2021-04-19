---
description: 在媒體基礎管線模型中，媒體來源會連接到與媒體接收器進一步連線的轉換。
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: 管線層 ASF 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993018"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="30c80-103">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="30c80-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="30c80-104">在媒體基礎的管線模型中，媒體來源會連接到與媒體接收器進一步連線的轉換。</span><span class="sxs-lookup"><span data-stu-id="30c80-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="30c80-105">來源中包含的資料會流經轉換，並在接收中產生輸出媒體範例，以供播放或編碼之用。</span><span class="sxs-lookup"><span data-stu-id="30c80-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="30c80-106">視應用程式是否想要播放 ASF 內容或編碼為 ASF 檔案而定，應用程式必須以不同的方式建立管線。</span><span class="sxs-lookup"><span data-stu-id="30c80-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="30c80-107">下列主題包含管線層元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="30c80-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="30c80-108">ASF 媒體來源</span><span class="sxs-lookup"><span data-stu-id="30c80-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="30c80-109">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="30c80-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="30c80-110">ASF 媒體接收</span><span class="sxs-lookup"><span data-stu-id="30c80-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="30c80-111">用於播放之 ASF 管線的三個主要元件如下：</span><span class="sxs-lookup"><span data-stu-id="30c80-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="30c80-112">ASF 媒體來源是由代表 ASF 檔案媒體基礎提供。</span><span class="sxs-lookup"><span data-stu-id="30c80-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="30c80-113">音訊 resamplers、影片影像 resizers 等， (轉換) </span><span class="sxs-lookup"><span data-stu-id="30c80-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="30c80-114">音訊和影片轉譯器 (接收器) </span><span class="sxs-lookup"><span data-stu-id="30c80-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="30c80-115">如需建立播放管線的詳細資訊，請參閱建立 [播放拓撲](creating-playback-topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="30c80-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="30c80-116">適用于編碼的 ASF 管線的三個主要元件如下：</span><span class="sxs-lookup"><span data-stu-id="30c80-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="30c80-117">媒體來源，代表需要轉換之格式的資料。</span><span class="sxs-lookup"><span data-stu-id="30c80-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="30c80-118">此元件可以是媒體基礎所提供的其中一個預設媒體來源，或是公開 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的自訂來源。</span><span class="sxs-lookup"><span data-stu-id="30c80-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="30c80-119">Windows Media 編碼器 (轉換) ，以執行格式轉換。</span><span class="sxs-lookup"><span data-stu-id="30c80-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="30c80-120">由媒體基礎提供的 ASF 媒體接收器，會在應用程式指定的輸出檔中寫入 ASF 物件和媒體範例。</span><span class="sxs-lookup"><span data-stu-id="30c80-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="30c80-121">管線會在拓撲中表示，而管線中的每個物件會以拓撲節點表示。</span><span class="sxs-lookup"><span data-stu-id="30c80-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="30c80-122">針對播放和編碼，所有的管線作業都是由媒體會話處理。</span><span class="sxs-lookup"><span data-stu-id="30c80-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="30c80-123">媒體會話的職責之一，就是要確保管線具有產生輸出所需的所有元件。</span><span class="sxs-lookup"><span data-stu-id="30c80-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="30c80-124">例如，在編碼管線中，如果音訊來源格式與目標格式不同，則媒體會話會插入其他轉換元件，例如執行適當取樣速率轉換的 resampler。</span><span class="sxs-lookup"><span data-stu-id="30c80-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="30c80-125">透過管線的資料流程控制也會由媒體會話管理。</span><span class="sxs-lookup"><span data-stu-id="30c80-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="30c80-126">在播放案例中，啟動媒體會話時，媒體會話會將範例傳送給 SAR 和 EVR，並將其呈現在輸出裝置上。</span><span class="sxs-lookup"><span data-stu-id="30c80-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="30c80-127">針對編碼，啟動媒體會話會開始編碼程式。</span><span class="sxs-lookup"><span data-stu-id="30c80-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="30c80-128">當編碼完成時，會話會以非同步方式通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="30c80-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="30c80-129">下列主題包含有關使用管線層元件建立編碼拓撲的逐步指示。</span><span class="sxs-lookup"><span data-stu-id="30c80-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="30c80-130">用來讀取和寫入 ASF 檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="30c80-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="30c80-131">教學課程： 1-傳遞 Windows Media 編碼</span><span class="sxs-lookup"><span data-stu-id="30c80-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="30c80-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="30c80-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30c80-133">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="30c80-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



