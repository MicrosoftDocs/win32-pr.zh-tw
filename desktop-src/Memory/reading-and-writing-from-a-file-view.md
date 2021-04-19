---
description: 若要從檔案視圖讀取，請取值 MapViewOfFile 函式所傳回的指標，如下列範例所示。
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: 從檔案視圖讀取和寫入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971652"
---
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="4cc91-103">從檔案視圖讀取和寫入</span><span class="sxs-lookup"><span data-stu-id="4cc91-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="4cc91-104">若要從檔案視圖讀取，請取值 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 函式所傳回的指標，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="4cc91-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="4cc91-105">讀取或寫入分頁檔案以外的檔案檔案視圖，可能會導致 **\_ \_ 頁面 \_ 錯誤** 例外狀況發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4cc91-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="4cc91-106">例如，如果與伺服器的連接遺失，存取位於遠端伺服器上的對應檔案可能會產生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4cc91-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="4cc91-107">發生例外狀況的原因也可能是因為磁片已滿、基礎裝置失敗或記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="4cc91-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="4cc91-108">寫入檔案時，也會發生例外狀況，因為檔案是共用的，且不同的進程已鎖定位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="4cc91-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="4cc91-109">為了防止由於輸入和輸出 (i/o) 錯誤所造成的例外狀況，所有存取記憶體對應檔案的嘗試都應該包裝在結構化例外狀況處理常式中。</span><span class="sxs-lookup"><span data-stu-id="4cc91-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="4cc91-110">當您在 [篩選準則] 的 [ **\_ \_** **\_ \_ \_ 錯誤] 頁面** 中收到例外狀況時，請確定該位址位於您目前所存取的對應中。</span><span class="sxs-lookup"><span data-stu-id="4cc91-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="4cc91-111">如果是，請以正常的復原或失敗;否則，請勿處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4cc91-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="4cc91-112">下列範例會使用 **MapViewOfFile** 所傳回的指標，從檔案視圖讀取：</span><span class="sxs-lookup"><span data-stu-id="4cc91-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



<span data-ttu-id="4cc91-113">下列範例會使用 **MapViewOfFile** 所傳回的指標寫入檔案視圖：</span><span class="sxs-lookup"><span data-stu-id="4cc91-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



<span data-ttu-id="4cc91-114">[**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile)函式會將檔案視圖的指定位元組數目複製到實體檔案中，而不需要等候快取的寫入作業：</span><span class="sxs-lookup"><span data-stu-id="4cc91-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="4cc91-115">如果您要在 NTFS 磁碟分割上對應壓縮或稀疏檔案，在檔案的一部分中分頁時，可能會有額外的 i/o 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cc91-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="4cc91-116">在此情況下，配置的磁碟空間可能不會支援 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 所對應的位址空間。</span><span class="sxs-lookup"><span data-stu-id="4cc91-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="4cc91-117">這是因為稀疏檔案可以有零個區域，而 NTFS 不會配置磁碟空間，而壓縮檔案所佔用的磁碟空間可能會比它所代表的實際資料少。</span><span class="sxs-lookup"><span data-stu-id="4cc91-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="4cc91-118">如果您讀取或寫入部分未受磁碟空間支援的稀疏或壓縮檔案，作業系統可能會嘗試配置磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="4cc91-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="4cc91-119">如果磁片已滿，這可能會導致例外狀況，指出 i/o 錯誤。</span><span class="sxs-lookup"><span data-stu-id="4cc91-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cc91-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cc91-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc91-121">結構化例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="4cc91-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
