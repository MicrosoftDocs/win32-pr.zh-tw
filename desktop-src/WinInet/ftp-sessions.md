---
title: FTP 會話
description: WinINet 可讓應用程式在 ftp 伺服器上流覽和操作目錄和檔案。 因為 CERN proxy 不支援 FTP，所以使用 CERN proxy 的應用程式必須使用 InternetOpenUrl 函數。
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023771"
---
# <a name="ftp-sessions"></a>FTP 會話

WinINet 可讓應用程式在 ftp 伺服器上流覽和操作目錄和檔案。 因為 CERN proxy 不支援 FTP，所以使用 CERN proxy 的應用程式必須使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函數。 如需如何使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)的詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)。

若要開始 FTP 會話，請使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 來建立會話控制碼。

WinINet 可讓您在 FTP 伺服器上執行下列動作：

-   在目錄之間流覽。
-   列舉、建立、移除和重新命名目錄。
-   重新命名、上傳、下載及刪除檔案。

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)和 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)函式會提供導覽。 這些函式會利用前一次呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的會話控制碼，判斷應用程式目前所在的目錄，或變更至不同的子目錄。

目錄列舉是使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 和 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 函數來執行。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 會使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的會話控制碼來尋找符合指定搜尋準則的第一個檔案，並傳回可繼續目錄列舉的控制碼。 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 會使用 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 傳回的控制碼來傳回符合原始搜尋準則的下一個檔案。 除非目錄中沒有其他檔案，否則應用程式應繼續呼叫 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 。

使用 [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) 函式來建立新的目錄。 此函式會使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所建立的會話控制碼，並建立傳遞給函式之字串所指定的目錄。 字串可以包含相對於目前的目錄的目錄名稱，或是完整的目錄路徑。

若要重新命名檔案或目錄，應用程式可以呼叫 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)。 此函式會將原始名稱取代為傳遞給函式的新名稱。 檔案或目錄的名稱可以相對於目前的目錄或完整名稱。

若要在 FTP 伺服器上上傳或放置檔案，應用程式可以使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) 或 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (以及 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)) 。 如果檔案已存在於本機，則可以使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) ，而如果需要將資料寫入 FTP 伺服器上的檔案，則可以使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)和 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) 。

若要下載或取得檔案，應用程式可以使用 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 或 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (搭配 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)) 。 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 是用來從 FTP 伺服器取出檔案並將它儲存在本機，而 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 可以用來控制下載資訊的 (例如，應用程式可以在編輯方塊中顯示資訊) 。

使用 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) 函數刪除 FTP 伺服器上的檔案。 此函式會從 FTP 伺服器移除相對於目前的目錄或完整檔案名的檔案名。 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) 需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)傳回的會話控制碼。

## <a name="ftp-function-handles"></a>FTP 函數控制碼

若要正常運作，FTP 函數需要特定類型的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼。 這些控制碼必須以特定順序建立，從 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)所建立的根控制碼開始。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 接著可以建立 FTP 會話控制碼。

下圖顯示相依于 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回之 FTP 會話控制碼的函式。 陰影方塊代表會傳回 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 HINTERNET 控制碼。

![ftp 函數相依于 internetconnect 所傳回的 ftp 會話控制碼](images/ax-wnt06.png)

下圖顯示兩個函式，這些函式會傳回 [HINTERNET](appendix-a-hinternet-handles.md) 控制碼和相依的函式。 陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。

![傳回 hinternet 控制碼的 ftp 函數](images/ax-wnt03.png)

如需詳細資訊，請參閱 [HINTERNET 控制碼](appendix-a-hinternet-handles.md)。

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>使用適用于 FTP 會話的 WinINet 函數

FTP 會話期間使用下列函數。 CERN proxy 無法辨識這些函數。 必須透過 CERN proxy 運作的應用程式應該使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 並直接存取資源。 如需直接存取資源的詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)。



| 函式                                                 | 描述                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | 在伺服器上建立新的目錄。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | 從伺服器刪除檔案。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                         |
| [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | 在目前的目錄中開始檔案列舉或檔案搜尋。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | 傳回伺服器上用戶端的目前的目錄。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                   |
| [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | 從伺服器抓取檔案。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | 起始存取伺服器上的檔案以進行讀取或寫入。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。 |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | 將檔案寫入伺服器。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | 刪除伺服器上的目錄。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | 重新命名伺服器上的檔案。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | 變更用戶端在伺服器上的目前的目錄。 此函數需要 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的控制碼。                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | 將資料寫入伺服器上已開啟的檔案。 此函數需要 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)所建立的控制碼。                                      |



 

### <a name="starting-an-ftp-session"></a>啟動 FTP 會話

應用程式會在 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)建立的控制碼上呼叫 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ，以建立 FTP 會話。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 需要 [伺服器名稱]、[埠號碼]、[使用者名稱]、[密碼] 和 [服務類型] (必須設定為 [網際網路 \_ 服務 \_ FTP]) 。 針對被動 FTP 語義，應用程式也必須設定 [網際網路 \_ 旗標 \_ 被動](api-flags.md) 旗標。

