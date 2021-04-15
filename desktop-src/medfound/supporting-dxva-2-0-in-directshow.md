---
description: 本主題說明如何在 DirectShow 解碼器篩選器中支援 (DXVA) 2.0 的 DirectX 影片加速。
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: 支援 DirectShow 中的 DXVA 2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848435"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="48cd9-103">支援 DirectShow 中的 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="48cd9-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="48cd9-104">本主題說明如何在 DirectShow 解碼器篩選器中支援 (DXVA) 2.0 的 DirectX 影片加速。</span><span class="sxs-lookup"><span data-stu-id="48cd9-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="48cd9-105">具體而言，它會描述解碼器與影片轉譯器之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="48cd9-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="48cd9-106">本主題不會說明如何執行 DXVA 解碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="48cd9-107">先決條件</span><span class="sxs-lookup"><span data-stu-id="48cd9-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="48cd9-108">遷移注意事項</span><span class="sxs-lookup"><span data-stu-id="48cd9-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="48cd9-109">尋找解碼器設定</span><span class="sxs-lookup"><span data-stu-id="48cd9-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="48cd9-110">通知影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="48cd9-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="48cd9-111">配置未壓縮的緩衝區</span><span class="sxs-lookup"><span data-stu-id="48cd9-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="48cd9-112">解碼</span><span class="sxs-lookup"><span data-stu-id="48cd9-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="48cd9-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="48cd9-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="48cd9-114">必要條件</span><span class="sxs-lookup"><span data-stu-id="48cd9-114">Prerequisites</span></span>

<span data-ttu-id="48cd9-115">本主題假設您已熟悉撰寫 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="48cd9-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="48cd9-116">如需詳細資訊，請參閱 DirectShow SDK 檔中的 [撰寫 Directshow 篩選器](../directshow/writing-directshow-filters.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="48cd9-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="48cd9-117">本主題中的程式碼範例假設已使用下列類別定義衍生自 [**CTransformFilter**](../directshow/ctransformfilter.md) 類別的解碼器篩選準則：</span><span class="sxs-lookup"><span data-stu-id="48cd9-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="48cd9-118">在本主題的其餘部分，「 *解碼* 」一詞指的是「解碼」篩選器，它會接收壓縮的影片並輸出未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="48cd9-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="48cd9-119">「 *解碼* 」一詞是指由圖形驅動程式所執行的硬體視頻加速器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="48cd9-120">以下是「解碼」篩選準則必須執行以支援 DXVA 2.0 的基本步驟：</span><span class="sxs-lookup"><span data-stu-id="48cd9-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="48cd9-121">協商媒體類型。</span><span class="sxs-lookup"><span data-stu-id="48cd9-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="48cd9-122">尋找 DXVA 的解碼器設定。</span><span class="sxs-lookup"><span data-stu-id="48cd9-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="48cd9-123">使用 DXVA 解碼通知影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="48cd9-124">提供可配置 Direct3D 表面的自訂配置器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="48cd9-125">本主題的其餘部分將更詳細地描述這些步驟。</span><span class="sxs-lookup"><span data-stu-id="48cd9-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="48cd9-126">遷移注意事項</span><span class="sxs-lookup"><span data-stu-id="48cd9-126">Migration Notes</span></span>

