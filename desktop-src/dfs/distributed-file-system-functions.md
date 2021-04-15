---
title: 分散式檔案系統函式
description: 以下是分散式檔案系統 (DFS) 函式的功能。
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468469"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="97297-103">分散式檔案系統函式</span><span class="sxs-lookup"><span data-stu-id="97297-103">Distributed File System Functions</span></span>

<span data-ttu-id="97297-104">以下是分散式檔案系統 (DFS) 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="97297-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="97297-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="97297-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="97297-106">NetDfsAdd</span><span class="sxs-lookup"><span data-stu-id="97297-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="97297-107">建立新的分散式檔案系統 (DFS) 連結，或將目標新增至 DFS 命名空間中的現有連結。</span><span class="sxs-lookup"><span data-stu-id="97297-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-108">NetDfsAddFtRoot</span><span class="sxs-lookup"><span data-stu-id="97297-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="97297-109">建立以網域為基礎的新分散式檔案系統 (DFS) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="97297-110">如果命名空間已存在，則函式會將指定的根目標新增至該命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-111">NetDfsAddRootTarget</span><span class="sxs-lookup"><span data-stu-id="97297-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="97297-112">建立網域型或獨立 DFS 命名空間，或將新的根目標新增至現有網域型命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-113">NetDfsAddStdRoot</span><span class="sxs-lookup"><span data-stu-id="97297-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="97297-114">建立新的獨立分散式檔案系統 (DFS) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-115">NetDfsEnum</span><span class="sxs-lookup"><span data-stu-id="97297-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="97297-116">列舉伺服器上裝載的分散式檔案系統 (DFS) 命名空間，或是由伺服器主控之命名空間的 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="97297-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-117">NetDfsGetClientInfo</span><span class="sxs-lookup"><span data-stu-id="97297-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="97297-118">從 DFS 用戶端所維護的快取中，抓取分散式檔案系統 (DFS) 根目錄或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97297-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-119">NetDfsGetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="97297-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="97297-120">針對指定 Active Directory 網域中的網域型 DFS 命名空間，抓取容器物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="97297-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-121">NetDfsGetInfo</span><span class="sxs-lookup"><span data-stu-id="97297-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="97297-122">抓取 DFS 命名空間中指定的分散式檔案系統 (DFS) 根目錄或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97297-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-123">NetDfsGetSecurity</span><span class="sxs-lookup"><span data-stu-id="97297-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="97297-124">抓取指定 DFS 命名空間之根物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="97297-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-125">NetDfsGetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="97297-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="97297-126">抓取指定獨立 DFS 命名空間之容器物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="97297-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-127">NetDfsGetSupportedNamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="97297-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="97297-128">判斷支援的中繼資料版本號碼。</span><span class="sxs-lookup"><span data-stu-id="97297-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-129">NetDfsMove</span><span class="sxs-lookup"><span data-stu-id="97297-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="97297-130">重新命名或移動 DFS 連結。</span><span class="sxs-lookup"><span data-stu-id="97297-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-131">NetDfsRemove</span><span class="sxs-lookup"><span data-stu-id="97297-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="97297-132">移除 dfs 命名空間中 dfs 連結的分散式檔案系統 (DFS) 連結或特定連結目標。</span><span class="sxs-lookup"><span data-stu-id="97297-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="97297-133">移除特定連結目標時，如果已移除連結的最後一個連結目標，則會移除連結本身。</span><span class="sxs-lookup"><span data-stu-id="97297-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-134">NetDfsRemoveFtRoot</span><span class="sxs-lookup"><span data-stu-id="97297-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="97297-135">從以網域為基礎的分散式檔案系統中移除指定的根目標 (DFS) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="97297-136">如果要移除 DFS 命名空間的最後一個根目標，此函數也會刪除 DFS 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="97297-137">您可以刪除 DFS 命名空間，而不需要先刪除其中的所有連結。</span><span class="sxs-lookup"><span data-stu-id="97297-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-138">NetDfsRemoveFtRootForced</span><span class="sxs-lookup"><span data-stu-id="97297-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="97297-139">從網域分散式檔案系統 (DFS) 命名空間移除指定的根目標，即使根目標伺服器已離線也一樣。</span><span class="sxs-lookup"><span data-stu-id="97297-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="97297-140">如果要移除 DFS 命名空間的最後一個根目標，此函數也會刪除 DFS 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="97297-141">您可以刪除 DFS 命名空間，而不需要先刪除其中的所有連結。</span><span class="sxs-lookup"><span data-stu-id="97297-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="97297-142">[**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)函數不會更新 DFS 根目標伺服器上的登錄。</span><span class="sxs-lookup"><span data-stu-id="97297-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="97297-143">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="97297-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-144">NetDfsRemoveRootTarget</span><span class="sxs-lookup"><span data-stu-id="97297-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="97297-145">從以網域為基礎的 DFS 命名空間移除 DFS 根目標。</span><span class="sxs-lookup"><span data-stu-id="97297-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="97297-146">如果根目標是 DFS 命名空間中的最後一個根目標，此函式會移除 DFS 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="97297-147">此函式也可以用來移除獨立 DFS 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-148">NetDfsRemoveStdRoot</span><span class="sxs-lookup"><span data-stu-id="97297-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="97297-149">刪除獨立分散式檔案系統 (DFS) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="97297-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-150">NetDfsSetClientInfo</span><span class="sxs-lookup"><span data-stu-id="97297-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="97297-151">在 DFS 用戶端所維護的快取中，修改分散式檔案系統 (DFS) 根目錄或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97297-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-152">NetDfsSetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="97297-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="97297-153">針對指定之 Active Directory 網域中的網域型 DFS 命名空間，設定容器物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="97297-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-154">NetDfsSetInfo</span><span class="sxs-lookup"><span data-stu-id="97297-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="97297-155">設定或修改特定分散式檔案系統 (DFS) 根、根目標、連結或連結目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97297-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-156">NetDfsSetSecurity</span><span class="sxs-lookup"><span data-stu-id="97297-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="97297-157">設定指定 DFS 命名空間之根物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="97297-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="97297-158">NetDfsSetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="97297-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="97297-159">設定指定之獨立 DFS 命名空間之容器物件的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="97297-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="97297-160">請注意，叫用任何函式的應用程式可能會間接讓本機 DFS 命名空間伺服器服務函式呼叫，從該網域的 PDC 模擬器主機執行相關命名空間中繼資料的完整同步處理。</span><span class="sxs-lookup"><span data-stu-id="97297-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="97297-161">即使已針對該命名空間設定根擴充性模式，也可能會發生這項完整的同步處理。</span><span class="sxs-lookup"><span data-stu-id="97297-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
