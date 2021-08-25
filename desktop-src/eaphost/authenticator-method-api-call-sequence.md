---
title: Authenticator方法 API 呼叫順序
description: 瞭解驗證器方法 API 呼叫順序。 請參閱清單，以示範 EAPHost 在 EAP 驗證器方法上所做的呼叫順序。
ms.assetid: 4756300c-5e49-44e8-ab49-1993d780d2a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3864d7b08c3c5c154ef3be86d0ac14716cd8b46adb1485fc5c55e598f870a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852288"
---
# <a name="authenticator-method-api-call-sequence"></a>Authenticator方法 API 呼叫順序

本主題提供驗證器方法 API 的特定呼叫順序。 在一般 EAP 驗證會話 EAPHost 期間，會在執行 EAPHost 驗證器方法 Api 的 EAP 方法上進行一些呼叫。

下列清單示範 EAPHost 在 EAP 驗證器方法上所做的呼叫順序。

-   EAP 驗證器會先將用於網路原則伺服器上特定驗證的 EAP 方法 DLL 載入 (NPS) 或其他驗證服務器。
-   使用已填入的 [**EAP \_ 型**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)別結構來呼叫方法上的 [**EapAuthenticatorGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) ，以取得在 DLL 上執行的函式指標清單。 驗證器方法 (server) 的後續函式呼叫會假設在 DLL 上執行。
-   呼叫 [**EapAuthenticatorInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) ，以指示 EAP 方法程式庫使用此驗證器方法為至少一個驗證會話做好準備。
-   呼叫 [**EapMethodAuthenticatorBeginSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorbeginsession) 來建立唯一的驗證會話。
-   重複執行下列步驟，直到 [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) 指出有可用的驗證結果。
    -   使用要傳遞給要求者的要求封包指標來呼叫 [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket) 。
    -   呼叫 [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket) 以取得要求者所傳送的回應封包。 此函式會傳回 **eap \_ 方法驗證器 \_ \_ 回應 \_ 動作** 碼，指出驗證器必須在 EAP 驗證會話中採取的下一個動作。
    -   如果動作程式碼為 [EAP \_ 方法 \_ 驗證 \_ 器 \_ 回應](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)回應，則表示 EAP 方法具有可供驗證器取得並傳遞給對等方法的屬性。 Authenticator 會呼叫 [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) ，以從 eap 驗證器方法取得各種 eap 驗證屬性。 在驗證器處理屬性之後，它會呼叫 [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) ，以提供在 eap 驗證器方法上設定的更新 eap 驗證屬性。 此函式會傳回 **EAP \_ 方法驗證器 \_ \_ 回應 \_ 動作** 碼，以決定後續的動作。
-   如果動作程式碼為 [EAP \_ 方法 \_ 驗證器 \_ 回應 \_ 結果](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)，則表示驗證器已判斷驗證會話的結果，而且這些結果可供 EAPHost。 Authenticator 會呼叫 [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) ，並取得驗證會話的結果。
-   接下來是呼叫 [**EapMethodAuthenticatorEndSession**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorendsession) 來結束驗證會話。
-   最後，會對 [**EapMethodAuthenticatorShutdown**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorshutdown) 進行呼叫，以卸載驗證器方法 DLL。
-   卸載 EAP 方法程式庫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**EAP \_ 方法 \_ 驗證器 \_ 回應 \_ 動作**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)
</dt> <dt>

[要求者 API 呼叫順序](supplicant-api-call-sequence.md)
</dt> <dt>

[對等方法 API 呼叫順序](peer-method-api-call-sequence.md)
</dt> <dt>

[EAPHost 呼叫順序](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




