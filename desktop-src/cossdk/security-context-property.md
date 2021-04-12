---
description: 資訊安全內容屬性
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: 資訊安全內容屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191023"
---
# <a name="security-context-property"></a><span data-ttu-id="9d4a2-103">資訊安全內容屬性</span><span class="sxs-lookup"><span data-stu-id="9d4a2-103">Security Context Property</span></span>

<span data-ttu-id="9d4a2-104">如同 COM + 所提供的每個自動服務，自動角色檢查是以物件內容所包含的屬性為基礎。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-104">As with every automatic service provided by COM+, automatic role checking is based on properties included on the object context.</span></span> <span data-ttu-id="9d4a2-105">決定是否必須在呼叫元件時執行安全性檢查，是根據設定的元件具現化時所建立物件內容上的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-105">The determination of whether a security check must be carried out on a call into a component is based on the security property on the object context created when the configured component is instantiated.</span></span>

<span data-ttu-id="9d4a2-106">您通常不需要擔心這個屬性;它直接由 COM + （而非您）使用。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-106">You generally don't need to be concerned with this property; it is used directly by COM+, not you.</span></span> <span data-ttu-id="9d4a2-107">不過，在某些情況下，您可能會想要嚴格控制物件的啟用。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-107">However, in some circumstances, you might want strict control over the activation of an object.</span></span> <span data-ttu-id="9d4a2-108">在此情況下，安全性屬性可能會影響您的物件在哪個內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-108">In this case, the security property can affect which context your object is activated in.</span></span> <span data-ttu-id="9d4a2-109">也就是說，如果物件的設定與其建立者的內容不相容，則會在其本身的內容中啟用。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-109">That is, if an object has a configuration incompatible with the context of its creator, it will be activated in its own context.</span></span> <span data-ttu-id="9d4a2-110">安全性屬性可能會影響這一點，如同物件內容上的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-110">The security property can influence this, as can any property on the object context.</span></span>

<span data-ttu-id="9d4a2-111">如果您不想讓安全性設定影響啟用，則只能選擇處理層級的存取檢查。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-111">If you don't want security settings to influence activation, you can choose process-level access checking only.</span></span> <span data-ttu-id="9d4a2-112">這會隱藏物件內容上的安全性屬性，雖然它會有效停用以角色為基礎的檢查，並讓 [安全性呼叫內容資訊](security-call-context-information.md) 無法使用。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-112">This suppresses the security property on the object context, although it effectively disables role-based checking and makes [security call context information](security-call-context-information.md) unavailable.</span></span>

<span data-ttu-id="9d4a2-113">如需有關進程層級存取檢查的詳細資訊，請參閱 [安全性界限](security-boundaries.md)。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-113">For more information about process-level access checks, see [Security Boundaries](security-boundaries.md).</span></span> <span data-ttu-id="9d4a2-114">若要瞭解如何設定進程層級安全性，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md)。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-114">To see how to set process-level security, see [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span>

<span data-ttu-id="9d4a2-115">如需物件內容的詳細資訊， [請參閱內容](com--contexts.md)。</span><span class="sxs-lookup"><span data-stu-id="9d4a2-115">For more information about object context, see [Contexts](com--contexts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d4a2-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d4a2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d4a2-117">有效設計角色</span><span class="sxs-lookup"><span data-stu-id="9d4a2-117">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
</dt> <dt>

[<span data-ttu-id="9d4a2-118">安全性界限</span><span class="sxs-lookup"><span data-stu-id="9d4a2-118">Security Boundaries</span></span>](security-boundaries.md)
</dt> <dt>

[<span data-ttu-id="9d4a2-119">安全性呼叫內容資訊</span><span class="sxs-lookup"><span data-stu-id="9d4a2-119">Security Call Context Information</span></span>](security-call-context-information.md)
</dt> <dt>

[<span data-ttu-id="9d4a2-120">使用角色進行用戶端授權</span><span class="sxs-lookup"><span data-stu-id="9d4a2-120">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



