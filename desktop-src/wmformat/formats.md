---
title: 格式
description: 格式
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- Windows Media Format SDK，輸入
- Windows Media Format SDK，資料流程
- Windows Media Format SDK，輸出
- Windows Media 格式 SDK，格式
- Advanced Systems Format (ASF) 、輸入
- ASF (Advanced Systems Format) ，輸入
- Advanced Systems Format (ASF) 、串流
- ASF (Advanced Systems Format) ，資料流程
- Advanced Systems Format (ASF) 、輸出
- ASF (Advanced Systems Format) ，輸出
- Advanced Systems Format (ASF) 、格式
- ASF (Advanced Systems Format) ，格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301623"
---
# <a name="formats"></a><span data-ttu-id="d38bd-115">格式</span><span class="sxs-lookup"><span data-stu-id="d38bd-115">Formats</span></span>

<span data-ttu-id="d38bd-116">格式的資訊描述特定媒體類型的所有須知事項。</span><span class="sxs-lookup"><span data-stu-id="d38bd-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="d38bd-117">每種格式都有一種主要類型，例如音訊或影片，而且可能有子類型。</span><span class="sxs-lookup"><span data-stu-id="d38bd-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="d38bd-118">格式包含以主要類型為基礎的不同資訊。</span><span class="sxs-lookup"><span data-stu-id="d38bd-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="d38bd-119">音訊和影片格式需要比其他類型更多的資訊。</span><span class="sxs-lookup"><span data-stu-id="d38bd-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="d38bd-120">就像 Windows Media 格式 SDK 的物件會區分輸入數位、串流號碼和輸出編號 (查看輸入 [、串流和](inputs-streams-and-outputs.md) 輸出) ，輸入格式、串流格式和輸出格式之間有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="d38bd-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="d38bd-121">以下說明這些差異：</span><span class="sxs-lookup"><span data-stu-id="d38bd-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="d38bd-122">輸入格式</span><span class="sxs-lookup"><span data-stu-id="d38bd-122">Input Formats</span></span>

<span data-ttu-id="d38bd-123">輸入格式描述您傳遞至寫入器物件的數位媒體。</span><span class="sxs-lookup"><span data-stu-id="d38bd-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="d38bd-124">如果 ASF 檔案中的串流以編解碼器壓縮，則編解碼器只會支援特定的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="d38bd-125">當您使用 Windows Media 音訊和影片編解碼器時，可以使用寫入器物件來列舉支援的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="d38bd-126">寫入檔案時，您必須負責選取符合輸入媒體的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="d38bd-127">雖然可壓縮資料的編解碼器必須支援輸入媒體格式，但有些輸入格式設定不需要符合資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="d38bd-128">例如，影片資料流程的輸入格式可能會有不同于資料流程格式所定義的框架大小。</span><span class="sxs-lookup"><span data-stu-id="d38bd-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="d38bd-129">編解碼器會在這些情況下執行轉換。</span><span class="sxs-lookup"><span data-stu-id="d38bd-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="d38bd-130">資料流程格式</span><span class="sxs-lookup"><span data-stu-id="d38bd-130">Stream Formats</span></span>

<span data-ttu-id="d38bd-131">資料流程格式描述儲存在 ASF 檔案中的媒體格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="d38bd-132">資料流程格式是設定檔中所描述的格式，而且不一定是輸入格式和輸出格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="d38bd-133">如果使用編解碼器壓縮資料流程中的資料，資料流程格式將會與輸入和輸出格式不同。</span><span class="sxs-lookup"><span data-stu-id="d38bd-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="d38bd-134">使用 Windows Media 音訊和影片編解碼器時，您必須從編解碼器取得支援的串流格式清單，以確保您不會嘗試指定程式碼不支援的格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="d38bd-135">您必須在抓取編解碼器格式之後，手動設定某些格式設定，例如影片框架的大小和色彩深度。</span><span class="sxs-lookup"><span data-stu-id="d38bd-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="d38bd-136">輸出格式</span><span class="sxs-lookup"><span data-stu-id="d38bd-136">Output Formats</span></span>

<span data-ttu-id="d38bd-137">輸出格式描述讀取器 (或同步讀取器) 傳遞至您應用程式的數位媒體。</span><span class="sxs-lookup"><span data-stu-id="d38bd-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="d38bd-138">如果 ASF 檔案中的串流以編解碼器壓縮，則編解碼器只會支援特定的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="d38bd-139">當您使用 Windows Media 音訊和影片編解碼器時，可以使用 reader 物件來列舉支援的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="d38bd-140">每個 Windows Media 編解碼器都有預設輸出格式，但您可以選取任何支援的輸出格式來傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="d38bd-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="d38bd-141">雖然壓縮資料的編解碼器必須支援輸出媒體格式，但某些輸出格式設定不需要符合資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="d38bd-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="d38bd-142">例如，影片資料流程的輸出格式可能會有不同于資料流程格式所定義的框架大小。</span><span class="sxs-lookup"><span data-stu-id="d38bd-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="d38bd-143">編解碼器會在這些情況下執行轉換。</span><span class="sxs-lookup"><span data-stu-id="d38bd-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d38bd-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="d38bd-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d38bd-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="d38bd-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




