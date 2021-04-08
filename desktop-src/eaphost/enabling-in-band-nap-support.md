---
title: 為 EAP 方法執行 In-Band NAP 支援
description: 可以針對支援將類型長度值物件傳輸 (TLVs) 的 EAPHost EAP 方法啟用。
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684186"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a>為 EAP 方法執行 In-Band NAP 支援

[網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) 對於 eap 方法的支援，可以啟用 EAPHost eap 方法，以支援 (TLVs) 的型別長度值物件傳輸。 啟用頻內 NAP 支援時，會在 EAP 方法封包內傳輸 NAP 封包。

相反地，當啟用頻外 NAP 支援時，健康情況的 NAP [聲明](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange 會透過 EAP 方法封包內部以外的方式進行。

所有 TLVs 都是廠商專屬的。

## <a name="implementing-nap-support-on-eap-peer-methods"></a>在 EAP 對等方法上執行 NAP 支援

EAP 對等方法會收到包含 [健康狀態聲明](https://go.microsoft.com/fwlink/p/?linkid=83917) 的 TLV (SoH) 從 EAP 伺服器要求 TLV。

EAP 對等方法的執行接著會將包含 SoH 要求 TLV 的 TLV 傳遞給 EAPHost，如下所示。

-   EAP 對等方法執行會在從 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)傳回時，將動作程式碼 [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction)傳回 EAPHost。
-   從 EAP 對等方法執行 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 的 EAPHost 呼叫。 這些屬性會在進程中傳遞。
-   EAP 對等方法執行會傳回包含 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)中 SOH 要求 TLV 的 TLV。 這些屬性會在進程中收到。

EAP 對等方法執行會從 EAPHost 接收包含 SoH TLV 的 TLV，如下所示。

-   從 EAP 對等方法執行 [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) 的 EAPHost 呼叫。 **EapPeerSetResponseAttributes** 包含承載 SoH TLV 的 tlv。
-   EAP 對等方法執行會將 SoH TLV 傳送至 EAP 伺服器。
-   EAP 對等方法的執行會接收包含來自 EAP 伺服器之 SoH 回應 TLV 的 TLV。

EAP 對等方法執行會將包含 SoH 回應 TLV 的 TLV 傳遞給 EAPHost，如下所示。

-   EAP 對等方法執行會在從 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)傳回時，將動作程式碼 **EapPeerMethodResponseActionRespond** 傳回 EAPHost。
-   從 EAP 對等方法的 EAPHost 呼叫 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 。 [**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)結構會在進程中傳遞。
-   EAP 對等方法執行會傳回包含 [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)中 SOH 回應 TLV 的 TLV。

> [!Note]  
> [**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)結構的 **eapType** 成員一律會設定為 **eatEAPTLV** ，而 **pValue** 成員將指向包含 SoH 回應 tlv 的 TLV 的第一個位元組。

 

### <a name="implementing-nap-support-on-eap-server-methods"></a>在 EAP 伺服器方法上執行 NAP 支援

EAP 伺服器方法執行會建立包含 SoH 要求 TLV 的 TLV。 EAP 伺服器方法執行會將包含 SoH 要求 TLV 的此 TLV 傳送給 EAP 對等。 EAP 伺服器方法執行會接收來自 EAP 對等的 TLV。

EAP 伺服器方法執行會將包含 SoH TLV 的 TLV 傳遞給 EAPHost，如下所示。

-   EAP 伺服器方法執行會傳回動作程式碼， **eap \_ 方法驗證器 \_ 回應 \_ \_** 會在從 [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)傳回時回應 EAPHost。
-   從 EAP 伺服器方法執行 [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) 的 EAPHost 呼叫。
-   EAP 伺服器方法執行會傳回包含 [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)中 SoH TLV 的 TLV。

EAP 伺服器方法執行會從 EAPHost 接收包含 SoH 回應 TLV 的 TLV，如下所示。

-   從 EAP 伺服器方法執行 [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) 的 EAPHost 呼叫。
-   包含 SoH 回應 TLV 的 TLV 會在 EapMethodAuthenticatorSetAttributes 中傳回。 [ ](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)
-   EAP 伺服器方法執行會傳送包含 SoH 回應 TLV 的 TLV。

> [!Note]  
> [**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)結構的 **eapType** 成員一律會設定為 **eatEAPTLV** ，而 **pValue** 成員將指向包含 SoH 回應 tlv 的 TLV 的第一個位元組。

 

### <a name="messages"></a>訊息

EAP SoH TLV 用來封裝 SoH 通訊協定，以便透過 EAP 方法進行傳輸。 所有 EAP SoH TLVs 都有相同的結構，但不同于訊息的訊息識別碼和資料部分。

如需詳細資訊，請參閱「 [網路存取保護」 (NAP) 健康狀態聲明 (SoH) 訊息](https://go.microsoft.com/fwlink/p/?linkid=83918)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 EAP 方法消費者介面](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[啟用群組原則](enabling-group-policy.md)
</dt> <dt>

[為 EAP 方法執行 NAP 支援](implementing-nap-for-eap-methods.md)
</dt> <dt>

[在要求者和 EAP 方法之間傳送資料](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[EAPHost 要求者](eaphost-supplicants.md)
</dt> </dl>

 

 