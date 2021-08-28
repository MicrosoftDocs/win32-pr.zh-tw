---
description: 測試寫入器是一種公用程式，可讓您用來測試 VSS 要求者應用程式。
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: VSS 測試編寫器工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c8ff5461c263754aa5771cc9db230dec795a98
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482094"
---
# <a name="vss-test-writer-tool"></a>VSS 測試編寫器工具

測試寫入器是一種公用程式，可讓您用來測試 VSS 要求者應用程式。 此寫入器可以設定為執行 VSS 寫入器可執行檔幾乎所有動作。 此外，測試寫入器會執行大量檢查，以確保要求者已正確處理這些寫入器動作。

寫入器的每個實例都是使用 XML 設定檔來初始化，此檔案描述寫入器將報告的元件，以及寫入器的運作方式。 您可以設定寫入器來報告各種類型的案例，包括使用累加和差異介面的更複雜案例。 寫入器會在程式期間的各種時間點執行檢查，以確保要求者的行為正確。 還原完成之後，寫入器會檢查所有必要的檔案是否已還原，而不會損毀。 寫入器也可以設定為執行其他作業，例如失敗的特定事件。

> [!Note]  
> 這項工具組含在適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中。 您可以從下載 Windows SDK [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) 。

 

在 Windows SDK 安裝中，您可以在 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 (的位 Windows) 和中找到 VssSampleProvider 工具 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 。

## <a name="running-the-test-writer-tool"></a>執行測試編寫器工具

若要啟動測試寫入器，請在命令提示字元中輸入下列命令：

**vswriter.exe** *設定檔*

其中 *設定檔是* 設定檔案的路徑，此設定檔會指定此寫入器的行為。

若要停止測試寫入器，請按 CTRL + C。

您可以同時執行多個測試寫入器實例。 不過，每個寫入器的實例將會報告相同的寫入器類別識別碼 (但) 不同的寫入器實例識別碼，因此邏輯路徑和元件名稱在所有同時執行的寫入器實例之間必須是唯一的。

為了確保寫入器能夠正確檢查要求者是否已遵守排除檔案規格，所有備份的檔案都應該先從原始磁片區中刪除，再嘗試還原它們。 建議您儲存每個寫入器案例的範本，以便可以輕鬆地重新建立案例。

## <a name="using-a-configuration-file"></a>使用組態檔

下列範例設定檔（vswriter \_config.xml）可以在 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` x86 平臺和 x64 平臺上找到 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` 。

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

此設定檔中的根項目命名為 TestWriter。 所有其他專案會排列在 TestWriter 元素之下。

其中一個與 TestWriter 相關聯的屬性是 usage 屬性。 這個屬性會指定透過 [**IVssExamineWriterMetadata：： GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)報告的使用類型。 此屬性的其中一個可能值為使用者 \_ 資料。

根項目的第一個子項目必須一律為 RestoreMethod 元素。 這個元素會指定下列專案：

-   在此情況下，restore 方法 (， \_ 如果 \_ 可以 \_ 取代則還原 \_) 
-   寫入器是否需要還原事件 (在此情況下，一律) 
-   還原寫入器之後是否需要重新開機 (在此案例中為否) 

這個元素可以選擇性地指定替代位置對應。  (在此案例中，未指定替代位置。 ) 

第二個子項目是 ExcludeFile 元素。 此元素會導致寫入器從備份中排除檔案或一組檔案。

第三個子項目是元件元素。 此元素會導致寫入器將元件新增至其中繼資料。 元件專案包含屬性，用來描述元件和子項目，以描述元件的內容，如下所示：

-   componentType，指出這是否為檔案群組或資料庫
-   元件邏輯路徑的 logicalPath
-   元件名稱的 componentName
-   可選取以指出可選取的備份狀態

Component 元素也有一個名為 ComponentFile 的子專案，可將檔案規格新增至此元件。  (元件元素可以有任意數目的 ComponentFile 元素，可為每個元件指定。 ) 此 ComponentFile 元素具有下列屬性：

-   path = "c： \\ writerData \\ myFilesHere"
-   filespec = " \* "
-   遞迴 = "no"

雖然測試寫入器會驗證要求者的行為，但並不會驗證設定檔是否一律為寫入器維護記載的語法。 良好的寫入器應該不會進行許多作業 (例如在多個元件中報告相同的檔案) ，而且是由 XML 設定檔的作者負責維護這些語義。

