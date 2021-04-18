---
description: 模擬的 Server-Side 需求
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: 模擬的 Server-Side 需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971315"
---
# <a name="server-side-requirements-for-impersonation"></a><span data-ttu-id="8cdc8-103">模擬的 Server-Side 需求</span><span class="sxs-lookup"><span data-stu-id="8cdc8-103">Server-Side Requirements for Impersonation</span></span>

<span data-ttu-id="8cdc8-104">伺服器會以程式設計的方式執行模擬。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-104">The server performs impersonation programmatically.</span></span> <span data-ttu-id="8cdc8-105">它會使用 [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)明確地假設用戶端的安全性認證。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-105">It explicitly assumes the client's security credentials by using [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span> <span data-ttu-id="8cdc8-106">當用戶端授與伺服器足夠的授權單位時，這會產生將用戶端的安全性認證取代為伺服器執行緒權杖的效果，以取代處理常式權杖。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-106">When the client has granted the server sufficient authority, this has the effect of substituting the client's security credentials with the server thread token, in place of the process token.</span></span>

<span data-ttu-id="8cdc8-107">例如，伺服器可以使用用戶端權杖來存取受安全描述項保護的資源。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-107">When this has been done, the server can, for example, use the client token to access resources guarded with a security descriptor.</span></span> <span data-ttu-id="8cdc8-108">或者，如果已啟用掩蓋，也可以在用戶端身分識別下進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-108">Or it can make calls under the client identity, if cloaking is enabled.</span></span>

<span data-ttu-id="8cdc8-109">伺服器可以用程式設計的方式明確設定掩蓋，也可以依賴系統管理設定。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-109">The server can explicitly set cloaking programmatically, or it can rely on an administrative setting.</span></span> <span data-ttu-id="8cdc8-110">根據預設，COM + 應用程式會設定為使用動態掩蓋。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-110">By default, COM+ applications are configured to use dynamic cloaking.</span></span> <span data-ttu-id="8cdc8-111">如需詳細資訊，請參閱「 [掩蔽](cloaking.md)」。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-111">For more detail, see [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="8cdc8-112">如果伺服器正在代表用戶端執行委派（使用用戶端身分識別透過網路），則伺服器進程身分識別必須在 Active Directory 服務中標示為「受信任的委派」;否則委派會失敗。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-112">If the server is implementing delegation on behalf of the client—using the client identity over network—the server process identity must be marked as "Trusted for delegation" in the Active Directory Service; otherwise, delegation will fail.</span></span>

<span data-ttu-id="8cdc8-113">當它完成使用用戶端的身分識別時，伺服器可以使用 [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)還原為自己的進程權杖。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-113">When it has finished using the client's identity, the server can revert to its own process token using [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="8cdc8-114">如需有關實施模擬和委派的詳細資訊，請參閱 [委派和](/windows/desktop/com/delegation-and-impersonation)模擬。</span><span class="sxs-lookup"><span data-stu-id="8cdc8-114">For details on implementing impersonation and delegation, see [Delegation and Impersonation](/windows/desktop/com/delegation-and-impersonation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cdc8-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8cdc8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cdc8-116">用戶端模擬和委派</span><span class="sxs-lookup"><span data-stu-id="8cdc8-116">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="8cdc8-117">模擬的用戶端需求</span><span class="sxs-lookup"><span data-stu-id="8cdc8-117">Client-Side Requirements for Impersonation</span></span>](client-side-requirements-for-impersonation.md)
</dt> <dt>

[<span data-ttu-id="8cdc8-118">隱形</span><span class="sxs-lookup"><span data-stu-id="8cdc8-118">Cloaking</span></span>](cloaking.md)
</dt> </dl>

 

 
