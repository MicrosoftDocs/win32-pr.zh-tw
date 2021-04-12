---
description: 在 Windows Vista 和 Windows Server 2008 和更新版本中，VSS 寫入器或應用程式的開發人員可能會選擇從陰影複製中排除特定檔案。
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: 排除陰影複製中的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195065"
---
# <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="6a63f-103">排除陰影複製中的檔案</span><span class="sxs-lookup"><span data-stu-id="6a63f-103">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="6a63f-104">在 Windows Vista 和 Windows Server 2008 和更新版本中，VSS 寫入器或應用程式的開發人員可能會選擇從陰影複製中排除特定檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-104">In Windows Vista and Windows Server 2008 and later, the developer of a VSS writer or application may choose to exclude certain files from shadow copies.</span></span>

<span data-ttu-id="6a63f-105">「效能影響」和「陰影複製存放區」區域 (也稱為「差異區域」 ) 在陰影複製中使用檔案的方式，與建立陰影複製之後檔案內容中的變更量直接相關。</span><span class="sxs-lookup"><span data-stu-id="6a63f-105">The performance impact and shadow copy storage area (also called "diff area") usage of a file in a shadow copy are directly related to the amount of change in the file's contents after the shadow copy is created.</span></span> <span data-ttu-id="6a63f-106">此外，從陰影複製排除檔案可能會使陰影複製建立變慢。</span><span class="sxs-lookup"><span data-stu-id="6a63f-106">In addition, excluding files from shadow copies may slow down shadow copy creation.</span></span>

<span data-ttu-id="6a63f-107">基於這些理由，只有當檔案很大時，才應該將它從陰影複製中排除，在一個陰影複製和下一個陰影複製之間進行重大變更，而不需要進行備份。</span><span class="sxs-lookup"><span data-stu-id="6a63f-107">For these reasons, a file should be excluded from shadow copies only if it is large, undergoes significant change between one shadow copy and the next, and does not need to be backed up.</span></span>

<span data-ttu-id="6a63f-108">您應該只排除屬於您應用程式的檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-108">You should only exclude files that belong to your application.</span></span>

<span data-ttu-id="6a63f-109">如果 \_ \_ \_ \_ 陰影複製內容中未設定 VSS VOLSNAP ATTR，則表示已停用自動復原，而且不可以從陰影複製中排除任何檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-109">If the VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY flag is set in the shadow copy context, this means that auto-recovery is disabled, and no files can be excluded from the shadow copy.</span></span> <span data-ttu-id="6a63f-110">如需詳細資訊，請參閱 [**\_ VSS \_ 磁片區快照集 \_ \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉。</span><span class="sxs-lookup"><span data-stu-id="6a63f-110">For more information, see the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration.</span></span>

## <a name="using-the-addexcludefilesfromsnapshot-method"></a><span data-ttu-id="6a63f-111">使用 AddExcludeFilesFromSnapshot 方法</span><span class="sxs-lookup"><span data-stu-id="6a63f-111">Using the AddExcludeFilesFromSnapshot Method</span></span>

<span data-ttu-id="6a63f-112">VSS 寫入器可以從陰影複製中排除檔案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6a63f-112">A VSS writer can exclude files from a shadow copy as follows:</span></span>

1.  <span data-ttu-id="6a63f-113">呼叫 [**IVssCreateWriterMetadataEx：： AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) 方法，以報告要排除的檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-113">Call the [**IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) method to report the files to be excluded.</span></span>
2.  <span data-ttu-id="6a63f-114">在寫入器的 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) 方法中，刪除陰影複製中的檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-114">In the writer's [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) method, delete the files from the shadow copy.</span></span>

## <a name="using-the-filesnottosnapshot-registry-key"></a><span data-ttu-id="6a63f-115">使用 FilesNotToSnapshot 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="6a63f-115">Using the FilesNotToSnapshot Registry Key</span></span>

