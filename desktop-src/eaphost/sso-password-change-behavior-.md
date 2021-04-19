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
# <a name="sso-password-change-behavior"></a><span data-ttu-id="1e3b2-103">SSO 密碼變更行為</span><span class="sxs-lookup"><span data-stu-id="1e3b2-103">SSO Password Change Behavior</span></span>

<span data-ttu-id="1e3b2-104">本主題提供解決 SSO 密碼變更行為的逐步方法。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-104">This topic provides a step-by-step approach for resolving SSO password change behavior.</span></span>

## <a name="step-by-step-approach"></a><span data-ttu-id="1e3b2-105">逐步方法</span><span class="sxs-lookup"><span data-stu-id="1e3b2-105">Step-By-Step Approach</span></span>

<span data-ttu-id="1e3b2-106">下列清單代表解決 SSO 密碼變更行為的逐步方法。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-106">The following list represents a step-by-step approach for resolving SSO password change behavior.</span></span>

-   <span data-ttu-id="1e3b2-107">當 EAP 方法收到有關密碼變更的通知時，方法會通知 EAPHost;EAPHost 接著會傳回動作碼 [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)來通知要求者。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-107">Once the EAP method is notified about a password change, the method notifies EAPHost; EAPHost in turn notifies the supplicant by returning the action code, [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).</span></span>
-   <span data-ttu-id="1e3b2-108">從 EAPHost 收到 [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) 動作碼之後，要求者藉由呼叫 [**EapHostPeerGetUICoNtext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) 函式，從 EAP 方法取得 UI 內容;EAPHost 接著藉由呼叫對應的方法函式，從 EAP 方法取得 UI 內容</span><span class="sxs-lookup"><span data-stu-id="1e3b2-108">After receiving the [EapHostPeerResponseInvokeUI](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction) action code from EAPHost, the supplicant obtains the UI context from the EAP method by calling the [**EapHostPeerGetUIContext**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext) function; EAPHost then obtains the UI context from the EAP method by calling the corresponding method function</span></span>
-   <span data-ttu-id="1e3b2-109">要求者將 UI 內容傳遞給 UI 進程 (使用某種形式的處理序間通訊) 。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-109">The supplicant passes the UI context to the UI process (using some form of inter-process communication).</span></span>
-   <span data-ttu-id="1e3b2-110">UI 進程會在 EAPHost 上呼叫 [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) 。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-110">The UI process calls [**EapHostPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields) on EAPHost.</span></span>
-   <span data-ttu-id="1e3b2-111">EAPHost 會藉由呼叫 EAP 方法上的 [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) 來收集 UI 內容。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-111">EAPHost collects the UI context by calling [**EapPeerQueryInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerqueryinteractiveuiinputfields) on the EAP method.</span></span>
-   <span data-ttu-id="1e3b2-112">EAP 方法會在 [**eap \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) 結構中提供任何必要的 UI 內容資訊，其中 *dwDataType* 會設定為 *EapCredExpiryReq* ，而 *pbUiData* 則會指向類型為 [**EAP 認證 \_ \_ 需求**](eap-cred-req.md)的結構。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-112">The EAP method provides any necessary UI context information in the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, where *dwDataType* is set to *EapCredExpiryReq* and *pbUiData* points to a structure of type [**EAP\_CRED\_REQ**](eap-cred-req.md).</span></span>
-   <span data-ttu-id="1e3b2-113">在填入 [**eap \_ 互動式 \_ UI \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構時，此 EAP 方法只會填入 *curCreds* 參數，而不會在 eap 設定 **\_ \_ 輸入 \_ 欄位 \_ 資料** 結構中設定 [**eap \_ UI \_ 輸入 \_ 欄位 \_ .props \_ 唯讀 \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)旗標。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-113">While populating the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure, this EAP method will only fill in the *curCreds* parameter, and not set the [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag in the **EAP\_CONFIG\_INPUT\_FIELD\_DATA** structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="1e3b2-114">[**EAP \_ UI \_ 輸入 \_ 欄位 \_ .props \_ 唯讀 \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)旗標適用于需要變更的成員欄位 (s) 。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-114">The [**EAP\_UI\_INPUT\_FIELD\_PROPS\_READ\_ONLY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) flag is for member field(s) which need to be changed.</span></span>

     

-   <span data-ttu-id="1e3b2-115">在收集 UI 內容資訊之後，UI 程式會呈現 UI 來收集使用者的變更密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-115">Having collected the UI context informtion, the UI process renders a UI to collect change password information from the user.</span></span> <span data-ttu-id="1e3b2-116">這項資訊會填入 [**EAP 認證 \_ \_ 到期 \_ 需求**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)結構的 *NewCreds* 參數中。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-116">This information is populated in the *NewCreds* parameter of the [**EAP\_CRED\_EXPIRY\_REQ**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req) structure.</span></span>
-   <span data-ttu-id="1e3b2-117">UI 進程會透過 [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields)將 [**EAP 認證 \_ \_ RESP**](eap-cred-resp.md)結構傳回 EAPHost。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-117">The UI process passes the [**EAP\_CRED\_RESP**](eap-cred-resp.md) structure back to EAPHost via [**EapHostPeerQueryUIBlobFromInteractiveUIInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuiblobfrominteractiveuiinputfields).</span></span>
-   <span data-ttu-id="1e3b2-118">UI 進程會將此使用者 BLOB 傳遞給要求者，而要求者會照常繼續 EAPHost 執行時間函式。</span><span class="sxs-lookup"><span data-stu-id="1e3b2-118">The UI process passes this user BLOB to the supplicant, and the supplicant continues with EAPHost run-time functions as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e3b2-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e3b2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e3b2-120">SSO EAPHost 案例</span><span class="sxs-lookup"><span data-stu-id="1e3b2-120">SSO EAPHost Scenarios</span></span>](why-eaphost-sso.md)
</dt> <dt>

[<span data-ttu-id="1e3b2-121">SSO 和 PLAP</span><span class="sxs-lookup"><span data-stu-id="1e3b2-121">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




