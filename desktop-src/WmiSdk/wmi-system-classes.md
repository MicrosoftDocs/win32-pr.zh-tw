---
description: WMI 系統類別是以通用訊息模型 (CIM) 為基礎的預先定義類別集合。
ms.assetid: 1a0323af-7c87-4016-9041-480518f3870a
ms.tgt_platform: multiple
title: WMI 系統類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cdee69b641fdbfdc006bdcef6d066687308ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971605"
---
# <a name="wmi-system-classes"></a>WMI 系統類別

WMI 系統類別是以 [*通用訊息模型 (CIM)*](gloss-c.md)為基礎的預先定義類別集合。 不同于提供者所提供的類別，系統類別不會在 [*受控物件格式 (MOF)*](gloss-m.md) 檔中宣告。 每當建立新的 WMI [*命名空間*](gloss-n.md) 時，WMI 就會建立一組這些類別。

系統類別中的物件是用來支援 WMI 活動，例如：事件和提供者註冊、安全性和事件通知。 某些物件是暫時性的，有些則是以系統類別的實例的形式儲存在存放庫中。

系統類別會遵循包含雙底線 (\_ \_) 後面接著類別名稱的命名慣例。 當您撰寫 MOF 檔案來定義 WMI [*提供者*](gloss-p.md)的類別時， [**Mofcomp.exe**](mofcomp.md)不會編譯具有初始雙底線 () 的任何類別， \_ \_ 因為這是保留給 wmi 系統類別名稱。

系統類別的檔只包含非系統的本機屬性。 類別定義中會提供連結，讓您可以快速且輕鬆地流覽類別階層。

## <a name="wmi-system-classes"></a>WMI 系統類別

下表列出各種系統類別。



