---
description: 如果您不熟悉數位媒體，本主題將介紹在撰寫媒體基礎的應用程式之前，您必須瞭解的一些概念。
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 媒體基礎：基本概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0298a20518df91dab4439770e0f1193802969ae8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104386316"
---
# <a name="media-foundation-essential-concepts"></a><span data-ttu-id="f75f8-103">媒體基礎：基本概念</span><span class="sxs-lookup"><span data-stu-id="f75f8-103">Media Foundation: Essential Concepts</span></span>

<span data-ttu-id="f75f8-104">如果您不熟悉數位媒體，本主題將介紹在撰寫媒體基礎的應用程式之前，您必須瞭解的一些概念。</span><span class="sxs-lookup"><span data-stu-id="f75f8-104">If you are new to digital media, this topic introduces some concepts that you will need to understand before writing a Media Foundation application.</span></span>

-   [<span data-ttu-id="f75f8-105">串流</span><span class="sxs-lookup"><span data-stu-id="f75f8-105">Streams</span></span>](#streams)
-   [<span data-ttu-id="f75f8-106">壓縮</span><span class="sxs-lookup"><span data-stu-id="f75f8-106">Compression</span></span>](#compression)
-   [<span data-ttu-id="f75f8-107">媒體容器</span><span class="sxs-lookup"><span data-stu-id="f75f8-107">Media Containers</span></span>](#media-containers)
-   [<span data-ttu-id="f75f8-108">格式</span><span class="sxs-lookup"><span data-stu-id="f75f8-108">Formats</span></span>](#formats)
-   [<span data-ttu-id="f75f8-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f75f8-109">Related topics</span></span>](#related-topics)

## <a name="streams"></a><span data-ttu-id="f75f8-110">串流</span><span class="sxs-lookup"><span data-stu-id="f75f8-110">Streams</span></span>

<span data-ttu-id="f75f8-111">*資料流程* 是一種具有統一類型的媒體資料序列。</span><span class="sxs-lookup"><span data-stu-id="f75f8-111">A *stream* is a sequence of media data with a uniform type.</span></span> <span data-ttu-id="f75f8-112">最常見的類型是音訊和影片，但是資料流程幾乎可以包含任何類型的資料，包括文字、指令碼命令和靜止影像。</span><span class="sxs-lookup"><span data-stu-id="f75f8-112">The most common types are audio and video, but a stream can contain almost any kind of data, including text, script commands, and still images.</span></span> <span data-ttu-id="f75f8-113">本檔中的「 *資料流程* 」一詞不表示透過網路傳遞。</span><span class="sxs-lookup"><span data-stu-id="f75f8-113">The term *stream* in this documentation does not imply delivery over a network.</span></span> <span data-ttu-id="f75f8-114">適用于本機播放的媒體檔案也包含資料流程。</span><span class="sxs-lookup"><span data-stu-id="f75f8-114">A media file intended for local playback also contains streams.</span></span>

<span data-ttu-id="f75f8-115">媒體檔案通常會包含單一音訊串流，或只包含一個影片串流和一個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="f75f8-115">Usually, a media file contains either a single audio stream, or exactly one video stream and one audio stream.</span></span> <span data-ttu-id="f75f8-116">不過，媒體檔案可能包含多個相同類型的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f75f8-116">However, a media file might contain several streams of the same type.</span></span> <span data-ttu-id="f75f8-117">例如，影片檔案可能包含數種不同語言的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="f75f8-117">For example, a video file might contain audio streams in several different languages.</span></span> <span data-ttu-id="f75f8-118">應用程式會在執行時間選取要使用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="f75f8-118">At run time, the application would select which stream to use.</span></span>

## <a name="compression"></a><span data-ttu-id="f75f8-119">壓縮</span><span class="sxs-lookup"><span data-stu-id="f75f8-119">Compression</span></span>

<span data-ttu-id="f75f8-120">「*壓縮*」指的是藉由移除多餘的資訊，來減少資料流程大小的任何處理程式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-120">*Compression* refers to any process that reduces the size of a data stream by removing redundant information.</span></span> <span data-ttu-id="f75f8-121">壓縮演算法分為兩大類：</span><span class="sxs-lookup"><span data-stu-id="f75f8-121">Compression algorithms fall into two broad categories:</span></span>

-   <span data-ttu-id="f75f8-122">無 *失真壓縮。*</span><span class="sxs-lookup"><span data-stu-id="f75f8-122">*Lossless* compression.</span></span> <span data-ttu-id="f75f8-123">使用無失真演算法時，重建的資料與原始資料相同。</span><span class="sxs-lookup"><span data-stu-id="f75f8-123">Using a lossless algorithm, the reconstructed data is identical to the original.</span></span>
-   <span data-ttu-id="f75f8-124">*損* 及壓縮。</span><span class="sxs-lookup"><span data-stu-id="f75f8-124">*Lossy* compression.</span></span> <span data-ttu-id="f75f8-125">使用失真演算法時，重建資料是原始的近似值，但不完全相符。</span><span class="sxs-lookup"><span data-stu-id="f75f8-125">Using a lossy algorithm, the reconstructed data is an approximation of the original, but is not an exact match.</span></span>

<span data-ttu-id="f75f8-126">在大部分的其他網域中，無法接受失真的壓縮。</span><span class="sxs-lookup"><span data-stu-id="f75f8-126">In most other domains, lossy compression is not acceptable.</span></span> <span data-ttu-id="f75f8-127"> (想像得到試算表的「近似值」！ ) 但因為有幾個原因，所以失真的壓縮配置非常適合音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="f75f8-127">(Imagine getting back an "approximation" of a spreadsheet!) But lossy compression schemes are well-suited to audio and video, for a couple of reasons.</span></span>

<span data-ttu-id="f75f8-128">第一個原因是人們認知的物理。</span><span class="sxs-lookup"><span data-stu-id="f75f8-128">The first reason has to do with the physics of human perception.</span></span> <span data-ttu-id="f75f8-129">當我們聆聽很複雜的音效（像是音樂錄音）時，該音效所包含的部分資訊不會可察覺到 ear 中。</span><span class="sxs-lookup"><span data-stu-id="f75f8-129">When we listen to a complex sound, like a music recording, some of the information contained in that sound is not perceptible to the ear.</span></span> <span data-ttu-id="f75f8-130">有了信號處理理論的協助，就可以分析和分隔無法察覺的頻率。</span><span class="sxs-lookup"><span data-stu-id="f75f8-130">With the help of signal processing theory, it is possible to analyze and separate the frequencies that cannot be perceived.</span></span> <span data-ttu-id="f75f8-131">這些頻率可以移除，而不會有任何感知效果。</span><span class="sxs-lookup"><span data-stu-id="f75f8-131">These frequencies can be removed with no perceptual effect.</span></span> <span data-ttu-id="f75f8-132">雖然重建音訊不會完全符合原始音訊，但與接聽程式的 *音效* 相同。</span><span class="sxs-lookup"><span data-stu-id="f75f8-132">Although the reconstructed audio will not match the original exactly, it will *sound* the same to the listener.</span></span> <span data-ttu-id="f75f8-133">類似的原則適用于影片。</span><span class="sxs-lookup"><span data-stu-id="f75f8-133">Similar principles apply to video.</span></span>

<span data-ttu-id="f75f8-134">其次，可能可接受某些音效或影像品質降低的情況，視用途而定。</span><span class="sxs-lookup"><span data-stu-id="f75f8-134">Second, some degradation in sound or image quality may be acceptable, depending on the intended purpose.</span></span> <span data-ttu-id="f75f8-135">例如，在電話語音中，音訊通常會高度壓縮。</span><span class="sxs-lookup"><span data-stu-id="f75f8-135">In telephony, for example, audio is often highly compressed.</span></span> <span data-ttu-id="f75f8-136">結果對電話對話而言夠好，但您不想在電話上接聽 symphony 管弦樂團。</span><span class="sxs-lookup"><span data-stu-id="f75f8-136">The result is good enough for a phone conversation—but you wouldn't want to listen to a symphony orchestra over a telephone.</span></span>

<span data-ttu-id="f75f8-137">壓縮也稱為 *編碼方式*，而編碼的裝置稱為 *編碼器*。</span><span class="sxs-lookup"><span data-stu-id="f75f8-137">Compression is also called *encoding*, and a device that encodes is called an *encoder*.</span></span> <span data-ttu-id="f75f8-138">反向程式正在 *解碼*，而裝置則是自然稱為 *解碼器*。</span><span class="sxs-lookup"><span data-stu-id="f75f8-138">The reverse process is *decoding*, and the device is a naturally called a *decoder*.</span></span> <span data-ttu-id="f75f8-139">編碼器和解碼器的一般詞彙都是 *編解碼器*。</span><span class="sxs-lookup"><span data-stu-id="f75f8-139">The general term for both encoders and decoders is *codec*.</span></span> <span data-ttu-id="f75f8-140">編解碼器可在硬體或軟體中執行。</span><span class="sxs-lookup"><span data-stu-id="f75f8-140">Codecs can be implemented in hardware or software.</span></span>

<span data-ttu-id="f75f8-141">從數位媒體的出現以來，壓縮技術的變更很快，而且目前正在使用大量的壓縮配置。</span><span class="sxs-lookup"><span data-stu-id="f75f8-141">Compression technology has changed rapidly since the advent of digital media, and a large number of compression schemes are in use today.</span></span> <span data-ttu-id="f75f8-142">這是數位媒體程式設計的主要挑戰之一。</span><span class="sxs-lookup"><span data-stu-id="f75f8-142">This fact is one of the main challenges for digital media programming.</span></span>

## <a name="media-containers"></a><span data-ttu-id="f75f8-143">媒體容器</span><span class="sxs-lookup"><span data-stu-id="f75f8-143">Media Containers</span></span>

<span data-ttu-id="f75f8-144">很少會將原始音訊或影片串流儲存為電腦檔案，或直接透過網路傳送一次。</span><span class="sxs-lookup"><span data-stu-id="f75f8-144">It is rare to store a raw audio or video stream as a computer file, or to send one directly over the network.</span></span> <span data-ttu-id="f75f8-145">其中一件事是無法將這類串流解碼，而不需要事先知道要使用哪個編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f75f8-145">For one thing, it would be impossible to decode such a stream, without knowing in advance which codec to use.</span></span> <span data-ttu-id="f75f8-146">因此，媒體檔案通常至少包含下列其中一些元素：</span><span class="sxs-lookup"><span data-stu-id="f75f8-146">Therefore, media files usually contain at least some of the following elements:</span></span>

-   <span data-ttu-id="f75f8-147">描述資料流程數目、每個資料流程格式等的檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="f75f8-147">File headers that describe the number of streams, the format of each stream, and so on.</span></span>
-   <span data-ttu-id="f75f8-148">可隨機存取內容的索引。</span><span class="sxs-lookup"><span data-stu-id="f75f8-148">An index that enables random access to the content.</span></span>
-   <span data-ttu-id="f75f8-149">描述內容 (的中繼資料，例如演出者或標題) 。</span><span class="sxs-lookup"><span data-stu-id="f75f8-149">Metadata that describes the content (for example, the artist or title).</span></span>
-   <span data-ttu-id="f75f8-150">封包標頭，以啟用網路傳輸或隨機存取。</span><span class="sxs-lookup"><span data-stu-id="f75f8-150">Packet headers, to enable network transmission or random access.</span></span>

<span data-ttu-id="f75f8-151">本檔使用「 *容器* 」一詞來描述整個資料流程、標頭、索引、中繼資料等等的封裝。</span><span class="sxs-lookup"><span data-stu-id="f75f8-151">This documentation uses the term *container* to describe the entire package of streams, headers, indexes, metadata, and so forth.</span></span> <span data-ttu-id="f75f8-152">使用詞彙 *容器* （而非檔案）的 *原因是某些* 容器格式是針對即時廣播所設計。</span><span class="sxs-lookup"><span data-stu-id="f75f8-152">The reason for using the term *container* rather than *file* is that some container formats are designed for live broadcast.</span></span> <span data-ttu-id="f75f8-153">應用程式可能會即時產生容器，而永遠不會將它儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="f75f8-153">An application could generate the container in real time, never storing it to a file.</span></span>

<span data-ttu-id="f75f8-154">媒體容器的早期範例是 AVI 檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-154">An early example of a media container is the AVI file format.</span></span> <span data-ttu-id="f75f8-155">其他範例包括 [的] 和 [Advanced] 系統格式， (ASF) 。</span><span class="sxs-lookup"><span data-stu-id="f75f8-155">Other examples include MP4 and Advanced Systems Format (ASF).</span></span> <span data-ttu-id="f75f8-156">您可以使用副檔名來識別容器 (例如，將) 或 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="f75f8-156">Containers can be identified by file name extension (for example, .mp4) or by MIME type.</span></span>

<span data-ttu-id="f75f8-157">下圖顯示媒體容器的一般結構。</span><span class="sxs-lookup"><span data-stu-id="f75f8-157">The following diagram shows a typical structure for a media container.</span></span> <span data-ttu-id="f75f8-158">此圖表不代表任何特定的格式;每種格式的詳細資料會有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="f75f8-158">The diagram does not represent any specific format; the details of each format vary widely.</span></span>

![顯示一般媒體容器的圖表](images/concepts01.png)

<span data-ttu-id="f75f8-160">請注意，圖中顯示的結構是階層式的，且標頭資訊會出現在容器的開頭。</span><span class="sxs-lookup"><span data-stu-id="f75f8-160">Notice that the structure shown in the diagram is hierarchical, with header information appearing at the start of the container.</span></span> <span data-ttu-id="f75f8-161">此結構通常是許多 (，但並非所有) 容器格式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-161">This structure is typical of many (but not all) container formats.</span></span> <span data-ttu-id="f75f8-162">另外也請注意，data 區段包含交錯的音訊和影片封包。</span><span class="sxs-lookup"><span data-stu-id="f75f8-162">Also notice that the data section contains interleaved audio and video packets.</span></span> <span data-ttu-id="f75f8-163">這種交錯類型在媒體容器中很常見。</span><span class="sxs-lookup"><span data-stu-id="f75f8-163">This type of interleaving is common in media containers.</span></span>

<span data-ttu-id="f75f8-164">「 *多* 任務處理」一詞是指 packetizing 音訊和影片串流，然後將封包交錯至容器的程式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-164">The term *multiplexing* refers to the process of packetizing the audio and video streams and interleaving the packets into the container.</span></span> <span data-ttu-id="f75f8-165">從 packetized 資料目的地重組資料流程的反向處理常式稱為 *分離信號*。</span><span class="sxs-lookup"><span data-stu-id="f75f8-165">The reverse process, reassembling the streams from the packetized data, is called *demultiplexing*.</span></span>

## <a name="formats"></a><span data-ttu-id="f75f8-166">格式</span><span class="sxs-lookup"><span data-stu-id="f75f8-166">Formats</span></span>

<span data-ttu-id="f75f8-167">在數位媒體中，字詞 *格式* 不明確。</span><span class="sxs-lookup"><span data-stu-id="f75f8-167">In digital media, the term *format* is ambiguous.</span></span> <span data-ttu-id="f75f8-168">格式可以參考 *編碼* 類型，例如 h.264 影片或 *容器*（例如，「數量」）。</span><span class="sxs-lookup"><span data-stu-id="f75f8-168">A format can refer to the type of *encoding*, such as H.264 video, or the *container*, such as MP4.</span></span> <span data-ttu-id="f75f8-169">這項區別通常會讓一般使用者感到混淆。</span><span class="sxs-lookup"><span data-stu-id="f75f8-169">This distinction is often confusing for ordinary users.</span></span> <span data-ttu-id="f75f8-170">提供給媒體格式的名稱不一定會有説明。</span><span class="sxs-lookup"><span data-stu-id="f75f8-170">The names given to media formats do not always help.</span></span> <span data-ttu-id="f75f8-171">例如， *MP3* 指的是編碼格式 (Mpeg-2 音訊第 3) 和檔案格式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-171">For example, *MP3* refers both to an encoding format (MPEG-1 Audio Layer 3) and a file format.</span></span>

<span data-ttu-id="f75f8-172">差別是很重要的，因為讀取媒體檔案實際上牽涉到兩個階段：</span><span class="sxs-lookup"><span data-stu-id="f75f8-172">The distinction is important, however, because reading a media file actually involves two stages:</span></span>

1.  <span data-ttu-id="f75f8-173">首先，必須剖析容器。</span><span class="sxs-lookup"><span data-stu-id="f75f8-173">First, the container must be parsed.</span></span> <span data-ttu-id="f75f8-174">在大部分情況下，在此步驟完成之前，無法得知資料流程數目和每個資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-174">In most cases, the number of streams and the format of each stream cannot be known until this step is complete.</span></span>
2.  <span data-ttu-id="f75f8-175">接下來，如果資料流程已壓縮，則必須使用適當的解碼器將其解碼。</span><span class="sxs-lookup"><span data-stu-id="f75f8-175">Next, if the streams are compressed, they must be decoded using the appropriate decoders.</span></span>

<span data-ttu-id="f75f8-176">這種事實很自然地指向軟體設計，其中會使用不同的元件來剖析容器和解碼資料流程。</span><span class="sxs-lookup"><span data-stu-id="f75f8-176">This fact leads quite naturally to a software design where separate components are used to parse containers and decode streams.</span></span> <span data-ttu-id="f75f8-177">此外，此方法也適合用於外掛程式模型，讓協力廠商可以提供自己的剖析器和編解碼器。</span><span class="sxs-lookup"><span data-stu-id="f75f8-177">Further, this approach lends itself to a plug-in model, so that third parties can provide their own parsers and codecs.</span></span> <span data-ttu-id="f75f8-178">在 Windows 上，元件物件模型 (COM) 會提供一種標準方式來分隔 API 與其實作為任何外掛程式模型的需求。</span><span class="sxs-lookup"><span data-stu-id="f75f8-178">On Windows, the Component Object Model (COM) provides a standard way to separate an API from its implementation, which is a requirement for any plug-in model.</span></span> <span data-ttu-id="f75f8-179">基於這個理由， (其他) ，媒體基礎會使用 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="f75f8-179">For this reason (among others), Media Foundation uses COM interfaces.</span></span>

<span data-ttu-id="f75f8-180">下圖顯示用來讀取媒體檔案的元件：</span><span class="sxs-lookup"><span data-stu-id="f75f8-180">The following diagram shows the components used to read a media file:</span></span>

![顯示讀取媒體檔案元件的圖表](images/concepts02.png)

<span data-ttu-id="f75f8-182">寫入媒體檔案也需要兩個步驟：</span><span class="sxs-lookup"><span data-stu-id="f75f8-182">Writing a media file also requires two steps:</span></span>

1.  <span data-ttu-id="f75f8-183">編碼未壓縮的音訊/影片資料。</span><span class="sxs-lookup"><span data-stu-id="f75f8-183">Encoding the uncompressed audio/video data.</span></span>
2.  <span data-ttu-id="f75f8-184">將壓縮的資料放入特定的容器格式。</span><span class="sxs-lookup"><span data-stu-id="f75f8-184">Putting the compressed data into a particular container format.</span></span>

<span data-ttu-id="f75f8-185">下圖顯示用來寫入媒體檔案的元件：</span><span class="sxs-lookup"><span data-stu-id="f75f8-185">The following diagram shows the components used to write a media file:</span></span>

![此圖顯示寫入媒體檔案的元件。](images/concepts03.png)

## <a name="related-topics"></a><span data-ttu-id="f75f8-187">相關主題</span><span class="sxs-lookup"><span data-stu-id="f75f8-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f75f8-188">媒體基礎程式設計指南</span><span class="sxs-lookup"><span data-stu-id="f75f8-188">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



