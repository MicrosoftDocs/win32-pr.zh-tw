---
description: 還原集是要還原之所有檔案的清單，以及這些檔案將還原至其中的位置。
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: 正在產生還原集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3447ba6d258a5f22fff958761abc7ac0e4f27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978912"
---
# <a name="generating-a-restore-set"></a>正在產生還原集

還原集是要還原之所有檔案的清單，以及這些檔案將還原至其中的位置。

如同產生備份檔案清單一樣 (請參閱 [產生備份組](generating-a-backup-set.md)) ，判斷要還原的檔案和要還原的位置的演算法，必須依照寫入器實例來繼續 [*寫入器實例*](vssgloss-w.md) ，並針對每個寫入器實例以元件為基礎。

您必須將備份媒體上的每個檔案與其管理的元件產生關聯。 您也必須取得管理元件的 [*還原方法*](vssgloss-r.md)，以及檔案的 [*還原目標*](vssgloss-r.md) 資訊，以及其 [*替代位置*](vssgloss-a.md) 對應 (是否有任何) 。

有些檔案也可能需要 [*部分*](vssgloss-p.md) 檔案作業或還原的 [*導向目標*](vssgloss-d.md) 。

藉由檢查元件的 [*selectability 以取得備份*](vssgloss-s.md) 和 [*邏輯路徑*](vssgloss-l.md) (請參閱) [使用 selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md) ，要求者可以判斷要還原之備份作業的元件結構。

建立備份的元件結構之後，要求者可以取得每個元件的檔案 [*集*](vssgloss-f.md) 資訊 (檔案規格、路徑和遞迴旗標) 。 然後，要求者可以產生還原集。

需要 [*部分*](vssgloss-p.md)檔案或 [*導向目標*](vssgloss-d.md) 的檔案會提供自己的詳細還原指示 (請參閱 [非預設備份和還原位置](non-default-backup-and-restore-locations.md)) ，然後將這些位置新增至還原集。

針對未牽涉到部分檔案作業的檔案產生還原集的一般機制，或 [*導向的目標*](vssgloss-d.md) ，可能會進行下列動作：

1.  取得備份媒體上的檔案清單，包括其原始路徑。

2.  執行下列動作，以識別備份媒體上每個檔案的 [*寫入器類別*](vssgloss-w.md) 和元件：

    -   針對每個寫入器，在其所有元件上呼叫 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) ，以取得 ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) 的元件資訊。
    -   針對每個元件，取得檔案描述項 ([**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 元件所包含的每一組檔案的) 資訊 (視元件包含的資料類型而定，方法是呼叫 [**IVssWMComponent：： GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile)、 [**IVssWMComponent：： GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)和 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)。
    -   將檔案的名稱和路徑資訊與 [**IVssWMFiledesc：： GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)、 [**IVssWMFiledesc：： GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)和 [**IVssWMFiledesc：：) GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive) 所傳回 (之路徑資訊所傳回的名稱和路徑資訊做比較，以判斷該檔案是否為元件的一部分，以判斷該檔案是否為元件的一部分。
        > [!Note]  
        > 您應忽略從儲存的寫入器元資料檔案中找到的元件所抓取之檔案描述元中的任何替代位置資訊 (也就是 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 不會傳回 **Null**) 。 此替代位置是 [*替代路徑*](vssgloss-a.md)，只會在備份期間使用。

         

3.  針對備份媒體上的每個檔案取得替代對應資訊：

    -   替代檔案對應會儲存在寫入器而非元件層級，並從 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)所傳回的物件 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)取得。
    -   您可以根據 [**IVssExamineWriterMetadata：：**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)、 [**IVssWMFiledesc：： GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)和 [**IVssWMFiledesc：： GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)所傳回之替代位置對應中包含的路徑和檔案規格，檢查檔案的路徑和名稱，以判斷特定檔案是否有替代位置對應。  (如果在備份期間使用替代路徑，在此檢查處理還原的期間，應該忽略該資訊。 ) 
    -   如果檔案和替代位置對應檔案描述項相符，則您可以使用 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)所傳回之 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)物件的 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)方法，尋找您可以還原檔案的替代位置。
    -   以這種方式取得的替代位置對應不一定會與 [**>ivsscomponent：： GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)從備份元件檔傳回的對應一致。 只有當替代位置對應用於檔案時， [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 值才為非空白。

4.  您可以使用這個檔案和元件資訊來查詢備份元件檔，以取得有關還原目標、選項以及每個檔案的新還原位置的資訊。 這項資訊可以結合檔案、元件和替代位置的清單。

5.  您可以使用與傳統還原作業一致的方式來選取未受寫入器保護的檔案。

此時，要求者應該會有所有需要還原的檔案清單，以及有關如何還原這些檔案的指示，並且可以開始還原檔案的基礎：

-   是否要使用替代位置對應或原始檔案位置作為還原目標，將取決於該目標位置的檔案是否存在，以及 [**vss \_ 還原 \_ 目標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) 和 [**vss \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 的元件設定 (查看 [非預設的備份和還原位置](non-default-backup-and-restore-locations.md)) 。
-   還原的嘗試是否成功將取決於問題，例如目標的存取權限、鎖定目標檔案的位置，以及檔案還原中牽涉到的其他傳統問題。
-   針對指定的寫入器實例還原指定元件的成功或失敗，應該透過呼叫 [**>ivssbackupcomponents：： SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)保留在備份元件檔中。 這會讓寫入器在處理 PostRestore 事件時可存取的資訊。
-   如果檔案還原至替代位置對應，要求者必須呼叫 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)。 這可讓寫入器透過 [**>ivsscomponent：： GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)，判斷其檔案是否已還原到替代位置。
-   要求者可能會發現要將檔案還原到全新的位置。 這是可接受的，但要求者必須使用 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) 方法向寫入器表示這一點。

 

 



