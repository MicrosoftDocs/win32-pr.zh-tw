---
description: 使用隱含選取的元件需要存取備份元件檔和寫入器元資料檔案。
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Selectability 和使用元件屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735481d4bd0d7fdaa4102026b74ca78be947afbab24858d88d9210dd7bd4e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751650"
---
# <a name="selectability-and-working-with-component-properties"></a>Selectability 和使用元件屬性

使用隱含選取的元件需要存取備份元件檔和寫入器元資料檔案。

不這麼做的原因有兩個：

-   儲存在備份元件檔中的元件資料 (由 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面表示，) 缺乏元件檔案集資訊（檔案規格、路徑和遞迴旗標）的存取權。  (參閱 [使用備份元件檔](working-with-the-backup-components-document.md)。 ) 
-   在備份期間，只有在備份元件檔中 [*明確包含*](vssgloss-e.md) 的元件會將其資訊直接儲存在備份元件檔中。 要求者和寫入器必須使用可透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面取得的資訊，以及 [*邏輯路徑*](vssgloss-l.md) 資訊和寫入器元資料檔案來取得的相關資訊，以及設定 [*隱含包含*](vssgloss-i.md) 元件的屬性。

在 [元件的邏輯路徑](logical-pathing-of-components.md) 中討論的「MyWriter」案例可用來說明備份的 selectability。



| 元件名稱 | 邏輯路徑            | 可選取以進行備份 | 可選取以進行還原 | 明確包含 |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| 執行  | ""                      | N                     | N                      | Y                   |
| "ConfigFiles"  | 執行           | N                     | N                      | Y                   |
| "LicenseInfo"  | ""                      | Y                     | N                      | Y                   |
| "Security"     | ""                      | Y                     | N                      | Y                   |
| 使用者     | "Security"              | N                     | N                      | N                   |
| 數位憑證 | "Security"              | N                     | N                      | N                   |
| "writerData"   | ""                      | Y                     | Y                      | Y                   |
| Set1         | "writerData"            | N                     | Y                      | N                   |
| Jan          | "writerData \\ Set1"      | N                     | N                      | N                   |
| 年          | "writerData \\ Set1"      | N                     | N                      | N                   |
| Set2         | "writerData"            | N                     | Y                      | N                   |
| Jan          | \\"writerData      | N                     | N                      | N                   |
| 年          | \\"writerData      | N                     | N                      | N                   |
| 查詢        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| 用法        | "writerData"            | Y                     | Y                      | N                   |
| Jan          | "writerData \\ Usage"     | N                     | N                      | N                   |
| 年          | "writerData \\ Usage"     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>備份組中隱含包含的元件

檢查寫入器的寫入器元資料檔案時 (請參閱 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) 在備份期間，要求者應儲存所有元件的清單、其 [*邏輯路徑*](vssgloss-l.md)及其檔案集資訊。

