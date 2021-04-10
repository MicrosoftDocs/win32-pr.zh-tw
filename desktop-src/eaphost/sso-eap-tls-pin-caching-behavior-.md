---
title: SSO EAP-TLS PIN 快取行為
description: 提供逐步的方法來解決會話繼續的問題，以及在 SSO EAP-TLS 環境中對漫遊使用者的重新驗證。
ms.assetid: aeded6c9-315d-4115-9750-485f017dd8dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7c4e3058598f98327570fbcd0347cfb84e5825
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104092473"
---
# <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="b01e1-103">SSO EAP-TLS PIN 快取行為</span><span class="sxs-lookup"><span data-stu-id="b01e1-103">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="b01e1-104">本主題提供逐步解決方法，以解決在 SSO EAP-TLS 環境中對漫遊使用者的會話繼續操作和重新驗證的問題。</span><span class="sxs-lookup"><span data-stu-id="b01e1-104">This topic provides a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="b01e1-105">逐步方法</span><span class="sxs-lookup"><span data-stu-id="b01e1-105">Step-By-Step Approach</span></span>

<span data-ttu-id="b01e1-106">下列清單表示在 SSO EAP-TLS 環境中，解決會話繼續和重新驗證漫遊使用者之重要的逐步方法。</span><span class="sxs-lookup"><span data-stu-id="b01e1-106">The following list represents a step-by-step approach for resolving matters of session resumption and re-authentication of a roaming user in an SSO EAP-TLS environment.</span></span>

-   <span data-ttu-id="b01e1-107">在具有 EAP-TLS 的 SSO 環境中第一次成功驗證之後，要求者預設會保留所有使用者認證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b01e1-107">After the first successful authentication in an SSO environment with EAP-TLS, the supplicant retains all user credential related information by default.</span></span>
    > [!Note]  
    > <span data-ttu-id="b01e1-108">雖然受限於特定要求者的執行，但建議要求者保留要求者最後在 [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields)呼叫中用來 EAPHost 的整個 [**EAP 設定 \_ \_ 輸入 \_ 欄位陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構。</span><span class="sxs-lookup"><span data-stu-id="b01e1-108">Although subject to the particular supplicant implementation, it's advisable for the supplicant to retain the entire [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure that the supplicant last used in the [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) call to EAPHost.</span></span>

     

-   <span data-ttu-id="b01e1-109">當使用者第一次漫遊和重新驗證開始時，要求者會再次使用相同的 [**EAP 設定 \_ \_ 輸入 \_ 欄位陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構來呼叫 [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) ; 要求者也必須在第一次成功驗證之後，傳入保留的相同使用者 BLOB。</span><span class="sxs-lookup"><span data-stu-id="b01e1-109">As the user first roams and the re-authentication begins, the supplicant calls [**EapHostPeerQueryUserBlobFromCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields) again with the same [**EAP\_CONFIG\_INPUT\_FIELD ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure; the supplicant must also pass in the same user BLOB retained after the first successful authentication.</span></span>
-   <span data-ttu-id="b01e1-110">然後，EAPHost 會將使用者 BLOB 中的資訊傳遞給 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="b01e1-110">EAPHost then passes the information in the user BLOB to the EAP method.</span></span>
-   <span data-ttu-id="b01e1-111">EAP 方法接著會以認證欄位（例如，在 *pEapConfigInputFieldArray* 中提供的 PIN）來更新使用者 BLOB，並保留其餘的值（例如，伺服器憑證，例如在原始使用者 BLOB 中）。</span><span class="sxs-lookup"><span data-stu-id="b01e1-111">The EAP method in turn updates the user BLOB with credential fields - the PIN for example - provided in *pEapConfigInputFieldArray*, and keeps the remaining values - the server certificate for example - as it was in the original user BLOB.</span></span>
-   <span data-ttu-id="b01e1-112">完成這些步驟之後，要求者可以使用此使用者 BLOB 呼叫 [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 執行時間函式，以正常方式繼續驗證。</span><span class="sxs-lookup"><span data-stu-id="b01e1-112">After completing these steps, the supplicant can resume authentication in a normal way by calling the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) run-time function with this user BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b01e1-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b01e1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b01e1-114">SSO EAPHost 案例</span><span class="sxs-lookup"><span data-stu-id="b01e1-114">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="b01e1-115">SSO 和 PLAP</span><span class="sxs-lookup"><span data-stu-id="b01e1-115">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