| System 類別                                                                         | Description                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md)                   | 導致在特定時間于特定日期產生事件。                                                                                                                               |
| [**\_\_Ace**](--ace.md)                                                             | 表示存取控制項目 (ACE)。                                                                                                                                                            |
| [**\_\_AggregateEvent**](--aggregateevent.md)                                       | 代表數個個別內建或外來事件的匯總事件。                                                                                                                   |
| [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md)                     | 設定類別，限制由 WMI 用戶端所起始的作業所使用的內部資源。                                                                                         |
| [**\_\_CacheControl**](--cachecontrol.md)                                           | 判斷 WMI 何時應該釋放元件物件模型 (COM) 物件。                                                                                                                            |
| [**\_\_CIMOMIdentification**](--cimomidentification.md)                             | 描述 WMI 的本機安裝。                                                                                                                                                             |
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                               | 表示類別建立事件，這是將新類別加入至命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。                          |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                               | 表示類別刪除事件，這是從命名空間移除類別時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。                          |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)                       | 表示類別修改事件，這是在命名空間中的類別變更時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。                        |
| [**\_\_ClassOperationEvent**](--classoperationevent.md)                             | 所有與類別相關之內建事件的基類。                                                                                                                                        |
| [**\_\_ClassProviderRegistration**](--classproviderregistration.md)                 | 在 WMI 中註冊類別提供者。                                                                                                                                                                    |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)                           | 代表由於事件取用者失敗而卸載的某個其他事件的發生次數。                                                                                     |
| [**\_\_事件**](--event.md)                                                         | 抽象基類，做為所有內建和外來事件的父類別。                                                                                                       |
| [**\_\_EventConsumer**](--eventconsumer.md)                                         | 用來註冊永久事件取用者的抽象基類。                                                                                                               |
| [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md) | 決定 WMI 何時應該釋放事件取用者提供者。                                                                                                                                       |
| [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) | 向 WMI 註冊事件取用者提供者。                                                                                                                                                         |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                                 | 表示已卸載之事件的發生次數。 卸載的事件是未傳遞給事件取用者的事件。                                                                       |
| [**\_\_>eventfilter**](--eventfilter.md)                                             | 註冊永久事件取用者需要 [**\_ \_ >eventfilter**](--eventfilter.md)系統類別的實例。                                                                        |
| [**\_\_EventGenerator**](--eventgenerator.md)                                       | 作為控制事件產生（例如 [計時器事件](receiving-a-timed-or-repeating-event.md)）之類別的父類別。                                                        |
| [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)                 | 控制何時卸載事件提供者。                                                                                                                                                         |
| [**\_\_EventProviderRegistration**](--eventproviderregistration.md)                 | 向 WMI 註冊事件提供者。                                                                                                                                                                  |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)                     | 報告因為傳遞佇列溢位而捨棄事件。                                                                                                                             |
| [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)                         | 用來判斷 WMI 何時釋放事件取用者提供者的 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) 指標。                                                                   |
| [**\_\_ExtendedStatus**](--extendedstatus.md)                                       | 用來報告詳細的狀態和錯誤資訊。                                                                                                                                                |
| [**\_\_ExtrinsicEvent**](--extrinsicevent.md)                                       | 作為所有使用者定義事件種類（也稱為外建 [事件](determining-the-type-of-event-to-receive.md)）的父類別。                                                           |
| [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md)                     | 用於永久事件取用者的註冊，以便將 [**\_ \_ EventConsumer**](--eventconsumer.md)的實例與 [**\_ \_ >eventfilter**](--eventfilter.md)的實例產生關聯。       |
| [**\_\_IndicationRelated**](--indicationrelated.md)                                 | 作為所有事件相關類別的父類別。                                                                                                                                              |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)                         | 報告實例建立事件，這是在新的實例新增至命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。              |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)                         | 報告實例刪除事件，這是從命名空間中刪除實例時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。                     |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)                 | 報告實例修改事件，這是在命名空間中的實例變更時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。                      |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)                       | 作為與實例相關之所有內建事件的基類。                                                                                                                          |
| [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md)           | 在 WMI 中註冊執行個體提供者。                                                                                                                                                                 |
| [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md)                   | 依時間間隔產生事件，類似于 Windows 程式設計中的 [**WM \_ 計時器**](/windows/desktop/winmsg/wm-timer) 訊息。                                                                                         |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)                         | 這個類別不會實作為。                                                                                                                                                                       |
| [**\_\_MethodProviderRegistration**](--methodproviderregistration.md)               | 使用 WMI 註冊方法提供者。                                                                                                                                                                 |
| [**\_\_命名空間**](--namespace.md)                                                 | 表示 WMI 命名空間。                                                                                                                                                                          |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)                       | 報告命名空間建立事件，這是將新的命名空間新增至目前的命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。             |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)                       | 報告命名空間刪除事件，這是從目前命名空間移除子命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。 |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md)               | 報告命名空間修改事件，這是在修改命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md) 類型。                           |
| [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md)                     | 所有與命名空間相關之內建事件的基類。                                                                                                                                    |
| [**\_\_NotifyStatus**](--notifystatus.md)                                           | 作為提供者定義之錯誤類別的父類別。                                                                                                                                       |
| [**\_\_NTLMUser9X**](--ntlmuser9x.md)                                               | 控制執行不支援之 Windows 版本之電腦的遠端存取。                                                                                                                        |
| [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)               | 控制何時卸載類別或執行個體提供者。                                                                                                                                              |
| [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md)               | 作為用來在 WMI 中註冊類別和執行個體提供者之類別的父系。                                                                                                      |
| [**\_\_參數**](--parameters.md)                                               | 定義方法的輸入和輸出參數。                                                                                                                                                 |
| [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)           | 當卸載屬性提供者時，控制快取。                                                                                                                                             |
| [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md)           | 在 WMI 中註冊屬性提供者。                                                                                                                                                                 |
| [**\_\_提供者**](--provider.md)                                                   | 作為 [**\_ \_ Win32Provider**](--win32provider.md)系統類別的父類別。                                                                                                        |
| [**\_\_ProviderHostQuotaConfiguration**](--providerhostquotaconfiguration.md)       | 允許在主機進程使用系統資源時設定限制。                                                                                                                                   |
| [**\_\_ProviderRegistration**](--providerregistration.md)                           | 作為各種提供者類型之註冊類別的父類別。                                                                                                                  |
| [**\_\_SecurityDescriptor**](--securitydescriptor.md)                               | 表示 [*安全描述項*](/windows/desktop/SecGloss/s-gly)。                                                                            |
| [**\_\_SecurityRelatedClass**](--securityrelatedclass.md)                           | 作為所有型別安全性類別的父類別。                                                                                                                                          |
| [**\_\_SystemClass**](--systemclass.md)                                             | 從中衍生大部分系統類別的基類。                                                                                                                                                    |
| [**\_\_SystemEvent**](--systemevent.md)                                             | 表示系統事件。                                                                                                                                                                           |
| [**\_\_SystemSecurity**](--systemsecurity.md)                                       | 包含方法，可讓您存取和修改命名空間的安全性設定。                                                                                                               |
| [**\_\_thisNAMESPACE**](--thisnamespace.md)                                         | 以安全描述項的形式保存命名空間的安全性許可權。                                                                                                                    |
| [**\_\_TimerEvent**](--timerevent.md)                                               | 報告 WMI 產生的事件，以回應取用者對間隔計時器事件或絕對計時器事件的要求。                                                                        |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                   | 指定如何為取用者產生 [計時器事件](receiving-a-timed-or-repeating-event.md) 的指示。                                                                            |
| [**\_\_TimerNextFiring**](--timernextfiring.md)                                     | 保留供作業系統使用。                                                                                                                                                                   |
| [**\_\_受託 人**](--trustee.md)                                                     | 表示 [*信任者*](/windows/desktop/SecGloss/t-gly)。 您可以使用 (位元組陣列的名稱或 SID) 。                                                               |
| [**\_\_Win32Provider**](--win32provider.md)                                         | 在 WMI 中註冊提供者實體執行的相關資訊。                                                                                                                             |



 

 

 
