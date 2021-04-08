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
# <a name="eaphost-supplicant-frequently-asked-questions"></a>EAPHost 要求者的常見問題

本主題提供 EAPHost 要求者 API 常見問題的解答。

### <a name="eaphost-supplicant-frequently-asked-questions"></a>EAPHost 要求者的常見問題



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
<td>為什麼我需要呼叫 [<strong>EapHostPeerInitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) 和 [<strong>EapHostPeerUninitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) ？</td>
<td>[<strong>EapHostPeerInitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerinitialize) 和 [<strong>EapHostPeerUninitialize</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeeruninitialize) 初始化和解除初始化用於處理序間通訊的 COM 環境， (要求者與 EAPHost 之間的 IPC) 。</td>
</tr>
<tr class="even">
<td>哪些函數必須在已針對 [單一線程單元](/previous-versions/ms810413(v=msdn.10)) (STA) 的 COM 初始化的執行緒上叫用？</td>
<td>[<strong>EapHostPeerInvokeConfigUI</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) 、[<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) 和 [<strong>EapHostAuthenticatorInvokeConfigUI</strong>] (/PREVIOUS-VERSIONS/WINDOWS/DESKTOP/API/EAPMETHODAUTHENTICATORAPIS/NF-EAPMETHODAUTHENTICATORAPIS-EAPMETHODAUTHENTICATORINVOKECONFIGUI) 必須在已針對 STA 初始化 COM 的執行緒上呼叫。 您可以呼叫 COM API [<strong>CoInitialize</strong>] (/windows/win32/api/objbase/nf-objbase-coinitialize) ; 來達成此目的當要求者完成 STA 執行緒 [<strong>CoUninitialize</strong>] 時 (/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 必須在結束之前呼叫。</td>
</tr>
<tr class="odd">
<td>EAPHost 如何匯出加密材料？</td>
<td>EAPHost EAP 方法會將主要工作階段金鑰匯出 (MSKs) 以 Microsoft 點對點加密形式 (MPPE) 金鑰給要求者。 使用 MSK 的要求者可以產生額外的金鑰處理內容，例如成對的主要金鑰 (Pmk) 。 針對在驗證期間產生任何其他金鑰的方法，這些方法可以提供這些金鑰做為要求者的廠商專屬屬性。</td>
</tr>
<tr class="even">
<td>什麼是 (EMSK) 的擴充主要工作階段金鑰？</td>
<td>EMSK 是 EAP 方法所匯出的額外金鑰內容。 EMSK 長度至少為64個八位。 EMSK 是在 EAP 用戶端與伺服器之間共用，但不會與驗證者或任何其他協力廠商共用。 目前，EMSK 已保留供日後使用。 如需詳細資訊，請參閱 [無線區域網路的可延伸驗證通訊協定 EAP) 方法需求](https://go.microsoft.com/fwlink/p/?linkid=84064)。<br/></td>
</tr>
<tr class="odd">
<td>方法使用或產生屬性的時機為何？</td>
<td>如果 EAP 方法產生屬性或 EMSK，則要求者將會使用屬性。 通常，要求者取用的屬性是索引鍵。 使用的屬性為 <strong>eatPeerId</strong>、 <strong>eatServerId</strong>、 <strong>eatMethodId</strong>、 <strong>eatEMSK</strong>和 <strong>eatCredentialsChanged</strong>。 如需詳細資訊，請參閱 [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type) 。 EAP 方法可以匯出其他應用程式特定的 EMSK 資料，例如：
<ul>
<li>工作階段識別碼</li>
<li>[網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) </li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10))使用哪些屬性？</td>
<td>原生無線 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 要求者將會使用下列 EAPHost authentication 屬性：
<ul>
<li>變更密碼通知</li>
<li>Microsoft 點對點加密 (MPPE) 傳送/接收金鑰。 VendorId/VendorType = 331/16 和311/1</li>
</ul>
MPPE 金鑰是在驗證成功後，由對等和驗證器所產生的金鑰。 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10))和網路存取伺服器會使用這些機碼 (NAS) 將傳送和接收的封包加密和解密。<br/></td>
</tr>
<tr class="odd">
<td>EAPHost 中的 EAP_PEER_FLAG_GUEST_ACCESS 旗標有何用途？</td>
<td>在 [<strong>EAPHostPeerBeginSession</strong>] 中設定此旗標時 (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 中，EAPHost 會將此旗標解釋為 guest 授權的要求，並傳回 <strong>Null</strong> 身分識別回應，然後傳遞給要求者並傳回到 EAP 伺服器。</td>
</tr>
<tr class="even">
<td>要求者如何要求電腦驗證？</td>
<td>藉由設定 [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 旗標來要求電腦驗證。</td>
</tr>
<tr class="odd">
<td>要求者如何要求使用者驗證？</td>
<td>未設定 [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) 旗標，要求使用者驗證。</td>
</tr>
<tr class="even">
<td>何時使用 [<strong>EapHostPeerFreeErrorMemory</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) ，而不是 [<strong>EapHostFreeEapError</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) 函數？</td>
<td>[<strong>EapHostPeerFreeErrorMemory</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) 函數僅用於釋出 EAPHost 設定 api 所傳回的 [<strong>EAP_ERROR</strong>] (/windows/desktop/api/eaptypes/ns-eaptypes-eap_error) 結構。 EAPHost 設定 Api 定義于 EapHostPeerConfigApis 中。 相反地，[<strong>EapHostPeerFreeEapError</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror) 函式是用來釋放 EAPHost 執行時間 api 所傳回的 <strong>EAP_ERROR</strong> 結構。 EAPHost 執行時間 Api 定義于 EapPApis 中。 請勿使用 API 的執行時間版本搭配 Api 的設定版本;若要這麼做，可能會產生非預期的結果。<br/></td>
</tr>
<tr class="odd">
<td>我已在我用來處理要求者上 EAP 驗證會話的相同執行緒中，執行我的 UI。 當我引發互動式使用者介面對話方塊來取得認證或其他使用者輸入資料之後，EAPHost 對 EAP 對等方法的下一個呼叫會失敗，並出現 <strong>ERROR_OBJECT_DISCONNECTED</strong>。 為什麼會發生這種情況，以及如何解決此問題？</td>
<td>雖然 EAPHost 用戶端 Api 都是 C 樣式 Api，但這些 C Api 只是對應 COM Api 的包裝函式。 C 樣式 Api 會在多執行緒 COM 環境中執行。 UI 程式碼通常會在單元執行緒模型中執行。 因為這兩個執行緒模型彼此衝突，所以請勿在處理 EAP 驗證的相同執行緒中執行 UI 程式碼。</td>
</tr>
<tr class="even">
<td>為什麼 [<strong>EapHostPeerBeginSession</strong>] (/PREVIOUS-VERSIONS/WINDOWS/DESKTOP/API/EAPPAPIS/NF-EAPPAPIS-EAPHOSTPEERBEGINSESSION) api 採用 [<em>NotificationHandler</em>] (/previous-versions/windows/desktop/api) 回呼函式指標做為參數？</td>
<td>[<em>NotificationHandler</em>] (/previous-versions/windows/desktop/api) 是一種機制，要求者會收到其必須重新驗證的機制。 在許多情況下，要求者必須重新進行驗證，包括使用 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) 進行驗證。</td>
</tr>
<tr class="odd">
<td>在 [<strong>EapHostPeerBeginSession</strong>] (/PREVIOUS-VERSIONS/WINDOWS/DESKTOP/API/EAPPAPIS/NF-EAPPAPIS-EAPHOSTPEERBEGINSESSION) api 中， <em>pConnectionId</em>參數的用途為何？</td>
<td><em>pConnectionId</em> 是要求者定義的 GUID 值的指標，用來識別屬於要求者的網路連接。 呼叫 [<em>NotificationHandler</em>] (/previous-versions/windows/desktop/api) 回呼函式時，會傳遞此 GUID 來識別要求者將用來重新驗證要求的網路連接。</td>
</tr>
<tr class="even">
<td>如何? 知道隔離狀態是否有變更？</td>
<td>只有當至少有一個網路存取保護 (NAP) 隔離強制用戶端 (QEC 系統中) 註冊的介面時，使用者才會收到隔離狀態變更的視覺通知。 如果是，則在嘗試重新驗證時，使用者將會透過快顯視窗收到隔離狀態變更的通知。</td>
</tr>
<tr class="odd">
<td>如何? 知道系統中是否有 NAP QEC 註冊介面？</td>
<td>開啟提升許可權的視窗，然後執行下列 netsh 命令： &quot; netsh nap client show state &quot; 。 如需詳細資訊，請參閱 [Netsh 命令](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10))。</td>
</tr>
<tr class="even">
<td>如果要求者重新驗證，QEC 在重新驗證期間應使用何種連接識別碼？</td>
<td>QEC 應該使用先前會話所用的相同連接識別碼。</td>
</tr>
<tr class="odd">
<td>只有一個 EAPHost 要求者方法可用來顯示 (UI) 對話方塊的使用者介面，但 EAP 方法有數種類型的 UI 特定呼叫。 當要求者取得 <strong>EapHostPeerResponseInvokeUI</strong> 動作程式碼時，應呼叫何種方法，指出要求者必須顯示 UI 對話方塊？</td>
<td>使用者不需要採取任何動作，因為 EAPHost 知道要呼叫哪一個方法函數。 例如，傳回動作程式碼 <strong>EapHostPeerResponseInvokeUI</strong> 時，要求者會以下列順序呼叫這三個函式： [<strong>EapHostPeerGetUICoNtext</strong>] (/Previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicoNtext) 、[<strong>EapHostPeerInvokeInteractiveUI</strong>] (/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) 和 [<strong>EapHostPeerSetUICoNtext</strong>] (/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicoNtext) 。</td>
</tr>
<tr class="even">
<td>認證 BLOB 與設定 BLOB 之間有何差異？</td>
<td>認證 BLOB 只包含使用者資料，例如使用者名稱、密碼和 PIN。 設定 BLOB 包含控制方法行為的設定。</td>
</tr>
<tr class="odd">
<td>是否可以在 EAPHost 用戶端上啟用追蹤？</td>
<td>是。 如需詳細資訊，請參閱 [啟用追蹤](enabling-tracing.md)。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 要求者 API 參考](eap-host-supplicant-api-reference.md)
</dt> <dt>

[EAPHost 一般常見問題](general-frequently-asked-questions.md)
</dt> <dt>

[EAPHost 方法常見問題](eap-method-frequently-asked-questions.md)
</dt> <dt>

[EAPHost 開發常見問題](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

