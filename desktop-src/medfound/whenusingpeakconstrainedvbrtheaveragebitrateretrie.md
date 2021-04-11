---
description: 當我使用尖峰限制的 VBR 時，從編解碼器物件取出的平均位元速率會大於尖峰位元速率。
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: 當我使用尖峰限制的 VBR 時，從編解碼器物件取出的平均位元速率會大於尖峰位元速率。 這有何可能？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318912"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="090b8-104">當我使用尖峰限制的 VBR 時，從編解碼器物件取出的平均位元速率會大於尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="090b8-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="090b8-105">這有何可能？</span><span class="sxs-lookup"><span data-stu-id="090b8-105">How is that possible?</span></span>

<span data-ttu-id="090b8-106">平均位元速率和尖峰位速率之間的關聯性通常會被誤解。</span><span class="sxs-lookup"><span data-stu-id="090b8-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="090b8-107">尖峰位速率會描述尖峰緩衝區視窗所指定的一段時間內的緩衝區條件約束。</span><span class="sxs-lookup"><span data-stu-id="090b8-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="090b8-108">雙通過 VBR (不受限制或尖峰限制的平均位元速率) 是檔案持續時間內每秒的平均位數。</span><span class="sxs-lookup"><span data-stu-id="090b8-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="090b8-109">如同有漏洞值區 [緩衝區模型](the-leaky-bucket-buffer-model.md)中所述，在一段時間內使用的實際位速率（等於緩衝區視窗）可以接近位元速率兩倍。</span><span class="sxs-lookup"><span data-stu-id="090b8-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="090b8-110">這是因為緩衝區定義為等於緩衝區視窗 (的位元速率乘以位元組數（以秒) 為單位），所以會以固定的速率清空。</span><span class="sxs-lookup"><span data-stu-id="090b8-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="090b8-111">例如，在 56 Kbps 串流的1秒內，編碼器會建立總計 59 Kb 的範例。</span><span class="sxs-lookup"><span data-stu-id="090b8-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="090b8-112">因此，56 Kb 的資料會在該秒內從緩衝區中移除，並將 3 Kb 保留在緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="090b8-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="090b8-113">如果資料流程的緩衝區視窗為三秒，因此緩衝區大小總計為 168 Kb，則需要將近40秒來填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="090b8-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="090b8-114">資料流程的平均位元速率 (如果其持續時間小於填滿緩衝區所花費的時間) 為 59 Kbps，即使位元速率設定為 56 Kbps 也一樣。</span><span class="sxs-lookup"><span data-stu-id="090b8-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="090b8-115">相同的現象也適用于尖峰位速率條件約束。</span><span class="sxs-lookup"><span data-stu-id="090b8-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="090b8-116">針對簡短內容，編解碼器物件在編碼完成後所計算的平均位速率可能會大於尖峰位元速率。</span><span class="sxs-lookup"><span data-stu-id="090b8-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="090b8-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="090b8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="090b8-118">常見問題集</span><span class="sxs-lookup"><span data-stu-id="090b8-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



