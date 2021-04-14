---
title: 驗證等級
description: 驗證層級會控制用戶端或伺服器希望其 SSP 有多少安全性。
ms.assetid: 0bad2bfd-6930-42fc-beb0-bce32440b0b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250661e4a8da42ffd91f37e282a39fbb52b6328a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311510"
---
# <a name="authentication-level"></a><span data-ttu-id="94281-103">驗證等級</span><span class="sxs-lookup"><span data-stu-id="94281-103">Authentication Level</span></span>

<span data-ttu-id="94281-104">驗證層級會控制用戶端或伺服器希望其 SSP 有多少安全性。</span><span class="sxs-lookup"><span data-stu-id="94281-104">The authentication level controls how much security a client or server wants from its SSP.</span></span> <span data-ttu-id="94281-105">驗證層級是透過 DwAuthnLevel 參數傳遞適當的 \_ RPC \_ C 驗證 \_ level \_ xxx 值給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)或 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) 所設定。</span><span class="sxs-lookup"><span data-stu-id="94281-105">The authentication level is set by passing an appropriate RPC\_C\_AUTHN\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwAuthnLevel* parameter.</span></span> <span data-ttu-id="94281-106">用戶端和伺服器的驗證層級會在交握期間進行比較，並使用較高層級的安全性保護設定來進行連接。</span><span class="sxs-lookup"><span data-stu-id="94281-106">The authentication levels from the client and server are compared during the handshake, and the higher level security protection setting is used for the connection.</span></span>

<span data-ttu-id="94281-107">不同的驗證等級如下所述，從最低層級安全性保護到最高：</span><span class="sxs-lookup"><span data-stu-id="94281-107">The different authentication levels are described as follows, from lowest level security protection to highest:</span></span>

<dl> <dt>

<span data-ttu-id="94281-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>無 (RPC \_ C \_ 驗證 \_ 層級 \_ 無) </span><span class="sxs-lookup"><span data-stu-id="94281-108"><span id="None__RPC_C_AUTHN_LEVEL_NONE_"></span><span id="none__rpc_c_authn_level_none_"></span><span id="NONE__RPC_C_AUTHN_LEVEL_NONE_"></span>None (RPC\_C\_AUTHN\_LEVEL\_NONE)</span></span>
</dt> <dd>

<span data-ttu-id="94281-109">在用戶端與伺服器之間進行通訊時，不會執行任何驗證。</span><span class="sxs-lookup"><span data-stu-id="94281-109">No authentication is performed during the communication between client and server.</span></span> <span data-ttu-id="94281-110">系統會忽略所有安全性設定。</span><span class="sxs-lookup"><span data-stu-id="94281-110">All security settings are ignored.</span></span> <span data-ttu-id="94281-111">只有在 [驗證服務層級](com-authentication-service-constants.md) 為 [RPC \_ C \_ 驗證無] 時，才可以設定此驗證等級 \_ 。</span><span class="sxs-lookup"><span data-stu-id="94281-111">This authentication level can be set only if the [authentication service level](com-authentication-service-constants.md) is RPC\_C\_AUTHN\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="94281-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>預設 (RPC \_ C \_ 驗證 \_ LEVEL \_ default) </span><span class="sxs-lookup"><span data-stu-id="94281-112"><span id="Default__RPC_C_AUTHN_LEVEL_DEFAULT_"></span><span id="default__rpc_c_authn_level_default_"></span><span id="DEFAULT__RPC_C_AUTHN_LEVEL_DEFAULT_"></span>Default (RPC\_C\_AUTHN\_LEVEL\_DEFAULT)</span></span>
</dt> <dd>

<span data-ttu-id="94281-113">COM 會使用其一般安全性整體協商來選擇驗證等級。</span><span class="sxs-lookup"><span data-stu-id="94281-113">COM chooses the authentication level by using its normal security blanket negotiation.</span></span> <span data-ttu-id="94281-114">它永遠不會選擇 [無] 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="94281-114">It will never choose an authentication level of None.</span></span>

</dd> <dt>

<span data-ttu-id="94281-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC \_ C \_ 驗證 \_ LEVEL \_ connect) </span><span class="sxs-lookup"><span data-stu-id="94281-115"><span id="Connect__RPC_C_AUTHN_LEVEL_CONNECT_"></span><span id="connect__rpc_c_authn_level_connect_"></span><span id="CONNECT__RPC_C_AUTHN_LEVEL_CONNECT_"></span>Connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT)</span></span>
</dt> <dd>

