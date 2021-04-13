---
title: 搜尋檔案中的新位置
description: 搜尋檔案中的新位置
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- 多媒體檔案 i/o，移至檔案開頭
- 檔案 i/o，移至檔案開頭
- 輸入和輸出 (i/o) ，移至檔案開頭
- I/o (輸入和輸出) ，移至檔案開頭
- 移至 i/o 檔案的開頭
- 多媒體檔案 i/o，搜尋檔案中的新位置
- 檔案 i/o，搜尋檔案中的新位置
- 輸入和輸出 (i/o) ，以搜尋檔案中的新位置
- I/o (輸入和輸出) ，搜尋檔案中的新位置
- 搜尋 i/o 檔案中的新位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314671"
---
# <a name="seeking-to-a-new-position-in-a-file"></a><span data-ttu-id="79cd8-113">搜尋檔案中的新位置</span><span class="sxs-lookup"><span data-stu-id="79cd8-113">Seeking to a New Position in a File</span></span>

<span data-ttu-id="79cd8-114">下列範例會使用 [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) 函數，移至開啟檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="79cd8-114">The following example moves to the beginning of an open file using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



<span data-ttu-id="79cd8-115">下列範例會移至開啟檔案的結尾。</span><span class="sxs-lookup"><span data-stu-id="79cd8-115">The following example moves to the end of an open file.</span></span>


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



<span data-ttu-id="79cd8-116">下列範例會從開啟的檔案結尾移至10個位元組的位置。</span><span class="sxs-lookup"><span data-stu-id="79cd8-116">The following example moves to a position 10 bytes from the end of an open file.</span></span>


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 