---
title: 查詢使用者
description: 若要查詢使用者，查詢必須包含搜尋運算式 \ 0034; ( (objectClass 使用者)  (objectCategory person) ) \ 0034;。
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- 使用者廣告，查詢使用者
- Active Directory、使用、使用者、查詢使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681647"
---
# <a name="querying-for-users"></a><span data-ttu-id="3ac4c-105">查詢使用者</span><span class="sxs-lookup"><span data-stu-id="3ac4c-105">Querying for Users</span></span>

<span data-ttu-id="3ac4c-106">若要查詢使用者，查詢必須包含搜尋運算式 " (& (objectClass = user)  (objectCategory = person) ) "。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="3ac4c-107">由於 computer 類別是使用者的子類別，因此只包含 (objectClass = user) 的查詢會傳回使用者物件和電腦物件。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="3ac4c-108">此外，使用者物件的物件類別是 person (不是使用者) ;因此， (objectCategory = user) 的運算式不會傳回任何使用者。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="3ac4c-109">如果您使用運算式 (objectCategory = person) ，查詢會傳回使用者物件和 contact 物件。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="3ac4c-110">使用者可以放在網域的任何容器或組織單位中，也可以放在網域的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="3ac4c-111">這表示使用者可以位於目錄階層中的多個位置。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="3ac4c-112">您可以執行 " (objectCategory = user) " 的深層搜尋，以尋找容器、組織單位、網域、網域樹狀結構或樹系中的所有使用者，視您所使用的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標所系結至的物件而定。</span><span class="sxs-lookup"><span data-stu-id="3ac4c-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 