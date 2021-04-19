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
# <a name="general-frequently-asked-questions"></a>常見問題的一般問題

下列主題提供有關 EAPHost Api 常見問題的解答。

### <a name="general-frequently-asked-questions"></a>常見問題的一般問題



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>問題</th>
<th>Answer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>什麼是要求者？</td>
<td>要求者是要使用 EAPHost 進行驗證的實體。 一般要求者為 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 用戶端、802.3 用戶端，以及路由及遠端存取服務 (RRAS) ，點對點 (PPP) 用戶端。</td>
</tr>
<tr class="even">
<td>什麼是對等？</td>
<td>對等是 EAP 驗證的用戶端。</td>
</tr>
<tr class="odd">
<td>對等和要求者有何不同？</td>
<td>要求者會傳輸封包，而對等則不會傳輸封包。 不過，對等、要求者和用戶端來說，這類詞彙大多同義。</td>
</tr>
<tr class="even">
<td>什麼是驗證器？</td>
<td>驗證者是無線存取點、網路存取伺服器 (NAS) ，或是用來驗證要求者的網路存取裝置 (NAD) 。 驗證器也稱為 EAP 伺服器。</td>
</tr>
<tr class="odd">
<td>驗證的存留期為何？</td>
<td>用戶端上單一驗證會話的存留期，是在 [<strong>EapHostPeerBeginSession</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 和 [<strong>EapHostPeerEndSession</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) 函式之間發生的所有事件。 驗證端端的存留期是在 [<strong>EapPeerBeginSession</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) 和 [<strong>EapPeerEndSession</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) 函數之間發生的所有事件。</td>
</tr>
<tr class="even">
<td>什麼是 BLOB？ 為什麼要將設定 (二進位) BLOB 轉換成 XML？</td>
<td>BLOB 是二進位大型物件。 XML 在二進位設定 BLOB 方面有幾個優點。 以 XML 儲存的設定資料是人們可讀取、人類可編輯的，且跨平臺。</td>
</tr>
<tr class="odd">
<td>何時要將儲存的 XML BLOB 轉換回二進位 BLOB？</td>
<td>您可以儲存二進位 BLOB 或 XML BLOB，但在搭配執行時間 Api 使用之前，您必須一律將 XML BLOB 轉換回二進位 BLOB;執行時間 Api 無法接受 XML 目錄。</td>
</tr>
<tr class="even">
<td>什麼是原生方法？</td>
<td>原生 EAP 方法會使用新的 EAPHost API。</td>
</tr>
<tr class="odd">
<td>什麼是舊版方法？</td>
<td>舊版 EAP 方法是在可延伸的 [驗證通訊協定參考](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference)中定義。 舊版 EAP 方法可用於 Windows Vista 和 Windows Server 2008。 這些方法可能無法在後續版本的作業系統中使用。</td>
</tr>
<tr class="even">
<td>舊版和原生方法之間有何差異？</td>
<td>原生 Api 更簡單，而且功能較少。 所有新的 EAP 方法都應使用 EAPHost API 來撰寫。</td>
</tr>
<tr class="odd">
<td>什麼是 &quot; 群組原則 &quot; ？</td>
<td>如需群組原則的說明，請參閱 [群組原則收集](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10))。</td>
</tr>
<tr class="even">
<td>EAPHost 函式是否可以覆寫群組原則所指定的設定原則？</td>
<td>否，永不。 如果群組原則已在使用中，群組原則設定一律會覆寫 EAPHost 設定。</td>
</tr>
<tr class="odd">
<td>什麼是單一登入 (SSO) ？</td>
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 是第2層驗證機制。 根據 SSO 設定，SSO 可讓使用者在登入 Windows 之前或立即使用 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 驗證來驗證網路。 SSO 可以設定為使用 Windows 認證進行網路驗證 (在這種情況下，使用者只需輸入其認證一次) 或使用不同的 Windows 和網路驗證認證。 如需詳細資訊，請參閱 [SSO 和 PLAP](understanding-sso-and-plap.md)。<br/></td>
</tr>
<tr class="even">
<td>什麼是預先登入存取提供者 (PLAP) </td>
<td>如需詳細資訊，請參閱 [SSO 和 PLAP](understanding-sso-and-plap.md)。</td>
</tr>
<tr class="odd">
<td>什麼是受保護的可延伸驗證通訊協定 (PEAP) ？</td>
<td>如需詳細資訊，請參閱 [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) 和關於可延伸的 [驗證通訊協定](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol)。</td>
</tr>
<tr class="even">
<td>PEAP 如何處理會話繼續和重新驗證？</td>
<td>在無線網路上漫遊時，通常會發生會話繼續和重新驗證。 Windows Data Protection API (DPAPI) 提供一種方式來保護資料，並將資料系結至使用者，並選擇性地將登入會話系結。 呼叫端會提供 [<strong>CryptProtectMemory</strong>] (/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) 未加密的緩衝區，而且 dpapi 會就地加密記憶體。 稍後，呼叫端可以將加密的緩衝區傳入 [<strong>CryptUnprotectMemory</strong>] (/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) ，dpapi 會再次解密記憶體。 如需詳細資訊，請參閱[](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) [ (TSL/IA) 和 PEAP 的 TLS 內部應用程式延伸](https://go.microsoft.com/fwlink/p/?linkid=84011)模組。<br/></td>
</tr>
<tr class="odd">
<td>什麼是 EAP-Transport 層級的安全性 (EAP-TLS) ？</td>
<td>EAP-TLS 是一種用戶端-伺服器通訊協定，其中的相異憑證設定檔通常用於用戶端和伺服器。如需詳細資訊，請參閱 [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10))。<br/></td>
</tr>
<tr class="even">
<td>如何? 使用本地安全機構 (LSA) API 來執行密碼變更？</td>
<td>使用 [<strong>LsaCallAuthenticationPackage</strong>] (/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) 函數來執行密碼變更。</td>
</tr>
<tr class="odd">
<td>為什麼要在 EAPHost 中啟用追蹤？</td>
<td>追蹤記錄檔包含 (僅提供英文的偵錯工具資訊) 可協助 Microsoft 開發人員和合作夥伴尋找任何在驗證程式中發生之問題的根本原因。 如需詳細資訊，請參閱 [啟用追蹤](enabling-tracing.md)。<br/></td>
</tr>
<tr class="even">
<td>為什麼當我使用 [密碼](/windows/desktop/SecCrypto/cryptography-portal) 編譯 API 登入 eap-tls exchange 時，NTE_BAD_KEY_STATE (0x8009000BL) 會遇到錯誤碼？</td>
<td>在 Winerror.h 中 NTE_BAD_KEY_STATE (0x8009000BL) 定義為 &quot; 不正確索引鍵，以用於指定的狀態 &quot; 。 此錯誤通常會在下列情況下傳回。
<ul>
<li>嘗試匯出不可匯出的私密金鑰 BLOB 時</li>
<li>嘗試使用 [<strong>CryptCreateHash</strong>] (/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash 來產生虛擬隨機函式時， (PRF) 雜湊控制碼失敗) </li>
</ul>
如需詳細資訊，請參閱 [在 TLS 1.0 通訊協定中完成訊息](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol)。</td>
</tr>
<tr class="odd">
<td>什麼是虛擬隨機函式 (PRF) ？</td>
<td>採用索引鍵、標籤和種子做為輸入的函式，然後產生任意長度的輸出。 如需詳細資訊，請參閱 [在 TLS 1.0 通訊協定中完成訊息](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol)。<br/></td>
</tr>
<tr class="even">
<td>EAPHost 如何系結至網路介面卡？</td>
<td>EAPHost 可讓多個要求者同時運作，而且每個要求者都可以系結至多個網路介面卡。 EAPHost 要求者會提供網路層的系結，並驅動驗證程式。 要求者包含驗證設定。 要求者也會儲存狀態，並提供後續的連接安全性。 由於 EAPHost 不會直接系結至任何網路機制，因此要求者可以擴充性。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 要求者常見問題](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[EAPHost 方法常見問題](eap-method-frequently-asked-questions.md)
</dt> <dt>

[EAPHost 開發常見問題](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

