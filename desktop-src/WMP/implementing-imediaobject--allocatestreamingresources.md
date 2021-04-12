---
title: 執行 IMediaObject AllocateStreamingResources
description: 執行 IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- Windows Media Player 外掛程式，Echo 範例串流資源
- 外掛程式，Echo 範例串流資源
- 數位信號處理外掛程式，Echo 範例串流資源
- DSP 外掛程式，Echo 範例串流資源
- Echo DSP 外掛程式範例，串流資源
- Echo DSP 外掛程式範例，延遲緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1e347e35eaabbcbcc00a586e4cba0d8ad31cc6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372319"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a><span data-ttu-id="35e0a-109">執行 IMediaObject：： AllocateStreamingResources</span><span class="sxs-lookup"><span data-stu-id="35e0a-109">Implementing IMediaObject::AllocateStreamingResources</span></span>

<span data-ttu-id="35e0a-110">在 Echo 範例中， **AllocateStreamingResources** 方法會建立延遲緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35e0a-110">In the Echo sample, the **AllocateStreamingResources** method creates the delay buffer.</span></span> <span data-ttu-id="35e0a-111">做法是執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="35e0a-111">It does this by doing the following:</span></span>

1.  <span data-ttu-id="35e0a-112">計算對應至指定媒體類型之指定延遲時間的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="35e0a-112">Calculating a size for the buffer that corresponds to the specified delay time for the given media type.</span></span>
2.  <span data-ttu-id="35e0a-113">配置新的記憶體或重新配置緩衝區大小（如果已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="35e0a-113">Either allocating new memory or reallocating the buffer size if it already exists.</span></span>
3.  <span data-ttu-id="35e0a-114">呼叫以代表無聲的值來填滿緩衝區的方法。</span><span class="sxs-lookup"><span data-stu-id="35e0a-114">Calling a method that fills the buffer with values representing silence.</span></span>

<span data-ttu-id="35e0a-115">無回應的值會根據位深度而有所不同。</span><span class="sxs-lookup"><span data-stu-id="35e0a-115">The value for silence is different depending upon the bit depth.</span></span> <span data-ttu-id="35e0a-116">若為8位音訊，無回應會以十六進位值80表示;若是16位音訊，無回應會以零表示。</span><span class="sxs-lookup"><span data-stu-id="35e0a-116">For 8-bit audio, silence is represented by the hex value 80; for 16-bit audio, silence is represented by zero.</span></span>

## <a name="calculating-the-delay-buffer-size"></a><span data-ttu-id="35e0a-117">計算延遲緩衝區大小</span><span class="sxs-lookup"><span data-stu-id="35e0a-117">Calculating the Delay Buffer Size</span></span>

<span data-ttu-id="35e0a-118">為了計算延遲緩衝區所需的大小，您必須先取出包含音訊資料相關資訊的 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="35e0a-118">In order to calculate the size required for the delay buffer, you must first retrieve a **WAVEFORMATEX** structure that contains information about the audio data.</span></span> <span data-ttu-id="35e0a-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span><span class="sxs-lookup"><span data-stu-id="35e0a-119">The following example retrieves a pointer to this structure from the input **DMO\_MEDIA\_TYPE** structure:</span></span>


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



<span data-ttu-id="35e0a-120">一旦將指標儲存至適當的 **WAVEFORMATEX** 結構之後，您就可以檢查其成員並使用它們來計算所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="35e0a-120">Once you have stored a pointer to the proper **WAVEFORMATEX** structure, you can inspect its members and use them to calculate the required buffer size.</span></span> <span data-ttu-id="35e0a-121">下列程式碼範例將示範此範例：</span><span class="sxs-lookup"><span data-stu-id="35e0a-121">The following code example demonstrates this:</span></span>


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



<span data-ttu-id="35e0a-122">此演算法會藉由將延遲時間（以毫秒為單位）乘以每毫秒樣本數來計算緩衝區大小，然後將結果乘以通道數目，然後將結果乘以每個樣本的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="35e0a-122">This algorithm computes the buffer size by multiplying the delay time, in milliseconds, by the number of samples per millisecond, then multiplying the result by the number of channels, and then multiplying the result by the number of bytes per sample.</span></span> <span data-ttu-id="35e0a-123">通道數目和每個樣本的位元組數目並不明顯;它們是在 nBlockAlign 成員中進行編碼。</span><span class="sxs-lookup"><span data-stu-id="35e0a-123">The number of channels and the number of bytes per sample are not obvious; they are encoded in the nBlockAlign member.</span></span> <span data-ttu-id="35e0a-124">除以1000可將 nSamplesPerSec 值縮減為每毫秒樣本數;毫秒是所需的單位，因為延遲時間以毫碼錶示。</span><span class="sxs-lookup"><span data-stu-id="35e0a-124">Dividing by 1000 reduces the nSamplesPerSec value to samples per millisecond; the millisecond is the desired unit because the delay time is expressed in milliseconds.</span></span>

