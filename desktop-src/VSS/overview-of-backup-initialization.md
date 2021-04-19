---
description: 備份的這個階段會初始化寫入器和要求者、填入其內部資料結構、指定備份，以及透過 >ivssbackupcomponents：： GatherWriterMetadata 的必要呼叫來建立寫入器/要求者通訊。 如需詳細資訊，請參閱在 VSS 下處理備份的總覽。
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: 備份初始化的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fb97b43cf19ca60e3e4601899700e35bdad3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975037"
---
# <a name="overview-of-backup-initialization"></a>備份初始化的總覽

備份的這個階段會初始化寫入器和要求者、填入其內部資料結構、指定備份，以及透過 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)的必要呼叫來建立寫入器/要求者通訊。 如需詳細資訊，請參閱 [在 VSS 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md)。

下表顯示備份初始化所需的動作和事件的順序。



| 要求者動作                                                                                                                                                                                                                                                                                                                            | 事件                                                     | 寫入器動作                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 建立 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面並將它初始化以管理備份 (請參閱 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)、 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) 並選擇性地啟用或停用系統上的寫入器。 | 無                                                      | 無                                                                                                                                                                                                                                                       |
| （選擇性）設定陰影複製作業的內容，並選擇性地查詢系統所支援之提供者和陰影複製的系統 (參閱 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)， [**>ivssbackupcomponents：： query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)) 。                                               | 無                                                      | 無                                                                                                                                                                                                                                                       |
| 要求者可以提供處理備份和還原作業的其他資訊 (請參閱 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate))                                                                                                                                                         | 無                                                      | 無                                                                                                                                                                                                                                                       |
| 使用寫入器起始非同步連絡人 (請參閱 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                            | [*識別*](vssgloss-i.md) | 建立寫入器元資料檔案 (請參閱 [使用寫入器元資料檔案](working-with-the-writer-metadata-document.md) [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)， [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata))  |



 

## <a name="requester-actions-during-backup-initialization"></a>備份初始化期間的要求者動作

[**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)物件只能用於一個備份。 因此，要求者必須繼續進行備份的結尾，包括釋放 **>ivssbackupcomponents** 介面。 如果備份必須提前終止，要求者必須呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) ，然後釋放 **>ivssbackupcomponents** 物件 (如需詳細資訊，請參閱 [中止 VSS 作業](aborting-vss-operations.md)) 。 請勿嘗試繼續 **>ivssbackupcomponents** 介面。

通常，要求者的備份元件檔會初始化為空白。 當呼叫 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) 時，可以載入預存的備份元件檔，通常支援可轉移陰影複製的磁片區。 在此情況下，寫入器要求者通訊將會與下面所述的內容稍有不同。  (如需詳細資訊，請參閱匯 [入可傳送的陰影複製磁片](importing-transportable-shadow-copied-volumes.md) 區。 ) 

若要將磁片區新增至陰影複製集，要求者必須先呼叫 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)來設定陰影複製作業的內容。 如果未呼叫這個方法，則會使用陰影複製的預設內容， \_ \_ 也就是 VSS CTX 備份。 如需設定陰影複製內容的相關資訊，請參閱 [陰影複製內容](shadow-copy-context-configurations.md)設定。

若要在備份之前開始完成設定，要求者必須呼叫 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)。 藉由執行此動作，要求者會向寫入器指出：

-   以 [**VSS \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) 定義的備份 (類型) 
-   備份是否包含可開機的系統狀態
-   要求者是否支援選取個別元件或備份整個磁片區。

所有參與備份和還原作業的要求者都必須一律呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)。 這個方法會藉由產生 VSS [*識別*](vssgloss-i.md) 事件來起始寫入器要求者通訊，以回應寫入器建立其元資料檔案的回應。

在呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)之前，要求者有機會明確地啟用或停用特定的寫入器和寫入器類別，方法是使用 [**>ivssbackupcomponents：： EnableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses)、 [**>ivssbackupcomponents：:D Isablewriterinstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)和 [**>ivssbackupcomponents：:D isablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (預設會啟用) 的所有類別。 呼叫 **>ivssbackupcomponents：： GatherWriterMetadata** 之後，這些呼叫不會有任何作用。

因為沒有任何方法可以在呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)之前取得系統上的寫入器清單，所以要求者可以考慮建立然後刪除第二個 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 實例來取得清單。

[**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)完成後，就不需要呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 。 無法處理呼叫所產生之 [*識別*](vssgloss-i.md) 事件的寫入器，將不會成為提供 [**>ivssbackupcomponents：： GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) 和 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) 所找到之中繼資料的寫入器清單的一部分 (請參閱 [判斷寫入器狀態](determining-writer-status.md)) 。

## <a name="writer-actions-during-backup-initialization"></a>備份初始化期間的寫入器動作

為了回應識別事件，VSS 會呼叫每個寫入器的虛擬處理常式方法，即 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)。 寫入器會藉由覆寫 **CVssWriter：： OnIdentify** 的預設執行，並使用 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 介面，來建立其寫入器元資料檔案。

請注意，目前要求者以外的應用程式 (例如，系統應用程式) 可以產生寫入器必須處理的識別事件。 此外，寫入器無法從 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 內判斷哪個應用程式已產生識別事件。

這是這樣的情況，假設寫入器可能會在處理備份作業時收到數個識別事件，寫入器絕對不應該在 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 處理常式中設定狀態資訊。

相反地， [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 應該執行一致的演算法來建立寫入器的寫入器元資料檔案，特別是在寫入器建立檔之後，要求者和寫入器都不能修改它。 從這裡開始，它是唯讀檔案。

這表示與寫入器相關聯的 [*元件*](vssgloss-c.md) 數目和類型、哪些檔案是每個元件的一部分，而從備份或還原作業明確排除檔案，則無法在寫入器從處理識別事件之後變更。

所有參與 VSS 的寫入器都必須執行下列動作：

1.  使用 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)指出寫入器所管理之所有元件的還原方法。
2.  使用 [**IVssCreateWriterMetadata：： AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) 加入至少一個元件 (如需元件規格) 的詳細資訊，請參閱 [作者的元件定義](definition-of-components-by-writers.md) 。

寫入器會使用 IVssCreateWriterMetadata：： AddFilesToFileGroup、IVssCreateWriterMetadata：： AddDatabaseFiles 或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)，藉由使用 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**：：**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或：：，將檔案 [*集*](vssgloss-f.md)（路徑、檔案規格和遞迴旗標的組合）加入至指定的元件，來指出要參與備份或還原作業的檔案， (參閱 [將檔案新增至元件](definition-of-components-by-writers.md)。 ) 

寫入器也可以有一或多個空白元件，也就是未新增任何檔案的元件。 這些都非常適合用來組織寫入器的元件。  (查看 [元件的邏輯路徑](logical-pathing-of-components.md)。 ) 

寫入器會使用 [**IVssCreateWriterMetadata：： AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) 明確防止檔案包含在備份中。 這個明確的排除功能很有用，因為萬用字元可以用來指定要包含的檔案 (請參閱 [排除檔案清單規格](writer-metadata-document-contents.md)) 。 請注意，[排除檔案] 清單優先于元件檔案清單。

[**IVssCreateWriterMetadata：： AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) 是用來針對已新增至其中一個寫入器元件的指定檔案集建立 [*替代位置*](vssgloss-a.md) 對應。 當您無法或不想要還原至檔案的原始位置時，會在檔案還原期間使用這些對應。  (參閱 [實際檔案還原](overview-of-actual-file-restoration.md) 和 [非預設備份和還原位置](non-default-backup-and-restore-locations.md)的總覽。 ) 

因為備份檔案集是在寫入器元資料檔案中指定，所以稍後無法進行修改。 因此，寫入器應該撰寫程式碼，讓檔案集的定義將包含備份中所需的所有檔案（依名稱或透過萬用字元）。 當然，這可能包含一些可能會在識別事件之後建立的檔案。

 

 



