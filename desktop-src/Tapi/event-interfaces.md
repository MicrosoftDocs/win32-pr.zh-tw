---
description: 事件 (通知) 介面可讓 TAPI 3 應用程式回應非同步事件。
ms.assetid: 27fd91e8-b628-49ee-af4e-9aec0afa5449
title: 事件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7b705c89988ff62d972e594ceb936bb01db78e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511540"
---
# <a name="event-interfaces"></a>事件介面

事件 (通知) 介面可讓 TAPI 3 應用程式回應非同步事件。

您必須呼叫 [**ITTAPI：:p 的 \_ >eventfilter**](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) 方法，並設定事件篩選器遮罩，以啟用要求事件的接收。 如果您未呼叫 **ITTAPI：:p] \_ >eventfilter**，您的應用程式將不會收到任何事件。

如需應用程式如何確保接收通知的說明，請參閱 [事件](./asynchronous-spontaneous-events.md) 總覽。 如需有關為個別事件種類設定篩選遮罩的詳細資訊，請參閱下表所列的個別介面。



| 介面                                                           | 描述                                                                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddressEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itaddressevent)                   | 抓取位址事件的描述。                                                                                                |
| [**ITASRTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itasrterminalevent)           | 抓取自動語音辨識終端機事件的描述。                                                                  |
| [**ITCallHubEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallhubevent)                   | 捕獲 CallHub 事件的描述。                                                                                                |
| [**ITCallInfoChangeEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallinfochangeevent)     | 抓取呼叫資訊變更事件的描述。                                                                                |
| [**ITCallMediaEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallmediaevent)               | 抓取通話媒體事件的描述。                                                                                             |
| [**ITCallNotificationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallnotificationevent) | 抓取呼叫通知事件的描述。                                                                                      |
| [**ITCallStateEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itcallstateevent)               | 抓取撥號狀態事件的描述。                                                                                             |
| [**ITDigitDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitdetectionevent)     | 在呼叫期間捕獲 DTMF 數位事件的相關資訊。                                                                                |
| [**ITDigitGenerationEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitgenerationevent)   | 抓取需要產生 DTMF 數位之呼叫的相關資訊。                                                               |
| [**ITDigitsGatheredEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itdigitsgatheredevent)     | 抓取與應用程式數位收集要求相關的資料。                                                                         |
| [**ITFileTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itfileterminalevent)         | 抓取檔終端機事件的描述。                                                                                          |
| [**ITParticipantEvent**](./itparticipantevent.md)           | 抓取會議參與者事件的描述。                                                                                 |
| [**ITPhoneEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itphoneevent)                       | 抓取電話事件的描述。                                                                                                  |
| [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)                           | 抓取服務品質 (QOS) 事件的描述。                                                                               |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)                       | 抓取自動呼叫散發 (ACD) 佇列事件的描述。                                                                |
| [**ITRequestEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itrequestevent)                   | 抓取 [輔助電話語音](./assisted-telephony-overview.md) 要求事件的描述。                                 |
| [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | 捕獲 TAPI 物件事件的描述。                                                                                            |
| [**ITTAPIObjectEvent2**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | 擴充 [**ITTAPIObjectEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittapiobjectevent);抓取造成 TAPI 物件事件的電話物件指標。 |
| [**ITToneDetectionEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittonedetectionevent)       | 抓取語氣偵測事件的相關資訊。                                                                                         |
| [**ITToneTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-ittoneterminalevent)         | 抓取語氣終端機事件的描述。                                                                                          |
| [**ITTTSTerminalEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itttsterminalevent)           | 抓取文字轉換語音 (TTS) 終端機事件的描述。                                                                          |



 



| 介面                                                                                             | 描述                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalEventSink**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsink)                         | 通知用戶端應用程式有關插入式終端機中的變更。                              |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/win32/api/tapi3/nn-tapi3-itpluggableterminaleventsinkregistration) | 註冊和取消註冊用戶端應用程式，以取得可插入終端機事件的通知。 |



 

 

 
