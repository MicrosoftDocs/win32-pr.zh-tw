---
title: Unicode 考慮
description: IPaper Save 方法中使用的 WriteFmtUserTypeStg 服務函數需要 Unicode 字串參數。
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06f8fa9592d3f29ccf82d42f38a48b2dc57d36bccf79b22b8fe159bad337cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886736"
---
# <a name="unicode-considerations"></a>Unicode 考慮

在 [**IPaper：： Save**](ipaper--save.md)方法中使用的 **WriteFmtUserTypeStg** 服務函數需要 Unicode 字串參數。 這是採用字串參數的 COM/OLE 服務呼叫所使用的情況。 針對 ANSI 字串進行編譯時，預期的 Unicode 參數需要從 ANSI 轉換成 Unicode。 您可以使用 APPUTIL 中的某些宏來達成此程式，這可能會隱匿轉換。 例如，請參閱 **WriteFmtUserTypeStg**。

下列呼叫會出現在 [**Save**](ipaper--save.md) 方法中。


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



當針對 ANSI (而不是針對 Unicode) 編譯 **StoServe** 時，此呼叫實際上會減少為內部 APPUTIL 代理函數的呼叫。 為了支援此功能，會在 Apputil 中使用下列宏配置，這是所有程式碼範例中包含的檔案。.CPP 檔案。


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



配置會使用代理服務呼叫函式。 ANSI 版本的呼叫以 A 為開頭 \_ 。 這些代理的 ANSI 函數會在 Apputil 中執行。 當針對 ANSI 字串編譯器代碼範例時，會使用這些值， (makefile) 中的預設值。 代理程式所取代的服務函式只支援 Unicode 字串參數。 這會強制將某些字串從 ANSI 轉換成 Unicode，然後才在代理內進行實際的 COM/OLE 服務呼叫。

例如，如果在編譯期間未定義 UNICODE，則宏實際上會將範例中的任何呼叫 **WriteFmtUserTypeStg** COM 服務函式變更為 WriteFmtUserTypeStg 函式 \_ 的呼叫，該函數會在 APPUTIL 中執行。CPP。 此函式會接受輸入 ANSI 字串指標、將其轉換為 Unicode 複本，並在實際 **WriteFmtUserTypeStg** 函式的呼叫中，將該 Unicode 複本傳遞為字串參數。

以下是 \_ Apputil 中的 WriteFmtUserTypeStg。

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




