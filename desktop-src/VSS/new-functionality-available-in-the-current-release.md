---
description: 磁碟區陰影複製服務的 Windows Server 2003 版本包含下列新功能：
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Windows Server 2003 中提供的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc444a062fd2e1dae33af80feb88e1da52452064d8ed38c2db6fd5f7f3ae2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591389"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Windows Server 2003 中提供的新功能

磁碟區陰影複製服務的 Windows Server 2003 版本包含下列新功能：

-   除了支援 [*selectability*](vssgloss-s.md) 之外，還支援使用 [*selectability for backup*](vssgloss-s.md) 來進行還原， (之前只是指 selectability) 。 如需詳細資訊，請參閱使用 [Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md) 。
-   引進 [*BackupShutdown*](vssgloss-b.md) 事件，指出 (要求者) 的 VSS 相容備份應用程式已關閉，是否已順利完成備份嘗試。 如需詳細資訊，請參閱 [處理 BackupShutdown 事件](handling-backupshutdown-events.md) 。
-   支援明確的寫入器元件相依性。 一種方法，用來描述和支援元件 (以及其定義) 由一個寫入器管理的元件，無法與其他寫入器所管理的元件分開備份或還原。 如需詳細資訊，請參閱 [由不同寫入器管理的元件之間](dependencies-between-components-managed-by-different-writers.md) 的相依性。
-   [*部分*](vssgloss-p.md)檔案作業的完整支援。 現在完全支援透過寫入器和要求者來備份和還原檔案區段。 如需部分檔案作業的詳細資訊，請參閱 [使用部分](working-with-partial-files.md) 檔案。
-   引進 [*差異*](vssgloss-d.md) 檔案以支援增量備份和還原作業。 如需詳細資訊，請參閱 [增量和差異備份](incremental-and-differential-backups.md) 。
-   引進備份架構作為概念，指出備份作業類型的寫入器支援層級。 如需詳細資訊，請參閱 [**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 。
-   在還原作業期間， ([*新的目標位置*](vssgloss-n.md)) 新的檔案還原目的地的要求者規格支援。 如需詳細資訊，請參閱 [在還原期間使用新目標](working-with-new-targets-during-restore.md) 。
-   在重新開機時支援條件式還原。 如需詳細資訊，請參閱重新開機時的 VSS \_ RME \_ 還原 \_ \_ \_ \_ （如果無法 \_ 取代 ([**VSE \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)) ）。
-   還原狀態和還原類型的定義。 如需詳細資訊，請參閱 [**vss \_ 還原 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) 和 [vss 還原狀態](vss-restore-state.md) 。
-   支援有關陰影複製狀態的寫入器查詢。 如需詳細資訊，請參閱 [**CVssWriter：： GetCoNtext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) 和 [**CVssWriter：： GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) 。
-   支援 Windows server 2003、Enterprise Edition 和 Windows Server 2003 Datacenter Edition 中可轉移的陰影複製。 如需詳細資訊，請參閱匯 [入可傳送的陰影複製磁片](importing-transportable-shadow-copied-volumes.md)區。

 

 



