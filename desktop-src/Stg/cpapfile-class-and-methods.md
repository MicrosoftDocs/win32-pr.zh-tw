---
title: CPapFile 類別和方法
description: StoClien 會將它的複合檔案作業封裝在 CPapFile c + + 物件中。
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932088"
---
# <a name="cpapfile-class-and-methods"></a><span data-ttu-id="d43f8-103">CPapFile 類別和方法</span><span class="sxs-lookup"><span data-stu-id="d43f8-103">CPapFile Class and Methods</span></span>

<span data-ttu-id="d43f8-104">**StoClien** 會將它的複合檔案作業封裝在 CPapFile c + + 物件中。</span><span class="sxs-lookup"><span data-stu-id="d43f8-104">**StoClien** encapsulates its compound file operations in a CPapFile C++ object.</span></span>

<span data-ttu-id="d43f8-105">以下是來自 Papfile 的 **CPapFile** 類別宣告。</span><span class="sxs-lookup"><span data-stu-id="d43f8-105">The following is the **CPapFile** class declaration from Papfile.h.</span></span>


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



<span data-ttu-id="d43f8-106">CPapFile 物件會在成員 **m \_ szCurFileName** 中保留目前的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d43f8-106">The CPapFile object keeps a current file name in member **m\_szCurFileName**.</span></span> <span data-ttu-id="d43f8-107">當 [**Load**](load-method---cpapfile.md) 和 [**Save**](save-method---cpapfile.md) 方法未明確接收檔案名時，會使用這個檔案名作為預設值。</span><span class="sxs-lookup"><span data-stu-id="d43f8-107">This file name is used as a default in the [**Load**](load-method---cpapfile.md) and [**Save**](save-method---cpapfile.md) methods when they do not explicitly receive a file name.</span></span>

<span data-ttu-id="d43f8-108">成員 **m \_ pIPaper** 會保留 COPaper [**IPaper**](ipaper-methods.md) 介面的介面指標。</span><span class="sxs-lookup"><span data-stu-id="d43f8-108">Member **m\_pIPaper** keeps an interface pointer to the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="d43f8-109">成員 **m \_ pIStorage** 會針對 **StoClien** 用於結構化儲存的目前複合檔案，保留 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d43f8-109">Member **m\_pIStorage** keeps a pointer to the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for the current compound file that **StoClien** is using for structured storage.</span></span>

<span data-ttu-id="d43f8-110">以下是 CPapFile 方法的摘要。</span><span class="sxs-lookup"><span data-stu-id="d43f8-110">The following is a summary of CPapFile's methods.</span></span>


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




