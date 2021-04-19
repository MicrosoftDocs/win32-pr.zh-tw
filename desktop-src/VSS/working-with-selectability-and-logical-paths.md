---
description: 寫入器參與備份或還原作業，以及儲存的資料是哪一種，取決於哪個元件會明確包含在要求者的備份元件檔中，以及這些元件與寫入器元資料檔案中其他元件的邏輯路徑之間的關聯性。
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: 使用 Selectability 和邏輯路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973066"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="66e82-103">使用 Selectability 和邏輯路徑</span><span class="sxs-lookup"><span data-stu-id="66e82-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="66e82-104">寫入器參與備份或還原作業，以及儲存的資料是哪一種，取決於哪個元件會 [*明確包含*](vssgloss-e.md) 在要求者的備份元件檔中，以及這些元件與寫入器元資料檔案中其他元件的邏輯路徑之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="66e82-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="66e82-105">在 [*PrepareForBackup*](vssgloss-p.md) 事件產生之前，沒有任何元件的寫入器會新增至要求者的備份元件檔 (在進行備份作業) 或 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (事件的情況下，) 在還原作業的情況下不會收到任何事件，且不會參與備份或還原作業。</span><span class="sxs-lookup"><span data-stu-id="66e82-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="66e82-106">不過，要求者可以自由地在備份或還原中包含或排除任何指定的元件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="66e82-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="66e82-107">由寫入器管理並以 [*邏輯路徑* 表示的元件之間存在的任何階層](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="66e82-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="66e82-108">元件是否已指定為可 [*選取以進行備份*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="66e82-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="66e82-109">是否要將它指定為可 [*供還原*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="66e82-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="66e82-110">給定寫入器中的指定元件與其他寫入器中的其他元件之間是否有明確的相依性</span><span class="sxs-lookup"><span data-stu-id="66e82-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="66e82-111">有關這些問題的詳細資訊，請按下列主題：</span><span class="sxs-lookup"><span data-stu-id="66e82-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="66e82-112">元件的邏輯路徑</span><span class="sxs-lookup"><span data-stu-id="66e82-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="66e82-113">使用 Selectability 進行備份</span><span class="sxs-lookup"><span data-stu-id="66e82-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="66e82-114">使用 Selectability 進行還原和子元件</span><span class="sxs-lookup"><span data-stu-id="66e82-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="66e82-115">Selectability 和使用元件屬性</span><span class="sxs-lookup"><span data-stu-id="66e82-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="66e82-116">不同寫入器所管理元件之間的相依性</span><span class="sxs-lookup"><span data-stu-id="66e82-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



