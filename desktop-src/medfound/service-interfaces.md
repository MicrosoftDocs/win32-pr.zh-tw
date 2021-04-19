---
description: 服務介面
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: 服務介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976786"
---
# <a name="service-interfaces"></a><span data-ttu-id="61a83-103">服務介面</span><span class="sxs-lookup"><span data-stu-id="61a83-103">Service Interfaces</span></span>

<span data-ttu-id="61a83-104">媒體基礎中的某些介面必須藉由呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得，而不是呼叫 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="61a83-104">Some interfaces in Media Foundation must be obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) instead of by calling **QueryInterface**.</span></span> <span data-ttu-id="61a83-105">[**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)方法的運作方式類似于 QueryInterface，但有下列差異：</span><span class="sxs-lookup"><span data-stu-id="61a83-105">The [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) method works like QueryInterface, but with the following differences:</span></span>

-   <span data-ttu-id="61a83-106">除了介面識別碼之外，還會採用服務識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="61a83-106">It takes a service identifier GUID in addition to the interface identifier.</span></span>
-   <span data-ttu-id="61a83-107">它可以傳回另一個物件的指標，該物件會實介面，而不是傳回所查詢之原始物件的指標。</span><span class="sxs-lookup"><span data-stu-id="61a83-107">It can return a pointer to another object that implements the interface, instead of returning a pointer to the original object that is queried.</span></span>

> [!Note]  
> <span data-ttu-id="61a83-108">[**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)介面非常類似于一些其他 api 中使用的 **IServiceProvider** 介面。</span><span class="sxs-lookup"><span data-stu-id="61a83-108">The [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface is very similar to the **IServiceProvider** interface used in some other APIs.</span></span>

 

<span data-ttu-id="61a83-109">*服務* 是透過 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)介面從特定物件類別取得的特定介面。</span><span class="sxs-lookup"><span data-stu-id="61a83-109">A *service* is a particular interface obtained from a particular class of objects through the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="61a83-110">定義了下列服務。</span><span class="sxs-lookup"><span data-stu-id="61a83-110">The following services are defined.</span></span>



