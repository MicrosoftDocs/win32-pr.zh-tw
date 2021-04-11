---
description: 下表列出 WMI 預先安裝的永久取用者類別。
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: 標準取用者類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195231"
---
# <a name="standard-consumer-classes"></a>標準取用者類別

下表列出 WMI 預先安裝的永久取用者類別。 您可以建立這些類別的實例，以提供永久取用者類別，以提供在篩選中指定的事件所觸發時所回應的邏輯取用者。 例如，使用 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別來定義在指定的事件發生時所執行的腳本。

如需詳細資訊，請參閱使用標準取用者和[監視事件](monitoring-events.md)[來監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。



| 類別                                                                        | 描述                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | 當事件傳遞給它時，以任意指令碼語言執行預先定義的腳本。<br/> 範例： [根據事件執行腳本](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | 當事件傳遞給它時，會在本機系統內容中啟動任意進程。<br/> 範例： [根據事件從命令列執行程式](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | 將事件傳遞給文字記錄檔時，將自訂字串寫入至文字記錄檔。<br/> 範例：[根據事件寫入記錄](writing-to-a-log-file-based-on-an-event.md)檔<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | 將事件傳遞給 Windows 事件記錄檔時，會將特定訊息記錄到該記錄檔。<br/> 範例：[根據事件記錄至 NT 事件記錄](logging-to-nt-event-log-based-on-an-event.md)檔<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | 提供 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別的所有實例通用的註冊資料。<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | 每次傳遞事件給它時，使用 SMTP 傳送電子郵件訊息。<br/> 範例： [根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[監視事件](monitoring-events.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[根據事件執行腳本](running-a-script-based-on-an-event.md)
</dt> <dt>

[根據事件傳送電子郵件](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




