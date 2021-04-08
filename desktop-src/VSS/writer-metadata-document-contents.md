---
description: 寫入器元資料檔案包含三組資料：寫入器識別碼和分類資訊、寫入器層級規格和元件資料。
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: 寫入器元資料檔案內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f222977f1c8d785e6f69613f219545dc3402af7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026228"
---
# <a name="writer-metadata-document-contents"></a>寫入器元資料檔案內容

寫入器元資料檔案包含三組資料：寫入器識別碼和分類資訊、寫入器層級規格和元件資料。

## <a name="writer-identification-information"></a>寫入器識別資訊

寫入器識別和分類資訊包括下列各項：

-   寫入器名稱
-   [*寫入器類別識別碼*](vssgloss-w.md)
-   [*寫入器實例*](vssgloss-w.md)
-   如何在主機系統上使用寫入器所管理的資料 (請參閱 [**VSS \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)) 
-   寫入器所管理的資料類型 (請參閱 [**VSS \_ 來源 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)) 

由於寫入器實例的例外狀況是唯一的，而且是由系統在 [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) 物件初始化時由系統所產生，因此所有這些值都是由寫入器在呼叫 [**CVssWriter：： Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) 時所設定，並藉由呼叫 [**IVssExamineWriterMetadata：： GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)來提供給要求者。

因為寫入器實例是唯一產生的，所以從預存寫入器元資料檔案中取出的預存寫入器實例不太可能很有用。

藉由檢查 [**VSS \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)，應用程式可以判斷寫入器是否管理一般應用程式資料，或其使用的檔案是系統開機狀態的一部分或系統服務所使用的檔案。 備份與還原應用程式必須遵守使用類型，以協助維護系統穩定性。

[**VSS \_ 來源 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)旗標會指出寫入器管理要備份的資料在正常操作期間執行的應用程式類型。

目前，差別僅限於指定寫入器是否要在交易式或非交易式資料庫作業中產生檔案，或檔案是否為更一般活動類型的結果。 這份清單可能會隨著時間成長。 這項資訊有助於判斷寫入器檔案中預期的一般活動層級。

## <a name="writer-level-specification"></a>Writer-Level 規格

寫入器層級規格包含在其範圍內全作者的寫入器，適用于所有資料，而不受元件管理。

寫入器一律必須指定 [*還原方法*](vssgloss-r.md)。

您可以選擇性地指定下列各項：

-   排除檔案清單
-   用於還原的 [*替代位置*](vssgloss-a.md)對應

包含和排除檔案清單包含元件中的檔案資訊，而其規格則取代元件規格。

## <a name="restore-method-specification"></a>Restore 方法規格

[*Restore 方法*](vssgloss-r.md)是透過 [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)在寫入器元資料檔案中設定，並由 [**IVssExamineWriterMetadata：： GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)的要求者抓取。

在設定還原方法時，寫入器會針對寫入器所管理的所有檔案，指出檔案還原的慣用方式（也稱為原始還原目標）。 例如，restore 方法會指定是否應該允許寫入器所管理的所有檔案覆寫目前在磁片上的檔案。 如需詳細資訊， (參閱 [Vss 還原](vss-restore-configurations.md) 設定和 [**vss \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 。 ) 

## <a name="exclude-file-list-specification"></a>排除檔案清單規格

排除清單可讓您明確地防止特定檔案包含在備份組內，以微調元件中的萬用字元規格。

例如，元件可能有檔案 [*集*](vssgloss-f.md)，其中包含 c： Database 的檔案規格 \\ \\ \* \* 。 雖然這是很方便的定義，但有時候可能會產生暫存檔案 (可能是 \* .tmp) ，而寫入器一律想要防止其備份。

在此情況下，寫入器會 \* 使用 [**IVssCreateWriterMetadata：： AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)將 .tmp 新增至其排除清單。 此規格可以是遞迴的。

要求者會使用 [**IVssExamineWriterMetadata：： GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)來查詢這項資訊。

排除檔案清單優先于元件檔案清單。

因此，在寫入器元資料檔案中指定用於備份的檔案清單，會由 [*明確包含*](vssgloss-e.md) 的元件中指定的所有檔案和 [*隱含包含*](vssgloss-i.md) 的元件，而不是所有排除的檔案所組成。

## <a name="alternate-location-mappings-specification"></a>替代位置對應規格

在建立寫入器元資料檔案時，一開始會設定替代位置對應，並指出當您無法將檔案還原至原始位置時，可以還原檔案的磁片位置。

這項資訊會以以 null 結尾的寬字元字串的形式加入 [**IVssCreateWriterMetadata：： AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) ，並由 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)取出為 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)物件。

雖然替代位置對應是使用寫入器層級介面來指定和檢查 ([**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 和 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) ，但是它們是以 [*檔集*](vssgloss-f.md)的方式指定。 用來指定替代位置對應的檔案集 (路徑、檔案規格和遞迴旗標) 必須符合其中一個已新增至寫入器元件的檔案集 (請參閱 [將檔案新增至元件](definition-of-components-by-writers.md)) 。

如需詳細資訊，請參閱 [非預設的備份與還原位置](non-default-backup-and-restore-locations.md)。

## <a name="component-level-information"></a>Component-Level 資訊

[*元件*](vssgloss-c.md) 是針對備份和還原用途形成邏輯單元的檔案集合。 元件中的所有檔案 (除了明確排除的) 必須以一個單位來備份和還原。

寫入器會使用 [**IVssCreateWriterMetadata：： AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)來新增元件，並指定下列元件資訊：

-   類型
-   名稱
-   邏輯路徑 (是否有任何) 
-   支援的功能
-   [*Selectability*](vssgloss-s.md)
-   在還原期間，寫入器所使用的中繼資料
-   顯示資訊
-   通知資訊

[*Selectability for backup*](vssgloss-s.md) 和 [*Selectability for restore*](vssgloss-s.md) 完全獨立，而且寫入器會搭配邏輯路徑使用它們來指出它所管理的各種元件之間的關聯性。 寫入器可以指出 [*明確包含*](vssgloss-e.md) 哪些元件 (明確包含的元件，而這些元件可能明確包含在要求者) ，以及只能 [*隱含包含*](vssgloss-i.md)的元件。  (，請參閱 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。 ) 

您可以使用 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)，將檔案加入至指定的元件。  (參閱 [將檔案新增至元件](definition-of-components-by-writers.md)。 ) 

在備份期間將檔案新增至元件時，寫入器必須指定檔案集 (路徑、檔案規格和遞迴旗標，) 定義要備份的檔案。

寫入器也可以指定備份的 [*替代路徑*](vssgloss-a.md) ，這應該不會與先前所述的 [*替代位置*](vssgloss-a.md) 對應混淆。 此替代路徑表示備份磁片區時，要從中複製檔案的非預設位置。

您可以透過 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)傳回的 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)介面，取得寫入器元資料檔案中指定元件的相關資訊。

檔案和路徑會在 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 中以 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 物件的形式傳回。

[作者在元件定義](definition-of-components-by-writers.md)中會詳細討論寫入器的元件資訊。

 

 



