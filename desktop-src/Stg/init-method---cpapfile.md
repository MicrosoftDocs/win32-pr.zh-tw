---
title: Init 方法-CPapFile
description: 下列程式碼範例顯示如何初始化 CPapFile。
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- Init 方法-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376268"
---
# <a name="init-method---cpapfile"></a><span data-ttu-id="b6268-104">Init 方法-CPapFile</span><span class="sxs-lookup"><span data-stu-id="b6268-104">Init Method - CPapFile</span></span>

<span data-ttu-id="b6268-105">下列程式碼範例顯示如何初始化 **CPapFile** 。</span><span class="sxs-lookup"><span data-stu-id="b6268-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="b6268-106">此範例是 Papfile 中的 **CPapFile** **Init** 方法。</span><span class="sxs-lookup"><span data-stu-id="b6268-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



<span data-ttu-id="b6268-107">*PszAppFileName* 參數是用來針對任何後續的載入或儲存作業，使用預設檔案名來初始化 CPapFile。</span><span class="sxs-lookup"><span data-stu-id="b6268-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="b6268-108">第一次載入時，複本會保留在成員 **m \_ szCurFileName** 中。</span><span class="sxs-lookup"><span data-stu-id="b6268-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="b6268-109">在 **StoClien** 中，當應用程式第一次在 CPapFile 已使用 *PSZAPPFILENAME* 指派的 StoClien 初始化之後啟動時，就會嘗試這種負載。PAP」。</span><span class="sxs-lookup"><span data-stu-id="b6268-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="b6268-110">這個檔案名是在 CGuiPaper 的函式中，藉由取得目前執行中的模組名稱來建立。</span><span class="sxs-lookup"><span data-stu-id="b6268-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="b6268-111"> (Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函式稱為) 。</span><span class="sxs-lookup"><span data-stu-id="b6268-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="b6268-112">CPapFile 需要 *pIPaper* 參數，因為它會在 COPaper 物件上使用此介面來執行其載入和儲存作業。</span><span class="sxs-lookup"><span data-stu-id="b6268-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="b6268-113">會根據 COM 規則，在此儲存的 *pIPaper* 複本上呼叫 **AddRef** 。</span><span class="sxs-lookup"><span data-stu-id="b6268-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="b6268-114">在 CPapFile 的函式中呼叫相符的 **版本** 。</span><span class="sxs-lookup"><span data-stu-id="b6268-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 