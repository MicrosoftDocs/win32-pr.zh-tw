---
description: URL 是網際網路上資源的位置和存取方法的 compact 標記法。
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: WinHTTP 中)  (Url 的統一資源定位器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026552"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a><span data-ttu-id="f3fa6-103">WinHTTP 中)  (Url 的統一資源定位器</span><span class="sxs-lookup"><span data-stu-id="f3fa6-103">Uniform Resource Locators (URLs) in WinHTTP</span></span>

<span data-ttu-id="f3fa6-104">URL 是網際網路上資源的位置和存取方法的 compact 標記法。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-104">A URL is a compact representation of the location and access method for a resource located on the Internet.</span></span> <span data-ttu-id="f3fa6-105">每個 URL 都是由 (HTTP、HTTPS、FTP 或 Gopher) 的配置，以及配置特定的字串所組成。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-105">Each URL consists of a scheme (HTTP, HTTPS, FTP, or Gopher) and a scheme-specific string.</span></span> <span data-ttu-id="f3fa6-106">這個字串也可以包含目錄路徑、搜尋字串或資源名稱的組合。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-106">This string can also include a combination of a directory path, search string, or name of the resource.</span></span> <span data-ttu-id="f3fa6-107">Microsoft Windows HTTP Services (WinHTTP) 函數可讓您建立、合併、細分和標準化 Url。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-107">The Microsoft Windows HTTP Services (WinHTTP) functions provide the ability to create, combine, break down, and canonicalize URLs.</span></span> <span data-ttu-id="f3fa6-108">如需詳細資訊，請參閱 [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt)、 [統一資源定位器](https://www.ietf.org/rfc/rfc1738.txt) 和 [Rfc 2396](https://www.ietf.org/rfc/rfc2396.txt)、 [統一資源識別項 (URI) ：泛型語法](https://www.ietf.org/rfc/rfc1738.txt)。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-108">For more information, see [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) and [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (URI): Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).</span></span>

## <a name="what-is-a-canonicalized-url"></a><span data-ttu-id="f3fa6-109">什麼是正式的 URL？</span><span class="sxs-lookup"><span data-stu-id="f3fa6-109">What Is a Canonicalized URL?</span></span>

<span data-ttu-id="f3fa6-110">指定的 Url 語法和語法會針對變異數和錯誤留下空間。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-110">The specified syntax and semantics of URLs leaves room for variation and error.</span></span> <span data-ttu-id="f3fa6-111">標準化是將實際的 URL 正規化為正確、標準、「標準」表單的程式。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-111">Canonicalization is the process of normalizing an actual URL into a correct, standard, "canonical" form.</span></span>

<span data-ttu-id="f3fa6-112">這牽涉到將某些字元編碼為「escape 序列」。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-112">This involves coding some characters as "escape sequences."</span></span> <span data-ttu-id="f3fa6-113">英數位元（美國）-ASCII 字元不需要編碼 (數位0-9、大寫字母 A-z 和小寫字母 a-z) 。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-113">Alphanumeric US-ASCII characters need not be encoded (the digits 0-9, the capital letters A-Z, and the lowercase letters a-z).</span></span> <span data-ttu-id="f3fa6-114">大部分其他字元都必須經過轉義，包括控制字元、空白字元、百分比符號、「unsafe 字元」 ( <、>、」、 \# 、{、}、 \| 、 \\ 、^、~、 \[ 、和「 \] ) ，以及具有127以上程式碼點的所有字元。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-114">Most other characters must be escaped, including control characters, the space character, the percent sign, "unsafe characters" ( <, >, ", \#, {, }, \|, \\, ^, ~, \[, \], and ' ), and all characters with a code point above 127.</span></span>

## <a name="using-the-winhttp-functions-to-handle-urls"></a><span data-ttu-id="f3fa6-115">使用 WinHTTP 函數來處理 Url</span><span class="sxs-lookup"><span data-stu-id="f3fa6-115">Using the WinHTTP Functions to Handle URLs</span></span>

<span data-ttu-id="f3fa6-116">WinHTTP 提供兩種處理 Url 的功能。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-116">WinHTTP provides two functions for handling URLs.</span></span> <span data-ttu-id="f3fa6-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 會將 url 分隔成其元件部分，而 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 會從元件建立 url。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-117">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) separates a URL into its component parts, and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) creates a URL from components.</span></span>

### <a name="separating-urls"></a><span data-ttu-id="f3fa6-118">分隔 Url</span><span class="sxs-lookup"><span data-stu-id="f3fa6-118">Separating URLs</span></span>

<span data-ttu-id="f3fa6-119">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)函式會將 url 分隔成其元件元件，並傳回傳遞給函式的 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components)結構所表示的元件。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-119">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function separates a URL into its component parts and returns the components indicated by the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure that is passed to the function.</span></span>

<span data-ttu-id="f3fa6-120">組成 [**URL \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構的元件為配置編號、主機名稱、埠號碼、使用者名稱、密碼、URL 路徑，以及其他資訊，例如搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-120">The components that make up the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure are the scheme number, host name, port number, user name, password, URL path, and additional information such as search parameters.</span></span> <span data-ttu-id="f3fa6-121">除了配置和埠號碼以外，每個元件都有一個字串成員，它會保存資訊和保存字串成員長度的成員。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-121">Each component, except the scheme and port numbers, has a string member that holds the information and a member that holds the length of the string member.</span></span> <span data-ttu-id="f3fa6-122">配置和埠號碼只有儲存對應值的成員;所有成功呼叫 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)時，都會傳回配置和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-122">The scheme and port numbers have only a member that stores the corresponding value; both the scheme and port numbers are returned on all successful calls to [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).</span></span>

<span data-ttu-id="f3fa6-123">若要在 [**URL \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構中取出特定元件的值，儲存該元件之字串長度的成員必須設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-123">To retrieve the value of a particular component in the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure, the member that stores the string length of that component must be set to a nonzero value.</span></span> <span data-ttu-id="f3fa6-124">字串成員可以是緩衝區的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-124">The string member can be either a pointer to a buffer or **NULL**.</span></span>

<span data-ttu-id="f3fa6-125">如果指標成員包含指向緩衝區的指標，則字串長度成員必須包含該緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-125">If the pointer member contains a pointer to a buffer, the string length member must contain the size of that buffer.</span></span> <span data-ttu-id="f3fa6-126">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)函式會傳回元件資訊做為緩衝區中的字串，並將字串長度儲存在字串長度成員中。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-126">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function returns the component information as a string in the buffer and stores the string length in the string length member.</span></span>

<span data-ttu-id="f3fa6-127">如果指標成員設為 **Null**，則字串長度成員可以設定為任何非零值。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-127">If the pointer member is set to **NULL**, the string length member can be set to any nonzero value.</span></span> <span data-ttu-id="f3fa6-128">[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)函式會儲存 url 字串中包含元件資訊之第一個字元的指標，並將字串長度設定為與元件相關之 url 字串其餘部分中的字元數。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-128">The [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) function stores a pointer to the first character of the URL string that contains the component information and sets the string length to the number of characters in the remaining part of the URL string that pertains to the component.</span></span>

<span data-ttu-id="f3fa6-129">所有的指標成員都會設定為 **Null** ，並將非零長度的成員指向 URL 字串中的適當起點。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-129">All pointer members set to **NULL** with a nonzero length member point to the appropriate starting point in the URL string.</span></span> <span data-ttu-id="f3fa6-130">長度成員中儲存的長度必須用來判斷個別元件資訊的結尾。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-130">The length stored in the length member must be used to determine the end of the individual component's information.</span></span>

<span data-ttu-id="f3fa6-131">若要正確地完成初始化 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構， **wstructsize** 成員必須設定為 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-131">To finish initializing the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure properly, the **dwStructSize** member must be set to the size of the [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure.</span></span>

### <a name="creating-urls"></a><span data-ttu-id="f3fa6-132">建立 Url</span><span class="sxs-lookup"><span data-stu-id="f3fa6-132">Creating URLs</span></span>

<span data-ttu-id="f3fa6-133">[**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)函數會使用先前所述 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components)結構中的資訊來建立 url。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-133">The [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) function uses the information in the previously described [**URL\_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components) structure to create a URL.</span></span>

<span data-ttu-id="f3fa6-134">針對每個必要元件，指標成員應該包含保存資訊之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-134">For each required component, the pointer member should contain a pointer to the buffer that holds the information.</span></span> <span data-ttu-id="f3fa6-135">如果指標成員包含以零結尾的字串指標，則長度成員應設為零。如果指標成員包含非以零終止之字串的指標，則長度成員應設定為字串長度。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-135">The length member should be set to zero if the pointer member contains a pointer to a zero-terminated string; the length member should be set to the string length if the pointer member contains a pointer to a string that is not zero-terminated.</span></span> <span data-ttu-id="f3fa6-136">任何不需要的元件之指標成員都必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-136">The pointer member of any components that are not required must be set to **NULL**.</span></span>

### <a name="sample-code"></a><span data-ttu-id="f3fa6-137">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="f3fa6-137">Sample code</span></span>

<span data-ttu-id="f3fa6-138">下列範例程式碼示範如何使用 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 和 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 來拆解現有的 URL、修改其中一個元件，然後將它重新組合成新的 url。</span><span class="sxs-lookup"><span data-stu-id="f3fa6-138">The following sample code shows how to use the [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) and [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) to disassemble an existing URL, modify one of its components, and reassemble it into a new URL.</span></span>


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



