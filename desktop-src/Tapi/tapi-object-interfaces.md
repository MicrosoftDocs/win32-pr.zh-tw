---
description: TAPI 物件是 TAPI 3 的主要物件。
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: TAPI 物件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987298"
---
# <a name="tapi-object-interfaces"></a>TAPI 物件介面

[Tapi 物件](tapi-object.md)是 tapi 3 的主要物件。

[**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)介面不會直接在 TAPI 物件上公開，但與其緊密相關，並在此處列出以供參考之用。



| 介面                                                 | Description                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | 主要 TAPI 3 介面。                                                                                                                              |
| [**ITTAPI2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | 衍生自 [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi);提供支援電話裝置的其他方法。                                                         |
| [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | 輸出介面，用來接收有關 TAPI 3 事件的非同步資訊。                                                                       |
| [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | 將輸入介面提供給撥入中心控制項。                                                                                                 |
| [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | 提供方法來取得有關 TAPI 物件事件的資訊。                                                                                |
| [**ITTAPIObjectEvent2**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | 擴充 [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent);提供方法，以抓取造成 TAPI 物件事件的電話物件指標。 |



 

 

 
