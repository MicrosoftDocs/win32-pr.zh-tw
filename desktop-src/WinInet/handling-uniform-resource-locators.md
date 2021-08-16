---
title: 處理統一資源定位器
description: 統一資源定位器 (URL) 是網際網路上資源的位置和存取方法的 compact 表示。
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419433c8a06b6243bf048896664a67da31a3c58d1d79eb6fea65f9fc99dbe63a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121868"
---
# <a name="handling-uniform-resource-locators"></a>處理統一資源定位器

統一資源定位器 (URL) 是網際網路上資源的位置和存取方法的 compact 表示。 每個 URL 都是由 (HTTP、HTTPS 或 FTP) 的配置以及配置特定的字串所組成。 這個字串也可以包含目錄路徑、搜尋字串或資源名稱的組合。 WinINet 函數可讓您建立、合併、細分和正常化 Url。 如需 Url 的詳細資訊，請參閱統一資源定位器上的 [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) (URL) 。

URL 函數會以工作導向的方式運作。 未驗證為函式提供的 URL 內容和格式。 呼叫應用程式應該追蹤這些函式的使用方式，以確保資料採用預期的格式。 例如，使用沒有旗標時， [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 函數會將字元 "%" 轉換成 escape 序列 "%25"。 如果在正式 URL 上使用 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) ，則會將 escape 序列 "%25" 轉換成 escape 序列 "%2525"，這將無法正常運作。

