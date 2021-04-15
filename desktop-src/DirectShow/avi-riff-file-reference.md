---
description: AVI RIFF 檔案參考
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: AVI RIFF 檔案參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467898"
---
# <a name="avi-riff-file-reference"></a><span data-ttu-id="00b53-103">AVI RIFF 檔案參考</span><span class="sxs-lookup"><span data-stu-id="00b53-103">AVI RIFF File Reference</span></span>

<span data-ttu-id="00b53-104">Microsoft AVI 檔案格式是一種 RIFF 檔規格，與可捕獲、編輯及播放音訊影片順序的應用程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="00b53-104">The Microsoft AVI file format is a RIFF file specification used with applications that capture, edit, and play back audio-video sequences.</span></span> <span data-ttu-id="00b53-105">一般情況下，AVI 檔案包含多個不同資料類型的資料流程。</span><span class="sxs-lookup"><span data-stu-id="00b53-105">In general, AVI files contain multiple streams of different types of data.</span></span> <span data-ttu-id="00b53-106">大部分的 AVI 序列都會使用音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="00b53-106">Most AVI sequences use both audio and video streams.</span></span> <span data-ttu-id="00b53-107">AVI 序列的簡單變化會使用影片資料，而且不需要音訊串流。</span><span class="sxs-lookup"><span data-stu-id="00b53-107">A simple variation for an AVI sequence uses video data and does not require an audio stream.</span></span>

<span data-ttu-id="00b53-108">本節不說明 OpenDML AVI 檔案格式延伸模組。</span><span class="sxs-lookup"><span data-stu-id="00b53-108">This section does not describe the OpenDML AVI file format extensions.</span></span> <span data-ttu-id="00b53-109">如需這些擴充功能的進一步資訊，請參閱 *OPENDML Avi 檔案格式延伸* 模組，由 OpenDML avi M-JPEG 檔案格式 Subcommittee 發行。</span><span class="sxs-lookup"><span data-stu-id="00b53-109">For further information on these extensions, see *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="fourccs"></a><span data-ttu-id="00b53-110">FOURCCs</span><span class="sxs-lookup"><span data-stu-id="00b53-110">FOURCCs</span></span>

<span data-ttu-id="00b53-111">FOURCC (四個字元的程式碼) 是串連四個 ASCII 字元所建立的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="00b53-111">A FOURCC (four-character code) is a 32-bit unsigned integer created by concatenating four ASCII characters.</span></span> <span data-ttu-id="00b53-112">例如，FOURCC ' abcd ' 在 Little-Endian 系統上表示為0x64636261。</span><span class="sxs-lookup"><span data-stu-id="00b53-112">For example, the FOURCC 'abcd' is represented on a Little-Endian system as 0x64636261.</span></span> <span data-ttu-id="00b53-113">FOURCCs 可包含空白字元，因此 ' abc ' 是有效的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="00b53-113">FOURCCs can contain space characters, so ' abc' is a valid FOURCC.</span></span> <span data-ttu-id="00b53-114">AVI 檔案格式會使用 FOURCC 碼來識別資料流程類型、資料區塊、索引項目目和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="00b53-114">The AVI file format uses FOURCC codes to identify stream types, data chunks, index entries, and other information.</span></span>

## <a name="riff-file-format"></a><span data-ttu-id="00b53-115">RIFF 檔案格式</span><span class="sxs-lookup"><span data-stu-id="00b53-115">RIFF File Format</span></span>

<span data-ttu-id="00b53-116">AVI 檔案格式是以 RIFF (資源交換檔案格式) 檔案格式為基礎。</span><span class="sxs-lookup"><span data-stu-id="00b53-116">The AVI file format is based on the RIFF (resource interchange file format) document format.</span></span> <span data-ttu-id="00b53-117">RIFF 檔案包含 RIFF 標頭，後面接著零或多個 *清單* 和 *區塊*。</span><span class="sxs-lookup"><span data-stu-id="00b53-117">A RIFF file consists of a RIFF header followed by zero or more *lists* and *chunks*.</span></span>

