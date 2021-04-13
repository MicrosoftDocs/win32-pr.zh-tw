---
title: 將資料從一種格式轉換成另一種格式
description: 將資料從一種格式轉換成另一種格式
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- 音訊壓縮管理員 (的) 、轉換資料
- " (音效壓縮管理員) 、轉換資料"
- 進行中的範例，轉換資料
- 轉換資料
- acmStreamOpen 函式
- acmStreamSize 函式
- acmStreamPrepareHeader 函式
- acmStreamConvert 函式
- acmStreamUnprepareHeader 函式
- acmStreamClose 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300756"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="9c3cf-113">將資料從一種格式轉換成另一種格式</span><span class="sxs-lookup"><span data-stu-id="9c3cf-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="9c3cf-114">使用中的串流函數可支援資料格式轉換。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="9c3cf-115">在 [資料類型] 中的轉換器會變更格式，但不會變更資料類型。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="9c3cf-116">例如，轉換器模組可以將 44-kHz、16位資料變更為 44-kHz、8位的資料。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="9c3cf-117">下列的執行的函數支援資料格式轉換。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="9c3cf-118">它們會依照您通常使用它們的順序列出。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="9c3cf-119">[**AcmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)函式會開啟轉換資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="9c3cf-120">[**AcmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)函數會計算來源或目的緩衝區的適當大小。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="9c3cf-121">[**AcmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)函式會準備要在轉換中使用的來源和目的地緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="9c3cf-122">[**AcmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)函式會將來源緩衝區中的資料轉換成目的地格式，將轉換的資料寫入目的地緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="9c3cf-123">[**AcmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)函式會清除 **acmStreamPrepareHeader** 所準備的來源和目的地緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="9c3cf-124">釋放來源和目的地緩衝區之前，您必須先呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="9c3cf-125">[**AcmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)函式會關閉轉換資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="9c3cf-126">轉換資料時，請先識別來源格式，然後選擇目的地格式。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="9c3cf-127">最簡單的方法是使用 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) 函式，此函式會顯示格式選擇對話方塊，並傳回使用者的格式選項。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="9c3cf-128">當您知道來源和目的地格式時，您可以使用 [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) 來開啟轉換資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="9c3cf-129">然後，您可以使用 [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) 函數來判斷適當的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="9c3cf-130">下一步是使用 [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)準備要在轉換中使用的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="9c3cf-131">若要執行轉換，請使用 [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) ，直到處理完所有緩衝區為止。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="9c3cf-132">當轉換完成時，請使用 [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) 來清除緩衝區，然後使用 [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) 來關閉轉換資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c3cf-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




