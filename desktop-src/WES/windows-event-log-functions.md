---
title: Windows 事件記錄檔函數
description: Windows 事件記錄檔會定義下列函式，讓您可以用來從通道或事件記錄檔中取得事件，以及取得提供者的中繼資料及其產生的事件。
ms.assetid: 0bc008e4-c01c-482b-b910-49de3de22fab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893130b2881f2064151f56b6806cebdb9bf225d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968928"
---
# <a name="windows-event-log-functions"></a>Windows 事件記錄檔函數

Windows 事件記錄檔會定義下列函式，讓您可以用來從通道或事件記錄檔中取得事件，以及取得提供者的中繼資料及其產生的事件。



| 函式                                                                   | 描述                                                                                                                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**.EVT \_ 訂閱 \_ 回呼**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback)                 | 如果您呼叫 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函式來接收符合查詢的事件，請執行此回呼。                                                                                    |
| [**EvtArchiveExportedLog**](/windows/desktop/api/WinEvt/nf-winevt-evtarchiveexportedlog)                     | 將當地語系化字串加入至指定之記錄檔中的事件。                                                                                                                                                   |
| [**EvtCancel**](/windows/desktop/api/WinEvt/nf-winevt-evtcancel)                                             | 取消控制碼上的所有暫止作業。                                                                                                                                                                       |
| [**EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog)                                         | 移除指定通道中的所有事件，並將其寫入目標記錄檔。                                                                                                                             |
| [**EvtClose**](/windows/desktop/api/WinEvt/nf-winevt-evtclose)                                               | 關閉開啟的控制碼。                                                                                                                                                                                            |
| [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark)                             | 建立可在通道中識別事件的書簽。                                                                                                                                                         |
| [**EvtCreateRenderCoNtext**](/windows/desktop/api/WinEvt/nf-winevt-evtcreaterendercontext)                   | 建立內容，以指定您想要呈現之事件中的資訊。                                                                                                                            |
| [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog)                                       | 從指定的通道或記錄檔複製事件，並將它們寫入目標記錄檔。                                                                                                                      |
| [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage)                               | 格式化訊息字串。                                                                                                                                                                                         |
| [**EvtGetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgetchannelconfigproperty)         | 取得指定的通道設定屬性。                                                                                                                                                                |
| [**EvtGetEventInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgeteventinfo)                                 | 取得資訊，此資訊會識別已選取事件的結構化 XML 查詢，以及其所來自的通道或記錄檔。                                                                                 |
| [**EvtGetEventMetadataProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgeteventmetadataproperty)         | 取得指定的事件中繼資料屬性。                                                                                                                                                                       |
| [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus)                       | 取得文字訊息，其中包含目前錯誤的延伸錯誤資訊。                                                                                                                           |
| [**EvtGetLogInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetloginfo)                                     | 取得通道或記錄檔的相關資訊。                                                                                                                                                                     |
| [**EvtGetObjectArrayProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgetobjectarrayproperty)             | 從陣列中指定的物件取得提供者中繼資料屬性。                                                                                                                                         |
| [**EvtGetObjectArraySize**](/windows/desktop/api/WinEvt/nf-winevt-evtgetobjectarraysize)                     | 取得物件陣列中的元素數目。                                                                                                                                                              |
| [**EvtGetPublisherMetadataProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtgetpublishermetadataproperty) | 取得指定的提供者中繼資料屬性。                                                                                                                                                                    |
| [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo)                                 | 取得您所執行之查詢的相關資訊，該查詢會識別查詢嘗試存取的通道或記錄檔清單，以及表示每個存取成功或失敗的傳回碼清單。 |
| [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext)                                                 | 從查詢或訂閱結果中取得下一個事件。                                                                                                                                                       |
| [**EvtNextChannelPath**](/windows/desktop/api/WinEvt/nf-winevt-evtnextchannelpath)                           | 從列舉值取得通道名稱。                                                                                                                                                                          |
| [**EvtNextEventMetadata**](/windows/desktop/api/WinEvt/nf-winevt-evtnexteventmetadata)                       | 從列舉值取得事件定義。                                                                                                                                                                     |
| [**EvtNextPublisherId**](/windows/desktop/api/WinEvt/nf-winevt-evtnextpublisherid)                           | 從列舉值取得提供者的識別碼。                                                                                                                                                            |
| [**EvtOpenChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelconfig)                       | 取得用來讀取或修改通道設定屬性的控制碼。                                                                                                                                  |
| [**EvtOpenChannelEnum**](/windows/desktop/api/WinEvt/nf-winevt-evtopenchannelenum)                           | 取得控制碼，您可以用來列舉電腦上已註冊的通道清單。                                                                                                                 |
| [**EvtOpenEventMetadataEnum**](/windows/desktop/api/WinEvt/nf-winevt-evtopeneventmetadataenum)               | 取得控制碼，您可以使用此控制碼來列舉提供者所定義的事件清單。                                                                                                                             |
| [**EvtOpenLog**](/windows/desktop/api/WinEvt/nf-winevt-evtopenlog)                                           | 取得通道或記錄檔的控制碼，您可以用來取得通道或記錄檔的相關資訊。                                                                                                    |
| [**EvtOpenPublisherEnum**](/windows/desktop/api/WinEvt/nf-winevt-evtopenpublisherenum)                       | 取得控制碼，您可以用來列舉電腦上已註冊之提供者的清單。                                                                                                                         |
| [**EvtOpenPublisherMetadata**](/windows/desktop/api/WinEvt/nf-winevt-evtopenpublishermetadata)               | 取得用來讀取指定提供者之中繼資料的控制碼。                                                                                                                                             |
| [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession)                                   | 建立遠端電腦的連線，您可以在呼叫其他 Windows 事件記錄檔時使用該連接。                                                                                                |
| [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery)                                               | 執行查詢，以從符合指定查詢準則的通道或記錄檔中取出事件。                                                                                                               |
| [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender)                                             | 根據您指定的轉譯內容呈現 XML 片段。                                                                                                                                          |
| [**EvtSaveChannelConfig**](/windows/desktop/api/WinEvt/nf-winevt-evtsavechannelconfig)                       | 儲存對通道設定所做的變更。                                                                                                                                                              |
| [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek)                                                 | 搜尋查詢結果集中的特定事件。                                                                                                                                                                  |
| [**EvtSetChannelConfigProperty**](/windows/desktop/api/WinEvt/nf-winevt-evtsetchannelconfigproperty)         | 設定通道的指定設定屬性。                                                                                                                                                           |
| [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe)                                       | 建立訂用帳戶，該訂閱將會從符合指定查詢準則的通道或記錄檔接收目前和未來的事件。                                                                            |
| [**EvtUpdateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark)                             | 使用可識別指定事件的資訊來更新書簽。                                                                                                                                        |



 

 

 