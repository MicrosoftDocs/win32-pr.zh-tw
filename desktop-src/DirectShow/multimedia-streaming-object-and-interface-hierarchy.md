---
description: 多媒體串流物件和介面階層
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: 多媒體串流物件和介面階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853495"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="30dc5-103">多媒體串流物件和介面階層</span><span class="sxs-lookup"><span data-stu-id="30dc5-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="30dc5-104">這些 Api 已被取代。</span><span class="sxs-lookup"><span data-stu-id="30dc5-104">These APIs are deprecated.</span></span> <span data-ttu-id="30dc5-105">應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。</span><span class="sxs-lookup"><span data-stu-id="30dc5-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="30dc5-106">下圖顯示多媒體串流中使用的物件階層。</span><span class="sxs-lookup"><span data-stu-id="30dc5-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![multimediastreaming 物件階層](images/mmstream02.png)

<span data-ttu-id="30dc5-108">多媒體串流架構會定義三種一般類型的物件：</span><span class="sxs-lookup"><span data-stu-id="30dc5-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="30dc5-109">**AMMultimediaStream** 物件會公開 [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)介面。</span><span class="sxs-lookup"><span data-stu-id="30dc5-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="30dc5-110">就內部而言，此物件會包裝 DirectShow 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="30dc5-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="30dc5-111">*媒體資料流程* 物件會公開 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) 介面，並且是特定資料。</span><span class="sxs-lookup"><span data-stu-id="30dc5-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="30dc5-112">AMMultimediaStream 物件包含一或多個媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="30dc5-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="30dc5-113">*Stream 範例* 物件包含特定資料流程的資料。</span><span class="sxs-lookup"><span data-stu-id="30dc5-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="30dc5-114">支援下列媒體資料流程物件：</span><span class="sxs-lookup"><span data-stu-id="30dc5-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="30dc5-115">音訊串流。</span><span class="sxs-lookup"><span data-stu-id="30dc5-115">Audio stream.</span></span> <span data-ttu-id="30dc5-116">公開 [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) 介面。</span><span class="sxs-lookup"><span data-stu-id="30dc5-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="30dc5-117">DirectDraw 資料流程。</span><span class="sxs-lookup"><span data-stu-id="30dc5-117">DirectDraw stream.</span></span> <span data-ttu-id="30dc5-118">表示轉譯為 DirectDraw 表面的影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="30dc5-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="30dc5-119">公開 [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) 介面。</span><span class="sxs-lookup"><span data-stu-id="30dc5-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="30dc5-120">媒體類型資料流程。</span><span class="sxs-lookup"><span data-stu-id="30dc5-120">Media type stream.</span></span> <span data-ttu-id="30dc5-121">代表任意資料。</span><span class="sxs-lookup"><span data-stu-id="30dc5-121">Represents arbitrary data.</span></span> <span data-ttu-id="30dc5-122">公開 [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) 介面。</span><span class="sxs-lookup"><span data-stu-id="30dc5-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="30dc5-123">每個媒體資料流程物件都會建立自己的資料流程範例物件：</span><span class="sxs-lookup"><span data-stu-id="30dc5-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="30dc5-124">音訊串流會建立可公開 [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) 介面的音訊範例。</span><span class="sxs-lookup"><span data-stu-id="30dc5-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="30dc5-125">DirectDraw 資料流程會建立 DirectDraw 範例，以公開 [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) 介面。</span><span class="sxs-lookup"><span data-stu-id="30dc5-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="30dc5-126">媒體類型資料流程會建立可公開 [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) 介面的媒體類型範例。</span><span class="sxs-lookup"><span data-stu-id="30dc5-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="30dc5-127">下圖顯示先前所列介面的介面階層：</span><span class="sxs-lookup"><span data-stu-id="30dc5-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![multimediastreaming 介面階層](images/mmstream01.png)

 

 



