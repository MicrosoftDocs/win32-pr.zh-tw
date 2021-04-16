---
title: 在複合影像上顯示應用程式提供的點陣圖
description: 在複合影像上顯示 Application-Supplied 點陣圖
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509805"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="8b531-103">在複合影像上顯示應用程式提供的點陣圖</span><span class="sxs-lookup"><span data-stu-id="8b531-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="8b531-104">應用程式可以使用 VMR 的混合模式，在影片矩形內部分或完全顯示 Alpha 混合的通道標誌、使用者介面或廣告。</span><span class="sxs-lookup"><span data-stu-id="8b531-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="8b531-105">因為圖形處理器會在硬體中執行混合，所以對影片串流的播放效能會有最大的影響，而且沒有可偵測的閃爍或撕裂的成品。</span><span class="sxs-lookup"><span data-stu-id="8b531-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="8b531-106">應用程式可以視需要頻繁地變更顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="8b531-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="8b531-107">請注意，只有當 DirectShow 篩選圖形處於 [執行中] 狀態時，才會在螢幕上反映變更。</span><span class="sxs-lookup"><span data-stu-id="8b531-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="8b531-108">VMR 會使用其混音器元件，將點陣圖重迭至複合影像。</span><span class="sxs-lookup"><span data-stu-id="8b531-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="8b531-109">使用 VMR-7 時，應用程式必須強制 VMR 載入其混音器，即使只有一個影片串流也一樣。</span><span class="sxs-lookup"><span data-stu-id="8b531-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="8b531-110">VMR-9 並不需要這麼做，因為它預設會載入其混音器。</span><span class="sxs-lookup"><span data-stu-id="8b531-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="8b531-111">為了 blend 靜態點陣圖影像與影片資料流程，應用程式會建立 VMR 並將它新增至圖形，然後呼叫 [**IVMRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)。</span><span class="sxs-lookup"><span data-stu-id="8b531-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="8b531-112">傳遞給此函式的值會識別 VMR 應該建立的輸入圖釘數目。</span><span class="sxs-lookup"><span data-stu-id="8b531-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="8b531-113">應用程式可以指定介於1到最大混音器串流之間的任何值 \_ \_ ; 如果應用程式只是要顯示單一影片串流，則指定1的值是有效的。</span><span class="sxs-lookup"><span data-stu-id="8b531-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="8b531-114">即使 VMR-7 預設有單一輸入 pin，還是必須呼叫這個方法，才能強制它載入其混音器元件。</span><span class="sxs-lookup"><span data-stu-id="8b531-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="8b531-115"> (VMR-9 預設會載入其混音器並設定四個 pin。 ) </span><span class="sxs-lookup"><span data-stu-id="8b531-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="8b531-116">若要設定點陣圖，請使用 VMR 7 上的 [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) 介面或 VMR-9 上的 [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) 介面。</span><span class="sxs-lookup"><span data-stu-id="8b531-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="8b531-117">您可以透過 GDI 裝置內容的控制碼 (hDC) 或 DirectDraw 介面介面來指定點陣圖。</span><span class="sxs-lookup"><span data-stu-id="8b531-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="8b531-118">如果應用程式想要影像包含內嵌的 Alpha 資訊 (也知道每個圖元的 Alpha) 必須將影像資料放在 DirectDraw 介面介面中。</span><span class="sxs-lookup"><span data-stu-id="8b531-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="8b531-119">這是因為目前無法使用 GDI 裝置內容來放置每個圖元的 Alpha 資訊。</span><span class="sxs-lookup"><span data-stu-id="8b531-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="8b531-120">DirectDraw 表面必須是 RGB32 或 ARGB32，而且最好是系統記憶體介面。</span><span class="sxs-lookup"><span data-stu-id="8b531-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="8b531-121">表面維度不需要是2的乘冪。</span><span class="sxs-lookup"><span data-stu-id="8b531-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="8b531-122">VMR 可讓應用程式指定影像的位置和整體透明度值。</span><span class="sxs-lookup"><span data-stu-id="8b531-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="8b531-123">下列程式碼示範如何將影像資料向下傳遞至 VMR，以進行後續的混合：</span><span class="sxs-lookup"><span data-stu-id="8b531-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



<span data-ttu-id="8b531-124">本主題所討論的概念是在 [VMRPlayer 範例](vmrplayer-sample.md) 應用程式範例中示範。</span><span class="sxs-lookup"><span data-stu-id="8b531-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="8b531-125">**使用點陣圖影像建立簡單的動畫**</span><span class="sxs-lookup"><span data-stu-id="8b531-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="8b531-126">若要建立簡單的動畫點陣圖標誌，請將所有點陣圖「框架」放入單一影像中，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="8b531-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![vmr 圖像塊](images/vmr-image-strip.png)

<span data-ttu-id="8b531-128">當您一開始使用 [**IVMRMixerBitmap：： SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap)設定點陣圖時，如果點陣圖位於 hdc 中，請設定 **VMRALPHABITMAP** 結構的 **.rsrc** 欄位，以指定在 hdc 內整個點陣圖的大小。</span><span class="sxs-lookup"><span data-stu-id="8b531-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="8b531-129">結構的 **top** 和 **left** 成員會設定為0，而 **右邊** 和 **下** 成員則是點陣圖的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="8b531-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="8b531-130">如果點陣圖在 DirectDraw 表面中，則會知道介面大小，因此不需要在此方法中指定 .Rsrc。</span><span class="sxs-lookup"><span data-stu-id="8b531-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="8b531-131">當您呼叫 [**IVMRMixerBitmap：： UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)時，請針對 HDC 和 DirectDraw 點陣圖使用 **.rsrc** 成員，以指定您想要顯示之影像內的特定框架或矩形，然後在 **>srcrect** 成員中設定 **VMRBITMAP \_ dwFlags** 旗標。</span><span class="sxs-lookup"><span data-stu-id="8b531-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b531-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b531-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b531-133">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="8b531-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



