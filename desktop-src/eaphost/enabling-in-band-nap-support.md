---
title: 為 EAP 方法執行 In-Band NAP 支援
description: 可以針對支援將類型長度值物件傳輸 (TLVs) 的 EAPHost EAP 方法啟用。
ms.assetid: 298c89d9-7a6a-4280-9af9-77c7c00cab92
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9eae9fc17e99b27f620fbab1ed42cbd4b73800
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684186"
---
# <a name="implementing-in-band-nap-support-for-eap-methods"></a><span data-ttu-id="3fe0f-103">為 EAP 方法執行 In-Band NAP 支援</span><span class="sxs-lookup"><span data-stu-id="3fe0f-103">Implementing In-Band NAP Support for EAP Methods</span></span>

<span data-ttu-id="3fe0f-104">[網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) (NAP) 對於 eap 方法的支援，可以啟用 EAPHost eap 方法，以支援 (TLVs) 的型別長度值物件傳輸。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-104">In-band [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) support for an EAP method can be enabled for EAPHost EAP methods that support the transmission of type-length-value objects (TLVs).</span></span> <span data-ttu-id="3fe0f-105">啟用頻內 NAP 支援時，會在 EAP 方法封包內傳輸 NAP 封包。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-105">When in-band NAP support is enabled, NAP packets are transported inside EAP method packets.</span></span>

