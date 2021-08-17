---
description: 當寫入器在寫入器元資料檔案中指定其資料的還原方式時，還原作業的設定實際上會在資料備份期間開始。
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: 設定 VSS 還原方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f7b0d138555b1e10dba55483c694c08a649e97e59cb66ed65c1a276187d3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751719"
---
# <a name="setting-vss-restore-methods"></a>設定 VSS 還原方法

當寫入器在寫入器元資料檔案中指定其資料的還原方式時，還原作業的設定實際上會在資料備份期間開始。

這些規格（稱為 [*還原方法*](vssgloss-r.md) 或原始 [*還原目標*](vssgloss-r.md)）可以在還原期間由寫入器設定新的還原目標或由要求者還原至新位置來修改， (查看 [非預設備份和還原位置](non-default-backup-and-restore-locations.md)) 。

藉由呼叫 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)，寫入器會指出應該在其寫入器元資料檔案中使用哪一個還原方法。 Restore 方法是設定為全作者，並套用至寫入器管理之所有元件中的所有檔案。

要求者取得 (，且必須藉由呼叫 [**IVssExamineWriterMetadata：： GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)來) 這項資訊。

Restore 方法是由 [**VSS \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 列舉所定義，它會傳遞至 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) ，並從 [**IVssExamineWriterMetadata：： GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)傳回。

寫入器元資料檔案支援下列有效的還原方法 (VSS \_ RME 未定義的還原方法 \_ 表示) 的寫入器錯誤。 這些圖表摘要說明各種支援和已定義的還原方法， (VSS \_ RME \_ 自訂並沒有相關聯的圖表，因為根據定義，它是寫入器特有的，而且必須遵循特定的寫入器 api 和檔) ：

-   VSS \_ RME \_ 還原（ \_ 如果沒有的話） \_ \_ 。 如果磁片上沒有任何檔案，請將元件檔案還原至磁片。 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)事件之後，應檢查目標檔案狀態。
    ![此圖顯示 VSS_RME_RESTORE_IF_NOT_THERE 的疑難排解樹狀目錄。](images/rint.png)
-   VSS \_ RME \_ RESTORE \_ 是否 \_ 可以 \_ REPLACE。 如果可以取代所有檔案，請將檔案還原至磁片。 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)事件之後，應檢查目標檔案狀態。
    ![此圖顯示 VSS_RME_RESTORE_IF_CAN_REPLACE 的疑難排解樹狀目錄。](images/ricr.png)
-   VSS \_ RME \_ 停止 \_ 還原 \_ 啟動。 在還原檔案之前，將會停止服務。
    ![此圖顯示 VSS_RME_STOP_RESTORE_START 的疑難排解樹狀目錄。](images/srr.png)
-   VSS \_ RME \_ 還原 \_ 至 \_ 替代 \_ 位置。 將檔案還原到其他位置的磁片。 替代位置對應是在寫入器元資料檔案中指定。
    ![此圖顯示 VSS_RME_RESTORE_TO_ALTERNATE_LOCATION 的疑難排解樹狀目錄。](images/rtal.png)
-   VSS \_ RME \_ \_ 在 \_ 重新開機時還原。 重新開機電腦時，會將檔案還原 (覆寫) 。
    ![此圖顯示 VSS_RME_RESTORE_AT_REBOOT 的疑難排解樹狀目錄。](images/rar.png)
-   \_ \_ \_ \_ \_ 如果 \_ 無法 \_ 取代，VSS RME 會在重新開機時還原。 如果檔案無法還原到執行中系統上的磁片，則會在電腦重新開機時還原 (覆寫) 。
    ![顯示疑難排解樹 forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE 的圖表。 ](images/raricr.png)
-   VSS \_ RME \_ 自訂。 沒有任何預先定義的方法可運作;備份應用程式必須使用特製化的 Api 來執行還原作業。 針對此備份方法，要求者必須完全瞭解有問題的寫入器。 請參閱目前支援之實例的 [特殊 VSS 使用案例](special-vss-usage-cases.md) 。

 

 



