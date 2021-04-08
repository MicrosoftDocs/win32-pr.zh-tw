---
title: 'EAP 方法屬性 (Eaptypes .h) '
description: 由要求者和驗證器用來判斷要搭配指定要求者或驗證器使用的 EAP 方法。 方法屬性也會指定方法的設定。
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685994"
---
# <a name="eap-method-properties"></a>EAP 方法屬性

由要求者和驗證器用來判斷要搭配指定要求者或驗證器使用的 EAP 方法。 方法屬性也會指定方法的設定。

例如， [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 要求者可能需要有一些方法，才能搭配 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 要求者使用特定屬性。 例如，金鑰資料是一項需求。

系統會列出 EAP 方法所支援的屬性。 屬性會儲存為登錄機碼值。 如需詳細資訊，請參閱[Eap 方法](registry-keys-for-eap-methods.md)的登錄設定主題中的 Eap 對等方法 DLL 登錄機碼一節。

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



方法可讓加密套件基於資料加密目的進行協商。 Windows Server 2008 支援下列 3DES [加密套件](/windows/desktop/SecAuthN/tls-cipher-suites)：

-   TLS \_ RSA \_ 與 \_ 3des \_ EDE \_ CBC \_ SHA (tls & SSL 3) 
-   \_ \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA (tls & SSL 3) 的 tls DHE DSS
-   \_ \_ \_ \_ \_ \_ 使用 MD5 (ssl 2 的 ssl CK DES 192 EDE3 CBC （ \_ 若已啟用）) 

如需 TLS 1.0 安全性通訊協定的詳細資訊，請參閱 [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035)。


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



方法會提供交換，而驗證器會驗證對等，反之亦然。


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



方法會提供資料來源驗證和保護，以防止未經授權修改 EAP 封包的資訊，包括 EAP 要求和回應。 進行此宣告時，方法規格必須指定 EAP 封包內受保護的 EAP 封包和受保護的欄位。


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



方法可以防止 EAP 方法或其訊息的重新執行。 無法重新執行成功和失敗的結果指示。


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



方法可以加密 EAP 訊息。 EAP 要求、EAP 回應、成功結果指示和失敗結果指示都會加密。 提出此宣告的方法必須支援 identity protection。


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



方法可以衍生可匯出的金鑰內容，例如 (MSK) 的主要工作階段金鑰，以及 (EMSK) 的擴充主要工作階段金鑰。 MSK 只用于進一步的金鑰衍生，而不是直接用來保護 EAP 交談或後續的資料。 EMSK 的使用是保留的。


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



EAP 方法所支援的最小金鑰長度是64位。


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



EAP 方法所支援的最小金鑰長度是128位。


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



EAP 方法所支援的最小金鑰長度是256位。


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



EAP 方法所支援的最小金鑰長度是512位。


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



EAP 方法所支援的最小金鑰長度是1024位。


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



此方法不允許根據攻擊者字典中的密碼數目來進行工作因素的離線攻擊。 使用密碼驗證時，通常會從較小的一組 (選取密碼，相較于一組 N 位金鑰) ，這會引發字典攻擊的相關問題。 您可以使用方法來提供保護，以防止字典攻擊，如果它使用密碼做為秘密時，方法就不允許根據攻擊者字典中的密碼數目來進行工作因素的離線攻擊。


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



在先前已建立安全性關聯的情況下，方法可以更有效率地建立新的或重新整理的安全性關聯，或以較少的往返次數來建立新的或重新整理的安全性關聯。


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



方法會向 EAP 伺服器示範，單一實體已作為通道方法內執行之所有方法的 EAP 對等。 系結也可能代表 EAP 伺服器向對等端示範了單一實體已作為通道方法內執行之所有方法的 EAP 伺服器。 如果正確執行，系結可減輕攔截式弱點。


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



此方法會示範被動式攻擊 (例如捕捉 EAP 對話) 或主動攻擊 (包括入侵 MSK 或 EMSK) 不會危害後續或先前的 MSKs 或 EMSKs。


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



如果 EAP 封包超過最小 MTU (最大傳輸單位) 1020 個八位，則此方法可支援片段和重組。


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



方法可以傳達受完整性保護的通道屬性，例如端點識別碼，而這些屬性可以與使用頻外機制（例如 [驗證、授權及帳戶](https://go.microsoft.com/fwlink/p/?linkid=84063) 處理 (AAA) 或較低層的通訊協定）進行通訊的值進行比較。


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



此方法支援 (NAP) 的網路存取保護。


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



方法可以在獨立電腦上使用。


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



方法支援 [ (MPPE) 通訊協定加密的 Microsoft 點對點加密](https://go.microsoft.com/fwlink/p/?linkid=83915) 。


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



方法支援其他 EAP 方法的通道。


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



方法支援可設定的屬性，而且具有使用者介面。


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



此方法是由 EAP 認證計畫認證。 此位應只由已通過認證的 EAP 方法傳送。


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 或更新版本：方法可用來使用電腦認證來驗證網路上的電腦。


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 或更新版本：方法可以用來利用使用者認證，對網路上的使用者進行驗證。


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 或更新版本：方法支援在受保護的通道中傳送使用者身分識別。


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 或更新版本：方法是 tunnelled 方法，並且支援通道內的 EAP 方法連結。


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 或更新版本：方法支援 [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455)中定義的共用狀態等價。


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



保留的。 未使用。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Eaptypes。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAP 方法的登錄機碼](registry-keys-for-eap-methods.md)
</dt> <dt>

[常見的 EAPHost 常數](common-eap-host-error-constants.md)
</dt> </dl>

