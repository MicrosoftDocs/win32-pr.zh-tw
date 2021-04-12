---
title: 通道方法 API 呼叫順序
description: 瞭解通道方法的 API 呼叫順序。 請參閱總覽並查看其他可用的資源。
ms.assetid: 48aad213-1d29-4809-9599-b56325b2b8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5f6b30fda111162585fb5c8b2aa370fa6af61e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316504"
---
# <a name="tunnel-method-api-call-sequence"></a>通道方法 API 呼叫順序

本主題涵蓋通道方法的 API 呼叫順序

## <a name="tunnel-method-call-sequence-overview"></a>通道方法呼叫順序總覽

當要求者取得使用者身分識別和使用者資料的要求時，通常會發生下列 API 呼叫流程。

-   要求者在 EapHost 上呼叫 EapHostPeerProcessReceivedPacket，以處理從驗證器收到的封包。
-   處理此封包時，EAPHost 會將它判斷為 IdentityRequest 封包，並在通道方法上呼叫 [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) ，以取得要用於驗證的使用者身分識別。
-   如果通道方法需要從內部方法取得使用者身分識別，它會在內部 EAPHost 上呼叫 [**EAPHostPeerGetIdentity**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetidentity) ，然後再呼叫內部方法上的 [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity) 。

## <a name="user-interaction-with-the-tunnel-methods-api-call-flow"></a>使用者與通道方法 API 呼叫流程的互動

在某些情況下，當身分識別無法使用，或當使用者必須提供其他資訊時，Eap 方法會在要求者上引發使用者介面對話方塊。

在這種情況下，通常會發生呼叫順序，以便直接從使用者取得資訊。

-   通道 Eap 方法會傳回動作程式碼，以叫用 UI 來 EapHost。 要求者呼叫 [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)來取得使用者介面對話方塊的目前使用者介面內容資訊。
-   然後要求者呼叫 [ **EapHostPeerInvokeInteractiveUI。**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) 此函式會使用 UI 內容資訊來引發互動式使用者介面，此介面是用來從使用者取得認證資訊。 UI 進程會載入 Eappcfg.dll，並取得 EapPeerInvokeInteractiveUI 和 EapPeerFreeMemory 的指標。
    > [!Note]  
    > UI 程式通常會收集 UI 或處理互動式 UI，並與要求者進程分開。 分隔這兩個程式並不是 EAPHost 的需求，但這麼做的優點是可以讓 UI 進程與桌面互動。

     

-   EapHost 會呼叫通道方法上的 [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) 來取得使用者身分識別資訊。
-   為了從內部方法取得使用者身分識別，通道方法會在內部 EAPHost 上呼叫 [**EapHostPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui) 。
-   內部 EAPHost 會呼叫內部方法上的 [**EapPeerInvokeIdentityUI**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinvokeidentityui) 來叫用使用者身分識別 UI。
-   [**EapHostPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) 會在引發 ui 之後，提供新的或更新的 ui 內容資訊給 EAPHost 上載入的 EAP 對等方法。

下圖說明通道方法的 API 呼叫順序

![通道方法 api 呼叫順序](images/tunnel-identity-processing-new.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 呼叫順序](about-eaphost-call-sequences.md)
</dt> <dt>

[要求者 API 呼叫順序](supplicant-api-call-sequence.md)
</dt> <dt>

[EAPHost 要求者 API 參考](eap-host-supplicant-api-reference.md)
</dt> </dl>

 

 




