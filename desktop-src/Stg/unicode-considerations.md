---
title: Unicode 考慮
description: IPaper Save 方法中使用的 WriteFmtUserTypeStg 服務函數需要 Unicode 字串參數。
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840059"
---
# <a name="unicode-considerations"></a><span data-ttu-id="8fef0-103">Unicode 考慮</span><span class="sxs-lookup"><span data-stu-id="8fef0-103">Unicode Considerations</span></span>

<span data-ttu-id="8fef0-104">在 [**IPaper：： Save**](ipaper--save.md)方法中使用的 **WriteFmtUserTypeStg** 服務函數需要 Unicode 字串參數。</span><span class="sxs-lookup"><span data-stu-id="8fef0-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="8fef0-105">這是採用字串參數的 COM/OLE 服務呼叫所使用的情況。</span><span class="sxs-lookup"><span data-stu-id="8fef0-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="8fef0-106">針對 ANSI 字串進行編譯時，預期的 Unicode 參數需要從 ANSI 轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="8fef0-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="8fef0-107">您可以使用 APPUTIL 中的某些宏來達成此程式，這可能會隱匿轉換。</span><span class="sxs-lookup"><span data-stu-id="8fef0-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="8fef0-108">例如，請參閱 **WriteFmtUserTypeStg**。</span><span class="sxs-lookup"><span data-stu-id="8fef0-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="8fef0-109">下列呼叫會出現在 [**Save**](ipaper--save.md) 方法中。</span><span class="sxs-lookup"><span data-stu-id="8fef0-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="8fef0-110">當針對 ANSI (而不是針對 Unicode) 編譯 **StoServe** 時，此呼叫實際上會減少為內部 APPUTIL 代理函數的呼叫。</span><span class="sxs-lookup"><span data-stu-id="8fef0-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="8fef0-111">為了支援此功能，會在 Apputil 中使用下列宏配置，這是所有程式碼範例中包含的檔案。.CPP 檔案。</span><span class="sxs-lookup"><span data-stu-id="8fef0-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="8fef0-112">配置會使用代理服務呼叫函式。</span><span class="sxs-lookup"><span data-stu-id="8fef0-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="8fef0-113">ANSI 版本的呼叫以 A 為開頭 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8fef0-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="8fef0-114">這些代理的 ANSI 函數會在 Apputil 中執行。</span><span class="sxs-lookup"><span data-stu-id="8fef0-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="8fef0-115">當針對 ANSI 字串編譯器代碼範例時，會使用這些值， (makefile) 中的預設值。</span><span class="sxs-lookup"><span data-stu-id="8fef0-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="8fef0-116">代理程式所取代的服務函式只支援 Unicode 字串參數。</span><span class="sxs-lookup"><span data-stu-id="8fef0-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="8fef0-117">這會強制將某些字串從 ANSI 轉換成 Unicode，然後才在代理內進行實際的 COM/OLE 服務呼叫。</span><span class="sxs-lookup"><span data-stu-id="8fef0-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="8fef0-118">例如，如果在編譯期間未定義 UNICODE，則宏實際上會將範例中的任何呼叫 **WriteFmtUserTypeStg** COM 服務函式變更為 WriteFmtUserTypeStg 函式 \_ 的呼叫，該函數會在 APPUTIL 中執行。Cpp。</span><span class="sxs-lookup"><span data-stu-id="8fef0-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="8fef0-119">此函式會接受輸入 ANSI 字串指標、將其轉換為 Unicode 複本，並在實際 **WriteFmtUserTypeStg** 函式的呼叫中，將該 Unicode 複本傳遞為字串參數。</span><span class="sxs-lookup"><span data-stu-id="8fef0-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="8fef0-120">以下是 \_ Apputil 中的 WriteFmtUserTypeStg。</span><span class="sxs-lookup"><span data-stu-id="8fef0-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

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

 

 




