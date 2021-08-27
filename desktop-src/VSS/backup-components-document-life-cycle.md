---
description: 要求者對於備份元件檔的生命週期具有主要責任。
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: 備份元件檔生命週期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4804625f979e0d5621d96a2230c1419354d0dbeb4c368312dbd3943e0ac0c4bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124528"
---
# <a name="backup-components-document-life-cycle"></a>備份元件檔生命週期

要求者對於備份元件檔的生命週期具有主要責任。

這個控制項是由 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)所傳回之 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)介面物件的實例所執行。

要求者必須藉由呼叫 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) 或 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)，初始化備份或還原之前的備份元件檔。 要求者可以將檔初始化為空的，或者可以載入先前儲存的檔複本。

針對備份作業，備份元件檔通常會初始化為空白。 在處理備份過程中，其資料將會填入系統作者的合作。

針對還原作業，備份元件檔通常會從初始備份期間所產生的預存檔初始化。 這可讓還原 (與儲存的寫入器元資料檔案的檢查) ，以判斷最初備份的資料以及應該如何還原。

備份可 [*轉移的陰影複製*](vssgloss-t.md) 是此規則的例外狀況。 在此情況下，陰影複製可能已從一個系統移出， (在其中建立的一個系統，以及初始備份元件檔) 至另一個系統，方法是重新指派共用存放裝置的邏輯單元。 在這些情況下進行備份時，要求者會載入儲存的備份狀態，並從初始系統離開的位置繼續進行。  (需詳細資訊，請參閱匯 [入已傳送的陰影複製磁片](importing-transportable-shadow-copied-volumes.md)區。 ) 

在處理備份的過程中，要求者會決定要實際複製哪些元件，而這些元件被標示為可 [*選取以進行備份*](vssgloss-s.md)、元件的 [*邏輯路徑*](vssgloss-l.md)，以及自己的內部邏輯。

部分元件會 [*明確包含*](vssgloss-e.md) 在備份作業中;元件的相關資訊將會加入至 [備份元件] 檔。 其他將會 [*隱含地包含*](vssgloss-i.md) 在備份中;新增的元件的相關資訊將不會加入至 [備份元件] 檔。

所有寫入器的備份元件其都沒有可選取的上階，而是由要求者選擇的備份元件來明確新增。

如果備份元件的邏輯路徑中有可選取的上階（明確包含在備份中），則可以隱含地加入其和可選取的備份元件。 這些元件 ([*子*](vssgloss-s.md) 元件) 是由其可選取的上階所定義之 [*元件集*](vssgloss-s.md) 的成員。

處理還原作業時，要求者會使用 [*selectability 來進行還原*](vssgloss-s.md) ，而不是使用 selectability 進行備份，以搭配邏輯路徑資訊及其本身的內部邏輯來決定要還原的檔案。

如果已隱含新增至備份的元件現在要明確新增至還原，要求者將會以該元件的資訊更新 [備份元件] 檔。

預存元件的相關資訊可透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例提供給要求者和寫入器。

它是透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面，讓寫入器可以查詢並 (到 [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) 和 [**PostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) 事件的結尾，) 修改備份元件檔中的資訊。

當呼叫 [**CVssWriter：： OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)、 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)、 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)、 [**CVssWriter：： OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)或 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) 事件處理常式時，寫入器會接收 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) 介面的實例。

請注意，在產生 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) 事件時，備份元件檔會設為唯讀，因此 [**CVssWriter：： OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) 無法使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面來修改它。

從 [**IVSSWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) 介面，寫入器可以取出 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例，讓它能夠存取所有明確加入至備份元件檔的元件，以及改變其狀態。 如需詳細資訊，請參閱在 vss 中 [處理備份的總覽](overview-of-processing-a-backup-under-vss.md) 和 [在 Vss 下處理還原的總覽](overview-of-processing-a-restore-under-vss.md)。

[**>Ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)介面釋放時，會從記憶體中移除備份元件檔，而且必須使用 [**>ivssbackupcomponents：： SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)來儲存，否則將會遺失其所有資訊。

此外，當 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 檔已正確釋出時，會產生 [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) 事件並刪除 [*自動發行陰影複製*](vssgloss-a.md) 。

 

 



