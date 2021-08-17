---
description: 在初始化 VSS 還原作業時，要求者需要取出備份元件檔，以及在備份作業期間建立和儲存的每個相關寫入器元資料檔案。
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: 還原初始化的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c531e4b47c49e5bd5538ea30583a31273bb6645a445ef1b1ea851bac539411c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751687"
---
# <a name="overview-of-restore-initialization"></a>還原初始化的總覽

在初始化 VSS 還原作業時，要求者需要取出備份元件檔，以及在備份作業期間建立和儲存的每個相關寫入器元資料檔案。 寫入器會將其目前的狀態查詢為處理要求者所產生的 [*識別事件*](vssgloss-i.md) 。 如需詳細資訊，請參閱 [在 VSS 下處理還原的總覽](overview-of-processing-a-restore-under-vss.md)。

下表顯示初始化還原作業所需的動作和事件順序。



| 要求者動作                                                                                                                                                                                                                                                                                                       | 事件                                                     | 寫入器動作                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 建立 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面、將它初始化以管理還原，以及載入儲存的要求者中繼資料 (參閱 [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents)、 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)) 。 | 無                                                      | 無                                                                                                                                                                                                                                                                                                                      |
| 呼叫 [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) 來建立 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面，並使用預存寫入器中繼資料載入這些介面。                                                                                                           | 無                                                      | 無                                                                                                                                                                                                                                                                                                                      |
| 使用寫入器起始非同步連絡人 (請參閱 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)) 。                                                                                                                                                                      | [*識別*](vssgloss-i.md) | 寫入器開始事件處理以支援還原。 建立寫入器元資料檔案 (請參閱 [使用寫入器元資料檔案](working-with-the-writer-metadata-document.md) [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)， [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) 。 |
| 要求者會藉由呼叫 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)來等候寫入器初始化。                                                                                                                                                                                                                               | 無                                                      | 無                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>還原初始化期間的要求者動作

在還原的初始化階段期間，要求者必須能夠存取已儲存的備份元件檔和所有寫入器元資料檔案。

根據執行的不同，這表示要求者需要掛接和讀取備份媒體，或有其他存取儲存中繼資料的機制可供使用。

要求者會使用儲存的 XML 檔，其中包含執行備份的要求者的備份元件檔，以使用 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) 來初始化其備份元件檔。

如同備份期間的情況，備份元件檔的資訊不足以支援還原;因此，要求者需要存取儲存在備份期間所儲存的寫入器元資料檔案 (請參閱要求 [者) 使用元件](use-of-components-by-the-requestor.md) 。

要求者會針對資料已備份且現在要還原的每個寫入器呼叫 [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) ，以抓取儲存的寫入器中繼資料。 此函式會為每個寫入器建立 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 物件，並將寫入器的寫入器元資料檔案載入物件中。

在備份期間，若要在本身和系統的寫入器之間起始合作，要求者必須藉由呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)來產生 [*識別*](vssgloss-i.md)事件。 在完成 [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)之後，不需要呼叫 [**>ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 。 無法處理 [*識別*](vssgloss-i.md) 事件的寫入器，將不會包含在寫入器清單中，提供 [**>ivssbackupcomponents：： GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) 和 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) 傳回的中繼資料 (請參閱 [判斷寫入器狀態](determining-writer-status.md)) 。

如同備份作業，要求者必須查詢和剖析備份元件檔中的資訊，並將其與寫入器元資料檔案中的資料進行比較，以判斷哪些元件已備份並選擇要還原的元件 (請參閱 [準備還原](overview-of-preparing-for-restore.md)) 。 此外，要求者必須產生詳細清單，其中包含選取要還原之備份媒體上的檔案相關資訊，以及還原的方式和位置。  (查看 [產生還原集](generating-a-restore-set.md)。 ) 

因此，某些備份應用程式可能會發現，儲存在備份媒體本身的清單 (，其本身的優化格式) 檔案及其相關聯的寫入器、元件、還原程式和位置資訊。 您可以使用這份清單，將寫入器元資料檔案和支援還原所需的備份元件檔的剖析和比較數量降到最低。

## <a name="writer-actions-during-restore-initialization"></a>還原初始化期間的寫入器動作

如同在還原作業期間所做的一樣，為了回應識別事件，VSS 會呼叫每個寫入器的虛擬處理常式方法 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)。

請注意，目前要求者以外的應用程式 (例如，系統應用程式) 可以產生必須由寫入器處理的識別事件。 此外，寫入器無法從 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 內判斷哪個應用程式已產生識別事件。

假設寫入器在處理還原作業時可能會收到數個識別事件，寫入器絕對不應該在 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 處理常式中設定狀態資訊。 相反地，它們必須使用相同的演算法來建立其寫入器元資料檔案，就像在備份作業期間所做的一樣 (請參閱 [備份初始化期間的寫入器動作](overview-of-backup-initialization.md) ，以取得詳細資訊) 。

 

 



