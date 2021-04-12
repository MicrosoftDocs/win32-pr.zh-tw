---
title: 執行 DoProcessOutput
description: 執行 DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，DoProcessOutput
- DSP 外掛程式，DoProcessOutput
- 音訊 DSP 外掛程式，DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68562444a3a8f0bfacad26fc5246181d33cefa2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372299"
---
# <a name="implementing-doprocessoutput"></a><span data-ttu-id="78d4e-108">執行 DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="78d4e-108">Implementing DoProcessOutput</span></span>

<span data-ttu-id="78d4e-109">若要處理音訊資料，您必須在 **DoProcessOutput** 中執行幾個步驟。</span><span class="sxs-lookup"><span data-stu-id="78d4e-109">To process audio data, you'll need to perform several steps in **DoProcessOutput**.</span></span> <span data-ttu-id="78d4e-110">下列步驟會使用外掛程式 wizard 範例程式碼做為範例。</span><span class="sxs-lookup"><span data-stu-id="78d4e-110">The following steps use the plug-in wizard sample code as examples.</span></span> <span data-ttu-id="78d4e-111">如果您想要建立音訊 DSP 外掛程式，以處理外掛程式嚮導範例程式碼所使用之相同類型的媒體內容，您只需要變更步驟6中所參考的實際處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="78d4e-111">If you want to create an audio DSP plug-in that processes media content of the same type that the plug-in wizard sample code does, you'll only need to change the actual processing code referred to in step 6.</span></span> <span data-ttu-id="78d4e-112">以下是在 **DoProcessOutput** 中執行的所有步驟：</span><span class="sxs-lookup"><span data-stu-id="78d4e-112">Following are all the steps implemented in **DoProcessOutput**:</span></span>

