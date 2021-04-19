---
title: 將存取權限授與服務登入帳戶
description: 安裝服務實例的主要考慮是確保已安裝的服務可以存取所需的資源。
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- 將存取權限授與服務登入帳戶 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106965229"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="0f00a-104">將存取權限授與服務登入帳戶</span><span class="sxs-lookup"><span data-stu-id="0f00a-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="0f00a-105">安裝服務實例的主要考慮是確保已安裝的服務可以存取所需的資源。</span><span class="sxs-lookup"><span data-stu-id="0f00a-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="0f00a-106">若要這樣做，請在服務必須存取之物件的安全描述項中設定 Ace。</span><span class="sxs-lookup"><span data-stu-id="0f00a-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="0f00a-107">ACE 可以授與或拒絕指定安全性主體的存取權限，例如服務使用者帳戶，或 LocalSystem 服務的電腦帳戶，或是服務帳戶所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="0f00a-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="0f00a-108">如需 Ace、安全描述項和存取控制的詳細資訊，請參閱 [控制存取 Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) 和 [存取控制](/windows/desktop/SecAuthZ/access-control)中的物件。</span><span class="sxs-lookup"><span data-stu-id="0f00a-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="0f00a-109">如需可用來設定可讓服務修改其服務連接點之 ACE 的詳細資訊和程式碼範例，請參閱 [啟用服務帳戶以存取 SCP 屬性](enabling-service-account-to-access-scp-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="0f00a-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="0f00a-110">在某些情況下，您必須將您的服務使用者帳戶新增為一或多個安全性群組的成員。</span><span class="sxs-lookup"><span data-stu-id="0f00a-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="0f00a-111">例如，如果您為您的服務建立系統管理員群組，您可能會將服務設為群組的成員。</span><span class="sxs-lookup"><span data-stu-id="0f00a-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="0f00a-112">然後，您可以將存取權限授與群組，而不是明確地授與服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="0f00a-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="0f00a-113">如需安全性群組的詳細資訊，請參閱 [管理群組](managing-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="0f00a-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 