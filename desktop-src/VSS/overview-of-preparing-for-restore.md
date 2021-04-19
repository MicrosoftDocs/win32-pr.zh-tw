---
description: 在準備還原時，要求者會搭配使用已儲存的寫入器元資料檔案與自己的已抓取備份元件檔，來判斷要還原的內容和方法。
ms.assetid: 36cf188f-fce6-467c-a200-cbd9dc8f31a6
title: 準備還原的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b1bc3e429da5be9872e8345fe6da32a5340005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996688"
---
# <a name="overview-of-preparing-for-restore"></a>準備還原的總覽

在準備還原時，要求者會搭配使用已儲存的寫入器元資料檔案與自己的已抓取備份元件檔，來判斷要還原的內容和方法。 如需詳細資訊，請參閱 [在 VSS 下處理還原的總覽](overview-of-processing-a-restore-under-vss.md)。

在選取了還原候選元件之後，目前在系統上執行的寫入器會存取要求者的備份元件檔。 寫入器會使用此存取權來指出如何導致執行服務的最小難度（因為還原）。

完成此作業之後，要求者會有足夠的資訊來判斷需要還原的檔案，以及應還原的位置和方式。  (需詳細資訊，請參閱 [產生還原集](generating-a-restore-set.md)。 ) 

下表顯示準備還原作業所需的動作和事件順序。



| 要求者動作                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | 事件                                                         | 寫入器動作                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 從備份元件檔中取出 [*明確包含*](vssgloss-e.md) 在備份作業中的元件相關資訊 (請參閱 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)) 檢查取出的寫入器元資料檔案，以取得有關備份中明確包含的元件詳細資料，以及任何 find [*隱含包含*](vssgloss-i.md) 的子元件。  (參閱 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)、 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) <br/> | 無                                                          | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 選取要還原的元件和元件集 (請參閱 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 和 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)) 。                                                                                                                                                                                                                                                                                                                                                                                          | 無                                                          | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 要求者允許寫入器更新備份元件檔，而且可以選擇性地將任何特殊的還原選項傳達給寫入器。  (參閱 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)、 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)和 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)。 )                                                                                                                                                                                                                                          | [*PreRestore*](vssgloss-p.md) | 寫入器會判斷參與還原、準備要還原的檔案，並選擇性地修改備份元件檔（如有必要）。  (參閱 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)、 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)、 [**>ivsscomponent：： IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore)、 [**>ivsscomponent：： GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)、 [**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)、 [**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)、 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)。 )  |
| 要求者等候寫入器處理具有 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)的 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)事件。 它也應該驗證寫入器狀態。  (參閱 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus)， [**>ivssbackupcomponents：： GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) 。                                                                                                                                                                                                                                                                                  | 無                                                          | 無                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requester-actions-during-restore-preparations"></a>還原準備期間的要求者動作

若要判斷哪些元件適合還原，要求者必須執行下列動作：

-   建立用來進行備份的元件和 [*元件集*](vssgloss-c.md) 結構。
-   檢查元件的 [*selectability 以進行還原*](vssgloss-s.md)。
-   使用 selectability 指導方針 (使用 [selectability 進行還原和子元件](working-with-selectability-for-restore-and-subcomponents.md) ，) 選擇要包含的元件。
-   使用元件檔案 [*集*](vssgloss-f.md) 資訊來判斷必須還原備份媒體上的哪些檔案。

若要這樣做，要求者必須檢查儲存的備份元件檔中 [*明確包含*](vssgloss-e.md) 的元件。 您可以使用 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)，以寫入器為基礎來取得此元件資訊，它會傳回 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面的實例，而這兩個數據源的寫入器資訊和 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例都可以從中抓取。

如同其他地方所述， (要求 [者) 使用元件](use-of-components-by-the-requestor.md) ，備份元件檔和 **>ivsscomponent** 介面未包含足夠的資訊來支援備份。 因此，要求者必須檢查對應的預存寫入器元資料檔案，方法是使用 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) (參閱 [寫入器識別資訊](writer-metadata-document-contents.md)) 。

