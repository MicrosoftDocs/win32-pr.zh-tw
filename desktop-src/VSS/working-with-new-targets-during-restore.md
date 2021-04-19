---
description: 要求者可能需要將檔案還原至檔案集的預設路徑以外的位置或其替代位置對應。
ms.assetid: ce11485c-da0e-4c16-962e-eeedc2da3de4
title: 在還原期間使用新目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f20a6e8c27c186648d0f662921160ab5c76988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970997"
---
# <a name="working-with-new-targets-during-restore"></a><span data-ttu-id="64128-103">在還原期間使用新目標</span><span class="sxs-lookup"><span data-stu-id="64128-103">Working with New Targets during Restore</span></span>

<span data-ttu-id="64128-104">要求者可能需要將檔案還原至檔案集的預設路徑以外的位置或其 [*替代位置對應*](vssgloss-a.md)。</span><span class="sxs-lookup"><span data-stu-id="64128-104">A requester may need to restore files to a location indicated by something other than a file set's default path or its [*alternate location mapping*](vssgloss-a.md).</span></span> <span data-ttu-id="64128-105">有許多原因可能會發生這種情況，例如，沒有可存取的還原目的地，或要求者使用者刻意要求將檔案還原至先前未知的位置。</span><span class="sxs-lookup"><span data-stu-id="64128-105">There are many reasons why this might happen—for example, neither restore destination was accessible, or a requester user intentionally requests that files be restored to some previously unknown location.</span></span> <span data-ttu-id="64128-106">在這種情況下，要求者會使用新的目的機制來指出寫入器已將檔案還原至磁片上的其他區域。</span><span class="sxs-lookup"><span data-stu-id="64128-106">In this case, the requester uses the new target mechanism to indicate to writers that it has restored a file to a different area on disk.</span></span>

<span data-ttu-id="64128-107">並非所有寫入器都支援要求者變更檔案的還原目的地。</span><span class="sxs-lookup"><span data-stu-id="64128-107">Not all writers support a requester changing the restore destination of a file.</span></span> <span data-ttu-id="64128-108">要求者必須檢查寫入器的備份架構遮罩 (由 [**IVssExamineWriterMetadata：：) GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) 傳回，然後確認它包含 VSS \_ BS \_ 寫入器 \_ 支援 \_ 新的 \_ 目標旗標，以驗證寫入器支援。</span><span class="sxs-lookup"><span data-stu-id="64128-108">A requester needs to verify writer support by checking the writer's backup schema mask (returned by [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)) and verifying that it contains the VSS\_BS\_WRITER\_SUPPORTS\_NEW\_TARGET flag.</span></span>

<span data-ttu-id="64128-109">要求者會透過 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) 方法來表示這類還原。</span><span class="sxs-lookup"><span data-stu-id="64128-109">The requester indicates such a restoration through the [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) method.</span></span> <span data-ttu-id="64128-110">除了指定檔案規格和原始和新的還原目的地，要求者會指定元件資訊，也就是邏輯路徑和元件名稱。</span><span class="sxs-lookup"><span data-stu-id="64128-110">In addition to specifying a file specification and an original and a new restore destination, the requester specifies component information—a logical path and component name.</span></span>

<span data-ttu-id="64128-111">使用哪個元件的資訊取決於管理檔案的元件是否已 [*明確納入*](vssgloss-e.md) 或 [*隱含地包含*](vssgloss-i.md) 在備份中的新目標。</span><span class="sxs-lookup"><span data-stu-id="64128-111">Which component's information is used depends on whether or not the component managing the file having a new target added was [*explicitly included*](vssgloss-e.md) or [*implicitly included*](vssgloss-i.md) in the backup.</span></span>

<span data-ttu-id="64128-112">如果已明確包含管理元件，則會使用其資訊。</span><span class="sxs-lookup"><span data-stu-id="64128-112">If the managing component was explicitly included, then its information is used.</span></span> <span data-ttu-id="64128-113">如果管理元件是隱含包含的，則它是元件集中的子元件。</span><span class="sxs-lookup"><span data-stu-id="64128-113">If the managing component was implicitly included, it is a subcomponent in a component set.</span></span> <span data-ttu-id="64128-114">在此情況下，會使用元件集的定義元件資訊。</span><span class="sxs-lookup"><span data-stu-id="64128-114">In this case, the component set's defining component's information is used.</span></span>

<span data-ttu-id="64128-115">處理 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 事件時，寫入器應該檢查是否有任何檔案已還原至新的位置。</span><span class="sxs-lookup"><span data-stu-id="64128-115">While handling the [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) event, writers should check to see if any of its files were restored to a new location.</span></span> <span data-ttu-id="64128-116">您可以使用 [**>ivsscomponent：： GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) 和 [**>ivsscomponent：： GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) 方法來完成此動作。</span><span class="sxs-lookup"><span data-stu-id="64128-116">This can be done by using the [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) and [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) methods.</span></span>

<span data-ttu-id="64128-117">使用的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例取決於檔案的管理元件是明確或隱含地新增至備份。</span><span class="sxs-lookup"><span data-stu-id="64128-117">The instance of the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface that is used depends on whether the file's managing component was explicitly or implicitly added to the backup.</span></span>

 

 



