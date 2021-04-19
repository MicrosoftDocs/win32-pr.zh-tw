---
title: 處理音訊資料
description: 處理音訊資料
ms.assetid: ba41e3f4-d991-4da6-9091-7a7e42622e76
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，音訊資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc14acb99aed20825ff970025363c6a795a0c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965991"
---
# <a name="processing-the-audio-data"></a><span data-ttu-id="2b31a-109">處理音訊資料</span><span class="sxs-lookup"><span data-stu-id="2b31a-109">Processing the Audio Data</span></span>

<span data-ttu-id="2b31a-110">**DoProcessOutput** 的預設執行一開始會先抓取有效 **WAVEFORMATEX** 結構的指標，就像是在 **AllocateStreamingResources** 中完成一樣。</span><span class="sxs-lookup"><span data-stu-id="2b31a-110">The default implementation of **DoProcessOutput** begins by retrieving a pointer to a valid **WAVEFORMATEX** structure, exactly like was done in **AllocateStreamingResources**.</span></span> <span data-ttu-id="2b31a-111">然後，它會使用該結構中的資訊來計算輸入緩衝區中等候處理的樣本數。</span><span class="sxs-lookup"><span data-stu-id="2b31a-111">It then uses the information in that structure to calculate the number of samples in the input buffer waiting to be processed.</span></span> <span data-ttu-id="2b31a-112">下列程式碼來自預設的執行：</span><span class="sxs-lookup"><span data-stu-id="2b31a-112">The following code is from the default implementation:</span></span>


```C++
// Get a pointer to the valid WAVEFORMATEX structure
// for the current media type.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;

// Calculate the number of samples to process.
DWORD dwSamplesToProcess = (*cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;

```



<span data-ttu-id="2b31a-113">然後，程式碼會檢查 **wBitsPerSample** 成員以判斷音訊的位深度。</span><span class="sxs-lookup"><span data-stu-id="2b31a-113">Then, the code inspects the **wBitsPerSample** member to determine the bit depth of the audio.</span></span> <span data-ttu-id="2b31a-114">Switch 語句中會使用這個值，為8位和16位的音訊提供個別的處理。</span><span class="sxs-lookup"><span data-stu-id="2b31a-114">This value is used in a switch statement to provide separate processing for 8-bit and 16-bit audio.</span></span>

## <a name="differences-between-8-bit-and-16-bit-audio"></a><span data-ttu-id="2b31a-115">8位和16位音訊之間的差異</span><span class="sxs-lookup"><span data-stu-id="2b31a-115">Differences Between 8-bit and 16-bit Audio</span></span>

<span data-ttu-id="2b31a-116">8位和16位音訊之間有重要的差異。</span><span class="sxs-lookup"><span data-stu-id="2b31a-116">There are important differences between 8-bit and 16-bit audio.</span></span> <span data-ttu-id="2b31a-117">因此，用來建立 echo 效果的處理常式會有所不同。</span><span class="sxs-lookup"><span data-stu-id="2b31a-117">Therefore, the processing routines to create the echo effect are different.</span></span> <span data-ttu-id="2b31a-118">這兩種格式的差異如下：</span><span class="sxs-lookup"><span data-stu-id="2b31a-118">The two formats differ in the following ways:</span></span>

-   <span data-ttu-id="2b31a-119">每個格式都有不同的取樣大小：8位樣本每個都佔用一個位元組的記憶體，而16位樣本每個都佔用兩個位元組。</span><span class="sxs-lookup"><span data-stu-id="2b31a-119">Each format has a different sample size: 8-bit samples each occupy one byte of memory, while 16-bit samples each occupy two bytes.</span></span>
-   <span data-ttu-id="2b31a-120">每種格式代表音訊振幅的方式不同。</span><span class="sxs-lookup"><span data-stu-id="2b31a-120">Each format represents the audio amplitude differently.</span></span> <span data-ttu-id="2b31a-121">8位音訊是以0到255範圍的不帶正負號的整數表示;128的值代表無聲。</span><span class="sxs-lookup"><span data-stu-id="2b31a-121">8-bit audio is represented by an unsigned integer with a range from 0 to 255; a value of 128 represents silence.</span></span> <span data-ttu-id="2b31a-122">16位音訊會以帶正負號的整數表示，範圍從-32768 到 32767;值為零表示無回應。</span><span class="sxs-lookup"><span data-stu-id="2b31a-122">16-bit audio is represented by a signed integer with a range from -32768 to 32767; a value of zero represents silence.</span></span>

<span data-ttu-id="2b31a-123">雖然建立回應效果的程式對每種格式基本上都完全相同，但詳細資料必須稍有不同。</span><span class="sxs-lookup"><span data-stu-id="2b31a-123">While the process of creating the echo effect is fundamentally identical for each format, the details must differ slightly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b31a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b31a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b31a-125">**執行 CEcho：:D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="2b31a-125">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




