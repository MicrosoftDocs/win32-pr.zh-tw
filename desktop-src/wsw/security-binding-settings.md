---
title: 安全性繫結設定
description: 安全性系結設定可控制取得或使用安全性權杖的方式。
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- 適用于 Windows 的安全性系結設定 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684239"
---
# <a name="security-binding-settings"></a>安全性繫結設定

安全性系結設定可控制取得或使用安全性權杖的方式。 它們會表示為屬性值組的集合，以及由列舉 [**WS 安全性系結 \_ \_ \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property)定義的屬性索引鍵。 集合中的每個屬性都有合理的預設值。 因此，您可以定義和使用安全性描述，而不需要指定任何安全性系結設定。


如需全通道安全性設定的詳細資訊，以及其索引鍵是由 [**WS \_ 安全性 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 列舉所定義的屬性，請參閱 [安全性通道設定](security-channel-settings.md)。

下列 API 元素會搭配安全性系結設定使用。

| 列舉型別                                                                          | 描述                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ 憑證 \_ 失敗**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | 定義與憑證驗證相關的失敗。                                                                                                               |
| [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 配置**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | 定義使用 HTTP 驗證標頭執行用戶端驗證的選項。                                                                       |
| [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 目標**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | 定義 HTTP 標頭驗證安全性系結的目標。                                                                                           |
| [**WS \_ 要求 \_ 安全性 \_ 權杖 \_ 動作**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | 定義使用 WS-TRUST 來協商安全性權杖時要使用的動作集合。                                                                              |
| [**WS \_ 安全性 \_ 演算法 \_ 套件 \_ 名稱**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | 用於簽署和 encryting 等工作的安全性演算法套件。                                                                                      |
| [**WS \_ 安全性系結 \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | 識別用來指定安全性系結設定的屬性。                                                                                              |
| [**WS \_ 安全性 \_ 金鑰 \_ 熵 \_ 模式**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | 定義在使用訊息和混合模式安全性完成安全性權杖協商期間，如何為發出的金鑰貢獻隨機性。                     |
| [**WS \_ 安全性 \_ 金鑰 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | 安全性權杖的金鑰類型。                                                                                                                                 |
| [**WS \_ 安全性 \_ 權杖 \_ 參考 \_ 模式**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | 在訊息和混合模式安全性系結的內容中，用來參考來自簽章、加密專案和衍生標記之安全性權杖的機制。 |
| [**WS \_ 信任 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | 定義要搭配訊息安全性和混合模式安全性使用的 WS-Trust 規格版本。                                                              |
| [**WS \_ WINDOWS \_ 整合式 \_ 驗證 \_ 套件**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | 定義要用於 Windows 整合式驗證的特定 SSP 套件。                                                                                |



 



| 結構                                                               | Description                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**WS \_ 安全性系結 \_ \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | 指定安全性系結特定設定。 |



 

 

 




