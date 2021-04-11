---
description: Microsoft Negotiate 是安全性支援提供者，可作為安全性支援提供者介面和其他 Ssp 之間的應用層。
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943369"
---
# <a name="microsoft-negotiate"></a><span data-ttu-id="60319-103">Microsoft Negotiate</span><span class="sxs-lookup"><span data-stu-id="60319-103">Microsoft Negotiate</span></span>

<span data-ttu-id="60319-104">Microsoft Negotiate 是 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) ，可作為 [*安全性支援提供者介面*](../secgloss/s-gly.md) ([SSPI](sspi.md)) 和其他 ssp 之間的應用層。</span><span class="sxs-lookup"><span data-stu-id="60319-104">Microsoft Negotiate is a [*security support provider*](../secgloss/s-gly.md) (SSP) that acts as an application layer between [*Security Support Provider Interface*](../secgloss/s-gly.md) ([SSPI](sspi.md)) and the other SSPs.</span></span> <span data-ttu-id="60319-105">當應用程式呼叫 SSPI 以登入網路時，它可以指定 SSP 來處理要求。</span><span class="sxs-lookup"><span data-stu-id="60319-105">When an application calls into SSPI to log on to a network, it can specify an SSP to process the request.</span></span> <span data-ttu-id="60319-106">如果應用程式指定 Negotiate，Negotiate 會分析要求，並根據客戶設定的安全性原則挑選最適合的 SSP 來處理要求。</span><span class="sxs-lookup"><span data-stu-id="60319-106">If the application specifies Negotiate, Negotiate analyzes the request and picks the best SSP to handle the request based on customer-configured security policy.</span></span>

<span data-ttu-id="60319-107">目前，協商安全性封裝會在 [Kerberos](microsoft-kerberos.md) 和 [NTLM](microsoft-ntlm.md)之間進行選取。</span><span class="sxs-lookup"><span data-stu-id="60319-107">Currently, the Negotiate security package selects between [Kerberos](microsoft-kerberos.md) and [NTLM](microsoft-ntlm.md).</span></span> <span data-ttu-id="60319-108">除非其中一個涉及驗證的系統無法使用，或呼叫的應用程式未提供足夠的資訊來使用 Kerberos，否則 Negotiate 會選取 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="60319-108">Negotiate selects Kerberos unless it cannot be used by one of the systems involved in the authentication or the calling application did not provide sufficient information to use Kerberos.</span></span>

<span data-ttu-id="60319-109">若要允許 Negotiate 選取 [Kerberos](microsoft-kerberos.md) 安全性提供者，用戶端應用程式必須提供 [*服務主體名稱*](../secgloss/s-gly.md) (SPN) 、使用者主體名稱 (UPN) 或 NetBIOS 帳戶名稱做為目標名稱。</span><span class="sxs-lookup"><span data-stu-id="60319-109">To allow Negotiate to select the [Kerberos](microsoft-kerberos.md) security provider, the client application must provide a [*service principal name*](../secgloss/s-gly.md) (SPN), a user principal name (UPN), or a NetBIOS account name as the target name.</span></span> <span data-ttu-id="60319-110">否則，Negotiate 一律會選取 [NTLM](microsoft-ntlm.md) 安全性提供者。</span><span class="sxs-lookup"><span data-stu-id="60319-110">Otherwise, Negotiate always selects the [NTLM](microsoft-ntlm.md) security provider.</span></span>

<span data-ttu-id="60319-111">使用 Negotiate 封裝的伺服器能夠回應明確選取 [Kerberos](microsoft-kerberos.md) 或 [NTLM](microsoft-ntlm.md) 安全性提供者的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="60319-111">A server that uses the Negotiate package is able to respond to client applications that specifically select either the [Kerberos](microsoft-kerberos.md) or [NTLM](microsoft-ntlm.md) security provider.</span></span> <span data-ttu-id="60319-112">不過，用戶端應用程式必須知道伺服器支援 Negotiate 封裝，才能使用 Negotiate 要求驗證。</span><span class="sxs-lookup"><span data-stu-id="60319-112">However, a client application must know that a server supports the Negotiate package to request authentication using Negotiate.</span></span> <span data-ttu-id="60319-113">不支援 Negotiate 的伺服器不一定會回應指定 Negotiate 作為 SSP 之用戶端的要求。</span><span class="sxs-lookup"><span data-stu-id="60319-113">A server that does not support Negotiate cannot always respond to requests from clients that specify Negotiate as the SSP.</span></span>

## <a name="reasons-to-use-the-negotiate-package"></a><span data-ttu-id="60319-114">使用 Negotiate 套件的原因</span><span class="sxs-lookup"><span data-stu-id="60319-114">Reasons to Use the Negotiate Package</span></span>

-   <span data-ttu-id="60319-115">允許系統使用最強的 (最安全) 可用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="60319-115">Allows the system to use the strongest (most secure) available protocol.</span></span>
-   <span data-ttu-id="60319-116">確保應用程式的向前相容性。</span><span class="sxs-lookup"><span data-stu-id="60319-116">Ensures forward compatibility for your application.</span></span>
-   <span data-ttu-id="60319-117">確保您的應用程式表現出與客戶所設定之安全性原則一致的行為。</span><span class="sxs-lookup"><span data-stu-id="60319-117">Ensures that your application exhibits behavior that is in accordance with the security policy set by the customer.</span></span>

 

 
