---
description: 有時候最好在一個系統上建立陰影複製，但在第二個系統上使用陰影複製。
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: 匯入可轉移的陰影複製磁片區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d259fbc047d088ee1f7064804a3ee98fe48da1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115164"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>匯入可轉移的陰影複製磁片區

有時候最好在一個系統上建立陰影複製，但在第二個系統上使用陰影複製。

假設要備份的資料通常是由指定的系統管理， (*systemOne* 在正常作業期間) ，而且這項資料實際上儲存在存放裝置陣列或設備上。

為了儘量減少 *systemOne* (的任何中斷情況，因為備份作業可能會耗用大量資源) ，因此最好使用 *systemTwo* 備份來執行備份，該備份伺服器可存取與 *systemOne* 相同的存放裝置陣列。

為了確保適當的陰影複製（與 *systemOne* 上的寫入器協同作業，並適當地保留狀態以進行進行中的工作），陰影複製應該由 *systemOne* 執行。

因此， *systemOne* 必須建立可 [*轉移的陰影複製*](vssgloss-t.md)， *systemTwo* 接著會匯入。

**Windows server 2003、Standard Edition、Windows server 2003、Web Edition 和 WINDOWS XP：** 不支援可轉移的陰影複製集。 所有版本的 Windows Server 2003 Service Pack 1 (SP1) 支援可轉移的陰影複製集。

匯入可轉移陰影複製的一般範例，可透過下列方式繼續進行：

1.  一開始，存放裝置陣列所提供的邏輯單元 (LUN) 會掛接為 *systemOne* 上的磁片區 (例如 F： ) 。
2.  在 *systemOne* 上執行的要求者會具現化 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 的實例，並繼續進行備份的準備。  (參閱 [備份初始化的總覽](overview-of-backup-initialization.md)、 [備份探索階段的總覽](overview-of-the-backup-discovery-phase.md)，以及詳細資訊的備份 [前工作總覽](overview-of-pre-backup-tasks.md) 。 ) 
3.  *SystemOne* 上的要求者會修改通常用於本機備份作業的陰影複製內容 (**VSS \_ CTX \_ 應用程式 \_ 備份**) ，表示將會建立可轉移的陰影複製 (**VSS \_ VOLSNAP \_ ATTR 可 \_ 轉移**) 。 可轉移的屬性也可以加入至其他陰影複製內容。
4.  透過 **vss \_ CTX \_ 應用程式 \_ 備份** \| **vss \_ VOLSNAP \_ ATTR 可 \_ 轉移** 的陰影複製內容， *systemOne* 的要求者會藉由呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)來建立陰影複製。
5.  *SystemOne* 會使用 [**>ivssbackupcomponents：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) 來儲存備份元件檔和 [**IVssExamineWriterMetadata：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) 的目前狀態，以儲存每個寫入器的寫入器元資料檔案。 接著，會將包含這些檔的 XML 字串提供給在 *systemTwo* 上執行的要求者。

    要求者會將備份元件檔傳送至 *systemTwo*。

    請注意，如果陰影複製的目的是要進行備份，則 *systemOne* 上的要求者在此時不會釋放其 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 實例。 介面應該保持開啟，直到 *systemTwo* 成功完成其備份作業為止。 只有在要求者發出 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) 事件時才應該發出，因為有些寫入器會截斷記錄，並在成功備份之後執行其他工作。 如果陰影複製的目標是資料採礦或其他用途，則可以在此步驟關閉介面。

6.  然後， *systemTwo* 的要求者會呼叫 [**>ivssbackupcomponents：： ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) ，以存取 *systemOne* 上要求者所建立的陰影複製。
    > [!Note]  
    > 要求者負責序列化「匯入陰影複製」作業。 此外，如果對 [**>ivssbackupcomponents：： ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) 的呼叫失敗，VSS 將不會自行清除 lun。 要求者必須起始 Lun 的清除。

     

7.  *SystemTwo* 的要求者會繼續備份陰影複製的材質，就像是備份本身所建立的陰影複製一樣 (查看) [檔的實際備份](overview-of-actual-backup-of-files.md)。

    *SystemTwo* 上的要求者會在匯入的陰影複製上，使用 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)取得陰影複製的 [*裝置物件*](vssgloss-d.md)，並將其附加至從中繼資料取得的原始檔案路徑開頭，以存取要備份的檔案。

8.  使用陰影複製之後， *systemTwo* 上的要求者必須刪除陰影複製。 如同不可傳送的陰影複製，如果陰影複製內容表示自動發行陰影複製 (例如， **VSS \_ CTX \_ 備份**) ，然後在 *systemTwo* 上釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ，將會導致 VSS 服務刪除陰影複製。 否則，如果內容指出持續的陰影複製 (例如 **VSS \_ CTX \_ 應用程式 \_ 復原**) ，則 *systemTwo* 上的要求者必須明確地刪除陰影複製。

    然後， *systemTwo* 的要求者會對 *systemOne* 發出要求，告知要求者已完成可轉移陰影複製的備份。

9.  在 *systemOne* 上的要求者收到通知，指出 *systemTwo* 的要求者已完成可轉移陰影複製的備份之後，它會透過呼叫 **>ivssbackupcomponents：： BackupComplete** 來產生 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)事件，以通知其系統上的寫入器。 此時， *systemOne* 上的要求者可以釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)的實例。

叢集中 **的可轉移陰影複製：** 只要原始磁片區裝載于叢集內，就必須從叢集外部匯入可轉移的陰影複製。 如需在叢集中執行快速復原的相關資訊，請參閱 [使用可轉移陰影複製磁片](fast-recovery-using-transportable-shadow-copied-volumes.md)區的快速復原。

 

 



