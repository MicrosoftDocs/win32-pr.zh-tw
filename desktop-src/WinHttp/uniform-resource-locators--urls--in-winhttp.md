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
# <a name="uniform-resource-locators-urls-in-winhttp"></a>WinHTTP 中)  (Url 的統一資源定位器

URL 是網際網路上資源的位置和存取方法的 compact 標記法。 每個 URL 都是由 (HTTP、HTTPS、FTP 或 Gopher) 的配置，以及配置特定的字串所組成。 這個字串也可以包含目錄路徑、搜尋字串或資源名稱的組合。 Microsoft Windows HTTP Services (WinHTTP) 函數可讓您建立、合併、細分和標準化 Url。 如需詳細資訊，請參閱 [RFC 1738](https://www.ietf.org/rfc/rfc1738.txt)、 [統一資源定位器](https://www.ietf.org/rfc/rfc1738.txt) 和 [Rfc 2396](https://www.ietf.org/rfc/rfc2396.txt)、 [統一資源識別項 (URI) ：泛型語法](https://www.ietf.org/rfc/rfc1738.txt)。

## <a name="what-is-a-canonicalized-url"></a>什麼是正式的 URL？

指定的 Url 語法和語法會針對變異數和錯誤留下空間。 標準化是將實際的 URL 正規化為正確、標準、「標準」表單的程式。

這牽涉到將某些字元編碼為「escape 序列」。 英數位元（美國）-ASCII 字元不需要編碼 (數位0-9、大寫字母 A-z 和小寫字母 a-z) 。 大部分其他字元都必須經過轉義，包括控制字元、空白字元、百分比符號、「unsafe 字元」 ( <、>、」、 \# 、{、}、 \| 、 \\ 、^、~、 \[ 、和「 \] ) ，以及具有127以上程式碼點的所有字元。

## <a name="using-the-winhttp-functions-to-handle-urls"></a>使用 WinHTTP 函數來處理 Url

WinHTTP 提供兩種處理 Url 的功能。 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 會將 url 分隔成其元件部分，而 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 會從元件建立 url。

### <a name="separating-urls"></a>分隔 Url

[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)函式會將 url 分隔成其元件元件，並傳回傳遞給函式的 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components)結構所表示的元件。

組成 [**URL \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構的元件為配置編號、主機名稱、埠號碼、使用者名稱、密碼、URL 路徑，以及其他資訊，例如搜尋參數。 除了配置和埠號碼以外，每個元件都有一個字串成員，它會保存資訊和保存字串成員長度的成員。 配置和埠號碼只有儲存對應值的成員;所有成功呼叫 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)時，都會傳回配置和埠號碼。

若要在 [**URL \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構中取出特定元件的值，儲存該元件之字串長度的成員必須設定為非零值。 字串成員可以是緩衝區的指標或 **Null**。

如果指標成員包含指向緩衝區的指標，則字串長度成員必須包含該緩衝區的大小。 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)函式會傳回元件資訊做為緩衝區中的字串，並將字串長度儲存在字串長度成員中。

如果指標成員設為 **Null**，則字串長度成員可以設定為任何非零值。 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)函式會儲存 url 字串中包含元件資訊之第一個字元的指標，並將字串長度設定為與元件相關之 url 字串其餘部分中的字元數。

所有的指標成員都會設定為 **Null** ，並將非零長度的成員指向 URL 字串中的適當起點。 長度成員中儲存的長度必須用來判斷個別元件資訊的結尾。

若要正確地完成初始化 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構， **wstructsize** 成員必須設定為 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components) 結構的大小。

### <a name="creating-urls"></a>建立 Url

[**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)函數會使用先前所述 [**url \_ 元件**](/windows/win32/api/winhttp/ns-winhttp-url_components)結構中的資訊來建立 url。

針對每個必要元件，指標成員應該包含保存資訊之緩衝區的指標。 如果指標成員包含以零結尾的字串指標，則長度成員應設為零。如果指標成員包含非以零終止之字串的指標，則長度成員應設定為字串長度。 任何不需要的元件之指標成員都必須設定為 **Null**。

### <a name="sample-code"></a>範例程式碼

下列範例程式碼示範如何使用 [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) 和 [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) 來拆解現有的 URL、修改其中一個元件，然後將它重新組合成新的 url。


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



 

 



