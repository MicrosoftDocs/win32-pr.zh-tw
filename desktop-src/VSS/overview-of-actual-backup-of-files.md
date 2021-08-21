---
description: VSS 可讓要求者存取包含要備份之資料的磁片區陰影複製，以及將資料複製到備份媒體。
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: 檔的實際備份總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c4f2d4c0d43e614fe956b2ca3b3253566f0d05a7c27a4e7337ae3b2cd6784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056376"
---
# <a name="overview-of-actual-backup-of-files"></a>檔的實際備份總覽

VSS 可讓要求者存取包含要備份之資料的磁片區陰影複製，以及將資料複製到備份媒體。 寫入器通常會在此程式期間繼續正常運作。 如需詳細資訊，請參閱 [在 VSS 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md)。

下表顯示備份檔案所需的動作和事件順序。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>要求者動作</th>
<th>事件</th>
<th>寫入器動作</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>存取陰影複製磁片區上的檔案 (參閱 <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>>ivssbackupcomponents：： GetSnapshotProperties</strong></a>、 <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>) </td>
<td>無</td>
<td>無</td>
</tr>
<tr class="even">
<td>產生要備份的檔案清單，並將檔案資料複製到備份媒體。</td>
<td>無</td>
<td>無</td>
</tr>
<tr class="odd">
<td>使用 <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>>ivssbackupcomponents：： SetBackupSucceeded</strong></a>指出備份成功或失敗。</td>
<td>無</td>
<td>無</td>
</tr>
<tr class="even">
<td>要求者會藉由呼叫 <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>>ivssbackupcomponents：： BackupComplete</strong></a>來指出備份已完成。</td>
<td><a href="vssgloss-b.md"><em>BackupComplete</em></a></td>
<td>執行任何備份後清除 (參閱 <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter：： OnBackupComplete</strong></a>、 <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>、 <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>>ivsscomponent</strong></a>) 。</td>
</tr>
<tr class="odd">
<td>要求者會使用<a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>來等候所有寫入器認可<a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>>ivssbackupcomponents：： BackupComplete</strong></a>事件的接收。 它也應該驗證寫入器狀態 (請參閱 <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>>ivssbackupcomponents：： GatherWriterStatus</strong></a>， <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>>ivssbackupcomponents：： GetWriterStatus</strong></a>) 。 要求者目前必須呼叫 <strong>GatherWriterStatus</strong> ，使寫入器會話設定為已完成狀態。
<blockquote>
[!Note]<br />
只有 Windows Server 2008 （含 Service Pack 2） (SP2) 及更早版本才需要此功能。
</blockquote>
<br/></td>
<td>無</td>
<td>無</td>
</tr>
<tr class="even">
<td>將備份元件檔和每個寫入器元資料檔案儲存至 XML 檔，這些檔可以寫入至備份媒體 (參閱 <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>>ivssbackupcomponents：： SaveAsXML</strong></a> 和 <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata：： SaveAsXML</strong></a>) 。</td>
<td>無</td>
<td>無</td>
</tr>
</tbody>
</table>



 

## <a name="writer-actions-during-backup-of-files"></a>備份檔案期間的寫入器動作

陰影複製完成之後，要備份之系統上的所有 i/o 作業都應該能夠繼續，而不會中斷備份的完整性。 這是具有陰影複製功能的其中一個主要動機。

因此，如同在探索階段 (請參閱 [備份探索階段](overview-of-the-backup-discovery-phase.md)) 的總覽，寫入器在檔案實際備份時有一些需求。

備份完成後，如果要求者已產生 [*BackupComplete*](vssgloss-b.md) 事件，則 VSS 會呼叫每個寫入器的 [**CVssWriter：： OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) 方法，預設只會傳回 **TRUE** 的虛擬方法。 但是，寫入器可以覆寫預設的執行，並採取這類動作來移除剩餘的暫存檔，或使用呼叫它的 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)介面來檢查每個 [*包含之明確*](vssgloss-e.md)元件的備份狀態 (以及它們可能會藉由取出對應的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)物件來定義) 的任何 [*元件集*](vssgloss-c.md)。 然後，寫入器可以藉由呼叫 [**>ivsscomponent： GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)，判斷備份成功或失敗。 **>Ivsscomponent： GetBackupSucceeded** 所傳回的值只有在元件中明確包含的所有檔案，[*而且全部都*](vssgloss-i.md)已成功地備份任何 [*子元件*](vssgloss-s.md)時，才會是 **TRUE** 。

