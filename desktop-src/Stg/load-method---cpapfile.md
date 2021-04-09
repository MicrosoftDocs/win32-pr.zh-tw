---
title: Load 方法-CPapFile
description: 當這些作業成功時，便會釋放取得的 IStorage 介面。 這會關閉檔案，並指出在其他用戶端操作期間，檔案未保持開啟狀態。 它會在需要時重新開啟。
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Load 方法-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840888"
---
# <a name="load-method---cpapfile"></a><span data-ttu-id="31fa4-106">Load 方法-CPapFile</span><span class="sxs-lookup"><span data-stu-id="31fa4-106">Load Method - CPapFile</span></span>

<span data-ttu-id="31fa4-107">當這些作業成功時，便會釋放取得的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="31fa4-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="31fa4-108">這會關閉檔案，並指出在其他用戶端操作期間，檔案未保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="31fa4-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="31fa4-109">它會在需要時重新開啟。</span><span class="sxs-lookup"><span data-stu-id="31fa4-109">It will be reopened when required.</span></span>

<span data-ttu-id="31fa4-110">這個範例是來自 Papfile 的 **CPapFile** **Load** 方法。</span><span class="sxs-lookup"><span data-stu-id="31fa4-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


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



### <a name="remarks"></a><span data-ttu-id="31fa4-111">備註</span><span class="sxs-lookup"><span data-stu-id="31fa4-111">Remarks</span></span>

<span data-ttu-id="31fa4-112">如同 [**Save**](save-method---cpapfile.md)方法，如果針對 *>pszfilename* 參數傳遞 **Null** ，則會使用成員 **m \_ szCurFileName** 的儲存內容作為檔案名。</span><span class="sxs-lookup"><span data-stu-id="31fa4-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="31fa4-113">因為可以開啟現有的檔案，所以會先使用 APPUTIL **FileExist** 函式來確認檔案是否存在。</span><span class="sxs-lookup"><span data-stu-id="31fa4-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="31fa4-114">如果存在，則會呼叫標準 [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) 服務函數來確認檔案的格式，以判斷它是否為有效的複合檔案。</span><span class="sxs-lookup"><span data-stu-id="31fa4-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="31fa4-115">如果檔案是有效的，則會呼叫標準 [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) 服務函式來開啟檔案，並將指標傳回給它的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="31fa4-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="31fa4-116">第一個參數是要開啟的複合檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="31fa4-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="31fa4-117">如同 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) 呼叫，此字串必須是 Unicode 格式，而且在 ANSI 編譯期間，會使用 APPUTIL 宏來確保 ansi 參數轉換為預期的 Unicode。</span><span class="sxs-lookup"><span data-stu-id="31fa4-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="31fa4-118">第二個優先權儲存體參數為 **Null**，表示未在此範例中使用。</span><span class="sxs-lookup"><span data-stu-id="31fa4-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="31fa4-119">存取模式旗標會以第三個參數的形式傳遞，以指定要在開啟的檔案上允許哪些存取模式。</span><span class="sxs-lookup"><span data-stu-id="31fa4-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="31fa4-120">[**STGM \_READ**](stgm-constants.md) 會開啟具有唯讀許可權的檔案。</span><span class="sxs-lookup"><span data-stu-id="31fa4-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="31fa4-121">[**STGM \_直接**](stgm-constants.md) 開啟檔案以供直接存取，而非交易存取。</span><span class="sxs-lookup"><span data-stu-id="31fa4-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="31fa4-122">[**STGM \_共用 \_ 獨佔**](stgm-constants.md) 會開啟檔案，以供呼叫端獨佔、非共用使用。</span><span class="sxs-lookup"><span data-stu-id="31fa4-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="31fa4-123">第四個元素排除參數 **為 Null**，表示未在此範例中使用。</span><span class="sxs-lookup"><span data-stu-id="31fa4-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="31fa4-124">第五個參數保留供日後使用，且必須為零。</span><span class="sxs-lookup"><span data-stu-id="31fa4-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="31fa4-125">指標變數 **m \_ pIStorage** 的位址會做為第六個參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="31fa4-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="31fa4-126">當呼叫成功傳回時， **m \_ pIStorage** 會包含 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="31fa4-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="31fa4-127">這是針對開啟之檔案的任何後續作業所使用的介面。</span><span class="sxs-lookup"><span data-stu-id="31fa4-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="31fa4-128">在此情況下，重要的作業是讓 COPaper 物件從檔案載入其繪製資料。</span><span class="sxs-lookup"><span data-stu-id="31fa4-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="31fa4-129">這是使用 COPaper 的 [**IPaper**](ipaper-methods.md)介面 **Load** 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="31fa4-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="31fa4-130">如果 COPaper 在使用提供的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 載入其資料時成功，則會將複合檔案的名稱複製到 **m \_ szCurFileName** 中，做為新的目前檔案名。</span><span class="sxs-lookup"><span data-stu-id="31fa4-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="31fa4-131">當這些作業成功完成時，就會釋放已取得的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="31fa4-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="31fa4-132">這會關閉檔案，表示檔案在其他用戶端作業期間不會保持開啟。</span><span class="sxs-lookup"><span data-stu-id="31fa4-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="31fa4-133">它會在需要時重新開啟。</span><span class="sxs-lookup"><span data-stu-id="31fa4-133">It will be reopened when required.</span></span>

 

 




