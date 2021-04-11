---
description: EVR 媒體類型的協商
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR 媒體類型的協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321559"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="4b068-103">EVR 媒體類型的協商</span><span class="sxs-lookup"><span data-stu-id="4b068-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="4b068-104">本主題說明增強型影片轉譯器 (EVR) 如何驗證媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="4b068-105">針對 DirectShow EVR 篩選準則，當篩選的釘選連線時，就會發生型別協商。</span><span class="sxs-lookup"><span data-stu-id="4b068-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="4b068-106">針對 EVR 媒體接收器，媒體類型是透過資料流程接收上的 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面進行設定。</span><span class="sxs-lookup"><span data-stu-id="4b068-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="4b068-107">拓撲載入器通常會協商媒體類型，但應用程式也可以直接設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="4b068-108">EVR 不會報告任何慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="4b068-109">用戶端必須測試媒體類型，直到找到可接受的類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="4b068-110">您必須先設定參考資料流的媒體類型，才能在任何子串流上設定類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="4b068-111">針對參考資料流，EVR 混音器會取得相容的 DirectX 影片加速清單， (DXVA) 轉譯目標格式。</span><span class="sxs-lookup"><span data-stu-id="4b068-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="4b068-112">EVR 展示者會使用此清單來選取 Direct3D 交換鏈的格式。</span><span class="sxs-lookup"><span data-stu-id="4b068-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="4b068-113">如果找不到相容的轉譯目標格式，EVR 會拒絕媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="4b068-114">針對子串流，EVR 混音器會查詢 DXVA 裝置是否支援該子資料流程格式與針對參考資料流所選取的呈現目標格式。</span><span class="sxs-lookup"><span data-stu-id="4b068-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="4b068-115">因此，可用的子資料流程格式可能會根據參考資料流而變更。</span><span class="sxs-lookup"><span data-stu-id="4b068-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="4b068-116">以下是更詳細的流程。</span><span class="sxs-lookup"><span data-stu-id="4b068-116">Here is the process in more detail.</span></span> <span data-ttu-id="4b068-117">這些詳細資料對大部分的應用程式而言並不重要，但如果您要撰寫自訂的混音器或簡報者，可能會很有説明。</span><span class="sxs-lookup"><span data-stu-id="4b068-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="4b068-118">參考資料流的協商會如下所示：</span><span class="sxs-lookup"><span data-stu-id="4b068-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="4b068-119">EVR 會在混音器上呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 。</span><span class="sxs-lookup"><span data-stu-id="4b068-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="4b068-120">混音器會使用 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構，將媒體類型轉換成 DXVA 2.0 描述。</span><span class="sxs-lookup"><span data-stu-id="4b068-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="4b068-121">混音器會呼叫 [**IDirectXVideoProcessorService：： GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) 來取得影片處理器 guid 清單。</span><span class="sxs-lookup"><span data-stu-id="4b068-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="4b068-122">針對每個視頻處理器 GUID，混音器會呼叫 [**IDirectXVideoProcessorService：： GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) 來取得支援的轉譯目標格式。</span><span class="sxs-lookup"><span data-stu-id="4b068-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="4b068-123">EVR 會使用 MFVP MESSAGE INVALIDATEMEDIATYPE 訊息來呼叫展示者上的 [**IMFVideoPresenter：:P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4b068-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="4b068-124">這則訊息會讓展示者選取新的格式。</span><span class="sxs-lookup"><span data-stu-id="4b068-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="4b068-125">展示者會呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以從混音器取得可用輸出格式的清單。</span><span class="sxs-lookup"><span data-stu-id="4b068-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="4b068-126">混音器會從步驟4中取得的格式產生這份清單。</span><span class="sxs-lookup"><span data-stu-id="4b068-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="4b068-127">展示者會選取一種格式，並在混音器上呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 。</span><span class="sxs-lookup"><span data-stu-id="4b068-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="4b068-128">針對子串流，此程式較簡單：</span><span class="sxs-lookup"><span data-stu-id="4b068-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="4b068-129">EVR 會在混音器上呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 。</span><span class="sxs-lookup"><span data-stu-id="4b068-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="4b068-130">混音器會呼叫 [**IDirectXVideoProcessorService：： GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) 來取得可用的子串流格式清單。</span><span class="sxs-lookup"><span data-stu-id="4b068-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="4b068-131">如果建議的格式包含在此清單中，EVR 會接受輸入類型。</span><span class="sxs-lookup"><span data-stu-id="4b068-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b068-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b068-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b068-133">增強的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="4b068-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



