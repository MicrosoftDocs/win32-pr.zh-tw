---
description: 本文包含使用 Direct3D 12 video Api 進行動作向量估計的指引。
ms.assetid: ''
title: Direct3D 影片移動估計
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106997299"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="2507d-103">Direct3D 影片移動估計</span><span class="sxs-lookup"><span data-stu-id="2507d-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="2507d-104">本文包含使用 Direct3D 12 video Api 進行動作向量估計的指引。</span><span class="sxs-lookup"><span data-stu-id="2507d-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="2507d-105">這項功能是在 Windows 10 2004 版 (10.0;組建 19041) 。</span><span class="sxs-lookup"><span data-stu-id="2507d-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="2507d-106">移動估計是決定將轉換從某個2D 影像轉換成另一個2D 影像的動作向量的流程。</span><span class="sxs-lookup"><span data-stu-id="2507d-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="2507d-107">移動估計是影片編碼的不可或缺部分，而且可以在畫面播放速率轉換演算法中使用。</span><span class="sxs-lookup"><span data-stu-id="2507d-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="2507d-108">雖然可以使用著色器來執行動作估計，但 D3D12 動作估計功能的目的是要公開固定的函式加速，以在移動搜尋時從3D 中卸載這部分的工作。</span><span class="sxs-lookup"><span data-stu-id="2507d-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="2507d-109">這通常是公開 GPU 視頻編碼器動作估算器的形式。</span><span class="sxs-lookup"><span data-stu-id="2507d-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="2507d-110">D3D12 移動估計的目標是光學流程，但請注意，編碼器動作估算器可能會優化以改善壓縮。</span><span class="sxs-lookup"><span data-stu-id="2507d-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="2507d-111">檢查支援</span><span class="sxs-lookup"><span data-stu-id="2507d-111">Checking for Support</span></span>

<span data-ttu-id="2507d-112">藉由呼叫 [ID3D12VideoDevice：： CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) 並傳入 [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) 列舉中的值，以指定要查詢支援的功能，判斷所有 D3D 影片功能的支援。</span><span class="sxs-lookup"><span data-stu-id="2507d-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="2507d-113">若要查詢指定格式的支援區塊大小和解析度，請使用 **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** 值，並為 *pFeatureSupportData* 提供 [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator)結構，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="2507d-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="2507d-114">在目前的版本中，僅支援 **DXGI_FORMAT_NV12** ，因此其他格式的內容可能需要轉換成色彩並 >downsampled，才能使用移動估計。</span><span class="sxs-lookup"><span data-stu-id="2507d-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="2507d-115">動作估算器內容物件</span><span class="sxs-lookup"><span data-stu-id="2507d-115">The motion estimator context object</span></span>

<span data-ttu-id="2507d-116">[ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator)物件會維護影片動作估計作業的內容。</span><span class="sxs-lookup"><span data-stu-id="2507d-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="2507d-117">呼叫 [ID3D12VideoDevice1：： CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator)，以建立這個介面的新實例。</span><span class="sxs-lookup"><span data-stu-id="2507d-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="2507d-118">選取的區塊大小、有效位數和支援的大小範圍取決於 **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** 功能檢查所傳回的硬體所支援的值。</span><span class="sxs-lookup"><span data-stu-id="2507d-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="2507d-119">您可以選取比驅動程式支援更小的大小範圍。</span><span class="sxs-lookup"><span data-stu-id="2507d-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="2507d-120">大小範圍會通知內部配置大小。</span><span class="sxs-lookup"><span data-stu-id="2507d-120">Size range informs internal allocation sizes.</span></span>

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="2507d-121">動作向量的儲存</span><span class="sxs-lookup"><span data-stu-id="2507d-121">Storage of motion vectors</span></span>

<span data-ttu-id="2507d-122">[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap)會儲存運動向量。</span><span class="sxs-lookup"><span data-stu-id="2507d-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="2507d-123">[ID3D12VideoEncodeCommandList：： EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion)所傳回的[D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output)結構會使用這個介面。</span><span class="sxs-lookup"><span data-stu-id="2507d-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="2507d-124">解析的輸出2D 材質是一個 [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 材質，其中 R 會保存水準元件，而 G 則會保留動作向量的垂直元件。</span><span class="sxs-lookup"><span data-stu-id="2507d-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="2507d-125">此材質的大小調整為每個區塊保留一對元件。</span><span class="sxs-lookup"><span data-stu-id="2507d-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="2507d-126">呼叫 [ID3D12VideoEncodeCommandList：： ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) ，將 **EstimateMotion** 的動作向量輸出從硬體相依的格式轉譯成影片動作估計 api 所定義的一致格式。</span><span class="sxs-lookup"><span data-stu-id="2507d-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 <span data-ttu-id="2507d-127">**ID3D12VideoMotionVectorHeap** 也可用來在 [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) 結構中提供提示向量。</span><span class="sxs-lookup"><span data-stu-id="2507d-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="2507d-128">估計命令清單中的動作</span><span class="sxs-lookup"><span data-stu-id="2507d-128">Estimate motion in a command list</span></span>

<span data-ttu-id="2507d-129">從[ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist)呼叫[EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) ，以叫用移動估計運算。</span><span class="sxs-lookup"><span data-stu-id="2507d-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="2507d-130">下列範例會執行動作搜尋，並使用 [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)將動作向量解析成2d 材質。</span><span class="sxs-lookup"><span data-stu-id="2507d-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="2507d-131">當做 **EstimateMotion** 輸入使用的 D3D12 資源必須處於 [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 狀態，且 **ResolveMotionVectorHeap** 所寫入的資源必須處於 [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 狀態。</span><span class="sxs-lookup"><span data-stu-id="2507d-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a><span data-ttu-id="2507d-132">受保護的資源</span><span class="sxs-lookup"><span data-stu-id="2507d-132">Protected resources</span></span>

<span data-ttu-id="2507d-133">當驅動程式支援時，Direct3D 12 動作向量估計支援讀取和寫入受硬體 DRM 保護的資源。</span><span class="sxs-lookup"><span data-stu-id="2507d-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="2507d-134">如果輸入資源受到硬體 DRM 保護，則輸出也是硬體 DRM 受保護的資源。用來建立動作估計內容物件和動作向量堆積  [ID3D12VideoDevice1：： CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) 和 [ID3D12VideoDevice1：： CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap)的方法，都接受用來管理受保護資源存取權的 [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) 。</span><span class="sxs-lookup"><span data-stu-id="2507d-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="2507d-135">使用 [ID3D12VideoMotionEstimator：： GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) 和 [ID3D12VideoMotionVectorHeap：： GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) 來取得建立物件時所提供的 **ID3D12ProtectedResourceSession** 物件。</span><span class="sxs-lookup"><span data-stu-id="2507d-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="2507d-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="2507d-136">Related topics</span></span>

* [<span data-ttu-id="2507d-137">Direct3D 12 影片 Api</span><span class="sxs-lookup"><span data-stu-id="2507d-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="2507d-138">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2507d-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
