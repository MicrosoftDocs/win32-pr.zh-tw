---
description: 本主題說明如何判斷 DFSR 或 FSR 是否複寫 SYSVOL 資料夾，並說明如何備份和還原 FRS 複寫的 SYSVOL 資料夾。
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: 備份和還原 FRS-Replicated SYSVOL 資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83ccbc156182a4a3b84c758cb22153f4f7110f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319867"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a><span data-ttu-id="ad112-103">備份和還原 FRS-Replicated SYSVOL 資料夾</span><span class="sxs-lookup"><span data-stu-id="ad112-103">Backing Up and Restoring an FRS-Replicated SYSVOL Folder</span></span>

<span data-ttu-id="ad112-104">系統磁碟區 (SYSVOL) 資料夾提供儲存 [群組原則](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) 物件和腳本重要元素的標準位置。</span><span class="sxs-lookup"><span data-stu-id="ad112-104">The System Volume (SYSVOL) folder provides a standard location to store important elements of [Group Policy](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) objects and scripts.</span></span> <span data-ttu-id="ad112-105">網域中的每個網域控制站上都有 SYSVOL 資料夾的複本。</span><span class="sxs-lookup"><span data-stu-id="ad112-105">A copy of the SYSVOL folder exists on each domain controller in a domain.</span></span> <span data-ttu-id="ad112-106">SYSVOL 資料夾是由 [分散式檔案系統複寫 (DFSR) ](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 或檔案複寫 [服務 (FRS) ](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10))複寫。</span><span class="sxs-lookup"><span data-stu-id="ad112-106">The SYSVOL folder is replicated by either [Distributed File System Replication (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) or the [File Replication Service (FRS)](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)).</span></span> <span data-ttu-id="ad112-107">本主題說明如何判斷 DFSR 或 FSR 是否複寫 SYSVOL 資料夾，並說明如何備份和還原 FRS 複寫的 SYSVOL 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-107">This topic explains how to determine whether a SYSVOL folder is replicated by DFSR or FSR and explains how to backup and restore an FRS-replicated SYSVOL folder.</span></span>

<span data-ttu-id="ad112-108">FRS 可將 SYSVOL 內容複寫到網域內的其他網域控制站。</span><span class="sxs-lookup"><span data-stu-id="ad112-108">FRS can copy SYSVOL contents to other domain controllers within the domain.</span></span> <span data-ttu-id="ad112-109">FRS 會監視 SYSVOL 資料夾，如果儲存在 SYSVOL 資料夾上的任何檔案發生變更，FRS 就會自動將變更的檔案複寫到網域中其他網域控制站上的 SYSVOL 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-109">FRS monitors the SYSVOL folder and, if a change occurs to any file stored on the SYSVOL folder, then FRS automatically replicates the changed file to the SYSVOL folders on the other domain controllers in the domain.</span></span>

> [!Note]  
> <span data-ttu-id="ad112-110">藉由複寫 SYSVOL 資料夾的內容，只會複寫群組原則範本。</span><span class="sxs-lookup"><span data-stu-id="ad112-110">Only the Group Policy template is replicated by replicating the contents of the SYSVOL folder.</span></span> <span data-ttu-id="ad112-111">群組原則的容器會透過 Active Directory 複寫進行複寫。</span><span class="sxs-lookup"><span data-stu-id="ad112-111">The Group Policy container is replicated through Active Directory replication.</span></span> <span data-ttu-id="ad112-112">若要讓群組原則能夠順利運作，您必須在網域控制站上使用群組原則範本和群組原則容器。</span><span class="sxs-lookup"><span data-stu-id="ad112-112">For Group Policy to operate successfully, both the Group Policy template and the Group Policy container must be available on a domain controller.</span></span>

 