-   [什麼是正式的 URL？](#what-is-a-canonicalized-url)
-   [使用 WinINet 函數來處理 Url](#using-the-wininet-functions-to-handle-urls)
-   [正常化 Url](#what-is-a-canonicalized-url)
-   [結合基底和相對 Url](#combining-base-and-relative-urls)
-   [破解 Url](#cracking-urls)
-   [建立 Url](#creating-urls)
-   [直接存取 Url](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>什麼是正式的 URL？

所有 Url 的格式都必須遵循接受的語法和語義，才能透過網際網路存取資源。 標準化是將 URL 格式化以遵循此接受語法和語義的程式。

必須編碼的字元包括在美國-ASCII 編碼字元集中沒有對應圖形字元的任何字元 (十六進位 80-FF、在美國-ASCII 編碼字元集中未使用，以及十六進位的 00-1f 和7F，也就是控制字元) 、空格、"%" (用來編碼其他字元) ，以及不安全的字元 (<、>、 \# \| \\ ^、~、 \[ 、 \] 和 ' ) 。

## <a name="using-the-wininet-functions-to-handle-urls"></a>使用 WinINet 函數來處理 Url

下表摘要說明 URL 函數。



| 函式                                                   | 描述                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | 正常化 URL。                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | 結合基底和相對 Url。                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | 將 URL 字串剖析為元件。               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | 從元件建立 URL 字串。              |
| [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | 開始取出 FTP、HTTP 或 HTTPS 資源。 |



 

## <a name="canonicalizing-urls"></a>正常化 Url

正常化 URL 是將 URL 轉換成可接受格式的程式，其中可能會包含不安全的字元，例如空格、保留的字元等等。

[**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla)函式可以用來將 url 正常化。 這個函式是以工作為導向，因此應用程式應謹慎追蹤其使用方式。 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 不會驗證傳遞給它的 url 是否已正式運作，而且它所傳回的 url 是否有效。

下列五個旗標控制 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 處理特定 URL 的方式。 旗標可以搭配使用。 如果未使用任何旗標，則函式預設會編碼 URL。



| 值                     | 意義                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ICU \_ 瀏覽器 \_ 模式        | 請勿在 "" 或 "？" 之後編碼或解碼字元 \# ，而且不要在 "？" 之後移除尾端空白字元。 如果未指定此值，則會編碼整個 URL，並移除尾端空白字元。 |
| ICU \_ 解碼               | 在剖析 URL 之前，將所有的% XX 序列轉換成字元，包括 escape 序列。                                                                                                          |
| ICU \_ \_ 只編碼空格 \_ | 僅編碼空格。                                                                                                                                                                                     |
| ICU \_ 無 \_ 編碼           | 請勿將 unsafe 字元轉換成 escape 序列。                                                                                                                                                   |
| ICU \_ 無 \_ 中繼             | 請勿移除中繼序列 (例如 "." 和 "..."從 URL ) 。                                                                                                                                       |



 

ICU 解碼 \_ 旗標只能用於正式的 url，因為它會假設所有的% XX 序列都是 escape 程式碼，並將它們轉換成程式碼所表示的字元。 如果 URL 中的 "%" 符號不是 escape 程式碼的一部分，則 ICU 解碼仍會 \_ 將它視為一個。 此特性可能會導致 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 建立不正確 URL。

若要使用 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 傳回完全解碼的 URL，您 \_ \_ 必須指定 icu 解碼和 icu \_ 。 此設定會假設傳遞給 [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) 的 URL 先前已正式正式。

## <a name="combining-base-and-relative-urls"></a>結合基底和相對 Url

相對 URL 是相對於絕對基底 URL 之資源位置的精簡標記法。 剖析器必須知道基底 URL，而且通常會包含配置、網路位置和 URL 路徑的部分。 應用程式可以呼叫 [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) 來合併相對 url 與其基底 url。 [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) 也會正常化結果 URL。

## <a name="cracking-urls"></a>破解 Url

[**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)函式會將 url 分隔成其元件元件，並傳回傳遞給函式的 [**url \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa)結構所表示的元件。

組成 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構的元件包括配置編號、主機名稱、埠號碼、使用者名稱、密碼、URL 路徑和其他資訊 (例如) 的搜尋參數。 除了配置和埠號碼以外，每個元件都具有保存資訊的字串成員，以及保存字串成員長度的成員。 配置和埠號碼只有儲存對應值的成員;所有成功呼叫 [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)都會傳回它們。

若要取得 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構中特定元件的值，儲存該元件之字串長度的成員必須設定為非零值。 字串成員可以是緩衝區的位址或 **Null**。

如果指標成員包含緩衝區的位址，字串長度成員必須包含該緩衝區的大小。 [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) 會以字串形式傳回緩衝區中的元件資訊，並將字串長度儲存在字串長度成員中。

如果指標成員為 **Null**，則字串長度成員可以設定為任何非零值。 [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) 會儲存 url 字串中包含元件資訊之第一個字元的位址，並將字串長度設定為與元件相關之 url 字串其餘部分中的字元數。

所有的指標成員都會設定為 **Null** ，並將非零長度的成員指向 URL 字串中的適當起點。 長度成員中儲存的長度必須用來判斷個別元件資訊的結尾。

若要正確地完成初始化 [**url \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構， **wstructsize** 成員必須設定為 [**url \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構的大小（以位元組為單位）。

下列範例會在 PreOpen1 的編輯方塊中傳回 URL 的元件， \_ 並將元件傳回至 idc PreOpenList 的清單方塊 \_ 。 若只要顯示個別元件的資訊，此函式會在字串中的元件資訊之後立即複製字元，並暫時將它取代為 **Null**。


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>建立 Url

[**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)函式會使用 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa)結構中的資訊來建立統一資源定位器。

組成 [**URL \_ 元件**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) 結構的元件包括配置、主機名稱、埠號碼、使用者名稱、密碼、URL 路徑和其他資訊 (例如) 的搜尋參數。 除了埠號碼以外，每個元件都具有保存資訊的字串成員，以及保存字串成員長度的成員。

針對每個必要元件，指標成員應該包含保存資訊的緩衝區位址。 如果指標成員包含以零結尾的字串位址，則長度成員應設定為零。如果指標成員包含非以零終止的字串位址，則長度成員應設定為字串長度。 任何不需要的元件之指標成員都必須是 **Null**。

## <a name="accessing-urls-directly"></a>直接存取 Url

您可以使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 功能，直接存取網際網路上的 FTP 和 HTTP 資源。 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 會在傳遞至函式的 URL 上開啟與資源的連接。 建立此連接時，有兩個可能的步驟。 首先，如果資源是檔案， [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 可以進行下載;其次，如果資源是目錄， [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 可以列舉目錄中的檔案 (除非使用 CERN proxy) 。 如需 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)的詳細資訊，請參閱 [讀取](common-functions.md)檔案。 如需 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)的詳細資訊，請參閱 [尋找下一個](common-functions.md)檔案。

對於需要透過 CERN proxy 運作的應用程式， [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 可以用來存取 FTP 目錄和檔案。 FTP 要求會進行封裝，以像是 CERN proxy 會接受的 HTTP 要求。

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)函數所建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼和資源的 URL。 URL 必須包含配置 (HTTP：、ftp：、file：適用于 \[ 本機檔案 \] 或 HTTPs： \[ 適用于超文字通訊協定安全 \]) 和網路位置 (例如 `www.microsoft.com`) 。 URL 也可以包含路徑 (例如/isapi/gomscom.asp？TARGET =/windows/feature/) 和資源名稱 (例如 default.htm) 。 針對 HTTP 或 HTTPS 要求，可以包含其他標頭。

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)、 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP 或 HTTPS url，只) 可以使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 所建立的控制碼來下載資源。

下圖說明每個函式所要使用的控制碼。

![搭配函式使用的控制碼](images/ax-wnt02.png)

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)會使用 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所建立的根 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼。 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)所建立的 **HINTERNET** 控制碼可用於 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (不會在這裡顯示) 和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (HTTP 或 HTTPS url) 。

如需詳細資訊，請參閱 [**HINTERNET 控制碼**](appendix-a-hinternet-handles.md)。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 