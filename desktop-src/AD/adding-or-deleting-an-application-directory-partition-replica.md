---
title: 新增或刪除應用程式目錄分割複本
description: 應用程式目錄分割的第一個複本是在建立時系結至該磁碟分割的網域控制站上建立的。
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- 新增或刪除應用程式目錄分割複本 AD
- 應用程式目錄分割 AD、新增或刪除分割區複本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092643"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a><span data-ttu-id="2b858-105">新增或刪除應用程式目錄分割複本</span><span class="sxs-lookup"><span data-stu-id="2b858-105">Adding or Deleting an Application Directory Partition Replica</span></span>

<span data-ttu-id="2b858-106">應用程式目錄分割的第一個複本是在建立時系結至該磁碟分割的網域控制站上建立的。</span><span class="sxs-lookup"><span data-stu-id="2b858-106">The first replica of an application directory partition is created on the domain controller that was bound to it at creation time.</span></span> <span data-ttu-id="2b858-107">您可以在樹系中的任何網域控制站上建立額外的複本，而不一定要在與初始網域控制站相同的網域中建立。</span><span class="sxs-lookup"><span data-stu-id="2b858-107">Additional replicas can be created on any domain controller in the forest, not necessarily in the same domain as the initial domain controller.</span></span> <span data-ttu-id="2b858-108">應用程式目錄分割複本只能存在於執行 Windows Server 2003 或更新版本的網域控制站上。</span><span class="sxs-lookup"><span data-stu-id="2b858-108">An application directory partition replica can only exist on a domain controller that is running Windows Server 2003 or later.</span></span> <span data-ttu-id="2b858-109">如需詳細資訊，請參閱這篇有關 [分割區管理](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10))的 TechNet 文章。</span><span class="sxs-lookup"><span data-stu-id="2b858-109">For more information, see this TechNet article on [Partition Management](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).</span></span>

<span data-ttu-id="2b858-110">**若要新增應用程式目錄分割的複本，請執行下列步驟**</span><span class="sxs-lookup"><span data-stu-id="2b858-110">**To add a replica for an application directory partition, perform the following steps**</span></span>

1.  <span data-ttu-id="2b858-111">在 [資料分割] 容器中搜尋具有與應用程式目錄分割的辨別名稱相等的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件。</span><span class="sxs-lookup"><span data-stu-id="2b858-111">Search the Partitions container for a [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that has an [**nCName**](/windows/desktop/ADSchema/a-ncname) attribute value that is equal to the distinguished name of the application directory partition.</span></span>
2.  <span data-ttu-id="2b858-112">系結至已啟用委派的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。</span><span class="sxs-lookup"><span data-stu-id="2b858-112">Bind to the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object with delegation enabled.</span></span> <span data-ttu-id="2b858-113">這是必要的，因為只能在 Domain-Naming FSMO 角色持有者上修改 **交叉引用** 物件。</span><span class="sxs-lookup"><span data-stu-id="2b858-113">This is required because the **crossRef** object can only be modified on the Domain-Naming FSMO role holder.</span></span> <span data-ttu-id="2b858-114">在啟用委派的情況下，網域控制站可以使用相同的認證來與 Domain-Naming FSMO 角色持有者聯繫。</span><span class="sxs-lookup"><span data-stu-id="2b858-114">With delegation enabled, the domain controller can contact the Domain-Naming FSMO role holder using the same credentials.</span></span>
3.  <span data-ttu-id="2b858-115">針對將裝載新複本的網域控制站，將 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa)物件的辨別名稱加入至 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [自 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性。</span><span class="sxs-lookup"><span data-stu-id="2b858-115">Add the distinguished name of the [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) object for the domain controller that will host the new replica to the [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) attribute of the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object.</span></span>

<span data-ttu-id="2b858-116">當新的「高階 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) 」屬性值複寫至將裝載應用程式目錄分割複本的新網域控制站時，系統會觸發 KCC 將應用程式目錄分割複寫到目標網域控制站。</span><span class="sxs-lookup"><span data-stu-id="2b858-116">When the new [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) attribute value is replicated to the new domain controller that will host a replica of the application directory partition, the KCC will be triggered to replicate the application directory partition to the target domain controller.</span></span>

<span data-ttu-id="2b858-117">若要移除應用程式目錄分割的複本，請執行上述相同步驟，以找出代表應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件，並從 **交叉引用** 物件的 [使用 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性中移除對應至網域控制站的值。</span><span class="sxs-lookup"><span data-stu-id="2b858-117">To remove a replica for an application directory partition, perform the same steps above to locate the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object that represents the application directory partition and remove the value that corresponds to the domain controller from the [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) attribute of the **crossRef** object.</span></span>

<span data-ttu-id="2b858-118">當新的「高階 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) 」屬性值複寫到將不再裝載應用程式目錄分割複本的網域控制站時，系統將會觸發 KCC，以移除目標網域控制站上的應用程式目錄分割複本。</span><span class="sxs-lookup"><span data-stu-id="2b858-118">When the new [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) attribute value is replicated to the domain controller that will no longer host a replica of the application directory partition, the KCC will be triggered to remove the replica of the application directory partition on the target domain controller.</span></span>

<span data-ttu-id="2b858-119">如果已移除或降級裝載應用程式目錄分割複本的網域控制站，Active Directory 伺服器將會自動從所有 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [使用中- [**-----**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) -----------------------replica-</span><span class="sxs-lookup"><span data-stu-id="2b858-119">If a domain controller that is hosting an application directory partition replica is removed or demoted, the Active Directory server will automatically remove the value corresponding to the domain controller from the [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) attribute of all [**crossRef**](/windows/desktop/ADSchema/c-crossref) objects.</span></span>

 

 