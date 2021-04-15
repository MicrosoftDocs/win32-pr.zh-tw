---
title: 安全性概觀
description: Windows Web 服務 API 中的安全性架構 (WWSAPI) 提供使用傳輸安全性的訊息完整性、機密性、重新執行偵測和伺服器驗證。
ms.assetid: 2681bffc-ba07-4822-b265-2bf7f95297d4
keywords:
- 適用于 Windows 的安全性概觀 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741e98ef023c0bae146b5fde582484f2dd133df6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463472"
---
# <a name="security-overview"></a>安全性概觀

Windows Web 服務 API 中的安全性架構 (WWSAPI) 提供：

-   使用傳輸安全性的訊息完整性、機密性、重新執行偵測和伺服器驗證。
-   使用 SOAP 訊息安全性或傳輸安全性的用戶端驗證，例如安全性權杖驗證、憑證信任和撤銷檢查等等。

## <a name="the-security-programming-model"></a>安全性程式設計模型

安全性[與通道相關聯。](channel-layer-overview.md) 保護通道是由下列步驟所組成。

-   建立並初始化適用于應用程式安全性需求的一或多個 [**安全性**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) 系結。
-   建立包含這些安全性系結的 [**安全性描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 。
-   在用戶端) 上建立 [**通道**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)或 [**服務 proxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (，或在伺服器端建立接聽 [**程式或**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)[**服務主機**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) (，) 傳遞該安全性描述。
-   進行開啟、接受、傳送、接收、關閉等的一般通道程式設計步驟。

在通道上傳送和接收的訊息，會根據提供的安全性描述自動受到執行時間的保護。 （選擇性）您可以在安全性系結中指定一或多個全 [通道安全性設定](security-channel-settings.md) ，或在安全性系結中指定整個系結 [安全性設定](security-binding-settings.md) ，以微調這些步驟。

任何需要的寄件者身分識別授權，都必須由應用程式使用附加至每個接收訊息的 [安全性處理結果](security-processing-results.md) 來完成。 安全性描述中未指定授權步驟，而且執行時間不會自動執行。

安全性描述中的錯誤，例如不支援的系結、不適用屬性/欄位、缺少必要屬性/欄位或不正確屬性/域值，將導致通道或接聽程式建立失敗。

## <a name="selecting-security-bindings"></a>選取安全性系結

設計應用程式的安全性時，主要決定是要包含在安全性描述中的安全性系結選取。 以下是一些指導方針，可讓您選擇適用于應用程式安全性案例的安全性系結。 有用的啟發學習法是先瞭解 (的安全性認證類型，例如 [**x.509 憑證**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)、 [**Windows 網域使用者名稱/密碼**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)、 [**應用程式定義的使用者名稱/密碼**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)) 將可供應用程式使用，然後選擇可以使用該認證類型的安全性系結。

-   安全性會套用至傳輸位元組資料流程層級 (在 SOAP 訊息界限) 底下的傳輸安全性，是第一個要考慮的選項。
    -   針對網際網路案例，以及可在伺服器上部署 x.509 憑證的內部網路案例中，應用程式可能會使用 [**WS \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結。 下列範例說明此選項。 Client： [HttpClientWithSslExample](httpclientwithsslexample.md) Server： [HttpServerWithSslExample](httpserverwithsslexample.md)。

        如果需要透過 HTTP 標頭驗證進行用戶端驗證，則可以新增 [**WS \_ HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) 系結來提供該功能。

    -   若是適用于 Windows 整合式驗證通訊協定（例如 Kerberos、NTLM 和 SPNEGO）的內部網路案例，應用程式可能會使用 [**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)系結。 下列範例說明此選項： Client： [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md) Server： [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md)。

        用戶端 over 具名管道： [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)

        伺服器 over 具名管道： [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)

    -   針對 Windows 整合式驗證通訊協定（例如 Kerberos、NTLM 和 SPNEGO）的本機電腦案例，應用程式可能會使用 [**ws \_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) 系結或 [**ws \_ NAMEDPIPE \_ SSPI \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)系結。 [**Ws \_ NAMEDPIPE \_ 通道系結在這 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)種情況下是慣用的，因為它可確保流量不會離開電腦 (這是 **WS \_ NAMEDPIPE \_ 通道 \_** 系結) 的屬性。

-   混合模式安全性，其中傳輸安全性可保護連接，而 SOAP 訊息中的 WS-Security 標頭會提供用戶端驗證，是下一個要考慮的選項。 下列系結會與上一節所述的其中一個傳輸安全性系結搭配使用。
    -   當用戶端是由應用層級的使用者名稱/密碼組進行驗證時，應用程式可以使用 [**WS 使用者 \_ 名稱 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) 系結來提供驗證資料。 下列範例說明如何使用此系結搭配 [**WS \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結：
        -   用戶端： [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)
        -   伺服器： [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)
    -   當用戶端由 Kerberos 票證進行驗證時，應用程式可以使用 [**WS \_ Kerberos \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結來提供驗證資料。
    -   使用 [安全性內容](security-context.md)時，用戶端會先建立與伺服器的安全性內容，然後使用該內容來驗證訊息。 若要啟用此功能，安全性描述必須包含 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系結。 一旦建立之後，就可以透過輕量權杖來傳輸安全性內容，這樣可避免必須在每個訊息中傳送可能耗用大量和計算成本的用戶端認證。
    -   在 [聯合安全性](federation.md) 案例中，用戶端會先取得安全性權杖服務所發出的安全性權杖 (STS) ，然後將發行的權杖提供給服務。 用戶端：若要從 STS 取得安全性權杖，應用程式可以使用 [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken)。 或者，應用程式可能會使用用戶端安全性權杖提供者程式庫（例如 CardSpace 或 LiveID），然後使用其輸出在本機建立使用 [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)的安全性權杖。 無論何種方式，當安全性權杖可供用戶端使用時，它可能會使用包含 [**WS \_ XML \_ 權杖 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)系結的安全性描述來呈現給服務。 伺服器端：如果 STS 所發行的安全性權杖是 SAML 權杖，則伺服器可能會使用具有 [**WS \_ SAML \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)系結的安全性描述。
        > [!Note]  
        > Windows 7 和 Windows Server 2008 R2： WWSAPI 只支援[輕量 Web 服務安全性設定檔 (LWSSP) ](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e)所定義的[ws-trust](http://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf)和[ws-SecureConversation](http://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) 。 如需有關 Microsoft 執行的詳細資訊，請參閱 LWSSP 的 [訊息語法](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) 一節。

         
-   最後一個要考慮的選項是使用驗證系結，而不使用保護系結，例如 [**WS \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)系結。 這會導致以純文字方式傳輸認證，而且可能會影響安全性。 應謹慎地評估使用此選項，以確保不會產生任何弱點。 有可能使用的範例是透過安全的私人網路，在後端伺服器之間交換訊息。 下列設定支援此選項。

    -   [**WS \_HTTP \_ 標頭 \_ 驗證 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) 系結在所有設定中都支援此選項。
    -   [**WS \_使用 HTTP 做為傳輸時，使用者名稱 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) 系結可在伺服器上支援這個選項。
    -   [**WS \_當使用 HTTP 做為傳輸時，KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) 系結支援伺服器上的這個選項。
    -   [**WS \_使用 HTTP 做為傳輸時，安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) 系結可在伺服器上支援這個選項。
    -   [**WS \_使用 HTTP 做為傳輸時，SAML \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding) 系結可在伺服器上支援這個選項。

    啟用此選項需要明確地將 [**ws \_ 保護 \_ 等級**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level) 設定為 **ws \_ 保護 \_ 層級 \_ 正負號 \_ 和 \_ 加密** 以外的值。

## <a name="channels-and-security"></a>通道和安全性

如先前所述，安全性的範圍是通道。 此外，通道作業會在所有安全性系結間一致地對應到安全性步驟。

-   通道建立：驗證安全性描述中指定的一組安全性系結，之後仍會為通道保持固定。 通道堆疊的形狀，包括用於以 WS-Trust 為基礎之協商的任何側邊通道，也會加以決定。
-   通道開啟：系統會載入安全性系結中提供的任何認證，並建立安全性會話。 一般而言，開啟的通道會包含「即時」安全性狀態。 開啟用戶端通道也會指定伺服器的端點位址，以供執行時間執行伺服器驗證。
-   在通道開啟和關閉之間：可在此階段安全地傳送和接收訊息。
-   訊息傳送：系統會視需要取得或更新安全性內容權杖，並根據安全性描述將安全性套用到每個傳輸的訊息。 套用安全性時所發生的錯誤會以傳送錯誤的形式傳回給應用程式。
-   訊息接收：根據安全性描述，在每個接收的訊息上驗證安全性。 任何訊息安全性驗證錯誤都會以接收錯誤的形式傳回給應用程式。 這些每個訊息的錯誤不會影響通道狀態或後續的接收。 應用程式可能會捨棄失敗的接收，並重新啟動另一個訊息的接收。
-   通道中止：通道可能會在任何時間中止，以中止通道上的所有 i/o。 在中止時，通道將會進入錯誤狀態，而且不會允許任何更多的傳送或接收。 不過，通道可能仍會保留一些「即時」安全性狀態，因此需要關閉後續通道，才能完全處置所有狀態。
-   通道關閉：已處置在開啟時建立的安全性狀態，並將會話中斷。 已取消安全性內容權杖。 通道堆疊會保持不變，但不包含「即時」安全性狀態或已載入的認證。
-   通道可用：在建立時建立的通道堆疊以及所有安全性資源都會釋出。

## <a name="security-apis"></a>安全性 Api

安全性的 API 檔分為下列主題。

-   [安全性描述](security-description.md)
    -   [安全性通道設定](security-channel-settings.md)
    -   [安全性系結](security-bindings.md)
        -   [安全性認證](security-credentials.md)
        -   [安全性繫結設定](security-binding-settings.md)
-   [同盟](federation.md)
-   [安全性內容](security-context.md)
-   [端點識別](endpoint-identity.md)
-   [安全性處理結果](security-processing-results.md)

## <a name="security"></a>安全性

使用 WWSAPI 安全性 API 時，應用程式會面臨許多安全性風險：

<dl> <dt>

<span id="Accidental_misconfiguration"></span><span id="accidental_misconfiguration"></span><span id="ACCIDENTAL_MISCONFIGURATION"></span>意外設定錯誤
</dt> <dd>

WWSAPI 支援一系列安全性相關的設定選項。 請參閱，例如 [**WS 安全性系結 \_ \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)。 其中一些選項（例如 **WS 安全性系 \_ 結 \_ \_ 屬性 \_ 允許 \_ 匿名 \_ 用戶端** ）允許應用程式降低各種安全性系結所提供的預設安全性層級。 您應該仔細評估使用這類選項，以確保沒有任何產生的攻擊媒介。

此外，如先前所述，WWSAPI 可讓應用程式刻意停用完整保護訊息結算所需的特定步驟，例如即使傳輸安全性認證，也允許停用加密。 這允許啟用某些特定案例，而且不應該用於一般通訊。 [**Ws-management \_ \_ 等級**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)必須明確地減少以啟用此案例，而且應用程式不應該變更該值，除非絕對必要，因為這樣做會停用許多設計來確保安全設定的檢查。

</dd> <dt>

<span id="Storing_confidential_information_in_memory"></span><span id="storing_confidential_information_in_memory"></span><span id="STORING_CONFIDENTIAL_INFORMATION_IN_MEMORY"></span>將機密資訊儲存在記憶體中
</dt> <dd>

儲存在記憶體中的機密資訊（例如密碼）很容易由具有特殊許可權的攻擊者（例如分頁檔）解壓縮。 WWSAPI 會複製所提供的認證，並將該複本加密，讓原始資料保持未受保護。 應用程式必須負責保護原始實例。 此外，加密的複本會在使用時短暫解密，開啟視窗將其解壓縮。

</dd> <dt>

<span id="Denial_of_service"></span><span id="denial_of_service"></span><span id="DENIAL_OF_SERVICE"></span>拒絕服務
</dt> <dd>

安全性處理可能會耗用大量資源。 每個額外的安全性系結都會增加這些成本。 WWSAPI 會在發生安全性驗證失敗時立即中止安全性處理，但是在執行重要工作之前，可能不會進行某些檢查（例如授權決策）。

當訊息在伺服器上處理時，安全性狀態會儲存在訊息堆積上。 應用程式可以藉由透過 WS \_ MESSAGE \_ PROPERTY \_ 堆積屬性減少該堆積的大小，來限制安全性處理期間的記憶體耗用量 \_ 。 此外，某些安全性系結（例如 WS \_ security \_ CONTEXT \_ MESSAGE \_ security \_ BINDING）可能會導致伺服器代表用戶端配置資源。 您可以透過下列 [**WS 安全性系結 \_ \_ \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) 值來設定這些資源的限制：

-   WS \_ 安全性系結 \_ \_ 屬性 \_ 安全性 \_ 內容 \_ 最大 \_ 暫止內容 \_
-   WS \_ 安全性系結 \_ \_ 屬性 \_ 安全性 \_ 內容 \_ 最大 \_ \_ 作用中內容
-   WS \_ 安全性系結 \_ \_ 屬性 \_ 安全性 \_ 內容 \_ 更新 \_ 間隔
-   WS \_ 安全性系結 \_ \_ 屬性 \_ 安全性 \_ 內容 \_ 變換 \_ 間隔

將這些限制設定為低值，可減少記憶體耗用量上限，但會導致在達到配額時拒絕合法的用戶端。

</dd> </dl>

 

 