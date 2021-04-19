---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: 'E (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973645"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="9dc07-103">E (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="9dc07-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="9dc07-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="9dc07-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="9dc07-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**明確元件包含**</span><span class="sxs-lookup"><span data-stu-id="9dc07-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="9dc07-106">當元件參與備份或還原作業時，將元件的資訊新增至要求者的備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="9dc07-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="9dc07-107">要求者會使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 明確地在備份作業中包含元件，並使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 或 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) 在還原作業中明確包含元件。</span><span class="sxs-lookup"><span data-stu-id="9dc07-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="9dc07-108">如果已備份或還原任何寫入器的元件，則備份或還原作業中必須明確包含所有沒有可選取之祖系的其元件。</span><span class="sxs-lookup"><span data-stu-id="9dc07-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="9dc07-109">在作業中，必須明確包含要求者為參與備份或還原所選擇的可選取元件，而不需要選取的祖系。</span><span class="sxs-lookup"><span data-stu-id="9dc07-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="9dc07-110">具有可選取上階的其元件絕不會明確包含在內。</span><span class="sxs-lookup"><span data-stu-id="9dc07-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="9dc07-111">具有可選取上階的可選取元件可能會明確包含，如果是明確包含上階，則可以隱含地包含。</span><span class="sxs-lookup"><span data-stu-id="9dc07-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="9dc07-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**公開陰影複製**</span><span class="sxs-lookup"><span data-stu-id="9dc07-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="9dc07-113">在系統上掛接的磁片區陰影複製，可供管理該磁片區以外的進程使用。</span><span class="sxs-lookup"><span data-stu-id="9dc07-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="9dc07-114">裝入磁碟機號或目錄位置下的陰影複製磁片區稱為「本機公開」。</span><span class="sxs-lookup"><span data-stu-id="9dc07-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="9dc07-115">可透過共用存取的陰影複製磁片區 (除了用戶端可存取的陰影複製之外) 稱為「遠端公開」。</span><span class="sxs-lookup"><span data-stu-id="9dc07-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="9dc07-116">所有公開的陰影複製也會呈現陰影複製。</span><span class="sxs-lookup"><span data-stu-id="9dc07-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="9dc07-117">另請參閱 [*用戶端可存取陰影複製*](vssgloss-c.md)、 [*陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="9dc07-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



