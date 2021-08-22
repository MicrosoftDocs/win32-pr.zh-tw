---
description: Kerberos 通訊協定是由三個 subprotocols 所組成。
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Kerberos Subprotocols
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ea1ababaf1ec7fe4e80112d4c1f69dc8bfc242a40cea56675d08198188a130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013358"
---
# <a name="kerberos-subprotocols"></a>Kerberos Subprotocols

[*Kerberos 通訊協定*](../secgloss/k-gly.md)是由三個 subprotocols 所組成。



| 子通訊協定                                                                         | 意義                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [驗證服務交換](authentication-service-exchange.md)<br/>   | 在此子通訊協定中， [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) 會為用戶端提供登入 [*工作階段金鑰*](../secgloss/s-gly.md) 和票證授權票證 (TGT) 。<br/> |
| [票證授權服務交換](ticket-granting-service-exchange.md)<br/> | 在此子通訊協定中，KDC 會散發服務工作階段金鑰和服務的票證。<br/>                                                                                                                                                                                                            |
| [用戶端/伺服器 Exchange](client-server-exchange.md)<br/>                     | 在此子通訊協定中，用戶端會提供服務的許可票證。<br/>                                                                                                                                                                                                                         |



 

 

 
