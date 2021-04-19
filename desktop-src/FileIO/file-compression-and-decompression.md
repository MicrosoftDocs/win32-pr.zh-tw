---
description: NTFS 檔案系統使用 Lempel-Ziv 壓縮，也就是不失真的壓縮演算法。
ms.assetid: 35a9fb47-5a73-479c-8fe0-5a2b07705536
title: 檔案壓縮和解壓縮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d1aa9d8d3540eff85413c03358fd1ba7e21300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996945"
---
# <a name="file-compression-and-decompression"></a><span data-ttu-id="594a2-103">檔案壓縮和解壓縮</span><span class="sxs-lookup"><span data-stu-id="594a2-103">File Compression and Decompression</span></span>

<span data-ttu-id="594a2-104">NTFS 檔案系統磁片區支援以個別檔案為基礎來壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="594a2-104">The NTFS file system volumes support file compression on an individual file basis.</span></span> <span data-ttu-id="594a2-105">NTFS 檔案系統所使用的檔案壓縮演算法 Lempel-Ziv 壓縮。</span><span class="sxs-lookup"><span data-stu-id="594a2-105">The file compression algorithm used by the NTFS file system is Lempel-Ziv compression.</span></span> <span data-ttu-id="594a2-106">這是不失真的壓縮演算法，這 *表示壓縮和* 解壓縮檔案時，不會遺失任何資料，而是在每次發生資料壓縮和解壓縮時遺失資料的 *失真壓縮演算法*（例如 JPEG）。</span><span class="sxs-lookup"><span data-stu-id="594a2-106">This is a *lossless* compression algorithm, which means that no data is lost when compressing and decompressing the file, as opposed to *lossy* compression algorithms such as JPEG, where some data is lost each time data compression and decompression occur.</span></span>

<span data-ttu-id="594a2-107">資料壓縮會將多餘的資料降到最低，以縮減檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="594a2-107">Data compression reduces the size of a file by minimizing redundant data.</span></span> <span data-ttu-id="594a2-108">在文字檔中，重複的資料可能是經常發生的字元，例如空白字元或一般母音，例如字母 e 和 a;它也可以是經常發生的字元字串。</span><span class="sxs-lookup"><span data-stu-id="594a2-108">In a text file, redundant data can be frequently occurring characters, such as the space character, or common vowels, such as the letters e and a; it can also be frequently occurring character strings.</span></span> <span data-ttu-id="594a2-109">資料壓縮會藉由將此多餘資料降到最低，來建立檔案的壓縮版本。</span><span class="sxs-lookup"><span data-stu-id="594a2-109">Data compression creates a compressed version of a file by minimizing this redundant data.</span></span>

<span data-ttu-id="594a2-110">每種類型的資料壓縮演算法會以獨特的方式將多餘的資料降到最低。</span><span class="sxs-lookup"><span data-stu-id="594a2-110">Each type of data-compression algorithm minimizes redundant data in a unique manner.</span></span> <span data-ttu-id="594a2-111">例如， *Huffman 編碼演算法* 會根據這些字元的出現頻率，將程式碼指派給檔案中的字元。</span><span class="sxs-lookup"><span data-stu-id="594a2-111">For example, the *Huffman encoding algorithm* assigns a code to characters in a file based on how frequently those characters occur.</span></span> <span data-ttu-id="594a2-112">另一個壓縮演算法（稱為「 *執行長度編碼*」）會針對重複字元產生兩個部分的值：第一個部分會指定重複字元的次數，而第二個部分則會識別該字元。</span><span class="sxs-lookup"><span data-stu-id="594a2-112">Another compression algorithm, called *run-length encoding*, generates a two-part value for repeated characters: the first part specifies the number of times the character is repeated, and the second part identifies the character.</span></span> <span data-ttu-id="594a2-113">另一個壓縮演算法（也稱為 *Lempel-ziv lempel-ziv 演算法*）會將可變長度的字串轉換成固定長度的程式碼，此程式碼耗用的空間比原始字串少。</span><span class="sxs-lookup"><span data-stu-id="594a2-113">Another compression algorithm, known as the *Lempel-Ziv algorithm*, converts variable-length strings into fixed-length codes that consume less space than the original strings.</span></span>

## <a name="the-ntfs-file-system-file-compression"></a><span data-ttu-id="594a2-114">NTFS 檔案系統檔案壓縮</span><span class="sxs-lookup"><span data-stu-id="594a2-114">The NTFS File System File Compression</span></span>

