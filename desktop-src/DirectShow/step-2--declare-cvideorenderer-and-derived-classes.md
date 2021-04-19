---
description: 本主題是在 DirectShow 中進行音訊/影片播放教學課程的步驟2。
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 步驟2：宣告 CVideoRenderer 和衍生類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975383"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a><span data-ttu-id="b8720-103">步驟2：宣告 CVideoRenderer 和衍生類別</span><span class="sxs-lookup"><span data-stu-id="b8720-103">Step 2: Declare CVideoRenderer and Derived Classes</span></span>

<span data-ttu-id="b8720-104">本主題是 [在 DirectShow 中進行音訊/影片播放](audio-video-playback-in-directshow.md)教學課程的步驟2。</span><span class="sxs-lookup"><span data-stu-id="b8720-104">This topic is step 2 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="b8720-105">完整的程式碼會顯示在「 [DirectShow 播放」範例](directshow-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="b8720-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="b8720-106">DirectShow 提供數種可轉譯影片的不同篩選：</span><span class="sxs-lookup"><span data-stu-id="b8720-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="b8720-107">[**增強的影片轉譯器篩選器**](enhanced-video-renderer-filter.md) (EVR) </span><span class="sxs-lookup"><span data-stu-id="b8720-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="b8720-108">[影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) </span><span class="sxs-lookup"><span data-stu-id="b8720-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="b8720-109">[影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) </span><span class="sxs-lookup"><span data-stu-id="b8720-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="b8720-110">如需這些篩選之間差異的詳細資訊，請參閱 [選擇正確的影片](choosing-the-right-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="b8720-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="b8720-111">在本教學課程中，會使用下列抽象類別來包裝影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="b8720-111">In this tutorial, the following abstract class is used to wrap the video renderer filter.</span></span>


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



<span data-ttu-id="b8720-112">注意：</span><span class="sxs-lookup"><span data-stu-id="b8720-112">Notes:</span></span>

-   <span data-ttu-id="b8720-113">如果已建立影片轉譯器，則此方法會傳回 `HasVideo` **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b8720-113">The `HasVideo` method returns **TRUE** if the video renderer has been created.</span></span>
-   <span data-ttu-id="b8720-114">`AddToGraph`方法會將影片轉譯器新增至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b8720-114">The `AddToGraph` method adds the video renderer to the filter graph.</span></span>
-   <span data-ttu-id="b8720-115">`FinalizeGraph`方法會完成圖形建立步驟。</span><span class="sxs-lookup"><span data-stu-id="b8720-115">The `FinalizeGraph` method completes the graph-building step.</span></span>
-   <span data-ttu-id="b8720-116">`UpdateVideoWindow`方法會更新影片目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="b8720-116">The `UpdateVideoWindow` method updates the video destination rectangle.</span></span>
-   <span data-ttu-id="b8720-117">方法會重新 `Repaint` 繪製目前的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="b8720-117">The `Repaint` method redraws the current video frame.</span></span>
-   <span data-ttu-id="b8720-118">`DisplayModeChanged`方法會處理顯示模式變更。</span><span class="sxs-lookup"><span data-stu-id="b8720-118">The `DisplayModeChanged` method handles display-mode changes.</span></span>

<span data-ttu-id="b8720-119">本教學課程稍後會詳細說明這些方法。</span><span class="sxs-lookup"><span data-stu-id="b8720-119">Each of these methods is described in detail later in this tutorial.</span></span>

<span data-ttu-id="b8720-120">接下來，宣告衍生類別以包裝三個影片轉譯器： EVR、VMR-9 和 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="b8720-120">Next, declare a derived class to wrap each of the three video renderers: the EVR, the VMR-9, and the VMR-7.</span></span>

### <a name="cevr-class"></a><span data-ttu-id="b8720-121">CEVR 類別</span><span class="sxs-lookup"><span data-stu-id="b8720-121">CEVR Class</span></span>

<span data-ttu-id="b8720-122">`CEVR`類別會管理 EVR。</span><span class="sxs-lookup"><span data-stu-id="b8720-122">The `CEVR` class manages the EVR.</span></span> <span data-ttu-id="b8720-123">它包含 EVR 的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 和 [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b8720-123">It contains a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) and [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interfaces of the EVR.</span></span>


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a><span data-ttu-id="b8720-124">CVMR9 類別</span><span class="sxs-lookup"><span data-stu-id="b8720-124">CVMR9 Class</span></span>

<span data-ttu-id="b8720-125">`CVMR9`類別會管理 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="b8720-125">The `CVMR9` class manages the VMR-9.</span></span> <span data-ttu-id="b8720-126">它包含 [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b8720-126">It contains a pointer to the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a><span data-ttu-id="b8720-127">CVMR7 類別</span><span class="sxs-lookup"><span data-stu-id="b8720-127">CVMR7 Class</span></span>

<span data-ttu-id="b8720-128">`CVMR7`類別會管理 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="b8720-128">The `CVMR7` class manages the VMR-7.</span></span> <span data-ttu-id="b8720-129">它包含 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b8720-129">It contains a pointer to the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



<span data-ttu-id="b8720-130">下一 [步：步驟3：建立篩選圖形](step-3--build-the-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="b8720-130">Next: [Step 3: Build the Filter Graph](step-3--build-the-filter-graph.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8720-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8720-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8720-132">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="b8720-132">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="b8720-133">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="b8720-133">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> <dt>

[<span data-ttu-id="b8720-134">影片轉譯</span><span class="sxs-lookup"><span data-stu-id="b8720-134">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 