> [!Note]  
> <span data-ttu-id="6a63f-116">**FilesNotToSnapshot** 登錄機碼僅供應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="6a63f-116">The **FilesNotToSnapshot** registry key is intended to be used only by applications.</span></span> <span data-ttu-id="6a63f-117">嘗試使用此登錄機碼的使用者會遇到下列限制：</span><span class="sxs-lookup"><span data-stu-id="6a63f-117">Users who attempt to use it will encounter limitations such as the following:</span></span>
>
> -   <span data-ttu-id="6a63f-118">無法在 Windows Server 上使用舊版功能建立的陰影複製中刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-118">It cannot delete files from a shadow copy that was created on a Windows Server by using the Previous Versions feature.</span></span>
> -   <span data-ttu-id="6a63f-119">無法從共用資料夾陰影複製中刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-119">It cannot delete files from shadow copies for shared folders.</span></span>
> -   <span data-ttu-id="6a63f-120">它可以從使用 [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) 公用程式所建立的陰影複製中刪除檔案，但它無法從使用 [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) 公用程式所建立的陰影複製中刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-120">It can delete files from a shadow copy that was created by using the [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) utility, but it cannot delete files from a shadow copy that was created by using the [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) utility.</span></span>
> -   <span data-ttu-id="6a63f-121">檔案會盡可能以各種方式從陰影複製中刪除。</span><span class="sxs-lookup"><span data-stu-id="6a63f-121">Files are deleted from a shadow copy on a best-effort basis.</span></span> <span data-ttu-id="6a63f-122">但這表示我們無法保證能將其刪除。</span><span class="sxs-lookup"><span data-stu-id="6a63f-122">This means that they are not guaranteed to be deleted.</span></span>

 

<span data-ttu-id="6a63f-123">VSS 應用程式可以使用下列登錄機碼，在陰影複製建立期間從陰影複製中刪除檔案：</span><span class="sxs-lookup"><span data-stu-id="6a63f-123">A VSS application can delete files from a shadow copy during shadow copy creation by using the following registry key:</span></span>

<span data-ttu-id="6a63f-124">**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**</span><span class="sxs-lookup"><span data-stu-id="6a63f-124">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\FilesNotToSnapshot**</span></span>

<span data-ttu-id="6a63f-125">此登錄機碼 \_ \_ 針對可排除其檔案的每個應用程式，都具有 REG 多重 SZ 值。</span><span class="sxs-lookup"><span data-stu-id="6a63f-125">This registry key has REG\_MULTI\_SZ values for each application whose files can be excluded.</span></span> <span data-ttu-id="6a63f-126">檔案是以完整路徑指定，可以包含 \* 萬用字元。</span><span class="sxs-lookup"><span data-stu-id="6a63f-126">The files are specified by fully qualified paths, which can contain the \* wildcard.</span></span>

<span data-ttu-id="6a63f-127">在所有情況下，如果沒有任何檔案符合路徑字串，則會忽略此專案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-127">In all cases, the entry is ignored if there are no files that match the path string.</span></span>

<span data-ttu-id="6a63f-128">將檔案新增至適當的登錄機碼值之後，陰影複製優化寫入器會以最佳方式在建立期間從陰影複製中刪除該檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-128">After a file is added to the appropriate registry key value, it is deleted from the shadow copy during creation by the shadow copy optimization writer on a best-effort basis.</span></span>

<span data-ttu-id="6a63f-129">如果無法指定完整路徑，則也可以使用 $UserProfile $ 或 $AllVolumes $ 變數來隱含路徑。</span><span class="sxs-lookup"><span data-stu-id="6a63f-129">If a fully qualified path cannot be specified, then a path can also be implied by using the $UserProfile$ or $AllVolumes$ variable.</span></span> <span data-ttu-id="6a63f-130">例如：</span><span class="sxs-lookup"><span data-stu-id="6a63f-130">For example:</span></span>

-   <span data-ttu-id="6a63f-131">$UserProfile $ \\ Directory \\ 子目錄 \\ 檔案名。\*</span><span class="sxs-lookup"><span data-stu-id="6a63f-131">$UserProfile$\\Directory\\Subdirectory\\FileName.\*</span></span>
-   <span data-ttu-id="6a63f-132">$AllVolumes $ \\ TemporaryFiles \\ \* 。\*</span><span class="sxs-lookup"><span data-stu-id="6a63f-132">$AllVolumes$\\TemporaryFiles\\\*.\*</span></span>

<span data-ttu-id="6a63f-133">若要將路徑設為遞迴，請將 "/s" 附加至結尾。</span><span class="sxs-lookup"><span data-stu-id="6a63f-133">To make the path recursive, append " /s" to the end.</span></span> <span data-ttu-id="6a63f-134">例如：</span><span class="sxs-lookup"><span data-stu-id="6a63f-134">For example:</span></span>