## <a name="configuring-writer-attributes"></a>設定寫入器屬性

TestWriter 根項目包含的屬性，可決定寫入器的各種行為。 以下是一些可以改變的行為：




| 屬性 | 描述 | 
|-----------|-------------|
| <span id="verbosity"></span><span id="VERBOSITY"></span>冗長<br /> | 寫入器會將狀態列印到主控台，因為它會接收事件並進行處理。 所顯示的詳細程度層級是由詳細資訊屬性所指定。 有三個詳細等級可供選擇：<br /><dl><dt><span id="low"></span><span id="LOW"></span>低</dt><dd> 只會列印寫入器中的失敗或要求者的不正確行為。<br /></dd><dt><span id="medium"></span><span id="MEDIUM"></span>中</dt><dd> 除了額外的狀態資訊（例如接收事件時），也會列印低詳細資訊層級的所有專案。 這是預設層級。<br /></dd><dt><span id="high"></span><span id="HIGH"></span>高</dt><dd> 報告寫入器操作的詳細狀態資訊。<br /></dd></dl> | 
| <span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br /> | 若要執行額外的驗證，請將此屬性設定為 [是]，讓寫入器在建立磁片區陰影複製後立即刪除其所有檔案。 接著，要求者必須複製陰影複製中的檔案，因為它們已不存在於原始磁片區上。 <br /><blockquote>[!Note]<br />在算寫入器的情況下，會在算之後，但在建立陰影複製之前，從原始位置刪除檔案。 建立陰影複製之後，就會從算目錄中刪除這些檔案。</blockquote><br /> | 
| <span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br /> | 若要刪除部分檔案，請將此屬性設定為 [是]。<br /> | 
| <span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br /> | 若要刪除差異的檔案，請將此屬性設定為 [是]。<br /> | 
| <span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br /> | 將此屬性設定為 [是]，讓寫入器檢查已備份的每個檔案都已還原到適當的位置，而且檔案未損毀。 部分檔案和差異檔案也會正確處理。<br /> | 
| <span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br /> | 將此屬性設定為 [是]，以使寫入器確認不會還原符合排除清單中檔案規格的檔案。 為了讓此功能正常運作，必須先清空還原目錄，再進行還原。<br /> | 




 

## <a name="specifying-alternate-location-mappings"></a>指定替代位置對應

如果還原方法是 VSS \_ WRE \_ 還原 \_ 至 \_ 替代 \_ 位置，或元件正常還原失敗，則替代位置對應會指定要還原的位置。 寫入器可以使用 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) 方法，向要求者報告其替代位置對應。 您可以藉由將 AlternateLocationMapping 子項目新增至 RestoreMethod 專案，將替代位置對應加入至測試寫入器設定檔。

下列 RestoreMethod 專案包含 AlternateLocationMapping 子項目。

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

這個範例會指定要求者應先嘗試將符合 c： files.txt 的所有檔案 \\ 還原 \\ \* 至 c： \\ files 目錄。 如果無法取代這些檔案的其中一個，要求者應該改為將所有檔案還原至 c： \\ altfiles 目錄。 要求者應該使用 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) 方法來儲存這個替代位置對應。 如果測試寫入器設定為檢查是否已還原檔案，它也會檢查要求者是否已呼叫 **AddAlternativeLocationMapping**。

## <a name="specifying-files-to-be-excluded"></a>指定要排除的檔案

每個寫入器都可以指定檔案規格清單，以指定要從備份中排除的要求者檔案。 您可以藉由將 ExcludeFile 子項目新增至 TestWriter 根項目，將這些檔案規格新增至測試寫入器設定檔。

以下是 ExcludeFile 子項目的範例，它會排除 C： \\ files 目錄中符合 c： temp 的所有 \\ 檔案 \* \* 。

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>備份算寫入器

許多寫入器可作為「算寫入器」。 算寫入器會根據一組原始的檔案建立中繼檔案或「算檔案」，並在備份時將算檔案放在替代位置。 寫入器會使用 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 方法，通知要求者應該從替代位置將這些檔案還原。 不過，這些檔案仍應還原至原始檔案的使用中位置。 測試寫入器可以設定為特定檔案規格的算寫入器。

下列 ComponentFile 元素包含 alternatePath 屬性：

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

