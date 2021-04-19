---
description: 本節說明訊息和訊息佇列，以及如何在您的應用程式中使用它們。
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\messagesandmessagequeues.htm
title: 訊息和訊息佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0233af932d1aa9a4130e244af002d6180fdf055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985456"
---
# <a name="messages-and-message-queues"></a>訊息和訊息佇列

本節說明訊息和訊息佇列，以及如何在您的應用程式中使用它們。

### <a name="in-this-section"></a>本節內容



| Name                                                                       | 描述                                                                                                                                |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [關於訊息和訊息佇列](about-messages-and-message-queues.md) | 本節討論 Windows 訊息和訊息佇列。<br/>                                                                     |
| [使用訊息和訊息佇列](using-messages-and-message-queues.md) | 下列程式碼範例示範如何執行與 Windows 訊息和訊息佇列相關聯的下列工作。<br/> |
| [訊息參考](message-and-message-queue-reference.md)               | 包含 API 參考。<br/>                                                                                                     |



 

### <a name="system-provided-messages"></a>System-Provided 訊息

如需系統提供之訊息的清單，請參閱 [系統定義的訊息](about-messages-and-message-queues.md)。

### <a name="message-functions"></a>訊息函數



| Name                                                         | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage)     | 將訊息傳送給指定的收件者。 收件者可以是應用程式、可安裝的驅動程式、網路驅動程式、系統層級的設備磁碟機，或這些系統元件的任何組合。 <br/> 若要在定義要求時接收其他資訊，請使用 [**BroadcastSystemMessageEx**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessageexa) 函數。<br/>                                                                                                                                                                                                                                  |
| [**BroadcastSystemMessageEx**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessageexa) | 將訊息傳送給指定的收件者。 收件者可以是應用程式、可安裝的驅動程式、網路驅動程式、系統層級的設備磁碟機，或這些系統元件的任何組合。 <br/> 此函式類似于 [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) ，不過這個函式可以從收件者傳回更多資訊。<br/>                                                                                                                                                                                                              |
| [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)                   | 將訊息分派至視窗程式。 它通常用來分派 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 函式所取出的訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**GetInputState**](/windows/win32/api/winuser/nf-winuser-getinputstate)                       | 判斷呼叫執行緒的訊息佇列中是否有滑鼠按鍵或鍵盤訊息。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)                             | 從呼叫執行緒的訊息佇列抓取訊息。 函數會分派傳入的傳送訊息，直到張貼的訊息可供抓取為止。 <br/> 不同于 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)， [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函式不會在傳回訊息之前等候訊息張貼。<br/>                                                                                                                                                                                                                                                              |
| [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo)           | 抓取目前線程的額外訊息資訊。 額外的訊息資訊是與目前線程訊息佇列相關聯的應用程式或驅動程式定義值。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetMessagePos**](/windows/win32/api/winuser/nf-winuser-getmessagepos)                       | 抓取 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 函數抓取之最後一個訊息的資料指標位置。 <br/> 若要判斷資料指標目前的位置，請使用 [**GetCursorPos**](/windows/desktop/api/winuser/nf-winuser-getcursorpos) 函數。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime)                     | 抓取 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 函式所抓取之最後一則訊息的訊息時間。 時間是長整數，指定從系統開始到建立訊息的時間（以毫秒為單位）， (也就是放線上程的訊息佇列) 。 <br/>                                                                                                                                                                                                                                                                         |
| [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus)                     | 表示在呼叫執行緒訊息佇列中找到的訊息類型。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**InSendMessage**](/windows/win32/api/winuser/nf-winuser-insendmessage)                       | 判斷目前的視窗程式是否正在處理從另一個執行緒 (在相同進程中傳送的訊息，或呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數) 的不同進程。 <br/> 若要取得有關如何傳送訊息的其他資訊，請使用 [**InSendMessageEx**](/windows/win32/api/winuser/nf-winuser-insendmessageex) 函數。<br/>                                                                                                                                                                                                                              |
| [**InSendMessageEx**](/windows/win32/api/winuser/nf-winuser-insendmessageex)                   | 判斷目前的視窗程式是否正在處理從另一個執行緒 (在相同進程或不同進程) 中傳送的訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                           | 分派傳入的已傳送訊息、檢查已張貼訊息的執行緒訊息佇列，以及抓取訊息 (如果有任何) 存在的話。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                           | 將訊息張貼在與建立指定視窗的執行緒相關聯的訊息佇列中，並傳回，而不等候執行緒訊息。 <br/> 若要在與執行緒相關聯的訊息佇列中公佈訊息，請使用 [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) 函數。<br/>                                                                                                                                                                                                                                                                          |
| [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)                   | 向系統表示執行緒已發出終止 (結束) 的要求。 它通常用於回應 [**WM \_**](wm-destroy.md) 終結訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea)               | 將訊息張貼到指定之執行緒的訊息佇列。 它會返回，而不會等候執行緒訊息。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)       | 定義在整個系統中保證是唯一的新視窗訊息。 傳送或張貼訊息時，可以使用訊息值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage)                         | 回復透過 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式傳送的訊息，而不將控制權傳回給呼叫 **SendMessage** 的函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [*SendAsyncProc*](/windows/win32/api/winuser/nc-winuser-sendasyncproc)                         | 搭配 [**SendMessageCallback**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka) 函式使用的應用程式定義回呼函數。 系統將訊息傳遞至目的地視窗程式之後，系統會將訊息傳遞給回呼函式。 **SENDASYNCPROC** 型別定義此回呼函數的指標。 [*SendAsyncProc*](/windows/win32/api/winuser/nc-winuser-sendasyncproc) 是應用程式定義函數名稱的預留位置。<br/>                                                                                                                                                                          |
| [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                           | 將指定的訊息傳送至視窗或視窗。 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)函式會呼叫指定視窗的視窗程式，且在視窗程式處理訊息之前不會傳回。 <br/> 若要傳送訊息並立即傳回，請使用 [**SendMessageCallback**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka) 或 [**SendNotifyMessage**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea) 函數。 若要將訊息張貼至執行緒的訊息佇列並立即傳回，請使用 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 或 [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) 函數。<br/> |
| [**SendMessageCallback**](/windows/win32/api/winuser/nf-winuser-sendmessagecallbacka)           | 將指定的訊息傳送至視窗或視窗。 它會呼叫指定視窗的視窗程式，並立即傳回。 在視窗程式處理訊息之後，系統會呼叫指定的回呼函式，並將訊息處理的結果和應用程式定義的值傳遞至回呼函式。<br/>                                                                                                                                                                                                                                             |
| [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)             | 將指定的訊息傳送到其中一個視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**SendNotifyMessage**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea)               | 將指定的訊息傳送至視窗或視窗。 如果視窗是由呼叫執行緒所建立， [**SendNotifyMessage**](/windows/win32/api/winuser/nf-winuser-sendnotifymessagea) 會呼叫視窗的視窗程式，且在視窗程式處理訊息之前不會傳回。 如果視窗是由不同的執行緒所建立， **SendNotifyMessage** 會將訊息傳遞至視窗程式，並立即傳回。它不會等候視窗程式完成訊息的處理。<br/>                                                                                              |
| [**SetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-setmessageextrainfo)           | 設定目前線程的額外訊息資訊。 額外的訊息資訊是與目前線程訊息佇列相關聯的應用程式或驅動程式定義值。 應用程式可以使用 [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) 函式來取出執行緒的額外訊息資訊。<br/>                                                                                                                                                                                                                                                                |
| [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage)                 | 將虛擬金鑰訊息轉譯為字元訊息。 系統會將字元訊息張貼至呼叫執行緒的訊息佇列，以在下次執行緒呼叫 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) 函數時讀取。<br/>                                                                                                                                                                                                                                                                                                                            |
| [**WaitMessage**](/windows/win32/api/winuser/nf-winuser-waitmessage)                           | 當執行緒在其訊息佇列中沒有其他訊息時，會將控制項產生給其他執行緒。 [**WaitMessage**](/windows/win32/api/winuser/nf-winuser-waitmessage)函式會暫停執行緒，並且在將新訊息放入執行緒的訊息佇列之前不會傳回。<br/>                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="message-constants"></a>訊息常數



| Name                             | 描述                                                                    |
|----------------------------------|--------------------------------------------------------------------------------|
| [**OCM \_ \_ 基底**](ocm--base.md) | 用來定義私用訊息供私用視窗類別使用。 <br/> |
| [**WM \_ 應用程式**](wm-app.md)        | 用來定義私用訊息。 <br/>                                   |
| [**WM \_ 使用者**](wm-user.md)      | 使用 todefine 私用訊息以供私用視窗類別使用。 <br/>  |



 

### <a name="message-structures"></a>訊息結構



| Name                       | 描述                                                                                                                              |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**BSMINFO**](/windows/win32/api/winuser/ns-winuser-bsminfo) | 包含拒絕 [**BroadcastSystemMessageEx**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessageexa)要求的視窗相關資訊。 <br/> |
| [**味精**](/windows/win32/api/winuser/ns-winuser-msg)         | 包含來自執行緒之訊息佇列的訊息資訊。 <br/>                                                                  |



 

 

