---
description: 授權管理員提供彈性的架構，將角色型存取控制整合到應用程式。 它讓使用這些應用程式的系統管理員，透過指派與工作功能相關的使用者角色來提供存取。
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: 授權管理員模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321220"
---
# <a name="authorization-manager-model"></a><span data-ttu-id="68f81-104">授權管理員模型</span><span class="sxs-lookup"><span data-stu-id="68f81-104">Authorization Manager Model</span></span>

<span data-ttu-id="68f81-105">授權管理員提供彈性的架構，將角色型存取控制整合到應用程式。</span><span class="sxs-lookup"><span data-stu-id="68f81-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="68f81-106">它讓使用這些應用程式的系統管理員，透過指派與工作功能相關的使用者角色來提供存取。</span><span class="sxs-lookup"><span data-stu-id="68f81-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="68f81-107">授權管理員應用程式會使用授權存放區的形式存放授權原則，授權存放區會儲存在 Active Directory 或 XML 檔案中，並且在執行階段套用授權原則。</span><span class="sxs-lookup"><span data-stu-id="68f81-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="68f81-108">然後，應用程式會呼叫執行時間存取檢查方法，以針對授權存放中的原則資訊檢查存取權。</span><span class="sxs-lookup"><span data-stu-id="68f81-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="68f81-109">授權原則包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="68f81-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="68f81-110">原則存放區、應用程式和範圍</span><span class="sxs-lookup"><span data-stu-id="68f81-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="68f81-111">使用者和群組</span><span class="sxs-lookup"><span data-stu-id="68f81-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="68f81-112">作業和工作</span><span class="sxs-lookup"><span data-stu-id="68f81-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="68f81-113">角色</span><span class="sxs-lookup"><span data-stu-id="68f81-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="68f81-114">商務規則</span><span class="sxs-lookup"><span data-stu-id="68f81-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="68f81-115">集合</span><span class="sxs-lookup"><span data-stu-id="68f81-115">Collections</span></span>](collections.md)

 

 