<span data-ttu-id="594a2-115">在 NTFS 檔案系統上，壓縮會以透明的方式執行。</span><span class="sxs-lookup"><span data-stu-id="594a2-115">On the NTFS file system, compression is performed transparently.</span></span> <span data-ttu-id="594a2-116">這表示可以使用它，而不需要變更現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="594a2-116">This means it can be used without requiring changes to existing applications.</span></span> <span data-ttu-id="594a2-117">應用程式無法存取檔案的壓縮位元組;他們只會看到未壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="594a2-117">The compressed bytes of the file are not accessible to applications; they see only the uncompressed data.</span></span> <span data-ttu-id="594a2-118">因此，開啟壓縮檔案的應用程式可以像是未壓縮的一樣運作。</span><span class="sxs-lookup"><span data-stu-id="594a2-118">Therefore, applications that open a compressed file can operate on it as if it were not compressed.</span></span> <span data-ttu-id="594a2-119">不過，這些檔案無法複製到另一個檔案系統。</span><span class="sxs-lookup"><span data-stu-id="594a2-119">However, these files cannot be copied to another file system.</span></span>

<span data-ttu-id="594a2-120">如果您壓縮超過 30 gb 的檔案，壓縮可能不會成功。</span><span class="sxs-lookup"><span data-stu-id="594a2-120">If you compress a file that is larger than 30 gigabytes, the compression may not succeed.</span></span>

<span data-ttu-id="594a2-121">下列主題會識別 NTFS 檔案系統檔案壓縮：</span><span class="sxs-lookup"><span data-stu-id="594a2-121">The following topics identify the NTFS file system file compression:</span></span>

-   [<span data-ttu-id="594a2-122">壓縮屬性</span><span class="sxs-lookup"><span data-stu-id="594a2-122">Compression Attribute</span></span>](compression-attribute.md)
-   [<span data-ttu-id="594a2-123">壓縮狀態</span><span class="sxs-lookup"><span data-stu-id="594a2-123">Compression State</span></span>](compression-state.md)
-   [<span data-ttu-id="594a2-124">取得壓縮檔案的大小</span><span class="sxs-lookup"><span data-stu-id="594a2-124">Obtaining the Size of a Compressed File</span></span>](obtaining-the-size-of-a-compressed-file.md)

## <a name="file-compression-and-decompression-libraries"></a><span data-ttu-id="594a2-125">檔案壓縮和解壓縮程式庫</span><span class="sxs-lookup"><span data-stu-id="594a2-125">File Compression and Decompression Libraries</span></span>

<span data-ttu-id="594a2-126">檔案壓縮和解壓縮程式庫會取得現有的檔案或檔案，並產生原始檔案的壓縮版本檔案。</span><span class="sxs-lookup"><span data-stu-id="594a2-126">The file compression and decompression libraries take an existing file or files and produce a file or files that are compressed versions of the originals.</span></span> <span data-ttu-id="594a2-127">壓縮也不會失真，但應用程式不會察覺壓縮。</span><span class="sxs-lookup"><span data-stu-id="594a2-127">The compression is also lossless, but the compression is not transparent to applications.</span></span> <span data-ttu-id="594a2-128">應用程式只能使用檔案壓縮程式庫的協助來操作這類檔案。</span><span class="sxs-lookup"><span data-stu-id="594a2-128">An application can only operate on such files with the assistance of a file compression library.</span></span> <span data-ttu-id="594a2-129">此外，您可以在這類檔案上執行的唯一作業是從原始的檔案建立壓縮檔案，並從解壓縮的版本復原原始資料。</span><span class="sxs-lookup"><span data-stu-id="594a2-129">In addition, the only operations you can perform on such files are creating a compressed file from an original and recovering the original data from the decompressed version.</span></span> <span data-ttu-id="594a2-130">通常不支援編輯，如果完全支援，則搜尋會受到限制。</span><span class="sxs-lookup"><span data-stu-id="594a2-130">Editing is typically not supported, and seeking is limited if supported at all.</span></span>

<span data-ttu-id="594a2-131">一般而言，應用程式會呼叫 Lz32.dll 中的函式，以解壓縮使用 Compress.exe 壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="594a2-131">Typically, an application calls functions in Lz32.dll to decompress data that was compressed using Compress.exe.</span></span> <span data-ttu-id="594a2-132">函式也可以處理檔案，而不會嘗試將它們解壓縮。</span><span class="sxs-lookup"><span data-stu-id="594a2-132">The functions can also process files without attempting to decompress them.</span></span>

<span data-ttu-id="594a2-133">您可以使用 Lz32.dll 中的函數，將單一或多個檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="594a2-133">You can use the functions in Lz32.dll to decompress single or multiple files.</span></span> <span data-ttu-id="594a2-134">您也可以使用它們，一次將壓縮檔案解壓縮到一個部分。</span><span class="sxs-lookup"><span data-stu-id="594a2-134">You can also use them to decompress compressed files a portion at a time.</span></span>

<span data-ttu-id="594a2-135">下列主題會識別 Lz32.dll 中的函式所提供的檔案解壓縮功能：</span><span class="sxs-lookup"><span data-stu-id="594a2-135">The following topics identify the file decompression that is provided by the functions in Lz32.dll:</span></span>

