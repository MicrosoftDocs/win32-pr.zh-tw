---
title: EAPHost 要求者的常見問題
description: 本主題提供 EAPHost 要求者 API 常見問題的解答。
ms.assetid: bf8db711-386e-47c2-be47-4cfd6c4d8d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38e75220b186ef58f2b9f264f8f5fc0550a4119
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "103684357"
---
# <a name="eaphost-supplicant-frequently-asked-questions"></a><span data-ttu-id="af9c5-103">EAPHost 要求者的常見問題</span><span class="sxs-lookup"><span data-stu-id="af9c5-103">EAPHost Supplicant Frequently Asked Questions</span></span>

<span data-ttu-id="af9c5-104">本主題提供 EAPHost 要求者 API 常見問題的解答。</span><span class="sxs-lookup"><span data-stu-id="af9c5-104">This topic provides answers to commonly-asked questions about the EAPHost Supplicant API.</span></span>

### <a name="eaphost-supplicant-frequently-asked-questions"></a><span data-ttu-id="af9c5-105">EAPHost 要求者的常見問題</span><span class="sxs-lookup"><span data-stu-id="af9c5-105">EAPHost Supplicant Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af9c5-106">問題</span><span class="sxs-lookup"><span data-stu-id="af9c5-106">Question</span></span></th>
<th><span data-ttu-id="af9c5-107">Answer</span><span class="sxs-lookup"><span data-stu-id="af9c5-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af9c5-108">為什麼我需要呼叫 [<strong>EapHostPeerInitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) 和 [<strong>EapHostPeerUninitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) ？</span><span class="sxs-lookup"><span data-stu-id="af9c5-108">Why do I need to call [<strong>EapHostPeerInitialize</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) and [<strong>EapHostPeerUninitialize</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize)?</span></span></td>
<td><span data-ttu-id="af9c5-109">[<strong>EapHostPeerInitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) 和 [<strong>EapHostPeerUninitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) 初始化和解除初始化用於處理序間通訊的 COM 環境， (要求者與 EAPHost 之間的 IPC) 。</span><span class="sxs-lookup"><span data-stu-id="af9c5-109">[<strong>EapHostPeerInitialize</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) and [<strong>EapHostPeerUninitialize</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) initialize and uninitialize the COM environment used for interprocess communication (IPC) between a supplicant and EAPHost.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-110">哪些函數必須在已針對 [單一線程單元](/previous-versions/ms810413(v=msdn.10)) (STA) 的 COM 初始化的執行緒上叫用？</span><span class="sxs-lookup"><span data-stu-id="af9c5-110">Which functions must be invoked on threads that have COM initialized for [Single Threaded Apartment](/previous-versions/ms810413(v=msdn.10)) (STA)?</span></span></td>
<td><span data-ttu-id="af9c5-111">[<strong>EapHostPeerInvokeConfigUI</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) 、[<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) 和 [<strong>EapHostAuthenticatorInvokeConfigUI</strong>] (/PREVIOUS-VERSIONS/WINDOWS/DESKTOP/API/EAPMETHODAUTHENTICATORAPIS/NF-EAPMETHODAUTHENTICATORAPIS-EAPMETHODAUTHENTICATORINVOKECONFIGUI) 必須在已針對 STA 初始化 COM 的執行緒上呼叫。</span><span class="sxs-lookup"><span data-stu-id="af9c5-111">[<strong>EapHostPeerInvokeConfigUI</strong>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), [<strong>EapHostPeerInvokeInteractiveUI</strong>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui), and [<strong>EapHostAuthenticatorInvokeConfigUI</strong>](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui) must be called on threads that have COM initialized for STA.</span></span> <span data-ttu-id="af9c5-112">您可以呼叫 COM API [<strong>CoInitialize</strong>] (/windows/win32/api/objbase/nf-objbase-coinitialize) ; 來達成此目的當要求者完成 STA 執行緒 [<strong>CoUninitialize</strong>] 時 (/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 必須在結束之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="af9c5-112">This can be achieved by calling COM API [<strong>CoInitialize</strong>](/windows/win32/api/objbase/nf-objbase-coinitialize); when the supplicant has finished with the STA thread [<strong>CoUninitialize</strong>](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) must be called before exiting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-113">EAPHost 如何匯出加密材料？</span><span class="sxs-lookup"><span data-stu-id="af9c5-113">How does EAPHost export keying material?</span></span></td>
<td><span data-ttu-id="af9c5-114">EAPHost EAP 方法會將主要工作階段金鑰匯出 (MSKs) 以 Microsoft 點對點加密形式 (MPPE) 金鑰給要求者。</span><span class="sxs-lookup"><span data-stu-id="af9c5-114">EAPHost EAP methods export Master Session Keys (MSKs)in the form of Microsoft Point-to-Point Encryption (MPPE) keys to the supplicants.</span></span> <span data-ttu-id="af9c5-115">使用 MSK 的要求者可以產生額外的金鑰處理內容，例如成對的主要金鑰 (Pmk) 。</span><span class="sxs-lookup"><span data-stu-id="af9c5-115">Additional keying material, such as Pairwise Master Keys (PMKs) can be generated by the supplicant using the MSK.</span></span> <span data-ttu-id="af9c5-116">針對在驗證期間產生任何其他金鑰的方法，這些方法可以提供這些金鑰做為要求者的廠商專屬屬性。</span><span class="sxs-lookup"><span data-stu-id="af9c5-116">For the methods to generate any other keys during authentication, the methods can provide those keys as vendor-specific attributes to the supplicants.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-117">什麼是 (EMSK) 的擴充主要工作階段金鑰？</span><span class="sxs-lookup"><span data-stu-id="af9c5-117">What is an Extended Master Session Key (EMSK)?</span></span></td>
<td><span data-ttu-id="af9c5-118">EMSK 是 EAP 方法所匯出的額外金鑰內容。</span><span class="sxs-lookup"><span data-stu-id="af9c5-118">EMSK is additional keying material that is exported by the EAP method.</span></span> <span data-ttu-id="af9c5-119">EMSK 長度至少為64個八位。</span><span class="sxs-lookup"><span data-stu-id="af9c5-119">EMSK is at least 64 octets in length.</span></span> <span data-ttu-id="af9c5-120">EMSK 是在 EAP 用戶端與伺服器之間共用，但不會與驗證者或任何其他協力廠商共用。</span><span class="sxs-lookup"><span data-stu-id="af9c5-120">EMSK is shared between the EAP client and server, but is not shared with the authenticator or any other third party.</span></span> <span data-ttu-id="af9c5-121">目前，EMSK 已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="af9c5-121">Currently, EMSK is reserved for future use.</span></span> <span data-ttu-id="af9c5-122">如需詳細資訊，請參閱 [無線區域網路的可延伸驗證通訊協定 EAP) 方法需求](https://go.microsoft.com/fwlink/p/?linkid=84064)。</span><span class="sxs-lookup"><span data-stu-id="af9c5-122">For more information, see [Extensible Authentication Protocol EAP) Method Requirements for Wireless LANs](https://go.microsoft.com/fwlink/p/?linkid=84064).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-123">方法使用或產生屬性的時機為何？</span><span class="sxs-lookup"><span data-stu-id="af9c5-123">When does a method consume or generate an attribute?</span></span></td>
<td><span data-ttu-id="af9c5-124">如果 EAP 方法產生屬性或 EMSK，則要求者將會使用屬性。</span><span class="sxs-lookup"><span data-stu-id="af9c5-124">If an EAP method generates attributes or EMSK, then the supplicant will consume attributes.</span></span> <span data-ttu-id="af9c5-125">通常，要求者取用的屬性是索引鍵。</span><span class="sxs-lookup"><span data-stu-id="af9c5-125">Typically, attributes that are consumed by supplicants are keys.</span></span> <span data-ttu-id="af9c5-126">使用的屬性為 <strong>eatPeerId</strong>、 <strong>eatServerId</strong>、 <strong>eatMethodId</strong>、 <strong>eatEMSK</strong>和 <strong>eatCredentialsChanged</strong>。</span><span class="sxs-lookup"><span data-stu-id="af9c5-126">The attributes consumed are <strong>eatPeerId</strong>, <strong>eatServerId</strong>, <strong>eatMethodId</strong>, <strong>eatEMSK</strong>, and <strong>eatCredentialsChanged</strong>.</span></span> <span data-ttu-id="af9c5-127">如需詳細資訊，請參閱 [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type) 。</span><span class="sxs-lookup"><span data-stu-id="af9c5-127">For more information, see [<strong>EAP_ATTRIBUTE_TYPE</strong>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span> <span data-ttu-id="af9c5-128">EAP 方法可以匯出其他應用程式特定的 EMSK 資料，例如：</span><span class="sxs-lookup"><span data-stu-id="af9c5-128">An EAP method can export additional application-specific EMSK material such as:</span></span>
<ul>
<li><span data-ttu-id="af9c5-129">工作階段識別碼</span><span class="sxs-lookup"><span data-stu-id="af9c5-129">Session ID</span></span></li>
<li><span data-ttu-id="af9c5-130">[網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) </span><span class="sxs-lookup"><span data-stu-id="af9c5-130">[Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-131">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10))使用哪些屬性？</span><span class="sxs-lookup"><span data-stu-id="af9c5-131">Which attributes does [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) consume?</span></span></td>
<td><span data-ttu-id="af9c5-132">原生無線 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 要求者將會使用下列 EAPHost authentication 屬性：</span><span class="sxs-lookup"><span data-stu-id="af9c5-132">The native wireless [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant will consume the following EAPHost authentication attributes:</span></span>
<ul>
<li><span data-ttu-id="af9c5-133">變更密碼通知</span><span class="sxs-lookup"><span data-stu-id="af9c5-133">Change password notification</span></span></li>
<li><span data-ttu-id="af9c5-134">Microsoft 點對點加密 (MPPE) 傳送/接收金鑰。</span><span class="sxs-lookup"><span data-stu-id="af9c5-134">Microsoft Point-to-Point Encryption (MPPE) send/receive keys.</span></span> <span data-ttu-id="af9c5-135">VendorId/VendorType = 331/16 和311/1</span><span class="sxs-lookup"><span data-stu-id="af9c5-135">VendorId/VendorType = 331/16 and 311/1</span></span></li>
</ul>
<span data-ttu-id="af9c5-136">MPPE 金鑰是在驗證成功後，由對等和驗證器所產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="af9c5-136">MPPE keys are keys generated at the end of successful authentication, by both peer and authenticator.</span></span> <span data-ttu-id="af9c5-137">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10))和網路存取伺服器會使用這些機碼 (NAS) 將傳送和接收的封包加密和解密。</span><span class="sxs-lookup"><span data-stu-id="af9c5-137">These keys are used by [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and the network access server (NAS) to encrypt and decrypt packets that are sent and received.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-138">EAPHost 中的 EAP_PEER_FLAG_GUEST_ACCESS 旗標有何用途？</span><span class="sxs-lookup"><span data-stu-id="af9c5-138">What's the purpose of the EAP_PEER_FLAG_GUEST_ACCESS flag in EAPHost?</span></span></td>
<td><span data-ttu-id="af9c5-139">在 [<strong>EAPHostPeerBeginSession</strong>] 中設定此旗標時 (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 中，EAPHost 會將此旗標解釋為 guest 授權的要求，並傳回 <strong>Null</strong> 身分識別回應，然後傳遞給要求者並傳回到 EAP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="af9c5-139">When this flag is set in [<strong>EAPHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession), EAPHost interprets this as a request for guest authorization and returns a <strong>NULL</strong> identity response that is then passed to the supplicant and returned to the EAP Server.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-140">要求者如何要求電腦驗證？</span><span class="sxs-lookup"><span data-stu-id="af9c5-140">How does the supplicant request machine authentication?</span></span></td>
<td><span data-ttu-id="af9c5-141">藉由設定 [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 旗標來要求電腦驗證。</span><span class="sxs-lookup"><span data-stu-id="af9c5-141">Machine authentication is requested by setting the [<strong>EAP_FLAG_MACHINE_AUTH</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) flag.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-142">要求者如何要求使用者驗證？</span><span class="sxs-lookup"><span data-stu-id="af9c5-142">How does the supplicant request user authentication?</span></span></td>
<td><span data-ttu-id="af9c5-143">未設定 [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 旗標，要求使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="af9c5-143">User authentication is requested by not setting the [<strong>EAP_FLAG_MACHINE_AUTH</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-144">何時使用 [<strong>EapHostPeerFreeErrorMemory</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) ，而不是 [<strong>EapHostFreeEapError</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) 函數？</span><span class="sxs-lookup"><span data-stu-id="af9c5-144">When do I use [<strong>EapHostPeerFreeErrorMemory</strong>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) instead of the [<strong>EapHostFreeEapError</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) function?</span></span></td>
<td><span data-ttu-id="af9c5-145">[<strong>EapHostPeerFreeErrorMemory</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) 函數僅用於釋出 EAPHost 設定 api 所傳回的 [<strong>EAP_ERROR</strong>] (/windows/desktop/api/eaptypes/ns-eaptypes-eap_error) 結構。</span><span class="sxs-lookup"><span data-stu-id="af9c5-145">The [<strong>EapHostPeerFreeErrorMemory</strong>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) function is used only for freeing [<strong>EAP_ERROR</strong>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error) structures returned by EAPHost configuration APIs.</span></span> <span data-ttu-id="af9c5-146">EAPHost 設定 Api 定義于 EapHostPeerConfigApis 中。</span><span class="sxs-lookup"><span data-stu-id="af9c5-146">EAPHost configuration APIs are defined in EapHostPeerConfigApis.h.</span></span> <span data-ttu-id="af9c5-147">相反地，[<strong>EapHostPeerFreeEapError</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) 函式是用來釋放 EAPHost 執行時間 api 所傳回的 <strong>EAP_ERROR</strong> 結構。</span><span class="sxs-lookup"><span data-stu-id="af9c5-147">In contrast, the [<strong>EapHostPeerFreeEapError</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) function is used for freeing <strong>EAP_ERROR</strong> structures returned by EAPHost run-time APIs.</span></span> <span data-ttu-id="af9c5-148">EAPHost 執行時間 Api 定義于 EapPApis 中。</span><span class="sxs-lookup"><span data-stu-id="af9c5-148">EAPHost run-time APIs are defined in EapPApis.h.</span></span> <span data-ttu-id="af9c5-149">請勿使用 API 的執行時間版本搭配 Api 的設定版本;若要這麼做，可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="af9c5-149">Never use the run-time version of the API with the configuration version of the APIs; to do so could produce unexpected results.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-150">我已在我用來處理要求者上 EAP 驗證會話的相同執行緒中，執行我的 UI。</span><span class="sxs-lookup"><span data-stu-id="af9c5-150">I have implemented my UI in the same thread that I use to process an EAP authentication session on the supplicant.</span></span> <span data-ttu-id="af9c5-151">當我引發互動式使用者介面對話方塊來取得認證或其他使用者輸入資料之後，EAPHost 對 EAP 對等方法的下一個呼叫會失敗，並出現 <strong>ERROR_OBJECT_DISCONNECTED</strong>。</span><span class="sxs-lookup"><span data-stu-id="af9c5-151">After I have raised an interactive user interface dialog box to obtain credentials or other user input data, the next call by the EAPHost to an EAP peer method fails with <strong>ERROR_OBJECT_DISCONNECTED</strong>.</span></span> <span data-ttu-id="af9c5-152">為什麼會發生這種情況，以及如何解決此問題？</span><span class="sxs-lookup"><span data-stu-id="af9c5-152">Why has this occurred, and how do I address it?</span></span></td>
<td><span data-ttu-id="af9c5-153">雖然 EAPHost 用戶端 Api 都是 C 樣式 Api，但這些 C Api 只是對應 COM Api 的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="af9c5-153">While the EAPHost client-side APIs are all C style APIs, these C APIs are just wrappers of corresponding COM APIs.</span></span> <span data-ttu-id="af9c5-154">C 樣式 Api 會在多執行緒 COM 環境中執行。</span><span class="sxs-lookup"><span data-stu-id="af9c5-154">The C style APIs run in a multithreaded COM environment.</span></span> <span data-ttu-id="af9c5-155">UI 程式碼通常會在單元執行緒模型中執行。</span><span class="sxs-lookup"><span data-stu-id="af9c5-155">UI code usually runs in the apartment thread model.</span></span> <span data-ttu-id="af9c5-156">因為這兩個執行緒模型彼此衝突，所以請勿在處理 EAP 驗證的相同執行緒中執行 UI 程式碼。</span><span class="sxs-lookup"><span data-stu-id="af9c5-156">Because the two thread models conflict with one another, do not run the UI code in the same thread that processes EAP authentications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-157">為什麼 [<strong>EapHostPeerBeginSession</strong>] (/PREVIOUS-VERSIONS/WINDOWS/DESKTOP/API/EAPPAPIS/NF-EAPPAPIS-EAPHOSTPEERBEGINSESSION) api 採用 [<em>NotificationHandler</em>] (/previous-versions/windows/desktop/api) 回呼函式指標做為參數？</span><span class="sxs-lookup"><span data-stu-id="af9c5-157">Why does the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) API take a [<em>NotificationHandler</em>](/previous-versions/windows/desktop/api) callback function pointer as a parameter?</span></span></td>
<td><span data-ttu-id="af9c5-158">[<em>NotificationHandler</em>] (/previous-versions/windows/desktop/api) 是一種機制，要求者會收到其必須重新驗證的機制。</span><span class="sxs-lookup"><span data-stu-id="af9c5-158">[<em>NotificationHandler</em>](/previous-versions/windows/desktop/api) is the mechanism by which a supplicant is notified that it must re-authenticate.</span></span> <span data-ttu-id="af9c5-159">在許多情況下，要求者必須重新進行驗證，包括使用 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) 進行驗證。</span><span class="sxs-lookup"><span data-stu-id="af9c5-159">There are various scenarios where the supplicant is required to re-authenticate, including authentication with [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-160">在 [<strong>EapHostPeerBeginSession</strong>] (/PREVIOUS-VERSIONS/WINDOWS/DESKTOP/API/EAPPAPIS/NF-EAPPAPIS-EAPHOSTPEERBEGINSESSION) api 中， <em>pConnectionId</em>參數的用途為何？</span><span class="sxs-lookup"><span data-stu-id="af9c5-160">What is the purpose of the <em>pConnectionId</em> parameter in the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) API?</span></span></td>
<td><span data-ttu-id="af9c5-161"><em>pConnectionId</em> 是要求者定義的 GUID 值的指標，用來識別屬於要求者的網路連接。</span><span class="sxs-lookup"><span data-stu-id="af9c5-161"><em>pConnectionId</em> is a pointer to a supplicant-defined GUID value used to identify a network connection that belongs to the supplicant.</span></span> <span data-ttu-id="af9c5-162">呼叫 [<em>NotificationHandler</em>] (/previous-versions/windows/desktop/api) 回呼函式時，會傳遞此 GUID 來識別要求者將用來重新驗證要求的網路連接。</span><span class="sxs-lookup"><span data-stu-id="af9c5-162">When the [<em>NotificationHandler</em>](/previous-versions/windows/desktop/api) callback function is called, this GUID is passed to identify the network connection that the supplicant will use for re-authentication requests.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-163">如何? 知道隔離狀態是否有變更？</span><span class="sxs-lookup"><span data-stu-id="af9c5-163">How do I know if there is a change in quarantine state?</span></span></td>
<td><span data-ttu-id="af9c5-164">只有當至少有一個網路存取保護 (NAP) 隔離強制用戶端 (QEC 系統中) 註冊的介面時，使用者才會收到隔離狀態變更的視覺通知。</span><span class="sxs-lookup"><span data-stu-id="af9c5-164">The user will receive visual notification of a change in quarantine state only if there is at least one Network Access Protection (NAP) quarantine enforcement client (QEC) registered interface in the system.</span></span> <span data-ttu-id="af9c5-165">如果是，則在嘗試重新驗證時，使用者將會透過快顯視窗收到隔離狀態變更的通知。</span><span class="sxs-lookup"><span data-stu-id="af9c5-165">If so, when re-authentication is attempted the user will be notified of a quarantine state change via a pop-up window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-166">如何? 知道系統中是否有 NAP QEC 註冊介面？</span><span class="sxs-lookup"><span data-stu-id="af9c5-166">How do I know if there is a NAP QEC registered interface in the system?</span></span></td>
<td><span data-ttu-id="af9c5-167">開啟提升許可權的視窗，然後執行下列 netsh 命令： &quot; netsh nap client show state &quot; 。</span><span class="sxs-lookup"><span data-stu-id="af9c5-167">Open an elevated window, and run the following netsh command: &quot;netsh nap client show state&quot;.</span></span> <span data-ttu-id="af9c5-168">如需詳細資訊，請參閱 [Netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="af9c5-168">For more information, see [Netsh Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-169">如果要求者重新驗證，QEC 在重新驗證期間應使用何種連接識別碼？</span><span class="sxs-lookup"><span data-stu-id="af9c5-169">If the supplicant re-authenticates, what connection ID should the QEC use during re-authentication?</span></span></td>
<td><span data-ttu-id="af9c5-170">QEC 應該使用先前會話所用的相同連接識別碼。</span><span class="sxs-lookup"><span data-stu-id="af9c5-170">The QEC should use the same connection ID that was used for the previous session.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-171">只有一個 EAPHost 要求者方法可用來顯示 (UI) 對話方塊的使用者介面，但 EAP 方法有數種類型的 UI 特定呼叫。</span><span class="sxs-lookup"><span data-stu-id="af9c5-171">There is only one EAPHost supplicant method available to display user interface (UI) dialog boxes, but EAP methods have several types of UI-specific calls.</span></span> <span data-ttu-id="af9c5-172">當要求者取得 <strong>EapHostPeerResponseInvokeUI</strong> 動作程式碼時，應呼叫何種方法，指出要求者必須顯示 UI 對話方塊？</span><span class="sxs-lookup"><span data-stu-id="af9c5-172">What method should the supplicant call when it obtains the <strong>EapHostPeerResponseInvokeUI</strong> action code, indicating that the supplicant must display a UI dialog box?</span></span></td>
<td><span data-ttu-id="af9c5-173">使用者不需要採取任何動作，因為 EAPHost 知道要呼叫哪一個方法函數。</span><span class="sxs-lookup"><span data-stu-id="af9c5-173">No action is required by the user because EAPHost knows which method function to call.</span></span> <span data-ttu-id="af9c5-174">例如，傳回動作程式碼 <strong>EapHostPeerResponseInvokeUI</strong> 時，要求者會以下列順序呼叫這三個函式： [<strong>EapHostPeerGetUICoNtext</strong>] (/Previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicoNtext) 、[<strong>EapHostPeerInvokeInteractiveUI</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) 和 [<strong>EapHostPeerSetUICoNtext</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicoNtext) 。</span><span class="sxs-lookup"><span data-stu-id="af9c5-174">For instance, when action code <strong>EapHostPeerResponseInvokeUI</strong> is returned, the supplicant calls these three functions in the following order: [<strong>EapHostPeerGetUIContext</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext), [<strong>EapHostPeerInvokeInteractiveUI</strong>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui), and [<strong>EapHostPeerSetUIContext</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af9c5-175">認證 BLOB 與設定 BLOB 之間有何差異？</span><span class="sxs-lookup"><span data-stu-id="af9c5-175">What is the difference between a credentials BLOB and a configuration BLOB?</span></span></td>
<td><span data-ttu-id="af9c5-176">認證 BLOB 只包含使用者資料，例如使用者名稱、密碼和 PIN。</span><span class="sxs-lookup"><span data-stu-id="af9c5-176">The credentials BLOB contains only user data such as user name, password, and PIN.</span></span> <span data-ttu-id="af9c5-177">設定 BLOB 包含控制方法行為的設定。</span><span class="sxs-lookup"><span data-stu-id="af9c5-177">The configuration BLOB contains the settings that control the behavior of the method.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af9c5-178">是否可以在 EAPHost 用戶端上啟用追蹤？</span><span class="sxs-lookup"><span data-stu-id="af9c5-178">Can I enable tracing on the EAPHost client side?</span></span></td>
<td><span data-ttu-id="af9c5-179">是。</span><span class="sxs-lookup"><span data-stu-id="af9c5-179">Yes.</span></span> <span data-ttu-id="af9c5-180">如需詳細資訊，請參閱 [啟用追蹤](enabling-tracing.md)。</span><span class="sxs-lookup"><span data-stu-id="af9c5-180">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="af9c5-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="af9c5-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af9c5-182">EAPHost 要求者 API 參考</span><span class="sxs-lookup"><span data-stu-id="af9c5-182">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)
</dt> <dt>

[<span data-ttu-id="af9c5-183">EAPHost 一般常見問題</span><span class="sxs-lookup"><span data-stu-id="af9c5-183">EAPHost General FAQs</span></span>](general-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="af9c5-184">EAPHost 方法常見問題</span><span class="sxs-lookup"><span data-stu-id="af9c5-184">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="af9c5-185">EAPHost 開發常見問題</span><span class="sxs-lookup"><span data-stu-id="af9c5-185">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