<span data-ttu-id="48cd9-127">如果您要從 DXVA 1.0 進行遷移，您應該注意這兩個版本之間的一些重大差異：</span><span class="sxs-lookup"><span data-stu-id="48cd9-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="48cd9-128">DXVA 2.0 不會使用 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) 和 [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) 介面，因為此解碼器可以直接透過 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 介面存取 DXVA 2.0 api。</span><span class="sxs-lookup"><span data-stu-id="48cd9-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="48cd9-129">在媒體類型協商期間，解碼器不會使用影片加速 GUID 做為子類型。</span><span class="sxs-lookup"><span data-stu-id="48cd9-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="48cd9-130">相反地，子類型只是未壓縮的影片格式 (例如 NV12) ，如同軟體解碼一樣。</span><span class="sxs-lookup"><span data-stu-id="48cd9-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="48cd9-131">設定加速器的程式已變更。</span><span class="sxs-lookup"><span data-stu-id="48cd9-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="48cd9-132">在 DXVA 1.0 中，使用 **DXVA \_ ConfigPictureDecode** 結構來 **執行** 的解碼器呼叫會設定 accerlator。</span><span class="sxs-lookup"><span data-stu-id="48cd9-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="48cd9-133">在 DXVA 2.0 中，此解碼器會使用 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面，如下一節中所述。</span><span class="sxs-lookup"><span data-stu-id="48cd9-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="48cd9-134">此解碼會配置未壓縮的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="48cd9-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="48cd9-135">影片轉譯器不再配置它們。</span><span class="sxs-lookup"><span data-stu-id="48cd9-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="48cd9-136">除了呼叫 [**IAMVideoAccelerator：:D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) 來顯示已解碼的框架，解碼器也會藉由呼叫 [**IMemInputPin：： Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive)將框架傳遞到轉譯器，如同軟體解碼一樣。</span><span class="sxs-lookup"><span data-stu-id="48cd9-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="48cd9-137">當資料緩衝區可以安全地進行更新時，此解碼器不再負責檢查。</span><span class="sxs-lookup"><span data-stu-id="48cd9-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="48cd9-138">因此，DXVA 2.0 沒有任何相當於 [**IAMVideoAccelerator：： QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)的方法。</span><span class="sxs-lookup"><span data-stu-id="48cd9-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="48cd9-139">子圖片混色是由影片轉譯器使用 DXVA 2.0 video 處理器 Api 來完成。</span><span class="sxs-lookup"><span data-stu-id="48cd9-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="48cd9-140">提供 subpictures (的解碼器例如，DVD 解碼器) 應該會在個別的輸出 pin 上傳送子圖片的資料。</span><span class="sxs-lookup"><span data-stu-id="48cd9-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="48cd9-141">針對解碼作業，DXVA 2.0 使用與 DXVA 1.0 相同的資料結構。</span><span class="sxs-lookup"><span data-stu-id="48cd9-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="48cd9-142">增強型影片轉譯器 (EVR) 篩選器支援 DXVA 2.0。</span><span class="sxs-lookup"><span data-stu-id="48cd9-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="48cd9-143">影片混合轉譯器篩選 (VMR-7 和 VMR-9) 僅支援 DXVA 1.0。</span><span class="sxs-lookup"><span data-stu-id="48cd9-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="48cd9-144">尋找解碼器設定</span><span class="sxs-lookup"><span data-stu-id="48cd9-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="48cd9-145">在解碼器協商輸出媒體類型之後，它必須找到 DXVA 解碼器裝置的相容設定。</span><span class="sxs-lookup"><span data-stu-id="48cd9-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="48cd9-146">您可以在輸出釘選的 [**CBaseOutputPin：： CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) 方法內執行這個步驟。</span><span class="sxs-lookup"><span data-stu-id="48cd9-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="48cd9-147">此步驟可確保在使用 DXVA 認可之前，圖形驅動程式支援該解碼器所需的功能。</span><span class="sxs-lookup"><span data-stu-id="48cd9-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="48cd9-148">若要尋找適用于解碼器裝置的設定，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="48cd9-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="48cd9-149">查詢轉譯器的輸入圖釘以取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="48cd9-150">呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="48cd9-151">服務 GUID 是 MR \_ 影片 \_ 加速 \_ 服務。</span><span class="sxs-lookup"><span data-stu-id="48cd9-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="48cd9-152">呼叫 [**IDirect3DDeviceManager9：： OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) 來取得轉譯器之 Direct3D 裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="48cd9-153">呼叫 [**IDirect3DDeviceManager9：： GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) ，並傳入裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="48cd9-154">這個方法會傳回 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="48cd9-155">呼叫 [**IDirectXVideoDecoderService：： GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids)。</span><span class="sxs-lookup"><span data-stu-id="48cd9-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="48cd9-156">這個方法會傳回一組解碼裝置 Guid。</span><span class="sxs-lookup"><span data-stu-id="48cd9-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="48cd9-157">在解碼 Guid 陣列中迴圈，以找出該解碼篩選器所支援的專案。</span><span class="sxs-lookup"><span data-stu-id="48cd9-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="48cd9-158">例如，針對 MPEG-2 解碼器，您會尋找 **DXVA2 \_ ModeMPEG2 \_ MOCOMP**、 **DXVA2 \_ ModeMPEG2 \_ IDCT** 或 **DXVA2 \_ ModeMPEG2 \_ VLD**。</span><span class="sxs-lookup"><span data-stu-id="48cd9-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="48cd9-159">當您找到候選的解碼器裝置 GUID 時，請將 GUID 傳遞給 [**IDirectXVideoDecoderService：： GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) 方法。</span><span class="sxs-lookup"><span data-stu-id="48cd9-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="48cd9-160">這個方法會傳回呈現目標格式的陣列，並指定為 **D3DFORMAT** 值。</span><span class="sxs-lookup"><span data-stu-id="48cd9-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="48cd9-161">逐一查看轉譯目標格式，並尋找符合您輸出格式的專案。</span><span class="sxs-lookup"><span data-stu-id="48cd9-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="48cd9-162">一般而言，解碼器裝置支援單一轉譯目標格式。</span><span class="sxs-lookup"><span data-stu-id="48cd9-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="48cd9-163">您應使用此子類型連接到轉譯器的轉譯器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="48cd9-164">在第一次呼叫 [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md)時，此解碼器可以判斷轉譯目標格式，然後將此格式傳回為慣用的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="48cd9-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="48cd9-165">呼叫 [**IDirectXVideoDecoderService：： GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations)。</span><span class="sxs-lookup"><span data-stu-id="48cd9-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="48cd9-166">傳入相同的解碼器裝置 GUID，以及描述建議格式的 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構。</span><span class="sxs-lookup"><span data-stu-id="48cd9-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="48cd9-167">方法會傳回 [**DXVA2 \_ ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="48cd9-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="48cd9-168">每個結構都描述一個可能的解碼器裝置設定。</span><span class="sxs-lookup"><span data-stu-id="48cd9-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="48cd9-169">假設先前的步驟成功，請儲存 Direct3D 裝置控制碼、解碼器裝置 GUID 和設定結構。</span><span class="sxs-lookup"><span data-stu-id="48cd9-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="48cd9-170">篩選器會使用此資訊來建立解碼器裝置。</span><span class="sxs-lookup"><span data-stu-id="48cd9-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="48cd9-171">下列程式碼顯示如何尋找解碼器設定。</span><span class="sxs-lookup"><span data-stu-id="48cd9-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="48cd9-172">因為此範例為泛型，所以某些邏輯已放在必須由該解碼器實作為的 helper 函式中。</span><span class="sxs-lookup"><span data-stu-id="48cd9-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="48cd9-173">下列程式碼顯示這些函數的宣告：</span><span class="sxs-lookup"><span data-stu-id="48cd9-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="48cd9-174">通知影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="48cd9-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="48cd9-175">如果此解碼器找到解碼器設定，下一步就是通知影片轉譯器，該解碼器將會使用硬體加速。</span><span class="sxs-lookup"><span data-stu-id="48cd9-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="48cd9-176">您可以在 [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) 方法中執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="48cd9-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="48cd9-177">在選取配置器之前，必須先執行此步驟，因為它會影響配置器的選取方式。</span><span class="sxs-lookup"><span data-stu-id="48cd9-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="48cd9-178">查詢轉譯器的輸入圖釘以取得 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="48cd9-179">呼叫 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 來取得 [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="48cd9-180">服務 GUID 是 **MR \_ 影片 \_ 加速 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="48cd9-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="48cd9-181">在迴圈中呼叫 [**IDirectXVideoMemoryConfiguration：： GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) ，將 *dwTypeIndex* 變數從零遞增。</span><span class="sxs-lookup"><span data-stu-id="48cd9-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="48cd9-182">當方法傳回 *pdwType* 參數中的 **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** 值時停止。</span><span class="sxs-lookup"><span data-stu-id="48cd9-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="48cd9-183">此步驟可確保影片轉譯器支援硬體加速解碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="48cd9-184">EVR 篩選器的這個步驟一律會成功。</span><span class="sxs-lookup"><span data-stu-id="48cd9-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="48cd9-185">如果上一個步驟成功，請呼叫 [**IDirectXVideoMemoryConfiguration：： SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) ，其值為 DXVA2 \_ SurfaceType \_ DecoderRenderTarget。</span><span class="sxs-lookup"><span data-stu-id="48cd9-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="48cd9-186">使用此值呼叫 **SetSurfaceType** ，會將影片轉譯器放入 DXVA 模式。</span><span class="sxs-lookup"><span data-stu-id="48cd9-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="48cd9-187">當影片轉譯器處於此模式時，該解碼器必須提供它自己的配置器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="48cd9-188">下列程式碼說明如何通知影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="48cd9-189">如果此解碼器找到有效的設定並成功通知影片轉譯器，則該解碼器可以使用 DXVA 進行解碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="48cd9-190">此解碼器必須針對其輸出圖釘來執行自訂配置器，如下一節所述。</span><span class="sxs-lookup"><span data-stu-id="48cd9-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="48cd9-191">配置未壓縮的緩衝區</span><span class="sxs-lookup"><span data-stu-id="48cd9-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="48cd9-192">在 DXVA 2.0 中，此解碼器負責配置 Direct3D 介面，以作為未壓縮的視訊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="48cd9-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="48cd9-193">因此，此解碼器必須執行將建立介面的自訂配置器。</span><span class="sxs-lookup"><span data-stu-id="48cd9-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="48cd9-194">此配置器所提供的媒體範例會保存 Direct3D 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="48cd9-195">EVR 會藉由呼叫媒體範例上的 [**IMFGetService：： GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) ，來抓取介面的指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="48cd9-196">服務識別碼是 **MR \_ 緩衝區 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="48cd9-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="48cd9-197">若要提供自訂配置器，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="48cd9-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="48cd9-198">定義媒體範例的類別。</span><span class="sxs-lookup"><span data-stu-id="48cd9-198">Define a class for the media samples.</span></span> <span data-ttu-id="48cd9-199">這個類別可以衍生自 [**CMediaSample**](../directshow/cmediasample.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="48cd9-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="48cd9-200">在這個類別中，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="48cd9-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="48cd9-201">將指標儲存至 Direct3D 介面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="48cd9-202">執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="48cd9-203">在 [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) 方法中，如果服務 GUID 是 **MR \_ 緩衝區 \_ 服務**，請查詢 Direct3D 介面以取得所要求的介面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="48cd9-204">否則， **GetService** 可以傳回 **MF \_ E \_ 不受支援的 \_ 服務**。</span><span class="sxs-lookup"><span data-stu-id="48cd9-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="48cd9-205">覆寫 [**CMediaSample：： GetPointer**](../directshow/cmediasample-getpointer.md) 方法，以傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="48cd9-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="48cd9-206">定義配置器的類別。</span><span class="sxs-lookup"><span data-stu-id="48cd9-206">Define a class for the allocator.</span></span> <span data-ttu-id="48cd9-207">配置器可以衍生自 [**CBaseAllocator**](../directshow/cbaseallocator.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="48cd9-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="48cd9-208">在這個類別中，執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="48cd9-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="48cd9-209">覆寫 [**CBaseAllocator：：分配**](../directshow/cbaseallocator-alloc.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="48cd9-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="48cd9-210">在這個方法中，呼叫 [**IDirectXVideoAccelerationService：： CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) 以建立表面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="48cd9-211"> ([**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 介面從 [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice)繼承這個方法。 ) </span><span class="sxs-lookup"><span data-stu-id="48cd9-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="48cd9-212">覆寫 [**CBaseAllocator：： Free**](../directshow/cbaseallocator-free.md) 方法以釋放表面。</span><span class="sxs-lookup"><span data-stu-id="48cd9-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="48cd9-213">在篩選的輸出釘選中，覆寫 [**CBaseOutputPin：： InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="48cd9-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="48cd9-214">在這個方法內，建立自訂配置器的實例。</span><span class="sxs-lookup"><span data-stu-id="48cd9-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="48cd9-215">在篩選準則中，執行 [**CTransformFilter：:D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="48cd9-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="48cd9-216">*>pproperties* 參數會指出 EVR 需要的表面數目。</span><span class="sxs-lookup"><span data-stu-id="48cd9-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="48cd9-217">將您的解碼所需的介面數目加到這個值，並在配置器上呼叫 [**IMemAllocator：： SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) 。</span><span class="sxs-lookup"><span data-stu-id="48cd9-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="48cd9-218">下列程式碼示範如何執行 media 範例類別：</span><span class="sxs-lookup"><span data-stu-id="48cd9-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="48cd9-219">下列程式碼顯示如何在配置器上執行 [**配置方法。**](../directshow/cbaseallocator-alloc.md)</span><span class="sxs-lookup"><span data-stu-id="48cd9-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="48cd9-220">以下是 [**免費**](../directshow/cbaseallocator-free.md) 方法的程式碼：</span><span class="sxs-lookup"><span data-stu-id="48cd9-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="48cd9-221">如需有關如何執行自訂配置器的詳細資訊，請參閱 DirectShow SDK 檔中 [提供自訂](../directshow/providing-a-custom-allocator.md) 配置器的主題。</span><span class="sxs-lookup"><span data-stu-id="48cd9-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="48cd9-222">解碼</span><span class="sxs-lookup"><span data-stu-id="48cd9-222">Decoding</span></span>

<span data-ttu-id="48cd9-223">若要建立解碼器裝置，請呼叫 [**IDirectXVideoDecoderService：： CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)。</span><span class="sxs-lookup"><span data-stu-id="48cd9-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="48cd9-224">方法會傳回解碼裝置之 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="48cd9-225">在每個畫面上，呼叫 [**IDirect3DDeviceManager9：： TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) 來測試裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="48cd9-226">如果裝置已變更，此方法會傳回 DXVA2 \_ E \_ NEW \_ VIDEO \_ 裝置。</span><span class="sxs-lookup"><span data-stu-id="48cd9-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="48cd9-227">如果發生這種情況，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="48cd9-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="48cd9-228">藉由呼叫 [**IDirect3DDeviceManager9：： CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle)來關閉裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="48cd9-229">釋放 [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) 和 [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) 指標。</span><span class="sxs-lookup"><span data-stu-id="48cd9-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="48cd9-230">開啟新的裝置控制碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="48cd9-231">如 [尋找解碼器](#finding-a-decoder-configuration)設定一節所述，協商新的解碼器設定。</span><span class="sxs-lookup"><span data-stu-id="48cd9-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="48cd9-232">建立新的解碼器裝置。</span><span class="sxs-lookup"><span data-stu-id="48cd9-232">Create a new decoder device.</span></span>

<span data-ttu-id="48cd9-233">假設裝置控制碼有效，則解碼程式的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="48cd9-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="48cd9-234">呼叫 [**IDirectXVideoDecoder：： BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)。</span><span class="sxs-lookup"><span data-stu-id="48cd9-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="48cd9-235">執行下列一或多次：</span><span class="sxs-lookup"><span data-stu-id="48cd9-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="48cd9-236">呼叫 [**IDirectXVideoDecoder：： GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) 來取得 DXVA 的解碼器緩衝區。</span><span class="sxs-lookup"><span data-stu-id="48cd9-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="48cd9-237">填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="48cd9-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="48cd9-238">呼叫 [**IDirectXVideoDecoder：： ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer)。</span><span class="sxs-lookup"><span data-stu-id="48cd9-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="48cd9-239">呼叫 [**IDirectXVideoDecoder：： Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) 以執行框架上的解碼作業。</span><span class="sxs-lookup"><span data-stu-id="48cd9-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="48cd9-240">DXVA 2.0 使用與 DXVA 1.0 相同的資料結構來進行解碼作業。</span><span class="sxs-lookup"><span data-stu-id="48cd9-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="48cd9-241">針對 DXVA 設定檔的原創組 (261、.H 和 MPEG-2) ，這些資料結構會在 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)中說明。</span><span class="sxs-lookup"><span data-stu-id="48cd9-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="48cd9-242">在每對 [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe) / [**執行**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)呼叫中，您可以多次呼叫 [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) ，但每種類型的 DXVA 緩衝區都只會呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="48cd9-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="48cd9-243">如果您使用相同的緩衝區類型呼叫它兩次，則會覆寫資料。</span><span class="sxs-lookup"><span data-stu-id="48cd9-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="48cd9-244">呼叫 [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)之後，呼叫 [**IMemInputPin：： Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) 將框架傳遞給影片轉譯器，如同軟體解碼一樣。</span><span class="sxs-lookup"><span data-stu-id="48cd9-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="48cd9-245">**Receive** 方法是非同步;在傳回之後，可以繼續對下一個框架進行解碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="48cd9-246">當緩衝區正在使用中時，顯示驅動程式會防止任何解碼命令覆寫緩衝區。</span><span class="sxs-lookup"><span data-stu-id="48cd9-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="48cd9-247">除非轉譯器已釋放範例，否則，此解碼器不應重複使用介面將另一個框架解碼。</span><span class="sxs-lookup"><span data-stu-id="48cd9-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="48cd9-248">當轉譯器釋放範例時，配置器會將範例放回其可用範例的集區。</span><span class="sxs-lookup"><span data-stu-id="48cd9-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="48cd9-249">若要取得下一個可用的範例，請呼叫 [**CBaseOutputPin：： GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md)，它接著會呼叫 [**IMemAllocator：： GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer)。</span><span class="sxs-lookup"><span data-stu-id="48cd9-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="48cd9-250">如需詳細資訊，請參閱 DirectShow 檔中有關 [directshow 之資料流程](../directshow/overview-of-data-flow-in-directshow.md) 的主題總覽。</span><span class="sxs-lookup"><span data-stu-id="48cd9-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48cd9-251">相關主題</span><span class="sxs-lookup"><span data-stu-id="48cd9-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48cd9-252">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="48cd9-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
