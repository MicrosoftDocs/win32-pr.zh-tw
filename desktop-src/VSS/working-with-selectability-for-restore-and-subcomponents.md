---
description: Selectability for restore 可讓要求者判斷何時可以個別還原元件。
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: 使用 Selectability 進行還原和子元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d988f4c4e029c7dd8623ad22fcaee7662d33e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511501"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>使用 Selectability 進行還原和子元件

Selectability for restore 可讓要求者判斷何時可以個別還原元件。 包含在備份中的元件可能會以下列兩種方式之一顯示：

-   元件可能已 [*明確包含*](vssgloss-e.md) 在備份中。 這些元件在 [備份元件] 檔中有對應的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例。 這些元件包含在使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)的還原中。
-   元件可能已 [*隱含地包含*](vssgloss-i.md) 在備份中。 這些元件在備份元件檔中沒有對應的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例;不過，檔中的某些祖系元件一律會有 **>ivsscomponent** 實例。 這些元件包含在使用 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)的還原中。

任何已明確包含在備份中的元件都可以個別選取進行還原，而不論其 selectability 還原值為何。 要求者會呼叫 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)，並傳入寫入器識別碼、邏輯路徑和特定元件的名稱。 已隱含包含在備份中的元件將會在已明確包含的上階還原時還原。 如果隱含包含的元件被標示為可選取進行還原，則可以個別選取以進行還原。 要求者會先在最近明確包含的上階元件上呼叫 **>ivssbackupcomponents：： SetSelectedForRestore** ，然後在上階元件上呼叫 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) ，以選取要用於還原的隱含包含元件。 完成此操作後，只會還原隱含選取的元件;元件集中的所有其他元件都不會還原。

不同于備份的 selectability，當使用 [**IVssCreateWriterMetadata：： AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)新增元件時，必須一律明確設定，而 selectability for restore 的預設值為 false （可以覆寫）。

因為最上層元件 (具有空白邏輯路徑的元件) 只能明確包含在備份中，所以 selectability for restore 對於這些元件沒有任何意義。

 

 