此範例會將測試編寫器設定為在 \\ 建立磁片區陰影複製之前，立即將符合 c： files.txt 的所有檔案複製 \\ \* 到 c： \\ files \\ 算目錄。 要求者必須從 c： \\ files \\ 算目錄備份檔案。 如果測試寫入器設定為刪除檔案，它會在建立陰影複製之前先刪除原始檔案，因此它們不會出現在陰影複製磁片區的 c： \\ files 目錄中。 在此情況下，會在 \\ \\ 建立陰影複製後刪除 c： files 算中的檔案，因此必須從 \\ 陰影複製磁片區上的 c： files \\ 算目錄進行備份。

## <a name="reporting-component-dependencies"></a>報告元件相依性

寫入器可以指定本機組件與存在於其他寫入器中的元件之間的相依性。 這些相依性會使用 [**IVssWMComponent：： GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)回報給要求者。 您可以將一或多個相依性子項目新增至 Component 專案，以設定測試寫入器來報告這些相依性。

下列元件專案包含相依性子項目：

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

相依性會指定為相依性專案的屬性。 writerId 是包含相依性目標的寫入器類別識別碼，logicalPath 是該寫入器中元件的邏輯路徑，而 componentName 是元件的名稱。 在此情況下，如果要求者在目前的寫入器中備份 "WriterComponent"，則也應該 \\ 在目標寫入器中備份元件 "ComponentPath Writer2Component"。

> [!Note]  
> 測試寫入器不會執行檢查，以確保會遵守相依性。

 

## <a name="failing-events"></a>失敗的事件

測試寫入器可以設定為使寫入器所收到的任何一般事件失敗。 這些事件如下所示：



| 事件                                                                                                                                    | 描述                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>識別<br/>                                     | 收到 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 呼叫的回應。 此處的失敗會導致無法報告寫入器。<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | 收到的回應是呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)的要求者。<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | 當要求者呼叫 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)，但在建立陰影複製之前收到。<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>凍結<br/>                                             | 在 [*PrepareForSnapshot*](vssgloss-p.md)之後立即收到，但在建立陰影複製之前。<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>解凍<br/>                                                     | 陰影複製建立完成之後收到。<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | 在解凍完成之後但在 >ivssbackupcomponents 之前收到 [**：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 完成。<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>中止<br/>                                                 | 在 [*凍結*](vssgloss-f.md) 和 [*解除*](vssgloss-t.md) 凍結之間的時間過久，或要求者呼叫 [**>ivssbackupcomponents：： AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)時收到。<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | 當要求者結束時收到。 絕不會回報此處的失敗。<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>PreRestore<br/>                             | 當要求者呼叫 >ivssbackupcomponents 時收到 [**：:P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)。<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | 當要求者呼叫 >ivssbackupcomponents 時收到 [**：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)。<br/>                                                                                                                                         |



 

這些失敗的設定方式是將一或多個 FailEvent 子項目新增至 TestWriter 根項目。 可以設定的失敗類別有兩種：可重試且無法重試。 如果重試整個備份程式，則可能會發生可重試的錯誤，而無法重試的錯誤則不可能消失。 根據可重試的屬性，選擇事件的失敗類型。

以下是基本無法重試的失敗範例：

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

此範例會導致寫入器在 [*凍結*](vssgloss-f.md) 事件期間失敗。 [**>Ivssbackupcomponents：： GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 會將寫入器失敗報告為 VSS \_ E \_ WRITERERROR \_ NONRETRYABLE。

以下是基本可重試錯誤的範例：

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

此範例會導致寫入器在收到 [*凍結*](vssgloss-f.md) 事件前兩次失敗。 在前兩次之後，寫入器一律會成功。 透過 [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) 回報的寫入器失敗會是隨機可重試的錯誤碼。

## <a name="declaring-supported-backup-types"></a>宣告支援的備份類型

寫入器會透過要求者的呼叫 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)來傳達支援哪些備份類型。 TestWriter 根項目包含每一種備份類型的屬性，以指出支援。 這些屬性是 supportsCopy、supportsDifferential、supportsIncremental 和 supportsLog。 若要指出對特定備份類型的支援，請將對應的屬性設定為 [是]。

如果要求者將備份類型設定為寫入器不支援的備份類型，寫入器會在 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)期間記下這項事實，否則會正常運作。

## <a name="indicating-the-file-backup-type"></a>指出檔案備份類型

