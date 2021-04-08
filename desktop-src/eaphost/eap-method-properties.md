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
# <a name="eap-method-properties"></a><span data-ttu-id="eafc5-104">EAP 方法屬性</span><span class="sxs-lookup"><span data-stu-id="eafc5-104">EAP Method Properties</span></span>

<span data-ttu-id="eafc5-105">由要求者和驗證器用來判斷要搭配指定要求者或驗證器使用的 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="eafc5-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="eafc5-106">方法屬性也會指定方法的設定。</span><span class="sxs-lookup"><span data-stu-id="eafc5-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="eafc5-107">例如， [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 要求者可能需要有一些方法，才能搭配 [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) 要求者使用特定屬性。</span><span class="sxs-lookup"><span data-stu-id="eafc5-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="eafc5-108">例如，金鑰資料是一項需求。</span><span class="sxs-lookup"><span data-stu-id="eafc5-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="eafc5-109">系統會列出 EAP 方法所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="eafc5-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="eafc5-110">屬性會儲存為登錄機碼值。</span><span class="sxs-lookup"><span data-stu-id="eafc5-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="eafc5-111">如需詳細資訊，請參閱[Eap 方法](registry-keys-for-eap-methods.md)的登錄設定主題中的 Eap 對等方法 DLL 登錄機碼一節。</span><span class="sxs-lookup"><span data-stu-id="eafc5-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="eafc5-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span><span class="sxs-lookup"><span data-stu-id="eafc5-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="eafc5-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-114">方法可讓加密套件基於資料加密目的進行協商。</span><span class="sxs-lookup"><span data-stu-id="eafc5-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="eafc5-115">Windows Server 2008 支援下列 3DES [加密套件](/windows/desktop/SecAuthN/tls-cipher-suites)：</span><span class="sxs-lookup"><span data-stu-id="eafc5-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="eafc5-116">TLS \_ RSA \_ 與 \_ 3des \_ EDE \_ CBC \_ SHA (tls & SSL 3) </span><span class="sxs-lookup"><span data-stu-id="eafc5-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="eafc5-117">\_ \_ \_ 具有 \_ 3des \_ EDE \_ CBC \_ SHA (tls & SSL 3) 的 tls DHE DSS</span><span class="sxs-lookup"><span data-stu-id="eafc5-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="eafc5-118">\_ \_ \_ \_ \_ \_ 使用 MD5 (ssl 2 的 ssl CK DES 192 EDE3 CBC （ \_ 若已啟用）) </span><span class="sxs-lookup"><span data-stu-id="eafc5-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="eafc5-119">如需 TLS 1.0 安全性通訊協定的詳細資訊，請參閱 [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035)。</span><span class="sxs-lookup"><span data-stu-id="eafc5-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span><span class="sxs-lookup"><span data-stu-id="eafc5-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="eafc5-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-122">方法會提供交換，而驗證器會驗證對等，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="eafc5-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span><span class="sxs-lookup"><span data-stu-id="eafc5-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="eafc5-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-125">方法會提供資料來源驗證和保護，以防止未經授權修改 EAP 封包的資訊，包括 EAP 要求和回應。</span><span class="sxs-lookup"><span data-stu-id="eafc5-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="eafc5-126">進行此宣告時，方法規格必須指定 EAP 封包內受保護的 EAP 封包和受保護的欄位。</span><span class="sxs-lookup"><span data-stu-id="eafc5-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span><span class="sxs-lookup"><span data-stu-id="eafc5-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="eafc5-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-129">方法可以防止 EAP 方法或其訊息的重新執行。</span><span class="sxs-lookup"><span data-stu-id="eafc5-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="eafc5-130">無法重新執行成功和失敗的結果指示。</span><span class="sxs-lookup"><span data-stu-id="eafc5-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span><span class="sxs-lookup"><span data-stu-id="eafc5-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafc5-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-133">方法可以加密 EAP 訊息。</span><span class="sxs-lookup"><span data-stu-id="eafc5-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="eafc5-134">EAP 要求、EAP 回應、成功結果指示和失敗結果指示都會加密。</span><span class="sxs-lookup"><span data-stu-id="eafc5-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="eafc5-135">提出此宣告的方法必須支援 identity protection。</span><span class="sxs-lookup"><span data-stu-id="eafc5-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span><span class="sxs-lookup"><span data-stu-id="eafc5-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="eafc5-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-138">方法可以衍生可匯出的金鑰內容，例如 (MSK) 的主要工作階段金鑰，以及 (EMSK) 的擴充主要工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="eafc5-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="eafc5-139">MSK 只用于進一步的金鑰衍生，而不是直接用來保護 EAP 交談或後續的資料。</span><span class="sxs-lookup"><span data-stu-id="eafc5-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="eafc5-140">EMSK 的使用是保留的。</span><span class="sxs-lookup"><span data-stu-id="eafc5-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="eafc5-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="eafc5-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-143">EAP 方法所支援的最小金鑰長度是64位。</span><span class="sxs-lookup"><span data-stu-id="eafc5-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="eafc5-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="eafc5-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-146">EAP 方法所支援的最小金鑰長度是128位。</span><span class="sxs-lookup"><span data-stu-id="eafc5-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="eafc5-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="eafc5-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-149">EAP 方法所支援的最小金鑰長度是256位。</span><span class="sxs-lookup"><span data-stu-id="eafc5-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="eafc5-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="eafc5-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-152">EAP 方法所支援的最小金鑰長度是512位。</span><span class="sxs-lookup"><span data-stu-id="eafc5-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="eafc5-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="eafc5-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-155">EAP 方法所支援的最小金鑰長度是1024位。</span><span class="sxs-lookup"><span data-stu-id="eafc5-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span><span class="sxs-lookup"><span data-stu-id="eafc5-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="eafc5-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-158">此方法不允許根據攻擊者字典中的密碼數目來進行工作因素的離線攻擊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="eafc5-159">使用密碼驗證時，通常會從較小的一組 (選取密碼，相較于一組 N 位金鑰) ，這會引發字典攻擊的相關問題。</span><span class="sxs-lookup"><span data-stu-id="eafc5-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="eafc5-160">您可以使用方法來提供保護，以防止字典攻擊，如果它使用密碼做為秘密時，方法就不允許根據攻擊者字典中的密碼數目來進行工作因素的離線攻擊。</span><span class="sxs-lookup"><span data-stu-id="eafc5-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span><span class="sxs-lookup"><span data-stu-id="eafc5-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="eafc5-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-163">在先前已建立安全性關聯的情況下，方法可以更有效率地建立新的或重新整理的安全性關聯，或以較少的往返次數來建立新的或重新整理的安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="eafc5-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="eafc5-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="eafc5-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-166">方法會向 EAP 伺服器示範，單一實體已作為通道方法內執行之所有方法的 EAP 對等。</span><span class="sxs-lookup"><span data-stu-id="eafc5-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="eafc5-167">系結也可能代表 EAP 伺服器向對等端示範了單一實體已作為通道方法內執行之所有方法的 EAP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="eafc5-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="eafc5-168">如果正確執行，系結可減輕攔截式弱點。</span><span class="sxs-lookup"><span data-stu-id="eafc5-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span><span class="sxs-lookup"><span data-stu-id="eafc5-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="eafc5-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-171">此方法會示範被動式攻擊 (例如捕捉 EAP 對話) 或主動攻擊 (包括入侵 MSK 或 EMSK) 不會危害後續或先前的 MSKs 或 EMSKs。</span><span class="sxs-lookup"><span data-stu-id="eafc5-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span><span class="sxs-lookup"><span data-stu-id="eafc5-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="eafc5-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-174">如果 EAP 封包超過最小 MTU (最大傳輸單位) 1020 個八位，則此方法可支援片段和重組。</span><span class="sxs-lookup"><span data-stu-id="eafc5-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="eafc5-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="eafc5-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-177">方法可以傳達受完整性保護的通道屬性，例如端點識別碼，而這些屬性可以與使用頻外機制（例如 [驗證、授權及帳戶](https://go.microsoft.com/fwlink/p/?linkid=84063) 處理 (AAA) 或較低層的通訊協定）進行通訊的值進行比較。</span><span class="sxs-lookup"><span data-stu-id="eafc5-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span><span class="sxs-lookup"><span data-stu-id="eafc5-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="eafc5-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="eafc5-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-180">此方法支援 (NAP) 的網路存取保護。</span><span class="sxs-lookup"><span data-stu-id="eafc5-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span><span class="sxs-lookup"><span data-stu-id="eafc5-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="eafc5-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-183">方法可以在獨立電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="eafc5-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span><span class="sxs-lookup"><span data-stu-id="eafc5-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="eafc5-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="eafc5-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-186">方法支援 [ (MPPE) 通訊協定加密的 Microsoft 點對點加密](https://go.microsoft.com/fwlink/p/?linkid=83915) 。</span><span class="sxs-lookup"><span data-stu-id="eafc5-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span><span class="sxs-lookup"><span data-stu-id="eafc5-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="eafc5-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-189">方法支援其他 EAP 方法的通道。</span><span class="sxs-lookup"><span data-stu-id="eafc5-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span><span class="sxs-lookup"><span data-stu-id="eafc5-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="eafc5-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-192">方法支援可設定的屬性，而且具有使用者介面。</span><span class="sxs-lookup"><span data-stu-id="eafc5-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span><span class="sxs-lookup"><span data-stu-id="eafc5-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="eafc5-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-195">此方法是由 EAP 認證計畫認證。</span><span class="sxs-lookup"><span data-stu-id="eafc5-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="eafc5-196">此位應只由已通過認證的 EAP 方法傳送。</span><span class="sxs-lookup"><span data-stu-id="eafc5-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span><span class="sxs-lookup"><span data-stu-id="eafc5-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="eafc5-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-199">Windows 7 或更新版本：方法可用來使用電腦認證來驗證網路上的電腦。</span><span class="sxs-lookup"><span data-stu-id="eafc5-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span><span class="sxs-lookup"><span data-stu-id="eafc5-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="eafc5-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-202">Windows 7 或更新版本：方法可以用來利用使用者認證，對網路上的使用者進行驗證。</span><span class="sxs-lookup"><span data-stu-id="eafc5-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="eafc5-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="eafc5-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-205">Windows 7 或更新版本：方法支援在受保護的通道中傳送使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="eafc5-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span><span class="sxs-lookup"><span data-stu-id="eafc5-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="eafc5-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-208">Windows 7 或更新版本：方法是 tunnelled 方法，並且支援通道內的 EAP 方法連結。</span><span class="sxs-lookup"><span data-stu-id="eafc5-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span><span class="sxs-lookup"><span data-stu-id="eafc5-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="eafc5-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-211">Windows 7 或更新版本：方法支援 [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455)中定義的共用狀態等價。</span><span class="sxs-lookup"><span data-stu-id="eafc5-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="eafc5-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span><span class="sxs-lookup"><span data-stu-id="eafc5-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eafc5-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="eafc5-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="eafc5-214">保留的。</span><span class="sxs-lookup"><span data-stu-id="eafc5-214">Reserved.</span></span> <span data-ttu-id="eafc5-215">未使用。</span><span class="sxs-lookup"><span data-stu-id="eafc5-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eafc5-216">規格需求</span><span class="sxs-lookup"><span data-stu-id="eafc5-216">Requirements</span></span>



| <span data-ttu-id="eafc5-217">需求</span><span class="sxs-lookup"><span data-stu-id="eafc5-217">Requirement</span></span> | <span data-ttu-id="eafc5-218">值</span><span class="sxs-lookup"><span data-stu-id="eafc5-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eafc5-219">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eafc5-219">Minimum supported client</span></span><br/> | <span data-ttu-id="eafc5-220">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eafc5-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eafc5-221">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eafc5-221">Minimum supported server</span></span><br/> | <span data-ttu-id="eafc5-222">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eafc5-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eafc5-223">標頭</span><span class="sxs-lookup"><span data-stu-id="eafc5-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="eafc5-224"><dt>Eaptypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="eafc5-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eafc5-225">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eafc5-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eafc5-226">EAP 方法的登錄機碼</span><span class="sxs-lookup"><span data-stu-id="eafc5-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="eafc5-227">常見的 EAPHost 常數</span><span class="sxs-lookup"><span data-stu-id="eafc5-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