-   <span data-ttu-id="00b53-118">RIFF 標頭的格式如下：</span><span class="sxs-lookup"><span data-stu-id="00b53-118">The RIFF header has the following form:</span></span>

    `'RIFF' fileSize fileType (data)`

    <span data-ttu-id="00b53-119">其中 ' RIFF ' 是常值 FOURCC 代碼 ' RIFF '， `fileSize` 是4位元組值，提供檔案中的資料大小，而 `fileType` 是識別特定檔案類型的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="00b53-119">where 'RIFF' is the literal FOURCC code 'RIFF', `fileSize` is a 4-byte value giving the size of the data in the file, and `fileType` is a FOURCC that identifies the specific file type.</span></span> <span data-ttu-id="00b53-120">的值 `fileSize` 包括 FOURCC 的大小 `fileType` 加上下列資料的大小，但不包含 ' RIFF ' FOURCC 的大小或的大小 `fileSize` 。</span><span class="sxs-lookup"><span data-stu-id="00b53-120">The value of `fileSize` includes the size of the `fileType` FOURCC plus the size of the data that follows, but does not include the size of the 'RIFF' FOURCC or the size of `fileSize`.</span></span> <span data-ttu-id="00b53-121">檔案資料是以任何順序由區塊和清單所組成。</span><span class="sxs-lookup"><span data-stu-id="00b53-121">The file data consists of chunks and lists, in any order.</span></span>

-   <span data-ttu-id="00b53-122">區塊的格式如下：</span><span class="sxs-lookup"><span data-stu-id="00b53-122">A chunk has the following form:</span></span>

    `ckID ckSize ckData`

    <span data-ttu-id="00b53-123">其中 `ckID` 是識別區塊中所含資料的 FOURCC， `ckSize` 是4位元組值，提供中資料的大小 `ckData` ，而 `ckData` 是零或多個位元組的資料。</span><span class="sxs-lookup"><span data-stu-id="00b53-123">where `ckID` is a FOURCC that identifies the data contained in the chunk, `ckSize` is a 4-byte value giving the size of the data in `ckData`, and `ckData` is zero or more bytes of data.</span></span> <span data-ttu-id="00b53-124">資料一律會填補到最接近的 **單字** 界限。</span><span class="sxs-lookup"><span data-stu-id="00b53-124">The data is always padded to nearest **WORD** boundary.</span></span> <span data-ttu-id="00b53-125">`ckSize` 提供區塊中有效資料的大小;它不包含填補、大小 `ckID` 或的大小 `ckSize` 。</span><span class="sxs-lookup"><span data-stu-id="00b53-125">`ckSize` gives the size of the valid data in the chunk; it does not include the padding, the size of `ckID`, or the size of `ckSize`.</span></span>

-   <span data-ttu-id="00b53-126">清單的格式如下：</span><span class="sxs-lookup"><span data-stu-id="00b53-126">A list has the following form:</span></span>

    `'LIST' listSize listType listData`

    <span data-ttu-id="00b53-127">其中 ' LIST ' 是常值 FOURCC 代碼 ' LIST '， `listSize` 是一個4位元組值，提供清單的大小、 `listType` 是 FOURCC 程式碼，並 `listData` 以任何順序包含區塊或清單。</span><span class="sxs-lookup"><span data-stu-id="00b53-127">where 'LIST' is the literal FOURCC code 'LIST', `listSize` is a 4-byte value giving the size of the list, `listType` is a FOURCC code, and `listData` consists of chunks or lists, in any order.</span></span> <span data-ttu-id="00b53-128">的值包含的大小 `listSize` `listType` 加上大小，不 `listData` 包含 ' LIST ' FOURCC 或的大小 `listSize` 。</span><span class="sxs-lookup"><span data-stu-id="00b53-128">The value of `listSize` includes the size of `listType` plus the size of `listData`; it does not include the 'LIST' FOURCC or the size of `listSize`.</span></span>

<span data-ttu-id="00b53-129">本節的其餘部分會使用下列標記法來描述 RIFF 區塊：</span><span class="sxs-lookup"><span data-stu-id="00b53-129">The remainder of this section uses the following notation to describe RIFF chunks:</span></span>

`ckID ( ckData )`

<span data-ttu-id="00b53-130">區塊大小是隱含的。</span><span class="sxs-lookup"><span data-stu-id="00b53-130">where the chunk size is implicit.</span></span> <span data-ttu-id="00b53-131">使用此標記法時，清單可以表示為：</span><span class="sxs-lookup"><span data-stu-id="00b53-131">Using this notation, a list can be represented as:</span></span>

`'LIST' ( listType ( listData ) )`

<span data-ttu-id="00b53-132">選擇性元素會放在括弧中： `[ optional element ]`</span><span class="sxs-lookup"><span data-stu-id="00b53-132">Optional elements are placed in brackets: `[ optional element ]`</span></span>

