---
title: 服務授權
description: 應用程式可以針對服務主機上的內送訊息，執行自訂授權。
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Windows 的服務授權 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109838"
---
# <a name="service-authorization"></a>服務授權

應用程式可以針對服務主機上的內送訊息，執行自訂授權。


服務主機會收到安全性回呼 [**ws \_ 服務 \_ 安全性 \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)，作為傳送至 [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)函式之 [**ws \_ 服務 \_ 端點**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)的一部分。 收到 [WS \_ 訊息](ws-message.md) 時，就會叫用此回呼。

應用程式可以依賴此回呼，針對服務主機上的內送訊息執行自訂授權。 如果授權失敗，安全性回呼函式會傳回失敗的 HR，而服務主機會中止通道。

如需範例的範例，請參閱 [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md)的使用者名稱（透過 SSL）範例。

 

 




