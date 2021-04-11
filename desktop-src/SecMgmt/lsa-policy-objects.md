---
description: LSA 會將本機安全性原則資訊儲存在一組物件中。 您的應用程式可以藉由存取這些物件來查詢或編輯本機安全性原則。
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: LSA 原則物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944357"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="c9eba-104">LSA 原則物件</span><span class="sxs-lookup"><span data-stu-id="c9eba-104">LSA Policy Objects</span></span>

<span data-ttu-id="c9eba-105">LSA 會將本機安全性原則資訊儲存在一組物件中。</span><span class="sxs-lookup"><span data-stu-id="c9eba-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="c9eba-106">您的應用程式可以藉由存取這些物件來查詢或編輯本機安全性原則。</span><span class="sxs-lookup"><span data-stu-id="c9eba-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="c9eba-107">此集合是由下列四個物件所組成：</span><span class="sxs-lookup"><span data-stu-id="c9eba-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="c9eba-108">[原則](policy-object.md) 包含全域原則資訊。</span><span class="sxs-lookup"><span data-stu-id="c9eba-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="c9eba-109">[TrustedDomain](trusteddomain-object.md) 包含受信任網域的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c9eba-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="c9eba-110">[帳戶](account-object.md) 包含使用者、群組或本機群組帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c9eba-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="c9eba-111">[私用資料](private-data-object.md) 報含受保護的資訊，例如伺服器帳戶密碼。</span><span class="sxs-lookup"><span data-stu-id="c9eba-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="c9eba-112">這項資訊會儲存為加密字串。</span><span class="sxs-lookup"><span data-stu-id="c9eba-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="c9eba-113">如需如何使用 LSA 原則函式來管理這些物件中所儲存資訊的詳細資訊，請參閱 [使用 Lsa 原則](using-lsa-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="c9eba-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