-   <span data-ttu-id="78d4e-113">如果目前未啟用外掛程式，只需將資料原封不動地複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="78d4e-113">If the plug-in is not currently enabled, simply copy the data unchanged into the output buffer.</span></span> <span data-ttu-id="78d4e-114">如果外掛程式將資料轉換成不同的格式，您也必須在這裡進行轉換處理。</span><span class="sxs-lookup"><span data-stu-id="78d4e-114">If your plug-in converts the data into a different format, you must also do the conversion processing here.</span></span>

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   <span data-ttu-id="78d4e-115">取得輸入格式結構的指標。</span><span class="sxs-lookup"><span data-stu-id="78d4e-115">Retrieve a pointer to the input format structure.</span></span> <span data-ttu-id="78d4e-116">您將需要從此結構取出成員資料，因此請複製 *m \_ mtInput* 的指標。**pbformat** 至類型的本機指標變數，此變數符合格式結構類型。</span><span class="sxs-lookup"><span data-stu-id="78d4e-116">You'll need to retrieve member data from this structure, so copy the pointer from *m\_mtInput*.**pbformat** to a local pointer variable of a type that matches the format structure type.</span></span> <span data-ttu-id="78d4e-117">下列範例會儲存 **WAVEFORMATEX** 輸入格式結構的指標：</span><span class="sxs-lookup"><span data-stu-id="78d4e-117">The following example stores a pointer to a **WAVEFORMATEX** input format structure:</span></span>

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   <span data-ttu-id="78d4e-118">計算要處理的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="78d4e-118">Calculate the number of samples to process.</span></span> <span data-ttu-id="78d4e-119">外掛程式 wizard 產生的範例程式碼會藉由將 WAVEFORMATEX 輸入格式結構的 **nBlockAlign** 成員所處理的位元組數目相除，然後將結果乘以儲存在 **nChannels** 成員中的通道數目，來執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="78d4e-119">The sample code that the plug-in wizard generates performs this step by dividing the number of bytes to process by the **nBlockAlign** member of the WAVEFORMATEX input format structure, and then multiplying the result by the number of channels, which was stored in the **nChannels** member.</span></span> <span data-ttu-id="78d4e-120">下列範例取自外掛程式 wizard 範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="78d4e-120">The following example is from the plug-in wizard sample code:</span></span>

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  <span data-ttu-id="78d4e-121">判斷音訊的位深度。</span><span class="sxs-lookup"><span data-stu-id="78d4e-121">Determine the bit depth of the audio.</span></span> <span data-ttu-id="78d4e-122">外掛程式 wizard 範例程式碼會檢查 **WAVEFORMATEX** 結構的 **wBitsPerSample** 成員，以決定8位或16位音訊。</span><span class="sxs-lookup"><span data-stu-id="78d4e-122">The plug-in wizard sample code determines 8-bit or 16-bit audio by inspecting the **wBitsPerSample** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="78d4e-123">然後，它會在 switch 語句中使用該值，為每個位深度提供個別的處理常式。</span><span class="sxs-lookup"><span data-stu-id="78d4e-123">It then uses that value in a switch statement to provide separate processing routines for each bit depth.</span></span> <span data-ttu-id="78d4e-124">當您處理其他格式類型和位深度時，可能需要使用不同的技巧。</span><span class="sxs-lookup"><span data-stu-id="78d4e-124">You may need to use a different technique when dealing with other format types and bit depths.</span></span>
    2.  <span data-ttu-id="78d4e-125">建立迴圈，以逐步執行輸入緩衝區中的音訊範例。</span><span class="sxs-lookup"><span data-stu-id="78d4e-125">Create a loop to step through the audio samples in the input buffer.</span></span>
    3.  <span data-ttu-id="78d4e-126">從輸入緩衝區取出範例。</span><span class="sxs-lookup"><span data-stu-id="78d4e-126">Retrieve a sample from the input buffer.</span></span> <span data-ttu-id="78d4e-127">若要這麼做，請將輸入資料指標取值，並將結果儲存在 int 類型的變數中。若是16位音訊，您必須重新轉換短指標的位元組指標，以處理較大的音訊樣本精確度。</span><span class="sxs-lookup"><span data-stu-id="78d4e-127">You do this by dereferencing the input data pointer and storing the result in a variable of type int. For 16-bit audio, you must recast the BYTE pointer to a short pointer to handle the greater audio sample precision.</span></span> <span data-ttu-id="78d4e-128">有了值之後，您就可以立即遞增 *pbInputData* 指標，使其指向下一個範例。</span><span class="sxs-lookup"><span data-stu-id="78d4e-128">Once you have the value, you can immediately increment the *pbInputData* pointer so that it points to the next sample.</span></span> <span data-ttu-id="78d4e-129">下列範例示範：</span><span class="sxs-lookup"><span data-stu-id="78d4e-129">The following examples demonstrate this:</span></span>

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    <span data-ttu-id="78d4e-130">-或-</span><span class="sxs-lookup"><span data-stu-id="78d4e-130">-or-</span></span>

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  <span data-ttu-id="78d4e-131">執行處理。</span><span class="sxs-lookup"><span data-stu-id="78d4e-131">Perform the processing.</span></span> <span data-ttu-id="78d4e-132">這是您套用以某種方式變更範例的演算法的位置。</span><span class="sxs-lookup"><span data-stu-id="78d4e-132">This is where you apply the algorithms that change the sample somehow.</span></span> <span data-ttu-id="78d4e-133">您可以自行決定。</span><span class="sxs-lookup"><span data-stu-id="78d4e-133">What you do here is up to you.</span></span>
    2.  <span data-ttu-id="78d4e-134">將處理過的資料寫入至輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="78d4e-134">Write the processed data to the output buffer.</span></span> <span data-ttu-id="78d4e-135">立即將指標遞增至輸出緩衝區，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="78d4e-135">Immediately increment the pointer to the output buffer, as in the following example:</span></span>

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  <span data-ttu-id="78d4e-136">重複執行迴圈，直到處理完所有樣本為止。</span><span class="sxs-lookup"><span data-stu-id="78d4e-136">Repeat the loop until all the samples have been processed.</span></span>
    2.  <span data-ttu-id="78d4e-137">傳回適當的 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="78d4e-137">Return an appropriate **HRESULT**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78d4e-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="78d4e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78d4e-139">**執行音訊 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="78d4e-139">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