-   <span data-ttu-id="6a63f-135">$UserProfile $ \\ Directory \\ 子目錄 \\ 檔案名 \* /s</span><span class="sxs-lookup"><span data-stu-id="6a63f-135">$UserProfile$\\Directory\\Subdirectory\\FileName.\* /s</span></span>
-   <span data-ttu-id="6a63f-136">$AllVolumes $ \\ TemporaryFiles \\ \* \* /s</span><span class="sxs-lookup"><span data-stu-id="6a63f-136">$AllVolumes$\\TemporaryFiles\\\*.\* /s</span></span>

<span data-ttu-id="6a63f-137">$UserProfile $ 變數會將路徑字串套用至電腦上的所有使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="6a63f-137">The $UserProfile$ variable causes the path string to be applied to all user profiles on the computer.</span></span> <span data-ttu-id="6a63f-138">藉由檢查下列登錄機碼來列舉使用者設定檔：</span><span class="sxs-lookup"><span data-stu-id="6a63f-138">The user profiles are enumerated by examining the following registry key:</span></span>

<span data-ttu-id="6a63f-139">**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ProfileList**</span><span class="sxs-lookup"><span data-stu-id="6a63f-139">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\ProfileList**</span></span>

<span data-ttu-id="6a63f-140">$AllVolumes $ 變數會將路徑字串套用至電腦上的所有陰影複製。</span><span class="sxs-lookup"><span data-stu-id="6a63f-140">The $AllVolumes$ variable causes the path string to be applied to all shadow copies on the computer.</span></span> <span data-ttu-id="6a63f-141">例如，假設路徑為 "$AllVolumes $ \\ TemporaryFiles \\ \* 。 \*/s "，且電腦有三個磁片區： C：、D：和 E:。</span><span class="sxs-lookup"><span data-stu-id="6a63f-141">For example, suppose the path is "$AllVolumes$\\TemporaryFiles\\\*.\* /s", and the computer has three volumes: C:, D:, and E:.</span></span> <span data-ttu-id="6a63f-142">如果 C：和 E：包含路徑 " \\ TemporaryFiles \\ "，而磁片區 D：只包含路徑 d： \\ Data，則 \\ 會從 C：的陰影複製中刪除目錄樹狀結構 C： \\ TemporaryFiles \\ ，且目錄樹狀結構 E： \\ TemporaryFiles \\ 會從 E:. 的陰影複製中刪除</span><span class="sxs-lookup"><span data-stu-id="6a63f-142">If C: and E: contain the path "\\TemporaryFiles\\", and volume D: contains only the path D:\\Data\\, the directory tree C:\\TemporaryFiles\\ is deleted from shadow copies of C:, and the directory tree E:\\TemporaryFiles\\ is deleted from shadow copies of E:.</span></span>

<span data-ttu-id="6a63f-143">系統管理員可以使用下列登錄機碼來停用 $UserProfile $ 變數的擴充：</span><span class="sxs-lookup"><span data-stu-id="6a63f-143">Administrators can disable expansion of the $UserProfile$ variable by using the following registry key:</span></span>

<span data-ttu-id="6a63f-144">**HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 服務 \\ Vss \\ 設定**</span><span class="sxs-lookup"><span data-stu-id="6a63f-144">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Vss\\Settings**</span></span>

<span data-ttu-id="6a63f-145">在此登錄機碼下，為值名稱指定 DisableUserProfileExpansion、為 \_ 數值型別指定 REG DWORD，並為值資料指定非零值。</span><span class="sxs-lookup"><span data-stu-id="6a63f-145">Under this registry key, specify DisableUserProfileExpansion for the value name, REG\_DWORD for the value type, and a nonzero value for the value data.</span></span>

## <a name="about-the-filesnottobackup-registry-key"></a><span data-ttu-id="6a63f-146">關於 FilesNotToBackup 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="6a63f-146">About the FilesNotToBackup Registry Key</span></span>

<span data-ttu-id="6a63f-147">**FilesNotToBackup** 登錄機碼可以用來指定備份應用程式不應備份或還原的檔案和目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="6a63f-147">The **FilesNotToBackup** registry key can be used to specify the names of the files and directories that backup applications should not backup or restore.</span></span> <span data-ttu-id="6a63f-148">不過，它不會從陰影複製中排除這些檔案。</span><span class="sxs-lookup"><span data-stu-id="6a63f-148">However, it does not exclude those files from shadow copies.</span></span> <span data-ttu-id="6a63f-149">如需此登錄機碼的詳細資訊，請參閱 [備份和還原的登錄機碼和值](../backup/registry-keys-for-backup-and-restore.md)。</span><span class="sxs-lookup"><span data-stu-id="6a63f-149">For more information about this registry key, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

 

 
