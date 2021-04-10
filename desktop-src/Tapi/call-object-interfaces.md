---
description: 呼叫物件會在呼叫存在時建立。 相關聯的介面會取得並設定有關呼叫的資訊。
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: 呼叫物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944346"
---
# <a name="call-object-interfaces"></a>呼叫物件介面

呼叫 [物件](call-object.md) 會在呼叫存在時建立。 相關聯的介面會取得並設定有關呼叫的資訊。

列舉值和事件介面不會直接在呼叫物件上公開，而是在這裡列出，以供參考便利性之用。

[**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)、 [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)、 [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)、 [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)和 [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)介面不會直接在呼叫物件上公開，但與其緊密相關，並在此處列出以供參考便利性。



| 介面                                                      | 描述                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | 提供有關呼叫物件的資訊，例如撥號狀態或使用中的終端機。                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | 藉由提供方法來針對個別呼叫來設定事件篩選，來擴充 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) 。                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | 用來連接、回答和執行呼叫物件上的基本電話語音作業。                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | 藉由提供方法讓您選取終端機進行呼叫，以擴充 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) 。              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)的通知介面。                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | 呼叫資訊變更的通知介面。                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | 取得有關呼叫事件的資訊。                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | 取得有關通話媒體事件的資訊。                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | 提供方法來控制某些電話組可能的自訂音調。                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | 提供方法來指定產生色調事件的色調和音調特性。                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | 支援必須直接與裝置通訊的繼承應用程式。                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | 藉由提供音調偵測和產生的方法來擴充 [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) 。 |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | 列舉 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)。                                                                                 |



 

 

 



