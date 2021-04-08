---
title: 儲存方法-CPapFile
description: 當 CPapFile 初始化時，它可以用來儲存 COPaper 物件中所保留的目前繪圖資料。
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- 儲存方法-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932592"
---
# <a name="save-method---cpapfile"></a>儲存方法-CPapFile

當 **CPapFile** 初始化時，它可以用來儲存 COPaper 物件中所保留的目前繪圖資料。

## <a name="save-method-papfilecpp"></a>將方法儲存 (PAPFILE。CPP) 

此範例是 Papfile 中的 **CPapFile** [**Save**](ipaper--save.md) 方法。


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



如果針對 *>pszfilename* 參數傳遞 **Null** ，則會使用成員 **m \_ szCurFileName** 的儲存內容作為檔案名。 *NLockKey* 是在上一次呼叫 **IPaper** 介面中的 COPaper [**鎖定**](ipaper-methods.md)方法時所取得的用戶端鎖定金鑰。

系統會呼叫 COM 標準 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 服務函數，以建立將儲存繪圖資料的複合檔案。

要建立的複合檔案名稱會當作第一個參數傳遞。 這是 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 所預期的 Unicode 字串。 針對 ANSI 字串編譯 **StoClien** 時 (不會定義 UNICODE （makefile) 中的預設值），此呼叫實際上會減少為內部 APPUTIL 函數（ **\_ StgCreateDocfile**）的呼叫。 這個函式會在呼叫 **StgCreateDocfile** 之前，先執行 ANSI pszFile 參數至 Unicode 版本的正確轉換。 如需詳細資訊，請參閱 Apputil .h 和 Stoserve.htm。

存取模式旗標會以第二個參數的形式傳遞，並決定要在新檔案上允許的存取模式。 [STGM \_ CREATE](stgm-constants.md) access mode 旗標會建立新的複合檔案，或覆寫現有的相同名稱。 [STGM \_READWRITE](stgm-constants.md) 開啟具有讀寫許可權的檔案。 [STGM \_直接](stgm-constants.md) 開啟檔案以供直接存取，而非交易存取。 [STGM \_共用 \_ 獨佔](stgm-constants.md) 會開啟檔案，以供呼叫端獨佔、非共用使用。

第三個參數是保留的，而且必須為零。

指標變數 **m \_ pIStorage** 的位址會傳遞至 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 做為第四個參數。 當呼叫成功傳回時， **m \_ pIStorage** 會包含 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的介面指標。 這是用於檔案上任何後續作業的介面。

在此情況下，重要的作業是讓 COPaper 物件將其繪製資料儲存在檔案中。 這是使用 COPaper [**IPaper**](ipaper-methods.md)介面的 [**Save**](ipaper--save.md)方法來完成。 如果 COPaper 成功將其資料儲存在提供的儲存物件中，則會將複合檔案的名稱複製到 **m \_ szCurFileName** 中，做為新的目前檔案名。

 

 




