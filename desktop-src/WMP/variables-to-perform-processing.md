---
title: 要執行處理的變數
description: 要執行處理的變數
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，處理變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673604"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="b09e5-109">要執行處理的變數</span><span class="sxs-lookup"><span data-stu-id="b09e5-109">Variables to Perform Processing</span></span>

<span data-ttu-id="b09e5-110">用來處理延遲緩衝區的成員變數會處理 **位元組** 數量;它們是 **位元組** 指標，以及用來儲存位元組計數的整數。</span><span class="sxs-lookup"><span data-stu-id="b09e5-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="b09e5-111">這很適合用來處理8位的音訊，因為8位範例可妥善容納一個位元組的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b09e5-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="b09e5-112">不過，在處理16位音訊時，將它們轉換成 **簡短** 指標會比較方便，因此處理可以一次出現兩個位元組。</span><span class="sxs-lookup"><span data-stu-id="b09e5-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="b09e5-113">下列程式碼範例會配置新的16位指標，並新增指標變數來儲存延遲緩衝區結尾的位址。</span><span class="sxs-lookup"><span data-stu-id="b09e5-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="b09e5-114">將它插入至迴圈進入點之前的「案例16」區段：</span><span class="sxs-lookup"><span data-stu-id="b09e5-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="b09e5-115">8位處理常式的程式碼也會組態變數，以儲存延遲緩衝區結尾的位址。</span><span class="sxs-lookup"><span data-stu-id="b09e5-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="b09e5-116">儲存此值可讓您輕鬆地測試可移動的延遲緩衝區指標是否已到達延遲緩衝區的結尾。</span><span class="sxs-lookup"><span data-stu-id="b09e5-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="b09e5-117">下列範例程式碼會計算值：</span><span class="sxs-lookup"><span data-stu-id="b09e5-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="b09e5-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="b09e5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b09e5-119">**執行 CEcho：:D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="b09e5-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