| <span data-ttu-id="61a83-111">服務識別碼</span><span class="sxs-lookup"><span data-stu-id="61a83-111">Service identifier</span></span>                          | <span data-ttu-id="61a83-112">介面</span><span class="sxs-lookup"><span data-stu-id="61a83-112">Interface</span></span>                                                                                                                                | <span data-ttu-id="61a83-113">可能公開此服務的物件</span><span class="sxs-lookup"><span data-stu-id="61a83-113">Objects that might expose this service</span></span>                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a83-114">MF \_ 中繼資料 \_ 提供者 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-114">MF\_METADATA\_PROVIDER\_SERVICE</span></span>             | [<span data-ttu-id="61a83-115">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="61a83-115">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | <span data-ttu-id="61a83-116">媒體來源</span><span class="sxs-lookup"><span data-stu-id="61a83-116">Media sources</span></span>                                                                                                                                     |
| <span data-ttu-id="61a83-117">MF \_ MEDIASOURCE \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-117">MF\_MEDIASOURCE\_SERVICE</span></span>                    | [<span data-ttu-id="61a83-118">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="61a83-118">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | <span data-ttu-id="61a83-119">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="61a83-119">Supported in Windows 8.1 and later.</span></span><br/>                                                                                                    |
| <span data-ttu-id="61a83-120">MF \_ PMP \_ 伺服器 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="61a83-120">MF\_PMP\_SERVER\_CONTEXT</span></span>                    | [<span data-ttu-id="61a83-121">**IMFPMPServer**</span><span class="sxs-lookup"><span data-stu-id="61a83-121">**IMFPMPServer**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | <span data-ttu-id="61a83-122"> (PMP) 媒體會話的受保護媒體路徑。</span><span class="sxs-lookup"><span data-stu-id="61a83-122">Protected media path (PMP) Media Session.</span></span>                                                                                                         |
| <span data-ttu-id="61a83-123">MF \_ 品質 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-123">MF\_QUALITY\_SERVICES</span></span>                       | [<span data-ttu-id="61a83-124">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="61a83-124">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | <span data-ttu-id="61a83-125">媒體來源。</span><span class="sxs-lookup"><span data-stu-id="61a83-125">Media sources.</span></span>                                                                                                                                    |
| <span data-ttu-id="61a83-126">MF \_ 速率 \_ 控制 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-126">MF\_RATE\_CONTROL\_SERVICE</span></span>                  | [<span data-ttu-id="61a83-127">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="61a83-127">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | <span data-ttu-id="61a83-128">媒體來源、媒體會話</span><span class="sxs-lookup"><span data-stu-id="61a83-128">Media sources, Media Session</span></span>                                                                                                                      |
| <span data-ttu-id="61a83-129">MF \_ 速率 \_ 控制 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-129">MF\_RATE\_CONTROL\_SERVICE</span></span>                  | [<span data-ttu-id="61a83-130">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="61a83-130">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | <span data-ttu-id="61a83-131">媒體來源、媒體接收器、媒體會話</span><span class="sxs-lookup"><span data-stu-id="61a83-131">Media sources, media sinks, Media Session</span></span>                                                                                                         |
| <span data-ttu-id="61a83-132">MF \_ 遠端 \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="61a83-132">MF\_REMOTE\_PROXY</span></span>                           | [<span data-ttu-id="61a83-133">**IMFRemoteProxy**</span><span class="sxs-lookup"><span data-stu-id="61a83-133">**IMFRemoteProxy**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | <span data-ttu-id="61a83-134">遠端物件的 proxy。</span><span class="sxs-lookup"><span data-stu-id="61a83-134">Proxies for remote objects.</span></span>                                                                                                                       |
| <span data-ttu-id="61a83-135">MF \_ 薩米文 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-135">MF\_SAMI\_SERVICE</span></span>                           | [<span data-ttu-id="61a83-136">**IMFSAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="61a83-136">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | <span data-ttu-id="61a83-137">已同步的可存取媒體交換 (薩米) 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="61a83-137">Synchronized Accessible Media Interchange (SAMI) media source.</span></span>                                                                                    |
| <span data-ttu-id="61a83-138">MF \_ 來源 \_ 表示 \_ 提供者 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-138">MF\_SOURCE\_PRESENTATION\_PROVIDER\_SERVICE</span></span> | [<span data-ttu-id="61a83-139">**IMFMediaSourcePresentationProvider**</span><span class="sxs-lookup"><span data-stu-id="61a83-139">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | <span data-ttu-id="61a83-140">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="61a83-140">Sequencer source</span></span>                                                                                                                                  |
| <span data-ttu-id="61a83-141">MF 時間 \_ 碼 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-141">MF\_TIMECODE\_SERVICE</span></span>                       | [<span data-ttu-id="61a83-142">**IMFTimecodeTranslate**</span><span class="sxs-lookup"><span data-stu-id="61a83-142">**IMFTimecodeTranslate**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | <span data-ttu-id="61a83-143">ASF 媒體來源。</span><span class="sxs-lookup"><span data-stu-id="61a83-143">ASF media source.</span></span>                                                                                                                                 |
| <span data-ttu-id="61a83-144">MF \_ TOPONODE \_ 屬性 \_ 編輯器 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-144">MF\_TOPONODE\_ATTRIBUTE\_EDITOR\_SERVICE</span></span>    | [<span data-ttu-id="61a83-145">**IMFTopologyNodeAttributeEditor**</span><span class="sxs-lookup"><span data-stu-id="61a83-145">**IMFTopologyNodeAttributeEditor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | <span data-ttu-id="61a83-146">媒體工作階段</span><span class="sxs-lookup"><span data-stu-id="61a83-146">Media session</span></span>                                                                                                                                     |
| <span data-ttu-id="61a83-147">MF \_ 包裝 \_ 物件</span><span class="sxs-lookup"><span data-stu-id="61a83-147">MF\_WRAPPED\_OBJECT</span></span>                         | [<span data-ttu-id="61a83-148">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="61a83-148">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | <span data-ttu-id="61a83-149">包裝的物件</span><span class="sxs-lookup"><span data-stu-id="61a83-149">Wrapped objects</span></span>                                                                                                                                   |
| <span data-ttu-id="61a83-150">MF \_ 包裝 \_ 緩衝區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-150">MF\_WRAPPED\_BUFFER\_SERVICE</span></span>                |                                                                                                                                          | <span data-ttu-id="61a83-151">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="61a83-151">Supported in Windows 8.1 and later.</span></span><br/>                                                                                                    |
| <span data-ttu-id="61a83-152">MF \_ 包裝 \_ 範例 \_ SERVIC</span><span class="sxs-lookup"><span data-stu-id="61a83-152">MF\_WRAPPED\_SAMPLE\_SERVIC</span></span>                 |                                                                                                                                          | <span data-ttu-id="61a83-153">在 Windows 8.1 和更新版本中支援。</span><span class="sxs-lookup"><span data-stu-id="61a83-153">Supported in Windows 8.1 and later.</span></span><br/>                                                                                                    |
| <span data-ttu-id="61a83-154">MF \_ WORKQUEUE \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-154">MF\_WORKQUEUE\_SERVICES</span></span>                     | [<span data-ttu-id="61a83-155">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="61a83-155">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | <span data-ttu-id="61a83-156">媒體工作階段</span><span class="sxs-lookup"><span data-stu-id="61a83-156">Media session</span></span>                                                                                                                                     |
| <span data-ttu-id="61a83-157">MFNET \_ SAVEJOB \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-157">MFNET\_SAVEJOB\_SERVICE</span></span>                     | [<span data-ttu-id="61a83-158">**IMFSaveJob**</span><span class="sxs-lookup"><span data-stu-id="61a83-158">**IMFSaveJob**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | <span data-ttu-id="61a83-159">位元組資料流程</span><span class="sxs-lookup"><span data-stu-id="61a83-159">Byte streams</span></span>                                                                                                                                      |
| <span data-ttu-id="61a83-160">MFNETSOURCE \_ 統計資料 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-160">MFNETSOURCE\_STATISTICS\_SERVICE</span></span>            | <span data-ttu-id="61a83-161">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="61a83-161">**IPropertyStore**</span></span>                                                                                                                       | <span data-ttu-id="61a83-162">網路來源。</span><span class="sxs-lookup"><span data-stu-id="61a83-162">Network source.</span></span> <span data-ttu-id="61a83-163">使用此服務來取得網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="61a83-163">Use this service to retrieve network statistics.</span></span> <span data-ttu-id="61a83-164">請參閱 [**MFNETSOURCE \_ STATISTICS 屬性**](mfnetsource-statistics-property.md)。</span><span class="sxs-lookup"><span data-stu-id="61a83-164">See [**MFNETSOURCE\_STATISTICS Property**](mfnetsource-statistics-property.md).</span></span> |
| <span data-ttu-id="61a83-165">MR \_ 音訊 \_ 原則 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-165">MR\_AUDIO\_POLICY\_SERVICE</span></span>                  | [<span data-ttu-id="61a83-166">**IMFAudioPolicy**</span><span class="sxs-lookup"><span data-stu-id="61a83-166">**IMFAudioPolicy**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | <span data-ttu-id="61a83-167">音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="61a83-167">Audio renderer</span></span>                                                                                                                                    |
| <span data-ttu-id="61a83-168">MR \_ 緩衝區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-168">MR\_BUFFER\_SERVICE</span></span>                         | <span data-ttu-id="61a83-169">**IDirect3DSurface9**</span><span class="sxs-lookup"><span data-stu-id="61a83-169">**IDirect3DSurface9**</span></span>                                                                                                                    | <span data-ttu-id="61a83-170">DirectX 介面緩衝區</span><span class="sxs-lookup"><span data-stu-id="61a83-170">DirectX surface buffers</span></span>                                                                                                                           |
| <span data-ttu-id="61a83-171">MR \_ CAPTURE \_ 原則 \_ 磁片區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-171">MR\_CAPTURE\_POLICY\_VOLUME\_SERVICE</span></span>        | [<span data-ttu-id="61a83-172">**IMFSimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="61a83-172">**IMFSimpleAudioVolume**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | <span data-ttu-id="61a83-173">音訊捕獲來源</span><span class="sxs-lookup"><span data-stu-id="61a83-173">Audio capture source</span></span>                                                                                                                              |
| <span data-ttu-id="61a83-174">MR \_ 原則 \_ 磁片區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-174">MR\_POLICY\_VOLUME\_SERVICE</span></span>                 | [<span data-ttu-id="61a83-175">**IMFSimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="61a83-175">**IMFSimpleAudioVolume**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | <span data-ttu-id="61a83-176">音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="61a83-176">Audio renderer</span></span>                                                                                                                                    |
| <span data-ttu-id="61a83-177">MR \_ 串流處理 \_ 大量 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-177">MR\_STREAM\_VOLUME\_SERVICE</span></span>                 | [<span data-ttu-id="61a83-178">**IMFAudioStreamVolume**</span><span class="sxs-lookup"><span data-stu-id="61a83-178">**IMFAudioStreamVolume**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | <span data-ttu-id="61a83-179">音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="61a83-179">Audio renderer</span></span>                                                                                                                                    |
| <span data-ttu-id="61a83-180">MR \_ 影片 \_ 加速 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-180">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>            | <span data-ttu-id="61a83-181">[**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)、 [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)</span><span class="sxs-lookup"><span data-stu-id="61a83-181">[**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)</span></span> | <span data-ttu-id="61a83-182">增強的影片轉譯器 (EVR) </span><span class="sxs-lookup"><span data-stu-id="61a83-182">Enhanced video renderer (EVR)</span></span>                                                                                                                     |
| <span data-ttu-id="61a83-183">MR \_ 影片 \_ 加速 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-183">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>            | [<span data-ttu-id="61a83-184">**IDirectXVideoMemoryConfiguration**</span><span class="sxs-lookup"><span data-stu-id="61a83-184">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | <span data-ttu-id="61a83-185">DirectShow EVR 篩選器上的輸入釘</span><span class="sxs-lookup"><span data-stu-id="61a83-185">Input pins on the DirectShow EVR filter</span></span>                                                                                                           |
| <span data-ttu-id="61a83-186">MR \_ 影片 \_ 加速 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-186">MR\_VIDEO\_ACCELERATION\_SERVICE</span></span>            | [<span data-ttu-id="61a83-187">**IMFVideoSampleAllocator 介面**</span><span class="sxs-lookup"><span data-stu-id="61a83-187">**IMFVideoSampleAllocator Interface**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | <span data-ttu-id="61a83-188">EVR 資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="61a83-188">EVR stream sinks.</span></span>                                                                                                                                 |
| <span data-ttu-id="61a83-189">MR \_ 影片 \_ 混音器 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-189">MR\_VIDEO\_MIXER\_SERVICE</span></span>                   | <span data-ttu-id="61a83-190">EVR 混音器所公開的各種介面。</span><span class="sxs-lookup"><span data-stu-id="61a83-190">Various interfaces exposed by the EVR mixer.</span></span> <span data-ttu-id="61a83-191">請參閱 [使用影片混音器控制項](using-the-video-mixer-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="61a83-191">See [Using the Video Mixer Controls](using-the-video-mixer-controls.md).</span></span>                   | <span data-ttu-id="61a83-192">EVR</span><span class="sxs-lookup"><span data-stu-id="61a83-192">EVR</span></span>                                                                                                                                               |
| <span data-ttu-id="61a83-193">MR \_ 影片 \_ 轉譯 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="61a83-193">MR\_VIDEO\_RENDER\_SERVICE</span></span>                  | <span data-ttu-id="61a83-194">EVR 展示者公開的各種介面。</span><span class="sxs-lookup"><span data-stu-id="61a83-194">Various interfaces exposed by the EVR presenter.</span></span> <span data-ttu-id="61a83-195">請參閱 [使用影片顯示控制項](using-the-video-display-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="61a83-195">See [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>           | <span data-ttu-id="61a83-196">EVR</span><span class="sxs-lookup"><span data-stu-id="61a83-196">EVR</span></span>                                                                                                                                               |



 

<span data-ttu-id="61a83-197">您必須使用 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 從下表所列的物件取得此資料表中所列的介面。</span><span class="sxs-lookup"><span data-stu-id="61a83-197">You must use [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the interfaces listed in this table from the objects listed in this table.</span></span>

<span data-ttu-id="61a83-198">在某些情況下，介面會由一個物件類別以服務的形式傳回，並由另一個物件類別透過 **QueryInterface** 傳回。</span><span class="sxs-lookup"><span data-stu-id="61a83-198">In some cases, an interface is returned as a service by one class of objects, and returned through **QueryInterface** by another class of objects.</span></span> <span data-ttu-id="61a83-199">每個介面的參考頁面會指出何時使用 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 以及何時使用 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="61a83-199">The reference pages for each interface indicate when to use [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) and when to use **QueryInterface**.</span></span>

> [!Caution]  
> <span data-ttu-id="61a83-200">物件可能會以透過 **QueryInterface** 和 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)傳回服務介面的方式來執行。</span><span class="sxs-lookup"><span data-stu-id="61a83-200">An object might be implemented in such a way that it returns a service interface through **QueryInterface** as well as [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="61a83-201">不過，在需要 **GetService** 時使用 **QueryInterface** 可能會在稍後導致相容性問題。</span><span class="sxs-lookup"><span data-stu-id="61a83-201">However, using **QueryInterface** when **GetService** is required might lead to compatibility problems later.</span></span>

 

<span data-ttu-id="61a83-202">[**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)函式是協助程式函數，可查詢物件的 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ，然後呼叫物件的 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)方法。</span><span class="sxs-lookup"><span data-stu-id="61a83-202">The [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function is a helper function that queries an object for [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) and then calls the object's [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method.</span></span>

## <a name="examples"></a><span data-ttu-id="61a83-203">範例</span><span class="sxs-lookup"><span data-stu-id="61a83-203">Examples</span></span>

<span data-ttu-id="61a83-204">下列範例會查詢媒體會話中的 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ，並取得 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="61a83-204">The following example queries the Media Session for [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) and gets the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



<span data-ttu-id="61a83-205">下列範例相當於前一個範例，但使用 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) 函式。</span><span class="sxs-lookup"><span data-stu-id="61a83-205">The following example is equivalent to the previous example but uses the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function.</span></span>


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a><span data-ttu-id="61a83-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="61a83-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61a83-207">**IMFGetService 介面**</span><span class="sxs-lookup"><span data-stu-id="61a83-207">**IMFGetService Interface**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[<span data-ttu-id="61a83-208">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="61a83-208">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 




