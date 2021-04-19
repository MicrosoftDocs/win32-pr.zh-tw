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
# <a name="reading-and-writing-from-a-file-view"></a>從檔案視圖讀取和寫入

若要從檔案視圖讀取，請取值 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 函式所傳回的指標，如下列範例所示。

讀取或寫入分頁檔案以外的檔案檔案視圖，可能會導致 **\_ \_ 頁面 \_ 錯誤** 例外狀況發生例外狀況。 例如，如果與伺服器的連接遺失，存取位於遠端伺服器上的對應檔案可能會產生例外狀況。 發生例外狀況的原因也可能是因為磁片已滿、基礎裝置失敗或記憶體配置失敗。 寫入檔案時，也會發生例外狀況，因為檔案是共用的，且不同的進程已鎖定位元組範圍。 為了防止由於輸入和輸出 (i/o) 錯誤所造成的例外狀況，所有存取記憶體對應檔案的嘗試都應該包裝在結構化例外狀況處理常式中。 當您在 [篩選準則] 的 [ **\_ \_** **\_ \_ \_ 錯誤] 頁面** 中收到例外狀況時，請確定該位址位於您目前所存取的對應中。 如果是，請以正常的復原或失敗;否則，請勿處理例外狀況。

下列範例會使用 **MapViewOfFile** 所傳回的指標，從檔案視圖讀取：


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



下列範例會使用 **MapViewOfFile** 所傳回的指標寫入檔案視圖：


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



[**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile)函式會將檔案視圖的指定位元組數目複製到實體檔案中，而不需要等候快取的寫入作業：


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



如果您要在 NTFS 磁碟分割上對應壓縮或稀疏檔案，在檔案的一部分中分頁時，可能會有額外的 i/o 錯誤。 在此情況下，配置的磁碟空間可能不會支援 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 所對應的位址空間。 這是因為稀疏檔案可以有零個區域，而 NTFS 不會配置磁碟空間，而壓縮檔案所佔用的磁碟空間可能會比它所代表的實際資料少。 如果您讀取或寫入部分未受磁碟空間支援的稀疏或壓縮檔案，作業系統可能會嘗試配置磁碟空間。 如果磁片已滿，這可能會導致例外狀況，指出 i/o 錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[結構化例外狀況處理](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
