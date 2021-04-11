---
title: 完整性和隱私權
description: 需要相互驗證的用戶端/服務通訊必須保護它們在成功驗證之後交換的流量。
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- 完整性和隱私權 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ed167c3796aec2b0717b1207ff56565ec94afa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933059"
---
# <a name="integrity-and-privacy"></a><span data-ttu-id="5bd7d-104">完整性和隱私權</span><span class="sxs-lookup"><span data-stu-id="5bd7d-104">Integrity and Privacy</span></span>

<span data-ttu-id="5bd7d-105">需要相互驗證的用戶端/服務通訊必須保護它們在成功驗證之後交換的流量。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-105">Client/service communications that require mutual authentication must protect the traffic they exchange after successful authentication.</span></span> <span data-ttu-id="5bd7d-106">如果流量稍後可能被未經授權的使用者修改，則造成在初始連線至服務時進行相互驗證。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-106">It is unwise to mutually authenticate at the time of the initial connection to the service if the traffic is later subject to modification by an unauthorized user.</span></span> <span data-ttu-id="5bd7d-107">SSPI、RPC 和 COM 都提供可用於數位簽署和加密訊息的公用程式。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-107">SSPI, RPC, and COM all provide utilities for digitally signing and encrypting messages.</span></span> <span data-ttu-id="5bd7d-108">套用數位簽章可防止未偵測到的已修改流量，以及防止竊聽。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-108">Applying digital signatures prevents modified traffic from going undetected and discourages eavesdropping.</span></span> <span data-ttu-id="5bd7d-109">您可以攔截流量，但是解密流量很難阻擋大多數未經授權的使用者。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-109">Traffic can be intercepted of course, but decrypting the traffic is sufficiently difficult to deter most unauthorized users.</span></span>

<span data-ttu-id="5bd7d-110">除非效能需求很嚴重，否則建議使用簽署和加密，尤其是針對系統管理功能。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-110">Unless performance requirements are severe, use of both signing and encryption is recommended, especially for administrative functions.</span></span> <span data-ttu-id="5bd7d-111">即使當效能是問題時，有些客戶會選擇更嚴密的安全性，以提升效能。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-111">Even when performance is an issue, some customers choose tighter security over better performance.</span></span> <span data-ttu-id="5bd7d-112">在這種情況下，請以較高的安全性提供完整性和隱私權可設定選項，此選項預設和更高的效能。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-112">In such cases, make integrity and privacy configurable options with higher security the default and higher performance the option.</span></span>

<span data-ttu-id="5bd7d-113">RPC 用戶端可以在呼叫 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函式來設定 RPC 系結的驗證資料時，指定完整性和隱私權的層級。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-113">RPC clients can specify the level of integrity and privacy when they call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="5bd7d-114">使用 **rpc \_ c \_ 驗證 \_ level \_ pkt \_ 完整性** 進行簽署，並使用 **rpc \_ c \_ 驗證 \_ LEVEL \_ pkt \_ 隱私權** 進行加密。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-114">Use **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** for signing and **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** for encryption.</span></span> <span data-ttu-id="5bd7d-115">如需詳細資訊，請參閱 [RPC 應用程式中的相互驗證](mutual-authentication-in-rpc-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-115">For more information, see [Mutual Authentication in RPC Applications](mutual-authentication-in-rpc-applications.md).</span></span>

<span data-ttu-id="5bd7d-116">使用 SSPI 套件進行相互驗證的服務可以查詢套件，以判斷它是否支援 [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature)、 [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature)、 [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)和 [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) 功能來簽署和加密訊息。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-116">Services that use an SSPI package for mutual authentication can query the package to determine whether it supports the [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md), and [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) functions for signing and encrypting messages.</span></span> <span data-ttu-id="5bd7d-117">如需詳細資訊和程式碼範例，請參閱 [確保訊息交換期間的通訊完整性](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange)。</span><span class="sxs-lookup"><span data-stu-id="5bd7d-117">For more information and a code example, see [Ensuring Communication Integrity During Message Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).</span></span>

 

 