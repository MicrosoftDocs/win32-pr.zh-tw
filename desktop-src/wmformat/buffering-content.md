---
title: 緩衝處理內容
description: 緩衝處理內容
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media Format SDK，緩衝內容
- 緩衝處理內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967807"
---
# <a name="buffering-content"></a><span data-ttu-id="b015b-105">緩衝處理內容</span><span class="sxs-lookup"><span data-stu-id="b015b-105">Buffering Content</span></span>

<span data-ttu-id="b015b-106">當讀取器物件開啟串流檔案時，它會根據檔案標頭中的設定來決定緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="b015b-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="b015b-107">您可以把緩衝區想像成一個值區，而底部的孔會以固定速率流失。</span><span class="sxs-lookup"><span data-stu-id="b015b-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="b015b-108">只要值區填滿的速率不是，平均地大於它流失的速率時，值區永遠不會溢位。</span><span class="sxs-lookup"><span data-stu-id="b015b-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="b015b-109">虛數值區流失的速率是資料流程的位元速率。</span><span class="sxs-lookup"><span data-stu-id="b015b-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="b015b-110">值區填滿的速率是實際的串流位元速率。</span><span class="sxs-lookup"><span data-stu-id="b015b-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="b015b-111">壓縮資料流程中的資料會根據所達到的壓縮量而有所不同，從樣本到樣本的大小。</span><span class="sxs-lookup"><span data-stu-id="b015b-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="b015b-112">因此，即使在設定檔中設定資料流程的位元速率，它還是代表平均位元速率，而不是常數。</span><span class="sxs-lookup"><span data-stu-id="b015b-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="b015b-113">另一個對緩衝處理常式而言很重要的資料流程設定是緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="b015b-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="b015b-114">緩衝區視窗會以時間測量，並指定可緩衝處理的內容數量。</span><span class="sxs-lookup"><span data-stu-id="b015b-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="b015b-115">您可以使用 [緩衝區] 視窗找到虛構值區的容量。</span><span class="sxs-lookup"><span data-stu-id="b015b-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="b015b-116">例如，如果您的資料流程的位元速率為 32 Kbps，而緩衝區視窗為3秒，則緩衝區的大小會調整為每秒3秒的 32 Kbps 內容，或12000個位元組 (每秒32000位 x 3 秒/8 位的位元組) 。</span><span class="sxs-lookup"><span data-stu-id="b015b-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="b015b-117">編解碼器會限制編碼樣本的實際串流處理位元速率之間的變化，如此一來，在一段時間內會等於緩衝區視窗，平均位元速率就不會大於資料流程的位元速率。</span><span class="sxs-lookup"><span data-stu-id="b015b-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="b015b-118">一般來說，您會在設定檔中設定資料流程的位元速率和緩衝區視窗，而寫入器會處理其餘部分。</span><span class="sxs-lookup"><span data-stu-id="b015b-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="b015b-119">不過，當將壓縮的範例傳遞給讀取器時，您必須將目的地設定檔中資料流程的位元速率和緩衝區視窗設定為壓縮資料流程的值，以確保將正確的值傳送至新的檔案。</span><span class="sxs-lookup"><span data-stu-id="b015b-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b015b-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b015b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b015b-121">**概念**</span><span class="sxs-lookup"><span data-stu-id="b015b-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="b015b-122">**媒體範例**</span><span class="sxs-lookup"><span data-stu-id="b015b-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="b015b-123">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="b015b-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




