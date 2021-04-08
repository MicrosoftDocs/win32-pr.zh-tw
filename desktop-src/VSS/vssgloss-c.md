---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: 'C (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690455"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="ead25-103">C (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="ead25-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ead25-104">[](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ead25-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ead25-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**憑證授權單位單位**</span><span class="sxs-lookup"><span data-stu-id="ead25-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-106">信賴于發出憑證的實體，判斷要求憑證的收件者個人、電腦或組織滿足已建立原則的條件。</span><span class="sxs-lookup"><span data-stu-id="ead25-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="ead25-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**用戶端可存取的陰影複製**</span><span class="sxs-lookup"><span data-stu-id="ead25-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-108">系統提供者所建立的陰影複製，可支援共用資料夾陰影複製和其他復原機制，可讓用戶端查看舊版檔案和復原錯誤，而不需要完整還原。</span><span class="sxs-lookup"><span data-stu-id="ead25-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="ead25-109">用戶端可存取的陰影複製是使用 [**\_ vss \_ 快照集 \_ 內容**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)列舉的 **vss \_ CTX \_ 用戶端 \_ 可存取** 值所建立。</span><span class="sxs-lookup"><span data-stu-id="ead25-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="ead25-110">此外，vss \_ \_ \_ \_ [**\_ 磁片區快照集 \_ \_ \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉的 vss VOLSNAP ATTR 用戶端可存取值，會自動針對用戶端可存取的陰影複製進行設定。</span><span class="sxs-lookup"><span data-stu-id="ead25-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="ead25-111">另請參閱 [*共用資料夾陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="ead25-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ead25-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**元件**</span><span class="sxs-lookup"><span data-stu-id="ead25-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-113">由寫入器定義的檔案群組，必須在備份和還原作業期間做為一個單位來處理。</span><span class="sxs-lookup"><span data-stu-id="ead25-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="ead25-114">另請參閱 [*資料庫元件*](vssgloss-d.md)、檔案 [*群組元件*](vssgloss-f.md)。</span><span class="sxs-lookup"><span data-stu-id="ead25-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="ead25-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**元件相依性**</span><span class="sxs-lookup"><span data-stu-id="ead25-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-116">如果元件 (以及它定義的元件集定義) 由一個寫入器管理，則無法與其他寫入器管理的元件分開備份或還原。</span><span class="sxs-lookup"><span data-stu-id="ead25-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="ead25-117">相依性不會指出元件之間的喜好設定順序，以及其相依的元件：相依性只會指出元件與其相依的元件必須同時進行備份或還原。</span><span class="sxs-lookup"><span data-stu-id="ead25-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="ead25-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**元件模式**</span><span class="sxs-lookup"><span data-stu-id="ead25-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-119">備份或還原作業利用寫入器元件資訊的模式。</span><span class="sxs-lookup"><span data-stu-id="ead25-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="ead25-120">另請參閱可 [*選取的元件*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="ead25-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ead25-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**元件集**</span><span class="sxs-lookup"><span data-stu-id="ead25-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-122">一組元件，其中至少有一個可選取的 (用於備份或還原) 元件，以及依其邏輯路徑組織在階層中的數個其元件。</span><span class="sxs-lookup"><span data-stu-id="ead25-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="ead25-123">備份或還原作業中的隱含參與取決於最上層可選取元件的明確包含。</span><span class="sxs-lookup"><span data-stu-id="ead25-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="ead25-124">只有這個可選取元件的元件資訊會包含在備份元件檔中。</span><span class="sxs-lookup"><span data-stu-id="ead25-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="ead25-125">元件集可能包含可選取和其的子元件。</span><span class="sxs-lookup"><span data-stu-id="ead25-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="ead25-126">另請參閱 [*邏輯路徑*](vssgloss-l.md)、可 [*選取的元件*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="ead25-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="ead25-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**複製時寫入陰影複製**</span><span class="sxs-lookup"><span data-stu-id="ead25-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-128">藉由只儲存原始磁片區的差異所建立的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="ead25-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="ead25-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**損毀一致狀態**</span><span class="sxs-lookup"><span data-stu-id="ead25-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="ead25-130">磁片的狀態，相當於在突然關閉系統的嚴重失敗之後所發現的磁片。</span><span class="sxs-lookup"><span data-stu-id="ead25-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="ead25-131">從這類陰影複製集進行還原，相當於在突然關機後重新開機。</span><span class="sxs-lookup"><span data-stu-id="ead25-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="ead25-132">這是不支援寫入器時，已陰影複製之資料的預設狀態。</span><span class="sxs-lookup"><span data-stu-id="ead25-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



