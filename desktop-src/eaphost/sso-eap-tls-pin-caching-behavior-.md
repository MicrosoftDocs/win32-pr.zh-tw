---
title: SSO EAP-TLS PIN 快取行為
description: 提供逐步的方法來解決會話繼續的問題，以及在 SSO EAP-TLS 環境中對漫遊使用者的重新驗證。
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bc8cb112a6def55085cbd0b94068407320e4116a4b0161d7d923319257258f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085882"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a>SSO EAP-TLS PIN 快取行為

本主題提供逐步解決方法，以解決在 SSO EAP-TLS 環境中對漫遊使用者的會話繼續操作和重新驗證的問題。

## <a name="step-by-step-approach"></a>逐步方法

下列清單表示在 SSO EAP-TLS 環境中，解決會話繼續和重新驗證漫遊使用者之重要的逐步方法。

-   在具有 EAP-TLS 的 SSO 環境中第一次成功驗證之後，要求者預設會保留所有使用者認證的相關資訊。
    > [!Note]  
    > 雖然受限於特定要求者的執行，但建議要求者保留要求者最後在 [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)呼叫中用來 EAPHost 的整個 [**EAP 設定 \_ \_ 輸入 \_ 欄位陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構。

     

-   當使用者第一次漫遊和重新驗證開始時，要求者會再次使用相同的 [**EAP 設定 \_ \_ 輸入 \_ 欄位陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構來呼叫 [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) ; 要求者也必須在第一次成功驗證之後，傳入保留的相同使用者 BLOB。
-   然後，EAPHost 會將使用者 BLOB 中的資訊傳遞給 EAP 方法。
-   EAP 方法接著會以認證欄位（例如，在 *pEapConfigInputFieldArray* 中提供的 PIN）來更新使用者 BLOB，並保留其餘的值（例如，伺服器憑證，例如在原始使用者 BLOB 中）。
-   完成這些步驟之後，要求者可以使用此使用者 BLOB 呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 執行時間函式，以正常方式繼續驗證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SSO EAPHost 案例](why-eaphost-sso.md)
</dt> <dt>

[SSO 和 PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




