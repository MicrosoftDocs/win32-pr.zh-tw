---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: '我 (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690447"
---
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="86c87-103">我 (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="86c87-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="86c87-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="86c87-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="86c87-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**識別事件**</span><span class="sxs-lookup"><span data-stu-id="86c87-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="86c87-106">VSS 事件，指出寫入器或要求者需要查詢目前的寫入器。</span><span class="sxs-lookup"><span data-stu-id="86c87-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="86c87-107">它是用來建立目前寫入器的中繼資料資訊。</span><span class="sxs-lookup"><span data-stu-id="86c87-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="86c87-108">[*另請*](vssgloss-r.md)參閱要求者、[*寫入器*](vssgloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="86c87-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="86c87-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**隱含元件包含**</span><span class="sxs-lookup"><span data-stu-id="86c87-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="86c87-110">當它參與備份或還原作業時，不會將元件的資訊新增至要求者的備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="86c87-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="86c87-111">具有可選取上階的其元件只有在包含其上階時，才會隱含包含。</span><span class="sxs-lookup"><span data-stu-id="86c87-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="86c87-112">如果包含上階，則可以隱含地包含可選取的上階，或可能明確地包含上階。</span><span class="sxs-lookup"><span data-stu-id="86c87-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="86c87-113">其元件若沒有任何可選取的祖系，則不會隱含地包含在備份或還原作業中; 如果有任何寫入器元件參與，則所有這類元件都必須明確地新增至備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="86c87-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="86c87-114">在作業中，不能以隱含方式包含要求者所選擇的可選取元件，而要求者參與備份或還原，但必須明確地將其新增至備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="86c87-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="86c87-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**增量備份作業**</span><span class="sxs-lookup"><span data-stu-id="86c87-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="86c87-116">備份或還原作業只會在儲存最後一個完整、增量或差異備份之後所建立或變更的檔案上執行。</span><span class="sxs-lookup"><span data-stu-id="86c87-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="86c87-117">另請參閱 [*差異備份作業*](vssgloss-d.md)。</span><span class="sxs-lookup"><span data-stu-id="86c87-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



