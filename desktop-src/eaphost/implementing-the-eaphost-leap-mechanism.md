---
title: 執行 EAPHost 的 LEAP 機制
description: 描述 EAPHost 機制，可讓協力廠商撰寫適用于 Windows 的輕量可延伸驗證通訊協定 (LEAP) 模組。
ms.assetid: d17a99cb-4a43-4719-984e-b742c9518f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc50cda8d32cc26dd81af5733345deebb579c792
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093467"
---
# <a name="implementing-the-eaphost-leap-mechanism"></a>執行 EAPHost 的 LEAP 機制

本主題說明的 EAPHost 機制可讓協力廠商撰寫適用于 Windows 的輕量) 模組 (的輕量可延伸驗證通訊協定。 LEAP 是根據 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84016)而由 Cisco 建立的傳統驗證方法。 如需有關 LEAP 的詳細資訊，請參閱 [CISCO 閏 Q&A](https://go.microsoft.com/fwlink/p/?linkid=84018)。

## <a name="eaphost-authentication-process"></a>EAPHost Authentication 進程

一般 EAPHost 驗證程式會如下所示：

-   驗證器傳送要求以驗證對等。 例如，應用程式會使用 EAPHost 設定和使用者資料來呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 。
-   對等會在回復中傳送回應封包至有效的要求。 例如，成功的呼叫會傳回 **EAP \_ 會話 \_ 句** 柄會話控制碼。
-   驗證器會傳送額外的要求封包，且對等會以回應來回複。 例如，應用程式會呼叫 [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) ，以取得 EAPHost 在整個會話中收到的 EAP 封包。 每個封包都會透過呼叫 [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket)來處理。
-   [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket) 一律會傳回動作碼。 然後要求者必須呼叫對應至動作程式碼的函式。
-   要求和回應的順序會持續一段時間。 例如，應用程式可以呼叫 [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) 來要求可用的 EAP 屬性，而對等會以 [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) 回應以傳回它們。
-   在初始要求之後，就無法傳送新的要求，直到收到有效的回應為止。
-   交談會繼續進行，直到驗證器無法驗證對等，在此情況下，驗證器的執行必須傳送 EAP 失敗。 例如，一或多個要求的無法接受回應會導致驗證器傳輸程式碼 4 EAP 失敗。
-   或者，驗證交談可以繼續進行，直到驗證器判斷已成功驗證，在此情況下，驗證器必須將 EAP 成功 (程式碼 3) 。
-   無論結果是指出成功或失敗，應用程式都會呼叫 [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) 來終止會話。 在失敗的情況下，您可以使用 EAPHost 開啟另一個會話，並提供相同或新的身分識別，來嘗試重新驗證。

### <a name="leap-authentication-process"></a>LEAP 驗證流程

LEAP 驗證程式與一般 EAPhost authentication 程式不同，如下所示：

-   EAP 驗證是由伺服器 (驗證器) 所起始。 相反地，相反地，用戶端 (對等) 起始。
    -   因此，在寫入 LEAP 模組時，您必須一律確定來自對等方法的挑戰要求封包，以及來自 EAP 伺服器的 EAP 回應，一律必須有與來自伺服器之 EAP 成功封包的相同封包識別碼。

    <!-- -->

    -   相反地，EAPHost 要求和回應和成功封包通常都有不同的識別碼。
        > [!Note]  
        > 每個 EAP 要求都有一個類型欄位，以指出所要求的內容。 和要求封包一樣，每個 EAP 回應封包都包含類型欄位，該欄位會對應至要求的類型欄位。 範例包括身分識別要求和挑戰要求封包。

         

-   在 EAPHost 失敗的情況下，您可以使用 EAPHost 開啟另一個會話，並提供相同的身分識別或新的身分識別，來嘗試重新驗證。

### <a name="leap-authenticator-method-implementation"></a>LEAP 驗證器方法的執行

開發 LEAP 驗證器方法時，請確定下列事項：

-   在驗證的第一階段之後，LEAP 驗證器方法必須傳回 [**EAP \_ 方法 \_ 驗證器 \_ 回應 \_ 傳送**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) 動作碼 (對等驗證) 成功。 然後當呼叫 [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket)時，它應該會傳回具有 EAP 代碼 [**EapCodeSuccess**](/windows/win32/api/eapmethodtypes/ne-eapmethodtypes-eapcode)的有效 [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket) 。
-   如果對等驗證的第一個階段失敗，則 LEAP 驗證器方法應該會傳回 [**EAP \_ 方法 \_ 驗證器 \_ 回應 \_ 結果**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action) 動作程式碼。
-   當呼叫 [**EapMethodAuthenticatorSendPacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsendpacket)時，LEAP 驗證器方法必須傳回最後一個驗證回應封包，以及 [**EAP \_ 方法 \_ 驗證程式 \_ 回應 \_ 結果**](/windows/desktop/api/EapAuthenticatorActionDefine/ne-eapauthenticatoractiondefine-eap_method_authenticator_response_action)的動作代碼。 然後，在後續呼叫 [**EapMethodAuthenticatorGetResult**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetresult) 時，必須傳回 **EAP \_ 會話 \_ 控制碼** ，以識別已驗證的會話。
-   

### <a name="leap-peer-method-implementation"></a>LEAP 對等方法的執行

開發 LEAP 對等方法時，請確定下列各項

-   在驗證的第一個階段 (對等驗證) 成功之後，LEAP 對等方法應該會傳回 [**EapPeerMethodResponseActionSend**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 動作程式碼。
-   在驗證的第二個階段成功之後，LEAP 對等方法應該會傳回 [**EapPeerMethodResponseActionResult**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 動作程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 呼叫順序](about-eaphost-call-sequences.md)
</dt> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> </dl>

 

 




