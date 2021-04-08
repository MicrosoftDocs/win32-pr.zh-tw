---
title: 建立 Echo 效果
description: 建立 Echo 效果
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，建立 echo 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020886"
---
# <a name="creating-the-echo-effect"></a><span data-ttu-id="969a1-109">建立 Echo 效果</span><span class="sxs-lookup"><span data-stu-id="969a1-109">Creating the Echo Effect</span></span>

<span data-ttu-id="969a1-110">您必須先從可調整音訊的 wizard 範例中移除程式碼。</span><span class="sxs-lookup"><span data-stu-id="969a1-110">You must first remove the code from the wizard sample that scales the audio.</span></span> <span data-ttu-id="969a1-111">從8位區段中，移除下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="969a1-111">From the 8-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="969a1-112"> (記得 m \_ fScaleFactor 已被 m dwDelayTime 取代 \_ 。 ) </span><span class="sxs-lookup"><span data-stu-id="969a1-112">(Remember that m\_fScaleFactor was replaced by m\_dwDelayTime.)</span></span>

<span data-ttu-id="969a1-113">從16位區段中，移除下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="969a1-113">From the 16-bit section, remove the following code:</span></span>


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



<span data-ttu-id="969a1-114">外掛程式 wizard 範例程式碼所提供的 **DoProcessOutput** 執行會建立 while 迴圈，以針對 Windows Media Player 所提供之輸入緩衝區中的每個樣本逐一查看一次。</span><span class="sxs-lookup"><span data-stu-id="969a1-114">The implementation of **DoProcessOutput** provided by the plug-in wizard sample code creates a while loop that iterates one time for each sample in the input buffer provided by Windows Media Player.</span></span> <span data-ttu-id="969a1-115">此迴圈的運作方式與8位和16位音訊相同，不過每個迴圈都需要個別的迴圈。</span><span class="sxs-lookup"><span data-stu-id="969a1-115">This loop works the same way for both 8-bit and 16-bit audio, although a separate loop is required for each.</span></span> <span data-ttu-id="969a1-116">在每個案例中，迴圈都會以下列測試起始：</span><span class="sxs-lookup"><span data-stu-id="969a1-116">In each case, the loop initiates with the following test:</span></span>


```C++
while (dwSamplesToProcess--)

```



<span data-ttu-id="969a1-117">在迴圈內，處理常式在8位和16位音訊方面都非常類似。</span><span class="sxs-lookup"><span data-stu-id="969a1-117">Once inside the loop, the processing routines are very similar for 8-bit and 16-bit audio.</span></span> <span data-ttu-id="969a1-118">主要差異在於8位區段中的程式碼會將資料值的範圍變更為-128 到127，然後在將資料寫入輸出緩衝區之前再次將範圍轉換回來。</span><span class="sxs-lookup"><span data-stu-id="969a1-118">The main difference is that the code in the 8-bit section changes the range of data values to -128 through 127, and then converts the range back again before writing the data to the output buffer.</span></span> <span data-ttu-id="969a1-119">在處理期間保留音訊波形的對稱是很重要的。</span><span class="sxs-lookup"><span data-stu-id="969a1-119">This is important to retain the symmetry of the audio waveform during processing.</span></span>

<span data-ttu-id="969a1-120">現在您可以開始新增和取代處理迴圈中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="969a1-120">Now you can begin to add and replace code in the processing loop.</span></span>

## <a name="retrieve-a-sample-from-the-input-buffer"></a><span data-ttu-id="969a1-121">從輸入緩衝區取出範例</span><span class="sxs-lookup"><span data-stu-id="969a1-121">Retrieve a Sample from the Input Buffer</span></span>

