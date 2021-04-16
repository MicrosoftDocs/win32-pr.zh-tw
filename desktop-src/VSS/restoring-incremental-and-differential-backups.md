---
description: 還原 VSS 下的增量或差異備份，與任何其他 VSS 還原作業並無太大差異。
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: 還原增量和差異備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 639919ea24f12fbc036116bd89b1630321cbae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513129"
---
# <a name="restoring-incremental-and-differential-backups"></a>還原增量和差異備份

還原 VSS 下的增量或差異備份，與任何其他 VSS 還原作業並無太大差異。

寫入器可以修改還原目標或要求導向目標，要求者必須處理替代位置對應和新目標，就像任何其他還原一樣。 不過，在處理增量或差異備份的還原時，有兩個重要的問題要注意：額外的還原和備份戳記。

## <a name="additional-restores"></a>額外的還原

第一個問題是額外的還原。 備份操作員可能需要使用初始完整和後續增量或差異備份媒體作為來源，來執行數個還原作業。

有些寫入器通常是使用 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)處理 [*PostRestore*](vssgloss-p.md)事件的一部分，使用已還原的檔案來執行目前在磁片上的資料更新。 對於這些寫入器的某些寫入器效率很低（或危險），以重複更新還原檔案中的磁片資料。

因此，備份應用程式必須藉由呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)來指出元件或元件的設定何時可能需要後續還原。

寫入器會呼叫 [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) ，以判斷備份操作員是否計畫對元件或元件集進行更多的還原。

如果要求者未呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)，則 [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) 會傳回 false，而寫入器可以執行所需的任何還原後處理。

如果已呼叫 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) ， [**>ivsscomponent：： GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) 會傳回 **true**，而寫入器應該決定如何處理還原後的作業，例如，寫入器可能會選擇不更新其在磁片上的資料。

## <a name="backup-stamps"></a>備份戳記

在上一次完整備份操作的過程中，寫入器可能已在要求者的備份元件檔中儲存備份戳記。

備份戳記會儲存為字串，且其格式和資訊不會智慧型給要求者。 因此，要求者無法直接使用備份戳記資訊。

相反地，其工作是在產生增量備份的 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)事件之前，先呼叫 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)方法，以將該資訊提供給寫入器。

要求者會以元件為基礎來執行此操作。 要求者會使用 [**>ivsscomponent：： GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)檢查預存元件或元件集的備份戳記資訊。

如果備份戳記資訊適用于正在進行的還原類型，則會使用 [**>ivssbackupcomponents：： SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) 方法，讓它成為元件最後一次備份的時間戳記。

寫入器會使用 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)來復原備份戳記資訊。 此類別的寫入器產生了初始備份戳記，因此寫入器能夠將此戳記解碼並使用資訊。 根據這一點，在處理 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 事件時，寫入器可以選擇採取動作，例如變更還原目標或要求導向目標。

 

 