<span data-ttu-id="94281-116">一般驗證交握會在用戶端與伺服器之間進行，並建立工作階段金鑰，但永遠不會將該金鑰用於用戶端與伺服器之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="94281-116">The normal authentication handshake occurs between the client and server, and a session key is established but that key is never used for communication between the client and server.</span></span> <span data-ttu-id="94281-117">交握之後的所有通訊都不是安全的。</span><span class="sxs-lookup"><span data-stu-id="94281-117">All communication after the handshake is nonsecure.</span></span>

</dd> <dt>

<span data-ttu-id="94281-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>呼叫 (RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫) </span><span class="sxs-lookup"><span data-stu-id="94281-118"><span id="Call__RPC_C_AUTHN_LEVEL_CALL_"></span><span id="call__rpc_c_authn_level_call_"></span><span id="CALL__RPC_C_AUTHN_LEVEL_CALL_"></span>Call (RPC\_C\_AUTHN\_LEVEL\_CALL)</span></span>
</dt> <dd>

<span data-ttu-id="94281-119">只有每個呼叫開頭的標頭會經過簽署。</span><span class="sxs-lookup"><span data-stu-id="94281-119">Only the headers of the beginning of each call are signed.</span></span> <span data-ttu-id="94281-120">用戶端與伺服器之間交換的其餘資料都不會進行簽署或加密。</span><span class="sxs-lookup"><span data-stu-id="94281-120">The rest of the data exchanged between the client and server is neither signed nor encrypted.</span></span> <span data-ttu-id="94281-121">大部分的 Ssp 都不支援此驗證層級，並以無訊息方式將它升級為封包。</span><span class="sxs-lookup"><span data-stu-id="94281-121">Most SSPs do not support this authentication level and silently promote it to Packet.</span></span>

</dd> <dt>

<span data-ttu-id="94281-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>封包 (RPC \_ C \_ 驗證 \_ 層級 \_ PKT) </span><span class="sxs-lookup"><span data-stu-id="94281-122"><span id="Packet__RPC_C_AUTHN_LEVEL_PKT_"></span><span id="packet__rpc_c_authn_level_pkt_"></span><span id="PACKET__RPC_C_AUTHN_LEVEL_PKT_"></span>Packet (RPC\_C\_AUTHN\_LEVEL\_PKT)</span></span>
</dt> <dd>

<span data-ttu-id="94281-123">每個封包的標頭都已簽署但未加密。</span><span class="sxs-lookup"><span data-stu-id="94281-123">The header of each packet is signed but not encrypted.</span></span> <span data-ttu-id="94281-124">封包本身不會進行簽署或加密。</span><span class="sxs-lookup"><span data-stu-id="94281-124">The packets themselves are not signed or encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="94281-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>封包完整性 (RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 完整性) </span><span class="sxs-lookup"><span data-stu-id="94281-125"><span id="Packet_Integrity__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span><span id="packet_integrity__rpc_c_authn_level_pkt_integrity_"></span><span id="PACKET_INTEGRITY__RPC_C_AUTHN_LEVEL_PKT_INTEGRITY_"></span>Packet Integrity (RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY)</span></span>
</dt> <dd>

<span data-ttu-id="94281-126">每個資料封包都會完整登入，但不會加密。</span><span class="sxs-lookup"><span data-stu-id="94281-126">Each packet of data is signed in its entirety but is not encrypted.</span></span> <span data-ttu-id="94281-127">由於所有資料都是由傳送者簽署，因此收件者可以確定在傳輸期間沒有任何資料遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="94281-127">Because all of the data is signed by the sender, the recipient can be certain that none of the data has been tampered with during transit.</span></span>

</dd> <dt>

<span data-ttu-id="94281-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>封包隱私權 (RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權) </span><span class="sxs-lookup"><span data-stu-id="94281-128"><span id="Packet_Privacy__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span><span id="packet_privacy__rpc_c_authn_level_pkt_privacy_"></span><span id="PACKET_PRIVACY__RPC_C_AUTHN_LEVEL_PKT_PRIVACY_"></span>Packet Privacy (RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY)</span></span>
</dt> <dd>

<span data-ttu-id="94281-129">每個資料封包都會經過簽署和加密。</span><span class="sxs-lookup"><span data-stu-id="94281-129">Each data packet is signed and encrypted.</span></span> <span data-ttu-id="94281-130">這有助於保護用戶端與伺服器之間的整個通訊。</span><span class="sxs-lookup"><span data-stu-id="94281-130">This helps protect the entire communication between the client and server.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="94281-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="94281-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94281-132">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="94281-132">AuthenticationLevel</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="94281-133">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="94281-133">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
</dt> </dl>

 

 




