---
title: 輸入、串流和輸出
description: 輸入、串流和輸出
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- Windows Media Format SDK，輸入
- Windows Media Format SDK，資料流程
- Windows Media Format SDK，輸出
- Advanced Systems Format (ASF) 、輸入
- ASF (Advanced Systems Format) ，輸入
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- Advanced Systems Format (ASF) 、輸出
- ASF (Advanced Systems Format) ，輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e6b6941a990b108c16b49648ec0d8d028a44d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965811"
---
# <a name="inputs-streams-and-outputs"></a><span data-ttu-id="c586c-112">輸入、串流和輸出</span><span class="sxs-lookup"><span data-stu-id="c586c-112">Inputs, Streams, and Outputs</span></span>

<span data-ttu-id="c586c-113">本檔中的「輸入」是任何數位媒體資料流程 (例如音訊或影片) ，您的應用程式會使用適當的 Api，從來源將其傳遞至寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="c586c-113">An "input" in this documentation is any digital media data stream (such as audio or video) that your application delivers to the writer object from a source by using appropriate APIs.</span></span> <span data-ttu-id="c586c-114">輸入必須以支援的格式傳遞。</span><span class="sxs-lookup"><span data-stu-id="c586c-114">Inputs must be delivered in a supported format.</span></span> <span data-ttu-id="c586c-115">支援數種標準 RGB 和 YUV 格式作為輸入，而音訊編解碼器支援 PCM。</span><span class="sxs-lookup"><span data-stu-id="c586c-115">Several standard RGB and YUV formats are supported as input, and the audio codecs support PCM.</span></span> <span data-ttu-id="c586c-116">如果編解碼器原生不支援指定的輸入格式，寫入器物件將會具現化能夠將各種格式轉換成編解碼器可接受之格式的音訊或影片協助程式物件。</span><span class="sxs-lookup"><span data-stu-id="c586c-116">If a specified input format is not supported natively by the codec, the writer object will instantiate either an audio or video helper object that is capable of converting a wide variety of formats into formats the codec can accept.</span></span> <span data-ttu-id="c586c-117">若為音訊輸入，helper 物件將會視需要調整位元速率、取樣率和通道數目。</span><span class="sxs-lookup"><span data-stu-id="c586c-117">For audio inputs, the helper object will adjust the bit depth, sample rate, and number of channels as necessary.</span></span> <span data-ttu-id="c586c-118">針對影片輸入，影片協助程式物件會執行色彩空間轉換和矩形大小調整。</span><span class="sxs-lookup"><span data-stu-id="c586c-118">For video inputs, the video helper object will perform color-space conversions and rectangle-size adjustments.</span></span> <span data-ttu-id="c586c-119">在某些情況下，可以在輸入資料流程中傳遞壓縮的音訊和影片資料。</span><span class="sxs-lookup"><span data-stu-id="c586c-119">In some cases, compressed audio and video data can be passed in an input stream.</span></span> <span data-ttu-id="c586c-120">輸入可能是除了音訊和影片以外的其他媒體類型，例如文字、指令碼命令、靜止影像或任意檔案資料。</span><span class="sxs-lookup"><span data-stu-id="c586c-120">An input may be of some other media type besides audio and video, such as text, script commands, still images, or arbitrary file data.</span></span>

<span data-ttu-id="c586c-121">本檔中的「輸出」是指讀取器物件傳遞給應用程式進行轉譯的資料。</span><span class="sxs-lookup"><span data-stu-id="c586c-121">An "output" in this documentation refers to data that the reader object passes to an application for rendering.</span></span> <span data-ttu-id="c586c-122">輸出會等於播放時的單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="c586c-122">An output equates to a single stream at the time of playback.</span></span> <span data-ttu-id="c586c-123">如果您使用相互排除，則所有互斥資料流程都會共用單一輸出。</span><span class="sxs-lookup"><span data-stu-id="c586c-123">If you are using mutual exclusion, all of the mutually exclusive streams share a single output.</span></span> <span data-ttu-id="c586c-124">輸出資料通常會以未壓縮的音訊或影片資料的形式呈現，雖然它可以包含任何類型的資料。</span><span class="sxs-lookup"><span data-stu-id="c586c-124">Typically, output data is in the form of uncompressed audio or video data, although it can contain any type of data.</span></span> <span data-ttu-id="c586c-125">本檔的其他位置會列出支援的影片輸出格式。</span><span class="sxs-lookup"><span data-stu-id="c586c-125">Supported video output formats are listed elsewhere in this documentation.</span></span>