## <a name="allocating-the-delay-buffer-memory"></a><span data-ttu-id="35e0a-125">配置延遲緩衝區記憶體</span><span class="sxs-lookup"><span data-stu-id="35e0a-125">Allocating the Delay Buffer Memory</span></span>

<span data-ttu-id="35e0a-126">當您計算出記憶體需求之後，就可以配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="35e0a-126">Once you have calculated the memory requirements, you can allocate the buffer.</span></span> <span data-ttu-id="35e0a-127">緩衝區可能需要刪除（如果存在的話），例如當使用者叫用屬性頁來變更延遲時間值時。</span><span class="sxs-lookup"><span data-stu-id="35e0a-127">The buffer may need to be deleted if it exists, such as when the user invokes the property page to change the delay time value.</span></span> <span data-ttu-id="35e0a-128">下列程式碼示範如何配置延遲緩衝區：</span><span class="sxs-lookup"><span data-stu-id="35e0a-128">The following code demonstrates allocating the delay buffer:</span></span>


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



<span data-ttu-id="35e0a-129">如果緩衝區已成功配置，您應該將可移動指標移至緩衝區的標頭，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="35e0a-129">If the buffer is successfully allocated, you should move the movable pointer to the head of the buffer, as demonstrated in the following example:</span></span>


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a><span data-ttu-id="35e0a-130">使用無聲填滿延遲緩衝區</span><span class="sxs-lookup"><span data-stu-id="35e0a-130">Filling the Delay Buffer with Silence</span></span>

<span data-ttu-id="35e0a-131">撰寫一個方法來填滿延遲緩衝區，並以代表無聲的值來填滿延遲緩衝區是很方便的。</span><span class="sxs-lookup"><span data-stu-id="35e0a-131">It is convenient to write a method to fill the delay buffer with values representing silence.</span></span> <span data-ttu-id="35e0a-132">方法應該接收有效 WAVEFORMATEX 結構的指標，然後檢查 wBitsPerSample 成員以判斷音訊是否為8位或更高。</span><span class="sxs-lookup"><span data-stu-id="35e0a-132">The method should receive the pointer to the valid WAVEFORMATEX structure and then inspect the wBitsPerSample member to determine whether the audio is 8-bit or higher.</span></span> <span data-ttu-id="35e0a-133">下列範例會以正確的無聲值填入延遲緩衝區：</span><span class="sxs-lookup"><span data-stu-id="35e0a-133">The following example fills the delay buffer with the correct value for silence:</span></span>


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



<span data-ttu-id="35e0a-134">請記得將函式的向前宣告新增至私用區段中的標頭檔 Echo：</span><span class="sxs-lookup"><span data-stu-id="35e0a-134">Remember to add the forward declaration for the function to the header file Echo.h in the private section:</span></span>


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



<span data-ttu-id="35e0a-135">您應該在 AllocateStreamingResources 結尾加入程式碼，以便在每次建立或調整延遲緩衝區時呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="35e0a-135">You should add code at the end of AllocateStreamingResources to call this method each time the delay buffer is created or resized.</span></span> <span data-ttu-id="35e0a-136">下列範例程式碼會將名為 pWave 的 WAVEFORMATEX 指標傳遞給新的方法：</span><span class="sxs-lookup"><span data-stu-id="35e0a-136">The following example code passes the WAVEFORMATEX pointer named pWave to the new method:</span></span>


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a><span data-ttu-id="35e0a-137">重新配置延遲緩衝區記憶體</span><span class="sxs-lookup"><span data-stu-id="35e0a-137">Reallocating the Delay Buffer Memory</span></span>

<span data-ttu-id="35e0a-138">當使用者使用 [屬性] 頁面變更延遲時間時，延遲緩衝區的大小也必須變更。</span><span class="sxs-lookup"><span data-stu-id="35e0a-138">When the user changes the delay time by using the property page, the size of the delay buffer must change as well.</span></span> <span data-ttu-id="35e0a-139">您已將程式碼新增至 AllocateStreamingResources 以調整緩衝區大小，但您需要將程式程式碼加入至 CEcho：:p \_ 每次屬性值變更時，呼叫資源配置方法。</span><span class="sxs-lookup"><span data-stu-id="35e0a-139">You've already added the code to AllocateStreamingResources to resize the buffer, but you need to add a line of code to CEcho::put\_delay to call the resource allocation method each time the property value changes.</span></span> <span data-ttu-id="35e0a-140">程式碼如下：</span><span class="sxs-lookup"><span data-stu-id="35e0a-140">Here is the code:</span></span>


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a><span data-ttu-id="35e0a-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="35e0a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35e0a-142">**使用串流資源**</span><span class="sxs-lookup"><span data-stu-id="35e0a-142">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




