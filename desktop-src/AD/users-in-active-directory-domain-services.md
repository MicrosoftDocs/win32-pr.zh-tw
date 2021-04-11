---
title: Active Directory Domain Services 中的使用者
description: Active Directory Domain Services 包含儲存網域、使用者、使用者群組和安全性資料的目錄服務。
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory 中的使用者
- 使用者、active directory 網域服務
- active directory 網域服務，使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10ad85f359cab6baf891df03f368f3e7da5974f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023211"
---
# <a name="users-in-active-directory-domain-services"></a><span data-ttu-id="10f82-106">Active Directory Domain Services 中的使用者</span><span class="sxs-lookup"><span data-stu-id="10f82-106">Users in Active Directory Domain Services</span></span>

<span data-ttu-id="10f82-107">Active Directory Domain Services 包含儲存網域、使用者、使用者群組和安全性資料的目錄服務。</span><span class="sxs-lookup"><span data-stu-id="10f82-107">Active Directory Domain Services includes a directory service that stores domain, user, user group, and security data.</span></span>

<span data-ttu-id="10f82-108">在 Windows NT 4.0 及更早版本上，您可以使用 [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd)、 [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum)、 [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel)等函數來管理使用者、使用者群組和其他網路專案。</span><span class="sxs-lookup"><span data-stu-id="10f82-108">On Windows NT 4.0 and earlier, you can use functions such as [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd), [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum), [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel), and so on, to manage users, user groups, and other network items.</span></span> <span data-ttu-id="10f82-109">在 Windows 2000 和更新版本的 Windows 上，ADSI 提供這些專案及其屬性的統一且安全的存取。</span><span class="sxs-lookup"><span data-stu-id="10f82-109">On Windows 2000 and later versions of Windows, ADSI provides uniform and secure access to these items and their properties.</span></span> <span data-ttu-id="10f82-110">請注意，ADSI 提供了 Windows NT 4.0 提供者，可讓您使用 ADSI 來管理 Windows NT 4.0 系統上的使用者、使用者群組和電腦。</span><span class="sxs-lookup"><span data-stu-id="10f82-110">Be aware that ADSI provides a Windows NT 4.0 provider that enables you to use ADSI to manage user, user groups, and computers on Windows NT 4.0 systems.</span></span> <span data-ttu-id="10f82-111">另外還有 Windows Server 2008 Enterprise (Server Core 安裝) 、Microsoft Exchange 5.5、Microsoft Internet information Server (IIS) 、Novell NetWare 目錄服務 (NDS) 和 Novell NetWare 3 的提供者。</span><span class="sxs-lookup"><span data-stu-id="10f82-111">There are also providers for Windows Server 2008 Enterprise (Server Core installation), Microsoft Exchange 5.5, Microsoft Internet Information Server (IIS), Novell NetWare Directory Services (NDS), and Novell NetWare 3.</span></span> <span data-ttu-id="10f82-112">也就是一組用來管理 Windows NT、NDS 和 NetWare 3 使用者和使用者群組的標準化方法。</span><span class="sxs-lookup"><span data-stu-id="10f82-112">That is, a single set of standardized methods for managing users and user groups for Windows NT, NDS, and NetWare 3.</span></span>

<span data-ttu-id="10f82-113">此外，Windows 2000 是多重主目錄。</span><span class="sxs-lookup"><span data-stu-id="10f82-113">In addition, Windows 2000 is a multi-master directory.</span></span> <span data-ttu-id="10f82-114">也就是說，您可以在任何網域控制站上，對使用者、使用者群組和其他儲存在目錄中的資料進行變更。</span><span class="sxs-lookup"><span data-stu-id="10f82-114">That is, changes to users, user groups, and other data stored in the directory can be made at any domain controller.</span></span> <span data-ttu-id="10f82-115">在 Windows 2000 中，您不需要找出網域主控站 (PDC) ，也不需要在 PDC 上進行使用者和使用者群組的變更。</span><span class="sxs-lookup"><span data-stu-id="10f82-115">On Windows 2000, you are not required to locate the primary domain controller (PDC) and make user and user group changes on the PDC.</span></span>

<span data-ttu-id="10f82-116">Windows 2000 也會在名為組織單位的網域內引進新的階層式命名空間， (OU) 。</span><span class="sxs-lookup"><span data-stu-id="10f82-116">Windows 2000 also introduces a new hierarchical namespace within a domain called an organizational unit (OU).</span></span> <span data-ttu-id="10f82-117">OU 可包含電腦、使用者、使用者群組和其他網路物件。</span><span class="sxs-lookup"><span data-stu-id="10f82-117">An OU can contain computers, users, user groups, and other network objects.</span></span> <span data-ttu-id="10f82-118">通常會基於管理目的而使用 OU 來將專案分組，例如委派系統管理許可權，並將原則指派給群組作為單一單位。</span><span class="sxs-lookup"><span data-stu-id="10f82-118">Usually, an OU is used for the purpose of grouping things for administrative purposes, such as delegating administrative rights and assigning policies to the group as a single unit.</span></span>

<span data-ttu-id="10f82-119">網域、Ou、使用者、使用者群組、電腦和其他網路專案會儲存為 Active Directory Domain Services 中的物件。</span><span class="sxs-lookup"><span data-stu-id="10f82-119">Domains, OUs, users, user groups, computers, and other network items are stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="10f82-120">在 Windows 2000 和更新版本的 Windows 中，您仍然會將使用者、使用者群組和電腦新增至網域。</span><span class="sxs-lookup"><span data-stu-id="10f82-120">In Windows 2000 and later versions of Windows, you still add users, user groups, and computers to a domain.</span></span> <span data-ttu-id="10f82-121">不過，您現在可以選擇將這些物件加入 OU 容器，或您想要新增的物件在其 **classSchema** 物件的 **possSuperiors** 屬性中定義的任何其他容器類型;這是物件的 **classSchema** 物件上的屬性，而這個屬性會限制可包含該物件的物件類型。</span><span class="sxs-lookup"><span data-stu-id="10f82-121">However, you now have the option of adding these objects to an OU container or any other type of container that the object you want to add defines in its **classSchema** object's **possSuperiors** attribute; this is an attribute on an object's **classSchema** object and this attribute restricts what types of objects can contain that object.</span></span>

 

 