<span data-ttu-id="c586c-126">本檔中的「資料流程」一詞是指 ASF 檔中的資料，而不是在寫入器物件處理之前， (1) 輸入來源資料，並在讀取器物件解壓縮輸出資料後， (2) 輸出資料。</span><span class="sxs-lookup"><span data-stu-id="c586c-126">The term "stream" in this documentation refers to data in an ASF file, as opposed to (1) the input source data before it is processed by the writer object, and (2) the output data after it is decompressed by the reader object.</span></span> <span data-ttu-id="c586c-127">ASF 資料流程所包含的資料是來自寫入器物件上的單一輸入，雖然可以從相同的輸入建立一個以上的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c586c-127">An ASF stream contains data that comes from a single input on the writer object, although more than one stream can be created from the same input.</span></span> <span data-ttu-id="c586c-128">資料流程的格式和壓縮設定從開始到結尾。</span><span class="sxs-lookup"><span data-stu-id="c586c-128">A stream has the same format and compression settings from beginning to end.</span></span> <span data-ttu-id="c586c-129">簡單的 ASF 檔案有兩個數據流，一個用於音訊，另一個用於影片。</span><span class="sxs-lookup"><span data-stu-id="c586c-129">A simple ASF file has two streams, one for audio and one for video.</span></span> <span data-ttu-id="c586c-130">較複雜的檔案可能會有兩個音訊串流和數個影片串流。</span><span class="sxs-lookup"><span data-stu-id="c586c-130">A more complex file might have two audio streams and several video streams.</span></span> <span data-ttu-id="c586c-131">音訊串流可能會有相同的壓縮設定，但包含不同的內容，例如不同語言的旁白。</span><span class="sxs-lookup"><span data-stu-id="c586c-131">The audio streams might have the same compression settings but contain different content, such as a narration in different languages.</span></span> <span data-ttu-id="c586c-132">影片串流可能包含相同的內容，但有不同的壓縮設定。</span><span class="sxs-lookup"><span data-stu-id="c586c-132">The video streams might contain the same content, but have different compression settings.</span></span> <span data-ttu-id="c586c-133">寫入器物件將套用至每個資料流程的媒體格式和壓縮設定會指定于設定檔中。</span><span class="sxs-lookup"><span data-stu-id="c586c-133">The media format and compression settings that the writer object will apply to each stream are specified in the profile.</span></span>

<span data-ttu-id="c586c-134">輸入、資料流程和輸出之間的關聯性可以有三種基本類型。</span><span class="sxs-lookup"><span data-stu-id="c586c-134">The relationship between inputs, streams, and outputs can be of three basic types.</span></span> <span data-ttu-id="c586c-135">下列三個圖表說明關聯性。</span><span class="sxs-lookup"><span data-stu-id="c586c-135">The following three diagrams illustrate the relationships.</span></span>

<span data-ttu-id="c586c-136">在最基本的關聯性中（不含任何互斥的設定檔），每個輸入都會由寫入器處理，並以單一資料流程的形式插入 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c586c-136">In the most basic relationship, which is a profile without any mutual exclusion, each input is processed by the writer and inserted in the ASF file as a single stream.</span></span> <span data-ttu-id="c586c-137">在播放時，讀取器會讀取資料流程並以單一輸出形式傳遞未壓縮的範例，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c586c-137">On playback, the reader reads the stream and delivers uncompressed samples as a single output, as shown in the following diagram.</span></span>

![顯示輸入、資料流程和輸出之間的一般關聯性的圖表。](images/formatsdk03.png)

<span data-ttu-id="c586c-139">使用多個位速率互斥時，會發生比較複雜的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c586c-139">A more complex relationship occurs when multiple bit rate mutual exclusion is used.</span></span> <span data-ttu-id="c586c-140">在此情況下，寫入器會處理單一輸入，並以數種位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="c586c-140">In this case, a single input is processed by the writer and encoded at several bit rates.</span></span> <span data-ttu-id="c586c-141">每個資料編碼都會以個別資料流程的形式插入 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c586c-141">Each encoding of the data is inserted in the ASF file as a separate stream.</span></span> <span data-ttu-id="c586c-142">在播放時，讀取器會根據可用的頻寬來決定要解壓縮的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c586c-142">On playback, the reader determines which stream to decompress based upon the available bandwidth.</span></span> <span data-ttu-id="c586c-143">讀取器接著會讀取選取的資料流程，並以單一輸出形式傳遞未壓縮的範例，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="c586c-143">The reader then reads the selected stream and delivers uncompressed samples as a single output, as shown in the following diagram.</span></span>

