---
title: HINTERNET 控制碼
description: 此區段包含 WinINet 函式所使用的控制碼和其運作階層的相關資訊。
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051900"
---
# <a name="hinternet-handles"></a>HINTERNET 控制碼

此區段包含 WinINet 函式所使用的控制碼和其運作階層的相關資訊。

-   [關於 HINTERNET 控制碼](#about-hinternet-handles)
-   [控制碼階層](#handle-hierarchy)
-   [FTP 階層](#ftp-hierarchy)
-   [HTTP 階層](#http-hierarchy)

## <a name="about-hinternet-handles"></a>關於 HINTERNET 控制碼

WinINet 函數所建立和使用的控制碼為 **HINTERNET** 類型。 WinINet 函數會傳回無法與其他控制碼類型互換的 **HINTERNET** 控制碼。 因此，它們不能與 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 或 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)等函數搭配使用。 同樣地，其他控制碼類型無法與 WinINet 函數一起使用。 例如， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 所傳回的控制碼無法傳遞至 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)。

[**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)函式會關閉 **HINTERNET** 類型的控制碼。 請注意，控制碼值會迅速回收;因此，如果控制碼已關閉，且立即產生新的控制碼，則新控制碼很有可能與剛剛關閉的控制碼具有相同的值。

## <a name="handle-hierarchy"></a>控制碼階層

**HINTERNET** 控制碼會在樹狀結構階層中進行維護。 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)函式所傳回的控制碼是根節點。 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式所傳回的控制碼佔用了下一個層級。 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)、 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)和 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)函數所傳回的控制碼是分葉節點。

**Windows XP 和 Windows Server 2003 R2 和更早版本：**、 [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)和 [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)所傳回的控制碼也是分葉節點。

下圖說明 **HINTERNET** 控制碼的階層架構。 圖中的每個方塊都代表會傳回 **HINTERNET** 控制碼的函式。

![建立控制碼的函式](images/ax-wnt01.png)

最上層是 [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) 函數，它會建立根控制碼。 下一個層級包含 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 和 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 函數。 使用 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) 所傳回之控制碼的函式會組成最後一個層級。

下圖顯示相依于 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)所建立之控制碼的函式。 陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊表示使用相關聯函式所建立之 **HINTERNET** 控制碼的函式。

![使用 internetopenurl 控制碼的函式](images/ax-wnt02.png)

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)函數會使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)所建立的 **HINTERNET** 控制碼。

## <a name="ftp-hierarchy"></a>FTP 階層

下圖顯示的 FTP 函數相依于 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所傳回的 ftp 會話控制碼。 陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。

![使用 ftp 會話控制碼的函式](images/ax-wnt06.png)

[**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)、 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)、 [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)、 [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)、 [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)、 [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)、 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)和 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)函數全都使用 [**HINTERNET**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)所建立的 **InternetConnect** 控制碼。

下圖顯示兩個傳回控制碼的 FTP 函數以及相依的函式。 陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。

![使用 ftpopen 和 ftpfindfirstfile 之控制碼的函式](images/ax-wnt03.png)

[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)函式相依于 [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)所建立的控制碼，而 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)則會使用 [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)所建立的控制碼。

## <a name="http-hierarchy"></a>HTTP 階層

下圖顯示用於 HTTP 通訊協定之函式的關聯性。 陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。

![使用 HTTPopenrequest 控制碼的函式](images/ax-wnt05.png)

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa)、 [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)、 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)、 [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)和 [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)函數相依于 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立的控制碼。

下圖顯示在 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)傳送 HttpOpenRequest 之後，使用 [](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所建立之 **HINTERNET** 控制碼的函式。 陰影方塊代表會傳回 **HINTERNET** 控制碼的函式，而一般方塊代表的函式會使用其相依的函式所建立的 **HINTERNET** 控制碼。

![HTTPsendrequest 之後使用控制碼的函式](images/ax-wnt07.png)

在 [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) 使用 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所傳回的控制碼之後，它就可以由 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)、 [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)和 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)使用。

![HTTPsendrequestex 之後使用控制碼的函式](images/ax-wnt08.png)

在 [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) 使用 [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)所傳回的控制碼之後， [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)、 [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)和 [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)可以使用此控制碼。 呼叫 [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) 之後， [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)、 [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)和 [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)可以使用此控制碼。

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 