[**IVssWMFiledesc：： GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)方法會將位元遮罩傳回給要求者，指出應如何備份檔案。 這會指出在特定類型的備份期間是否需要檔案，以及在特定類型的備份期間是否需要進行陰影複製。 在 [備份複雜存放區](requestor-role-in-backing-up-complex-stores.md)的檔要求者角色中，會以更高的長度解釋此位元遮罩中的備份類型。

在測試寫入器中，會藉由設定每個 ComponentFile 專案中的屬性來指定此位元遮罩的元素。 FullBackupRequired、diffBackupRequired、incBackupRequired 和 logBackupRequired 屬性會指定何時需要備份檔案。 FullSnapshotRequired、diffSnapshotRequired、incSnapshotRequired 和 logSnapshotRequired 屬性會指定何時必須從磁片區的陰影複本備份檔， (而不是從原始磁片區) 。 所有這些值的預設值為 [是]，表示必須一律備份檔案，而且必須從磁片區的陰影複本備份。

## <a name="adding-partial-files"></a>新增部分檔案

在處理 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)期間，寫入器有機會將部分檔案新增至每個元件。 這些部分檔案會使用 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)來回報。 您可以藉由在元件專案中指定 PartialFile 子項目，將測試編寫器設定為加入部分檔案。

以下是具有兩個 PartialFile 子項目的元件元素範例：

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

只有部分符合現有 ComponentFile (的部分檔案，與範例中的第一個部分檔案相同) 或在與現有 ComponentFile (相同的磁片區上的新部分檔案（如同在第二個部分檔案) 應該以此方式指定）。 對於此元件，要求者必須完全備份符合 c：檔案的所有 \\ 檔案 \\ \*.txt 但 partial.txt 除外。 接著，要求者必須備份指定的範圍 (其中範圍是位移，後面接著檔案 c： \\ files \\partial.txt 和 c： \\ files2partial.txt 的長度) \\ 。

如果將寫入器設定為檢查檔案還原，則只會在還原時檢查部分檔案的備份範圍。 檔案其他部分的修改將會被忽略。 如果設定 TestWriter 根項目的 deletePartialFiles 屬性，則在建立陰影複製之後，會立即從原始磁片區中刪除部分檔案。

## <a name="adding-differenced-files"></a>新增差異檔案

在處理 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)期間，寫入器可以將差異檔案新增至每個元件。 這些差異檔案會使用 [**>ivsscomponent：： GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)來回報。 您可以設定測試寫入器，藉由在元件專案中指定 DifferencedFile 子項目，來加入差異較差的檔案。

以下是具有兩個 DifferencedFile 子項目的元件元素範例：

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

與部分檔案不同的是，差異檔案絕不會部分符合 ComponentFile 規格。 DifferencedFile 元素中的檔案規格應該完全符合 ComponentFile (，就像範例) 的第一個差異檔案中一樣，否則它不應該完全相符，而是在 ComponentFile (所參考的磁片區上，如同第二個差異檔案) 。 日期和時間值應該相對於本地時區，但在回報給要求者之前，將會轉換為 GMT。 在此範例中，只會備份符合 c： \\ files \\ \*.txt 或 c： \\ files2 \\ \*.txt 的檔案，這些檔案已在1/22/2003:12:44:17 之後修改。

如果測試寫入器設定為檢查檔案還原，則只會檢查修改過的檔案進行還原。 如果設定 TestWriter 根項目的 deleteDifferencedFiles 屬性，就會在建立陰影複製後立即從原始磁片區中刪除差異的檔案。

## <a name="new-targets"></a>新目標

某些寫入器可讓要求者告知已選擇新位置來還原某些檔案。 寫入器表示它支援此模式，做為 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)所傳回之位元遮罩的一部分。 依預設，測試寫入器一律支援新目標。 將 TestWriter 根項目中的 supportsNewTarget 屬性設定為 "no"，即可停用這項支援。

如果寫入器支援新的目標，要求者可以藉由呼叫 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)，通知寫入器的新目標。 然後，寫入器會檢查新的目標位置，以確認還原，而不是原始的位置。

## <a name="more-information"></a>相關資訊

測試寫入器支援這裡未描述的更多設定選項。 測試編寫器所有設定功能的完整架構，都是在 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (for 64 位 Windows) 和 `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (32 位 Windows) 中指定的 swriter.xml。 這個檔案包含一個 XML 架構，可完整描述組成設定檔的所有元素和屬性。 在此檔案中的每個專案和每個屬性都會以描述，說明文件該元素或屬性的用途。

 

 




