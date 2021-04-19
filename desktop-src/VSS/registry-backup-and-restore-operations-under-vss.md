---
description: Windows 登錄服務支援 VSS 寫入器，稱為登錄寫入器，它可讓要求者使用儲存在陰影複製磁片區上的資料來備份系統登錄。
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: VSS 下的登錄備份和還原作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980802"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a><span data-ttu-id="817bd-103">VSS 下的登錄備份和還原作業</span><span class="sxs-lookup"><span data-stu-id="817bd-103">Registry Backup and Restore Operations Under VSS</span></span>

<span data-ttu-id="817bd-104">Windows 登錄服務支援 VSS 寫入器，稱為登錄寫入器，它可讓要求者使用儲存在陰影複製磁片區上的資料來備份系統登錄。</span><span class="sxs-lookup"><span data-stu-id="817bd-104">The Windows Registry Service supports a VSS writer, called the registry writer, which allows requesters to back up a system registry using data stored on a shadow copied volume.</span></span> <span data-ttu-id="817bd-105">如需登錄寫入器的詳細資訊，請參閱 [內建的 VSS 寫入](in-box-vss-writers.md)器。</span><span class="sxs-lookup"><span data-stu-id="817bd-105">For more information about the registry writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

<span data-ttu-id="817bd-106">登錄寫入器會執行登錄的就地備份和還原。</span><span class="sxs-lookup"><span data-stu-id="817bd-106">The registry writer performs in-place backups and restores of the registry.</span></span> <span data-ttu-id="817bd-107">此外，登錄寫入器只會報告系統 hive;它不會報告使用者 hive。</span><span class="sxs-lookup"><span data-stu-id="817bd-107">In addition, the registry writer reports only system hives; it does not report user hives.</span></span>

<span data-ttu-id="817bd-108">**Windows Server 2003：** 登錄寫入器使用中繼存放庫檔案 (也稱為算檔) 來儲存登錄資料。</span><span class="sxs-lookup"><span data-stu-id="817bd-108">**Windows Server 2003:** The registry writer uses an intermediate repository file (also known as a spit file) to store registry data.</span></span> <span data-ttu-id="817bd-109">此外，登錄寫入器會報告系統 hive 和使用者 hive。</span><span class="sxs-lookup"><span data-stu-id="817bd-109">In addition, the registry writer reports system hives and user hives.</span></span>

<span data-ttu-id="817bd-110">登錄寫入器的寫入器識別碼是 AFBAB4A2-367D-4D15-A586-71DBB18F8485。</span><span class="sxs-lookup"><span data-stu-id="817bd-110">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

<span data-ttu-id="817bd-111">**WINDOWS XP：** 沒有任何登錄寫入器。</span><span class="sxs-lookup"><span data-stu-id="817bd-111">**Windows XP:** There is no registry writer.</span></span> <span data-ttu-id="817bd-112">登錄資料是由可開機狀態寫入器所報告，其寫入器識別碼是 F2436E37-09F5-41AF-9B2A-4CA2435DBFD5。</span><span class="sxs-lookup"><span data-stu-id="817bd-112">The registry data is reported by the Bootable State writer, whose writer ID is F2436E37-09F5-41AF-9B2A-4CA2435DBFD5.</span></span>

