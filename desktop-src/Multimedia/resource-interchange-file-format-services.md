---
title: 資源交換檔案格式服務
description: 資源交換檔案格式服務
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- '多媒體檔案 i/o、資源交換檔案格式 (RIFF) '
- '檔案 i/o、資源交換檔案格式 (RIFF) '
- '輸入和輸出 (i/o) 、資源交換檔案格式 (RIFF) '
- 'I/o (輸入和輸出) 、資源交換檔案格式 (RIFF) '
- mmioOpen 函式
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314680"
---
# <a name="resource-interchange-file-format-services"></a><span data-ttu-id="ad3cb-112">資源交換檔案格式服務</span><span class="sxs-lookup"><span data-stu-id="ad3cb-112">Resource Interchange File Format Services</span></span>

<span data-ttu-id="ad3cb-113">多媒體檔案的慣用格式是 (RIFF) 的資源交換檔案格式。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-113">The preferred format for multimedia files is resource interchange file format (RIFF).</span></span> <span data-ttu-id="ad3cb-114">RIFF 檔案 i/o 函式適用于基本的緩衝和無緩衝檔案 i/o 服務。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-114">The RIFF file I/O functions work with the basic buffered and unbuffered file I/O services.</span></span> <span data-ttu-id="ad3cb-115">您可以用與其他檔案類型相同的方式來開啟、讀取和寫入 RIFF 檔案。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-115">You can open, read, and write RIFF files in the same way as other file types.</span></span> <span data-ttu-id="ad3cb-116">如需 RIFF 的詳細資訊，請參閱 [AVIFile 函數和宏](avifile-functions-and-macros.md)。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-116">For detailed information about RIFF, see [AVIFile Functions and Macros](avifile-functions-and-macros.md).</span></span>

<span data-ttu-id="ad3cb-117">RIFF 檔案會使用四個字元的代碼來識別檔案元素。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-117">RIFF files use four-character codes to identify file elements.</span></span> <span data-ttu-id="ad3cb-118">這些程式碼是32位的數量，代表一到四個 ASCII 英數位元的序列，並以空白字元填補右邊。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-118">These codes are 32-bit quantities representing a sequence of one to four ASCII alphanumeric characters, padded on the right with space characters.</span></span> <span data-ttu-id="ad3cb-119">四個字元代碼的資料類型為 **FOURCC**。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-119">The data type for four-character codes is **FOURCC**.</span></span> <span data-ttu-id="ad3cb-120">使用 [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) 宏將四個字元轉換成四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-120">Use the [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) macro to convert four characters into a four-character code.</span></span> <span data-ttu-id="ad3cb-121">若要將以 null 終止的字串轉換成四個字元的程式碼，請使用 [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) 函式。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-121">To convert a null-terminated string into a four-character code, use the [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) function.</span></span>

<span data-ttu-id="ad3cb-122">RIFF 檔的基本組建區塊是一個 *區塊*。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-122">The basic building block of a RIFF file is a *chunk*.</span></span> <span data-ttu-id="ad3cb-123">區塊是多媒體資料的邏輯單元，例如影片剪輯中的單一畫面格。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-123">A chunk is a logical unit of multimedia data, such as a single frame in a video clip.</span></span> <span data-ttu-id="ad3cb-124">每個區塊都包含下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="ad3cb-124">Each chunk contains the following fields:</span></span>

-   <span data-ttu-id="ad3cb-125">指定區塊識別碼的四個字元的代碼</span><span class="sxs-lookup"><span data-stu-id="ad3cb-125">A four-character code specifying the chunk identifier</span></span>
-   <span data-ttu-id="ad3cb-126">指定區塊中資料成員大小的雙精度值</span><span class="sxs-lookup"><span data-stu-id="ad3cb-126">A doubleword value specifying the size of the data member in the chunk</span></span>
-   <span data-ttu-id="ad3cb-127">資料欄位</span><span class="sxs-lookup"><span data-stu-id="ad3cb-127">A data field</span></span>

<span data-ttu-id="ad3cb-128">下圖顯示包含兩個 subchunks 的 "RIFF" 區塊。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-128">The following illustration shows a "RIFF" chunk that contains two subchunks.</span></span>

![riff 包含兩個 subchunks 影像的區塊](images/mmio1.gif)

