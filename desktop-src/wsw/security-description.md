---
title: 安全性描述
description: 安全性描述是以 WS \_ 安全性 \_ 描述結構表示，而當您呼叫 WsCreateChannel 函式來建立安全通道或 WsCreateListener 函式以建立接聽程式時，會提供安全性描述的實例。
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Windows 的安全性描述 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a2395e2c1e894968f47fa41e98599ec333f6d2724cf6ffe6cbc5219396bca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083155"
---
# <a name="security-description"></a>安全性描述

安全性描述是以 [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構表示，而當您呼叫 [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) 函式來建立安全通道或 [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) 函式以建立接聽程式時，會提供安全性描述的實例。


## <a name="structure-of-a-security-description"></a>安全性描述的結構

通道安全性的基本模型是使用一或多個安全性權杖來保護通道。 建立此模型時， [**ws \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構包含安全性系結的清單（由 [**ws \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) 系結結構所代表），而每個安全性系結會說明如何取得和使用通道上的一個安全性權杖。 通道上所使用的安全性類型是由安全性描述中所包含的安全性系結子類型選取專案所決定。

安全性系結特定的選用安全性設定會指定為安全性系結結構中的安全性系結 [設定](security-binding-settings.md);不過，與安全性系結無關的全通道設定，會直接在安全性描述本身的 [**屬性**] 欄位中指定為 [安全性通道設定](security-channel-settings.md)。

![顯示安全性描述結構的圖表。](images/securitydescription.png)

下列 API 元素會搭配安全性描述使用。

| 結構                                                    | 描述                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | 最上層結構，用來指定用戶端上的通道 (的安全性需求) 或伺服器端)  (的接聽程式。 |



 

 

 




