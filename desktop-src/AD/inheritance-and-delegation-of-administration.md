---
title: 管理的繼承和委派
description: 描述在物件樹狀結構中繼承許可權的 AD DS 支援，以及物件特定的繼承。
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- 管理繼承和委派 Active Directory
- Active Directory Active Directory，許可權繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183008"
---
# <a name="inheritance-and-delegation-of-administration"></a><span data-ttu-id="13f85-105">管理的繼承和委派</span><span class="sxs-lookup"><span data-stu-id="13f85-105">Inheritance and Delegation of Administration</span></span>

<span data-ttu-id="13f85-106">Active Directory Domain Services 支援在物件樹狀結構中繼承許可權，以允許在樹狀結構中較高的層級執行系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="13f85-106">Active Directory Domain Services supports the inheritance of permissions down the object tree to allow administration tasks to be performed at higher levels in the tree.</span></span> <span data-ttu-id="13f85-107">這可讓系統管理員設定根目錄附近物件的可繼承許可權，例如網域和組織單位，並將這些許可權散發給樹狀結構中的各種物件。</span><span class="sxs-lookup"><span data-stu-id="13f85-107">This enables administrators to set up inheritable permissions on objects near the root, such as domain and organizational units, and have those permissions distributed to various objects in the tree.</span></span>

<span data-ttu-id="13f85-108">您可以根據每個 ACE 來設定繼承。</span><span class="sxs-lookup"><span data-stu-id="13f85-108">Inheritance can be set on a per-ACE basis.</span></span> <span data-ttu-id="13f85-109">下表列出可在 **AceFlags** 中指定以控制 ACE 繼承的旗標。</span><span class="sxs-lookup"><span data-stu-id="13f85-109">The following table lists flags that can be specified in the **AceFlags** to control inheritance of the ACE.</span></span>



| <span data-ttu-id="13f85-110">旗標</span><span class="sxs-lookup"><span data-stu-id="13f85-110">Flag</span></span>                                                     | <span data-ttu-id="13f85-111">描述</span><span class="sxs-lookup"><span data-stu-id="13f85-111">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f85-112">**ADS \_ ACEFLAG \_ 繼承 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="13f85-112">**ADS\_ACEFLAG\_INHERIT\_ACE**</span></span><br/>                | <span data-ttu-id="13f85-113">使 ACE 在樹狀結構中被繼承。</span><span class="sxs-lookup"><span data-stu-id="13f85-113">Causes the ACE to be inherited down in the tree.</span></span><br/>                                                                                     |
| <span data-ttu-id="13f85-114">**ADS \_ ACEFLAG \_ 沒有 \_ 傳播 \_ 繼承 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="13f85-114">**ADS\_ACEFLAG\_NO\_PROPAGATE\_INHERIT\_ACE**</span></span><br/> | <span data-ttu-id="13f85-115">使 ACE 只在樹狀結構中繼承一個層級。</span><span class="sxs-lookup"><span data-stu-id="13f85-115">Causes the ACE to be inherited down only one level in the tree.</span></span><br/>                                                                      |
| <span data-ttu-id="13f85-116">**ADS \_ ACEFLAG \_ 只會繼承 \_ \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="13f85-116">**ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE**</span></span><br/>          | <span data-ttu-id="13f85-117">使 ACE 在指定的物件上被忽略，而且只會被繼承，並且在繼承的地方有效。</span><span class="sxs-lookup"><span data-stu-id="13f85-117">Causes the ACE to be ignored on the object it is specified on, only be inherited down, and be effective where it has been inherited.</span></span><br/> |



 

