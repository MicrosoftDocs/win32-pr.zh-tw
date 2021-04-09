---
description: IP 會議 MSP 會為參與者控制項實作為提供者專用的數個介面。 如果此 MSP 與呼叫相關聯，則會在呼叫物件上公開這些介面。
ms.assetid: 01af2452-de2d-42ce-970d-82a83ae0b428
title: IPConf MSP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edb3c04a93909d237ae25e06c3ed2e0fcc5db9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114928"
---
# <a name="ipconf-msp-interfaces"></a>IPConf MSP 介面

\[ IPConf MSP 介面無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

IP 會議 MSP 會為參與者控制項實作為提供者專用的數個介面。 如果此 MSP 與呼叫相關聯，則會在呼叫物件上公開這些介面。

[**ITParticipantEvent**](itparticipantevent.md)和 [**IEnumParticipant**](ienumparticipant.md)介面是獨立的物件，此處會列出以供參考之用。



| 介面                                            | 描述                                                                                                                                               |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMulticastControl**](imulticastcontrol.md)       | 允許應用程式為多播會議物件設定和取得 ( [**多播 \_ 回送 \_ 模式**](multicast-loopback-mode.md)) 的回送模式。 |
| [**ITParticipant**](itparticipant.md)               | 允許應用程式抓取會議參與者的資訊，以及取得與這些參與者相關聯之資料流程的指標。             |
| [**ITParticipantControl**](itparticipantcontrol.md) | 允許應用程式取得會議中參與者的指標。                                                                           |
| [**ITParticipantEvent**](itparticipantevent.md)     | 允許應用程式抓取有關會議參與者的事件資訊。                                                                  |
| [**IEnumParticipant**](ienumparticipant.md)         | 列舉 [**ITParticipant**](itparticipant.md)。                                                                                                        |



 

 

 