<span data-ttu-id="3fe0f-106">相反地，當啟用頻外 NAP 支援時，健康情況的 NAP [聲明](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange 會透過 EAP 方法封包內部以外的方式進行。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-106">In contrast, when out-of-band NAP support is enabled, the NAP [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) exchange occurs through means other than internal to EAP method packets.</span></span>

<span data-ttu-id="3fe0f-107">所有 TLVs 都是廠商專屬的。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-107">All TLVs are vendor specific.</span></span>

## <a name="implementing-nap-support-on-eap-peer-methods"></a><span data-ttu-id="3fe0f-108">在 EAP 對等方法上執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="3fe0f-108">Implementing NAP Support on EAP Peer Methods</span></span>

<span data-ttu-id="3fe0f-109">EAP 對等方法會收到包含 [健康狀態聲明](https://go.microsoft.com/fwlink/p/?linkid=83917) 的 TLV (SoH) 從 EAP 伺服器要求 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-109">The EAP peer method implementation receives a TLV containing the [Statement of Health](https://go.microsoft.com/fwlink/p/?linkid=83917) (SoH) request TLV from an EAP server.</span></span>

<span data-ttu-id="3fe0f-110">EAP 對等方法的執行接著會將包含 SoH 要求 TLV 的 TLV 傳遞給 EAPHost，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-110">The EAP peer method implementation then passes the TLV containing the SoH request TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="3fe0f-111">EAP 對等方法執行會在從 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)傳回時，將動作程式碼 [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction)傳回 EAPHost。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-111">The EAP peer method implementation returns the action code [**EapPeerMethodResponseActionRespond**](/windows/win32/api/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="3fe0f-112">從 EAP 對等方法執行 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 的 EAPHost 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-112">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="3fe0f-113">這些屬性會在進程中傳遞。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-113">The attributes are passed in the process.</span></span>
-   <span data-ttu-id="3fe0f-114">EAP 對等方法執行會傳回包含 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)中 SOH 要求 TLV 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-114">The EAP peer method implementation returns the TLV containing the SoH request TLV in [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes).</span></span> <span data-ttu-id="3fe0f-115">這些屬性會在進程中收到。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-115">The attributes are received in the process.</span></span>

<span data-ttu-id="3fe0f-116">EAP 對等方法執行會從 EAPHost 接收包含 SoH TLV 的 TLV，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-116">The EAP peer method implementation receives a TLV containing an SoH TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="3fe0f-117">從 EAP 對等方法執行 [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) 的 EAPHost 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-117">EAPHost calls [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes) from the EAP peer method implementation.</span></span> <span data-ttu-id="3fe0f-118">**EapPeerSetResponseAttributes** 包含承載 SoH TLV 的 tlv。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-118">**EapPeerSetResponseAttributes** contains a TLV that houses an SoH TLV.</span></span>
-   <span data-ttu-id="3fe0f-119">EAP 對等方法執行會將 SoH TLV 傳送至 EAP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-119">The EAP peer method implementation sends the SoH TLV to the EAP server.</span></span>
-   <span data-ttu-id="3fe0f-120">EAP 對等方法的執行會接收包含來自 EAP 伺服器之 SoH 回應 TLV 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-120">The EAP peer method implementation receives a TLV containing an SoH response TLV from the EAP server.</span></span>

<span data-ttu-id="3fe0f-121">EAP 對等方法執行會將包含 SoH 回應 TLV 的 TLV 傳遞給 EAPHost，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-121">The EAP peer method implementation passes the TLV containing the SoH response TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="3fe0f-122">EAP 對等方法執行會在從 [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)傳回時，將動作程式碼 **EapPeerMethodResponseActionRespond** 傳回 EAPHost。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-122">The EAP peer method implementation returns the action code **EapPeerMethodResponseActionRespond** to EAPHost on return from [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket).</span></span>
-   <span data-ttu-id="3fe0f-123">從 EAP 對等方法的 EAPHost 呼叫 [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) 。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-123">EAPHost calls [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes) from the EAP peer method implementations.</span></span> <span data-ttu-id="3fe0f-124">[**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)結構會在進程中傳遞。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-124">The [**EAP\_ATTRIBUTES**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes) structure is passed in the process.</span></span>
-   <span data-ttu-id="3fe0f-125">EAP 對等方法執行會傳回包含 [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)中 SOH 回應 TLV 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-125">The EAP peer method implementation returns the TLV containing the SoH response TLV in [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes).</span></span>

> [!Note]  
> <span data-ttu-id="3fe0f-126">[**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)結構的 **eapType** 成員一律會設定為 **eatEAPTLV** ，而 **pValue** 成員將指向包含 SoH 回應 tlv 的 TLV 的第一個位元組。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-126">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="implementing-nap-support-on-eap-server-methods"></a><span data-ttu-id="3fe0f-127">在 EAP 伺服器方法上執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="3fe0f-127">Implementing NAP Support on EAP Server Methods</span></span>

<span data-ttu-id="3fe0f-128">EAP 伺服器方法執行會建立包含 SoH 要求 TLV 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-128">The EAP server method implementation constructs a TLV containing an SoH request TLV.</span></span> <span data-ttu-id="3fe0f-129">EAP 伺服器方法執行會將包含 SoH 要求 TLV 的此 TLV 傳送給 EAP 對等。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-129">The EAP server method implementation sends this TLV containing the SoH Request TLV to the EAP peer.</span></span> <span data-ttu-id="3fe0f-130">EAP 伺服器方法執行會接收來自 EAP 對等的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-130">The EAP server method implementation receives the TLV from the EAP peer.</span></span>

<span data-ttu-id="3fe0f-131">EAP 伺服器方法執行會將包含 SoH TLV 的 TLV 傳遞給 EAPHost，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-131">The EAP server method implementation passes the TLV containing an SoH TLV to EAPHost as follows.</span></span>

-   <span data-ttu-id="3fe0f-132">EAP 伺服器方法執行會傳回動作程式碼， **eap \_ 方法驗證器 \_ 回應 \_ \_** 會在從 [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket)傳回時回應 EAPHost。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-132">The EAP server method implementation returns the action code **EAP\_METHOD\_AUTHENTICATOR\_RESPONSE\_RESPOND** to EAPHost on return from [**EapMethodAuthenticatorReceivePacket**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorreceivepacket).</span></span>
-   <span data-ttu-id="3fe0f-133">從 EAP 伺服器方法執行 [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) 的 EAPHost 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-133">EAPHost calls [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="3fe0f-134">EAP 伺服器方法執行會傳回包含 [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes)中 SoH TLV 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-134">The EAP server method implementation returns the TLV containing the SoH TLV in [**EapMethodAuthenticatorGetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorgetattributes).</span></span>

<span data-ttu-id="3fe0f-135">EAP 伺服器方法執行會從 EAPHost 接收包含 SoH 回應 TLV 的 TLV，如下所示。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-135">The EAP server method implementation receives a TLV containing an SoH response TLV from EAPHost as follows.</span></span>

-   <span data-ttu-id="3fe0f-136">從 EAP 伺服器方法執行 [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) 的 EAPHost 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-136">EAPHost calls [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes) from the EAP server method implementation.</span></span>
-   <span data-ttu-id="3fe0f-137">包含 SoH 回應 TLV 的 TLV 會在 EapMethodAuthenticatorSetAttributes 中傳回。 [ ](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span><span class="sxs-lookup"><span data-stu-id="3fe0f-137">The TLV containing the SoH response TLV is returned in [**EapMethodAuthenticatorSetAttributes**](/previous-versions/windows/desktop/api/eapmethodauthenticatorapis/nf-eapmethodauthenticatorapis-eapmethodauthenticatorsetattributes)</span></span>
-   <span data-ttu-id="3fe0f-138">EAP 伺服器方法執行會傳送包含 SoH 回應 TLV 的 TLV。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-138">The EAP server method implementation sends the TLV containing the SoH response TLV.</span></span>

> [!Note]  
> <span data-ttu-id="3fe0f-139">[**EAP \_ 屬性**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)結構的 **eapType** 成員一律會設定為 **eatEAPTLV** ，而 **pValue** 成員將指向包含 SoH 回應 tlv 的 TLV 的第一個位元組。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-139">The **eapType** member of the [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure will always be set to **eatEAPTLV** and the **pValue** member will point to the first byte of the TLV that contains the SoH response TLV.</span></span>

 

### <a name="messages"></a><span data-ttu-id="3fe0f-140">訊息</span><span class="sxs-lookup"><span data-stu-id="3fe0f-140">Messages</span></span>

<span data-ttu-id="3fe0f-141">EAP SoH TLV 用來封裝 SoH 通訊協定，以便透過 EAP 方法進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-141">The EAP SoH TLV is used to encapsulate the SoH protocol for transmission via an EAP method.</span></span> <span data-ttu-id="3fe0f-142">所有 EAP SoH TLVs 都有相同的結構，但不同于訊息的訊息識別碼和資料部分。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-142">All EAP SoH TLVs have the same structure, differing only on the message ID and data portion of the message.</span></span>

<span data-ttu-id="3fe0f-143">如需詳細資訊，請參閱「 [網路存取保護」 (NAP) 健康狀態聲明 (SoH) 訊息](https://go.microsoft.com/fwlink/p/?linkid=83918)。</span><span class="sxs-lookup"><span data-stu-id="3fe0f-143">For more information, see [Network Access Protection (NAP) Statement of Health (SoH) Messages](https://go.microsoft.com/fwlink/p/?linkid=83918).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe0f-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fe0f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe0f-145">設定 EAP 方法消費者介面</span><span class="sxs-lookup"><span data-stu-id="3fe0f-145">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="3fe0f-146">啟用群組原則</span><span class="sxs-lookup"><span data-stu-id="3fe0f-146">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="3fe0f-147">為 EAP 方法執行 NAP 支援</span><span class="sxs-lookup"><span data-stu-id="3fe0f-147">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="3fe0f-148">在要求者和 EAP 方法之間傳送資料</span><span class="sxs-lookup"><span data-stu-id="3fe0f-148">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="3fe0f-149">EAPHost 要求者</span><span class="sxs-lookup"><span data-stu-id="3fe0f-149">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 