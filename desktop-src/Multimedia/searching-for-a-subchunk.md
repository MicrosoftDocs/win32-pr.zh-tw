---
title: 搜尋 Subchunk
description: 搜尋 Subchunk
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- 多媒體檔案 i/o，搜尋 RIFF 區塊
- 檔案 i/o，搜尋 RIFF 區塊
- 輸入和輸出 (i/o) ，搜尋 RIFF 區塊
- I/o (輸入和輸出) ，搜尋 RIFF 區塊
- 搜尋 RIFF 區塊
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315112"
---
# <a name="searching-for-a-subchunk"></a><span data-ttu-id="8e4e7-112">搜尋 Subchunk</span><span class="sxs-lookup"><span data-stu-id="8e4e7-112">Searching for a Subchunk</span></span>

<span data-ttu-id="8e4e7-113">下列範例會使用 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) 函數來搜尋先前範例 "RIFF" 區塊中的 "bcp.fmt" 區塊。</span><span class="sxs-lookup"><span data-stu-id="8e4e7-113">The following example uses the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function to search for the "FMT" chunk in the "RIFF" chunk of the previous example.</span></span>


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



<span data-ttu-id="8e4e7-114">若要搜尋 subchunk (也就是 "RIFF" 或 "LIST" 區塊以外的任何區塊) ，請在 [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)函數的 *lpckParent* 參數中識別其父區塊。</span><span class="sxs-lookup"><span data-stu-id="8e4e7-114">To search for a subchunk (that is, any chunk other than a "RIFF" or "LIST" chunk), identify its parent chunk in the *lpckParent* parameter of the [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) function.</span></span>

<span data-ttu-id="8e4e7-115">如果您未指定父區塊，則在呼叫 **mmioDescend** 函式之前，目前的檔案位置應該在區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="8e4e7-115">If you do not specify a parent chunk, the current file position should be at the beginning of a chunk before you call the **mmioDescend** function.</span></span> <span data-ttu-id="8e4e7-116">如果您指定了父區塊，則目前的檔案位置可以是該區塊中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="8e4e7-116">If you do specify a parent chunk, the current file position can be anywhere in that chunk.</span></span>

<span data-ttu-id="8e4e7-117">如果搜尋 subchunk 失敗，則表示目前的檔案位置是未定義的。</span><span class="sxs-lookup"><span data-stu-id="8e4e7-117">If the search for a subchunk fails, the current file position is undefined.</span></span> <span data-ttu-id="8e4e7-118">您可以使用 [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)函式和 [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)結構的 **dwDataOffset** 成員來描述父區塊，以向後搜尋至父區塊的開頭，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="8e4e7-118">You can use the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function and the **dwDataOffset** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure describing the parent chunk to seek back to the beginning of the parent chunk, as in the following example:</span></span>


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



<span data-ttu-id="8e4e7-119">因為 **dwDataOffset** 指定了區塊資料部分開頭的位移，所以您必須搜尋4位元組之前的 **dwDataOffset** ，以設定表單類型之後的檔案位置。</span><span class="sxs-lookup"><span data-stu-id="8e4e7-119">Because **dwDataOffset** specifies the offset to the beginning of the data portion of the chunk, you must seek 4 bytes past **dwDataOffset** to set the file position after the form type.</span></span>

 

 