---
title: EAP 方法的常見問題
description: 提供關於 EAP 方法撰寫的常見程式設計問題的解答。
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "106968121"
---
# <a name="eap-method-frequently-asked-questions"></a>EAP 方法的常見問題

本主題提供關於 EAP 方法撰寫的常見程式設計問題的解答。

## <a name="eap-method-frequently-asked-questions"></a>EAP 方法的常見問題



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
<td>什麼是設定 &quot; 資料 &quot; ？</td>
<td>設定 &quot; 資料 &quot; 和 &quot; 連接資料的詞彙 &quot; 為同義。</td>
</tr>
<tr class="even">
<td>什麼是 &quot; 連接資料 &quot; ？</td>
<td>&quot;連接資料 &quot; 是 EAP 方法特定的不透明 BLOB，其中包含方法的設定資訊。 此連接資料是在一開始設定時由方法所建立，且絕對不會由任何其他元件（而非 EAP 方法本身）進行解讀或修改。</td>
</tr>
<tr class="odd">
<td>什麼是 &quot; 認證 &quot; ？</td>
<td>&quot;認證 &quot; 和 &quot; 使用者資料的意義 &quot; 是同義。</td>
</tr>
<tr class="even">
<td>什麼是 &quot; 使用者資料 &quot; ？</td>
<td>&quot;使用者資料 &quot; 是 EAP 方法特定的不透明 BLOB，其中包含使用者認證資料，例如使用者名稱和密碼。 使用者資料絕對不會由任何其他元件解讀或修改，而非 EAP 方法本身。 &quot;使用者資料 &quot; 和認證的 &quot; 詞彙 &quot; 是同義的。</td>
</tr>
<tr class="odd">
<td>什麼是 &quot; EAP 屬性 &quot; ？</td>
<td>&quot;EAP 屬性 &quot; 是一種資料結構，其中包含預先決定的資料類型。 屬性是用來在 EAP 方法和要求者之間，或在 EAP 方法和驗證器之間傳達資訊。 EAP 方法的對等和驗證器執行可能會透過網路交換這些屬性。</td>
</tr>
<tr class="even">
<td>設定 API 和執行時間 API 是否會出現在相同的方法 DLL 中？</td>
<td>是。 設定 EAP 方法本身的登錄專案時，請務必指定差異。 設定路徑和對等路徑必須相同。</td>
</tr>
<tr class="odd">
<td>設定 API 和執行時間 API 是否會顯示在不同的方法 Dll 中？</td>
<td>是。 設定 EAP 方法本身的登錄專案時，請務必指定差異。 設定和對等路徑必須指向正確的 Dll。</td>
</tr>
<tr class="even">
<td>如何? 安裝 EAP 方法？</td>
<td>若要安裝 EAP 方法，您必須先在 EAP 方法 DLL 本身中，執行 [<strong>DllRegisterServer</strong>] (/windows/win32/api/olectl/nf-olectl-dllregisterserver) 和 [<strong>DllUnregisterServer</strong>] (/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 。 之後，請使用 <strong>regsvr32.exe</strong> 來安裝和卸載方法。 您也必須設定適當的登錄機碼。 如需詳細資訊，請參閱 [安裝 EAP 方法](installing-an-eap-method.md)。<br/></td>
</tr>
<tr class="odd">
<td>什麼是頻內 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) 支援？</td>
<td>啟用頻內 NAP 支援時，會在 EAP 方法封包內傳輸 NAP 封包。 相反地，當啟用頻外 NAP 支援時，健康情況的 NAP [聲明](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange 會透過 eap 方法封包內部以外的方式進行，而 nap 產生的憑證則用於 eap 方法驗證。</td>
</tr>
<tr class="even">
<td>我可以為我的 EAP 方法啟用頻內 NAP 支援嗎？</td>
<td>是的，您可以啟用 EAP 方法的頻內 NAP 支援。 如需詳細資訊，請參閱 [啟用 EAP 方法的 In-Band NAP 支援](enabling-in-band-nap-support.md)。</td>
</tr>
<tr class="odd">
<td>EAP 如何透過安全通道進行彈性驗證 (EAP-FAST) 運作？</td>
<td>EAP 快速案例的運作方式如下。 <br/>
<ul>
<li>方法會在採用方法 UI 的單一登入 (SSO) 處理密碼變更。</li>
<li>方法會傳回 [<strong>eatCredentialsChanged</strong>] (/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type) 屬性。</li>
<li>要求者向使用者指出認證已變更，並要求使用者重新輸入認證。</li>
<li>要求者重新輸入使用者認證，然後將這些認證傳送給方法。</li>
</ul>
如需有關 EAP-FAST 的詳細資訊，請參閱透過 [安全通道的 Eap 彈性驗證](https://go.microsoft.com/fwlink/p/?linkid=84010) (eap-fast) 。</td>
</tr>
<tr class="even">
<td>什麼是預先共用金鑰 (PSK) ？</td>
<td>傳送和接收數位信號的方法，在此方法中，傳輸信號的階段會因傳達資訊而有所不同。 [<strong>EAPConfigInputPSK</strong>] (/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type) 輸入欄位包含使用者的 EAP 快速 PSK。</td>
</tr>
<tr class="odd">
<td>什麼是 WOW，以及它對 EAPHost 有何影響？</td>
<td>Microsoft Windows-32-位在 Windows-64 位 (WOW) 是支援32位 x86 平臺應用程式之64位 Windows 中的作業系統元件。 通常，EAP 方法作者會定義某種形式的 C/c + + 結構，以封裝設定資料、認證資料和互動式 UI 資料。 為了避免在 WOW 和其他案例中發生不相容的情況，請務必確保資料結構在不同處理器架構中的對齊方式， (32 位和64位處理器) 。 通常會使用虛擬填補來對齊欄位，讓32和64位處理器上的設定、認證和互動式 UI 資料都相同。</td>
</tr>
<tr class="even">
<td>什麼是 &quot; 動作碼 &quot; ？這些動作碼會傳回哪些條件？</td>
<td>&quot;動作程式碼 &quot; 允許方法控制驗證流程，而且是狀態機器的整數。 它們是 EAP 方法所傳回的值，表示 EAPHost 應採取的下一個動作。 例如，動作程式碼可能表示 EAPHost EAP 方法有封包可以進行傳輸。 由 EAP 方法所傳回的所有動作程式碼所遵守的要求者，但永遠不會發出動作碼。如需詳細資訊，請參閱 [EAP 對等要求者動作代碼](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)。<br/></td>
</tr>
<tr class="odd">
<td>方法何時會傳回 [<strong>EapPeerMethodResponseActionDiscard</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</td>
<td>[<strong>EapPeerMethodResponseActionDiscard</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 由 EAP 方法傳回，表示 EAPHost 必須捨棄提供給方法的封包。 具體而言，方法已判定封包無效。 EAPHost 接著會等待下一個套件。</td>
</tr>
<tr class="even">
<td>方法何時會傳回 [<strong>EapPeerMethodResponseActionSend</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</td>
<td>[<strong>EapPeerMethodResponseActionSend</strong>] EAP 方法會傳回 [] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，表示 EAPHost EAPHost 所接收的下一個封包必須傳送至網路存取伺服器 (NAS) 。</td>
</tr>
<tr class="odd">
<td>方法何時會傳回 [<strong>EapPeerMethodResponseActionResult</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</td>
<td>[<strong>EapPeerMethodResponseActionResult</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 由 EAP 方法傳回，以向 EAPHost 指出驗證會話已結束，且該會話的結果可供使用。</td>
</tr>
<tr class="even">
<td>方法何時會傳回 [<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</td>
<td>[<strong>EapPeerMethodResponseActionInvokeUI</strong>] EAP 方法會傳回 [] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，表示 EAPHost 需要使用者輸入才能繼續進行驗證，而且必須顯示使用者介面對話方塊才能取得該輸入。 一旦取得使用者輸入資料之後，EAPHost 就可以使用更新的 UI 內容資料，再次呼叫 EAP 方法。</td>
</tr>
<tr class="odd">
<td>方法何時會傳回 [<strong>EapPeerMethodResponseActionRespond</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</td>
<td>[<strong>EapPeerMethodResponseActionRespond</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) 由 eap 方法傳回，表示 EAPHost eap 方法具有可供 EAPHost 在驗證期間使用的屬性。 EAPHost 藉由呼叫 [<strong>EapPeerGetResponseAttributes</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 方法取得屬性，然後再呼叫 [<strong>EapPeerSetResponseAttributes</strong>] (/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) 方法。</td>
</tr>
<tr class="even">
<td>方法何時會傳回 [<strong>EapPeerMethodResponseActionNone</strong>] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，而此動作程式碼代表 EAPHost 的意義為何？</td>
<td>[<strong>EapPeerMethodResponseActionNone</strong>] EAP 方法會傳回 [] (/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) ，表示 EAPHost 目前不需要採取任何動作。</td>
</tr>
<tr class="odd">
<td>是否可以在驗證器端啟用追蹤？</td>
<td>是。 如需詳細資訊，請參閱 [啟用追蹤](enabling-tracing.md)。</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 對等方法 API 參考](eap-host-peer-method-api-reference.md)
</dt> <dt>

[EAPHost 一般常見問題](general-frequently-asked-questions.md)
</dt> <dt>

[EAPHost 要求者常見問題](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[EAPHost 開發常見問題](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 

