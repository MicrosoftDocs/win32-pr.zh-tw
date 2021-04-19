---
description: 本總覽說明 (RIFF) 的資源交換檔案格式，該格式會在 .wav 檔案中使用。 RIFF 是 XAudio2 將載入音訊資料的一般格式。
ms.assetid: b543e949-223c-ddd3-7527-a41f3709a0c1
title: 資源交換檔案格式 (RIFF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d61eb45eff8db119eb73209b53b595f1cf6d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978182"
---
# <a name="resource-interchange-file-format-riff"></a><span data-ttu-id="4adc3-104">資源交換檔案格式 (RIFF)</span><span class="sxs-lookup"><span data-stu-id="4adc3-104">Resource Interchange File Format (RIFF)</span></span>

<span data-ttu-id="4adc3-105">本總覽說明 (RIFF) 的資源交換檔案格式，該格式會在 .wav 檔案中使用。</span><span class="sxs-lookup"><span data-stu-id="4adc3-105">This overview describes the Resource Interchange File Format (RIFF), which is used in .wav files.</span></span> <span data-ttu-id="4adc3-106">RIFF 是 XAudio2 將載入音訊資料的一般格式。</span><span class="sxs-lookup"><span data-stu-id="4adc3-106">RIFF is the typical format from which audio data for XAudio2 will be loaded.</span></span>

## <a name="riff"></a><span data-ttu-id="4adc3-107">RIFF</span><span class="sxs-lookup"><span data-stu-id="4adc3-107">RIFF</span></span>

<span data-ttu-id="4adc3-108">RIFF 檔案是由多個分隔資料區段（稱為 *區塊*）所組成。</span><span class="sxs-lookup"><span data-stu-id="4adc3-108">A RIFF file is composed of multiple discrete sections of data called *chunks*.</span></span>

## <a name="fourcc-identifiers"></a><span data-ttu-id="4adc3-109">FOURCC 識別碼</span><span class="sxs-lookup"><span data-stu-id="4adc3-109">FOURCC Identifiers</span></span>

<span data-ttu-id="4adc3-110">區塊中的資料類型是由四個字元的程式碼所表示 (FOURCC) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4adc3-110">The type of data in a chunk is indicated by a four-character code (FOURCC) identifier.</span></span> <span data-ttu-id="4adc3-111">FOURCC 是在 RIFF 檔案中串連用來識別區塊類型的四個 ASCII 字元所建立的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="4adc3-111">A FOURCC is a 32-bit unsigned integer created by concatenating four ASCII characters used to identify chunk types in a RIFF file.</span></span> <span data-ttu-id="4adc3-112">例如，FOURCC "abcd" 在以位元組由小到大的系統上表示為0x64636261。</span><span class="sxs-lookup"><span data-stu-id="4adc3-112">For example, the FOURCC "abcd" is represented on a little-endian system as 0x64636261.</span></span> <span data-ttu-id="4adc3-113">FOURCCs 可包含空白字元，因此 "abc" 是有效的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="4adc3-113">FOURCCs can contain space characters, so " abc" is a valid FOURCC.</span></span> <span data-ttu-id="4adc3-114">音訊檔案使用 FOURCC 碼來識別音訊格式區塊、音訊資料區塊，以及音訊格式特定的任何其他區塊。</span><span class="sxs-lookup"><span data-stu-id="4adc3-114">Audio files use FOURCC codes to identify audio format chunks, audio data chunks, and any other chunks specific to the audio format.</span></span>

<span data-ttu-id="4adc3-115">下表顯示 XAudio2 支援的音訊格式所能預期的 FOURCC 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4adc3-115">The following table shows the FOURCC identifiers that can be expected in the audio formats supported by XAudio2.</span></span> 

| <span data-ttu-id="4adc3-116">格式</span><span class="sxs-lookup"><span data-stu-id="4adc3-116">Format</span></span> | <span data-ttu-id="4adc3-117">FOURCC 識別碼</span><span class="sxs-lookup"><span data-stu-id="4adc3-117">FOURCC identifiers</span></span>                     | <span data-ttu-id="4adc3-118">其他資訊</span><span class="sxs-lookup"><span data-stu-id="4adc3-118">Additional information</span></span>                                                                               |
|--------|----------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adc3-119">PCM</span><span class="sxs-lookup"><span data-stu-id="4adc3-119">PCM</span></span>    | <span data-ttu-id="4adc3-120">"RIFF"、"bcp.fmt"、"data"</span><span class="sxs-lookup"><span data-stu-id="4adc3-120">"RIFF", "fmt" , "data"</span></span>                 |                                                                                                      |
| <span data-ttu-id="4adc3-121">ADPCM</span><span class="sxs-lookup"><span data-stu-id="4adc3-121">ADPCM</span></span>  | <span data-ttu-id="4adc3-122">"RIFF"、"bcp.fmt"、"data"、"smpl"、"wsmpl"</span><span class="sxs-lookup"><span data-stu-id="4adc3-122">"RIFF", "fmt", "data", "smpl", "wsmpl"</span></span> | <span data-ttu-id="4adc3-123">如需 ADPCM 特定 FOURCC 識別碼的說明，請參閱 [ADPCM 總覽](adpcm-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="4adc3-123">See [ADPCM Overview](adpcm-overview.md) for a description of the ADPCM-specific FOURCC identifiers.</span></span> |



 

<span data-ttu-id="4adc3-124">FOURCC 識別碼 "RIFF"、"bcp.fmt" 和 "data" 通用於所有支援的格式。</span><span class="sxs-lookup"><span data-stu-id="4adc3-124">The FOURCC identifiers "RIFF", "fmt", and "data" are common to all of the supported formats.</span></span> <span data-ttu-id="4adc3-125">下表描述在所有支援的格式中找到的 FOURCC 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4adc3-125">The following table describes the FOURCC identifiers that are found in all of the supported formats.</span></span> 

| <span data-ttu-id="4adc3-126">FOURCC 識別碼</span><span class="sxs-lookup"><span data-stu-id="4adc3-126">FOURCC identifier</span></span> | <span data-ttu-id="4adc3-127">Description</span><span class="sxs-lookup"><span data-stu-id="4adc3-127">Description</span></span>                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4adc3-128">"RIFF"</span><span class="sxs-lookup"><span data-stu-id="4adc3-128">"RIFF"</span></span>            | <span data-ttu-id="4adc3-129">標準 RIFF 區塊，其中包含的檔案類型值為 "WAVE" 或 "XWMA" （在其資料區段的前四個位元組中）和檔案中的其他區塊（資料區段的其餘部分）。</span><span class="sxs-lookup"><span data-stu-id="4adc3-129">Standard RIFF chunk containing a file type with the value of "WAVE" or "XWMA" in the first four bytes of its data section and the other chunks in the file in the remainder of its data section.</span></span>                                   |
| <span data-ttu-id="4adc3-130">"fmt"</span><span class="sxs-lookup"><span data-stu-id="4adc3-130">"fmt"</span></span>             | <span data-ttu-id="4adc3-131">包含音訊檔案的格式標頭。</span><span class="sxs-lookup"><span data-stu-id="4adc3-131">Contains the format header for the audio file.</span></span> <span data-ttu-id="4adc3-132">此區塊中的資料會對應到下列其中一個結構： **WAVEFORMATEX**、 **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**。</span><span class="sxs-lookup"><span data-stu-id="4adc3-132">The data in this chunk corresponds to one of the following structures: **WAVEFORMATEX**, **WAVEFORMATEXTENSIBLE ADPCMWAVEFORMAT**.</span></span>                                                  |
| <span data-ttu-id="4adc3-133">"data"</span><span class="sxs-lookup"><span data-stu-id="4adc3-133">"data"</span></span>            | <span data-ttu-id="4adc3-134">包含音訊檔案的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="4adc3-134">Contains audio data for the audio file.</span></span> <span data-ttu-id="4adc3-135">在 XAudio2 中，資料區塊的內容將會讀入緩衝區，並傳遞至來源語音作為 [**XAudio2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)結構的 **pAudioData** 成員。</span><span class="sxs-lookup"><span data-stu-id="4adc3-135">In XAudio2, the contents of the data chunk will be read into a buffer and passed to a source voice as the **pAudioData** member of an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> |



 

## <a name="chunks"></a><span data-ttu-id="4adc3-136">區塊</span><span class="sxs-lookup"><span data-stu-id="4adc3-136">Chunks</span></span>

<span data-ttu-id="4adc3-137">RIFF 檔案是由包含零或多個其他區塊的 RIFF 區塊所組成。</span><span class="sxs-lookup"><span data-stu-id="4adc3-137">A RIFF file consists of a RIFF chunk containing zero or more other chunks.</span></span>

-   <span data-ttu-id="4adc3-138">RIFF 區塊的格式如下：</span><span class="sxs-lookup"><span data-stu-id="4adc3-138">The RIFF chunk has the following form:</span></span>

    <span data-ttu-id="4adc3-139">"RIFF"，fileSize，資料類型，資料</span><span class="sxs-lookup"><span data-stu-id="4adc3-139">"RIFF", fileSize, fileType, data</span></span>

    <span data-ttu-id="4adc3-140">其中 "RIFF" 是常值 FOURCC 代碼 "RIFF"， *fileSize* 是4位元組值，可提供檔案中的資料大小，而 *類型類型* 則是可識別特定檔案類型的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="4adc3-140">Where "RIFF" is the literal FOURCC code "RIFF", *fileSize* is a 4-byte value giving the size of the data in the file, and *fileType* is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="4adc3-141">*FileSize* 的值包含資料 *類型* 的大小 FOURCC 加上下列資料的大小，但不包含 "RIFF" FOURCC 或 *fileSize* 大小的大小。</span><span class="sxs-lookup"><span data-stu-id="4adc3-141">The value of *fileSize* includes the size of *fileType* FOURCC plus the size of the data that follows, but does not include the size of the "RIFF" FOURCC or the size of *fileSize*.</span></span> <span data-ttu-id="4adc3-142">資料包含任何順序的區塊。</span><span class="sxs-lookup"><span data-stu-id="4adc3-142">The data consists of chunks in any order.</span></span>

-   <span data-ttu-id="4adc3-143">其他區塊的格式如下：</span><span class="sxs-lookup"><span data-stu-id="4adc3-143">Other chunks have the following form:</span></span>

    ```
    chunkID, chunkSize, data
    ```

    

    <span data-ttu-id="4adc3-144">其中 *chunkID* 是識別區塊中所含資料的 FOURCC， *chunkSize* 是4位元組值，可提供區塊的資料區段大小，而資料是零或多個位元組的資料。</span><span class="sxs-lookup"><span data-stu-id="4adc3-144">Where *chunkID* is a FOURCC that identifies the data contained in the chunk, *chunkSize* is a 4-byte value giving the size of the data section of the chunk, and data is zero or more bytes of data.</span></span> <span data-ttu-id="4adc3-145">資料一律會填補到最接近的單字界限。</span><span class="sxs-lookup"><span data-stu-id="4adc3-145">The data is always padded to the nearest WORD boundary.</span></span> <span data-ttu-id="4adc3-146">*chunkSize* 會在區塊中提供有效資料的大小。</span><span class="sxs-lookup"><span data-stu-id="4adc3-146">*chunkSize* gives the size of the valid data in the chunk.</span></span> <span data-ttu-id="4adc3-147">它不包含填補、 *chunkID* 大小或 *chunkSize* 大小。</span><span class="sxs-lookup"><span data-stu-id="4adc3-147">It does not include the padding, the size of *chunkID*, or the size of *chunkSize*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4adc3-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="4adc3-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adc3-149">快速入門</span><span class="sxs-lookup"><span data-stu-id="4adc3-149">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="4adc3-150">使用方法：使用 XAudio2 播放音效</span><span class="sxs-lookup"><span data-stu-id="4adc3-150">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="4adc3-151">XAudio2 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="4adc3-151">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 



