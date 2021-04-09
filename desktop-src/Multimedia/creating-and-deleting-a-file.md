---
title: 建立和刪除檔案
description: 建立和刪除檔案
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- 多媒體檔案 i/o，建立檔案
- 檔案 i/o，建立檔案
- 輸入和輸出 (i/o) ，建立檔案
- I/o (輸入和輸出) ，建立檔案
- 建立 i/o 檔案
- 多媒體檔案 i/o，刪除檔案
- 檔案 i/o，刪除檔案
- 輸入和輸出 (i/o) ，刪除檔案
- I/o (輸入和輸出) ，刪除檔案
- 刪除 i/o 檔案
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681875"
---
# <a name="creating-and-deleting-a-file"></a><span data-ttu-id="d0a25-114">建立和刪除檔案</span><span class="sxs-lookup"><span data-stu-id="d0a25-114">Creating and Deleting a File</span></span>

<span data-ttu-id="d0a25-115">若要建立檔案，請將 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)函數的 *dwOpenFlags* 參數設定為 MMIO \_ create。</span><span class="sxs-lookup"><span data-stu-id="d0a25-115">To create a file, set the *dwOpenFlags* parameter of the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to MMIO\_CREATE.</span></span> <span data-ttu-id="d0a25-116">下列範例會建立檔案，並將它開啟以供讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="d0a25-116">The following example creates a file and opens it for reading and writing.</span></span>


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



<span data-ttu-id="d0a25-117">如果您要建立的檔案已經存在，則會截斷為零長度。</span><span class="sxs-lookup"><span data-stu-id="d0a25-117">If the file you are creating already exists, it will be truncated to zero length.</span></span>

<span data-ttu-id="d0a25-118">若要刪除檔案，請將 **mmioOpen** 函數的 *dwOpenFlags* 參數設定為 MMIO \_ delete。</span><span class="sxs-lookup"><span data-stu-id="d0a25-118">To delete a file, set the *dwOpenFlags* parameter of the **mmioOpen** function to MMIO\_DELETE.</span></span> <span data-ttu-id="d0a25-119">當您刪除檔案之後，就無法以任何標準方法復原。</span><span class="sxs-lookup"><span data-stu-id="d0a25-119">After you delete a file, it cannot be recovered by any standard means.</span></span> <span data-ttu-id="d0a25-120">如果您的應用程式在使用者要求時刪除檔案，請在刪除該檔案之前先查詢使用者，以確定使用者想要刪除它。</span><span class="sxs-lookup"><span data-stu-id="d0a25-120">If your application is deleting a file at the request of a user, query the user before deleting the file to make sure the user wants to delete it.</span></span>

 

 