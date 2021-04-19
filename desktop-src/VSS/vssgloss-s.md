---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: 'S (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970610"
---
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="77024-103">S (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="77024-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="77024-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="77024-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="77024-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**適用于備份的 selectability**</span><span class="sxs-lookup"><span data-stu-id="77024-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="77024-106">如果在備份作業中明確包含的元件是選擇性的，則會將元件視為可供選擇進行備份。</span><span class="sxs-lookup"><span data-stu-id="77024-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="77024-107">如果 [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)結構的 **bSelectable** 成員值為 **true**，就會啟用 Selectability for backup。</span><span class="sxs-lookup"><span data-stu-id="77024-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="77024-108">元件的 selectability 沒有預設值可進行備份;寫入器一律必須明確設定此值。</span><span class="sxs-lookup"><span data-stu-id="77024-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="77024-109">寫入器也會使用 selectability 進行還原，以組織其元件參與還原作業。</span><span class="sxs-lookup"><span data-stu-id="77024-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="77024-110">另請參閱可 *選取的元件*、 *還原 selectability*、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**用於還原的 selectability**</span><span class="sxs-lookup"><span data-stu-id="77024-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="77024-112">如果元件可以隱含地備份為元件集的一部分，則會被視為可選取的元件，然後在未設定其餘元件的情況下個別進行還原。</span><span class="sxs-lookup"><span data-stu-id="77024-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="77024-113">如果 [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)結構的 **bSelectableForRestore** 成員值為 **true**，就會啟用 Selectability for restore。</span><span class="sxs-lookup"><span data-stu-id="77024-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="77024-114">根據預設，元件的還原 selectability 為 **false**。</span><span class="sxs-lookup"><span data-stu-id="77024-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="77024-115">只有當元件尚未新增至備份檔案時，Selectability for restore 才有意義。</span><span class="sxs-lookup"><span data-stu-id="77024-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="77024-116">另請參閱可 *選取的元件*、 *selectability 以進行備份*、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**可選取的元件**</span><span class="sxs-lookup"><span data-stu-id="77024-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="77024-118">如果在備份或還原作業中明確包含的元件是選擇性的，則會將其視為可選取。</span><span class="sxs-lookup"><span data-stu-id="77024-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="77024-119">Selectability for backup 和 Selectability for restore 彼此獨立，因此可以針對這兩項作業、還原和不備份，或備份和不還原來選取元件。</span><span class="sxs-lookup"><span data-stu-id="77024-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="77024-120">寫入器也會使用 selectability 將其元件組織成群組：</span><span class="sxs-lookup"><span data-stu-id="77024-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="77024-121">如果要備份或還原寫入器，則在邏輯路徑中沒有可選取之祖系的其元件，一律必須明確包含。</span><span class="sxs-lookup"><span data-stu-id="77024-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="77024-122">如果至少包含一個可選取的上階，其具有可選取之祖系的元件只會包含在備份或還原中。</span><span class="sxs-lookup"><span data-stu-id="77024-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="77024-123">沒有可選取之祖系的可選取元件只能在備份或還原作業中明確包含。</span><span class="sxs-lookup"><span data-stu-id="77024-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="77024-124">具有可選取上階的可選取元件可以明確地包含在備份或還原作業中，或者如果包含其中一個可選取的祖系，則可以隱含地包含這些元件。</span><span class="sxs-lookup"><span data-stu-id="77024-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="77024-125">另請參閱 [*元件*](vssgloss-c.md)、 *selectability for backup*、 *selectability for restore*、 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件包含*](vssgloss-i.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**陰影複製**</span><span class="sxs-lookup"><span data-stu-id="77024-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="77024-127">原始磁片區內容的唯讀時間點複本。</span><span class="sxs-lookup"><span data-stu-id="77024-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="77024-128">每個陰影複製是以持續性 GUID 為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="77024-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="77024-129">也稱為磁片區陰影複製。</span><span class="sxs-lookup"><span data-stu-id="77024-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="77024-130">另請參閱 *陰影複製集*。</span><span class="sxs-lookup"><span data-stu-id="77024-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="77024-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**共用資料夾陰影複製**</span><span class="sxs-lookup"><span data-stu-id="77024-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="77024-132">Windows 的一項功能，可使用 VSS 建立磁片區的輕量線上備份複本。</span><span class="sxs-lookup"><span data-stu-id="77024-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="77024-133">用戶端可以透過 Windows shell 存取這些備份，以查看舊版檔案和復原錯誤，而不需要完整還原。</span><span class="sxs-lookup"><span data-stu-id="77024-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="77024-134">另請參閱 [*用戶端可存取陰影複製*](vssgloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**陰影複製集**</span><span class="sxs-lookup"><span data-stu-id="77024-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="77024-136">同時建立的磁片區陰影複製集合，並以一般的陰影複製集識別碼識別 (持續性 GUID) 值。</span><span class="sxs-lookup"><span data-stu-id="77024-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="77024-137">這是用來允許跨磁片區管理陰影複製作業的機制。</span><span class="sxs-lookup"><span data-stu-id="77024-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="77024-138">另請參閱 *陰影複製*。</span><span class="sxs-lookup"><span data-stu-id="77024-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="77024-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**軟體提供者**</span><span class="sxs-lookup"><span data-stu-id="77024-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="77024-140">在檔案系統與磁片區管理員之間的軟體層級攔截 i/o 要求的提供者。</span><span class="sxs-lookup"><span data-stu-id="77024-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="77024-141">另請參閱 [*硬體提供者*](vssgloss-h.md)和 [*提供者*](vssgloss-p.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**子元件**</span><span class="sxs-lookup"><span data-stu-id="77024-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="77024-143">任何具有邏輯路徑的元件，其中包含備份或還原) 父元件的可選取 (。</span><span class="sxs-lookup"><span data-stu-id="77024-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="77024-144">子元件必須有格式 {元件 \_ 名稱} \\ {子元件名稱} 的邏輯路徑 \_ 。</span><span class="sxs-lookup"><span data-stu-id="77024-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="77024-145">如果備份或還原) 上階的子元件可選取 (明確包含在備份或還原中，則子元件會隱含地包含在作業中。</span><span class="sxs-lookup"><span data-stu-id="77024-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="77024-146">隱含包含子群組件不會將其資料包含在備份元件檔中，而不論是否可針對 restore 或 Backup) 選擇 (。</span><span class="sxs-lookup"><span data-stu-id="77024-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="77024-147">另請參閱 [*元件*](vssgloss-c.md)、 [*邏輯路徑*](vssgloss-l.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**呈現的陰影複製**</span><span class="sxs-lookup"><span data-stu-id="77024-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="77024-149">系統的 Mount Manager 命名空間可以看到陰影複製的磁片區，這表示 **FindFirstVolume** 和 **FindNextVolume** 可以找到它，並產生磁片區抵達和起飛通知。</span><span class="sxs-lookup"><span data-stu-id="77024-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="77024-150">所有公開的陰影複製也會呈現陰影複製。</span><span class="sxs-lookup"><span data-stu-id="77024-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="77024-151">但是，不需要公開所呈現的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="77024-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="77024-152">如果陰影複製是可轉移的，則無法呈現。</span><span class="sxs-lookup"><span data-stu-id="77024-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="77024-153">另請參閱 [*公開陰影複製*](vssgloss-e.md)、可 [*轉移的陰影複製*](vssgloss-t.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**系統檔案保護**</span><span class="sxs-lookup"><span data-stu-id="77024-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="77024-155">請參閱 [*Windows 檔案保護*](vssgloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="77024-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**系統層級應用程式**</span><span class="sxs-lookup"><span data-stu-id="77024-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="77024-157">指出 VSS 通知寫入器的時間點。</span><span class="sxs-lookup"><span data-stu-id="77024-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="77024-158">初始化為系統層級應用程式的寫入器會在寫入器初始化為前端層級應用程式或後端層級應用程式之後收到通知。</span><span class="sxs-lookup"><span data-stu-id="77024-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="77024-159">另請參閱 [*應用層級*](vssgloss-a.md)、 [*後端層級*](vssgloss-b.md)應用程式、 [*前端層級應用*](vssgloss-f.md)程式。</span><span class="sxs-lookup"><span data-stu-id="77024-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="77024-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**系統提供者**</span><span class="sxs-lookup"><span data-stu-id="77024-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="77024-161">在 Windows 中提供的預設預先安裝提供者。</span><span class="sxs-lookup"><span data-stu-id="77024-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="77024-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**系統磁碟區資料夾**</span><span class="sxs-lookup"><span data-stu-id="77024-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="77024-163">共用的目錄，儲存網域公用檔案的共用複本，也就是在網域中的所有網域控制站之間複寫的檔案。</span><span class="sxs-lookup"><span data-stu-id="77024-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



