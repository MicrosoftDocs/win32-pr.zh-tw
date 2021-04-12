---
description: 模擬的 Client-Side 需求
ms.assetid: c2d20233-93c6-4d2d-946d-8abccbeb3c5e
title: 模擬的 Client-Side 需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c3c188f3c03e46a0e6e414efc66c5fdd2366d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317940"
---
# <a name="client-side-requirements-for-impersonation"></a><span data-ttu-id="4b95d-103">模擬的 Client-Side 需求</span><span class="sxs-lookup"><span data-stu-id="4b95d-103">Client-Side Requirements for Impersonation</span></span>

<span data-ttu-id="4b95d-104">您可以針對用戶端上的模擬指定下列兩個設定：</span><span class="sxs-lookup"><span data-stu-id="4b95d-104">The following two settings can be specified relative to impersonation on the client side:</span></span>

-   <span data-ttu-id="4b95d-105">模擬層級，指出用戶端要讓伺服器使用其身分識別的意願。</span><span class="sxs-lookup"><span data-stu-id="4b95d-105">Impersonation level, which indicates the client's willingness to have the server use its identity.</span></span>
-   <span data-ttu-id="4b95d-106">Active Directory 服務中的設定，可將用戶端帳戶標示為「帳戶是機密的，無法委派」，這將會停用委派。</span><span class="sxs-lookup"><span data-stu-id="4b95d-106">A setting in the Active Directory Service through which the client account can be marked "Account is sensitive and cannot be delegated," which will disable delegation.</span></span>

<span data-ttu-id="4b95d-107">您可以透過各種方式來設定模擬層級。</span><span class="sxs-lookup"><span data-stu-id="4b95d-107">The impersonation level can be set in a variety of ways.</span></span> <span data-ttu-id="4b95d-108">如果用戶端沒有指出模擬等級，COM 將會使用整個電腦的預設值。</span><span class="sxs-lookup"><span data-stu-id="4b95d-108">If the client does not indicate an impersonation level, the machine-wide default will be used by COM.</span></span> <span data-ttu-id="4b95d-109">您可以使用 [元件服務] 系統管理工具或 Dcomcnfg.exe 來設定整個電腦的預設值。</span><span class="sxs-lookup"><span data-stu-id="4b95d-109">The machine-wide default can be set using either the Component Services administrative tool or Dcomcnfg.exe.</span></span> <span data-ttu-id="4b95d-110">用戶端也可以使用 Dcomcnfg.exe 來表示系統管理慣用的模擬等級。</span><span class="sxs-lookup"><span data-stu-id="4b95d-110">The client can also indicate a preferred impersonation level administratively with Dcomcnfg.exe.</span></span>

<span data-ttu-id="4b95d-111">用戶端可以透過程式設計的方式，使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)（相當於 [**IClientSecurity：： SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket)）來表示模擬層級，您可以視需要經常呼叫此層級，或 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)，每個進程都可以呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="4b95d-111">The client can indicate the impersonation level programmatically, using either [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)—equivalent to [**IClientSecurity::SetBlanket**](/windows/desktop/api/objidl/nf-objidl-iclientsecurity-setblanket), which can be called as often as necessary—or [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), which can be called once per process.</span></span>

<span data-ttu-id="4b95d-112">如果用戶端指出委派層級模擬（可授與伺服器的最大授權），則用戶端應該在 Active Directory 服務中正確設定的身分識別下執行，以啟用其身分識別的委派。</span><span class="sxs-lookup"><span data-stu-id="4b95d-112">If the client indicates delegate-level impersonation—the broadest authority it can grant to the server—the client should be running under an identity that is properly configured in the Active Directory Service to enable its identity to be delegated.</span></span>

<span data-ttu-id="4b95d-113">如需有關模擬層級和委派運作需求的詳細資訊，請參閱 [委派和](/windows/desktop/com/delegation-and-impersonation)模擬。</span><span class="sxs-lookup"><span data-stu-id="4b95d-113">For more detail regarding impersonation levels and the requirements for delegation to work, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

<span data-ttu-id="4b95d-114">當然，COM + 應用程式一律可以做為用戶端。</span><span class="sxs-lookup"><span data-stu-id="4b95d-114">COM+ applications can always act as clients, of course.</span></span> <span data-ttu-id="4b95d-115">當 COM + 應用程式呼叫另一個應用程式或資源時，它會表示模擬層級。</span><span class="sxs-lookup"><span data-stu-id="4b95d-115">When the COM+ application makes a call to another application or resource, it expresses an impersonation level.</span></span> <span data-ttu-id="4b95d-116">針對 COM + 伺服器應用程式，您可以設定模擬層級的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="4b95d-116">For COM+ server applications, you can set an impersonation level administratively.</span></span> <span data-ttu-id="4b95d-117">COM + 程式庫應用程式無法設定自己的模擬層級;它們會改用主機進程的。</span><span class="sxs-lookup"><span data-stu-id="4b95d-117">COM+ library applications cannot set their own impersonation level; they use that of the host process instead.</span></span> <span data-ttu-id="4b95d-118">若要瞭解如何設定 COM + 應用程式的模擬，請參閱 [設定模擬等級](setting-an-impersonation-level.md)。</span><span class="sxs-lookup"><span data-stu-id="4b95d-118">To learn how to set impersonation for a COM+ application, see [Setting an Impersonation Level](setting-an-impersonation-level.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b95d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b95d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b95d-120">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="4b95d-120">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="4b95d-121">隱形</span><span class="sxs-lookup"><span data-stu-id="4b95d-121">Cloaking</span></span>](cloaking.md)
</dt> <dt>

[<span data-ttu-id="4b95d-122">模擬的伺服器端需求</span><span class="sxs-lookup"><span data-stu-id="4b95d-122">Server-Side Requirements for Impersonation</span></span>](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
