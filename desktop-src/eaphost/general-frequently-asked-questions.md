---
title: 常見問題的一般問題
description: 閱讀 EAPHost Api 常見問題的解答，例如「驗證的存留期為何？」。
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "106966072"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="3aa1c-103">常見問題的一般問題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="3aa1c-104">下列主題提供有關 EAPHost Api 常見問題的解答。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="3aa1c-105">常見問題的一般問題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3aa1c-106">問題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-106">Question</span></span></th>
<th><span data-ttu-id="3aa1c-107">Answer</span><span class="sxs-lookup"><span data-stu-id="3aa1c-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3aa1c-108">什麼是要求者？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="3aa1c-109">要求者是要使用 EAPHost 進行驗證的實體。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="3aa1c-110">一般要求者為 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 用戶端、802.3 用戶端，以及路由及遠端存取服務 (RRAS) ，點對點 (PPP) 用戶端。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-111">什麼是對等？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-111">What is a peer?</span></span></td>
<td><span data-ttu-id="3aa1c-112">對等是 EAP 驗證的用戶端。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-113">對等和要求者有何不同？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="3aa1c-114">要求者會傳輸封包，而對等則不會傳輸封包。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="3aa1c-115">不過，對等、要求者和用戶端來說，這類詞彙大多同義。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-116">什麼是驗證器？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="3aa1c-117">驗證者是無線存取點、網路存取伺服器 (NAS) ，或是用來驗證要求者的網路存取裝置 (NAD) 。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="3aa1c-118">驗證器也稱為 EAP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-119">驗證的存留期為何？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="3aa1c-120">用戶端上單一驗證會話的存留期，是在 [<strong>EapHostPeerBeginSession</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 和 [<strong>EapHostPeerEndSession</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) 函式之間發生的所有事件。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="3aa1c-121">驗證端端的存留期是在 [<strong>EapPeerBeginSession</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) 和 [<strong>EapPeerEndSession</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) 函數之間發生的所有事件。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-122">什麼是 BLOB？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-122">What is a BLOB?</span></span> <span data-ttu-id="3aa1c-123">為什麼要將設定 (二進位) BLOB 轉換成 XML？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="3aa1c-124">BLOB 是二進位大型物件。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="3aa1c-125">XML 在二進位設定 BLOB 方面有幾個優點。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="3aa1c-126">以 XML 儲存的設定資料是人們可讀取、人類可編輯的，且跨平臺。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-127">何時要將儲存的 XML BLOB 轉換回二進位 BLOB？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="3aa1c-128">您可以儲存二進位 BLOB 或 XML BLOB，但在搭配執行時間 Api 使用之前，您必須一律將 XML BLOB 轉換回二進位 BLOB;執行時間 Api 無法接受 XML 目錄。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-129">什麼是原生方法？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-129">What are native methods?</span></span></td>
<td><span data-ttu-id="3aa1c-130">原生 EAP 方法會使用新的 EAPHost API。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-131">什麼是舊版方法？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="3aa1c-132">舊版 EAP 方法是在可延伸的 [驗證通訊協定參考](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference)中定義。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="3aa1c-133">舊版 EAP 方法可用於 Windows Vista 和 Windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="3aa1c-134">這些方法可能無法在後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-135">舊版和原生方法之間有何差異？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="3aa1c-136">原生 Api 更簡單，而且功能較少。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="3aa1c-137">所有新的 EAP 方法都應使用 EAPHost API 來撰寫。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-138">什麼是 &quot; 群組原則 &quot; ？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="3aa1c-139">如需群組原則的說明，請參閱 [群組原則收集](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-140">EAPHost 函式是否可以覆寫群組原則所指定的設定原則？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="3aa1c-141">否，永不。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-141">No, never.</span></span> <span data-ttu-id="3aa1c-142">如果群組原則已在使用中，群組原則設定一律會覆寫 EAPHost 設定。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-143">什麼是單一登入 (SSO) ？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="3aa1c-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 是第2層驗證機制。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="3aa1c-145">根據 SSO 設定，SSO 可讓使用者在登入 Windows 之前或立即使用 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 驗證來驗證網路。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="3aa1c-146">SSO 可以設定為使用 Windows 認證進行網路驗證 (在這種情況下，使用者只需輸入其認證一次) 或使用不同的 Windows 和網路驗證認證。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="3aa1c-147">如需詳細資訊，請參閱 [SSO 和 PLAP](understanding-sso-and-plap.md)。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-148">什麼是預先登入存取提供者 (PLAP) </span><span class="sxs-lookup"><span data-stu-id="3aa1c-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="3aa1c-149">如需詳細資訊，請參閱 [SSO 和 PLAP](understanding-sso-and-plap.md)。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-150">什麼是受保護的可延伸驗證通訊協定 (PEAP) ？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="3aa1c-151">如需詳細資訊，請參閱 [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) 和關於可延伸的 [驗證通訊協定](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol)。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-152">PEAP 如何處理會話繼續和重新驗證？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="3aa1c-153">在無線網路上漫遊時，通常會發生會話繼續和重新驗證。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="3aa1c-154">Windows Data Protection API (DPAPI) 提供一種方式來保護資料，並將資料系結至使用者，並選擇性地將登入會話系結。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="3aa1c-155">呼叫端會提供 [<strong>CryptProtectMemory</strong>] (/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) 未加密的緩衝區，而且 dpapi 會就地加密記憶體。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="3aa1c-156">稍後，呼叫端可以將加密的緩衝區傳入 [<strong>CryptUnprotectMemory</strong>] (/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) ，dpapi 會再次解密記憶體。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="3aa1c-157">如需詳細資訊，請參閱[](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) [ (TSL/IA) 和 PEAP 的 TLS 內部應用程式延伸](https://go.microsoft.com/fwlink/p/?linkid=84011)模組。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-158">什麼是 EAP-Transport 層級的安全性 (EAP-TLS) ？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="3aa1c-159">EAP-TLS 是一種用戶端-伺服器通訊協定，其中的相異憑證設定檔通常用於用戶端和伺服器。如需詳細資訊，請參閱 [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-160">如何? 使用本地安全機構 (LSA) API 來執行密碼變更？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="3aa1c-161">使用 [<strong>LsaCallAuthenticationPackage</strong>] (/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 函數來執行密碼變更。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-162">為什麼要在 EAPHost 中啟用追蹤？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="3aa1c-163">追蹤記錄檔包含 (僅提供英文的偵錯工具資訊) 可協助 Microsoft 開發人員和合作夥伴尋找任何在驗證程式中發生之問題的根本原因。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="3aa1c-164">如需詳細資訊，請參閱 [啟用追蹤](enabling-tracing.md)。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-165">為什麼當我使用 [密碼](/windows/desktop/SecCrypto/cryptography-portal) 編譯 API 登入 eap-tls exchange 時，NTE_BAD_KEY_STATE (0x8009000BL) 會遇到錯誤碼？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="3aa1c-166">在 Winerror.h 中 NTE_BAD_KEY_STATE (0x8009000BL) 定義為 &quot; 不正確索引鍵，以用於指定的狀態 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="3aa1c-167">此錯誤通常會在下列情況下傳回。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="3aa1c-168">嘗試匯出不可匯出的私密金鑰 BLOB 時</span><span class="sxs-lookup"><span data-stu-id="3aa1c-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="3aa1c-169">嘗試使用 [<strong>CryptCreateHash</strong>] (/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash 來產生虛擬隨機函式時， (PRF) 雜湊控制碼失敗) </span><span class="sxs-lookup"><span data-stu-id="3aa1c-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="3aa1c-170">如需詳細資訊，請參閱 [在 TLS 1.0 通訊協定中完成訊息](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol)。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3aa1c-171">什麼是虛擬隨機函式 (PRF) ？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="3aa1c-172">採用索引鍵、標籤和種子做為輸入的函式，然後產生任意長度的輸出。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="3aa1c-173">如需詳細資訊，請參閱 [在 TLS 1.0 通訊協定中完成訊息](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol)。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3aa1c-174">EAPHost 如何系結至網路介面卡？</span><span class="sxs-lookup"><span data-stu-id="3aa1c-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="3aa1c-175">EAPHost 可讓多個要求者同時運作，而且每個要求者都可以系結至多個網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="3aa1c-176">EAPHost 要求者會提供網路層的系結，並驅動驗證程式。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="3aa1c-177">要求者包含驗證設定。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="3aa1c-178">要求者也會儲存狀態，並提供後續的連接安全性。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="3aa1c-179">由於 EAPHost 不會直接系結至任何網路機制，因此要求者可以擴充性。</span><span class="sxs-lookup"><span data-stu-id="3aa1c-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="3aa1c-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3aa1c-181">EAPHost 要求者常見問題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="3aa1c-182">EAPHost 方法常見問題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="3aa1c-183">EAPHost 開發常見問題</span><span class="sxs-lookup"><span data-stu-id="3aa1c-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

