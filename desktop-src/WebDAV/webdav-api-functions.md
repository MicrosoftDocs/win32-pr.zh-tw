---
title: WebDAV API 函數
description: 下列函式用於 WebDAV API。
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401f527bcd98f86f8116df5b25ba1ea71e0f432e19dc89eae00582a2a0b4865e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995038"
---
# <a name="webdav-api-functions"></a>WebDAV API 函數

下列函式用於 WebDAV API。



| 函式                                                             | 描述                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | 建立與 WebDAV 伺服器的安全連線，或連接到 WebDAV 伺服器上的遠端檔案或目錄。                                                                                                                                   |
| [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | WebDAV 用戶端會呼叫應用程式定義的 [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) 回呼函數，以提示使用者輸入認證。                                                                                           |
| [**DavCancelConnectionsToServer**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | 關閉 webdav 伺服器的所有連線，或連接到 WebDAV 伺服器上的遠端檔案或目錄。                                                                                                                                        |
| [**DavDeleteConnection**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | 關閉使用 [**DavAddConnection**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) 函數建立的連接。                                                                                                                              |
| [**DavFlushFile**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | 將遠端檔案的本機版本資料排清到 WebDAV 伺服器。                                                                                                                                                        |
| [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | WebDAV 用戶端會呼叫應用程式定義的 [*DavFreeCredCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) 回呼函式，以釋放 [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) 回呼函式所取出的認證資訊。 |
| [**DavGetExtendedError**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | 抓取 WebDAV 伺服器針對先前失敗的 i/o 作業傳回的擴充錯誤碼資訊。                                                                                                                  |
| [**DavGetHTTPFromUNCPath**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | 將指定的 UNC 路徑轉換為對等的 HTTP 路徑。                                                                                                                                                                           |
| [**DavGetTheLockOwnerOfTheFile**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | 傳回 WebDAV 伺服器上鎖定之檔案的檔案鎖定擁有者。                                                                                                                                                             |
| [**DavGetUNCFromHTTPPath**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | 將指定的 HTTP 路徑轉換為相等的 UNC 路徑。                                                                                                                                                                           |
| [**DavInvalidateCache**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | 使 WebDAV 伺服器上遠端檔案的本機快取內容失效。                                                                                                                                                     |
| [**DavRegisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | 註冊應用程式定義的回呼函式，讓 WebDAV 用戶端可以用來提示使用者輸入認證。                                                                                                                 |
| [**DavUnregisterAuthCallback**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | 將 WebDAV 用戶端用來提示使用者輸入認證的已註冊回呼函數取消註冊。                                                                                                                            |



 

 

 