<span data-ttu-id="ad3cb-130">包含在另一個區塊中的區塊是 *subchunk*。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-130">A chunk contained in another chunk is a *subchunk*.</span></span> <span data-ttu-id="ad3cb-131">唯一允許包含 subchunks 的區塊是具有 "RIFF" 或 "LIST" 區塊識別碼的區塊。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-131">The only chunks allowed to contain subchunks are those with a chunk identifier of "RIFF" or "LIST".</span></span> <span data-ttu-id="ad3cb-132">包含另一個區塊的區塊稱為 *父區塊*。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-132">A chunk that contains another chunk is called a *parent chunk*.</span></span> <span data-ttu-id="ad3cb-133">RIFF 檔案中的第一個區塊必須是 "RIFF" 區塊。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-133">The first chunk in a RIFF file must be a "RIFF" chunk.</span></span> <span data-ttu-id="ad3cb-134">檔案中的所有其他區塊都是 "RIFF" 區塊的 subchunks。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-134">All other chunks in the file are subchunks of the "RIFF" chunk.</span></span>

<span data-ttu-id="ad3cb-135">"RIFF" 區塊在資料欄位的前四個位元組中包含額外的欄位。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-135">"RIFF" chunks include an additional field in the first four bytes of the data field.</span></span> <span data-ttu-id="ad3cb-136">這個額外的欄位提供欄位的 *表單類型* 。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-136">This additional field provides the *form type* of the field.</span></span> <span data-ttu-id="ad3cb-137">表單類型是四個字元的代碼，可識別儲存在檔案中的資料格式。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-137">The form type is a four-character code identifying the format of the data stored in the file.</span></span> <span data-ttu-id="ad3cb-138">例如，Microsoft 波形-音訊檔案的格式為 "WAVE"。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-138">For example, Microsoft waveform-audio files have a form type of "WAVE".</span></span>

<span data-ttu-id="ad3cb-139">「清單」區塊也會在資料欄位的前四個位元組中包含額外的欄位。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-139">"LIST" chunks also include an additional field in the first four bytes of the data field.</span></span> <span data-ttu-id="ad3cb-140">此額外欄位包含欄位的 *清單類型* 。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-140">This additional field contains the *list type* of the field.</span></span> <span data-ttu-id="ad3cb-141">清單類型是識別清單內容的四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-141">The list type is a four-character code identifying the contents of the list.</span></span> <span data-ttu-id="ad3cb-142">例如，清單類型為 "INFO" 的 "LIST" 區塊可以包含 "ICOP" 和 "ICRD" 區塊，以提供著作權和建立日期資訊。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-142">For example, a "LIST" chunk with a list type of "INFO" can contain "ICOP" and "ICRD" chunks providing copyright and creation date information.</span></span> <span data-ttu-id="ad3cb-143">下圖顯示「RIFF」區塊，其中包含「清單」區塊和另一個 subchunk (「清單」區塊包含兩個 subchunks) 。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-143">The following illustration shows a "RIFF" chunk that contains a "LIST" chunk and one other subchunk (the "LIST" chunk contains two subchunks).</span></span>

![包含清單區塊影像的 riff 區塊](images/mmio2.gif)

<span data-ttu-id="ad3cb-145">多媒體檔案 i/o 服務包含兩個函式，可供您在 RIFF 檔中的區塊之間進行流覽： [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) 和 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-145">Multimedia file I/O services include two functions you can use to navigate among chunks in a RIFF file: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) and [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend).</span></span> <span data-ttu-id="ad3cb-146">您可以使用這些函數做為高階搜尋函式。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-146">You can use these functions as high-level seek functions.</span></span> <span data-ttu-id="ad3cb-147">當您下降到區塊時，檔案位置會設定為區塊的資料欄位， (從區塊開頭算起的8個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-147">When you descend into a chunk, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="ad3cb-148">針對 "RIFF" 和 "LIST" 區塊，檔案位置會設定為表單類型或清單類型後面的位置， (從區塊開頭的12個位元組開始) 。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-148">For "RIFF" and "LIST" chunks, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="ad3cb-149">當您將區塊遞增時，檔案位置會設定為在區塊結尾之後的位置。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-149">When you ascend out of a chunk, the file position is set to the location following the end of the chunk.</span></span>

<span data-ttu-id="ad3cb-150">若要建立新的區塊，請使用 [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) 函式，在開啟的檔案中的目前位置寫入區塊標頭。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-150">To create a new chunk, use the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to write a chunk header at the current position in an open file.</span></span> <span data-ttu-id="ad3cb-151">**MmioAscend**、 **mmioDescend** 和 **MmioCreateChunk** 函式會使用 [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)結構來指定和取得 "RIFF" 區塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad3cb-151">The **mmioAscend**, **mmioDescend**, and **mmioCreateChunk** functions use the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure to specify and retrieve information about "RIFF" chunks.</span></span>

 

 