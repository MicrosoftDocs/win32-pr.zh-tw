---
title: 安全性系結
description: 安全性系結是安全性權杖的規格，可告知執行時間如何取得和使用安全性權杖來進行通道安全性。
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Windows 的安全性系結 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afc668e6dc6ab42e2d57066ecfb47ce337603bcadeccfb6b12a14a0e0550381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054538"
---
# <a name="security-bindings"></a>安全性系結

安全性系結是安全性權杖的規格，可告知執行時間如何取得和使用安全性權杖來進行通道安全性。 安全性權杖包含的資訊可擔保存取資源的許可權。 它可能也有相關聯的密碼編譯金鑰可執行簽章和加密。


每個安全性系結都包含它自己的選用安全性系結設定集合，其範圍 [設定](security-binding-settings.md) 為其所定義的安全性權杖。 它也包含 [安全性認證](security-credentials.md)，代表安全性辨識項 (例如使用者名稱和密碼，或建立安全性權杖所需) 憑證。

下列回呼是安全性系結的一部分：

-   [**WS \_ 驗證 \_ SAML \_ 回呼**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

下列列舉是安全性系結的一部分：

-   [**WS \_ 訊息 \_ 安全性 \_ 使用方式**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**WS \_ SAML \_ 驗證器 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**WS \_ 安全性系結 \_ \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**WS \_ 安全性 \_ 金鑰 \_ 控制碼 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

下列函數是安全性系結的一部分：

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

下列結構是安全性系結的一部分：

-   [**WS \_ CAPI \_ 非對稱 \_ 安全性 \_ 金鑰 \_ 控制碼**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**WS \_ CERT \_ 簽署的 \_ SAML \_ 驗證器**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**WS \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**WS \_ NAMEDPIPE \_ SSPI \_ TRANSPORT \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**WS \_ NCRYPT \_ 非對稱 \_ 安全性 \_ 金鑰 \_ 控制碼**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**WS \_ RAW \_ 對稱 \_ 安全性 \_ 金鑰 \_ 控制碼**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**WS \_ SAML \_ 驗證器**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**WS \_ SAML \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**WS \_ 安全性系結 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**WS \_ 安全性 \_ 金鑰 \_ 控制碼**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**WS \_ SSL \_ 傳輸 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**WS 使用者 \_ 名稱 \_ 訊息 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**WS \_ XML \_ 權杖 \_ 訊息 \_ 安全性 \_ 系結**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




