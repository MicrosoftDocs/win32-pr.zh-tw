---
title: 應用程式目錄分割
description: 在 Windows Server 2003 中，Active Directory Domain Services 支援應用程式目錄磁碟分割。
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- 應用程式目錄分割廣告
- 應用程式目錄分割 AD，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023291"
---
# <a name="application-directory-partitions"></a><span data-ttu-id="f37be-105">應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="f37be-105">Application Directory Partitions</span></span>

<span data-ttu-id="f37be-106">在 Windows Server 2003 中，Active Directory Domain Services 支援應用程式目錄磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="f37be-106">In Windows Server 2003, Active Directory Domain Services support application directory partitions.</span></span> <span data-ttu-id="f37be-107">應用程式目錄分割可以包含任何類型物件的階層，但安全性主體除外，而且可以設定為複寫到樹系中的任何一組網域控制站。</span><span class="sxs-lookup"><span data-stu-id="f37be-107">An application directory partition can contain a hierarchy of any type of objects, except security principals, and can be configured to replicate to any set of domain controllers in the forest.</span></span> <span data-ttu-id="f37be-108">與網域分割不同的是，應用程式目錄分割不需要複寫到網域中的所有網域控制站，而且資料分割可以複寫到樹系中不同網域的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="f37be-108">Unlike a domain partition, an application directory partition is not required to replicate to all domain controllers in a domain and the partition can replicate to domain controllers in different domains of the forest.</span></span> <span data-ttu-id="f37be-109">如需應用程式目錄分割的詳細資訊，請參閱 [關於應用程式目錄](about-application-directory-partitions.md)分割。</span><span class="sxs-lookup"><span data-stu-id="f37be-109">For more information about application directory partitions, see [About Application Directory Partitions](about-application-directory-partitions.md).</span></span>

<span data-ttu-id="f37be-110">您可以建立應用程式目錄分割。</span><span class="sxs-lookup"><span data-stu-id="f37be-110">An application directory partition can be created.</span></span> <span data-ttu-id="f37be-111">使用標準的 ADSI、LDAP 和 [DirectoryServices](/dotnet/api/system.directoryservices) 作業來修改和刪除。</span><span class="sxs-lookup"><span data-stu-id="f37be-111">modified and deleted using standard ADSI, LDAP and [System.DirectoryServices](/dotnet/api/system.directoryservices) operations.</span></span> <span data-ttu-id="f37be-112">建立和修改應用程式目錄分割所需的安全性內容，與建立網域分割的方式相同。</span><span class="sxs-lookup"><span data-stu-id="f37be-112">The security context required to create and modify an application directory partition is the same as that for creating a domain partition.</span></span>

<span data-ttu-id="f37be-113">下列主題描述如何使用應用程式目錄分割：</span><span class="sxs-lookup"><span data-stu-id="f37be-113">The following topics describe how to work with application directory partitions:</span></span>

-   [<span data-ttu-id="f37be-114">應用程式目錄分割複寫</span><span class="sxs-lookup"><span data-stu-id="f37be-114">Application Directory Partition Replication</span></span>](application-directory-partition-replication.md)
-   [<span data-ttu-id="f37be-115">應用程式目錄分割安全性</span><span class="sxs-lookup"><span data-stu-id="f37be-115">Application Directory Partition Security</span></span>](application-directory-partition-security.md)
-   [<span data-ttu-id="f37be-116">建立應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="f37be-116">Creating an Application Directory Partition</span></span>](creating-an-application-directory-partition.md)
-   [<span data-ttu-id="f37be-117">刪除應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="f37be-117">Deleting an Application Directory Partition</span></span>](deleting-an-application-directory-partition.md)
-   [<span data-ttu-id="f37be-118">列舉樹系中的應用程式目錄分割</span><span class="sxs-lookup"><span data-stu-id="f37be-118">Enumerating Application Directory Partitions in a Forest</span></span>](enumerating-application-directory-partitions-in-a-forest.md)
-   [<span data-ttu-id="f37be-119">尋找應用程式目錄分割主機伺服器</span><span class="sxs-lookup"><span data-stu-id="f37be-119">Locating an Application Directory Partition Host Server</span></span>](locating-an-application-directory-partition-host-server.md)
-   [<span data-ttu-id="f37be-120">新增或刪除應用程式目錄分割複本</span><span class="sxs-lookup"><span data-stu-id="f37be-120">Adding or Deleting an Application Directory Partition Replica</span></span>](adding-or-deleting-an-application-directory-partition-replica.md)
-   [<span data-ttu-id="f37be-121">列舉應用程式目錄分割的複本</span><span class="sxs-lookup"><span data-stu-id="f37be-121">Enumerating Replicas of an Application Directory Partition</span></span>](enumerating-replicas-of-an-application-directory-partition.md)
-   [<span data-ttu-id="f37be-122">修改應用程式目錄分割設定</span><span class="sxs-lookup"><span data-stu-id="f37be-122">Modifying Application Directory Partition Configuration</span></span>](modifying-application-directory-partition-configuration.md)

 

 