<span data-ttu-id="ad112-113">本主題涵蓋下列主題：</span><span class="sxs-lookup"><span data-stu-id="ad112-113">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="ad112-114">判斷網域控制站的 SYSVOL 資料夾是否由 DFSR 或 FRS 複寫</span><span class="sxs-lookup"><span data-stu-id="ad112-114">Determining Whether a Domain Controller's SYSVOL Folder is Replicated by DFSR or FRS</span></span>](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [<span data-ttu-id="ad112-115">備份 DFSR-Replicated SYSVOL 資料夾</span><span class="sxs-lookup"><span data-stu-id="ad112-115">Backing Up a DFSR-Replicated SYSVOL Folder</span></span>](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [<span data-ttu-id="ad112-116">備份 Windows Server 2008 或 Windows Server 2003 網域上的 FRS-Replicated SYSVOL 資料夾</span><span class="sxs-lookup"><span data-stu-id="ad112-116">Backing Up an FRS-Replicated SYSVOL Folder on a Windows Server 2008 or Windows Server 2003 Domain</span></span>](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [<span data-ttu-id="ad112-117">範例 FRS 寫入器元資料檔案</span><span class="sxs-lookup"><span data-stu-id="ad112-117">Sample FRS Writer Metadata Document</span></span>](#sample-frs-writer-metadata-document)
-   [<span data-ttu-id="ad112-118">設定用於還原 FRS-Replicated SYSVOL 資料夾的登錄機碼</span><span class="sxs-lookup"><span data-stu-id="ad112-118">Setting Registry Keys for a Restore of an FRS-Replicated SYSVOL Folder</span></span>](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [<span data-ttu-id="ad112-119">執行 FRS-Replicated SYSVOL 資料夾的非系統授權還原</span><span class="sxs-lookup"><span data-stu-id="ad112-119">Performing a Nonauthoritative Restore of an FRS-Replicated SYSVOL Folder</span></span>](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [<span data-ttu-id="ad112-120">執行 FRS-Replicated SYSVOL 資料夾的授權還原</span><span class="sxs-lookup"><span data-stu-id="ad112-120">Performing an Authoritative Restore of an FRS-Replicated SYSVOL Folder</span></span>](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a><span data-ttu-id="ad112-121">判斷網域控制站的 SYSVOL 資料夾是否由 DFSR 或 FRS 複寫</span><span class="sxs-lookup"><span data-stu-id="ad112-121">Determining Whether a Domain Controller's SYSVOL Folder is Replicated by DFSR or FRS</span></span>

<span data-ttu-id="ad112-122">下表摘要說明如何判斷 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 或 FRS 是否正在複寫網域控制站的 SYSVOL 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-122">The following table summarizes how to determine whether a domain controller's SYSVOL folder is being replicated by [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) or FRS.</span></span>

| <span data-ttu-id="ad112-123">如果網域控制站正在執行</span><span class="sxs-lookup"><span data-stu-id="ad112-123">If the domain controller is running</span></span>                                                                                                                  | <span data-ttu-id="ad112-124">SYSVOL 的複寫方式</span><span class="sxs-lookup"><span data-stu-id="ad112-124">SYSVOL is replicated by</span></span> |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="ad112-125">Windows server 2008 + Windows Server 2008 + [SYSVOL 遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) 的網域功能等級已完成</span><span class="sxs-lookup"><span data-stu-id="ad112-125">Windows Server 2008 + domain functional level of Windows Server 2008 + [SYSVOL migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) completed</span></span> | <span data-ttu-id="ad112-126">DFSR</span><span class="sxs-lookup"><span data-stu-id="ad112-126">DFSR</span></span>                    |
| <span data-ttu-id="ad112-127">Windows server 2008 + 網域功能等級低於 Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad112-127">Windows Server 2008 + domain functional level below Windows Server 2008</span></span>                                                                              | <span data-ttu-id="ad112-128">Frs</span><span class="sxs-lookup"><span data-stu-id="ad112-128">FRS</span></span>                     |
| <span data-ttu-id="ad112-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ad112-129">Windows Server 2003</span></span>                                                                                                                                  | <span data-ttu-id="ad112-130">Frs</span><span class="sxs-lookup"><span data-stu-id="ad112-130">FRS</span></span>                     |



 

<span data-ttu-id="ad112-131">如果網域的 [功能等級](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) 為 Windows Server 2008 且網域已通過 [SYSVOL 遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)，則會使用 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 來複寫 sysvol 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-131">If the domain's [functional level](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) is Windows Server 2008 and the domain has undergone [SYSVOL migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx), [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) will be used to replicate the SYSVOL folder.</span></span> <span data-ttu-id="ad112-132">如果網域中的第一個網域控制站直接升級為 Windows Server 2008 [功能等級](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))，則會自動使用 DFSR 進行 SYSVOL 複寫。</span><span class="sxs-lookup"><span data-stu-id="ad112-132">If the first domain controller in the domain was promoted directly into the Windows Server 2008 [functional level](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)), DFSR is automatically used for SYSVOL replication.</span></span> <span data-ttu-id="ad112-133">在這種情況下，不需要將 SYSVOL 複寫從 FRS 遷移至 DFSR。</span><span class="sxs-lookup"><span data-stu-id="ad112-133">In such cases, there is no need for migration of SYSVOL replication from FRS to DFSR.</span></span> <span data-ttu-id="ad112-134">如果網域已升級為 Windows Server 2008 [功能等級](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))，則會使用 FRS 進行 SYSVOL 複寫，直到從 FRS 到 DFSR 的 [遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) 程式完成為止。</span><span class="sxs-lookup"><span data-stu-id="ad112-134">If the domain was upgraded to Windows Server 2008 [functional level](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)), FRS is used for SYSVOL replication until the [migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) process from FRS to DFSR is complete.</span></span>

<span data-ttu-id="ad112-135">若要判斷是否正在執行 Windows Server 2008 的網域控制站上使用 DFSR 或 FRS，請檢查 [ **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** 參數] 的值 SysVols 是否正在 \\  \\  \\ **遷移 SysVols** \\ **LocalState** 登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="ad112-135">To determine whether DFSR or FRS is being used on a domain controller that is running Windows Server 2008, check the value of the **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**DFSR**\\**Parameters**\\**SysVols**\\**Migrating Sysvols**\\**LocalState** registry subkey.</span></span> <span data-ttu-id="ad112-136">如果此登錄子機碼存在，且其值設為 3 (會消除) ，則會使用 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 。</span><span class="sxs-lookup"><span data-stu-id="ad112-136">If this registry subkey exists and its value is set to 3 (ELIMINATED), [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) is being used.</span></span> <span data-ttu-id="ad112-137">如果子機碼不存在，或其具有不同的值，則會使用 FRS。</span><span class="sxs-lookup"><span data-stu-id="ad112-137">If the subkey does not exist, or if it has a different value, FRS is being used.</span></span>

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a><span data-ttu-id="ad112-138">備份 DFSR-Replicated SYSVOL 資料夾</span><span class="sxs-lookup"><span data-stu-id="ad112-138">Backing Up a DFSR-Replicated SYSVOL Folder</span></span>

<span data-ttu-id="ad112-139">如果 [dfsr](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)複寫 SYSVOL 資料夾，則可以使用 dfsr VSS 寫入器進行備份。</span><span class="sxs-lookup"><span data-stu-id="ad112-139">If the SYSVOL folder is replicated by [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr), the DFSR VSS writer can be used to back it up.</span></span> <span data-ttu-id="ad112-140">如需有關 DFSR VSS 寫入器的詳細資訊，請參閱 [dfsr 複寫資料夾](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)。</span><span class="sxs-lookup"><span data-stu-id="ad112-140">For more information about the DFSR VSS writer, see [DFSR Replicated Folders](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).</span></span>

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a><span data-ttu-id="ad112-141">備份 Windows Server 2008 或 Windows Server 2003 網域上的 FRS-Replicated SYSVOL 資料夾</span><span class="sxs-lookup"><span data-stu-id="ad112-141">Backing Up an FRS-Replicated SYSVOL Folder on a Windows Server 2008 or Windows Server 2003 Domain</span></span>

<span data-ttu-id="ad112-142">在執行 Windows Server 2008 或 Windows Server 2003 的網域控制站上，會有 VSS 基礎結構，因此 FRS VSS 寫入器可以用來備份 SYSVOL 資料夾和 FRS 元件。</span><span class="sxs-lookup"><span data-stu-id="ad112-142">On a domain controller that is running Windows Server 2008 or Windows Server 2003, the VSS infrastructure is present, and therefore the FRS VSS writer can be used to back up the SYSVOL folder and FRS components.</span></span>

<span data-ttu-id="ad112-143">FRS VSS 寫入器的寫入器元資料檔案提供 SYSVOL 資料夾的位置和寫入器排除清單的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad112-143">The FRS VSS writer's Writer Metadata Document provides information about the location of the SYSVOL folder and the exclusion lists for the writer.</span></span> <span data-ttu-id="ad112-144">根據此資訊， (要求者) 的 VSS 備份應用程式可以使用定期以 VSS 為基礎的備份技術來備份 SYSVOL 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-144">Based on this information, a VSS backup application (requester) can back up the SYSVOL folder using the regular VSS-based backup techniques.</span></span>

<span data-ttu-id="ad112-145">寫入器元資料檔案包含寫入器的相關資訊、寫入器擁有的資料，以及如何還原該資料。</span><span class="sxs-lookup"><span data-stu-id="ad112-145">The Writer Metadata Document contains information about the writer, the data that the writer owns, and how to restore that data.</span></span> <span data-ttu-id="ad112-146">這是唯讀檔案，可以在進行備份之前，由備份應用程式取出。</span><span class="sxs-lookup"><span data-stu-id="ad112-146">This is a read-only document that can be retrieved by the backup application before taking a backup.</span></span> <span data-ttu-id="ad112-147">[DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11))工具可以用來查看 FRS VSS 寫入器的寫入器元資料檔案。</span><span class="sxs-lookup"><span data-stu-id="ad112-147">The [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) tool can be used to view the FRS VSS writer's Writer Metadata Document.</span></span> <span data-ttu-id="ad112-148">[DiskShadow 清單寫入](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11))器命令會提供有關系統上的寫入器的資訊。</span><span class="sxs-lookup"><span data-stu-id="ad112-148">The [DiskShadow list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) command provides information about the writers present on the system.</span></span> <span data-ttu-id="ad112-149">這份清單包含有關網域控制站上使用 FRS 進行 SYSVOL 複寫的網域控制站上的 FRS 寫入器的資訊，或是使用 FRS 複寫 [DFS 連結目標](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10))的檔案伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad112-149">This list contains information about the FRS writer on domain controllers that use FRS for SYSVOL replication or on file servers that use FRS for replication of [DFS link targets](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10)).</span></span>

<span data-ttu-id="ad112-150">下列範例 FRS 寫入器元資料檔案章節針對在 D： Windows sysvol 上具有 SYSVOL 資料夾的網域控制站，顯示範例 FRS 寫入器元資料檔案 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="ad112-150">The following Sample FRS Writer Metadata Document section shows a sample FRS Writer Metadata Document for a domain controller that has the SYSVOL folder on D:\\Windows\\Sysvol.</span></span> <span data-ttu-id="ad112-151">[排除的檔案] 區段中顯示的路徑將與查詢 Netlogon 服務的 **SysVol** 登錄機碼時所取得的路徑相同：</span><span class="sxs-lookup"><span data-stu-id="ad112-151">The path shown in the "Excluded files" section will be the same as that obtained when querying the Netlogon service's **SysVol** registry key:</span></span>

<span data-ttu-id="ad112-152">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NetLogon** \\ **參數** \\ **SysVol**</span><span class="sxs-lookup"><span data-stu-id="ad112-152">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NetLogon**\\**Parameters**\\**SysVol**</span></span>

<span data-ttu-id="ad112-153">當網域控制站處於 [SYSVOL 遷移](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)的重新導向狀態時，就會發生此規則的唯一例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ad112-153">The only exception to this rule occurs when the domain controller is in the REDIRECTED state of [SYSVOL migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx).</span></span> <span data-ttu-id="ad112-154">在此狀態中，對應至 FRS 和 [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 服務的寫入器會報告其各自的 SYSVOL 資料夾複本。</span><span class="sxs-lookup"><span data-stu-id="ad112-154">In this state, the writers corresponding to both FRS and the [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) service report their respective copies of the SYSVOL folder.</span></span> <span data-ttu-id="ad112-155">不過， [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) 服務的 SYSVOL 資料夾複本 (通常是一個名為 sysvol DFSR 的資料夾， \_) 是網域控制站所共用的資料夾。此路徑是 **sysvol** 登錄機碼所參考的路徑。</span><span class="sxs-lookup"><span data-stu-id="ad112-155">However, the [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) service's copy of the SYSVOL folder (usually a folder called SYSVOL\_DFSR) is the one that is shared by the domain controller; this path is the one referenced by the **SysVol** registry key.</span></span>

<span data-ttu-id="ad112-156">FRS VSS 寫入器需要自訂的還原方法。</span><span class="sxs-lookup"><span data-stu-id="ad112-156">The FRS VSS writer requires a custom restore method.</span></span> <span data-ttu-id="ad112-157">這表示在還原由 FRS 複寫的檔案時，必須執行特定的自訂步驟。</span><span class="sxs-lookup"><span data-stu-id="ad112-157">This means that certain custom steps must be performed when restoring files that are being replicated by FRS.</span></span> <span data-ttu-id="ad112-158">如需詳細資訊，請參閱執行 FRS-Replicated SYSVOL 資料夾的非系統授權還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-158">For more information, see Performing a Nonauthoritative Restore of an FRS-Replicated SYSVOL Folder.</span></span>

> [!Note]  
> <span data-ttu-id="ad112-159">Windows 網域控制站的系統狀態備份不包含 FRS 資料庫，此資料庫會維護與 SYSVOL 資料夾內的檔案相關之 FRS 服務的狀態資訊，以及其他內容集。</span><span class="sxs-lookup"><span data-stu-id="ad112-159">System state backups for Windows domain controllers do not include the FRS database that maintains state information for the FRS service pertaining to the files within the SYSVOL folder and other content sets.</span></span> <span data-ttu-id="ad112-160">系統狀態備份會排除 FRS 資料庫、調試記錄、暫存區域檔案，以及 [預先存在之資料檔案夾](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) 中的檔案。</span><span class="sxs-lookup"><span data-stu-id="ad112-160">The FRS database, debug logs, staging area files, and files in the [pre-existing data folder](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) are excluded from a system state backup.</span></span> <span data-ttu-id="ad112-161">下列範例 FRS 寫入器規格包含 [排除的檔案] 區段中的排除清單。</span><span class="sxs-lookup"><span data-stu-id="ad112-161">The following sample FRS writer specification contains the exclusion list in the "Excluded files" section.</span></span>

 

## <a name="sample-frs-writer-metadata-document"></a><span data-ttu-id="ad112-162">範例 FRS 寫入器元資料檔案</span><span class="sxs-lookup"><span data-stu-id="ad112-162">Sample FRS Writer Metadata Document</span></span>

<span data-ttu-id="ad112-163">以下是網域控制站的範例 FRS 寫入器元資料檔案，其 SYSVOL 資料夾路徑為 D： \\ Windows \\ SYSVOL。</span><span class="sxs-lookup"><span data-stu-id="ad112-163">The following is a sample FRS Writer Metadata Document for a domain controller whose SYSVOL folder path is D:\\Windows\\Sysvol.</span></span>

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a><span data-ttu-id="ad112-164">設定用於還原 FRS-Replicated SYSVOL 資料夾的登錄機碼</span><span class="sxs-lookup"><span data-stu-id="ad112-164">Setting Registry Keys for a Restore of an FRS-Replicated SYSVOL Folder</span></span>

<span data-ttu-id="ad112-165">**BurFlags** 登錄機碼可用來在 DFS 或 SYSVOL 複本集的 FRS 成員上執行權威或非系統授權還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-165">The **BurFlags** registry key is used to perform authoritative or nonauthoritative restores on FRS members of DFS or SYSVOL replica sets.</span></span> <span data-ttu-id="ad112-166">Global (整個電腦的) **BurFlags** 登錄機碼包含 REG \_ DWORD 值，而且位於登錄中的下列位置：</span><span class="sxs-lookup"><span data-stu-id="ad112-166">The global (computer-wide) **BurFlags** registry key contains REG\_DWORD values and is located in the following location in the registry:</span></span>

<span data-ttu-id="ad112-167">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **備份/還原** \\ **在啟動時的進程**</span><span class="sxs-lookup"><span data-stu-id="ad112-167">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NtFrs**\\**Parameters**\\**Backup/Restore**\\**Process at Startup**</span></span>

<span data-ttu-id="ad112-168">最常見的 **BurFlags** 登錄機碼值為：</span><span class="sxs-lookup"><span data-stu-id="ad112-168">The most common values for the **BurFlags** registry key are:</span></span>

-   <span data-ttu-id="ad112-169">D2，也稱為非系統授權模式還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-169">D2, also known as a nonauthoritative mode restore.</span></span>
-   <span data-ttu-id="ad112-170">D4，也稱為授權模式還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-170">D4, also known as an authoritative mode restore.</span></span>

<span data-ttu-id="ad112-171">有全域和複本集特定的 **BurFlags** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ad112-171">There are global and replica set-specific **BurFlags** registry keys.</span></span> <span data-ttu-id="ad112-172">設定 global **BurFlags** 登錄機碼會重新初始化成員持有的所有複本集。</span><span class="sxs-lookup"><span data-stu-id="ad112-172">Setting the global **BurFlags** registry key reinitializes all replica sets that the member holds.</span></span> <span data-ttu-id="ad112-173">當伺服器只保留一個複本集時，或它所保存的複本集相對較少且大小較小時，應設定此全域金鑰。</span><span class="sxs-lookup"><span data-stu-id="ad112-173">This global key should be set when the server holds only one replica set, or when the replica sets that it holds are relatively few in number and small in size.</span></span> <span data-ttu-id="ad112-174">例如，如果伺服器是網域控制站，而該控制器未裝載使用 SYSVOL 資料夾以外的 FRS 複寫的任何內容集，則可以設定全域 **BurFlags** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ad112-174">For example, if the server is a domain controller that does not host any content sets that are replicated using FRS other than the SYSVOL folder, the global **BurFlags** registry key can be set.</span></span>

<span data-ttu-id="ad112-175">全域 **BurFlags** 登錄機碼可在登錄中的下列位置找到：</span><span class="sxs-lookup"><span data-stu-id="ad112-175">The global **BurFlags** registry key is found in the following location in the registry:</span></span>

<span data-ttu-id="ad112-176">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **備份/還原** \\ **在啟動時的進程**</span><span class="sxs-lookup"><span data-stu-id="ad112-176">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NtFrs**\\**Parameters**\\**Backup/Restore**\\**Process At Startup**</span></span>

<span data-ttu-id="ad112-177">相較于全域 **BurFlags** 索引鍵，複本集特定的 **BurFlags** 索引鍵允許重新初始化離散的個別複本集，讓狀況良好的複寫集保持不變。</span><span class="sxs-lookup"><span data-stu-id="ad112-177">In contrast to the global **BurFlags** key, the replica set-specific **BurFlags** key permits the re-initialization of discrete, individual replica sets, allowing healthy replication sets to be left intact.</span></span>

<span data-ttu-id="ad112-178">您可以藉由決定該特定複本集的 GUID，找出複本集特定的 **BurFlags** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ad112-178">Replica set-specific **BurFlags** registry keys can be located by determining the GUID for that particular replica set.</span></span>

<span data-ttu-id="ad112-179">下列程式說明如何判斷哪個 GUID 對應至特定的複本集，並描述如何設定還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-179">The following procedure describes how to determine which GUID corresponds to a particular replica set and describes how to configure a restore.</span></span>

<span data-ttu-id="ad112-180">**判斷哪個 GUID 對應至特定的複本集和設定還原**</span><span class="sxs-lookup"><span data-stu-id="ad112-180">**To determine which GUID corresponds to a particular replica set and to configure a restore**</span></span>

1.  <span data-ttu-id="ad112-181">停止 FRS 服務。</span><span class="sxs-lookup"><span data-stu-id="ad112-181">Stop the FRS service.</span></span>
2.  <span data-ttu-id="ad112-182">若要判斷表示特定複本集的 GUID：</span><span class="sxs-lookup"><span data-stu-id="ad112-182">To determine the GUID that represents a particular replica set:</span></span>
    1.  <span data-ttu-id="ad112-183">在登錄中找出下列機碼。</span><span class="sxs-lookup"><span data-stu-id="ad112-183">Locate the following key in the registry.</span></span>

        <span data-ttu-id="ad112-184">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **複本集**</span><span class="sxs-lookup"><span data-stu-id="ad112-184">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NtFrs**\\**Parameters**\\**Replica Sets**</span></span>

    2.  <span data-ttu-id="ad112-185">在 [ **複本集** ] 子機碼底下，有一個或多個子機碼由 GUID 識別。</span><span class="sxs-lookup"><span data-stu-id="ad112-185">Below the **Replica Sets** subkey, there are one or more subkeys that are each identified by a GUID.</span></span>
    3.  <span data-ttu-id="ad112-186">每個 GUID 的 **複本集根目錄** 值都是檔案系統路徑，指出由此 GUID 表示的複本集。</span><span class="sxs-lookup"><span data-stu-id="ad112-186">The **Replica Set Root** value for each GUID is a file system path that indicates the replica set that is represented by this GUID.</span></span>
    4.  <span data-ttu-id="ad112-187">反復查看此 Guid 清單，直到找到所需的複本集為止。</span><span class="sxs-lookup"><span data-stu-id="ad112-187">Iterate over this list of GUIDs until the desired replica set is located.</span></span> <span data-ttu-id="ad112-188">請注意對應的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ad112-188">Note the corresponding GUID.</span></span>

3.  <span data-ttu-id="ad112-189">在登錄中找出下列子機碼：</span><span class="sxs-lookup"><span data-stu-id="ad112-189">Locate the following subkey in the registry:</span></span>

    <span data-ttu-id="ad112-190">**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **參數** \\ **累計複本集**</span><span class="sxs-lookup"><span data-stu-id="ad112-190">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NtFrs**\\**Parameters**\\**Cumulative Replica Sets**</span></span>

4.  <span data-ttu-id="ad112-191">在此子機碼底下，找出在步驟2中記下的相同 GUID。</span><span class="sxs-lookup"><span data-stu-id="ad112-191">Below this subkey, locate the same GUID that was noted in step 2.</span></span> <span data-ttu-id="ad112-192">在 GUID 子機碼底下，建立 **BurFlags** 索引鍵的專案。</span><span class="sxs-lookup"><span data-stu-id="ad112-192">Below the GUID subkey, create an entry for the **BurFlags** key.</span></span>
5.  <span data-ttu-id="ad112-193">重新開機 FRS 服務。</span><span class="sxs-lookup"><span data-stu-id="ad112-193">Restart the FRS service.</span></span>

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a><span data-ttu-id="ad112-194">執行 FRS-Replicated SYSVOL 資料夾的非系統授權還原</span><span class="sxs-lookup"><span data-stu-id="ad112-194">Performing a Nonauthoritative Restore of an FRS-Replicated SYSVOL Folder</span></span>

<span data-ttu-id="ad112-195">非系統授權還原是在個別網域控制站上重新初始化 SYSVOL 複寫最常見的方式。</span><span class="sxs-lookup"><span data-stu-id="ad112-195">The nonauthoritative restore is the most common way to reinitialize SYSVOL replication on individual domain controllers.</span></span> <span data-ttu-id="ad112-196">Nonauthoritatively 還原的網域控制站必須具有來自其他工作網域控制站的輸入連線，而這些網域控制站會參與 Active Directory 和 FRS 複寫。</span><span class="sxs-lookup"><span data-stu-id="ad112-196">Domain controllers that are nonauthoritatively restored must have inbound connections from other working domain controllers, which are participating in Active Directory and FRS replication.</span></span> <span data-ttu-id="ad112-197">在包含許多網域控制站的大型部署環境中，您可以在下列情況下使用非系統授權模式還原來復原其餘的網域控制站：</span><span class="sxs-lookup"><span data-stu-id="ad112-197">In a large deployment environment consisting of many domain controllers, the remaining domain controllers can be recovered using a nonauthoritative mode restore under the following conditions:</span></span>

-   <span data-ttu-id="ad112-198">至少必須有一個已知的良好複本成員 (具有健康情況良好的 SYSVOL 資料夾) 的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="ad112-198">There must be at least one known good replica member (a domain controller with a healthy SYSVOL folder).</span></span>
-   <span data-ttu-id="ad112-199">其他網域控制站必須以直接複寫夥伴順序重新初始化。</span><span class="sxs-lookup"><span data-stu-id="ad112-199">The other domain controllers must be reinitialized in direct replication partner order.</span></span>

<span data-ttu-id="ad112-200">下列程式說明如何執行非系統授權還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-200">The following procedure describes how to perform a nonauthoritative restore.</span></span>

<span data-ttu-id="ad112-201">**執行非系統授權還原**</span><span class="sxs-lookup"><span data-stu-id="ad112-201">**To perform a nonauthoritative restore**</span></span>

1.  <span data-ttu-id="ad112-202">停止 FRS 服務。</span><span class="sxs-lookup"><span data-stu-id="ad112-202">Stop the FRS service.</span></span>
2.  <span data-ttu-id="ad112-203">將備份的資料還原到 SYSVOL 資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-203">Restore the backed-up data to the SYSVOL folder.</span></span>
3.  <span data-ttu-id="ad112-204">將下列登錄機碼的值設定為 DWORD 值 D2，以設定 **BurFlags** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ad112-204">Configure the **BurFlags** registry key by setting the value of the following registry key to the DWORD value D2.</span></span>

    <span data-ttu-id="ad112-205">**HKEY \_\_** \\  \\  \\  \\  \\  \\  \\ **Startup** \\ **BurFlags** 的本機電腦 System CurrentControlSet Services NtFrs 參數備份/還原程式</span><span class="sxs-lookup"><span data-stu-id="ad112-205">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**NtFrs**\\**Parameters**\\**Backup/Restore**\\**Process at Startup**\\**BurFlags**</span></span>

4.  <span data-ttu-id="ad112-206">重新開機 FRS 服務。</span><span class="sxs-lookup"><span data-stu-id="ad112-206">Restart the FRS service.</span></span>

<span data-ttu-id="ad112-207">當 FRS 服務重新開機時，會發生下列動作：</span><span class="sxs-lookup"><span data-stu-id="ad112-207">When the FRS service is restarted, the following actions occur:</span></span>

-   <span data-ttu-id="ad112-208">**BurFlags** 登錄機碼的值會重設為零。</span><span class="sxs-lookup"><span data-stu-id="ad112-208">The value of the **BurFlags** registry key is reset to zero.</span></span>
-   <span data-ttu-id="ad112-209">重新初始化的 FRS 資料夾中的檔案會移至預先存在的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-209">Files in the reinitialized FRS folders are moved to a pre-existing folder.</span></span>
-   <span data-ttu-id="ad112-210">事件13565會記錄在 FRS 事件記錄檔中，以指出已啟動非系統授權還原。</span><span class="sxs-lookup"><span data-stu-id="ad112-210">Event 13565 is logged in the FRS event log to signal that a nonauthoritative restore has started.</span></span>
    > [!Note]  
    > <span data-ttu-id="ad112-211">FRS 事件碼記載于的 [說明及支援] 知識庫中的 [FRS 事件記錄檔錯誤碼] <https://go.microsoft.com/fwlink/p/?linkid=117779></span><span class="sxs-lookup"><span data-stu-id="ad112-211">FRS event codes are documented in "FRS event log error codes" in the Help and Support Knowledge Base at <https://go.microsoft.com/fwlink/p/?linkid=117779></span></span>

     

-   <span data-ttu-id="ad112-212">FRS 資料庫會重建。</span><span class="sxs-lookup"><span data-stu-id="ad112-212">The FRS database is rebuilt.</span></span>
-   <span data-ttu-id="ad112-213">如果已針對 SYSVOL 複本集指定父系，則成員會從上游夥伴或從 **複本集父** 登錄機碼中指定的電腦，執行複本集的初始聯結。</span><span class="sxs-lookup"><span data-stu-id="ad112-213">The member performs an initial join of the replica set from an upstream partner or from the computer that is specified in the **Replica Set Parent** registry key if a parent has been specified for SYSVOL replica sets.</span></span>
-   <span data-ttu-id="ad112-214">重新初始化的電腦會在相關的複寫排程開始時，執行受影響複本集的完整複寫。</span><span class="sxs-lookup"><span data-stu-id="ad112-214">The reinitialized computer runs a full replication of the affected replica sets when the relevant replication schedule begins.</span></span>
-   <span data-ttu-id="ad112-215">當程式完成時，系統會記錄事件13516，以指出 FRS 可正常運作。</span><span class="sxs-lookup"><span data-stu-id="ad112-215">When the process is complete, an event 13516 is logged to signal that FRS is operational.</span></span> <span data-ttu-id="ad112-216">如果未記錄此事件，則 FRS 設定有問題。</span><span class="sxs-lookup"><span data-stu-id="ad112-216">If the event is not logged, there is a problem with the FRS configuration.</span></span>

> [!Note]  
> <span data-ttu-id="ad112-217">在重新初始化的成員上，將檔案放置在 [預先存在](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) 的資料夾中，是 FRS 中的一項防護措施，其設計目的是為了避免意外的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="ad112-217">The placement of files in the [pre-existing](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) folder on reinitialized members is a safeguard in FRS that is designed to prevent accidental data loss.</span></span> <span data-ttu-id="ad112-218">任何目的地為複本的檔案，只存在於本機預先存在的資料夾中，並在初始複寫之後複寫到適當的資料夾。</span><span class="sxs-lookup"><span data-stu-id="ad112-218">Any files destined for the replica that exist only in the local pre-existing folder and were replicated after the initial replication may then be copied to the appropriate folder.</span></span> <span data-ttu-id="ad112-219">發生輸出複寫時，可以刪除預先存在的資料夾中的檔案，以釋放額外的磁片磁碟機空間。</span><span class="sxs-lookup"><span data-stu-id="ad112-219">When outbound replication has occurred, files in the pre-existing folder can be deleted to free additional drive space.</span></span>

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a><span data-ttu-id="ad112-220">執行 FRS-Replicated SYSVOL 資料夾的授權還原</span><span class="sxs-lookup"><span data-stu-id="ad112-220">Performing an Authoritative Restore of an FRS-Replicated SYSVOL Folder</span></span>

<span data-ttu-id="ad112-221">在重大情況下，會使用授權還原作為最後的手段，例如目錄衝突所造成的內容集上的資料分歧。</span><span class="sxs-lookup"><span data-stu-id="ad112-221">Authoritative restores are used as a last resort in case of critical situations such as divergence of data on the content set caused by directory collisions.</span></span> <span data-ttu-id="ad112-222">例如，您可能需要進行授權還原，才能還原複寫已完全停止，且需要從頭重建的 FRS 複本集。</span><span class="sxs-lookup"><span data-stu-id="ad112-222">For example, an authoritative restore might be needed to restore an FRS replica set where replication has completely stopped and a rebuild from scratch is required.</span></span>

<span data-ttu-id="ad112-223">如果您必須執行 SYSVOL 資料夾的授權還原，請注意這是非常複雜的程式。</span><span class="sxs-lookup"><span data-stu-id="ad112-223">If you must perform an authoritative restore of the SYSVOL folder, be aware that it is a very complicated process.</span></span> <span data-ttu-id="ad112-224">完整的指導方針會詳細說明在 [說明及支援] 知識庫中的「如何在網域中重建 SYSVOL 樹狀結構和其內容」中，需要針對該 SYSVOL 資料夾內容進行授權還原所需執行的作業 <https://go.microsoft.com/fwlink/p/?linkid=117780> 。</span><span class="sxs-lookup"><span data-stu-id="ad112-224">Comprehensive guidelines detailing the operations that need to be performed for an authoritative restore of the contents of the SYSVOL folder are documented in "How to rebuild the SYSVOL tree and its content in a domain" in the Help and Support Knowledge Base at <https://go.microsoft.com/fwlink/p/?linkid=117780>.</span></span>

<span data-ttu-id="ad112-225">執行授權的 FRS 還原之前，必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="ad112-225">The following requirements must be met before an authoritative FRS restore is performed:</span></span>

1.  <span data-ttu-id="ad112-226">您必須在所有下游複寫協力電腦上停用 FRS 服務， (已重新初始化的 SYSVOL 資料夾的直接與可轉移) ，才能讓授權還原進行設定。</span><span class="sxs-lookup"><span data-stu-id="ad112-226">The FRS service must be disabled on all downstream replication partners (direct and transitive) for the reinitialized SYSVOL folder before the authoritative restore has been configured to occur.</span></span>
2.  <span data-ttu-id="ad112-227">事件13553和13516已記錄在 FRS 事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="ad112-227">Events 13553 and 13516 have been logged in the FRS event log.</span></span> <span data-ttu-id="ad112-228">這些事件表示已在為授權還原設定的網域控制站上建立 SYSVOL 複本集的成員資格。</span><span class="sxs-lookup"><span data-stu-id="ad112-228">These events indicate that the membership of the SYSVOL replica set has been established on the domain controller that is configured for the authoritative restore.</span></span>
    > [!Note]  
    > <span data-ttu-id="ad112-229">FRS 事件碼記載于的 [說明及支援] 知識庫中的 [FRS 事件記錄檔錯誤碼] <https://go.microsoft.com/fwlink/p/?linkid=117779></span><span class="sxs-lookup"><span data-stu-id="ad112-229">FRS event codes are documented in "FRS event log error codes" in the Help and Support Knowledge Base at <https://go.microsoft.com/fwlink/p/?linkid=117779></span></span>

     

3.  <span data-ttu-id="ad112-230">針對授權還原設定的網域控制站，會設定為要複寫至其餘網域控制站的所有 SYSVOL 資料的授權。</span><span class="sxs-lookup"><span data-stu-id="ad112-230">The domain controller that is configured for the authoritative restore is configured to be authoritative for all the SYSVOL data that is to be replicated to the remaining domain controllers.</span></span>
4.  <span data-ttu-id="ad112-231">複本集中的所有其他夥伴都必須使用非系統授權還原來重新初始化。</span><span class="sxs-lookup"><span data-stu-id="ad112-231">All other partners in the replica set must be reinitialized with a nonauthoritative restore.</span></span>

 

 