-   [<span data-ttu-id="594a2-136">解壓縮單一檔案</span><span class="sxs-lookup"><span data-stu-id="594a2-136">Decompressing a single file</span></span>](decompressing-a-single-file.md)
-   [<span data-ttu-id="594a2-137">解壓縮多個檔案</span><span class="sxs-lookup"><span data-stu-id="594a2-137">Decompressing multiple files</span></span>](decompressing-multiple-files.md)
-   [<span data-ttu-id="594a2-138">從壓縮檔案讀取</span><span class="sxs-lookup"><span data-stu-id="594a2-138">Reading from compressed files</span></span>](reading-from-compressed-files.md)

## <a name="cabinets"></a><span data-ttu-id="594a2-139">櫃</span><span class="sxs-lookup"><span data-stu-id="594a2-139">Cabinets</span></span>

<span data-ttu-id="594a2-140">Cab 是由支援磁片跨越和多檔案壓縮等功能的壓縮程式庫所建立。</span><span class="sxs-lookup"><span data-stu-id="594a2-140">Cabinets are created by a compression library that supports features such as disk spanning and multi-file compression.</span></span> <span data-ttu-id="594a2-141">如需其他資訊，請參閱「封包軟體發展工具組：」 [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="594a2-141">For additional information, see the Cabinet Software Development Kit: [https://msdn.microsoft.com/library/dncabsdk/html/cabdl.asp](/previous-versions/ms974336(v=msdn.10)).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="594a2-142">本節內容</span><span class="sxs-lookup"><span data-stu-id="594a2-142">In this section</span></span>



| <span data-ttu-id="594a2-143">主題</span><span class="sxs-lookup"><span data-stu-id="594a2-143">Topic</span></span>                                                                                             | <span data-ttu-id="594a2-144">描述</span><span class="sxs-lookup"><span data-stu-id="594a2-144">Description</span></span>                                                                                                                              |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="594a2-145">壓縮屬性</span><span class="sxs-lookup"><span data-stu-id="594a2-145">Compression Attribute</span></span>](compression-attribute.md)<br/>                                     | <span data-ttu-id="594a2-146">在 NTFS 檔案系統磁片區上，每個檔案和目錄都有一個 *壓縮屬性*。</span><span class="sxs-lookup"><span data-stu-id="594a2-146">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span><br/>                                         |
| [<span data-ttu-id="594a2-147">壓縮狀態</span><span class="sxs-lookup"><span data-stu-id="594a2-147">Compression State</span></span>](compression-state.md)<br/>                                             | <span data-ttu-id="594a2-148">磁片區上的每個檔案和目錄都支援個別檔案和目錄的壓縮，都有 *壓縮狀態*。</span><span class="sxs-lookup"><span data-stu-id="594a2-148">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span><br/> |
| [<span data-ttu-id="594a2-149">取得壓縮檔案的大小</span><span class="sxs-lookup"><span data-stu-id="594a2-149">Obtaining the Size of a Compressed File</span></span>](obtaining-the-size-of-a-compressed-file.md)<br/> | <span data-ttu-id="594a2-150">若要取得壓縮的檔案大小，請使用 GetCompressedFileSize 函數。</span><span class="sxs-lookup"><span data-stu-id="594a2-150">To obtain the compressed size of a file use the GetCompressedFileSize function.</span></span><br/>                                               |
| [<span data-ttu-id="594a2-151">解壓縮單一檔案</span><span class="sxs-lookup"><span data-stu-id="594a2-151">Decompressing a Single File</span></span>](decompressing-a-single-file.md)<br/>                         | <span data-ttu-id="594a2-152">應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式來解壓縮單一壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="594a2-152">An application can decompress a single compressed file by using the LZOpenFile, LZCopy, and LZClose functions.</span></span><br/>                |
| [<span data-ttu-id="594a2-153">解壓縮多個檔案</span><span class="sxs-lookup"><span data-stu-id="594a2-153">Decompressing Multiple Files</span></span>](decompressing-multiple-files.md)<br/>                       | <span data-ttu-id="594a2-154">應用程式可以使用 LZOpenFile、LZCopy 和 LZClose 函式，將多個檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="594a2-154">An application can decompress multiple files by using the LZOpenFile, LZCopy, and LZClose functions.</span></span><br/>                          |
| [<span data-ttu-id="594a2-155">從壓縮檔案讀取</span><span class="sxs-lookup"><span data-stu-id="594a2-155">Reading from Compressed Files</span></span>](reading-from-compressed-files.md)<br/>                     | <span data-ttu-id="594a2-156">應用程式可以使用 LZSeek 和 LZRead 函數，一次將壓縮檔案解壓縮。</span><span class="sxs-lookup"><span data-stu-id="594a2-156">An application can decompress a compressed file a portion at a time by using the LZSeek and LZRead functions.</span></span><br/>                 |



 

 

