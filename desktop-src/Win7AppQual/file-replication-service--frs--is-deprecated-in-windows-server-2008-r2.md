---
description: Windows Server 2008 R2 中的檔案複寫服務 (FRS) 已淘汰
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Windows Server 2008 R2 中的檔案複寫服務 (FRS) 已淘汰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088366"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a><span data-ttu-id="5fbcf-103">Windows Server 2008 R2 中的檔案複寫服務 (FRS) 已淘汰</span><span class="sxs-lookup"><span data-stu-id="5fbcf-103">File Replication Service (FRS) Is Deprecated in Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="5fbcf-104">平台</span><span class="sxs-lookup"><span data-stu-id="5fbcf-104">Platform</span></span>

 <span data-ttu-id="5fbcf-105">**伺服器-** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5fbcf-105">**Servers -** Windows Server 2008 R2</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="5fbcf-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="5fbcf-106">Feature Impact</span></span>

 <span data-ttu-id="5fbcf-107">**嚴重性-** 高</span><span class="sxs-lookup"><span data-stu-id="5fbcf-107">**Severity -** High</span></span>  
<span data-ttu-id="5fbcf-108">**頻率-** 高</span><span class="sxs-lookup"><span data-stu-id="5fbcf-108">**Frequency -** High</span></span>  


## <a name="description"></a><span data-ttu-id="5fbcf-109">Description</span><span class="sxs-lookup"><span data-stu-id="5fbcf-109">Description</span></span>

<span data-ttu-id="5fbcf-110">在 Windows Server 2008 R2 中， (FRS) 的檔案複寫服務無法用於複寫分散式檔案系統 (DFS) 資料夾或自訂 (非 SYSVOL) 資料。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-110">In Windows Server 2008 R2, File Replication Service (FRS) cannot be used for replicating Distributed File System (DFS) folders or custom (non-SYSVOL) data.</span></span> <span data-ttu-id="5fbcf-111">Windows Server 2008 R2 網域控制站仍可使用 FRS 來複寫網域中使用 FRS 來複寫網域控制站之間 SYSVOL 共用的 SYSVOL 共用內容。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-111">A Windows Server 2008 R2 domain controller can still use FRS to replicate the contents of the SYSVOL share in a domain that uses FRS for replicating the SYSVOL share between domain controllers.</span></span> <span data-ttu-id="5fbcf-112">不過，Windows Server 2008 R2 伺服器無法使用 FRS 來複寫 SYSVOL 共用以外的任何複本集的內容。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-112">However, Windows Server 2008 R2 servers cannot use FRS to replicate the contents of any replica set apart from the SYSVOL share.</span></span> <span data-ttu-id="5fbcf-113">DFS 複寫服務是 FRS 的替代方案，可用來複寫 SYSVOL 共用、DFS 資料夾，以及其他自訂 (非 SYSVOL) 資料的內容。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-113">The DFS Replication service is a replacement for FRS and can be used to replicate the contents of the SYSVOL share, DFS folders as well as other custom (non-SYSVOL) data.</span></span> <span data-ttu-id="5fbcf-114">將所有非 SYSVOL 的 FRS 複本集遷移至 DFS 複寫。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-114">Migrate all non-SYSVOL FRS replica sets to DFS Replication.</span></span> <span data-ttu-id="5fbcf-115">我們也強烈建議您將 SYSVOL 共用的複寫從 FRS 遷移至 DFS 複寫，因為 DFS 複寫更健全、可調整規模，且複寫效能比 FRS 更好。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-115">We also highly recommend that you migrate replication of the SYSVOL share from FRS to DFS Replication because DFS Replication is more robust, scalable and has better replication performance than FRS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="5fbcf-116">表現</span><span class="sxs-lookup"><span data-stu-id="5fbcf-116">Manifestation</span></span>

<span data-ttu-id="5fbcf-117">自訂資料的 FRS 複寫會在就地升級時中斷將失效。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-117">FRS replication of custom data will break irreversibly upon in-place upgrade.</span></span> <span data-ttu-id="5fbcf-118">從這種情況復原的唯一方法是在伺服器上重新安裝較舊的作業系統，然後重新初始化 FRS 複寫。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-118">The only way to recover from this situation would be to reinstall an older operating system on the server and reinitialize FRS replication.</span></span> <span data-ttu-id="5fbcf-119">升級至 Windows Server 2008 R2 的伺服器不能參與現有的 FRS 複寫群組。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-119">Servers that have been upgraded to Windows Server 2008 R2 are not allowed to participate in existing FRS replication groups.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="5fbcf-120">影響緩和措施</span><span class="sxs-lookup"><span data-stu-id="5fbcf-120">Mitigation of Impact</span></span>

<span data-ttu-id="5fbcf-121">為了避免因這些變更而發生的問題，請將自訂的 FRS 複寫集遷移至 DFS 複寫。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-121">To prevent issues that might occur as a result of these changes, migrate custom FRS replication sets to DFS Replication.</span></span> <span data-ttu-id="5fbcf-122">DFS 複寫服務在 FRS 方面有許多優點，包括改良的管理工具、更高的效能和委派的管理。</span><span class="sxs-lookup"><span data-stu-id="5fbcf-122">The DFS Replication service has many benefits over FRS, including improved management tools, higher performance, and delegated management.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="5fbcf-123">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="5fbcf-123">Links to Other Resources</span></span>

-   <span data-ttu-id="5fbcf-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="5fbcf-124">[FRS Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))</span></span>
-   [<span data-ttu-id="5fbcf-125">分散式檔案系統複寫：常見問題集</span><span class="sxs-lookup"><span data-stu-id="5fbcf-125">Distributed File System Replication: Frequently Asked Questions</span></span>](/windows-server/storage/dfs-replication/dfsr-faq)
-   [<span data-ttu-id="5fbcf-126">SYSVOL 複寫遷移指南： FRS 至 DFS 複寫</span><span class="sxs-lookup"><span data-stu-id="5fbcf-126">SYSVOL Replication Migration Guide: FRS to DFS Replication</span></span>](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
