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
# <a name="working-with-new-targets-during-restore"></a>在還原期間使用新目標

要求者可能需要將檔案還原至檔案集的預設路徑以外的位置或其 [*替代位置對應*](vssgloss-a.md)。 有許多原因可能會發生這種情況，例如，沒有可存取的還原目的地，或要求者使用者刻意要求將檔案還原至先前未知的位置。 在這種情況下，要求者會使用新的目的機制來指出寫入器已將檔案還原至磁片上的其他區域。

並非所有寫入器都支援要求者變更檔案的還原目的地。 要求者必須檢查寫入器的備份架構遮罩 (由 [**IVssExamineWriterMetadata：：) GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) 傳回，然後確認它包含 VSS \_ BS \_ 寫入器 \_ 支援 \_ 新的 \_ 目標旗標，以驗證寫入器支援。

要求者會透過 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) 方法來表示這類還原。 除了指定檔案規格和原始和新的還原目的地，要求者會指定元件資訊，也就是邏輯路徑和元件名稱。

使用哪個元件的資訊取決於管理檔案的元件是否已 [*明確納入*](vssgloss-e.md) 或 [*隱含地包含*](vssgloss-i.md) 在備份中的新目標。

如果已明確包含管理元件，則會使用其資訊。 如果管理元件是隱含包含的，則它是元件集中的子元件。 在此情況下，會使用元件集的定義元件資訊。

處理 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 事件時，寫入器應該檢查是否有任何檔案已還原至新的位置。 您可以使用 [**>ivsscomponent：： GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) 和 [**>ivsscomponent：： GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget) 方法來完成此動作。

使用的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例取決於檔案的管理元件是明確或隱含地新增至備份。

 

 



