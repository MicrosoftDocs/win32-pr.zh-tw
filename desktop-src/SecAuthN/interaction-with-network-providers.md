---
description: 說明 Winlogon 和網路提供者之間的互動。
ms.assetid: 09d0b5ce-e2ac-40d7-bc35-272c5f831788
title: 與網路提供者的互動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d3eeadb7a9f4d8137e1d9b1ef7ff2430910cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851740"
---
# <a name="interaction-with-network-providers"></a><span data-ttu-id="d88d6-103">與網路提供者的互動</span><span class="sxs-lookup"><span data-stu-id="d88d6-103">Interaction with Network Providers</span></span>

<span data-ttu-id="d88d6-104">您可以將系統設定為支援零個或更多的網路提供者。</span><span class="sxs-lookup"><span data-stu-id="d88d6-104">You can configure a system to support zero or more network providers.</span></span> <span data-ttu-id="d88d6-105">這些網路提供者都可以指定需要進行特殊的互動式驗證處理。</span><span class="sxs-lookup"><span data-stu-id="d88d6-105">Each of these network providers can specify that it requires special interactive authentication processing.</span></span> <span data-ttu-id="d88d6-106">這項功能可讓已安裝的網路收集每個網路專屬的識別和驗證資訊，但可讓它們在正常登入期間以及 [*Winlogon*](../secgloss/w-gly.md)的 [*內容*](../secgloss/c-gly.md) 和桌面的安全傘下收集它。</span><span class="sxs-lookup"><span data-stu-id="d88d6-106">This capability allows installed networks to collect identification and authentication information specific to each network, yet allows them to collect it during normal logon and under the secure umbrella of [*Winlogon's*](../secgloss/w-gly.md) [*context*](../secgloss/c-gly.md) and desktop.</span></span>

<span data-ttu-id="d88d6-107">Winlogon 會在許多情況下呼叫網路提供者。</span><span class="sxs-lookup"><span data-stu-id="d88d6-107">Winlogon calls network providers under a number of circumstances.</span></span> <span data-ttu-id="d88d6-108">成功登入後，Winlogon 會呼叫網路提供者，讓他們可以收集 [*認證*](../secgloss/c-gly.md) 並驗證使用者的網路。</span><span class="sxs-lookup"><span data-stu-id="d88d6-108">Following a successful logon, Winlogon calls network providers so they can collect [*credentials*](../secgloss/c-gly.md) and authenticate the user for their network.</span></span> <span data-ttu-id="d88d6-109">當使用者變更其密碼時，Winlogon 也會呼叫網路提供者。</span><span class="sxs-lookup"><span data-stu-id="d88d6-109">Winlogon also calls network providers when users change their passwords.</span></span> <span data-ttu-id="d88d6-110">這可讓每個使用者維護單一密碼以用於所有網路。</span><span class="sxs-lookup"><span data-stu-id="d88d6-110">This lets each user maintain a single password for use on all networks.</span></span>

<span data-ttu-id="d88d6-111">[**WLX \_ MPR \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info)結構是用來提供相關 GINA 函式中的識別和驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="d88d6-111">The [**WLX\_MPR\_NOTIFY\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_mpr_notify_info) structure is used to provide identification and authentication information in the relevant GINA functions.</span></span> <span data-ttu-id="d88d6-112">此結構包含下列成員。</span><span class="sxs-lookup"><span data-stu-id="d88d6-112">This structure includes the following members.</span></span>



| <span data-ttu-id="d88d6-113">member</span><span class="sxs-lookup"><span data-stu-id="d88d6-113">Member</span></span>             | <span data-ttu-id="d88d6-114">描述</span><span class="sxs-lookup"><span data-stu-id="d88d6-114">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88d6-115">**pszUserName**</span><span class="sxs-lookup"><span data-stu-id="d88d6-115">**pszUserName**</span></span>    | <span data-ttu-id="d88d6-116">登入之使用者的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d88d6-116">The account name of the logged-on user.</span></span>                                                                                                                                                      |
| <span data-ttu-id="d88d6-117">**pszDomain**</span><span class="sxs-lookup"><span data-stu-id="d88d6-117">**pszDomain**</span></span>      | <span data-ttu-id="d88d6-118">已登入使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d88d6-118">The domain name of the logged-on user.</span></span> <span data-ttu-id="d88d6-119">並非所有的驗證模型都有 (或其對等) 的領域概念，因此這個成員可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d88d6-119">Not all authentication models have a domain concept (or its equivalent), so this member can be **NULL**.</span></span>                                              |
| <span data-ttu-id="d88d6-120">**pszPassword**</span><span class="sxs-lookup"><span data-stu-id="d88d6-120">**pszPassword**</span></span>    | <span data-ttu-id="d88d6-121">當使用者在驗證期間提供了純文字密碼時，在此提供它可讓其他網路提供者使用相同的密碼 (來達到單一登入) ，而不會提示使用者。</span><span class="sxs-lookup"><span data-stu-id="d88d6-121">When the user gave a plaintext password during authentication, providing it here lets other network providers use the same password (to achieve single logon) without prompting the user.</span></span>    |
| <span data-ttu-id="d88d6-122">**pszOldPassword**</span><span class="sxs-lookup"><span data-stu-id="d88d6-122">**pszOldPassword**</span></span> | <span data-ttu-id="d88d6-123">在密碼變更之後，在此提供原始密碼以及 **pszPassword** 成員的新密碼，可讓網路提供者在不提示使用者的情況下升級其密碼。</span><span class="sxs-lookup"><span data-stu-id="d88d6-123">After a password change, providing the original password here and the new password in the **pszPassword** member, lets network providers upgrade their passwords without prompting the user.</span></span> |



 

<span data-ttu-id="d88d6-124">[*GINA*](../secgloss/g-gly.md)不需要將此資訊提供給網路提供者。</span><span class="sxs-lookup"><span data-stu-id="d88d6-124">A [*GINA*](../secgloss/g-gly.md) does not have to provide this information to network providers.</span></span> <span data-ttu-id="d88d6-125">如果傳遞 **Null** 指標而非有效的結構指標，網路提供者將會提示使用者提供資訊。</span><span class="sxs-lookup"><span data-stu-id="d88d6-125">If a **NULL** pointer is passed instead of a valid structure pointer, the network providers will prompt the user for information.</span></span>

 

 
