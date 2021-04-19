---
description: 撥置中心介面提供在撥打電話中心內佇列和散發呼叫的方法。
ms.assetid: 0b9a455d-a614-4698-90ab-e81f020fad3e
title: 撥置中心控制項快速參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfc34f1f30fc1f06d543cb7d5fa811517040523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976925"
---
# <a name="call-center-controls-quick-reference"></a>撥置中心控制項快速參考

撥置中心介面提供在撥打電話中心內佇列和散發呼叫的方法。 TAPI 3.x 定義五個主要的話務中心物件： ACDGroup、Agent、AgentHandler、AgentSession 和 Queue。 所有這些物件都可以擴充，以提供特定的執行方法。 此外，TAPI 物件上的 [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter) 介面也提供列舉 AgentHandler 物件的方法。



| 撥置中心介面                              | Description                                                              |
|----------------------------------------------------|--------------------------------------------------------------------------|
| [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)                   | 取得 ACD 群組的名稱和佇列資訊。                        |
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | 取得 ACD 群組事件的描述。                                    |
| [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)                         | 提供方法來設定和取得有關代理程式的資訊。         |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)的通知介面。                   |
| [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)           | 提供用來建立代理程式物件和列舉 ACD 群組的方法。       |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | 取得 AgentHandler 事件的描述。                                 |
| [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)           | 提供方法來設定和取得代理程式會話的相關資訊。 |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)的通知介面。     |
| [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                         | 取得和設定有關佇列的資訊。                            |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)               | 取得有關佇列事件的資訊。                               |
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)             | 列舉 [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)。                             |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)                   | 列舉 [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)。                                   |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler)     | 列舉 [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)。                     |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession)     | 列舉 [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)。                     |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                   | 列舉 [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)。                                   |



 

下列介面會根據 COM 標準來列舉 TAPI 3.x 元素。 這些介面會構成獨立的物件，而且也會以其相關物件摘要。



| 列舉值介面                           | Description                                          |
|------------------------------------------------|------------------------------------------------------|
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)         | 列舉 [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)。         |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)               | 列舉 [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)。               |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler) | 列舉 [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)。 |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession) | 列舉 [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)。 |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)               | 列舉 [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)。               |



 

事件 (通知) 介面可讓 TAPI 3.x 應用程式回應非同步事件。 您必須呼叫 [**ITTAPI：:p 的 \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) 方法，並設定事件篩選器遮罩，以啟用要求事件的接收。 如果您未呼叫 **ITTAPI：:p] \_ >eventfilter**，您的應用程式將不會收到任何事件。



| 事件介面                                    | Description                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------|
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | 抓取自動呼叫散發 (ACD) 群組事件的描述。 |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | 抓取代理程式事件的描述。                                   |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | 抓取代理程式處理程式事件的描述。                           |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | 抓取代理程式會話事件的描述。                           |



 

 

 
