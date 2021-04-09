---
title: 要求者 API 呼叫順序
description: 瞭解要求者 API 呼叫順序。 查看通話順序的總覽，並查看其他可用的資源。
ms.assetid: 83276783-aee5-43ac-982d-1144df982a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c93afea6dbf4c3220bbeaec4f6278eb3d0b756
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933629"
---
# <a name="supplicant-api-call-sequence"></a>要求者 API 呼叫順序

本主題提供要求者 API 的特定呼叫順序。

## <a name="supplicant-api-call-sequence-overview"></a>要求者 API 呼叫順序總覽

當要求者從提供者（例如存取點）接收 EAP 封包時，通常會發生下列要求者 API 呼叫流程。

-   應用程式會使用 EAPHost 設定資料和使用者資料來呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 。 成功的呼叫會傳回 **EAP \_ 會話 \_ 句** 柄會話控制碼。
-   要求者接收的每個封包都會透過呼叫 [**EapHostPeerProcessReceivedPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket)來處理。 然後，要求者會呼叫對應至函式所傳回之動作程式碼的函式。
-   如果動作碼是 **EapHostPeerResponseSend**，要求者會呼叫 [**EapHostPeerGetSendPacket**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetsendpacket) 來取得要傳送給驗證器的回應。
-   如果在會話期間，傳回給要求者的動作程式碼是 **EapHostPeerResponseRespond**，則表示 EAP 屬性可供使用。 要求者接著會呼叫 [**EapHostPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresponseattributes) 來取得它們。 這些屬性包含在驗證過程中所使用的補充資料。 在要求者完成處理屬性之後，它會呼叫 [**EapHostPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetresponseattributes) 來更新資料。 此函式會傳回動作碼，以決定要求者的下一個動作。
-   如果動作程式碼 **EapHostPeerResponseInvokeUI** ，要求者會引發使用者介面對話方塊來取得使用者的互動式資料，例如認證或身分識別資訊。 請參閱下面的要求者 API 呼叫流程使用者互動。
-   如果動作碼是 **EapHostPeerResponseResult**，則表示驗證會話的結果可供要求者使用。 要求者接著會呼叫 [**EapHostPeerGetResult**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetresult) 來取得結果。 無論結果是表示成功還是失敗，要求者都會呼叫 [**EapHostPeerEndSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession)。 在失敗的情況下，您可以使用 EAPHost 開啟另一個會話並提供新的身分識別，或再次嘗試使用原始身分識別進行驗證，來嘗試重新驗證。

## <a name="user-interaction-with-the-supplicant-api-call-flow"></a>使用者與要求者 API 呼叫流程的互動

在某些情況下，要求者需要取得使用者的資訊，才能繼續進行驗證程式。

下列清單示範啟用互動式輸入所需的要求者和 EAPHost UI 進程的呼叫順序。

1.  要求者藉由呼叫 [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext)來取得目前的使用者介面內容。
2.  要求者接著將 UI 內容資料傳送給要求者 UI 進程。
    > [!Note]  
    > UI 進程通常會收集 UI 或處理互動式 UI，與要求者進程不同。 分隔這兩個程式並不是 EAPHost 的需求，但這麼做的優點是可以讓 UI 進程與桌面互動。

     

3.  如果要求者想要自行轉譯 UI，則會呼叫 [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 函式來取得要引發之互動式 UI 元件的輸入欄位。 否則，它會遵循傳統的叫用方法互動式 UI 的模型，方法是呼叫 [ **EapHostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)
    > [!Note]  
    > 如果傳回的是 [**\_ \_ \_ \_ \_ 不 \_ 支援的 EAP E EAPHOST 方法**](eap-related-error-and-information-constants.md) 作業，要求者必須藉由呼叫 [**EAPHOSTPEERINVOKEINTERACTIVEUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui)來遵循傳統的叫用方法互動式 UI 模型。 如果發生錯誤， [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 會傳回 **Null** 以外的傳回碼。

     

4.  當要求者呼叫 [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 或 [**EaphostPeerInvokeInteractiveUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) UI 進程時，會傳遞現有的內容資料並載入 Eappcfg.dll。 引發適當的 UI 來收集新的資料。 新的 UI 內容資料（現在可能包含使用者輸入）會進行複製，而舊的內容資料會透過呼叫 [**EapPeerFreeMemory**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory)來釋放。
5.  UI 進程會將新的內容資料傳回給要求者，以呼叫 [**EapHostPeerSetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext) 來設定它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[對等方法 API 呼叫順序](peer-method-api-call-sequence.md)
</dt> <dt>

[驗證者方法 API 呼叫順序](authenticator-method-api-call-sequence.md)
</dt> <dt>

[EAPHost 呼叫順序](about-eaphost-call-sequences.md)
</dt> <dt>

[EAPHost 要求者](eaphost-supplicants.md)
</dt> </dl>

 

 




