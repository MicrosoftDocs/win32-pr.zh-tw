---
title: 同盟
description: 同盟允許將授權授權單位委派給其他 interprise 成員。
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- 適用于 Windows 的同盟 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a02744c9c0a5358da35f4c31c20633c420fee9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104551319"
---
# <a name="federation"></a>同盟

同盟允許將授權授權單位委派給其他 interprise 成員。 例如，請考慮下列商務問題： Contoso 公司的自動零件製造業希望允許其客戶 Fabrikam Inc. 的授權員工安全地存取 Contoso 的部分訂單 Web 服務。 此案例的其中一個安全性解決方案，是讓 Contoso 以 Fabrikam 設定信任機制，將存取授權決策委派給 Fabrikam。 此程式的運作方式如下：

-   Fabrikam 在成為 Contoso 的夥伴時，會設定 Contoso 的信任合約。 此步驟的目標是同意安全性權杖類型，以及將代表 Fabrikam 授權的內容，並可接受 Contoso。 例如，可能會決定主體名稱為 "CN = Fabrikam Inc. 供應商 STS" 的受信任 x.509 憑證應簽署 SAML 權杖，讓 Contoso Web 服務能夠接受該 SAML 權杖。 此外，可能會決定發出的 SAML 權杖中的安全性宣告應該是「 https://schemas.contoso.com/claims/lookup (部分查閱授權) 或 '」 https://schemas.contoso.com/claims/order (以進行部分訂購授權) 。
-   當 Fabrikam 員工使用內部部分訂購應用程式時，它會先將安全性權杖服務與 Fabrikam 內的 (STS) 聯繫。 該員工會使用內部 Fabrikam 安全性機制進行驗證 (比方說，Windows 網域使用者名稱/密碼) ，他對訂購部分的授權會經過驗證，而且會發出簡短的 SAML 權杖，其中包含適當的宣告，並由上面決定的 x.509 憑證簽署。 元件訂購應用程式接著會向 Contoso 服務顯示發行的 SAML 權杖，以驗證並執行訂購工作。

在這裡，Fabrikam STS 會以「發行方」的形式運作，而 Contoso 元件服務會作為「信賴憑證者」。 ![此圖顯示同盟中的發行方和信賴憑證者。](images/stsmodel.png)

## <a name="federation-features"></a>同盟功能

以下是針對同盟案例中涉及之合作物件或角色所支援的安全性功能：

-   用戶端：若要從 STS 取得安全性權杖，您可以使用 [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) 函數。 或者，您可以使用用戶端安全性權杖提供者程式庫（例如 CardSpace 或 LiveID），然後使用其輸出在本機建立使用 [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)的安全性權杖。 無論哪一種方式，一旦用戶端具有安全性權杖，就可以建立通道給服務，指定 [**ws \_ XML \_ 權杖 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) 系結來呈現權杖，以及使用傳輸安全性系結（例如 [**WS \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) 系結）來保護通道。
-   伺服器端：在具有發行 SAML 權杖之安全性權杖服務的同盟案例中，伺服器可能會使用 [**ws \_ SAML \_ MESSAGE \_ security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)系結，以及傳輸安全性系結（例如 [**WS \_ SSL \_ 傳輸 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) 系結）來保護通道。
-   STS 端：請注意，STS 是 Web 服務應用程式，而且可以在接聽程式建立時使用 [**安全性描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構來指定要求安全性權杖的安全性需求，就像任何其他安全的 Web 服務一樣。 然後，它可以剖析傳入的要求訊息承載以驗證權杖要求，並將發出的權杖傳回為回復訊息承載。 目前未提供任何功能來協助這些剖析和發出步驟。

請注意，用戶端可以一般地以 XML 安全性權杖的形式來處理發出的安全性權杖，而不需要知道權杖類型，或執行權杖型別特定的處理。 但是，伺服器必須瞭解特定的安全性權杖類型，才能瞭解及處理它。 安全性權杖的要求和回應步驟會使用 WS-Trust 規格中定義的結構。

## <a name="more-complex-federation-scenarios"></a>更複雜的同盟案例

同盟案例可能涉及組成同盟鏈的多個 Sts。 請考慮下列範例：

-   用戶端會使用 LiveID 使用者名稱/密碼向 LiveID STS 進行驗證，並取得安全性權杖 T1。
-   用戶端會使用 T1 向 STS1 進行驗證，並取得安全性權杖 T2。
-   用戶端會使用 T2 向 STS2 進行驗證，並取得安全性權杖 T3。
-   用戶端會使用 T3 向目標服務進行驗證。

在這裡，LiveID STS、STS1、STS2 和 S 形成同盟鏈。 同盟鏈中的 Sts 可以針對整體應用程式案例執行各種角色。 這類 STS 功能角色的範例包括身分識別提供者、授權決策 maker、anonymizer 和 resource manager。

## <a name="sts-request-parameters-and-metadata-exchange"></a>STS 要求參數和中繼資料交換

若要讓用戶端順利進行 [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) 呼叫，必須知道該呼叫的參數 (例如，所需的權杖類型和宣告類型) 、sts 要求通道的 [**安全性描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 需求，以及 sts 的 [端點位址](endpoint-address.md) 。 用戶端應用程式可以使用下列任何一種技術來判斷這項資訊：

-   在設計階段決策的過程中，將應用程式中的資訊硬編碼。
-   從本機應用程式部署者所設定的應用層級設定檔中讀取此資訊。
-   使用 [中繼資料匯入](metadata-import.md) 功能搭配 [**WS \_ 發出的 \_ 權杖訊息安全性系結 \_ \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) 結構，在執行時間動態探索這項資訊。

若要說明如何搭配使用動態 MEX 與同盟，請考慮上述的3個 STS 範例。 用戶端會先使用動態 MEX 來取得 T3 的相關資訊 (亦即，STS2) 的要求，以及 STS2 動態 MEX 位址 (也就是尋找 STS2) 的位置。 然後，它會使用該資訊來執行動態 MEX 與 STS2，以探索 T2 和 STS1 的相關資訊等等。

因此，動態 MEX 步驟會依照順序4、3、2、1執行，以建立同盟鏈，並在訂單1、2、3、4中進行的權杖要求和展示步驟，以回溯同盟鏈。

> [!Note]  
> Windows 7 和 Windows Server 2008 R2： WWSAPI 只支援[輕量 Web 服務安全性設定檔 (LWSSP) ](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e)所定義的[ws-trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf)和[ws-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) 。 如需有關 Microsoft 執行的詳細資訊，請參閱 LWSSP 的 [訊息語法](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) 一節。

 

 

 