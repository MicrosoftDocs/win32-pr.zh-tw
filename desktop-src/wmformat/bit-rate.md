---
title: 位元速度
description: 位元速度
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK，位元速率
- Advanced Systems Format (ASF) ，bit 速率
- ASF (Advanced Systems Format) ，bit 速率
- 位元速率，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675340"
---
# <a name="bit-rate"></a><span data-ttu-id="bfd3a-107">位元速度</span><span class="sxs-lookup"><span data-stu-id="bfd3a-107">Bit Rate</span></span>

<span data-ttu-id="bfd3a-108">位元速率指的是從 ASF 檔案傳遞的每秒資料量。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="bfd3a-109">位元速率測量的單位為每秒 (bps) 或每秒千位 (Kbps) 。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="bfd3a-110">位元速率通常會與頻寬混淆，這是網路資料傳輸容量的度量。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="bfd3a-111">頻寬也是以 bps 和 Kbps 來測量。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="bfd3a-112">Windows Media Format SDK 可以用來建立應用程式，以從網際網路或內部網路位置傳遞串流式 Windows Media 內容。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="bfd3a-113">當您在網路或網際網路上串流處理資料時，位元速率對終端使用者體驗而言相當重要。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="bfd3a-114">如果網路可用的頻寬小於 ASF 檔案的位元速率，檔案的播放將會以某種方式中斷。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="bfd3a-115">通常，頻寬不足會導致略過兩個樣本，或在多個資料經過緩衝處理時暫停播放。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="bfd3a-116">在建立時，系統會根據所用設定檔中包含的資料流程類型和數目，在建立時指派每個 ASF 檔案的位元速率值。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="bfd3a-117">個別的串流有自己的位元速率。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="bfd3a-118">位速率可以是固定的 (原始資料會以接近相同速率的平均資料量) 或變數的方式來進行壓縮， (原始資料會以平均維持相同品質的方式進行壓縮，即使這可能表示) 不平均的資料流程。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="bfd3a-119">不同的位速率類型可以套用至相同檔案中的不同資料流程。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="bfd3a-120">您可以針對數個不同的資料流程編碼相同的內容，每個資料流程各有不同的位元速率。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="bfd3a-121">然後您可以設定資料流程，讓它們彼此互斥。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="bfd3a-122">這可讓您建立單一檔案，以串流處理至具有不同頻寬的使用者。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="bfd3a-123">這項功能稱為「多位元率」或「MBR」。</span><span class="sxs-lookup"><span data-stu-id="bfd3a-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfd3a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfd3a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfd3a-125">**概念**</span><span class="sxs-lookup"><span data-stu-id="bfd3a-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="bfd3a-126">**固定位元速率 (CBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="bfd3a-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="bfd3a-127">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="bfd3a-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="bfd3a-128">**配置 檔**</span><span class="sxs-lookup"><span data-stu-id="bfd3a-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="bfd3a-129">**變數位速率 (VBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="bfd3a-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




