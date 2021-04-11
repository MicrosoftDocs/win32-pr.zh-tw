---
description: 以下是與 Windows Vista 和 Windows Server 2008 中引進的各種檔案系統和安全性功能正確互通的提示。
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: 使用檔案系統和安全性功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113156"
---
# <a name="working-with-file-system-and-security-features"></a><span data-ttu-id="166bd-103">使用檔案系統和安全性功能</span><span class="sxs-lookup"><span data-stu-id="166bd-103">Working with File System and Security Features</span></span>

<span data-ttu-id="166bd-104">以下是與 Windows Vista 和 Windows Server 2008 中引進的各種檔案系統和安全性功能正確互通的提示。</span><span class="sxs-lookup"><span data-stu-id="166bd-104">The following are hints for interoperating correctly with various file system and security features that were introduced in Windows Vista and Windows Server 2008.</span></span>

## <a name="interoperability-with-transactions"></a><span data-ttu-id="166bd-105">與交易互通性</span><span class="sxs-lookup"><span data-stu-id="166bd-105">Interoperability with Transactions</span></span>

<span data-ttu-id="166bd-106">為了支援交易，VSS 可確保核心交易管理員 (KTM) 和分散式交易協調器 (DTC) 在建立磁片區陰影複製之前已凍結。</span><span class="sxs-lookup"><span data-stu-id="166bd-106">To support transactions, VSS ensures that both the Kernel Transaction Manager (KTM) and the Distributed Transaction Coordinator (DTC) are frozen prior to the creation of volume shadow copies.</span></span> <span data-ttu-id="166bd-107">如果系統無法凍結或解除凍結 KTM 或 DTC， [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 方法可能會傳回下列逾時錯誤：</span><span class="sxs-lookup"><span data-stu-id="166bd-107">If the system fails to freeze or thaw KTM or DTC, the following timeout errors may be returned by the [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) method:</span></span>

<dl> <span data-ttu-id="166bd-108">VSS \_ E \_ 交易 \_ 凍結 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="166bd-108">VSS\_E\_TRANSACTION\_FREEZE\_TIMEOUT</span></span>  
<span data-ttu-id="166bd-109">VSS \_ E \_ 交易 \_ 解除凍結 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="166bd-109">VSS\_E\_TRANSACTION\_THAW\_TIMEOUT</span></span>  
</dl>

<span data-ttu-id="166bd-110">如果要求者收到上述其中一個錯誤碼，則必須重試建立陰影複製。</span><span class="sxs-lookup"><span data-stu-id="166bd-110">If the requester receives one of these error codes, it must retry the shadow copy creation.</span></span>

<span data-ttu-id="166bd-111">登錄和檔案系統作業也可以進行交易。</span><span class="sxs-lookup"><span data-stu-id="166bd-111">Registry and file system operations can also be transacted.</span></span> <span data-ttu-id="166bd-112">在登錄的案例中，登錄寫入器負責確保交易一致性。</span><span class="sxs-lookup"><span data-stu-id="166bd-112">In the case of the registry, the registry writer is responsible for ensuring transactional consistency.</span></span> <span data-ttu-id="166bd-113">如果是交易式 NTFS (TxF) 檔案系統作業，系統提供者負責確保交易一致性。</span><span class="sxs-lookup"><span data-stu-id="166bd-113">In the case of Transactional NTFS (TxF) file system operations, the system provider is responsible for ensuring transactional consistency.</span></span> <span data-ttu-id="166bd-114">完成此作業的方法是在建立陰影複製時，將其裝載為讀取/寫入，以允許自動復原。</span><span class="sxs-lookup"><span data-stu-id="166bd-114">This is accomplished by mounting the shadow copy as read/write after it is created to allow for auto-recovery.</span></span> <span data-ttu-id="166bd-115">在自動復原階段，KTM 會復原任何未完成的交易。</span><span class="sxs-lookup"><span data-stu-id="166bd-115">During the auto-recovery phase, KTM rolls back any incomplete transactions.</span></span>

## <a name="identifying-and-creating-hard-links"></a><span data-ttu-id="166bd-116">識別和建立永久連結</span><span class="sxs-lookup"><span data-stu-id="166bd-116">Identifying and Creating Hard Links</span></span>

<span data-ttu-id="166bd-117">備份檔案時，備份應用程式必須識別每個檔案的所有硬連結，以避免備份相同的檔案一次以上。</span><span class="sxs-lookup"><span data-stu-id="166bd-117">When backing up files, a backup application must identify all hard links to each file to avoid backing up the same file more than once.</span></span> <span data-ttu-id="166bd-118">有兩個新函數可用於列舉永久連結： [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) 和 [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew)。</span><span class="sxs-lookup"><span data-stu-id="166bd-118">Two new functions are available for enumerating hard links: [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).</span></span>

<span data-ttu-id="166bd-119">同樣地，在還原檔案時，備份應用程式必須使用 [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) 函式來還原永久連結。</span><span class="sxs-lookup"><span data-stu-id="166bd-119">Similarly, when restoring files, the backup application must restore hard links using the [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) function.</span></span>

<span data-ttu-id="166bd-120">備份應用程式也必須在 \_ \_ 備份階段和 se 還原名稱中判斷提示「se 備份名稱」許可權，然後在 \_ \_ 還原階段進行。</span><span class="sxs-lookup"><span data-stu-id="166bd-120">Backup applications must also assert the SE\_BACKUP\_NAME privilege during the backup phase and the SE\_RESTORE\_NAME during the restore phase.</span></span>

## <a name="permissions-and-privileges-required-by-backup-applications"></a><span data-ttu-id="166bd-121">備份應用程式所需的許可權和許可權</span><span class="sxs-lookup"><span data-stu-id="166bd-121">Permissions and Privileges Required by Backup Applications</span></span>

<span data-ttu-id="166bd-122">還原系統檔案的備份應用程式需要下列許可權：</span><span class="sxs-lookup"><span data-stu-id="166bd-122">Backup applications that restore system files require the following privileges:</span></span>

<dl> <span data-ttu-id="166bd-123">SE \_ 備份 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="166bd-123">SE\_BACKUP\_NAME</span></span>  
<span data-ttu-id="166bd-124">SE \_ 還原 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="166bd-124">SE\_RESTORE\_NAME</span></span>  
<span data-ttu-id="166bd-125">SE \_ 安全性 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="166bd-125">SE\_SECURITY\_NAME</span></span>  
<span data-ttu-id="166bd-126">SE \_ 取得 \_ 擁有權 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="166bd-126">SE\_TAKE\_OWNERSHIP\_NAME</span></span>  
</dl>

<span data-ttu-id="166bd-127">備份應用程式也必須在 \_ 還原階段要求寫入擁有者存取權。</span><span class="sxs-lookup"><span data-stu-id="166bd-127">Backup applications must also request WRITE\_OWNER access rights during the restore phase.</span></span>

## <a name="windows-media-digital-rights-management"></a><span data-ttu-id="166bd-128">Windows Media 數位 Rights Management</span><span class="sxs-lookup"><span data-stu-id="166bd-128">Windows Media Digital Rights Management</span></span>

<span data-ttu-id="166bd-129">Windows Media 數位 Rights Management (DRM) 用戶端會在% ProgramData% \\ Microsoft \\ Windows DRM 目錄中維護敏感性狀態和授權檔案的目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="166bd-129">Windows Media Digital Rights Management (DRM) client maintains a directory of sensitive state and license files in the %ProgramData%\\Microsoft\\Windows\\DRM directory.</span></span> <span data-ttu-id="166bd-130">此目錄中的檔案應該與暫存和快取檔案同時進行清除。</span><span class="sxs-lookup"><span data-stu-id="166bd-130">The files in this directory should be purged at the same time as temporary and cache files.</span></span> <span data-ttu-id="166bd-131">若要確保 Windows DRM 用戶端維持一致的狀態，您必須避免備份或還原這些檔案。</span><span class="sxs-lookup"><span data-stu-id="166bd-131">To ensure that the Windows DRM client remains in a consistent state, you must avoid backing up or restoring these files.</span></span> <span data-ttu-id="166bd-132">此目錄列在 FilesNotToBackup 登錄機碼中。</span><span class="sxs-lookup"><span data-stu-id="166bd-132">This directory is listed in the FilesNotToBackup registry key.</span></span> <span data-ttu-id="166bd-133">如需 FilesNotToBackup 索引鍵的詳細資訊，請參閱 [產生備份組](generating-a-backup-set.md)。</span><span class="sxs-lookup"><span data-stu-id="166bd-133">For more information about the FilesNotToBackup key, see [Generating a Backup Set](generating-a-backup-set.md).</span></span>

## <a name="user-account-control"></a><span data-ttu-id="166bd-134">使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="166bd-134">User Account Control</span></span>

<span data-ttu-id="166bd-135">在 Windows Vista 中引進 (UAC) 的使用者帳戶控制，表示除非另有指定，否則應用程式必須在標準使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="166bd-135">The introduction of User Account Control (UAC) in Windows Vista means that unless specified otherwise, applications must run under a standard user account.</span></span> <span data-ttu-id="166bd-136">此外，UAC 的檔案和登錄虛擬化功能會改變儲存使用者資料的位置。</span><span class="sxs-lookup"><span data-stu-id="166bd-136">Additionally, the file and registry virtualization feature of UAC alters the locations where user data is stored.</span></span> <span data-ttu-id="166bd-137">如需如何使用 UAC 和檔案和登錄虛擬化的詳細資訊，請參閱下列參考：</span><span class="sxs-lookup"><span data-stu-id="166bd-137">For more information about how to work with UAC and file and registry virtualization, see the following references:</span></span>

<dl>

<span data-ttu-id="166bd-138">[Windows Vista 和 Windows Server 2008 開發人員故事： Windows Vista 應用程式開發需求適用于使用者帳戶控制 (UAC) ](/previous-versions/aa905330(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="166bd-138">[The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10))</span></span>  
<span data-ttu-id="166bd-139">[使用者帳戶控制相容性的 Windows Vista 應用程式開發需求](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="166bd-139">[Windows Vista Application Development Requirements for User Account Control Compatibility](/previous-versions/dotnet/articles/bb530410(v=msdn.10))</span></span>  
[<span data-ttu-id="166bd-140"> (UAC) 修補的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="166bd-140">User Account Control (UAC) Patching</span></span>](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a><span data-ttu-id="166bd-141">BitLocker 磁碟機加密</span><span class="sxs-lookup"><span data-stu-id="166bd-141">BitLocker Drive Encryption</span></span>

<span data-ttu-id="166bd-142">BitLocker 磁碟機加密是 Windows Vista Enterprise、Windows Vista 旗艦版以及 Windows Server 2008 中的一項新功能，可提供安全的啟動和完整磁片區加密。</span><span class="sxs-lookup"><span data-stu-id="166bd-142">BitLocker Drive Encryption is a new feature in Windows Vista Enterprise, Windows Vista Ultimate, and Windows Server 2008 that offers secure startup and full volume encryption.</span></span> <span data-ttu-id="166bd-143">瞭解這項功能對於執行離線還原的備份應用程式開發人員而言很重要，因為可能需要將資料還原至加密的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="166bd-143">Understanding this feature is important for developers of backup applications that perform offline restores where data may need to be restored onto an encrypted drive.</span></span>

<span data-ttu-id="166bd-144">若要將資料還原至加密的磁片磁碟機，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="166bd-144">To restore data onto an encrypted drive, perform the following steps:</span></span>

1.  <span data-ttu-id="166bd-145">解除鎖定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="166bd-145">Unlock the drive.</span></span>
2.  <span data-ttu-id="166bd-146">關閉 BitLocker 磁碟機加密。</span><span class="sxs-lookup"><span data-stu-id="166bd-146">Turn off BitLocker Drive Encryption.</span></span>
3.  <span data-ttu-id="166bd-147">執行還原。</span><span class="sxs-lookup"><span data-stu-id="166bd-147">Perform the restore.</span></span>
4.  <span data-ttu-id="166bd-148">開機進入還原的作業系統，然後開啟 BitLocker 磁碟機加密。</span><span class="sxs-lookup"><span data-stu-id="166bd-148">Boot into the restored operating system and turn on BitLocker Drive Encryption.</span></span>

<span data-ttu-id="166bd-149">如需有關 BitLocker 磁碟機加密的詳細資訊（包括逐步指南），請參閱 Microsoft TechNet Windows Vista 網站上的 [BitLocker 磁碟機加密](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) 。</span><span class="sxs-lookup"><span data-stu-id="166bd-149">For detailed information about BitLocker Drive Encryption, including a step-by-step guide, see [BitLocker Drive Encryption](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) on the Microsoft TechNet Windows Vista website.</span></span> <span data-ttu-id="166bd-150">如需 BitLocker 磁碟機加密 WMI 提供者的詳細資訊，請參閱 [BitLocker 磁碟機加密提供者](../secprov/bitlocker-drive-encryption-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="166bd-150">For information about the BitLocker Drive Encryption WMI provider, see [BitLocker Drive Encryption Provider](../secprov/bitlocker-drive-encryption-provider.md).</span></span>

 

 
