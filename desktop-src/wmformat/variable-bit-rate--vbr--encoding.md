---
title: 變數位速率 (VBR) 編碼
description: 變數位速率 (VBR) 編碼
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK，VBR 編碼
- 'Windows Media Format SDK，變數位元速率 (VBR) '
- Windows Media Format SDK，以品質為基礎的 VBR 編碼
- Windows Media Format SDK，未受限制的 VBR 編碼
- Windows Media Format SDK，受限的 VBR 編碼
- 編解碼器，VBR 編碼
- '編解碼器、變數位元速率 (VBR) '
- 編解碼器、以品質為基礎的 VBR 編碼
- 編解碼器，未受限制的 VBR 編碼
- 編解碼器，受限的 VBR 編碼
- 變數位元速率 (VBR) ，關於
- VBR (變數位速率) ，關於
- 以品質為基礎的 VBR 編碼，關於
- 未受限制的 VBR 編碼，關於
- 受限的 VBR 編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106990882"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="a6dcb-118">變數位速率 (VBR) 編碼</span><span class="sxs-lookup"><span data-stu-id="a6dcb-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="a6dcb-119">變數位元速率 (VBR) 編碼方式，是 (CBR) 的常數速率編碼的替代方式，而且有些編解碼器支援。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="a6dcb-120">在 CBR 編碼的目的是維持編碼媒體的位元速率時，VBR 會致力於達到編碼媒體的最佳品質。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="a6dcb-121">已編碼內容的品質取決於壓縮和解壓縮內容時遺失的資料量。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="a6dcb-122">有許多因素在壓縮過程中會影響資料的流失量，但一般而言，原始資料越複雜且壓縮率越高，在壓縮過程中就會流失更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="a6dcb-123">有三種類型的 VBR 編碼：品質型、無限制且受限。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="a6dcb-124">以品質為基礎的 VBR 編碼</span><span class="sxs-lookup"><span data-stu-id="a6dcb-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="a6dcb-125">第一種類型的 VBR 編碼是以品質為基礎，它使用一種編碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="a6dcb-126">以品質為基礎的 VBR 編碼可讓您指定數位媒體串流的品質層級，而不是位元速率。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="a6dcb-127">然後，編解碼器會將內容編碼，讓所有範例都具有相當的品質。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="a6dcb-128">以品質為基礎之 VBR 編碼的主要優點是，檔案中和從一個檔案到下一個檔案的品質都是一致的。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="a6dcb-129">例如，您可以撰寫一個程式，從 CD 將歌曲複製到電腦上的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="a6dcb-130">在此情況下，一致的品質對終端使用者體驗而言可能比一致的檔案大小更重要。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="a6dcb-131">使用以品質為基礎的 VBR 編碼，可確保複製的所有歌曲都具有相同的品質。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="a6dcb-132">以品質為基礎之 VBR 編碼的缺點是，在編碼之前，沒有辦法知道編碼媒體的大小或頻寬需求。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="a6dcb-133">這可以讓以品質為基礎的 VBR 編碼檔案不適用於記憶體或頻寬受限的情況，例如便攜媒體播放機或低頻寬的網際網路連線。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="a6dcb-134">一般而言，以品質為基礎的 VBR 編碼非常適合本機播放或高頻寬的網路連接。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="a6dcb-135">在這些情況下，一致的品質將提供更好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="a6dcb-136">未受限制的 VBR 編碼</span><span class="sxs-lookup"><span data-stu-id="a6dcb-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="a6dcb-137">未受限制的 VBR 編碼會使用兩種編碼階段。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="a6dcb-138">使用不受限制的 VBR 編碼時，您可以指定資料流程的位元速率，如同使用 CBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="a6dcb-139">不過，編解碼器只會使用此值做為資料流程的平均位元速率，並進行編碼，讓品質盡可能高，同時維持平均。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="a6dcb-140">編碼資料流程中任何時間點的實際位元速率可能會有極大的差異。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="a6dcb-141">您未針對未受限制的 VBR 編碼設定緩衝區視窗，就像是針對 CBR 編碼的資料流程一樣。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="a6dcb-142">相反地，編解碼器會根據編碼範例的需求來計算所需緩衝區視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="a6dcb-143">未受限制的 VBR 編碼的優點在於壓縮的資料流程具有最高的可能品質，同時維持在可預測的平均頻寬內。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="a6dcb-144">受限的 VBR 編碼</span><span class="sxs-lookup"><span data-stu-id="a6dcb-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="a6dcb-145">受限制的 VBR 編碼與未受限制的 VBR 編碼相同，不同之處在于您會在設定檔中指定最大位元速率和最大緩衝區視窗。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="a6dcb-146">然後，編解碼器會使用最大值來決定壓縮資料的方式。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="a6dcb-147">如果設定的最大值夠高，則受限制的 VBR 編碼將會產生與未受限制的 VBR 編碼相同的編碼資料流程。</span><span class="sxs-lookup"><span data-stu-id="a6dcb-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6dcb-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6dcb-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6dcb-149">**選擇編碼方法**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="a6dcb-150">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="a6dcb-151">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="a6dcb-152">**設定 VBR 資料流程**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="a6dcb-153">**固定位元速率 (CBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="a6dcb-154">**雙通路編碼**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="a6dcb-155">**使用 Two-Pass 編碼**</span><span class="sxs-lookup"><span data-stu-id="a6dcb-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




