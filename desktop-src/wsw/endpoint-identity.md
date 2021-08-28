---
title: 端點識別
description: 此區段中定義的類型是用來定義端點位址的安全性識別。
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Windows 的端點身分識別 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819fd2b33f1c74f88ef9032a49bd9aa4f04e34f1dcd4e599120951afabb6e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927588"
---
# <a name="endpoint-identity"></a>端點識別

此區段中定義的類型是用來定義端點位址的安全性識別。

下列 API 元素是端點識別的一部分：



| 列舉型別                                                       | 描述                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 端點身分 \_ 識別 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | 端點身分識別的型別，用來做為 [**WS \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)之子類型的選取器。 |



 



| 結構                                                               | 描述                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WS \_ CERT \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | 憑證端點身分識別的類型。                                                 |
| [**WS \_ DNS \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | 用來指定 DNS 名稱所代表之端點身分識別的型別。                      |
| [**WS \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | 所有端點身分識別的基底類型。                                                   |
| [**WS \_ RSA \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | 輸入 RSA 端點身分識別。                                                              |
| [**WS \_ SPN \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | 型別，用來指定由 SPN 表示的端點識別 (服務主體名稱) 。 |
| [**WS \_ 未知的 \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | 未知端點身分識別的類型。                                                   |
| [**WS \_ UPN \_ 端點身分 \_ 識別**](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | 用來指定 UPN 所代表之端點身分識別的型別 (使用者主體名稱) 。     |



 

 

 




