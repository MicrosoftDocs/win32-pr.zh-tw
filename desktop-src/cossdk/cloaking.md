---
description: 有兩個因素可決定模擬的行為：用戶端會透過模擬等級明確授與伺服器的授權，以及在用戶端上呼叫用戶端時，能夠遮罩自己的身分識別。
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: " (元件服務的掩蔽) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688719"
---
# <a name="cloaking-component-services"></a><span data-ttu-id="ddafb-103"> (元件服務的掩蔽) </span><span class="sxs-lookup"><span data-stu-id="ddafb-103">Cloaking (Component Services)</span></span>

<span data-ttu-id="ddafb-104">有兩個因素可決定模擬的行為：用戶端會透過模擬等級明確授與伺服器，以及在代表用戶端進行呼叫時，讓伺服器能夠遮罩自己的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ddafb-104">There are two ingredients in determining the behavior of impersonation: the authority the client explicitly grants the server through an impersonation level and the server's ability to mask its own identity when making calls on the client's behalf.</span></span> <span data-ttu-id="ddafb-105">後者的功能稱為 *掩蓋*。</span><span class="sxs-lookup"><span data-stu-id="ddafb-105">This latter capability is known as *cloaking*.</span></span> <span data-ttu-id="ddafb-106">掩蓋必須利用伺服器進行呼叫所使用的安全性識別。</span><span class="sxs-lookup"><span data-stu-id="ddafb-106">Cloaking has to do with the security identity under which the server makes calls.</span></span>

<span data-ttu-id="ddafb-107">當伺服器模擬用戶端時，它可以直接存取用戶端的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="ddafb-107">When the server impersonates the client, it has direct access to the client's security credentials.</span></span> <span data-ttu-id="ddafb-108">在本機上，伺服器執行緒會採用用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ddafb-108">In a very local sense, the server thread takes on the identity of the client.</span></span> <span data-ttu-id="ddafb-109">但是，當伺服器在其進程之外進行呼叫時，不一定會將用戶端身分識別投射為進行呼叫時所用的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ddafb-109">But when the server makes calls outside of its process, the client identity will not necessarily be projected as the identity under which the call is made.</span></span>

<span data-ttu-id="ddafb-110">啟用「遮蓋」時，您可以透過用戶端的身分識別，在模擬用戶端的伺服器上進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="ddafb-110">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="ddafb-111">停用遮蓋時，伺服器的呼叫會在伺服器的身分識別下進行。</span><span class="sxs-lookup"><span data-stu-id="ddafb-111">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

<span data-ttu-id="ddafb-112">此外，也有兩種形式的掩蓋、 *靜態的掩蓋* 和 *動態掩蓋*，如下所述：</span><span class="sxs-lookup"><span data-stu-id="ddafb-112">Moreover, there are two forms of cloaking, *static cloaking* and *dynamic cloaking*, which can be described as follows:</span></span>

-   <span data-ttu-id="ddafb-113">使用靜態掩蓋進行模擬。</span><span class="sxs-lookup"><span data-stu-id="ddafb-113">Impersonation with static cloaking.</span></span> <span data-ttu-id="ddafb-114">原始用戶端身分識別 (發現為伺服器執行緒權杖，) 可以使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)在呼叫上向下游伺服器顯示一次，並在 proxy 上設定一次原始用戶端識別，而該執行緒權杖將用於後續的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="ddafb-114">The original client identity (realized as the server thread token) can be presented once to a downstream server on a call using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), setting the original client identity once on the proxy, and that thread token will be used on subsequent method calls.</span></span>
-   <span data-ttu-id="ddafb-115">使用動態掩蓋進行模擬。</span><span class="sxs-lookup"><span data-stu-id="ddafb-115">Impersonation with dynamic cloaking.</span></span> <span data-ttu-id="ddafb-116">在對下游伺服器的每個方法呼叫上，會將原始用戶端身分識別視為伺服器執行緒 token。</span><span class="sxs-lookup"><span data-stu-id="ddafb-116">The original client identity is discovered as the server thread token on each method call to the downstream server.</span></span> <span data-ttu-id="ddafb-117">實際上，提供的身分識別可動態判斷。</span><span class="sxs-lookup"><span data-stu-id="ddafb-117">In effect, the identity that is presented can be determined dynamically.</span></span> <span data-ttu-id="ddafb-118">進行此作業所需的額外負荷可能會大幅增加。</span><span class="sxs-lookup"><span data-stu-id="ddafb-118">The overhead required to do this can be considerably more expensive.</span></span>

<span data-ttu-id="ddafb-119">針對 COM + 應用程式，預設設定為動態掩蓋功能。</span><span class="sxs-lookup"><span data-stu-id="ddafb-119">For COM+ applications, the default configuration is for dynamic cloaking capability.</span></span> <span data-ttu-id="ddafb-120">這可以透過程式設計的方式和系統管理員來變更。</span><span class="sxs-lookup"><span data-stu-id="ddafb-120">This can be changed programmatically and administratively.</span></span> <span data-ttu-id="ddafb-121">雖然動態擬呼可能會有效能額外負荷，但它提供的彈性通常是需要先使用模擬的情況。</span><span class="sxs-lookup"><span data-stu-id="ddafb-121">While dynamic cloaking can have performance overhead, it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

<span data-ttu-id="ddafb-122">如需有關可能行為之掩蓋和精確描述的詳細資訊，請參閱 COM 檔中的「 [掩蔽](/windows/desktop/com/cloaking) 」。</span><span class="sxs-lookup"><span data-stu-id="ddafb-122">For more detail regarding cloaking and precise descriptions of possible behaviors, see [Cloaking](/windows/desktop/com/cloaking) in the COM documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddafb-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="ddafb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddafb-124">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="ddafb-124">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="ddafb-125">模擬的用戶端需求</span><span class="sxs-lookup"><span data-stu-id="ddafb-125">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="ddafb-126">模擬的伺服器端需求</span><span class="sxs-lookup"><span data-stu-id="ddafb-126">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