當 [**CVssWriter：： OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) 的呼叫完成時，要求者應該針對每個寫入器呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 和 [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (最後一次) 。 寫入器會話狀態記憶體是有限的資源，而寫入器最後必須重複使用會話狀態。 此步驟會將寫入器的備份會話狀態標示為已完成，並通知 VSS 此備份會話位置可以由後續的備份作業重複使用。

## <a name="requester-actions-during-backup-of-files"></a>備份檔案期間的要求者動作

如同 [備份探索階段](overview-of-the-backup-discovery-phase.md)所述，您不應該產生要備份的實際檔案清單，直到陰影複製完成為止。

當陰影複製完成之後，會使用對應于指定磁片區陰影複製的 [*裝置物件*](vssgloss-d.md) 來存取陰影複製磁片區上的檔案。 裝置物件是從 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)所傳回的 [**VSS \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集內容物件取得。 陰影複製集的每個陰影複製都有自己的裝置物件。

接著會使用裝置物件以及從元件的寫入器元資料檔案規格取得的路徑，來選取要備份的檔案。 如需詳細資訊，請參閱要求者 [存取陰影複製的資料](requestor-access-to-shadow-copied-data.md) 。

哪些檔案將包含在備份清單中，取決於特定備份的本質、在元件 [*selectability 進行備份*](vssgloss-s.md)時，以及寫入器的邏輯路徑結構 (請參閱使用 [selectability 進行備份](working-with-selectability-for-backup.md)) 。

除了元件中指定的檔案之外，指定的寫入器也可能已明確排除檔案。 無論選取哪一個元件，都必須遵守檔案排除。

此外，如「 [備份探索」階段所](overview-of-the-backup-discovery-phase.md)述，已掛接的資料夾或重新分析點可能會出現在陰影複製中，並可進行備份。 但是，無法在陰影複製的磁片區上，執行裝載的資料夾或重新分析點 (請參閱) 使用掛接的 [資料夾和重新分析點](working-with-reparse-and-mount-points.md) 。

如果 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)所傳回的 [*替代路徑*](vssgloss-a.md)不是空白，則在備份作業期間也應該小心。 替代的路徑不同于 [*替代位置對應*](vssgloss-a.md) ，因為它只會在備份期間使用，而替代位置對應只會在還原期間使用。

在此情況下，資料不會從它的一般位置進行備份 (由 [**IVssWMFiledesc：： GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)) 指定，而是從 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)所傳回的位置。 還原時，應該會將檔案傳回至其正常位置。 如需詳細資訊，請參閱 [非預設的備份與還原位置](non-default-backup-and-restore-locations.md) 。

VSS 對於將資料備份到儲存媒體或選擇該媒體的實際機制沒有任何限制。 不過，建議您將每個 [*寫入器實例*](vssgloss-w.md) 的每個元件檔案視為一個單位來處理。 如需有關產生備份檔案清單中的最佳作法的討論，請參閱 [產生備份組](generating-a-backup-set.md) 。

備份指定元件所管理之任何檔案的成功或失敗，如果它定義 [*元件集*](vssgloss-c.md) ，) 其 [*子*](vssgloss-s.md) 元件針對指定的寫入器實例 (，應該透過呼叫 [**>ivssbackupcomponents：： SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)保留在備份元件檔中。 如果元件或元件集所管理的任何檔案無法備份，就會將整個元件視為失敗。 應該一律記錄哪些檔案無法備份的確切資訊。

開發人員可能會發現，將記錄儲存在備份媒體上的檔案、其所屬的元件與元件、規格，以及它們的原始路徑，都很有説明。 儲存每個寫入器元件定義等資訊也可能很有用。 這樣做可能會讓抓取作業更簡單。 不過，這類詳細資料會留給要求者開發人員。

因為寫入器可以在處理要求者呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)所產生的 [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)事件時，修改備份元件檔，所以必須等到非同步呼叫完成之後，才會儲存備份元件檔。

雖然先前可能會發生這種情況，但這也是儲存寫入器元資料檔案的便利時機。

請務必使用 [**>ivssbackupcomponents：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) 和 [**IVssExamineWriterMetadata：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml)保留備份元件檔和寫入器元資料檔案。 如果不是，則在檔案還原期間將無法使用 VSS。

除了儲存原始的中繼資料之外，某些備份應用程式可能會發現，將自己的檔案)  (清單（也就是其相關聯的寫入器、元件、還原程式和位置資訊）儲存到備份媒體以供稍後抓取，是很有用的。 這類清單可以用來避免在還原期間剖析和比較寫入器元資料檔案與備份元件檔。

正在備份的磁片區可能會有不受 VSS 寫入器管理的資料。 這項資料可以和應該從陰影複製的磁片區進行備份，在這種情況下，它會處於損 [*毀一致的狀態*](vssgloss-c.md)。 如需詳細資訊，請參閱 [不含 Writer 參與的備份](backups-without-writer-participation.md) 。

 

 