> [!Note]  
> <span data-ttu-id="817bd-113">Microsoft 不會提供開發人員或 IT 專業人員技術支援，以在 Windows (所有版本) 上執行線上系統狀態還原。</span><span class="sxs-lookup"><span data-stu-id="817bd-113">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span> <span data-ttu-id="817bd-114">如需有關使用 Microsoft 提供的 Api 和程式來執行線上系統狀態還原的詳細資訊，請參閱 [MSDN 論壇中心](https://msdn.microsoft.com/community/default.aspx)提供的「社區資源」。</span><span class="sxs-lookup"><span data-stu-id="817bd-114">For information about using Microsoft-provided APIs and procedures to implement online system state restores, see the community resources available at the [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span></span>

 

> [!Note]  
> <span data-ttu-id="817bd-115">下列資訊僅適用于 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="817bd-115">The following information only applies to Windows Server 2003 and Windows XP.</span></span>

 

## <a name="registry-backup-using-vss"></a><span data-ttu-id="817bd-116">使用 VSS 的登錄備份</span><span class="sxs-lookup"><span data-stu-id="817bd-116">Registry Backup Using VSS</span></span>

<span data-ttu-id="817bd-117">登錄寫入器會將 active registry 檔案匯出並儲存在 key **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist** 所定義的位置。</span><span class="sxs-lookup"><span data-stu-id="817bd-117">The registry writer will export and save active registry files in the locations defined by the key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**hivelist**.</span></span>

<span data-ttu-id="817bd-118">此登錄專案下的值名稱會識別要儲存的登錄區，而值的資料會提供檔案，其中包含 (hive 檔案) 的檔案。</span><span class="sxs-lookup"><span data-stu-id="817bd-118">The names of the values under this registry entry identify the registry hive to be saved, and the value's data provides the file containing the file (the hive file).</span></span> <span data-ttu-id="817bd-119">Hive 檔案的指定格式如下： \\ 裝置 \\ *HarddiskVolumeX* \\ *路徑* \\ *檔案名*。</span><span class="sxs-lookup"><span data-stu-id="817bd-119">The hive files are specified with the following format: \\Device\\*HarddiskVolumeX*\\*path*\\*filename*.</span></span>

<span data-ttu-id="817bd-120">例如，在 [ **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**] 底下，您可能會看到登錄 **\\ \\ 電腦 \\ 軟體**  =  \\ 裝置 \\ HarddiskVolume1 \\ Windows \\ System32 \\ config \\ SOFTWARE。</span><span class="sxs-lookup"><span data-stu-id="817bd-120">For example, under **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**hivelist**, you might see **\\REGISTRY\\MACHINE\\SOFTWARE** = \\Device\\HarddiskVolume1\\Windows\\System32\\config\\SOFTWARE.</span></span>

<span data-ttu-id="817bd-121">登錄寫入器可確保在磁片陰影複製之前，將 hive 檔案儲存至磁片。</span><span class="sxs-lookup"><span data-stu-id="817bd-121">The registry writer ensures that hive files are saved to disk prior to its shadow copy.</span></span>

<span data-ttu-id="817bd-122">備份登錄 hive 時，要求者會 \\ \\ 以磁片區陰影複製的 [*裝置物件*](vssgloss-d.md)字串來取代裝置 *HarddiskVolumeX* 。</span><span class="sxs-lookup"><span data-stu-id="817bd-122">When backing up the registry hives, a requester would replace \\Device\\*HarddiskVolumeX* with the [*device object*](vssgloss-d.md) string of the volume's shadow copy.</span></span>

> [!Note]  
> <span data-ttu-id="817bd-123">您可以 \\ 使用 QueryDosDevice 函數，將裝置 \\ *HarddiskVolumeX* 路徑轉換成相等的 Win32 [](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew)路徑。</span><span class="sxs-lookup"><span data-stu-id="817bd-123">You can convert the \\Device\\*HarddiskVolumeX* path to an equivalent Win32 path by using the [**QueryDosDevice**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) function.</span></span> <span data-ttu-id="817bd-124">如需詳細資訊，請參閱 [從檔案控制代碼取得檔案名](../memory/obtaining-a-file-name-from-a-file-handle.md) 或 [顯示磁片區路徑名稱](../fileio/displaying-volume-paths.md)。</span><span class="sxs-lookup"><span data-stu-id="817bd-124">For more information, see [Obtaining a File Name From a File Handle](../memory/obtaining-a-file-name-from-a-file-handle.md) or [Displaying Volume Path Names](../fileio/displaying-volume-paths.md).</span></span>

 

## <a name="registry-restore-using-non-vss-win32-apis"></a><span data-ttu-id="817bd-125">使用非 VSS Win32 Api 的登錄還原</span><span class="sxs-lookup"><span data-stu-id="817bd-125">Registry Restore Using Non-VSS Win32 APIs</span></span>

<span data-ttu-id="817bd-126">若為線上 (安全模式或完整作業系統) 還原，必須保留 **HKEY \_ 本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **會話管理員** \\ **PendingFileRenameOperations** 登錄機碼中的子機碼。</span><span class="sxs-lookup"><span data-stu-id="817bd-126">For an online (safe mode or full operating system) restore, the subkeys in the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**PendingFileRenameOperations** registry key must be preserved.</span></span>

<span data-ttu-id="817bd-127">[**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa)和 [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda)函式會使用此登錄機碼，儲存在 \_ \_ \_ *DWFLAGS* 參數中重新開機值之前使用 MOVEFILE 延遲重新命名之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="817bd-127">The [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) and [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) functions use this registry key to store information about files that were renamed by using the MOVEFILE\_DELAY\_UNTIL\_REBOOT value in the *dwFlags* parameter.</span></span>

<span data-ttu-id="817bd-128">為了保留 **PendingFileRenameOperations** 登錄機碼的內容，您的備份應用程式應該呼叫 [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) 函式，以連接要還原到 active registry 的登錄檔。</span><span class="sxs-lookup"><span data-stu-id="817bd-128">To preserve the contents of the **PendingFileRenameOperations** registry key, your backup application should call the [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) function to connect the registry file to be restored to the active registry.</span></span> <span data-ttu-id="817bd-129">然後，您的備份應用程式可以使用各種登錄功能，將所需的金鑰和值複製到載入的 hive。</span><span class="sxs-lookup"><span data-stu-id="817bd-129">Your backup application can then use the various registry functions to copy the desired keys and values into the loaded hive.</span></span> <span data-ttu-id="817bd-130">複製完成之後，應該呼叫 [**RegFlushKey**](/windows/win32/api/winreg/nf-winreg-regflushkey) 和 [**RegUnloadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="817bd-130">After the copy is complete, the [**RegFlushKey**](/windows/win32/api/winreg/nf-winreg-regflushkey) and [**RegUnloadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) functions should be called.</span></span>

<span data-ttu-id="817bd-131">若為離線 (Windows 修復環境或 Windows PE) 還原，則不需要接受 **PendingFileRenameOperations** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="817bd-131">For an offline (Windows Recovery Environment or Windows PE) restore, it is not necessary to honor the **PendingFileRenameOperations** registry key.</span></span>

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a><span data-ttu-id="817bd-132">在 Windows Server 2003 中使用非 VSS Win32 Api 的登錄還原</span><span class="sxs-lookup"><span data-stu-id="817bd-132">Registry Restore Using Non-VSS Win32 APIs in Windows Server 2003</span></span>

> [!Note]  
> <span data-ttu-id="817bd-133">下列資訊僅適用于與嚴重損壞修復相關的還原作業 (也稱為在 Windows Server 2003 中執行的裸機修復) 。</span><span class="sxs-lookup"><span data-stu-id="817bd-133">The following information applies only to restore operations related to disaster recovery (also known as bare-metal recovery) that are performed in Windows Server 2003.</span></span>

 

<span data-ttu-id="817bd-134">還原登錄時，備份應用程式必須將目前登錄的一些子機碼移至要還原的登錄中。</span><span class="sxs-lookup"><span data-stu-id="817bd-134">When restoring the registry, a backup application needs to move some of the subkeys from the current registry into the registry that is to be restored.</span></span>

<span data-ttu-id="817bd-135">若要這樣做，備份應用程式可以呼叫 **RegLoadKey** 來連接要還原到目前作用中登錄的登錄檔。</span><span class="sxs-lookup"><span data-stu-id="817bd-135">To do this, a backup application can call **RegLoadKey** to connect the registry file to be restored to the currently active registry.</span></span> <span data-ttu-id="817bd-136">然後，它可以使用各種登錄函式，將所需的金鑰和值複製到載入的 hive。</span><span class="sxs-lookup"><span data-stu-id="817bd-136">It can then use the various registry functions to copy the desired keys and values into the loaded hive.</span></span> <span data-ttu-id="817bd-137">複製完成之後，會呼叫 **RegFlushKey** 和 **RegUnloadKey** 。</span><span class="sxs-lookup"><span data-stu-id="817bd-137">After the copy is complete, **RegFlushKey** and **RegUnloadKey** are called.</span></span>

<span data-ttu-id="817bd-138">有一個登錄機碼，指出還原應用程式 (要求者) **HKEY \_ 本機 \_ 電腦 \\ 系統** 下的登錄機碼，在還原時不應覆寫這些登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="817bd-138">There is a registry key that indicates to a restore application (requester) the registry keys under **HKEY\_LOCAL\_MACHINE\\SYSTEM** that should not be overwritten at restore time:</span></span>

<span data-ttu-id="817bd-139">**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**</span><span class="sxs-lookup"><span data-stu-id="817bd-139">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\KeysNotToRestore**</span></span>

<span data-ttu-id="817bd-140">系統狀態還原程式的一部分牽涉到還原先前備份的登錄。</span><span class="sxs-lookup"><span data-stu-id="817bd-140">Part of the system state restore process involves restoring a previously backed-up registry.</span></span>

<span data-ttu-id="817bd-141">還原 **HKEY \_ 本機 \_ 電腦 \\ 系統** hive 時，備份應用程式必須特別小心，因為安裝 Windows 作業系統暫存版本的程式將會在新安裝的系統 hive 中建立索引鍵，其值必須存留在還原作業的時間。</span><span class="sxs-lookup"><span data-stu-id="817bd-141">Backup applications need to take special care when restoring the **HKEY\_LOCAL\_MACHINE\\SYSTEM** hive because the process of installing a temporary version of the Windows operating system will have established keys in the newly installed system hive whose values must survive the restore operation.</span></span>

<span data-ttu-id="817bd-142">例如，當更換系統有不同于原始系統的網路介面卡時，還原上一張卡片的原始金鑰將會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="817bd-142">For example, when the replacement system has a network interface card different from the original system, restoration of the original keys for the previous card will lead to unpredictable results.</span></span> <span data-ttu-id="817bd-143">這是因為隨插即用服務已偵測到並將適當的服務和驅動程式登錄專案放入登錄中。</span><span class="sxs-lookup"><span data-stu-id="817bd-143">This is because the Plug and Play service has detected and placed proper service and driver registry entries into the registry.</span></span> <span data-ttu-id="817bd-144">您必須保留這些值，才能在系統還原之後正確開機。</span><span class="sxs-lookup"><span data-stu-id="817bd-144">These values must be preserved to properly boot after system restore.</span></span>

<span data-ttu-id="817bd-145">本節說明在執行 **HKEY \_ 本機 \_ 電腦 \\ 系統** hive 的還原時，備份應用程式如何探索要保留的金鑰和檔案。</span><span class="sxs-lookup"><span data-stu-id="817bd-145">This section describes how backup applications can discover which keys and files are to be preserved when executing a restore of the **HKEY\_LOCAL\_MACHINE\\SYSTEM** hive.</span></span> <span data-ttu-id="817bd-146">在某些情況下，這會牽涉到以程式設計的方式，將新安裝的安裝 hive 中的金鑰複製到要還原的 hive。</span><span class="sxs-lookup"><span data-stu-id="817bd-146">In some cases, this will involve programmatically copying the keys from the newly installed installation hive into the hive to be restored.</span></span> <span data-ttu-id="817bd-147">在其他情況下，確保不會取代產品的登錄機碼，就像在產品的 INF 設定檔中指定這類金鑰一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="817bd-147">In other cases, ensuring that a product's registry keys are not replaced is as simple as specifying such keys in the product's INF configuration file.</span></span>

<span data-ttu-id="817bd-148">金鑰 (和要保留的金鑰資料) 會在 **HKEY 的 \_ 本機 \_ 電腦 \\ 系統** hive 中列舉</span><span class="sxs-lookup"><span data-stu-id="817bd-148">Keys (and key data) that are to be preserved are enumerated in the **HKEY\_LOCAL\_MACHINE\\SYSTEM** hive under the</span></span>

<span data-ttu-id="817bd-149">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**</span><span class="sxs-lookup"><span data-stu-id="817bd-149">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\BackupRestore\\KeysNotToRestore**</span></span>

<span data-ttu-id="817bd-150">這份檔中的索引鍵是一組 REG \_ 多重 \_ SZ 字串 (稱為索引 *鍵字串*) 。</span><span class="sxs-lookup"><span data-stu-id="817bd-150">key as sets of REG\_MULTI\_SZ strings (called *key strings* in this document).</span></span>

<span data-ttu-id="817bd-151">備份應用程式 (要求者) 必須檢查 active registry 和新還原登錄中這些機碼的值，因為任何應用程式或服務都可以隨時新增值。</span><span class="sxs-lookup"><span data-stu-id="817bd-151">A backup application (requester) must examine the values of these keys in the active registry and the newly restored registry because any application or service can add values at any time.</span></span>

<span data-ttu-id="817bd-152">備份應用程式如何解讀金鑰字串是由其終端字元所決定：</span><span class="sxs-lookup"><span data-stu-id="817bd-152">How key strings are to be interpreted by backup applications is determined by their terminal character:</span></span>

1.  <span data-ttu-id="817bd-153">以反斜線 ( ' ' 結尾的索引鍵字串，) 會被視為子機碼 \\ 。</span><span class="sxs-lookup"><span data-stu-id="817bd-153">Key strings terminated with a backslash ('\\') are interpreted as subkeys.</span></span> <span data-ttu-id="817bd-154">當遇到這類子字串時，備份應用程式必須保留所有資料和所有附屬索引鍵。</span><span class="sxs-lookup"><span data-stu-id="817bd-154">When such a substring is encountered, the backup application must preserve all data and all subordinate keys.</span></span>

    <span data-ttu-id="817bd-155">例如，下列程式指定要在整個還原作業中保留所有從屬金鑰和資料：</span><span class="sxs-lookup"><span data-stu-id="817bd-155">For example, the following specifies that all subordinate keys and data are to be preserved across a restore operation:</span></span>

    <span data-ttu-id="817bd-156">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services \\ dmio \\ boot info\\**</span><span class="sxs-lookup"><span data-stu-id="817bd-156">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\dmio\\boot info\\**</span></span>

    <span data-ttu-id="817bd-157">至此，您必須從現有的登錄複製這個金鑰和所有附屬金鑰和資料 (也就是安裝 Windows) 所建立的登錄到新還原的登錄中。</span><span class="sxs-lookup"><span data-stu-id="817bd-157">To this end, this key and all subordinate keys and data must be copied from the existing registry (that is, the one created by the installation of Windows) into the newly restored registry.</span></span> <span data-ttu-id="817bd-158">這稱為「 *金鑰取代* 」作業。</span><span class="sxs-lookup"><span data-stu-id="817bd-158">This is called a *key replace* operation.</span></span> <span data-ttu-id="817bd-159">這項操作會取代還原登錄中的對應機碼。</span><span class="sxs-lookup"><span data-stu-id="817bd-159">This operation replaces the corresponding key in the restored registry.</span></span>

2.  <span data-ttu-id="817bd-160">終止字元是星號 ( ' ' 的索引鍵字串， \* ) 指定應合併所有子機碼。</span><span class="sxs-lookup"><span data-stu-id="817bd-160">Key strings whose termination character is an asterisk ('\*') specifies that all subkeys should be merged.</span></span> <span data-ttu-id="817bd-161">例如，索引鍵字串：</span><span class="sxs-lookup"><span data-stu-id="817bd-161">For example, the key string:</span></span>

    <span data-ttu-id="817bd-162">\**HKEY \_LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ \\ Services \** _</span><span class="sxs-lookup"><span data-stu-id="817bd-162">\**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\\** _</span></span>

    <span data-ttu-id="817bd-163">指定現有登錄中的服務機碼 (例如，安裝 Windows) 所建立的服務金鑰必須合併到還原的登錄中。</span><span class="sxs-lookup"><span data-stu-id="817bd-163">specifies that the services key in the existing registry (for example those created by the installation of Windows) must be merged into the restored registry.</span></span> <span data-ttu-id="817bd-164">這稱為 _key merge \* 作業，而且如果子機碼同時存在於現有的 hive 和還原的 hive 中，則會保留還原目錄中的金鑰，但有下列例外狀況：</span><span class="sxs-lookup"><span data-stu-id="817bd-164">This is called a _key merge\* operation, and if a subkey exists in both the existing hive and the restored hive, the key in the restored directory is preserved with the following exceptions:</span></span>

    -   <span data-ttu-id="817bd-165">如果現有 hive 中的子機碼包含名為 "start" 的值，而且還原中的子機碼不是。</span><span class="sxs-lookup"><span data-stu-id="817bd-165">If the subkey in the existing hive contains a value named "start", and the subkey in the restored does not.</span></span>
    -   <span data-ttu-id="817bd-166">如果現有和已還原之 hive 中的子機碼包含名為 "start" 的值，且其在現有 hive 中的數值較小。</span><span class="sxs-lookup"><span data-stu-id="817bd-166">If the subkey in both the existing and restored hive contain a value named "start", and its numeric value in the existing hive is less.</span></span>

    <span data-ttu-id="817bd-167">登錄中的 "start" 值會指定何時啟動服務或驅動程式，且可具有來自0-4 的數值。</span><span class="sxs-lookup"><span data-stu-id="817bd-167">The "start" value in the registry specifies when a service or driver will start and can have a numeric value from 0-4.</span></span> <span data-ttu-id="817bd-168">值越低，啟動程式中的服務就會越快開始。</span><span class="sxs-lookup"><span data-stu-id="817bd-168">The lower the value, the sooner in the boot process the service will start.</span></span>

    <span data-ttu-id="817bd-169">如果現有和已還原的目錄中都有此金鑰，您必須檢查每個 hive 中的 start 鍵值。</span><span class="sxs-lookup"><span data-stu-id="817bd-169">If this key exists in both the existing and the restored directory, you must examine the value of the start key in each hive.</span></span> <span data-ttu-id="817bd-170">如果現有 hive 中的值低於還原的目錄中的值，則必須保留較低的值。</span><span class="sxs-lookup"><span data-stu-id="817bd-170">If the value in the existing hive is lower than the value in the restored directory, the lower value must be preserved.</span></span>

    <span data-ttu-id="817bd-171">同樣地，此金鑰是用來判斷服務或驅動程式是在開機時、系統時間、手動、自動或停用時啟動。</span><span class="sxs-lookup"><span data-stu-id="817bd-171">Once again, this key is used to determine whether a service or driver is to be started at boot time, at system time, manually, automatically, or be disabled.</span></span> <span data-ttu-id="817bd-172">較低的值代表較早的開始時間。</span><span class="sxs-lookup"><span data-stu-id="817bd-172">The lower value represents an earlier start time.</span></span> <span data-ttu-id="817bd-173">您必須將先前的開始時間套用至新的登錄，以確保服務或驅動程式會在下一次開機時正常啟動。</span><span class="sxs-lookup"><span data-stu-id="817bd-173">The earlier start time must be applied to the new registry to ensure that the service or drivers are started properly at the next boot.</span></span>

3.  <span data-ttu-id="817bd-174">其終止字元不是反斜線也不是星號的索引鍵字串，會被視為要保留的登錄值。</span><span class="sxs-lookup"><span data-stu-id="817bd-174">Key strings whose termination character is neither a backslash nor an asterisk are interpreted as registry values to be preserved.</span></span>

    <span data-ttu-id="817bd-175">例如，索引鍵字串：</span><span class="sxs-lookup"><span data-stu-id="817bd-175">For example, the key string:</span></span>

    <span data-ttu-id="817bd-176">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Session Manager \\ PendingFileRenameOperations**</span><span class="sxs-lookup"><span data-stu-id="817bd-176">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Session Manager\\PendingFileRenameOperations**</span></span>

    <span data-ttu-id="817bd-177">可以用程式設計的方式來保留金鑰的機制包含 Win32 登錄 API。</span><span class="sxs-lookup"><span data-stu-id="817bd-177">The mechanism by which keys can be preserved programmatically involves the Win32 registry API.</span></span> <span data-ttu-id="817bd-178">例如，以下列舉一個演算法：</span><span class="sxs-lookup"><span data-stu-id="817bd-178">For example, one algorithm is enumerated below:</span></span>

    1.  <span data-ttu-id="817bd-179">將備份的系統 hive 檔案還原至檔案。</span><span class="sxs-lookup"><span data-stu-id="817bd-179">Restore the backed-up system hive file to a file.</span></span> <span data-ttu-id="817bd-180">在此範例中，讓名稱為 system.string。</span><span class="sxs-lookup"><span data-stu-id="817bd-180">For this example, let the name be System.reg.</span></span>
    2.  <span data-ttu-id="817bd-181">使用 **RegLoadKey** ，以暫存名稱將 System.string 載入 **HKEY \_ 本機 \_ 電腦** 。</span><span class="sxs-lookup"><span data-stu-id="817bd-181">Use **RegLoadKey** to load System.reg into **HKEY\_LOCAL\_MACHINE** under a temporary name.</span></span> <span data-ttu-id="817bd-182">例如，其中一個名稱可能是</span><span class="sxs-lookup"><span data-stu-id="817bd-182">For example, one such name might be</span></span>

        <span data-ttu-id="817bd-183">**HKEY \_ 本機 \_ 電腦 \\ TMP \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="817bd-183">**HKEY\_LOCAL\_MACHINE\\TMP\_SYSTEM**</span></span>

    3.  <span data-ttu-id="817bd-184">從兩個登錄複本列舉 **KeysNotToRestore** 子機碼中的值，並建立清單的超集合。</span><span class="sxs-lookup"><span data-stu-id="817bd-184">Enumerate the values in the **KeysNotToRestore** subkey from both of the registry copies and create a superset of the lists.</span></span> <span data-ttu-id="817bd-185">從現有的中複製每個這類金鑰</span><span class="sxs-lookup"><span data-stu-id="817bd-185">Copy each such key from the existing</span></span>

        <span data-ttu-id="817bd-186">**HKEY \_ 本機 \_ 電腦 \\ 系統**</span><span class="sxs-lookup"><span data-stu-id="817bd-186">**HKEY\_LOCAL\_MACHINE\\SYSTEM**</span></span>

        <span data-ttu-id="817bd-187">的索引鍵</span><span class="sxs-lookup"><span data-stu-id="817bd-187">key into the</span></span>

        <span data-ttu-id="817bd-188">**HKEY \_ 本機 \_ 電腦 \\ TMP \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="817bd-188">**HKEY\_LOCAL\_MACHINE\\TMP\_SYSTEM**</span></span>

        <span data-ttu-id="817bd-189">根據上述語義的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="817bd-189">key according to the semantics described above.</span></span>

    4.  <span data-ttu-id="817bd-190">完成時，請使用 **RegFlushKey**  &  **RegUnloadKey** 進入點來儲存</span><span class="sxs-lookup"><span data-stu-id="817bd-190">When complete use the **RegFlushKey** & **RegUnloadKey** entry points to save the</span></span>

        <span data-ttu-id="817bd-191">**HKEY \_ 本機 \_ 電腦 \\ TMP \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="817bd-191">**HKEY\_LOCAL\_MACHINE\\TMP\_SYSTEM**</span></span>

        <span data-ttu-id="817bd-192">金鑰傳回給 System.object。</span><span class="sxs-lookup"><span data-stu-id="817bd-192">key back to System.reg.</span></span>

    5.  <span data-ttu-id="817bd-193">最後，使用 **RegReplaceKey** 來指定要取代</span><span class="sxs-lookup"><span data-stu-id="817bd-193">Finally, use **RegReplaceKey** to specify that System.reg is to replace the</span></span>

        <span data-ttu-id="817bd-194">**HKEY \_ 本機 \_ 電腦 \\ 系統**</span><span class="sxs-lookup"><span data-stu-id="817bd-194">**HKEY\_LOCAL\_MACHINE\\SYSTEM**</span></span>

        <span data-ttu-id="817bd-195">hive 檔案、SYSTEM。</span><span class="sxs-lookup"><span data-stu-id="817bd-195">hive file, SYSTEM.</span></span>

 

 
