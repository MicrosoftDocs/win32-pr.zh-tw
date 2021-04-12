---
title: 長條圖效果
description: 使用長條圖效果，根據指定的 bin 數目產生輸入點陣圖的長條圖。
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- 長條圖效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384493"
---
# <a name="histogram-effect"></a><span data-ttu-id="46f08-104">長條圖效果</span><span class="sxs-lookup"><span data-stu-id="46f08-104">Histogram effect</span></span>

<span data-ttu-id="46f08-105">使用長條圖效果，根據指定的 bin 數目產生輸入點陣圖的長條圖。</span><span class="sxs-lookup"><span data-stu-id="46f08-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="46f08-106">這項效果的 CLSID 是 CLSID \_ D2D1Histogram。</span><span class="sxs-lookup"><span data-stu-id="46f08-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="46f08-107">範例</span><span class="sxs-lookup"><span data-stu-id="46f08-107">Example</span></span>](#example)
-   [<span data-ttu-id="46f08-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="46f08-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="46f08-109">通道選取器</span><span class="sxs-lookup"><span data-stu-id="46f08-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="46f08-110">資料輸出</span><span class="sxs-lookup"><span data-stu-id="46f08-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="46f08-111">備註</span><span class="sxs-lookup"><span data-stu-id="46f08-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="46f08-112">需求</span><span class="sxs-lookup"><span data-stu-id="46f08-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="46f08-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="46f08-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="46f08-114">範例</span><span class="sxs-lookup"><span data-stu-id="46f08-114">Example</span></span>



| <span data-ttu-id="46f08-115">之前</span><span class="sxs-lookup"><span data-stu-id="46f08-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| <span data-ttu-id="46f08-117">長條圖輸出資料的圖表</span><span class="sxs-lookup"><span data-stu-id="46f08-117">Graph of the histogram output data</span></span>                         |
| ![轉換後的影像。](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="46f08-119">效果屬性</span><span class="sxs-lookup"><span data-stu-id="46f08-119">Effect properties</span></span>

<span data-ttu-id="46f08-120">以下是產生輸出的方程式。</span><span class="sxs-lookup"><span data-stu-id="46f08-120">Here's the equation to generate the output.</span></span>

![產生長條圖效果輸出的方程式。](images/histogram-formula.png)

<span data-ttu-id="46f08-122">*我* 會從0到 bin 數目進行評估。效果會產生介於0和1之間圖元值的長條圖。</span><span class="sxs-lookup"><span data-stu-id="46f08-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="46f08-123">此範圍外的值會壓制至範圍。</span><span class="sxs-lookup"><span data-stu-id="46f08-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="46f08-124">特定值區的範圍取決於 bucket 數目。</span><span class="sxs-lookup"><span data-stu-id="46f08-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="46f08-125">此效果適用于純點陣圖圖元。</span><span class="sxs-lookup"><span data-stu-id="46f08-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="46f08-126">輸入點陣圖的色彩通道是由 Alpha 色板除以，以計算此效果。</span><span class="sxs-lookup"><span data-stu-id="46f08-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="46f08-127">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="46f08-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="46f08-128">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="46f08-128">Type and default value</span></span>                                                   | <span data-ttu-id="46f08-129">Description</span><span class="sxs-lookup"><span data-stu-id="46f08-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f08-130">NumBins</span><span class="sxs-lookup"><span data-stu-id="46f08-130">NumBins</span></span><br/> <span data-ttu-id="46f08-131">D2D1 \_ 長條圖 \_ 的 \_ 數目 \_ 分類</span><span class="sxs-lookup"><span data-stu-id="46f08-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="46f08-132">UINT32</span><span class="sxs-lookup"><span data-stu-id="46f08-132">UINT32</span></span><br/> <span data-ttu-id="46f08-133">256</span><span class="sxs-lookup"><span data-stu-id="46f08-133">256</span></span><br/>                                         | <span data-ttu-id="46f08-134">指定用於長條圖的 bin 數目。</span><span class="sxs-lookup"><span data-stu-id="46f08-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="46f08-135">落在特定值區中的濃度值範圍取決於指定的 bucket 數目。</span><span class="sxs-lookup"><span data-stu-id="46f08-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="46f08-136">ChannelSelect</span><span class="sxs-lookup"><span data-stu-id="46f08-136">ChannelSelect</span></span><br/> <span data-ttu-id="46f08-137">D2D1 \_ 長條圖 \_ 的 \_ \_ 選擇通道</span><span class="sxs-lookup"><span data-stu-id="46f08-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="46f08-138">D2D1 \_ 通道 \_ 選取器</span><span class="sxs-lookup"><span data-stu-id="46f08-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="46f08-139">D2D1 \_ 通道 \_ 選取器 \_ R</span><span class="sxs-lookup"><span data-stu-id="46f08-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="46f08-140">指定用來產生長條圖的通道。</span><span class="sxs-lookup"><span data-stu-id="46f08-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="46f08-141">此效果具有對應至指定通道的單一資料輸出。</span><span class="sxs-lookup"><span data-stu-id="46f08-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="46f08-142">如需詳細資訊，請參閱 [通道選取器](#channel-selectors) 。</span><span class="sxs-lookup"><span data-stu-id="46f08-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="46f08-143">HistogramOutput</span><span class="sxs-lookup"><span data-stu-id="46f08-143">HistogramOutput</span></span><br/> <span data-ttu-id="46f08-144">D2D1 \_ 長條圖 \_ 的 \_ 長條圖 \_ 輸出</span><span class="sxs-lookup"><span data-stu-id="46f08-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="46f08-145">浮動\[\]</span><span class="sxs-lookup"><span data-stu-id="46f08-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="46f08-146">僅限輸出屬性。</span><span class="sxs-lookup"><span data-stu-id="46f08-146">Output property only.</span></span><br/>                    | <span data-ttu-id="46f08-147">輸出陣列。</span><span class="sxs-lookup"><span data-stu-id="46f08-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="46f08-148">通道選取器</span><span class="sxs-lookup"><span data-stu-id="46f08-148">Channel selectors</span></span>



| <span data-ttu-id="46f08-149">列舉型別</span><span class="sxs-lookup"><span data-stu-id="46f08-149">Enumeration</span></span>                | <span data-ttu-id="46f08-150">描述</span><span class="sxs-lookup"><span data-stu-id="46f08-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="46f08-151">D2D1 \_ 通道 \_ 選取器 \_ R</span><span class="sxs-lookup"><span data-stu-id="46f08-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="46f08-152">效果會根據紅色通道產生長條圖輸出。</span><span class="sxs-lookup"><span data-stu-id="46f08-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="46f08-153">D2D1 \_ 通道 \_ 選取器 \_ G</span><span class="sxs-lookup"><span data-stu-id="46f08-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="46f08-154">效果會根據綠色通道產生長條圖輸出。</span><span class="sxs-lookup"><span data-stu-id="46f08-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="46f08-155">D2D1 \_ 通道 \_ 選取器 \_ B</span><span class="sxs-lookup"><span data-stu-id="46f08-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="46f08-156">效果會根據藍色通道產生長條圖輸出。</span><span class="sxs-lookup"><span data-stu-id="46f08-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="46f08-157">D2D1 \_ 通道 \_ 選取器 \_ A</span><span class="sxs-lookup"><span data-stu-id="46f08-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="46f08-158">效果會根據 Alpha 色板產生長條圖輸出。</span><span class="sxs-lookup"><span data-stu-id="46f08-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="46f08-159">資料輸出</span><span class="sxs-lookup"><span data-stu-id="46f08-159">Data output</span></span>

<span data-ttu-id="46f08-160">此效果會輸出浮點數 \[ \] ，其中包含對應至指定之 bin 數目的專案數目。FLOAT 中的每個元素 \[ \] 都是浮點數。</span><span class="sxs-lookup"><span data-stu-id="46f08-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="46f08-161">元素的值會對應到該 bin 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="46f08-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="46f08-162">備註</span><span class="sxs-lookup"><span data-stu-id="46f08-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="46f08-163">如果裝置不支援 DirectCompute， [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) 方法會失敗，並傳回 HRESULT = D2DERR 的 \_ \_ 裝置 \_ 功能不足。</span><span class="sxs-lookup"><span data-stu-id="46f08-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="46f08-164">所有支援 DirectCompute 的 DirectX11 卡和 DirectX10 卡片都可以使用效果。</span><span class="sxs-lookup"><span data-stu-id="46f08-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46f08-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="46f08-165">Requirements</span></span>



| <span data-ttu-id="46f08-166">需求</span><span class="sxs-lookup"><span data-stu-id="46f08-166">Requirement</span></span> | <span data-ttu-id="46f08-167">值</span><span class="sxs-lookup"><span data-stu-id="46f08-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46f08-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46f08-168">Minimum supported client</span></span> | <span data-ttu-id="46f08-169">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46f08-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="46f08-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46f08-170">Minimum supported server</span></span> | <span data-ttu-id="46f08-171">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46f08-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="46f08-172">標頭</span><span class="sxs-lookup"><span data-stu-id="46f08-172">Header</span></span>                   | <span data-ttu-id="46f08-173">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="46f08-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="46f08-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="46f08-174">Library</span></span>                  | <span data-ttu-id="46f08-175">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="46f08-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="46f08-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="46f08-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46f08-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="46f08-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

