---
description: 使用 mailslots、用戶端和伺服器時所要使用之函式的描述。
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: 郵筒作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977951"
---
# <a name="mailslot-operations"></a>郵筒作業

使用 mailslots 時，用戶端和伺服器只應使用下表中所討論的函式。 請勿使用其他函式，即使它們接受檔案控制代碼或檔案名作為參數，因為它們不是設計來與 mailslots 搭配使用。

## <a name="mailslot-server-functions"></a>郵筒伺服器函數

郵筒伺服器獨佔使用三個功能，如下表所示。



| 函式                                   | 描述                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | 建立信箱並傳回郵筒控制碼。                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | 抓取訊息大小上限、信箱大小、郵件中下一則訊息的大小、郵筒中的訊息數目，以及讀取作業可等候訊息的時間量。 |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | 變更郵筒的讀取超時時間。                                                                                                                                                                    |



 

郵筒伺服器也會使用下列函數。



| 函式                                                         | 描述                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | 複製郵筒控制碼。                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | 從郵筒抓取訊息。                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | 捕獲建立郵筒的日期和時間。 |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | 設定建立郵筒的日期和時間。      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | 抓取郵筒控點的屬性。        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | 設定信箱控點的屬性。             |



 

## <a name="mailslot-client-functions"></a>郵筒用戶端函式

在與信箱互動時，用戶端進程會使用下列功能。



| 函式                                                             | 描述                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | 關閉用戶端進程的信箱控制碼。  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | 建立用戶端進程的郵筒控制碼。 |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | 複製郵筒控制碼。                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)、 [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | 將資料寫入郵筒。                      |



 

 

 
