---
title: 開始就支援
description: 「擴充保護」是一種機制，可將外部安全通道（例如 SSL）系結至內部通道驗證通訊協定，例如 Kerberos APREQ 和 HTTP 標頭驗證。
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- 擴充保護原生 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e327d929b77108c1b675e6f42a311e4cad6dd9a056e5ac38b6d7e7f4558788c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927539"
---
# <a name="extended-protection"></a>開始就支援

「擴充保護」是一種機制，可將外部安全通道（例如 SSL）系結至內部通道驗證通訊協定，例如 Kerberos APREQ 和 HTTP 標頭驗證。

擴充保護的概念是在 RFC2743 中定義。

如果有擴充保護，則會自動在用戶端上設定，但在伺服器上可能需要針對非預設案例進行設定。

## <a name="supported-configurations"></a>支援的組態

使用 Windows 整合式驗證通訊協定（例如 [**ws \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)系結和 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結）搭配安全性系結使用 [**WS \_ HTTP \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)系結時，支援擴充保護。 它是透過下列 [**安全性屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)進行設定：

-   [**WS \_ 安全性 \_ 屬性 \_ 延伸 \_ 保護 \_ 原則**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**WS \_ 安全性 \_ 屬性 \_ 擴充 \_ 保護 \_ 案例**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**WS \_ 安全性 \_ 屬性 \_ 服務 \_ 身分識別**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

以下是可能涉及擴充保護的設定：

用戶端

-   [**WS \_SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) 系結會與 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結或 [**ws \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)系結搭配使用。 在這項設定中，驗證系結會透過從 SSL 連線自動解壓縮的延伸保護權杖，系結至 SSL 連線。
-   未使用任何 SSL，且已設定 [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) 系結。 驗證系結會透過伺服器主體名稱 (SPN) 來系結，autonatically 由 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)決定。

伺服器

-   [**WS \_SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) 系結會與 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結或 [**ws \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)系結搭配使用。 在這項設定中，驗證系結會透過擴充保護權杖系結至 SSL 連線，此權杖會從 SSL 連線中解壓縮並自動驗證。
-   未使用任何 SSL，且已設定 [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) 系結。 驗證系結會透過伺服器主體名稱系結 (SPN) ，必須透過 [**WS \_ 安全性 \_ 屬性 \_ 服務 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)識別來提供。 收到訊息時，會將 SPN 解壓縮，並驗證是否完全符合所提供的服務名稱。 未提供 Spn 等同于設定 [**WS \_ 延伸 \_ 保護 \_ 原則 \_ 永不**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)如此。
-   未使用任何 SSL、已指定 [**ws \_ 擴充 \_ 保護 \_ 案例 \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) 系結伺服器，且使用 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結。 在此設定中，不能設定 [**WS \_ SECURITY \_ PROPERTY \_ SERVICE \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 身分識別。 除了 Kerberos 通訊協定的一部分以外，不會執行任何 SPN 檢查。
-   [**WS \_已指定擴充 \_ 保護 \_ 案例 \_ 終止的 \_ SSL**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) ，且使用 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結或 [**ws \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) 系結。 [**WS \_必須設定安全性 \_ 屬性 \_ 服務 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 識別。

## <a name="supported-platforms"></a>支援的平台

在作業系統中支援擴充保護的平臺支援。 Windows 7 和 Windows Server 2008 R2 提供內建支援。 其他平臺可能需要更新。

如果伺服器的作業系統未提供這類支援，用戶端傳送的任何擴充保護資訊都會被忽略。 如此一來，使用擴充保護的用戶端就可以與這類伺服器通訊，但會遺失安全性優勢。 在用戶端上， [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結與 [**ws \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) 系結結合，只支援 Vista 和更新版本的擴充保護。

注意：無法使用擴充保護，因此不會防止使用任何特定設定。

## <a name="interoperability"></a>互通性

預設設定的伺服器可以與 SOAP 用戶端通訊，而不論它們是否使用擴充保護。 其中一個例外狀況是 Windows XP 和 Windows Server 2003 WWSAPI 用戶端，這些用戶端已更新為支援擴充保護，並且使用 [**ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結和 [**ws \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結。 若要支援這類用戶端，您永遠都不能指定伺服器所指定的 [**WS \_ 延伸 \_ 保護 \_ 原則 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) 。 使用 **WS \_ 延伸 \_ 保護 \_ 原則 \_** 設定的伺服器一律會拒絕不使用擴充保護的用戶端進行通訊。 在用戶端上， **ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_** 系結與 **ws \_ SSL \_ 傳輸 \_ 安全性 \_** 系結結合之後，將會使用 Vista 和更新版本上的 HTTP 區塊傳輸編碼來傳送訊息。 這可能會造成不支援區區塊轉送的伺服器發生互通性問題。

下列列舉/常數屬於擴充保護的一部分：

-   [**WS \_ 延伸 \_ 保護 \_ 原則**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**WS \_ 擴充 \_ 保護 \_ 案例**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

下列結構是擴充保護的一部分：

-   [**WS \_ 服務 \_ 安全性身分識別 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




