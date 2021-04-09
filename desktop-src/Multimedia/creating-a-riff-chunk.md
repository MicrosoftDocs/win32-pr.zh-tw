---
title: 建立 RIFF 區塊
description: 建立 RIFF 區塊
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- 多媒體檔案 i/o，建立 RIFF 區塊
- 檔案 i/o，建立 RIFF 區塊
- 輸入和輸出 (i/o) ，建立 RIFF 區塊
- I/o (輸入和輸出) ，建立 RIFF 區塊
- 建立 RIFF 區塊
- mmioCreateChunk 函式
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
- RIFF 區塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842195"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="03630-113">建立 RIFF 區塊</span><span class="sxs-lookup"><span data-stu-id="03630-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="03630-114">下列範例會使用 [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) 函式來建立區塊識別碼為 "RIFF" 且表單類型為 "RDIB" 的區塊。</span><span class="sxs-lookup"><span data-stu-id="03630-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="03630-115">如果您要建立 "RIFF" 或 "LIST" 區塊，則必須在 [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)結構的 **fccType** 成員中指定表單類型或清單類型。</span><span class="sxs-lookup"><span data-stu-id="03630-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="03630-116">在上述範例中，"RDIB" 是表單類型。</span><span class="sxs-lookup"><span data-stu-id="03630-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="03630-117">如果您知道資料欄位在新的區塊中的大小，您可以在建立區塊時，設定 **MMCKINFO** 結構的 **cksize** 成員。</span><span class="sxs-lookup"><span data-stu-id="03630-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="03630-118">此值將會寫入新區塊中的資料大小欄位。</span><span class="sxs-lookup"><span data-stu-id="03630-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="03630-119">當您呼叫 [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) 來標示區塊結尾時，如果此值不正確，則會自動重寫該值，以反映資料欄位的正確大小。</span><span class="sxs-lookup"><span data-stu-id="03630-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="03630-120">使用 [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) 函式建立區塊之後，檔案位置會設定為區塊的資料欄位， (從區塊開頭算起的8個位元組) 。</span><span class="sxs-lookup"><span data-stu-id="03630-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="03630-121">如果區塊是 "RIFF" 或 "LIST" 區塊，則檔案位置會設定為表單類型或清單類型後面的位置， (從區塊開頭的12個位元組開始) 。</span><span class="sxs-lookup"><span data-stu-id="03630-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 