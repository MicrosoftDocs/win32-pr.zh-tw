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
# <a name="init-method---cpapfile"></a>Init 方法-CPapFile

下列程式碼範例顯示如何初始化 **CPapFile** 。

此範例是 Papfile 中的 **CPapFile** **Init** 方法。


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



*PszAppFileName* 參數是用來針對任何後續的載入或儲存作業，使用預設檔案名來初始化 CPapFile。 第一次載入時，複本會保留在成員 **m \_ szCurFileName** 中。 在 **StoClien** 中，當應用程式第一次在 CPapFile 已使用 *PSZAPPFILENAME* 指派的 StoClien 初始化之後啟動時，就會嘗試這種負載。PAP」。 這個檔案名是在 CGuiPaper 的函式中，藉由取得目前執行中的模組名稱來建立。  (Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) 函式稱為) 。

CPapFile 需要 *pIPaper* 參數，因為它會在 COPaper 物件上使用此介面來執行其載入和儲存作業。 會根據 COM 規則，在此儲存的 *pIPaper* 複本上呼叫 **AddRef** 。 在 CPapFile 的函式中呼叫相符的 **版本** 。

 

 