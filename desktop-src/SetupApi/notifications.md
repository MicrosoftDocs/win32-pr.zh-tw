---
description: 通知是安裝函數傳送給回呼常式以指定狀態或事件的值。 Param1 和 Param2 這兩個參數會隨著通知一起傳送，並且包含與通知相關的其他資訊。
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: " (設定 API) 的通知"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096d4261a99e0a837a90aa5c965a3b676843945d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979262"
---
# <a name="notifications-setup-api"></a> (設定 API) 的通知

通知是安裝函數傳送給回呼常式以指定狀態或事件的值。 *Param1* 和 *Param2* 這兩個參數會隨著通知一起傳送，並且包含與通知相關的其他資訊。

回呼常式會處理通知，並將不帶正負號的整數傳回至安裝函式。 根據安裝函式而定，您可以使用這個值來指定作業或使用者選擇，也可以忽略它。

安裝函式會使用下列語法，將通知傳送給回呼常式。

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

*內容* 參數是內容變數或結構的 void 指標，回呼常式可以用它來儲存必須在回呼常式後續呼叫之間保存的資訊。

由於回呼常式會指定內容的執行，而且它永遠不會由安裝函式參考或改變，因此內容不會記載在後續通知訊息的參考資料中。

*通知* 參數會針對事件或狀態指定不帶正負號的整數值，使設定函數呼叫回呼常式。

*Param1* 和 *Param2* 是選擇性參數，可包含與通知相關的其他資訊。 這些參數是不帶正負號的整數。 如果 *Param1* 或 *Param2* 傳回的資訊不是不帶正負號的整數，則會轉換成不帶正負號的整數，而且必須先重新轉換成其原始資料類型，才能讓回呼常式使用它。

> [!Note]  
> 下列通知代表安裝函數所使用的每個通知。 個別函式會使用這些通知的子集。 換句話說，並非每個函數都使用每個通知。

 

安裝函數會使用下列通知。



| 通知                                                                     | Description                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)                        | 檔案複製作業期間發生錯誤。                                               |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)                    | 檔案刪除作業期間發生錯誤。                                           |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)                            | 檔案複製作業已結束。                                                              |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)                        | 檔案刪除操作已結束。                                                          |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)                          | 佇列已完成認可。                                                            |
| [**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)            | 檔案的註冊或取消註冊已完成。                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)                        | 檔案重新命名作業已結束。                                                            |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)                    | 子佇列 (複製、重新命名或刪除) 已結束。                                         |
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)                | 已從封包解壓縮檔案。                                                 |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)                | 在封包中發現檔案。                                                         |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md)                | 檔案已在使用中，而且目前的操作已延遲，直到系統重新開機為止。 |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)                  | 目前操作的語言與系統語言不符。                     |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)                        | 需要新的來源媒體。                                                                 |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md)              | 目前的檔案會在下一個封包中繼續。                                            |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)                        | 已掃描檔案佇列中的節點。                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ EX**](spfilenotify-queuescan-ex.md)                 | 已掃描檔案佇列中的節點。                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**](spfilenotify-queuescan-signerinfo.md) | 已掃描檔案佇列中的節點。                                                    |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)                    | 檔案重新命名作業期間發生錯誤。                                             |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)                        | 檔案複製作業已啟動。                                                            |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)                    | 檔案刪除作業已啟動。                                                          |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)                      | 佇列已開始認可。                                                              |
| [**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)        | 檔案的註冊或取消註冊已開始。                                   |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)                    | 檔案重新命名作業已啟動。                                                          |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md)                | 子佇列 (複製、重新命名或刪除) 已開始。                                       |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)                  | 目標上已有指定檔案的複本。                                    |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)                    | 目標上有較新版本的指定檔案。                                   |



 

 

 