![此圖顯示使用多個位速率互斥時，輸入、資料流程和輸出之間的關聯性。](images/formatsdk04.png)

<span data-ttu-id="c586c-145">使用以語言為基礎或自訂的互斥時，可能會發生第三種類型的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c586c-145">The third type of relationship can occur when a language-based or custom mutual exclusion is used.</span></span> <span data-ttu-id="c586c-146">在此關聯性中，讀取器會處理多個輸入，而且每個輸入都會以個別資料流程的形式插入 ASF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c586c-146">In this relationship, multiple inputs are processed by the reader and each is inserted into the ASF file as an individual stream.</span></span> <span data-ttu-id="c586c-147">在播放時，您的應用程式會根據您提供的邏輯，以手動方式選取要解壓縮的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c586c-147">On playback, your application manually selects which stream to decompress based upon logic you provide.</span></span> <span data-ttu-id="c586c-148">讀取器接著會讀取選取的資料流程，並以單一輸出形式傳遞未壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="c586c-148">The reader then reads the selected stream and delivers uncompressed samples as a single output.</span></span> <span data-ttu-id="c586c-149">此程式可用於包含多種語言的 soundtracks。</span><span class="sxs-lookup"><span data-stu-id="c586c-149">This process can be used for including soundtracks in multiple languages.</span></span> <span data-ttu-id="c586c-150">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="c586c-150">The following diagram illustrates this process.</span></span>

![此圖顯示使用自訂相互排除時輸入、資料流程和輸出之間的關聯性。](images/formatsdk02.png)

<span data-ttu-id="c586c-152">先前所述的關聯性有一些變化。</span><span class="sxs-lookup"><span data-stu-id="c586c-152">There is some variation in the relationships described previously.</span></span> <span data-ttu-id="c586c-153">例如，檔案可以包含三個關聯性，或其中一個或兩個關聯性。</span><span class="sxs-lookup"><span data-stu-id="c586c-153">For example, a file can contain all three relationships, or one or two of them.</span></span> <span data-ttu-id="c586c-154">您也可以壓縮某些輸入，在這種情況下，寫入器不會執行額外的壓縮。</span><span class="sxs-lookup"><span data-stu-id="c586c-154">It is also possible for some inputs to be compressed, in which case the writer performs no additional compression.</span></span> <span data-ttu-id="c586c-155">讀者也可以傳遞壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="c586c-155">The reader, also, can deliver compressed samples.</span></span> <span data-ttu-id="c586c-156">但在此情況下，您必須依串流號碼存取它們，而不是依輸出編號來存取。</span><span class="sxs-lookup"><span data-stu-id="c586c-156">But when it does, you must access them by stream number, not by output number.</span></span>

> [!Note]  
> <span data-ttu-id="c586c-157">輸入、steams 和輸出都是由 Windows Media 格式 SDK 的物件所指派的數位。</span><span class="sxs-lookup"><span data-stu-id="c586c-157">Inputs, steams, and outputs are all assigned numbers by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="c586c-158">資料流程具有您在設定檔中定義的資料流程編號（以1為基礎）。</span><span class="sxs-lookup"><span data-stu-id="c586c-158">Streams have a stream number, which is 1-based, that you define in the profile.</span></span> <span data-ttu-id="c586c-159">每個資料流程也會被指派一個資料流程索引，以用於列舉設定檔中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="c586c-159">Each stream is also assigned a stream index for use in enumerating streams in a profile.</span></span> <span data-ttu-id="c586c-160">這些數位都不保證彼此一致。</span><span class="sxs-lookup"><span data-stu-id="c586c-160">None of these numbers are guaranteed to be consistent with each other.</span></span> <span data-ttu-id="c586c-161">也就是說，輸入編號1可能不會對應到資料流程編號1，資料流程編號1可能不會對應到資料流程索引1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="c586c-161">That is, input number 1 may not correspond with stream number 1, stream number 1 may not correspond with stream index 1, and so on.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c586c-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="c586c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c586c-163">**概念**</span><span class="sxs-lookup"><span data-stu-id="c586c-163">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="c586c-164">**互斥**</span><span class="sxs-lookup"><span data-stu-id="c586c-164">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> </dl>

 

 




