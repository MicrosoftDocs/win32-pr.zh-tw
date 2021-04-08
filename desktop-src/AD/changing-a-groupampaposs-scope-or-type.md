---
title: 變更群組的範圍或類型
description: 本主題說明如何變更原生模式網域中的群組範圍或類型。
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- 群組 AD、變更群組的範圍或類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671004"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="cf39d-104">變更群組的範圍或類型</span><span class="sxs-lookup"><span data-stu-id="cf39d-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="cf39d-105">混合模式網域中不允許變更群組領域或類型。</span><span class="sxs-lookup"><span data-stu-id="cf39d-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="cf39d-106">不過，原生模式網域中允許下列轉換：</span><span class="sxs-lookup"><span data-stu-id="cf39d-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="cf39d-107">全域群組至萬用群組：只有在全域群組不是另一個全域群組的成員時，才允許這種情況。</span><span class="sxs-lookup"><span data-stu-id="cf39d-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="cf39d-108">網域本機群組到萬用群組：要轉換的網網域本機群組不能包含另一個網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="cf39d-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="cf39d-109">萬用群組對全域或網域本機群組：若要轉換為全域群組，正在轉換的萬用群組不能包含來自另一個網域的使用者或全域群組。</span><span class="sxs-lookup"><span data-stu-id="cf39d-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="cf39d-110">若要轉換為網域本機群組，正在轉換的萬用群組不能是任何萬用群組的成員，也不能是來自另一個網域的網域本機群組成員。</span><span class="sxs-lookup"><span data-stu-id="cf39d-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="cf39d-111">在原生模式中，群組類型可以在安全性群組和通訊群組之間自由轉換。</span><span class="sxs-lookup"><span data-stu-id="cf39d-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="cf39d-112">請注意，如果群組是用來設定存取控制，則變更範圍或類型可能會影響包含該群組 (Ace) 的存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="cf39d-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="cf39d-113">安全性系統會忽略包含不是安全性群組之群組的 Ace。</span><span class="sxs-lookup"><span data-stu-id="cf39d-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




