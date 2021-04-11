---
description: 影片範例
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: 影片範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848694"
---
# <a name="video-samples"></a><span data-ttu-id="9ea93-103">影片範例</span><span class="sxs-lookup"><span data-stu-id="9ea93-103">Video Samples</span></span>

<span data-ttu-id="9ea93-104">影片範例物件是 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的特製化，可搭配 [增強型影片](enhanced-video-renderer.md) 轉譯器 (EVR) 使用。</span><span class="sxs-lookup"><span data-stu-id="9ea93-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="9ea93-105">若要建立這個物件的實例，請呼叫 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) 函數。</span><span class="sxs-lookup"><span data-stu-id="9ea93-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="9ea93-106">函式會接受 Direct3D 介面的指標，並傳回 **IMFSample** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9ea93-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="9ea93-107">下列類型的物件應使用此函數來配置範例：</span><span class="sxs-lookup"><span data-stu-id="9ea93-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="9ea93-108">自訂 EVR 展示者。</span><span class="sxs-lookup"><span data-stu-id="9ea93-108">Custom EVR presenters.</span></span> <span data-ttu-id="9ea93-109">展示者會配置影片範例，並將其傳送至混音器的 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法。</span><span class="sxs-lookup"><span data-stu-id="9ea93-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="9ea93-110">如需詳細資訊，請參閱 [如何撰寫 EVR 的簡報者](how-to-write-an-evr-presenter.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea93-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="9ea93-111">支援影片加速的影片解碼器。</span><span class="sxs-lookup"><span data-stu-id="9ea93-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="9ea93-112">如需詳細資訊，請參閱 [媒體基礎中的支援 DXVA 2.0](supporting-dxva-2-0-in-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea93-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="9ea93-113">影片範例物件會執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="9ea93-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="9ea93-114">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="9ea93-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="9ea93-115">**IMFDesiredSample**</span><span class="sxs-lookup"><span data-stu-id="9ea93-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="9ea93-116">**IMFTrackedSample**</span><span class="sxs-lookup"><span data-stu-id="9ea93-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="9ea93-117">如果 [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface)的 *pUnkSurface* 參數不是 **Null**，則產生的視頻範例會包含封裝 Direct3D 介面的單一媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9ea93-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="9ea93-118">這個緩衝區物件的功能有限：</span><span class="sxs-lookup"><span data-stu-id="9ea93-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="9ea93-119">緩衝區的 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 方法會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="9ea93-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="9ea93-120">緩衝區不會執行 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="9ea93-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="9ea93-121">從緩衝區存取介面的唯一方法是使用服務識別碼 MR 緩衝區服務來呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="9ea93-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="9ea93-122">如果 *pUnkSurface* 參數為 **Null**，則會以零個媒體緩衝區來建立影片範例。</span><span class="sxs-lookup"><span data-stu-id="9ea93-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="9ea93-123">若要在範例中新增緩衝區，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="9ea93-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="9ea93-124">建立 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="9ea93-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="9ea93-125">藉由呼叫 [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer)來建立介面緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9ea93-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="9ea93-126">如需詳細資訊，請參閱 [DirectX 介面緩衝區](directx-surface-buffer.md)。</span><span class="sxs-lookup"><span data-stu-id="9ea93-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="9ea93-127">藉由呼叫 [**IMFSample：： AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)，將緩衝區新增至範例。</span><span class="sxs-lookup"><span data-stu-id="9ea93-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="9ea93-128">如果您需要可透過 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面存取 surface 記憶體，請使用此方法。</span><span class="sxs-lookup"><span data-stu-id="9ea93-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ea93-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ea93-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea93-130">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="9ea93-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="9ea93-131">媒體範例</span><span class="sxs-lookup"><span data-stu-id="9ea93-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
