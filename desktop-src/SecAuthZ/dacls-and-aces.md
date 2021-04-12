---
description: 如果 Windows 物件沒有任意的存取控制清單 (DACL) ，則系統允許所有人都能完整存取它。
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: Dacl 和 Ace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194939"
---
# <a name="dacls-and-aces"></a><span data-ttu-id="e54fe-103">Dacl 和 Ace</span><span class="sxs-lookup"><span data-stu-id="e54fe-103">DACLs and ACEs</span></span>

<span data-ttu-id="e54fe-104">如果 Windows 物件沒有 [*任意的存取控制清單*](/windows/desktop/SecGloss/d-gly) (DACL) ，則系統允許所有人都能完整存取它。</span><span class="sxs-lookup"><span data-stu-id="e54fe-104">If a Windows object does not have a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), the system allows everyone full access to it.</span></span> <span data-ttu-id="e54fe-105">如果物件具有 DACL，則系統只允許在 DACL 中 (Ace) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) 所明確允許的存取權。</span><span class="sxs-lookup"><span data-stu-id="e54fe-105">If an object has a DACL, the system allows only the access that is explicitly allowed by the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the DACL.</span></span> <span data-ttu-id="e54fe-106">如果 DACL 中沒有 Ace，系統就不允許存取任何人。</span><span class="sxs-lookup"><span data-stu-id="e54fe-106">If there are no ACEs in the DACL, the system does not allow access to anyone.</span></span> <span data-ttu-id="e54fe-107">同樣地，如果 DACL 有允許存取一組有限使用者或群組的 Ace，系統會隱含地拒絕所有不包含在 Ace 中的受信任者的存取權。</span><span class="sxs-lookup"><span data-stu-id="e54fe-107">Similarly, if a DACL has ACEs that allow access to a limited set of users or groups, the system implicitly denies access to all trustees not included in the ACEs.</span></span>

<span data-ttu-id="e54fe-108">在大部分的情況下，您可以使用允許存取的 Ace 來控制物件的存取;您不需要明確拒絕對物件的存取。</span><span class="sxs-lookup"><span data-stu-id="e54fe-108">In most cases, you can control access to an object by using access-allowed ACEs; you do not need to explicitly deny access to an object.</span></span> <span data-ttu-id="e54fe-109">例外狀況是當 ACE 允許存取群組，而您想要拒絕存取群組的成員時。</span><span class="sxs-lookup"><span data-stu-id="e54fe-109">The exception is when an ACE allows access to a group and you want to deny access to a member of the group.</span></span> <span data-ttu-id="e54fe-110">若要這樣做，請在群組的「存取允許的 ACE」之前，將使用者的「拒絕存取」 ACE 放在 DACL 中。</span><span class="sxs-lookup"><span data-stu-id="e54fe-110">To do this, place an access-denied ACE for the user in the DACL ahead of the access-allowed ACE for the group.</span></span> <span data-ttu-id="e54fe-111">請注意， [ace 的順序](order-of-aces-in-a-dacl.md) 很重要，因為系統會依序讀取 ace，直到授與或拒絕存取為止。</span><span class="sxs-lookup"><span data-stu-id="e54fe-111">Note that the [order of the ACEs](order-of-aces-in-a-dacl.md) is important because the system reads the ACEs in sequence until access is granted or denied.</span></span> <span data-ttu-id="e54fe-112">使用者的拒絕存取權 ACE 必須先出現;否則，當系統讀取群組的存取權允許 ACE 時，即會將存取權授與受限制的使用者。</span><span class="sxs-lookup"><span data-stu-id="e54fe-112">The user's access-denied ACE must appear first; otherwise, when the system reads the group's access allowed ACE, it will grant access to the restricted user.</span></span>

<span data-ttu-id="e54fe-113">下圖顯示的 DACL 會拒絕對一位使用者的存取，並授與對兩個群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="e54fe-113">The following illustration shows a DACL that denies access to one user and grants access to two groups.</span></span> <span data-ttu-id="e54fe-114">群組 A 的成員會藉由將允許群組 A 和許可權的許可權累積給所有人，來取得讀取、寫入和執行存取權限。</span><span class="sxs-lookup"><span data-stu-id="e54fe-114">The members of Group A get Read, Write, and Execute access rights by accumulating the rights allowed to Group A and rights allowed to Everyone.</span></span> <span data-ttu-id="e54fe-115">例外狀況是 Andrew，因為它是 Everyone 群組的成員，所以遭到拒絕存取的 ACE 拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e54fe-115">The exception is Andrew, who is denied access by the access-denied ACE in spite of being a member of the Everyone Group.</span></span>

![根據群組成員資格授與不同存取權限的 dacl](images/accctrl1.png)

 

 
