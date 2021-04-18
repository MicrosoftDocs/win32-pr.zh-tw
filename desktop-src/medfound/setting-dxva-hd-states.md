---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: 設定 DXVA-HD 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983371"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="e9b4e-103">設定 DXVA-HD 狀態</span><span class="sxs-lookup"><span data-stu-id="e9b4e-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="e9b4e-104">在影片處理期間，Microsoft DirectX Video 加速 High 定義 (DXVA-HD) 裝置會將持續性狀態從某個畫面維持到下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="e9b4e-105">每個狀態都有記載的預設值。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-105">Each state has a documented default.</span></span> <span data-ttu-id="e9b4e-106">設定裝置之後，請設定您想要變更其預設值的任何狀態。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="e9b4e-107">在您處理每個畫面格之前，請更新任何應變更的狀態。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="e9b4e-108">這種設計與 DXVA-VP 不同。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="e9b4e-109">在 DXVA-VP 中，應用程式必須指定每個框架的總 VP 參數。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="e9b4e-110">裝置狀態分為兩類：</span><span class="sxs-lookup"><span data-stu-id="e9b4e-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="e9b4e-111">*資料流程* 狀態會分別套用每個輸入資料流程。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="e9b4e-112">您可以將不同的設定套用至每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="e9b4e-113">*Array.blit* 狀態會全域套用至整個影片處理 array.blit。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="e9b4e-114">已定義下列資料流程狀態。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-114">The following stream states are defined.</span></span>



| <span data-ttu-id="e9b4e-115">資料流程狀態</span><span class="sxs-lookup"><span data-stu-id="e9b4e-115">Stream State</span></span>                                   | <span data-ttu-id="e9b4e-116">Description</span><span class="sxs-lookup"><span data-stu-id="e9b4e-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b4e-117">**DXVAHD \_ 資料流程 \_ 狀態 \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="e9b4e-118">輸入影片格式。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="e9b4e-119">**DXVAHD \_ 資料流程 \_ 狀態 \_ 框架 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="e9b4e-120">交錯。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="e9b4e-121">**DXVAHD \_ 資料流程 \_ 狀態 \_ 輸入 \_ 色彩 \_ 空間**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="e9b4e-122">輸入色彩空間。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-122">Input color space.</span></span> <span data-ttu-id="e9b4e-123">此狀態指定輸入資料流程的 RGB 色彩範圍和 YCbCr 傳輸矩陣。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="e9b4e-124">**DXVAHD \_ 資料流程 \_ 狀態 \_ 輸出 \_ 速率**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="e9b4e-125">輸出畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-125">Output frame rate.</span></span> <span data-ttu-id="e9b4e-126">此狀態控制畫面播放速率的轉換。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="e9b4e-127">**DXVAHD \_ 資料流程 \_ 狀態 \_ 來源 \_ 矩形**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="e9b4e-128">來源矩形。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="e9b4e-129">**DXVAHD \_ 資料流程 \_ 狀態 \_ 目的地 \_ 矩形**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="e9b4e-130">目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="e9b4e-131">**DXVAHD \_ 資料流程 \_ 狀態 \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="e9b4e-132">平面 Alpha。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="e9b4e-133">**DXVAHD \_ 資料流程 \_ 狀態 \_ 調色板**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="e9b4e-134">調色板。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-134">Color palette.</span></span> <span data-ttu-id="e9b4e-135">此狀態只適用于調色盤輸入格式。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="e9b4e-136">**DXVAHD \_ 資料流程 \_ 狀態 \_ LUMA \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="e9b4e-137">Luma 鍵。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="e9b4e-138">**DXVAHD \_ 資料流程 \_ 狀態 \_ 外觀 \_ 比例**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="e9b4e-139">圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="e9b4e-140">**DXVAHD \_ 資料流程 \_ 狀態 \_ 篩選 \_ Xxxx**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="e9b4e-141">影像篩選設定。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-141">Image filter settings.</span></span> <span data-ttu-id="e9b4e-142">驅動程式可支援亮度、對比和其他影像篩選。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="e9b4e-143">以下是定義的 array.blit 狀態：</span><span class="sxs-lookup"><span data-stu-id="e9b4e-143">The following blit states are defined:</span></span>



| <span data-ttu-id="e9b4e-144">Array.blit 狀態</span><span class="sxs-lookup"><span data-stu-id="e9b4e-144">Blit State</span></span>                                   | <span data-ttu-id="e9b4e-145">Description</span><span class="sxs-lookup"><span data-stu-id="e9b4e-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e9b4e-146">**DXVAHD \_ BLT \_ 狀態 \_ 目標 \_ 矩形**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="e9b4e-147">目標矩形。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="e9b4e-148">**DXVAHD \_ BLT \_ 狀態 \_ 背景 \_ 色彩**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="e9b4e-149">背景色彩。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-149">Background color.</span></span>                                                            |
| <span data-ttu-id="e9b4e-150">**DXVAHD \_ BLT \_ 狀態 \_ 輸出 \_ 色彩 \_ 空間**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="e9b4e-151">輸出色彩空間。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="e9b4e-152">**DXVAHD \_ BLT \_ 狀態 \_ ALPHA \_ 填滿**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="e9b4e-153">Alpha 填滿模式。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="e9b4e-154">**DXVAHD \_ BLT \_ 狀態 \_ CONSTRICTION**</span><span class="sxs-lookup"><span data-stu-id="e9b4e-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="e9b4e-155">收縮。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-155">Constriction.</span></span> <span data-ttu-id="e9b4e-156">此狀態控制裝置是否 downsamples 輸出。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="e9b4e-157">若要設定資料流程狀態，請呼叫 [**IDXVAHD \_ VideoProcessor：： SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) 方法。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="e9b4e-158">若要設定 array.blit 狀態，請呼叫 [**IDXVAHD \_ VideoProcessor：： SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) 方法。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="e9b4e-159">在這兩種方法中，列舉值會指定要設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="e9b4e-160">狀態資料是使用特定狀態的資料結構來指定，應用程式會將它轉換成 **void \*** 型別。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="e9b4e-161">下列程式碼範例會設定資料流程0的輸入格式和目的矩形，並將背景色彩設為黑色。</span><span class="sxs-lookup"><span data-stu-id="e9b4e-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e9b4e-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9b4e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9b4e-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="e9b4e-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



