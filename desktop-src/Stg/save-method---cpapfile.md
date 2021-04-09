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
# <a name="save-method---cpapfile"></a><span data-ttu-id="977be-104">儲存方法-CPapFile</span><span class="sxs-lookup"><span data-stu-id="977be-104">Save Method - CPapFile</span></span>

<span data-ttu-id="977be-105">當 **CPapFile** 初始化時，它可以用來儲存 COPaper 物件中所保留的目前繪圖資料。</span><span class="sxs-lookup"><span data-stu-id="977be-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="977be-106">將方法儲存 (PAPFILE。CPP) </span><span class="sxs-lookup"><span data-stu-id="977be-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="977be-107">此範例是 Papfile 中的 **CPapFile** [**Save**](ipaper--save.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="977be-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


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



<span data-ttu-id="977be-108">如果針對 *>pszfilename* 參數傳遞 **Null** ，則會使用成員 **m \_ szCurFileName** 的儲存內容作為檔案名。</span><span class="sxs-lookup"><span data-stu-id="977be-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="977be-109">*NLockKey* 是在上一次呼叫 **IPaper** 介面中的 COPaper [**鎖定**](ipaper-methods.md)方法時所取得的用戶端鎖定金鑰。</span><span class="sxs-lookup"><span data-stu-id="977be-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="977be-110">系統會呼叫 COM 標準 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 服務函數，以建立將儲存繪圖資料的複合檔案。</span><span class="sxs-lookup"><span data-stu-id="977be-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="977be-111">要建立的複合檔案名稱會當作第一個參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="977be-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="977be-112">這是 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 所預期的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="977be-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="977be-113">針對 ANSI 字串編譯 **StoClien** 時 (不會定義 UNICODE （makefile) 中的預設值），此呼叫實際上會減少為內部 APPUTIL 函數（ **\_ StgCreateDocfile**）的呼叫。</span><span class="sxs-lookup"><span data-stu-id="977be-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="977be-114">這個函式會在呼叫 **StgCreateDocfile** 之前，先執行 ANSI pszFile 參數至 Unicode 版本的正確轉換。</span><span class="sxs-lookup"><span data-stu-id="977be-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="977be-115">如需詳細資訊，請參閱 Apputil .h 和 Stoserve.htm。</span><span class="sxs-lookup"><span data-stu-id="977be-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="977be-116">存取模式旗標會以第二個參數的形式傳遞，並決定要在新檔案上允許的存取模式。</span><span class="sxs-lookup"><span data-stu-id="977be-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="977be-117">[STGM \_ CREATE](stgm-constants.md) access mode 旗標會建立新的複合檔案，或覆寫現有的相同名稱。</span><span class="sxs-lookup"><span data-stu-id="977be-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="977be-118">[STGM \_READWRITE](stgm-constants.md) 開啟具有讀寫許可權的檔案。</span><span class="sxs-lookup"><span data-stu-id="977be-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="977be-119">[STGM \_直接](stgm-constants.md) 開啟檔案以供直接存取，而非交易存取。</span><span class="sxs-lookup"><span data-stu-id="977be-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="977be-120">[STGM \_共用 \_ 獨佔](stgm-constants.md) 會開啟檔案，以供呼叫端獨佔、非共用使用。</span><span class="sxs-lookup"><span data-stu-id="977be-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="977be-121">第三個參數是保留的，而且必須為零。</span><span class="sxs-lookup"><span data-stu-id="977be-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="977be-122">指標變數 **m \_ pIStorage** 的位址會傳遞至 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 做為第四個參數。</span><span class="sxs-lookup"><span data-stu-id="977be-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="977be-123">當呼叫成功傳回時， **m \_ pIStorage** 會包含 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的介面指標。</span><span class="sxs-lookup"><span data-stu-id="977be-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="977be-124">這是用於檔案上任何後續作業的介面。</span><span class="sxs-lookup"><span data-stu-id="977be-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="977be-125">在此情況下，重要的作業是讓 COPaper 物件將其繪製資料儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="977be-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="977be-126">這是使用 COPaper [**IPaper**](ipaper-methods.md)介面的 [**Save**](ipaper--save.md)方法來完成。</span><span class="sxs-lookup"><span data-stu-id="977be-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="977be-127">如果 COPaper 成功將其資料儲存在提供的儲存物件中，則會將複合檔案的名稱複製到 **m \_ szCurFileName** 中，做為新的目前檔案名。</span><span class="sxs-lookup"><span data-stu-id="977be-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




