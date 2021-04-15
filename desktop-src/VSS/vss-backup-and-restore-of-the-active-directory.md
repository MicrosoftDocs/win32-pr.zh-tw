---
description: Active Directory 寫入器在備份作業期間不需要執行任何特殊動作。
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Active Directory 的 VSS 備份和還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511521"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="a1db8-103">Active Directory 的 VSS 備份和還原</span><span class="sxs-lookup"><span data-stu-id="a1db8-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="a1db8-104">Active Directory 寫入器在備份作業期間不需要執行任何特殊動作。</span><span class="sxs-lookup"><span data-stu-id="a1db8-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="a1db8-105">寫入器會提供元件和檔案集資訊給要求者，而要求者會使用該資訊來決定要複製到備份媒體的檔案。</span><span class="sxs-lookup"><span data-stu-id="a1db8-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="a1db8-106">不需要使用任何特殊的 Api 來備份 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="a1db8-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="a1db8-107">執行還原的方式取決於 Active Directory 是否要在發生嚴重損壞修復作業時還原，或還原到執行 Active Directory 的系統。</span><span class="sxs-lookup"><span data-stu-id="a1db8-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="a1db8-108">此外，Active Directory 狀態的備份副本存留期可能會因為 Active Directory 的標記而發生問題。</span><span class="sxs-lookup"><span data-stu-id="a1db8-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="a1db8-109">在嚴重損壞修復之後 Active Directory 還原</span><span class="sxs-lookup"><span data-stu-id="a1db8-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="a1db8-110">在需要嚴重損壞修復的損毀之後，Active Directory 可以還原為作業系統狀態還原的一部分。</span><span class="sxs-lookup"><span data-stu-id="a1db8-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="a1db8-111">這項還原作業基本上是 writerless 還原。</span><span class="sxs-lookup"><span data-stu-id="a1db8-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="a1db8-112">Active Directory 正在執行的系統上還原</span><span class="sxs-lookup"><span data-stu-id="a1db8-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="a1db8-113">如果 Active Directory 目前正在伺服器上執行，則必須以目錄服務還原模式重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="a1db8-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="a1db8-114">作業系統會在沒有 Active Directory 的情況下執行，而所有使用者驗證都會透過登錄中的安全性帳戶管理員 (SAM) 進行。</span><span class="sxs-lookup"><span data-stu-id="a1db8-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="a1db8-115">只有系統管理員才有復原 Active Directory 的許可權。</span><span class="sxs-lookup"><span data-stu-id="a1db8-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="a1db8-116">進入目錄服務還原模式之後，就可以正常進行 VSS 還原。</span><span class="sxs-lookup"><span data-stu-id="a1db8-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="a1db8-117">沒有理由使用非 VSS Win32 Active Directory Api 來還原 Active Directory 狀態。</span><span class="sxs-lookup"><span data-stu-id="a1db8-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="a1db8-118">Active Directory 還原和 Active Directory 的標記</span><span class="sxs-lookup"><span data-stu-id="a1db8-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="a1db8-119">任何復原方案都應該確保備份的存留期不應超過 Active Directory 的標記存留期 (預設值為60天) 。</span><span class="sxs-lookup"><span data-stu-id="a1db8-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="a1db8-120">還原超過標記的備份將會導致網域控制站有不會複寫到其他伺服器的物件。</span><span class="sxs-lookup"><span data-stu-id="a1db8-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="a1db8-121">未複寫的物件將不會在該 (還原) 網域控制站上自動刪除，因為已刪除其他複本上的那些物件的標記。</span><span class="sxs-lookup"><span data-stu-id="a1db8-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="a1db8-122">系統管理員必須手動刪除未複寫的已還原網域控制站上的每個物件。</span><span class="sxs-lookup"><span data-stu-id="a1db8-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="a1db8-123">不支援 Active Directory 的增量備份;需要完整備份。</span><span class="sxs-lookup"><span data-stu-id="a1db8-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



