---
description: 以媒體會話使用媒體來源
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: 以媒體會話使用媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945634"
---
# <a name="using-media-sources-with-the-media-session"></a><span data-ttu-id="c8134-103">以媒體會話使用媒體來源</span><span class="sxs-lookup"><span data-stu-id="c8134-103">Using Media Sources with the Media Session</span></span>

<span data-ttu-id="c8134-104">如果您使用媒體會話來控制播放，您應該在媒體來源上呼叫的一組方法會受到限制。</span><span class="sxs-lookup"><span data-stu-id="c8134-104">If you are using the Media Session to control playback, the set of methods that you should call on a media source is restricted.</span></span> <span data-ttu-id="c8134-105">本節說明如何搭配媒體會話使用媒體來源。</span><span class="sxs-lookup"><span data-stu-id="c8134-105">This section describes how to use media source in conjunction with the Media Session.</span></span>

<span data-ttu-id="c8134-106">以下是您的應用程式將執行的基本步驟：</span><span class="sxs-lookup"><span data-stu-id="c8134-106">Here are the basic steps your application will perform:</span></span>

1.  <span data-ttu-id="c8134-107">建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="c8134-107">Create the media source.</span></span> <span data-ttu-id="c8134-108">若要建立媒體來源，請使用來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="c8134-108">To create a media source, use the source resolver.</span></span> <span data-ttu-id="c8134-109">如需詳細資訊，請參閱 [來源解析程式](source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="c8134-109">For more information, see [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="c8134-110">來源解析程式會傳回來源 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c8134-110">The source resolver returns a pointer to the source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="c8134-111"> (如果您已經撰寫自訂媒體來源，則可以改為提供自訂的建立方法。 ) </span><span class="sxs-lookup"><span data-stu-id="c8134-111">(If you have written a custom media source, you can provide a custom creation method instead.)</span></span>

2.  <span data-ttu-id="c8134-112">設定簡報。</span><span class="sxs-lookup"><span data-stu-id="c8134-112">Configure the presentation.</span></span> <span data-ttu-id="c8134-113">若要設定來源的簡報，請呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="c8134-113">To configure the source's presentation, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="c8134-114">您可以修改此複本，但在播放開始之前，這些變更不會變成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="c8134-114">You can modify this copy, but the changes do not become active until the playback starts.</span></span> <span data-ttu-id="c8134-115">播放期間請勿修改簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="c8134-115">Do not modify the presentation descriptor during playback.</span></span> <span data-ttu-id="c8134-116">如需詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。</span><span class="sxs-lookup"><span data-stu-id="c8134-116">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

3.  <span data-ttu-id="c8134-117">建立包含媒體來源的拓撲。</span><span class="sxs-lookup"><span data-stu-id="c8134-117">Create a topology that contains the media source.</span></span> <span data-ttu-id="c8134-118">如需詳細資訊，請參閱 [拓撲](topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="c8134-118">For more information, see [Topologies](topologies.md).</span></span>

4.  <span data-ttu-id="c8134-119">使用媒體會話來控制播放。</span><span class="sxs-lookup"><span data-stu-id="c8134-119">Use the Media Session to control playback.</span></span> <span data-ttu-id="c8134-120">媒體會話會呼叫媒體來源上的方法。</span><span class="sxs-lookup"><span data-stu-id="c8134-120">The Media Session calls methods on the media source.</span></span> <span data-ttu-id="c8134-121">應用程式目前不應呼叫媒體來源上的任何方法。</span><span class="sxs-lookup"><span data-stu-id="c8134-121">The application should not call any methods on the media source at this time.</span></span>

5.  <span data-ttu-id="c8134-122">釋放媒體來源之前，請呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 以關閉來源。</span><span class="sxs-lookup"><span data-stu-id="c8134-122">Before releasing the media source, call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the source.</span></span>

    > [!Note]  
    > <span data-ttu-id="c8134-123">如果您使用 sequencer 來源，sequencer 來源會處理關閉區段來源的工作。</span><span class="sxs-lookup"><span data-stu-id="c8134-123">If you are using the sequencer source, the sequencer source handles shutting down the segment sources.</span></span> <span data-ttu-id="c8134-124">如需詳細資訊，請參閱 [Sequencer 來源](sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="c8134-124">For more information, see [Sequencer Source](sequencer-source.md).</span></span>

     

<span data-ttu-id="c8134-125">如果您使用媒體會話，您應該在媒體來源上呼叫的唯一方法是 [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)、 [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)和 [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)。</span><span class="sxs-lookup"><span data-stu-id="c8134-125">If you use the Media Session, the only methods that you should call on the media source are [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics), and [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span> <span data-ttu-id="c8134-126">尤其是：</span><span class="sxs-lookup"><span data-stu-id="c8134-126">In particular:</span></span>

-   <span data-ttu-id="c8134-127">請勿呼叫 [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)、 [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)或 [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop);這些方法只能由媒體會話呼叫。</span><span class="sxs-lookup"><span data-stu-id="c8134-127">Do not call [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause), or [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); these methods should be called only by the Media Session.</span></span>

-   <span data-ttu-id="c8134-128">請勿呼叫任何 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 方法。</span><span class="sxs-lookup"><span data-stu-id="c8134-128">Do not call any [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) methods.</span></span>

-   <span data-ttu-id="c8134-129">請勿直接從媒體來源或任何資料流程取得事件。</span><span class="sxs-lookup"><span data-stu-id="c8134-129">Do not retrieve events directly from the media source or any of the streams.</span></span> <span data-ttu-id="c8134-130">媒體會話必須接收這些事件，管線才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="c8134-130">The Media Session must receive these events for the pipeline to function correctly.</span></span> <span data-ttu-id="c8134-131">媒體會話轉送應用程式所需的任何事件。</span><span class="sxs-lookup"><span data-stu-id="c8134-131">The Media Session forwards any events that are needed by the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8134-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8134-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8134-133">媒體會話</span><span class="sxs-lookup"><span data-stu-id="c8134-133">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



