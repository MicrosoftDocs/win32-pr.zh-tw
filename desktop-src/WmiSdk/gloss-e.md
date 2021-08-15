---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: 'E (WMI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319217"
---
# <a name="e-wmi"></a>E (WMI) 

[B](gloss-a.md) [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**事件類別**
</dt> <dd>

事件取用 *者* 可以透過 *事件查詢* 訂閱的 WMI 類別。 類別會報告特定類型的發生。 例如， [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) 類別會報告特定進程已停止。

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**事件取用者**
</dt> <dd>

報告事件發生之通知的接收者。 事件取用者是 [*暫時性*](gloss-t.md) 或 [*永久性*](gloss-p.md)。

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**事件取用者提供者**
</dt> <dd>

決定哪一個永久的事件消費者會處理給定之事件的提供者。 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)實例會向 WMI 註冊事件取用者提供者，其中包含事件取用者提供者所支援的 [*邏輯取用者*](gloss-l.md)類別清單。 事件取用者提供者是將 [*實體取用者*](gloss-p.md) 對應至 *邏輯取用者* 的 COM 伺服器。 事件取用者提供者支援 [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) 介面，且為永久取用者架構的元件。

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**事件篩選器**
</dt> <dd>

[**\_ \_ >Eventfilter**](--eventfilter.md)系統類別的實例，描述事件種類和傳遞通知的條件。 取用者會使用事件篩選器來註冊，以接收特定事件種類的通知。

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**事件提供者**
</dt> <dd>

WMI 提供者，可監視事件的來源，並在事件發生時通知 WMI。 事件提供者會執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) 介面，有時也會 [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)。

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**事件查詢**
</dt> <dd>

事件取用者用來註冊的 [*WMI 查詢語言*](gloss-w.md) 語句，以接收特定事件的通知。 事件提供者使用事件查詢來登錄要產生特定事件的告知。

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**延伸模組架構**
</dt> <dd>

[*cim 架構*](gloss-c.md)的第三層，包括 cim 架構的平臺專屬延伸模組，例如 Windows、UNIX 和 Exchange Server。 另請參閱 [*常見的模型*](gloss-c.md) 和核心模型。

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**外來事件**
</dt> <dd>

來自提供者的事件通知。 大部分的提供者會建立提供者 MOF 檔案中定義之事件類別的實例。 外來事件繼承自 [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md)。 例如， [事件記錄檔提供者](/previous-versions/windows/desktop/eventlogprov/event-log-provider) 會定義事件類別 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)。 另請參閱 [*內部事件*](gloss-i.md)。

</dd> </dl>

 

 
