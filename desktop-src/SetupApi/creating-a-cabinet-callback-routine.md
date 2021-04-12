---
description: 因為安裝程式 API 未提供預設的封包回呼常式，所以您必須提供常式。 SetupIterateCabinet 函式所需的回呼常式必須具有與 FileCallback 所指向的相同形式。
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: 建立封包回呼常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193080"
---
# <a name="creating-a-cabinet-callback-routine"></a>建立封包回呼常式

因為安裝程式 API 未提供預設的封包回呼常式，所以您必須提供常式。 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)函式所需的回呼常式必須具有與 [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)所指向的相同形式。

以下是 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 用來傳送通知給回呼常式的語法。

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

*內容* 參數是內容變數或結構的 void 指標，可供回呼常式用來儲存在後續呼叫回呼常式之間必須保存的資訊。

此內容的實作為回呼常式的指定，且 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)絕對不會參考或改變。

*通知* 參數是不帶正負號的整數，而且會是下列其中一個值。



| 通知                                                        | Description                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)   | 已從封包解壓縮檔案。      |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)   | 在封包中發現檔案。              |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md) | 目前的檔案會在下一個封包中繼續。 |



 

最後兩個參數 *Param1* 和 *Param2* 也是不帶正負號的整數，並包含與通知相關的其他資訊。 如需 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)所傳送通知的詳細資訊，請參閱封 [包檔通知](cabinet-file-notifications.md)。

SP 檔案 \_ \_ 通知 \_ 回呼常式傳回不帶正負號的整數。 根據通知，封包回呼常式應該會傳回下列其中一個值。

針對 SPFILENOTIFY \_ FILEINCABINET 通知， [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 預期回呼常式會傳回下列其中一個值。



| 值         | 意義                   |
|---------------|---------------------------|
| FILEOP \_ 中止 | 中止封包處理。 |
| FILEOP \_ DOIT R  | 將目前的檔案解壓縮。 |
| FILEOP \_ SKIP  | 略過目前的檔案。    |



 

針對 SPFILENOTIFY \_ NEEDNEWCABINET 和 SPFILENOTIFY \_ FILEEXTRACTED 通知， **SetupIterateCabinet** 預期回呼常式會傳回下列其中一個值。



| 值      | 意義                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 沒有 \_ 錯誤  | 未發生任何錯誤，請繼續處理封包。                                                                                                                                                                        |
| 錯誤 \_ XXX | 發生指定的類型時發生錯誤。 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)函式會傳回 **FALSE**，而指定的錯誤碼會由對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫傳回。 |



 

如果回呼常式傳回 FILEOP \_ doit r，則常式也必須提供完整的目標路徑。 如需詳細資訊，請參閱 [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)。

 

 
