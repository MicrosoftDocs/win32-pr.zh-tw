---
description: Windows Media 音訊和影片編解碼器是物件的集合，可用來壓縮和解壓縮數位媒體資料。
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Windows Media 轉碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998949"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="23269-103">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="23269-103">Windows Media Codecs</span></span>

<span data-ttu-id="23269-104">Windows Media 音訊和影片編解碼器是物件的集合，可用來壓縮和解壓縮數位媒體資料。</span><span class="sxs-lookup"><span data-stu-id="23269-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="23269-105">每個編解碼器都是由兩個物件所組成：編碼器和一個解碼器。</span><span class="sxs-lookup"><span data-stu-id="23269-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="23269-106">檔的這個部分會說明如何使用 Windows Media 音訊和影片編解碼器的功能來產生和取用壓縮的資料流程。</span><span class="sxs-lookup"><span data-stu-id="23269-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="23269-107">本檔主要適用于想要在以 c + + 為基礎的媒體應用程式中使用 Windows Media 編解碼器的開發人員。</span><span class="sxs-lookup"><span data-stu-id="23269-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="23269-108">如需 Windows Media 編解碼器功能的技術總覽，請參閱 [關於 Windows Media 編解碼器](about-the-windows-media-codecs.md)。</span><span class="sxs-lookup"><span data-stu-id="23269-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="23269-109">「 *編解碼器* 」一詞是「壓縮程式」和「解壓縮程式」一詞的獨有。</span><span class="sxs-lookup"><span data-stu-id="23269-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="23269-110">編解碼器通常會實作為一對 COM 物件：一個用於編碼內容，另一個用於解碼內容。</span><span class="sxs-lookup"><span data-stu-id="23269-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="23269-111">在某些情況下，COM 物件會佔用相同的動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="23269-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="23269-112">每個編解碼器物件都會執行兩個不同但類似的介面：</span><span class="sxs-lookup"><span data-stu-id="23269-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="23269-113">介面</span><span class="sxs-lookup"><span data-stu-id="23269-113">Interface</span></span>                              | <span data-ttu-id="23269-114">描述</span><span class="sxs-lookup"><span data-stu-id="23269-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="23269-115">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="23269-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="23269-116">與 Microsoft 媒體基礎相容。</span><span class="sxs-lookup"><span data-stu-id="23269-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="23269-117">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="23269-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="23269-118">與 DirectShow 相容。</span><span class="sxs-lookup"><span data-stu-id="23269-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="23269-119">音訊和影片不僅有不同的編解碼器，也有不同的編解碼器可用於不同類型的內容，您可能想要將它放入音訊或影片檔案中。</span><span class="sxs-lookup"><span data-stu-id="23269-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="23269-120">用來壓縮和解壓縮單字資料的演算法，與用來壓縮和解壓縮音樂資料的演算法不同。</span><span class="sxs-lookup"><span data-stu-id="23269-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="23269-121">編解碼器描述</span><span class="sxs-lookup"><span data-stu-id="23269-121">Codec Descriptions</span></span>

<span data-ttu-id="23269-122">下表說明 Windows Media 編解碼器的用途。</span><span class="sxs-lookup"><span data-stu-id="23269-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="23269-123">轉碼器</span><span class="sxs-lookup"><span data-stu-id="23269-123">Codec</span></span>                                                                     | <span data-ttu-id="23269-124">Description</span><span class="sxs-lookup"><span data-stu-id="23269-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23269-125">Windows Media 音訊</span><span class="sxs-lookup"><span data-stu-id="23269-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="23269-126">支援三種編碼內容類別別的音訊編解碼器： Standard、Professional 和無損。</span><span class="sxs-lookup"><span data-stu-id="23269-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="23269-127">Windows Media 音訊語音</span><span class="sxs-lookup"><span data-stu-id="23269-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="23269-128">針對以高壓縮率編碼人類聲音而優化的音訊編解碼器。</span><span class="sxs-lookup"><span data-stu-id="23269-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="23269-129">這是最常用於串流的串流編解碼器。</span><span class="sxs-lookup"><span data-stu-id="23269-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="23269-130">針對混合音樂和語音的內容，此編解碼器可以動態變更所使用的編碼演算法，以獲得最佳品質。</span><span class="sxs-lookup"><span data-stu-id="23269-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="23269-131">Windows Media 視訊9</span><span class="sxs-lookup"><span data-stu-id="23269-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="23269-132">支援四種編碼內容類別別的影片編解碼器：簡單設定檔、主要設定檔、Advanced Profile 和 Image。</span><span class="sxs-lookup"><span data-stu-id="23269-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="23269-133">Windows Media 視訊9螢幕</span><span class="sxs-lookup"><span data-stu-id="23269-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="23269-134">針對從電腦監視器編碼順序螢幕擷取畫面優化的影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="23269-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="23269-135">此編解碼器通常用於軟體訓練或支援，方法是在使用電腦應用程式時錄製監視器映射。</span><span class="sxs-lookup"><span data-stu-id="23269-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="23269-136">最新版本的編解碼器物件也可以存取某些舊版編解碼器，包括 Windows Media 視訊7和8、Windows Media Screen 7、較舊的 Microsoft MPEG-2 編解碼器，以及 Microsoft ISO MPEG-2 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="23269-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="23269-137">本檔未涵蓋這些舊版編解碼器;它僅涵蓋目前版本的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="23269-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="23269-138">針對較舊的編解碼器，請使用與使用目前編解碼器時相同的程式;不過，請記住，並非所有編解碼器都支援所有的功能。</span><span class="sxs-lookup"><span data-stu-id="23269-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="23269-139">本節內容</span><span class="sxs-lookup"><span data-stu-id="23269-139">In this section</span></span>

-   [<span data-ttu-id="23269-140">關於 Windows Media 編解碼器</span><span class="sxs-lookup"><span data-stu-id="23269-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="23269-141">使用編解碼器和 DSP 物件</span><span class="sxs-lookup"><span data-stu-id="23269-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="23269-142">編碼方法</span><span class="sxs-lookup"><span data-stu-id="23269-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="23269-143">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="23269-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="23269-144">有漏洞 Bucket 緩衝區模型</span><span class="sxs-lookup"><span data-stu-id="23269-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="23269-145">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="23269-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="23269-146">使用編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="23269-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="23269-147">使用音訊</span><span class="sxs-lookup"><span data-stu-id="23269-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="23269-148">使用影片</span><span class="sxs-lookup"><span data-stu-id="23269-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="23269-149">將壓縮的媒體儲存在 AVI 檔案中</span><span class="sxs-lookup"><span data-stu-id="23269-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="23269-150">使用 VBR 編碼</span><span class="sxs-lookup"><span data-stu-id="23269-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="23269-151">使用 Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="23269-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="23269-152">取得編碼統計資料</span><span class="sxs-lookup"><span data-stu-id="23269-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="23269-153">使用資料單位延伸模組</span><span class="sxs-lookup"><span data-stu-id="23269-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="23269-154">編解碼器和 DSP IPropertyBag 常數</span><span class="sxs-lookup"><span data-stu-id="23269-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="23269-155">目錄剖析器</span><span class="sxs-lookup"><span data-stu-id="23269-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="23269-156">Windows Media 編解碼器常見問題</span><span class="sxs-lookup"><span data-stu-id="23269-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="23269-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="23269-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23269-158">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="23269-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="23269-159">[適用于 Windows 的媒體技術](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="23269-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
