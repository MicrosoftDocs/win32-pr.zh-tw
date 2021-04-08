---
title: NAP 介面
description: NAP 介面
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021958"
---
# <a name="nap-interfaces"></a>NAP 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

NAP 系統是由下列介面所組成。



| 介面名稱                                                                   | 描述                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | 提供憑證信賴憑證者必須用來與 NapAgent 通訊的方法。                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | 用於 SoH 快取和 SoH 交換觸發的 NAP 用戶端管理。 已取代。                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | 用於 SoH 快取和 SoH 交換觸發的 NAP 用戶端管理。                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | 用於 SHV 元件的自訂設定。 已取代。                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | 提供適用于系統健全狀況驗證程式的 NAP 系統組態方法 (Shv) 從遠端設定 NPS) 使用者介面的網路原則 (伺服器。   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | 提供適用于系統健全狀況驗證程式的 NAP 系統組態方法 (Shv) 設定和修改特定設定識別碼的設定資料。 |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | 必須由外掛程式元件（例如 Sha 和 Shv）來執行，才能透過 NAP 系統進行通訊。                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | 由強制用戶端用來與 NapAgent 通訊。                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | 強制用戶端必須執行這個介面，才能讓 NapAgent 與它們進行通訊。                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | 允許用戶端連接管理。 已取代。                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | 允許用戶端連接管理。                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | Shv 會在此介面上使用單一方法，以通知非同步要求完成。                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | 管理用戶端使用 (例如 WMI 提供者、命令列工具等 ) 來查詢 NAP 伺服器系統的狀態。                             |
| [**INapServerManagement**](inapservermanagement.md)                             | 用於 NAP 伺服器的基本管理。                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | 供 Sha 用來建立 SoH 要求以及由 Shv 建立 SoH 回應。                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | 供 Sha 用來處理 soh 回應的內容，以及由 Shv 處理 SoH 要求的內容。                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | Sha 必須使用此介面來與 NapAgent 通訊。 已取代。                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | Sha 必須使用此介面來與 NapAgent 通訊。                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | Sha 必須執行這個介面，以協調與 NAP 系統的處理。                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | Sha 使用此介面與 NAP 系統進行通訊並協調其處理。                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | 提供 SHV 必須實行的方法，讓 NAP 系統能夠與其進行通訊。                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | Shv 會將此介面用於與其用戶端對應的資料通訊。 已取代。                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | Shv 會將此介面用於與其用戶端對應的資料通訊。                                                                  |



 

 

 