<span data-ttu-id="969a1-122">在迴圈的每個反復專案期間，會從輸入緩衝區取出單一樣本。</span><span class="sxs-lookup"><span data-stu-id="969a1-122">During each iteration of the loop, a single sample is retrieved from the input buffer.</span></span> <span data-ttu-id="969a1-123">若為8位音訊，此範例會移至新的範圍，然後輸入緩衝區的指標會前進到下一個範例。</span><span class="sxs-lookup"><span data-stu-id="969a1-123">For 8-bit audio, the sample is shifted into the new range, and then the pointer to the input buffer is advanced to the next sample.</span></span> <span data-ttu-id="969a1-124">下列程式碼來自于外掛程式 wizard：</span><span class="sxs-lookup"><span data-stu-id="969a1-124">The following code is from the plug-in wizard:</span></span>


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



<span data-ttu-id="969a1-125">若是16位音訊，除了正規化以外，程式也相同：</span><span class="sxs-lookup"><span data-stu-id="969a1-125">For 16-bit audio, the process is the same except for the normalization:</span></span>


```C++
// Get the input sample.
int i = *pwInputData++;

```



<span data-ttu-id="969a1-126">請記住，16位程式碼中的指標已轉換成 **short** 類型。</span><span class="sxs-lookup"><span data-stu-id="969a1-126">Remember that the pointers in the 16-bit code have been converted to type **short**.</span></span>

## <a name="retrieve-a-sample-from-the-delay-buffer"></a><span data-ttu-id="969a1-127">從延遲緩衝區取出範例</span><span class="sxs-lookup"><span data-stu-id="969a1-127">Retrieve a Sample from the Delay Buffer</span></span>

<span data-ttu-id="969a1-128">接下來，從延遲緩衝區取出單一範例。</span><span class="sxs-lookup"><span data-stu-id="969a1-128">Next, retrieve a single sample from the delay buffer.</span></span> <span data-ttu-id="969a1-129">若為8位程式碼，延遲樣本會儲存在其原生範圍0到255。</span><span class="sxs-lookup"><span data-stu-id="969a1-129">For 8-bit code, the delay samples are stored in their native range of 0 to 255.</span></span> <span data-ttu-id="969a1-130">您必須加入的下列程式碼會捕獲8位延遲範例：</span><span class="sxs-lookup"><span data-stu-id="969a1-130">The following code, which you must add, retrieves an 8-bit delay sample:</span></span>


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



<span data-ttu-id="969a1-131">若是16位音訊，此程式很類似：</span><span class="sxs-lookup"><span data-stu-id="969a1-131">For 16-bit audio, the process is similar:</span></span>


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a><span data-ttu-id="969a1-132">將輸入範例寫入延遲緩衝區</span><span class="sxs-lookup"><span data-stu-id="969a1-132">Write the Input Sample to the Delay Buffer</span></span>

<span data-ttu-id="969a1-133">現在，您必須將輸入範例儲存在延遲緩衝區中您抓取延遲樣本的相同位置。</span><span class="sxs-lookup"><span data-stu-id="969a1-133">Now, you must store the input sample in the delay buffer in the same location from which you retrieved the delay sample.</span></span> <span data-ttu-id="969a1-134">以下是您必須為8位音訊新增的程式碼：</span><span class="sxs-lookup"><span data-stu-id="969a1-134">The following is the code you must add for 8-bit audio:</span></span>


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



<span data-ttu-id="969a1-135">這是要為16位區段新增的程式碼：</span><span class="sxs-lookup"><span data-stu-id="969a1-135">This is the code to add for the 16-bit section:</span></span>


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a><span data-ttu-id="969a1-136">移動延遲緩衝區指標</span><span class="sxs-lookup"><span data-stu-id="969a1-136">Move the Delay Buffer Pointer</span></span>

<span data-ttu-id="969a1-137">現在，延遲緩衝區中的工作已完成此反復專案，您可以將可移動指標前進至延遲緩衝區。</span><span class="sxs-lookup"><span data-stu-id="969a1-137">Now that the work in the delay buffer is finished for this iteration, you can advance the movable pointer to the delay buffer.</span></span> <span data-ttu-id="969a1-138">如果指標到達迴圈緩衝區的結尾，您必須變更其值以指向緩衝區的標頭。</span><span class="sxs-lookup"><span data-stu-id="969a1-138">If the pointer reaches the end of the circular buffer, you must change its value to point to the head of the buffer.</span></span> <span data-ttu-id="969a1-139">若要為8位音訊執行這項操作，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="969a1-139">To do this for 8-bit audio, use the following code:</span></span>


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