## <a name="avi-riff-form"></a><span data-ttu-id="00b53-133">AVI RIFF 表單</span><span class="sxs-lookup"><span data-stu-id="00b53-133">AVI RIFF Form</span></span>

<span data-ttu-id="00b53-134">AVI 檔案是由 RIFF 標頭中的 FOURCC ' AVI ' 所識別。</span><span class="sxs-lookup"><span data-stu-id="00b53-134">AVI files are identified by the FOURCC 'AVI ' in the RIFF header.</span></span> <span data-ttu-id="00b53-135">所有 AVI 檔案都包含兩個強制清單區塊，分別定義資料流程和資料流程資料的格式。</span><span class="sxs-lookup"><span data-stu-id="00b53-135">All AVI files include two mandatory LIST chunks, which define the format of the streams and the stream data, respectively.</span></span> <span data-ttu-id="00b53-136">AVI 檔案也可能包含索引區塊，以提供檔案內資料區塊的位置。</span><span class="sxs-lookup"><span data-stu-id="00b53-136">An AVI file might also include an index chunk, which gives the location of the data chunks within the file.</span></span> <span data-ttu-id="00b53-137">具有這些元件的 AVI 檔案具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="00b53-137">An AVI file with these components has the following form:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



<span data-ttu-id="00b53-138">' Hdrl ' 清單會定義資料的格式，而且是第一個必要的清單區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-138">The 'hdrl' list defines the format of the data and is the first required LIST chunk.</span></span> <span data-ttu-id="00b53-139">' Movi ' 清單包含 AVI 序列的資料，而是第二個必要的清單區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-139">The 'movi' list contains the data for the AVI sequence and is the second required LIST chunk.</span></span> <span data-ttu-id="00b53-140">' Idx1 ' 清單包含索引。</span><span class="sxs-lookup"><span data-stu-id="00b53-140">The 'idx1' list contains the index.</span></span> <span data-ttu-id="00b53-141">AVI 檔案必須以正確的順序保留這三個元件。</span><span class="sxs-lookup"><span data-stu-id="00b53-141">AVI files must keep these three components in the proper sequence.</span></span>

> [!Note]  
> <span data-ttu-id="00b53-142">OpenDML 延伸模組會定義另一個索引類型，由 FOURCC ' indx ' 識別。</span><span class="sxs-lookup"><span data-stu-id="00b53-142">The OpenDML extensions define another type of index, identified by the FOURCC 'indx'.</span></span>

 

<span data-ttu-id="00b53-143">' Hdrl ' 和 ' movi ' 清單會將 subchunks 用於其資料。</span><span class="sxs-lookup"><span data-stu-id="00b53-143">The 'hdrl' and 'movi' lists use subchunks for their data.</span></span> <span data-ttu-id="00b53-144">下列範例顯示以完成這些清單所需的區塊擴充的 AVI RIFF 表單：</span><span class="sxs-lookup"><span data-stu-id="00b53-144">The following example shows the AVI RIFF form expanded with the chunks needed to complete these lists:</span></span>


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a><span data-ttu-id="00b53-145">AVI 主要標頭</span><span class="sxs-lookup"><span data-stu-id="00b53-145">AVI Main Header</span></span>