網際網路 \_ 預設 \_ FTP \_ 埠和網際網路通訊 \_ \_ 埠 \_ 編號值可以用於埠號碼。 網際網路 \_ 預設 \_ ftp \_ 埠使用預設的 ftp 埠，但仍然必須設定服務類型。 網際網路 \_ 無效 \_ \_ 的埠號碼會使用指定之服務類型的預設值。

您可以將使用者名稱和密碼的值設定為 **Null**。 如果這兩個值都設定為 **Null**， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 會使用「匿名」作為使用者名稱，並使用使用者的電子郵件地址做為密碼。 如果只有密碼設定為 **Null**，則會使用傳遞至 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 的使用者名稱做為使用者名稱，並使用空字串作為密碼。 如果兩個值都不是 **Null**，就會使用提供給 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 的使用者名稱和密碼。

### <a name="enumerating-directories"></a>列舉目錄

您必須透過 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)建立控制碼，以列舉 FTP 伺服器上的目錄。 這個控制碼是 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立之會話控制碼的分支。 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 會找出伺服器上的第一個檔案或目錄，並將它傳回 [**WIN32 \_ FIND \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) 結構中。 使用 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) 直到傳回 [**錯誤的 \_ 檔案 \_ \_**](wininet-errors.md)為止。 這個方法會尋找伺服器上的所有後續檔案和目錄。 如需 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)的詳細資訊，請參閱 [尋找下一個](common-functions.md)檔案。

若要判斷 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)或 [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)取出的檔案是否為目錄，請檢查 [**WIN32 \_ FIND \_ 資料**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa)結構的 **dwFileAttributes** 成員，看看它是否等於檔 \_ 屬性 \_ 目錄。

如果應用程式在 FTP 伺服器上進行變更，或 FTP 伺服器經常變更，則不應在 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)中設定「[網際網路 \_ 旗 \_ \_ \_](api-flags.md)標」和「[網際網路 \_ 旗標 \_ 重載](api-flags.md)」旗標。 這些旗標可確保從 FTP 伺服器取出的目錄資訊是最新的。

在應用程式完成目錄列舉之後，應用程式必須在 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)建立的控制碼上呼叫 [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) 。 在該控制碼關閉之前，應用程式無法在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)建立的會話控制碼上再次呼叫 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 。 如果在前一次呼叫相同的函式之前，對相同的會話控制碼進行 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) 呼叫，此函式會失敗， [並 \_ 傳回錯誤 FTP \_ 傳輸 \_ \_ 進行中](wininet-errors.md)。

下列範例會將 FTP 目錄的內容列舉為清單方塊控制項。 *HConnection* 參數是 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式在建立 FTP 會話之後所傳回的控制碼。 此範例中所參考 InternetErrorOut 函式的範例原始程式碼可在 [處理錯誤](appendix-c-handling-errors.md)主題中找到。


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a>流覽目錄

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)和 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)函式會處理目錄導覽。

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) 會傳回 FTP 伺服器上應用程式的目前的目錄。 包含 FTP 伺服器根目錄的目錄路徑。

[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) 會變更伺服器上的工作目錄。 傳遞至 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) 的目錄資訊可以是相對於目前的目錄的部分或完整路徑名稱。 例如，如果應用程式目前位於目錄 "public/info"，且路徑為 "ftp/example"， [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) 會將目前的目錄變更為 "public/info/ftp/example"。

下列範例會使用由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回的 FTP 會話控制碼 hConnection。 新的目錄名稱是取自父對話方塊的 [編輯] 方塊，其 IDC 會在 *nDirNameId* 參數中傳遞。 在進行目錄變更之前，此函式會抓取目前的目錄，並將它儲存在相同的編輯方塊中。 上述 DisplayFtpDir 函式的來源程式代碼會在上方列出。


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a>操作 FTP 伺服器上的目錄

WinINet 提供在 FTP 伺服器上建立和移除目錄的功能，應用程式具有必要的許可權。 如果應用程式必須以特定的使用者名稱和密碼登入伺服器，則在建立 FTP 會話控制碼時，可以在 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 中使用這些值。

[**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)函式會採用有效的 FTP 會話控制碼和以 **null** 終止的字串，其中包含相對於目前的目錄的完整路徑或名稱，並在 FTP 伺服器上建立目錄。

下列範例顯示兩個不同的 [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)呼叫。 在這兩個範例中，hFtpSession 是由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數所建立的會話控制碼，而根目錄是目前的目錄。

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

[**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)函式會採用會話控制碼和以 **null** 終止的字串，其中包含相對於目前的目錄的完整路徑或名稱，然後從 FTP 伺服器移除該目錄。

