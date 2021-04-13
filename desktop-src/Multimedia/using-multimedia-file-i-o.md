---
title: 使用多媒體檔案 i/o
description: 使用多媒體檔案 i/o
ms.assetid: bc568e80-f1ca-43c8-bd45-2b4ad1dd53ed
keywords:
- Windows 多媒體，檔案 i/o
- 多媒體，檔案 i/o
- 多媒體輸入，file i/o
- 多媒體檔案 i/o，關於
- 檔案 i/o，關於
- 輸入和輸出 (i/o) ，關於
- I/o (輸入和輸出) ，關於
- 多媒體檔案 i/o，範例
- 檔案 i/o，範例
- 輸入和輸出 (i/o) ，範例
- I/o (輸入和輸出) ，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477e7b07394b33326030b0eeebae8eb1a6415c1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301468"
---
# <a name="using-multimedia-file-io"></a><span data-ttu-id="996ad-114">使用多媒體檔案 i/o</span><span class="sxs-lookup"><span data-stu-id="996ad-114">Using Multimedia File I/O</span></span>

<span data-ttu-id="996ad-115">本節包含的範例示範如何執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="996ad-115">This section contains examples demonstrating how to perform the following tasks:</span></span>

-   [<span data-ttu-id="996ad-116">使用 mmioOpen 開啟檔案</span><span class="sxs-lookup"><span data-stu-id="996ad-116">Opening a File with mmioOpen</span></span>](opening-a-file-with-mmioopen.md)
-   <span data-ttu-id="996ad-117">[建立和刪除](creating-and-deleting-a-file.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="996ad-117">[Creating and Deleting a File](creating-and-deleting-a-file.md).</span></span>
-   <span data-ttu-id="996ad-118">[搜尋檔案中的新位置](seeking-to-a-new-position-in-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-118">[Seeking to a New Position in a File](seeking-to-a-new-position-in-a-file.md).</span></span>
-   <span data-ttu-id="996ad-119">[變更 I/o 緩衝區大小](changing-the-i-o-buffer-size.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-119">[Changing the I/O Buffer Size](changing-the-i-o-buffer-size.md).</span></span>
-   <span data-ttu-id="996ad-120">[存取檔案 I/o 緩衝區](accessing-a-file-i-o-buffer.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-120">[Accessing a File I/O Buffer](accessing-a-file-i-o-buffer.md).</span></span>
-   <span data-ttu-id="996ad-121">[產生 Four-Character 碼](generating-four-character-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-121">[Generating Four-Character Codes](generating-four-character-codes.md).</span></span>
-   <span data-ttu-id="996ad-122">[建立 RIFF 區塊](creating-a-riff-chunk.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-122">[Creating a RIFF Chunk](creating-a-riff-chunk.md).</span></span>
-   <span data-ttu-id="996ad-123">[搜尋 RIFF 區塊](searching-for-a-riff-chunk.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-123">[Searching for a RIFF Chunk](searching-for-a-riff-chunk.md).</span></span>
-   <span data-ttu-id="996ad-124">[搜尋 Subchunk](searching-for-a-subchunk.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-124">[Searching for a Subchunk](searching-for-a-subchunk.md).</span></span>
-   <span data-ttu-id="996ad-125">[在 RIFF 檔案上執行檔案 i/o](performing-file-i-o-on-riff-files.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-125">[Performing File I/O on RIFF Files](performing-file-i-o-on-riff-files.md).</span></span>
-   <span data-ttu-id="996ad-126">[正在執行記憶體檔 i/o](performing-memory-file-i-o.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-126">[Performing Memory File I/O](performing-memory-file-i-o.md).</span></span>
-   <span data-ttu-id="996ad-127">[安裝自訂 I/o 程式](installing-custom-i-o-procedures.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-127">[Installing Custom I/O Procedures](installing-custom-i-o-procedures.md).</span></span>
-   <span data-ttu-id="996ad-128">[與其他應用程式共用 I/o 程式](sharing-an-i-o-procedure-with-other-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="996ad-128">[Sharing an I/O Procedure with Other Applications](sharing-an-i-o-procedure-with-other-applications.md).</span></span>

 

 




