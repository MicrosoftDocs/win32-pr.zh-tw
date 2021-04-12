---
title: 固定位元速率 (CBR) 編碼
description: 固定位元速率 (CBR) 編碼
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK，CBR 編碼
- 'Windows Media Format SDK，常數位元速率 (CBR) '
- 編解碼器，CBR 編碼
- '編解碼器、常數速率 (CBR) '
- '固定位元速率 (CBR) '
- 'CBR (常數位速率) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372539"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="5c8e6-109">固定位元速率 (CBR) 編碼</span><span class="sxs-lookup"><span data-stu-id="5c8e6-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="5c8e6-110">常數位速率 (CBR) 編碼是 Windows Media Format SDK 的預設編碼方法。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="5c8e6-111">使用 CBR 編碼時，您會指定資料流程的目標位速率，且編解碼器會使用所需的壓縮數量來達成。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="5c8e6-112">在編碼之前，使用 CBR 編碼，編碼資料流程的位元速率和大小都是已知的。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="5c8e6-113">例如，如果您要將三分鐘的歌曲編碼成每秒32000位，您知道檔案大小大約是 704 kb (32000 bps x 180 秒/8 位/每個位元組/1024) 。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="5c8e6-114">您也知道串流編碼內容所需的頻寬大約是每秒32000位。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="5c8e6-115">下一節所述的限制變數位速率編碼 () 也可讓您知道編碼之前的位元速率，但由於速率是變數，因此產生的檔案無法有效率地串流處理為在 CBR 模式中編碼的檔案。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="5c8e6-116">使用 CBR 時，一段時間的位元速率永遠保持接近平均或目標位元速率，而且可以指定變異數。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="5c8e6-117">CBR 編碼的缺點是編碼內容的品質不會是常數。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="5c8e6-118">因為有些內容較難壓縮，所以 CBR 串流的部分會比其他部分的品質低。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="5c8e6-119">例如，典型的電影有一些相當靜態的場景，以及一些完全行動的場景。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="5c8e6-120">如果您使用 CBR 將電影編碼、靜態的場景，因此可以有效率地編碼，則其品質會比動作場景高，更難以有效率地編碼。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="5c8e6-121">CBR 編碼也可能導致不一致的品質從某個檔案到另一個檔案。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="5c8e6-122">如果您使用 CBR 以相同的位元速率來編碼數個不同內容的歌曲，您可能會注意到兩者之間的品質有一些差異。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="5c8e6-123">一般而言，CBR 檔案品質的變化會以較低的位元速率更明顯。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="5c8e6-124">以較高的位元速率來說，CBR 編碼檔案的品質仍會有所不同，但對使用者而言，品質問題將會比較不明顯。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="5c8e6-125">使用 CBR 編碼時，您應該在傳遞案例允許的情況下設定最高的頻寬。</span><span class="sxs-lookup"><span data-stu-id="5c8e6-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c8e6-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c8e6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8e6-127">**選擇編碼方法**</span><span class="sxs-lookup"><span data-stu-id="5c8e6-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="5c8e6-128">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="5c8e6-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="5c8e6-129">**變數位速率 (VBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="5c8e6-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