<span data-ttu-id="969a1-140">以下是16位區段的程式碼：</span><span class="sxs-lookup"><span data-stu-id="969a1-140">Here is the code for the 16-bit section:</span></span>


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



<span data-ttu-id="969a1-141">由於16位區段中的指標其實是成員變數的複本，因此您必須記得使用新的位址來更新成員變數中的值。</span><span class="sxs-lookup"><span data-stu-id="969a1-141">Since the pointer in the 16-bit section is really a copy of the member variable, you must remember to update the value in the member variable with the new address.</span></span> <span data-ttu-id="969a1-142">如果您無法這麼做，延遲緩衝區指標會重複指向緩衝區的標頭，而且您的 echo 效果將無法如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="969a1-142">If you fail to do this, the delay buffer pointer will point to the head of the buffer repeatedly and your echo effect will not work as expected.</span></span> <span data-ttu-id="969a1-143">將下列程式碼新增至16位區段：</span><span class="sxs-lookup"><span data-stu-id="969a1-143">Add the following code to the 16-bit section:</span></span>


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a><span data-ttu-id="969a1-144">使用 Delay 範例混合輸入範例</span><span class="sxs-lookup"><span data-stu-id="969a1-144">Mix the Input Sample with the Delay Sample</span></span>

<span data-ttu-id="969a1-145">這是您使用濕混合和幹混合值的位置，以建立最終的輸出範例。</span><span class="sxs-lookup"><span data-stu-id="969a1-145">This is where you use the wet mix and dry mix values to create the final output sample.</span></span> <span data-ttu-id="969a1-146">您只需將每個範例乘以表示樣本最後信號百分比的浮點值。</span><span class="sxs-lookup"><span data-stu-id="969a1-146">You simply multiply each sample by the floating-point value that represents the percentage of the final signal for the sample.</span></span> <span data-ttu-id="969a1-147">將輸入範例乘以儲存在 m fDryMix 中的值， \_ 然後將延遲樣本乘以 m fWetMix 中儲存的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="969a1-147">Multiply the input sample by the value stored in m\_fDryMix; multiply the delay sample by the value stored in m\_fWetMix.</span></span> <span data-ttu-id="969a1-148">然後，新增兩個值。</span><span class="sxs-lookup"><span data-stu-id="969a1-148">Then, add the two values.</span></span> <span data-ttu-id="969a1-149">您必須新增的程式碼在8位和16位區段中都是相同的：</span><span class="sxs-lookup"><span data-stu-id="969a1-149">The code you must add is identical for the 8-bit and 16-bit sections:</span></span>


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a><span data-ttu-id="969a1-150">將資料寫入輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="969a1-150">Write the Data to the Output Buffer</span></span>

<span data-ttu-id="969a1-151">最後，將混合範例複製到輸出緩衝區，然後前進輸出緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="969a1-151">Finally, copy the mixed sample to the output buffer, and then advance the output buffer pointer.</span></span> <span data-ttu-id="969a1-152">若為8位音訊，外掛程式 wizard 會使用下列程式碼，將範例傳回至其原始範圍：</span><span class="sxs-lookup"><span data-stu-id="969a1-152">For 8-bit audio, the plug-in wizard uses the following code to return the sample to its original range:</span></span>


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



<span data-ttu-id="969a1-153">若是16位音訊，嚮導會使用下列程式碼做為處理迴圈中的最後一個步驟：</span><span class="sxs-lookup"><span data-stu-id="969a1-153">For 16-bit audio, the wizard uses the following code as the final step in the processing loop:</span></span>


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a><span data-ttu-id="969a1-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="969a1-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="969a1-155">**執行 CEcho：:D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="969a1-155">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




