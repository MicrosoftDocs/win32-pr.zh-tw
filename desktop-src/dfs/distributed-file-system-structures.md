---
description: 以下是分散式檔案系統 DFS 結構
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: 分散式檔案系統結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468472"
---
# <a name="distributed-file-system-structures"></a><span data-ttu-id="3a3b0-103">分散式檔案系統結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-103">Distributed File System Structures</span></span>

<span data-ttu-id="3a3b0-104">以下是 DFS) 結構的分散式檔案系統 (：</span><span class="sxs-lookup"><span data-stu-id="3a3b0-104">The following are the Distributed File System (DFS) structures:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3a3b0-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="3a3b0-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3a3b0-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span><span class="sxs-lookup"><span data-stu-id="3a3b0-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span></span>](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

<span data-ttu-id="3a3b0-107">搭配 [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) 控制程式代碼使用的輸入緩衝區</span><span class="sxs-lookup"><span data-stu-id="3a3b0-107">Input buffer used with the [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code</span></span>
</dd> <dt>

[<span data-ttu-id="3a3b0-108">_DFS_INFO_1 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-108">_DFS_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
<span data-ttu-id="3a3b0-109">包含分散式檔案系統 (DFS) 根目錄或連結的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-109">Contains the name of a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-110">_DFS_INFO_2 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-110">_DFS_INFO_2 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
<span data-ttu-id="3a3b0-111">包含分散式檔案系統 (DFS) 根或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-111">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="3a3b0-112">此結構包含根或連結的名稱、狀態和 DFS 目標數目。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-112">This structure contains the name, status, and number of DFS targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-113">_DFS_INFO_3 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-113">_DFS_INFO_3 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
<span data-ttu-id="3a3b0-114">包含分散式檔案系統 (DFS) 根或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-114">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="3a3b0-115">此結構包含名稱、狀態、DFS 目標數目，以及根或連結的每個目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-115">This structure contains the name, status, number of DFS targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-116">_DFS_INFO_4 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-116">_DFS_INFO_4 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
<span data-ttu-id="3a3b0-117">包含分散式檔案系統 (DFS) 根或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-117">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="3a3b0-118">此結構包含名稱、狀態、 **GUID**、超時時間、目標數目，以及根或連結的每個目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-118">This structure contains the name, status, **GUID**, time-out, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-119">_DFS_INFO_5 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-119">_DFS_INFO_5 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
<span data-ttu-id="3a3b0-120">包含分散式檔案系統 (DFS) 根或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-120">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="3a3b0-121">此結構包含名稱、狀態、 **GUID**、超時、命名空間/根/連結屬性、中繼資料大小，以及根或連結的目標數目。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-121">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-122">_DFS_INFO_6 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-122">_DFS_INFO_6 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
<span data-ttu-id="3a3b0-123">包含分散式檔案系統 (DFS) 根或連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-123">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="3a3b0-124">此結構包含名稱、狀態、 **GUID**、超時、命名空間/根/連結屬性、中繼資料大小、目標數目，以及每個根或連結目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-124">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-125">_DFS_INFO_7 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-125">_DFS_INFO_7 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
<span data-ttu-id="3a3b0-126">包含 DFS 命名空間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-126">Contains information about a DFS namespace.</span></span> <span data-ttu-id="3a3b0-127">此結構包含命名空間中繼資料的版本 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-127">This structure contains the version **GUID** for the metadata for the namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-128">_DFS_INFO_8 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-128">_DFS_INFO_8 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
<span data-ttu-id="3a3b0-129">包含根或連結的名稱、狀態、 **GUID**、超時、屬性旗標、中繼資料大小、DFS 目標資訊，以及連結重新分析點安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-129">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, and link reparse point security descriptor for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-130">_DFS_INFO_9 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-130">_DFS_INFO_9 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
<span data-ttu-id="3a3b0-131">包含名稱、狀態、 **GUID**、超時、屬性旗標、中繼資料大小、DFS 目標資訊、連結重新分析點安全描述項，以及根或連結的 DFS 目標清單。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-131">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, link reparse point security descriptor, and a list of DFS targets for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-132">_DFS_INFO_50 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-132">_DFS_INFO_50 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
<span data-ttu-id="3a3b0-133">包含現有 DFS 命名空間的 DFS 中繼資料版本和功能。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-133">Contains the DFS metadata version and capabilities of an existing DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-134">_DFS_INFO_100 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-134">_DFS_INFO_100 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
<span data-ttu-id="3a3b0-135">包含與分散式檔案系統 (DFS) 根或連結相關聯的批註。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-135">Contains a comment associated with a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-136">_DFS_INFO_101 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-136">_DFS_INFO_101 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
<span data-ttu-id="3a3b0-137">描述 DFS 根目錄、連結、根目標或連結目標上的儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-137">Describes the state of storage on a DFS root, link, root target, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-138">_DFS_INFO_102 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-138">_DFS_INFO_102 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
<span data-ttu-id="3a3b0-139">包含與指定的 DFS 根目錄中的分散式檔案系統 (DFS) 根目錄或連結相關聯的超時值。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-139">Contains a time-out value to associate with a Distributed File System (DFS) root or a link in a named DFS root.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-140">_DFS_INFO_103 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-140">_DFS_INFO_103 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
<span data-ttu-id="3a3b0-141">包含屬性，這些屬性會設定 DFS 根目錄或連結的特定行為。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-141">Contains properties that set specific behaviors for a DFS root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-142">_DFS_INFO_104 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-142">_DFS_INFO_104 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
<span data-ttu-id="3a3b0-143">包含 DFS 根目標或連結目標的優先順序。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-143">Contains the priority of a DFS root target or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-144">_DFS_INFO_105 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-144">_DFS_INFO_105 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
<span data-ttu-id="3a3b0-145">包含有關 DFS 根目錄或連結的資訊，包括批註、狀態、超時，以及屬性旗標所指定的 DFS 行為。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-145">Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-146">_DFS_INFO_106 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-146">_DFS_INFO_106 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
<span data-ttu-id="3a3b0-147">包含 DFS 根目標或連結目標的儲存狀態和優先順序。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-147">Contains the storage state and priority for a DFS root target or link target.</span></span> <span data-ttu-id="3a3b0-148">此結構只適用于 [**NetDfsSetInfo**](netdfssetinfo.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-148">This structure is only for use with the [**NetDfsSetInfo**](netdfssetinfo.md) function.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-149">_DFS_INFO_107 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-149">_DFS_INFO_107 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
<span data-ttu-id="3a3b0-150">包含有關 DFS 根目錄或連結的資訊，包括批註、狀態、超時、屬性旗標和連結重新分析點安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-150">Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-151">_DFS_INFO_150 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-151">_DFS_INFO_150 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
<span data-ttu-id="3a3b0-152">包含 DFS 連結的重新分析點的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-152">Contains the security descriptor for a DFS link's reparse point.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-153">_DFS_INFO_200 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-153">_DFS_INFO_200 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
<span data-ttu-id="3a3b0-154">包含以網域為基礎的分散式檔案系統名稱 (DFS) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-154">Contains the name of a domain-based Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-155">_DFS_INFO_300 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-155">_DFS_INFO_300 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
<span data-ttu-id="3a3b0-156">包含 DFS 命名空間 (網域型或獨立) 的名稱和類型。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-156">Contains the name and type (domain-based or stand-alone) of a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-157">_DFS_STORAGE_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-157">_DFS_STORAGE_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
<span data-ttu-id="3a3b0-158">包含 dfs 命名空間或 DFS 用戶端所維護的快取中，DFS 根目錄或連結目標的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-158">Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-159">_DFS_STORAGE_INFO_1 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-159">_DFS_STORAGE_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
<span data-ttu-id="3a3b0-160">包含 DFS 目標的相關資訊，包括 DFS 目標伺服器名稱和共用名稱，以及目標的狀態和優先順序。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-160">Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
<span data-ttu-id="3a3b0-162">包含 DFS 命名空間的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-162">Contains version information for a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="3a3b0-163">_DFS_TARGET_PRIORITY 結構</span><span class="sxs-lookup"><span data-stu-id="3a3b0-163">_DFS_TARGET_PRIORITY structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
<span data-ttu-id="3a3b0-164">包含特定 DFS 目標的優先順序類別和等級。</span><span class="sxs-lookup"><span data-stu-id="3a3b0-164">Contains the priority class and rank of a specific DFS target.</span></span>

</dd> </dl>
