---
title: SSO 密碼變更行為
description: 提供解決 SSO 密碼變更行為的逐步方法。
ms.assetid: c52ffeb8-ecee-4398-a7df-388b523c737c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005fe5191b3bdccf2bb1643be50817a3b0405336
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106967463"
---
# <a name="sso-password-change-behavior"></a>SSO 密碼變更行為

本主題提供解決 SSO 密碼變更行為的逐步方法。

## <a name="step-by-step-approach"></a>逐步方法

下列清單代表解決 SSO 密碼變更行為的逐步方法。

-   當 EAP 方法收到有關密碼變更的通知時，方法會通知 EAPHost;EAPHost 接著會傳回動作碼 [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)來通知要求者。
-   從 EAPHost 收到 [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) 動作碼之後，要求者藉由呼叫 [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) 函式，從 EAP 方法取得 UI 內容;EAPHost 接著藉由呼叫對應的方法函式，從 EAP 方法取得 UI 內容
-   要求者將 UI 內容傳遞給 UI 進程 (使用某種形式的處理序間通訊) 。
-   UI 進程會在 EAPHost 上呼叫 [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 。
-   EAPHost 會藉由呼叫 EAP 方法上的 [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) 來收集 UI 內容。
-   EAP 方法會在 [**eap \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) 結構中提供任何必要的 UI 內容資訊，其中 *dwDataType* 會設定為 *EapCredExpiryReq* ，而 *pbUiData* 則會指向類型為 [**EAP 認證 \_ \_ 需求**](eap-cred-req.md)的結構。
-   在填入 [**eap \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構時，此 EAP 方法只會填入 *curCreds* 參數，而不會在 eap 設定 **\_ \_ 輸入 \_ 欄位 \_ 資料** 結構中設定 [**eap \_ UI \_ 輸入 \_ 欄位 \_ .props \_ 唯讀 \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)旗標。
    > [!Note]  
    > [**EAP \_ UI \_ 輸入 \_ 欄位 \_ .props \_ 唯讀 \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)旗標適用于需要變更的成員欄位 (s) 。

     

-   在收集 UI 內容資訊之後，UI 程式會呈現 UI 來收集使用者的變更密碼資訊。 這項資訊會填入 [**EAP 認證 \_ \_ 到期 \_ 需求**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)結構的 *NewCreds* 參數中。
-   UI 進程會透過 [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)將 [**EAP 認證 \_ \_ RESP**](eap-cred-resp.md)結構傳回 EAPHost。
-   UI 進程會將此使用者 BLOB 傳遞給要求者，而要求者會照常繼續 EAPHost 執行時間函式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SSO EAPHost 案例](why-eaphost-sso.md)
</dt> <dt>

[SSO 和 PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