<span data-ttu-id="13f85-118">除了設定繼承之外，Active Directory Domain Services 還支持對象特定的繼承。</span><span class="sxs-lookup"><span data-stu-id="13f85-118">In addition to setting inheritance, Active Directory Domain Services supports object-specific inheritance.</span></span> <span data-ttu-id="13f85-119">這允許將可繼承 Ace 繼承到樹狀結構，但只在特定類型的物件上生效。</span><span class="sxs-lookup"><span data-stu-id="13f85-119">This allows the inheritable ACEs to be inherited down the tree, but be effective only on a specific type of object.</span></span> <span data-ttu-id="13f85-120">這非常適合用來委派管理。</span><span class="sxs-lookup"><span data-stu-id="13f85-120">This is extremely useful in delegating administration.</span></span> <span data-ttu-id="13f85-121">例如，這可以用來設定組織單位上的特定物件可繼承 ACE，讓群組能夠完全掌控組織單位中的所有使用者物件，而不是其他任何專案。</span><span class="sxs-lookup"><span data-stu-id="13f85-121">For example, this can be used to set an object-specific inheritable ACE at an organizational unit that enables a group to have full control on all user objects in the organizational unit, but nothing else.</span></span> <span data-ttu-id="13f85-122">因此，該組織單位中的使用者管理會委派給該群組中的使用者。</span><span class="sxs-lookup"><span data-stu-id="13f85-122">Thereby, the management of users in that organizational unit gets delegated to the users in that group.</span></span>

### <a name="delegating-service-administration-with-security-groups"></a><span data-ttu-id="13f85-123">使用安全性群組委派服務管理</span><span class="sxs-lookup"><span data-stu-id="13f85-123">Delegating Service Administration with Security Groups</span></span>

<span data-ttu-id="13f85-124">使用安全性群組來定義和委派與您的應用程式伺服器相關聯的系統管理角色。</span><span class="sxs-lookup"><span data-stu-id="13f85-124">Use Security groups to define and delegate administrative roles associated with your application server.</span></span> <span data-ttu-id="13f85-125">例如，您的服務可能會與 MyService 系統管理員群組相關聯。</span><span class="sxs-lookup"><span data-stu-id="13f85-125">For example, your service may be associated with a group MyService Administrators.</span></span> <span data-ttu-id="13f85-126">識別為 MyService 系統管理員的使用者將會新增至 MyService Administrators 群組。</span><span class="sxs-lookup"><span data-stu-id="13f85-126">Users who are identified as the MyService administrators will be added to MyService Administrators group.</span></span> <span data-ttu-id="13f85-127">MyService 的安裝程式可以在目錄上設定 Acl，讓 MyService 系統管理員有足夠的許可權可讀取/寫入 MyService 相關的屬性，或建立 MyService 特定的物件。</span><span class="sxs-lookup"><span data-stu-id="13f85-127">The setup program for MyService can set ACLs on the directory to enable MyService Administrators sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

### <a name="roles-in-security-groups-for-computers-running-your-service"></a><span data-ttu-id="13f85-128">執行服務的電腦安全性組中的角色</span><span class="sxs-lookup"><span data-stu-id="13f85-128">Roles in Security Groups for Computers Running Your Service</span></span>

<span data-ttu-id="13f85-129">使用安全性群組來定義在目錄中被授與您服務物件存取權的電腦集合。</span><span class="sxs-lookup"><span data-stu-id="13f85-129">Use security groups to define the set of computers that are granted access to your service's objects in the directory.</span></span> <span data-ttu-id="13f85-130">例如，您的服務可能會與群組 MyService 伺服器相關聯。</span><span class="sxs-lookup"><span data-stu-id="13f85-130">For example, your service may be associated with a group MyService Servers.</span></span> <span data-ttu-id="13f85-131">所有執行 MyService 伺服器的電腦都會新增至 MyService Servers 群組，然後此群組就可以存取 MyService 伺服器需要讀取/寫入資料的目錄部分。</span><span class="sxs-lookup"><span data-stu-id="13f85-131">All computers running the MyService server are added to MyService Servers group and this group can then be given access to parts of the directory where MyService servers need to read/write data.</span></span> <span data-ttu-id="13f85-132">MyService 的安裝程式可以在目錄上設定 Acl，讓 MyService 伺服器有足夠的許可權可讀取/寫入 MyService 相關的屬性，或建立 MyService 特定的物件。</span><span class="sxs-lookup"><span data-stu-id="13f85-132">The setup program for MyService can set ACLs on the directory to enable MyService Servers sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

 

 