下列範例顯示兩個對 [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)的呼叫範例。 在這兩個呼叫中，hFtpSession 是由 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數所建立的會話控制碼，而根目錄是目前的目錄。 根目錄中有一個名為 "test" 的目錄，以及 "test" 目錄中名為 "example" 的目錄。

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



下列範例會在 FTP 伺服器上建立新的目錄。 新的目錄名稱是取自父對話方塊的 [編輯] 方塊，其 IDC 會在 *nDirNameId* 參數中傳遞。 建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。 在結尾處呼叫 DisplayFtpDir 函式的原始程式碼如下所示。


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



下列範例會從 FTP 伺服器刪除目錄。 要刪除的目錄名稱是取自父對話方塊中的 [編輯] 方塊，其 IDC 會傳入 *nDirNameId* 參數。 建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。 在結尾處呼叫 DisplayFtpDir 函式的原始程式碼如下所示。


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a>取得 FTP 伺服器上的檔案

有三種方法可從 FTP 伺服器上取出檔案：

-   使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)。
-   使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 和 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)。
-   使用 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)。

如需使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 函數的詳細資訊，請參閱 [讀取](common-functions.md)檔案。

如果檔案的 URL 可用，應用程式可以呼叫 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 來連接到該 url，然後使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 來控制檔案的下載。 這可讓應用程式更嚴密地控制下載，而且非常適合在 FTP 伺服器上不需要進行其他作業的情況下。 如需如何直接存取資源的詳細資訊，請參閱 [直接存取 url](handling-uniform-resource-locators.md)。

如果應用程式已使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)建立與伺服器的 FTP 會話控制碼，則應用程式可以使用現有的檔案名和本機儲存之檔案的新名稱來呼叫 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 。 然後，應用程式可以使用 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) 來下載檔案。 如此一來，應用程式就能更嚴密地控制下載內容並保持與 FTP 伺服器的連接，因此可以執行更多命令。

如果應用程式不需要嚴格控制下載，則應用程式可以使用 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 與 FTP 會話控制碼、遠端檔案名和本機檔案名來取出檔案。 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) 會執行所有與從 FTP 伺服器讀取檔案並儲存在本機的相關簿記和負擔。

下列範例會從 FTP 伺服器抓取檔案，並將它儲存在本機。 FTP 伺服器上的檔案名是取自父對話方塊中的 [編輯] 方塊，其 IDC 會在 *nFtpFileNameId* 參數中傳遞，而儲存檔案的本機名稱則是取自在 *nLocalFileNameId* 參數中傳遞其 idc 的編輯方塊。 建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a>將檔案放在 FTP 伺服器上

有兩種方法可將檔案放在 FTP 伺服器上：

-   搭配使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 與 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)。
-   使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)。

必須將資料傳送至 FTP 伺服器的應用程式，但沒有包含所有資料的本機檔案，則應該使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) 在 ftp 伺服器上建立並開啟檔案。 然後，應用程式可以使用 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) 將資訊上傳至檔案。

如果檔案已存在於本機，則應用程式可以使用 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) 將檔案上傳到 FTP 伺服器。 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) 會執行將本機檔案上傳到遠端 FTP 伺服器所產生的所有負擔。

下列範例會將本機檔案複製到 FTP 伺服器上。 檔案的本機名稱是取自父對話方塊中的 [編輯] 方塊，其 IDC 是在 *nLocalFileNameId* 參數中傳遞，而檔案儲存在 FTP 伺服器上的名稱則是取自在 *nFtpFileNameId* 參數中傳遞其 idc 的編輯方塊。 建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a>從 FTP 伺服器刪除檔案

若要從 FTP 伺服器刪除檔案，請使用 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) 函數。 呼叫應用程式必須具有從 FTP 伺服器刪除檔案的必要許可權。

下列範例會從 FTP 伺服器刪除檔案。 要刪除之檔案的名稱是取自父對話方塊中的 [編輯] 方塊，其 IDC 會以 int 傳遞 *nFtpFileNameId* 參數。 建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。 由於此函式不會重新整理檔案清單或目錄顯示，因此呼叫進程應該在成功刪除時這樣做。


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>重新命名 FTP 伺服器上的檔案和目錄

您可以使用 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) 函式來重新命名 FTP 伺服器上的檔案和目錄。 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) 接受兩個以 **null** 終止的字串，其中包含相對於目前的目錄的部分或完整名稱。 函式會將第一個字串所指定的檔案名，變更為第二個字串所指定的名稱。

下列範例會重新命名 FTP 伺服器上的檔案或目錄。 檔案或目錄的目前名稱取自父對話方塊中的 [編輯] 方塊，其 IDC 會在 *nOldFileNameId* 參數中傳遞，而新的名稱則是取自在 *nNewFileNameId* 參數中傳遞其 idc 的編輯方塊。 建立 FTP 會話之後， [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)會建立 *hConnection* 控制碼。 由於此函式不會重新整理檔案清單或目錄顯示，因此呼叫進程應該在成功重新命名時這麼做。


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 