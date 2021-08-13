---
title: 非同步作業
description: 在非同步模式中，應用程式可以執行任何包含內容值的函式，做為它的其中一個參數，而且可以在應用程式等候函式完成其工作時，繼續執行其他命令或函數。
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e494b79b28b9aaf005fc6b1790d0cf84b07ceade6606f03ce03198426ac33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562090"
---
# <a name="asynchronous-operation"></a>非同步作業

應用程式存取網際網路資源所需的時間量，取決於許多因素，例如使用的連線、資源所在的伺服器，以及嘗試存取資源的使用者數目。 針對下載多項資源或處理多項工作的應用程式 (包括一或多個下載) ，等候每個下載完成，再繼續進行下一項工作，會非常沒有效率。 若要減少應用程式必須等待的時間，許多 WinINet 函數都可以非同步作業。

在非同步模式中，應用程式可以執行任何包含內容值的函式，做為它的其中一個參數，而且可以在應用程式等候函式完成其工作時，繼續執行其他命令或函數。 當工作完成時，應用程式所提供的狀態回呼函式會在工作進度以及完成時收到通知。 目前，狀態回呼函式可以呼叫其他函式，或執行任何其他相依于工作完成的必要工作。

當您以非同步方式呼叫 WinINet 時，不會 afinity 回呼執行緒：呼叫可能會從一個執行緒開始，但任何其他執行緒都可以接收回呼。

-   [優點](#benefits)
-   [案例](#scenarios)
-   [相關主題](#related-topics)

## <a name="benefits"></a>優點

非同步作業有幾個優點。 例如：

-   同時下載多個網際網路資源。

    您可以同時連線至多個網際網路資源，並在可用時加以下載。

-   提高應用程式的效能。

    使用 WinINet 函式的應用程式不需要等待要求完成，因此應用程式可以自由執行其他不相依于要求的工作，進而改善應用程式的整體效能。

-   監視下載進度。

    狀態回呼函式會在處理要求時接收通知。 如有需要，您的應用程式可以使用該狀態回呼函式所提供的資訊，讓使用者知道作業進度，或中斷花費太長時間才能完成的要求。

## <a name="scenarios"></a>案例

假設您的應用程式需要從 Downfall 咖啡 & 茶和第四個咖啡地點下載咖啡價格，並比較價格。 第四個咖啡場所通常會有較慢的回應時間，因此您的應用程式應該先從 Downfall 咖啡 & 茶下載資訊。

開發應用程式的兩個版本。 其中一個是以同步方式運作，先從 Downfall 咖啡 & 茶網站下載價格，再從第四個咖啡網站下載價格。 第二個作業會以非同步方式運作，並將要求傳送至兩個網站，並在可用時下載價格。

下表說明第四個咖啡網站在特定一天的速度較快時，會發生什麼事。



| 事件                                                            | 同步版本                        | 非同步版本                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| 開始                                                            | 將要求傳送至 Downfall 咖啡 & 茶      | 傳送要求以 Downfall 咖啡 & 茶和第四咖啡 |
| 從非同步版本到第四個咖啡的要求已完成 | 等候中                                    | 下載第四個咖啡的價格                       |
| 要求 Downfall 咖啡 & 茶已完成                       | 從 Downfall 咖啡 & 茶下載價格 | 從 Downfall 咖啡 & 茶下載價格               |
| Downfall 咖啡之後 & 茶的價格將會下載              | 將要求傳送至第四個咖啡              | 比較價格                                           |
| 非同步版本的比較已完成                      | 等候中                                    | 作業完成                                       |
| 從同步版本到第四個咖啡的要求已完成  | 下載第四個咖啡的價格         | n/a                                                      |
| 下載第四次咖啡的價格之後                      | 比較價格                             | n/a                                                      |
| 同步版本的比較已完成                       | 作業完成                         | n/a                                                      |



 

另一個範例是網頁瀏覽器，例如 Microsoft Internet Explorer。 當瀏覽器下載頁面時，通常需要下載其他資源，例如影像和音效檔。 在非同步模式中，頁面和其相關聯的資源可以在可用時同時進行要求和下載，而不是一次要求和下載頁面和每一個資源。

## <a name="related-topics"></a>[相關主題]

以下是相關的連結。

教學課程

-   [建立狀態回呼函數](creating-status-callback-functions.md)

設定非同步作業所需的函數

-   [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

可以非同步使用的函式

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)、 [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)、 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)、 [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)、 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)和 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)函數會使用對 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式的呼叫中所提供的內容值。

 

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 