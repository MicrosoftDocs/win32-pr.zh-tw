---
description: 媒體來源物件模型
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: 媒體來源物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321588"
---
# <a name="media-source-object-model"></a><span data-ttu-id="41080-103">媒體來源物件模型</span><span class="sxs-lookup"><span data-stu-id="41080-103">Media Source Object Model</span></span>

<span data-ttu-id="41080-104">本主題說明 Microsoft 媒體基礎中媒體來源的物件模型。</span><span class="sxs-lookup"><span data-stu-id="41080-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="41080-105">媒體來源必須執行兩個物件：</span><span class="sxs-lookup"><span data-stu-id="41080-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="41080-106">表示來源內容的簡報描述項，包括資料流程的數目和每個資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="41080-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="41080-107">如需簡報描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="41080-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="41080-108">產生來源資料的一或多個媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="41080-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="41080-109">在播放開始之前，來源不會建立資料流程。</span><span class="sxs-lookup"><span data-stu-id="41080-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="41080-110">媒體來源介面</span><span class="sxs-lookup"><span data-stu-id="41080-110">Media Source Interfaces</span></span>

<span data-ttu-id="41080-111">媒體來源必須透過 **QueryInterface** 公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="41080-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="41080-112">介面</span><span class="sxs-lookup"><span data-stu-id="41080-112">Interface</span></span>                                                | <span data-ttu-id="41080-113">描述</span><span class="sxs-lookup"><span data-stu-id="41080-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41080-114">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="41080-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="41080-115">所有媒體來源都需要。</span><span class="sxs-lookup"><span data-stu-id="41080-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="41080-116">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="41080-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="41080-117">所有媒體來源都需要。</span><span class="sxs-lookup"><span data-stu-id="41080-117">Required for all media sources.</span></span> <span data-ttu-id="41080-118">[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)介面會繼承這個介面。</span><span class="sxs-lookup"><span data-stu-id="41080-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="41080-119">（選擇性）媒體來源可以執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面，並將下列任何介面實作為服務：</span><span class="sxs-lookup"><span data-stu-id="41080-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="41080-120">服務介面</span><span class="sxs-lookup"><span data-stu-id="41080-120">Service interface</span></span>                                  | <span data-ttu-id="41080-121">Description</span><span class="sxs-lookup"><span data-stu-id="41080-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="41080-122">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="41080-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="41080-123">控制播放速率。</span><span class="sxs-lookup"><span data-stu-id="41080-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="41080-124">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="41080-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="41080-125">報告支援的播放率範圍。</span><span class="sxs-lookup"><span data-stu-id="41080-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="41080-126">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="41080-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="41080-127">可讓品質管制員調整音訊或影片品質。</span><span class="sxs-lookup"><span data-stu-id="41080-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="41080-128">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="41080-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="41080-129">提供中繼資料。</span><span class="sxs-lookup"><span data-stu-id="41080-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="41080-130">如果媒體來源可 (1.0) 的速率來播放，則應該公開速率控制服務 ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 和 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)) 。</span><span class="sxs-lookup"><span data-stu-id="41080-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="41080-131">否則，假設來源僅支援以正常速度播放。</span><span class="sxs-lookup"><span data-stu-id="41080-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="41080-132">如需詳細資訊，請參閱 [執行速率控制](implementing-rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="41080-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="41080-133">如需服務介面和 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)的詳細資訊，請參閱 [服務介面](service-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="41080-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="41080-134">媒體資料流程介面</span><span class="sxs-lookup"><span data-stu-id="41080-134">Media Stream Interfaces</span></span>

<span data-ttu-id="41080-135">媒體資料流程必須執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="41080-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="41080-136">介面</span><span class="sxs-lookup"><span data-stu-id="41080-136">Interface</span></span>                                                | <span data-ttu-id="41080-137">描述</span><span class="sxs-lookup"><span data-stu-id="41080-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41080-138">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="41080-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="41080-139">所有媒體資料流程都需要。</span><span class="sxs-lookup"><span data-stu-id="41080-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="41080-140">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="41080-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="41080-141">所有媒體資料流程都需要。</span><span class="sxs-lookup"><span data-stu-id="41080-141">Required for all media streams.</span></span> <span data-ttu-id="41080-142">[**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)介面會繼承這個介面。</span><span class="sxs-lookup"><span data-stu-id="41080-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="41080-143">目前沒有針對媒體資料流程定義任何服務介面。</span><span class="sxs-lookup"><span data-stu-id="41080-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41080-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="41080-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41080-145">媒體來源</span><span class="sxs-lookup"><span data-stu-id="41080-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



