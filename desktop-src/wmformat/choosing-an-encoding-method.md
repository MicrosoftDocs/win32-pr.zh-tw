---
title: 選擇編碼方法
description: 選擇編碼方法
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- 設定檔，選擇編碼方法
- 設定檔，編碼方法
- 編解碼器，選擇編碼方法
- 編解碼器，編碼方法
- 設定檔，選取編碼方法
- 編解碼器，選取編碼方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969850"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="8bf1a-109">選擇編碼方法</span><span class="sxs-lookup"><span data-stu-id="8bf1a-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="8bf1a-110">某些編解碼器（例如 Windows Media 視訊9編解碼器）支援多種編碼方法。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="8bf1a-111">您為數據流選擇的編碼方法將取決於資料流程的傳遞方式。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="8bf1a-112">下表說明使用各種編碼方法的時機。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="8bf1a-113">編碼方法</span><span class="sxs-lookup"><span data-stu-id="8bf1a-113">Encoding method</span></span>                | <span data-ttu-id="8bf1a-114">Description</span><span class="sxs-lookup"><span data-stu-id="8bf1a-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf1a-115">1-傳遞常數的位速率 (CBR) </span><span class="sxs-lookup"><span data-stu-id="8bf1a-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="8bf1a-116">即時串流的唯一選項。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-116">The only option for live streaming.</span></span> <span data-ttu-id="8bf1a-117">編碼為可預測的位元速率，並提供所有編碼方法的最低品質。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="8bf1a-118">2-通過 CBR</span><span class="sxs-lookup"><span data-stu-id="8bf1a-118">2-pass CBR</span></span>                     | <span data-ttu-id="8bf1a-119">針對將透過網路串流至用戶端讀取器，但不是從即時來源進行廣播的檔案使用。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="8bf1a-120">編碼為可預測的位元速率，但品質優於 1-通過 CBR。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="8bf1a-121">1-傳遞變數位元速率 (VBR) </span><span class="sxs-lookup"><span data-stu-id="8bf1a-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="8bf1a-122">當您需要指定編碼輸出的品質時，請使用。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="8bf1a-123">提供所有編碼方法的最一致品質。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="8bf1a-124">僅適用于本機檔案或供下載之用。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="8bf1a-125">2-通過 VBR –未受限制</span><span class="sxs-lookup"><span data-stu-id="8bf1a-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="8bf1a-126">當您需要指定頻寬，但可接受指定頻寬周圍的波動時，請使用。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="8bf1a-127">本機檔案或僅限下載。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="8bf1a-128">2-通過 VBR –受限制</span><span class="sxs-lookup"><span data-stu-id="8bf1a-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="8bf1a-129">在與未受限制的情況下使用相同的情況下，但您必須指定最大的暫時位元速率。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="8bf1a-130">本機檔案或僅限下載。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="8bf1a-131">下表列出 Windows Media Format SDK 隨附的編解碼器所支援的編碼方法。</span><span class="sxs-lookup"><span data-stu-id="8bf1a-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="8bf1a-132">轉碼器</span><span class="sxs-lookup"><span data-stu-id="8bf1a-132">Codec</span></span>                                  | <span data-ttu-id="8bf1a-133">Cbr</span><span class="sxs-lookup"><span data-stu-id="8bf1a-133">CBR</span></span> | <span data-ttu-id="8bf1a-134">2-通過 CBR</span><span class="sxs-lookup"><span data-stu-id="8bf1a-134">2-pass CBR</span></span> | <span data-ttu-id="8bf1a-135">Vbr</span><span class="sxs-lookup"><span data-stu-id="8bf1a-135">VBR</span></span> | <span data-ttu-id="8bf1a-136">2-通過 VBR</span><span class="sxs-lookup"><span data-stu-id="8bf1a-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="8bf1a-137">Windows Media 視訊9</span><span class="sxs-lookup"><span data-stu-id="8bf1a-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="8bf1a-138">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-138">X</span></span>   | <span data-ttu-id="8bf1a-139">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-139">X</span></span>          | <span data-ttu-id="8bf1a-140">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-140">X</span></span>   | <span data-ttu-id="8bf1a-141">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-141">X</span></span>          |
| <span data-ttu-id="8bf1a-142">Windows Media 音訊9和更新版本</span><span class="sxs-lookup"><span data-stu-id="8bf1a-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="8bf1a-143">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-143">X</span></span>   | <span data-ttu-id="8bf1a-144">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-144">X</span></span>          | <span data-ttu-id="8bf1a-145">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-145">X</span></span>   | <span data-ttu-id="8bf1a-146">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-146">X</span></span>          |
| <span data-ttu-id="8bf1a-147">Windows Media 視訊9螢幕</span><span class="sxs-lookup"><span data-stu-id="8bf1a-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="8bf1a-148">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-148">X</span></span>   |            | <span data-ttu-id="8bf1a-149">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-149">X</span></span>   |            |
| <span data-ttu-id="8bf1a-150">Windows Media 音訊9語音</span><span class="sxs-lookup"><span data-stu-id="8bf1a-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="8bf1a-151">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-151">X</span></span>   |            |     |            |
| <span data-ttu-id="8bf1a-152">Windows Media 音訊專業人員</span><span class="sxs-lookup"><span data-stu-id="8bf1a-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="8bf1a-153">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-153">X</span></span>   | <span data-ttu-id="8bf1a-154">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-154">X</span></span>          | <span data-ttu-id="8bf1a-155">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-155">X</span></span>   | <span data-ttu-id="8bf1a-156">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-156">X</span></span>          |
| <span data-ttu-id="8bf1a-157">Windows Media 音訊無損</span><span class="sxs-lookup"><span data-stu-id="8bf1a-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="8bf1a-158">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-158">X</span></span>   |            |
| <span data-ttu-id="8bf1a-159">Windows Media 視訊9映射和更新版本</span><span class="sxs-lookup"><span data-stu-id="8bf1a-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="8bf1a-160">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-160">X</span></span>   |            | <span data-ttu-id="8bf1a-161">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-161">X</span></span>   |            |
| <span data-ttu-id="8bf1a-162">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="8bf1a-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="8bf1a-163">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-163">X</span></span>   | <span data-ttu-id="8bf1a-164">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-164">X</span></span>          | <span data-ttu-id="8bf1a-165">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-165">X</span></span>   | <span data-ttu-id="8bf1a-166">X</span><span class="sxs-lookup"><span data-stu-id="8bf1a-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="8bf1a-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="8bf1a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf1a-168">**設計設定檔**</span><span class="sxs-lookup"><span data-stu-id="8bf1a-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="8bf1a-169">**固定位元速率 (CBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="8bf1a-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="8bf1a-170">**雙通路編碼**</span><span class="sxs-lookup"><span data-stu-id="8bf1a-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="8bf1a-171">**變數位速率 (VBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="8bf1a-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




