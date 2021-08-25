---
title: Load 方法-CPapFile
description: 當這些作業成功時，便會釋放取得的 IStorage 介面。 這會關閉檔案，並指出在其他用戶端操作期間，檔案未保持開啟狀態。 它會在需要時重新開啟。
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Load 方法-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49eac23bcb79738a30b18eb87a4d8ef4598aba89de0748c58b433df28d614886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034888"
---
# <a name="load-method---cpapfile"></a>Load 方法-CPapFile

當這些作業成功時，便會釋放取得的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。 這會關閉檔案，並指出在其他用戶端操作期間，檔案未保持開啟狀態。 它會在需要時重新開啟。

這個範例是來自 Papfile 的 **CPapFile** **Load** 方法。


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a>備註

如同 [**Save**](save-method---cpapfile.md)方法，如果針對 *>pszfilename* 參數傳遞 **Null** ，則會使用成員 **m \_ szCurFileName** 的儲存內容作為檔案名。 因為可以開啟現有的檔案，所以會先使用 APPUTIL **FileExist** 函式來確認檔案是否存在。 如果存在，則會呼叫標準 [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) 服務函數來確認檔案的格式，以判斷它是否為有效的複合檔案。

如果檔案是有效的，則會呼叫標準 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) 服務函式來開啟檔案，並將指標傳回給它的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。

第一個參數是要開啟的複合檔案名稱。 如同 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 呼叫，此字串必須是 Unicode 格式，而且在 ANSI 編譯期間，會使用 APPUTIL 宏來確保 ansi 參數轉換為預期的 Unicode。

第二個優先權儲存體參數為 **Null**，表示未在此範例中使用。

存取模式旗標會以第三個參數的形式傳遞，以指定要在開啟的檔案上允許哪些存取模式。 [**STGM \_READ**](stgm-constants.md) 會開啟具有唯讀許可權的檔案。 [**STGM \_直接**](stgm-constants.md) 開啟檔案以供直接存取，而非交易存取。 [**STGM \_共用 \_ 獨佔**](stgm-constants.md) 會開啟檔案，以供呼叫端獨佔、非共用使用。

第四個元素排除參數 **為 Null**，表示未在此範例中使用。

第五個參數保留供日後使用，且必須為零。

指標變數 **m \_ pIStorage** 的位址會做為第六個參數傳遞。 當呼叫成功傳回時， **m \_ pIStorage** 會包含 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的指標。 這是針對開啟之檔案的任何後續作業所使用的介面。

在此情況下，重要的作業是讓 COPaper 物件從檔案載入其繪製資料。 這是使用 COPaper 的 [**IPaper**](ipaper-methods.md)介面 **Load** 方法來完成。 如果 COPaper 在使用提供的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 載入其資料時成功，則會將複合檔案的名稱複製到 **m \_ szCurFileName** 中，做為新的目前檔案名。

當這些作業成功完成時，就會釋放已取得的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。 這會關閉檔案，表示檔案在其他用戶端作業期間不會保持開啟。 它會在需要時重新開啟。

 

 