[**IVssExamineWriterMetadata：： GetFileCounts**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getfilecounts)會傳回每個寫入器所管理的元件數目。 然後，要求者可以使用 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) 來取得寫入器管理之每個元件的 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面。

藉由檢查元件的 [*selectability 以取得備份*](vssgloss-s.md) 和 [*邏輯路徑*](vssgloss-l.md) (請參閱) [使用 selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md) ，要求者能夠找出定義的備份時間元件集 (明確包含的元件所設定的元件) ，以及這些集合的子元件成員 (隱含包含的元件) 。

如果要使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 或 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)明確還原元件，要求者會透過備份元件檔來指出。 方法的選擇將取決於元件最初的備份方式，以及其 [*selectability 的還原*](vssgloss-s.md)方式。 明確包含用於還原的這些元件會指定隱含包含的其他元件 (請參閱 [使用 Selectability 進行還原和子元件](working-with-selectability-for-restore-and-subcomponents.md) 以取得詳細資料) 。

要求者可以使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 或 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)明確地包含目前執行中的寫入器元件，以便進行還原。 在此情況下，該寫入器在還原作業的其餘部分將不會收到任何 VSS 事件。

明確使用 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) 或 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) 來選取目前未執行之寫入器的元件，會傳回「 \_ 找不到 VSS E 物件」 \_ \_ \_ 錯誤。 請參閱 [不含寫入器參與的還原](restores-without-writer-participation.md) ，以取得還原遺失之寫入器資料的相關資訊。

若要讓寫入器具有要採取行動的完整資訊，寫入器專屬的還原選項以及增量還原的指示，可以分別由要求者呼叫 [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) 和 [**>ivssbackupcomponents：： SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)來傳送給寫入器。

此時，要求者已完成準備，並藉由呼叫 [**>ivssbackupcomponents：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)來產生 **PreRestore** 事件，讓寫入器準備實際還原。

## <a name="writer-actions-during-restore-preparations"></a>還原準備期間的寫入器動作

使用虛擬方法 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)處理 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)事件時，會進行還原作業的寫入器準備。 預設的實值只會在不採取任何動作的情況下傳回。 寫入器可以選擇覆寫預設的執行方式，以執行更多控制：

-   使用 [*還原目標*](vssgloss-r.md)覆寫 [*restore 方法*](vssgloss-r.md)
-   定義 [*導向的目標*](vssgloss-d.md)
-   建立錯誤訊息和其他資料
-   提供備份戳記資訊

事件處理常式 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) 接收 [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)的實例，可從中取得在備份期間明確包含在備份元件檔中之元件的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面。

使用 **>ivsscomponent** 的實例（對應于定義其備份 [*元件集*](vssgloss-c.md)的元件），以隱含的方式包含在備份作業中，並明確包含在還原中的子元件的相關資訊。

[**>ivsscomponent：： IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore)方法是用來判斷是否要還原已明確包含的備份元件。

若要判斷備份子元件是否已明確包含在還原中，寫入器會使用 [**>ivsscomponent：： GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent)。

寫入器應該檢查每個元件中的檔案 [*集*](vssgloss-f.md) ，並判斷是否需要採取動作來支援還原。 寫入器必須評估它是否想要覆寫目前的檔案，或者是否需要還原至新的位置。 動作可包括下列各項：

-   取得和操作任何撰寫或要求者專屬選項來管理還原作業 (請參閱 [**>ivsscomponent：： GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)) 
-   關閉並讓任何目前開啟的檔案變成可寫入
-   更新實例的還原目標 (，以強制還原至替代位置對應) 。 請參閱 [**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)。
-   透過私用中繼資料與要求者通訊 (請參閱 [**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)) 
-   表示應該透過重新對應來還原檔案，方法是透過將 [*導向目標*](vssgloss-d.md) 的定義 (參閱 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)) 

所使用的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例將會是在備份期間，由元件的明確包含在備份元件檔中所建立，或是定義其所屬備份元件集之元件的元件 (請參閱使用 [Selectability 進行還原和子元件](working-with-selectability-for-restore-and-subcomponents.md)) 。

 

 