需要檔案集和排除的檔案資訊，才能明確或隱含) 包含的元件，判斷任何 (的檔案清單。

針對沒有可選取的備份元件的其，以及未定義 [*元件集*](vssgloss-c.md)的備份元件可選取的專案，因為這些元件不會定義子元件，所以只需要檔案集和排除的檔案資訊來識別所有元件的候選備份。

若要針對定義元件集的備份元件明確包含可選取的，則必須使用檔案設定和排除定義元件和所有 [*子元件*](vssgloss-s.md) 的檔案資訊，以選取要備份的檔案。

這表示只有使用 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面的實例檢查這些元件的寫入器中繼資料，才能找到元件 "可執行檔"、"ConfigFiles" 和 "LicenseInfo" 的備份組。

但是，如果 writerData 明確包含在備份中，您就必須檢查其 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面的實例，以及 "Set1"、"Jan" (邏輯路徑 "writerData \\ Set1" ) "的實例。 Dec" (的邏輯路徑 "writerData \\ Set1" ) ，"WriterData '，" Jan " (具有邏輯路徑" \\ ' ) ，"Dec" (，邏輯路徑 "writerData ) ' (\\ ，" Query "，" Usage "，" Jan " \\ \\ ) 具有邏輯路徑" writerData usage " (，" ") 具有邏輯路徑" writerData usage "。

若要這樣做，要求者必須先找出元件 "writerData" (邏輯路徑 "" ) 是可選取的。 然後，它必須掃描寫入器所管理的所有其他元件，以判斷其邏輯路徑中的第一個元素是否為 "writerData"。 以 "writerData" 作為邏輯路徑前置成員的元件會被識別為 "writerData" 的子元件，並在明確選取時隱含地選取。

事實上，需要進行類似的掃描以判斷沒有任何元件以「LicenseInfo」作為其邏輯路徑的主要成員，因此「LicenseInfo」沒有子元件。

由於 VSS 中的這項機制複雜度，許多要求者寫入器可能會發現建立自己的結構來儲存明確和隱含新增元件的元件和備份組資訊，會很有説明。

## <a name="properties-of-implicitly-included-components"></a>隱含包含元件的屬性

在還原和備份作業期間，會使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 和 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面的實例來取出元件的相關資訊，以及設定或變更元件屬性。 不過，只有明確包含的元件會有 **>ivsscomponent** 介面的實例，或可供 **>ivssbackupcomponents** 介面存取。

某些屬性在範圍內是全元件集。 這些屬性包括下列各項：

-   備份與還原狀態： <dl>

[**>ivssbackupcomponents：： SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**>ivsscomponent：： GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**>ivssbackupcomponents：： SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**>ivsscomponent：： GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   備份和還原選項： <dl>

[**>ivssbackupcomponents：： SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**>ivsscomponent：： GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**>ivssbackupcomponents：： SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**>ivsscomponent：： GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   失敗訊息： <dl>

[**>ivsscomponent：： SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**>ivsscomponent：： SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**>ivsscomponent：： SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**>ivsscomponent：： SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   還原目標： <dl>

[**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   備份戳記： <dl>

[**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**>ivsscomponent：： GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   其他中繼資料： <dl>

[**>ivsscomponent：： SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**>ivsscomponent：： GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**>ivsscomponent：： SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**>ivsscomponent：： GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

因此，您可以使用元件集之定義成員的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面實例，或使用定義成員的名稱、類型和邏輯路徑與 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 方法，來設定或抓取所有元件集成員的屬性。

基於這個理由，元件集會被視為單位。 比方說，只有在所有元件的所有檔案集都成功備份時，元件集的備份才會成功。

在上述範例中，假設元件 "Jan" (中的一個檔案具有邏輯路徑 "writerData '， \\ ) 是" writerData "所定義之元件集的成員。 如果 "Jan" 的檔案中有一個無法備份，要求者會使用 "writerData" 的資訊 (其名稱 "writerData"、其路徑 ""，以及其元件類型) 做為引數，在設定 [**>ivssbackupcomponents：： SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) 與 **false** 以表示元件集失敗時。

同樣地， [**>ivsscomponent：： GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) 針對 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例所傳回的狀態，不只適用于 "writerData"，也適用于其所有子元件。

此外，如果寫入器選擇使用 "writerData" 之 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)實例的 [**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)來變更還原目標，則會變更所有 "writerData" 子元件的所有檔案集的還原目標。

下列屬性不適用於全元件，而是套用至特定檔案或檔案集：

-   替代位置對應： <dl>

[**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**>ivsscomponent：： GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**>ivsscomponent：： GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   差異檔案： <dl>

[**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**>ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**>ivsscomponent：： GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   部分檔案： <dl>

[**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**>ivsscomponent：： GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   導向的目標： <dl>

[**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**>ivsscomponent：： GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**>ivsscomponent：： GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   新目標： <dl>

[**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**>ivsscomponent：： GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**>ivsscomponent：： GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

當要求者使用 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面來存取子元件的這些功能時，它會使用元件集定義元件的元件資訊，但會使用元件的檔案或檔案集資訊。

同樣地，如果屬性可透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面存取，則會使用對應至定義子元件的實例，但會從子元件取得檔案或檔案集引數。

比方說，假設子元件 "Jan" (邏輯路徑 "writerData \\ '： '，) 具有路徑為" c： fred "的檔案 \\ （檔案規格為" \* .dat "），且遞迴旗標為 **true** 可能必須還原至替代位置。

如果發生這種情況，要求者會呼叫 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)，並使用 "writerData" 的資訊 (元件類型、"writeData" 的元件名稱，以及 "" ) 的邏輯路徑以及 "Jan" 的檔案集資訊 (路徑 "c： \\ fred"、檔案規格 " \* .dat" 和遞迴等於 **true**) 。

請注意，在此情況下，檔案集資訊必須完全符合 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 用來將檔案新增至 Jan 的檔案集資訊。

同樣地，如果寫入器想要將導向的目標新增至路徑為 "c： ethel" 且名稱為 "lucy" 的檔案，且該檔案具有 \\ 邏輯路徑 "writerData ' ) 所管理的" jan " (\\ ，則會使用對應于" writerData "的 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例，但" jan "的檔案資訊。

## <a name="implicitly-included-components-in-the-restore-set"></a>還原集中隱含包含的元件

如果已隱含包含在備份中的元件，可以在還原時明確包含在還原中。 如同使用 [Selectability 進行還原和子元件](working-with-selectability-for-restore-and-subcomponents.md)所述，這類元件會使用 [**>ivssbackupcomponents：： AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) 方法加入至備份元件檔。

不過，這不會建立 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的新實例，也不會直接透過 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面存取元件。

相反地，明確包含用於還原的元件，但隱含包含在備份中的元件，必須透過 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例來存取，而該介面會對應到在備份時定義其所屬元件的元件集。

例如，若要明確地包含 restore "Set1" （可選取的子元件為 "writerData"），您可以藉由呼叫 [**writerData**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面之 ">ivsscomponent" 實例的 [**>ivsscomponent：： GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent)方法，取得其相關資訊。

 

 



