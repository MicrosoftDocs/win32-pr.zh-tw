---
title: 對等方法 API 呼叫順序
description: 深入瞭解對等方法 API 呼叫順序。 請參閱清單，以示範 EAPHost 在 EAP 對等方法上所做的呼叫順序。
ms.assetid: aac69e89-249d-4bc8-baef-1f0681f9f7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647a6a558d282ff4ae3691c23600b696b79764ee68a1007ccabb445c5a1fe65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042786"
---
# <a name="peer-method-api-call-sequence"></a>對等方法 API 呼叫順序

本主題提供對等方法 API 的特定呼叫順序。 在一般 EAP 驗證會話 EAPHost 期間，會在 EAP 方法上進行一些呼叫，以執行 EAPHost 對等方法 API。

下列清單示範 EAPHost 在 EAP 對等方法上所做的呼叫順序。

-   載入用於驗證的 EAP 對等方法 DLL。
-   呼叫方法上的 [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo) ，以取得在 DLL 上所執行之函式的指標清單。 EAPHost 對等 (用戶端) 的後續函式呼叫會假設在 DLL 上執行。
-   呼叫 [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize) ，以指示 EAP 方法程式庫使用此對等方法來準備至少一個驗證會話。
-   呼叫 [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) 來建立唯一的驗證會話。
-   呼叫 [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) 以取得要用於驗證的身分識別。 如果無法使用身分識別，或是使用者必須提供其他資訊，EAPHost 會呼叫 [ **EapPeerGetUICoNtext。**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext) 此函式會取得使用者介面對話方塊的內容資訊，此對話方塊會在要求者上引發。 在使用者提交身分識別資訊之後，使用者身分識別會透過呼叫 [**EapPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)來設定，並透過呼叫 **EapPeerGetIdentity** 取得。
-   重複執行下列步驟，直到 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) 指出有可用的驗證結果。
    -   使用要傳遞給要求者的要求封包指標來呼叫 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket) 。
    -   呼叫 **EapPeerGetResponsePacket** 以取得要傳送給驗證器的回應封包。
    -   （選擇性）如果在驗證會話期間需要抓取或傳送 EAP 屬性，EAPHost 會分別呼叫 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 和 [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) 。
-   當驗證器傳送指出驗證已完成的動作程式碼時，EAPHost 會呼叫 [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult) 並取得驗證的結果。
-   呼叫 [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) 以結束驗證會話。
-   呼叫 [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown) 以卸載對等方法 DLL。
-   卸載 EAP 方法程式庫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[要求者 API 呼叫順序](supplicant-api-call-sequence.md)
</dt> <dt>

[Authenticator方法 API 呼叫順序](authenticator-method-api-call-sequence.md)
</dt> <dt>

[EAPHost 呼叫順序](about-eaphost-call-sequences.md)
</dt> </dl>

 

 