<span data-ttu-id="00b53-146">' Hdrl ' 清單是以包含在 ' avih ' 區塊中的主要 AVI 標頭為開頭。</span><span class="sxs-lookup"><span data-stu-id="00b53-146">The 'hdrl' list begins with the main AVI header, which is contained in an 'avih' chunk.</span></span> <span data-ttu-id="00b53-147">主要標頭包含整個 AVI 檔案的全域資訊，例如檔案內的資料流程數目，以及 AVI 序列的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="00b53-147">The main header contains global information for the entire AVI file, such as the number of streams within the file and the width and height of the AVI sequence.</span></span> <span data-ttu-id="00b53-148">主要標頭區塊是由 [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) 結構所組成。</span><span class="sxs-lookup"><span data-stu-id="00b53-148">The main header chunk consists of an [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

## <a name="avi-stream-headers"></a><span data-ttu-id="00b53-149">AVI 資料流程標頭</span><span class="sxs-lookup"><span data-stu-id="00b53-149">AVI Stream Headers</span></span>

<span data-ttu-id="00b53-150">一或多個 ' strl ' 清單在主要標頭之後。</span><span class="sxs-lookup"><span data-stu-id="00b53-150">One or more 'strl' lists follow the main header.</span></span> <span data-ttu-id="00b53-151">每個資料流程都需要 ' strl ' 清單。</span><span class="sxs-lookup"><span data-stu-id="00b53-151">A 'strl' list is required for each data stream.</span></span> <span data-ttu-id="00b53-152">每個 ' strl ' 清單都包含檔案中某個資料流程的相關資訊，而且必須包含資料流程標頭區塊 ( ' strh ' ) 和 ( ' strf ' ) 的資料流程格式區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-152">Each 'strl' list contains information about one stream in the file, and must contain a stream header chunk ('strh') and a stream format chunk ('strf').</span></span> <span data-ttu-id="00b53-153">此外，' strl ' 清單可能包含資料流程標頭資料區塊 ( ' strd ' ) 和 ( ' strn ' ) 的資料流程名稱區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-153">In addition, a 'strl' list might contain a stream-header data chunk ('strd') and a stream name chunk ('strn').</span></span>

<span data-ttu-id="00b53-154">資料流程標頭區塊 ( ' strh ' ) 由 [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) 結構組成。</span><span class="sxs-lookup"><span data-stu-id="00b53-154">The stream header chunk ('strh') consists of an [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure.</span></span>

<span data-ttu-id="00b53-155">資料流程格式區塊 ( ' strf ' ) 必須遵照資料流程標頭區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-155">A stream format chunk ('strf') must follow the stream header chunk.</span></span> <span data-ttu-id="00b53-156">資料流程格式區塊描述資料流程中資料的格式。</span><span class="sxs-lookup"><span data-stu-id="00b53-156">The stream format chunk describes the format of the data in the stream.</span></span> <span data-ttu-id="00b53-157">此區塊中包含的資料取決於資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="00b53-157">The data contained in this chunk depends on the stream type.</span></span> <span data-ttu-id="00b53-158">針對影片串流，此資訊是 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構，其中包含適用的調色板資訊。</span><span class="sxs-lookup"><span data-stu-id="00b53-158">For video streams, the information is a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, including palette information if appropriate.</span></span> <span data-ttu-id="00b53-159">針對音訊串流，此資訊是 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="00b53-159">For audio streams, the information is a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="00b53-160">如果資料流程標頭資料 ( ' strd ' ) 區塊存在，則會遵循資料流程格式區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-160">If the stream-header data ('strd') chunk is present, it follows the stream format chunk.</span></span> <span data-ttu-id="00b53-161">此區塊的格式和內容是由編解碼器驅動程式所定義。</span><span class="sxs-lookup"><span data-stu-id="00b53-161">The format and content of this chunk are defined by the codec driver.</span></span> <span data-ttu-id="00b53-162">通常，驅動程式會使用此資訊進行設定。</span><span class="sxs-lookup"><span data-stu-id="00b53-162">Typically, drivers use this information for configuration.</span></span> <span data-ttu-id="00b53-163">讀取和寫入 AVI 檔案的應用程式不需要解讀此資訊;它們可輕鬆地將它傳輸到驅動程式，做為記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-163">Applications that read and write AVI files do not need to interpret this information; they simple transfer it to and from the driver as a memory block.</span></span>

<span data-ttu-id="00b53-164">選擇性的 ' strn ' 區塊包含描述資料流程的以 null 結束的文字字串。</span><span class="sxs-lookup"><span data-stu-id="00b53-164">The optional 'strn' chunk contains a null-terminated text string describing the stream.</span></span>

<span data-ttu-id="00b53-165">' Hdrl ' 清單中的資料流程標頭會根據 ' strl ' 區塊的順序，與 ' movi ' 清單中的資料流程資料相關聯。</span><span class="sxs-lookup"><span data-stu-id="00b53-165">The stream headers in the 'hdrl' list are associated with the stream data in the 'movi' list according to the order of the 'strl' chunks.</span></span> <span data-ttu-id="00b53-166">第一個 ' strl ' 區塊適用于 stream 0，第二個區塊適用于 stream 1 等等。</span><span class="sxs-lookup"><span data-stu-id="00b53-166">The first 'strl' chunk applies to stream 0, the second applies to stream 1, and so forth.</span></span>

## <a name="stream-data-movi-list"></a><span data-ttu-id="00b53-167">串流資料 ( ' movi ' 清單) </span><span class="sxs-lookup"><span data-stu-id="00b53-167">Stream Data ('movi' List)</span></span>

<span data-ttu-id="00b53-168">標頭資訊之後的「movi」清單會包含資料流程中的實際資料，也就是影片畫面和音訊範例。</span><span class="sxs-lookup"><span data-stu-id="00b53-168">Following the header information is a 'movi' list that contains the actual data in the streams—that is, the video frames and audio samples.</span></span> <span data-ttu-id="00b53-169">資料區塊可以直接位於 ' movi ' 清單中，或可能會在 ' rec ' 清單中分組。</span><span class="sxs-lookup"><span data-stu-id="00b53-169">The data chunks can reside directly in the 'movi' list, or they might be grouped within 'rec ' lists.</span></span> <span data-ttu-id="00b53-170">「Rec」群組意指應一次從磁片讀取群組的區塊，並將其用於交錯從 CD-ROM 播放的檔案。</span><span class="sxs-lookup"><span data-stu-id="00b53-170">The 'rec ' grouping implies that the grouped chunks should be read from disk all at once, and is intended for files that are interleaved to play from CD-ROM.</span></span>

<span data-ttu-id="00b53-171">識別每個資料區塊的 FOURCC 包含兩位數的資料流程數位，後面接著兩個字元的程式碼，以定義區塊中的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="00b53-171">The FOURCC that identifies each data chunk consists of a two-digit stream number followed by a two-character code that defines the type of information in the chunk.</span></span>



| <span data-ttu-id="00b53-172">雙字元碼</span><span class="sxs-lookup"><span data-stu-id="00b53-172">Two-character code</span></span> | <span data-ttu-id="00b53-173">Description</span><span class="sxs-lookup"><span data-stu-id="00b53-173">Description</span></span>              |
|--------------------|--------------------------|
| <span data-ttu-id="00b53-174">db</span><span class="sxs-lookup"><span data-stu-id="00b53-174">db</span></span>                 | <span data-ttu-id="00b53-175">未壓縮的影片畫面</span><span class="sxs-lookup"><span data-stu-id="00b53-175">Uncompressed video frame</span></span> |
| <span data-ttu-id="00b53-176">dc</span><span class="sxs-lookup"><span data-stu-id="00b53-176">dc</span></span>                 | <span data-ttu-id="00b53-177">壓縮的影片畫面</span><span class="sxs-lookup"><span data-stu-id="00b53-177">Compressed video frame</span></span>   |
| <span data-ttu-id="00b53-178">pc</span><span class="sxs-lookup"><span data-stu-id="00b53-178">pc</span></span>                 | <span data-ttu-id="00b53-179">元件變更</span><span class="sxs-lookup"><span data-stu-id="00b53-179">Palette change</span></span>           |
| <span data-ttu-id="00b53-180">工 務 局</span><span class="sxs-lookup"><span data-stu-id="00b53-180">wb</span></span>                 | <span data-ttu-id="00b53-181">音訊資料</span><span class="sxs-lookup"><span data-stu-id="00b53-181">Audio data</span></span>               |



 

<span data-ttu-id="00b53-182">例如，如果 stream 0 包含音訊，則該資料流程的資料區塊會有 FOURCC ' 00wb '。</span><span class="sxs-lookup"><span data-stu-id="00b53-182">For example, if stream 0 contains audio, the data chunks for that stream would have the FOURCC '00wb'.</span></span> <span data-ttu-id="00b53-183">如果 stream 1 包含影片，則該資料流程的資料區塊會有 FOURCC ' 01db ' 或 ' 01dc '。</span><span class="sxs-lookup"><span data-stu-id="00b53-183">If stream 1 contains video, the data chunks for that stream would have the FOURCC '01db' or '01dc'.</span></span> <span data-ttu-id="00b53-184">影片資料區塊也可以定義新的調色板專案，在 AVI 序列期間更新調色板。</span><span class="sxs-lookup"><span data-stu-id="00b53-184">Video data chunks can also define new palette entries to update the palette during an AVI sequence.</span></span> <span data-ttu-id="00b53-185">每個調色板-變更區塊 ( ' xxpc ' ) 包含 [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) 結構。</span><span class="sxs-lookup"><span data-stu-id="00b53-185">Each palette-change chunk ('xxpc') contains an [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) structure.</span></span> <span data-ttu-id="00b53-186">如果資料流程包含元件元件變更，請在該資料流程的 [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader)結構的 **dwFlags** 成員中設定 **AVISF \_ VIDEO \_ PALCHANGES** 旗標。</span><span class="sxs-lookup"><span data-stu-id="00b53-186">If a stream contains palette changes, set the **AVISF\_VIDEO\_PALCHANGES** flag in the **dwFlags** member of the [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) structure for that stream.</span></span>

<span data-ttu-id="00b53-187">文字資料流程可以使用任意兩個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="00b53-187">Text streams can use arbitrary two-character codes.</span></span>

## <a name="avi-index-entries"></a><span data-ttu-id="00b53-188">AVI 索引項目</span><span class="sxs-lookup"><span data-stu-id="00b53-188">AVI Index Entries</span></span>

<dl> <dt>

<span data-ttu-id="00b53-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 索引</span><span class="sxs-lookup"><span data-stu-id="00b53-189"><span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1.0 index</span></span>
</dt> <dd>

<span data-ttu-id="00b53-190"> ( ' idx1 ' ) 區塊的選擇性索引可以跟隨在 ' movi ' 清單後面。</span><span class="sxs-lookup"><span data-stu-id="00b53-190">An optional index ('idx1') chunk can follow the 'movi' list.</span></span> <span data-ttu-id="00b53-191">索引包含資料區塊的清單，以及其在檔案中的位置。</span><span class="sxs-lookup"><span data-stu-id="00b53-191">The index contains a list of the data chunks and their location in the file.</span></span> <span data-ttu-id="00b53-192">它包含 [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) 結構，其中包含每個資料區塊的專案，包括 ' rec ' 區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-192">It consists of an [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) structure with entries for each data chunk, including 'rec ' chunks.</span></span> <span data-ttu-id="00b53-193">如果檔案包含索引，請在 [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader)結構的 **dwFlags** 成員中設定 **AVIF \_ HASINDEX** 旗標。</span><span class="sxs-lookup"><span data-stu-id="00b53-193">If the file contains an index, set the **AVIF\_HASINDEX** flag in the **dwFlags** member of the [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="00b53-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 索引</span><span class="sxs-lookup"><span data-stu-id="00b53-194"><span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2.0 index</span></span>
</dt> <dd>

<span data-ttu-id="00b53-195">AVI 2.0 索引可以顯示為單一區塊。</span><span class="sxs-lookup"><span data-stu-id="00b53-195">An AVI 2.0 index can appear as a single chunk.</span></span> <span data-ttu-id="00b53-196">或者，索引區段可以交錯在 ' movi ' 區塊內。</span><span class="sxs-lookup"><span data-stu-id="00b53-196">Alternatively, index segments can be interleaved within the 'movi' chunk.</span></span> <span data-ttu-id="00b53-197">如果索引區段放在 ' movi ' 區塊中，則超級索引會包含索引區段的索引。</span><span class="sxs-lookup"><span data-stu-id="00b53-197">If the index segments are placed in the 'movi' chunk, a super index contains an index of the index segments.</span></span> <span data-ttu-id="00b53-198">[**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex)結構是索引區段和超級索引的基底結構。</span><span class="sxs-lookup"><span data-stu-id="00b53-198">The [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) structure is the base structure for both the index segments and the super index.</span></span> <span data-ttu-id="00b53-199">如需詳細資訊，請參閱 OpenDML AVI M-JPEG 檔案格式 Subcommittee 所發佈的 *OPENDML Avi 檔案格式延伸*。</span><span class="sxs-lookup"><span data-stu-id="00b53-199">For more information, see the *OpenDML AVI File Format Extensions*, published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span> <span data-ttu-id="00b53-200"> (此資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="00b53-200">(This resource may not be available in some languages and countries.)</span></span>

</dd> </dl>

## <a name="other-data-chunks"></a><span data-ttu-id="00b53-201">其他資料區塊</span><span class="sxs-lookup"><span data-stu-id="00b53-201">Other Data Chunks</span></span>

<span data-ttu-id="00b53-202">您可以視需要插入「垃圾」區塊，以將資料對齊 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="00b53-202">Data can be aligned in an AVI file by inserting 'JUNK' chunks as needed.</span></span> <span data-ttu-id="00b53-203">應用程式應該忽略「垃圾」區塊的內容。</span><span class="sxs-lookup"><span data-stu-id="00b53-203">Applications should ignore the contents of a 'JUNK' chunk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b53-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="00b53-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b53-205">AVI 檔案格式</span><span class="sxs-lookup"><span data-stu-id="00b53-205">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
