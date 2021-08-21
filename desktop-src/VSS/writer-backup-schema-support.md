---
description: 若要完整地執行備份，必須參與系統的寫入器。
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: 寫入器備份架構支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b037591d6deda2657acdfe4f4e4755fef96b52bafc92e4cc51e4ef7119de1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344241"
---
# <a name="writer-backup-schema-support"></a>寫入器備份架構支援

若要完整地執行備份，必須參與系統的寫入器。 不同類型的支援備份稱為「架構」（schema），並由「 (」或「 [**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) 列舉」成員的位 or) 表示。 目前支援的有效架構包括下列各項：

-   預設架構： Full (VSS \_ BS \_ 未定義的) -表示寫入器支援備份，其中所有檔案都會備份，不論其上次備份日期為何。 要求者可以更新每個檔案的備份歷程記錄，而寫入器支援 VSS \_ BS 時間 \_ 戳的列舉值，它會將更新的時間戳記與要求者一起儲存。 此備份配置可用來作為增量或差異備份的基礎。

    還原完整備份只需要單一備份映射。

-   複本備份 (VSS \_ BS \_ 複製) （像是 vss \_ BS \_ 完整備份架構）指出寫入器支援備份，其中所有檔案都會備份，不論其上次備份日期為何。 不過，「要求者」或「寫入器」不會更新每個檔案的備份歷程記錄，也不能使用這類備份作為增量或差異備份的基礎。
-   記錄檔 (VSS \_ BS \_ 記錄) -只會備份寫入器的記錄檔。 這需要寫入器至少使用 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 方法，將至少一個檔案新增至至少一個元件。 這是 VSS 專用的備份類型。
-   自訂還原位置 (VSS \_ BS \_ 寫入器 \_ 支援 \_ 新 \_ 的目標) —表示在還原時，要求者會在還原時變更其檔案的寫入器支援。 這表示已使用 [**>ivsscomponent：： GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) 將寫入器編碼為檢查這類重新配置 (，並具有使用重新放置檔案的容量。
-   Restore with Move (VSS \_ BS \_ 寫入器 \_ 支援 \_ restore \_ with \_ move) -表示寫入器支援使用相同的類別 ID 執行多個寫入器實例，並支援要求者在還原時將元件移至不同的寫入器實例。 寫入器實例是使用做為 *wszWriterInstanceName* 參數傳遞至 [**CVssWriter：： Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) 方法的持續性寫入器實例名稱來指定。 要求者可以使用 [**IVssExamineWriterMetadataEx：： GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) 取得寫入器實例名稱，並在還原期間使用 [**IVssBackupComponentsEx：： SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)來移動元件。

    **Windows Server 2003 和 Windows XP：** 在 Windows Server 2003 Service Pack 1 (SP1) 之前，不支援這個值。

-   增量 (VSS \_ BS 累加 \_ 式) -指出寫入器使用 VSS API 來協助要求者，以確保只有在上一次完整或增量備份之後變更或新增的檔案才會複製到儲存媒體。

    還原增量備份需要原始備份映射，以及自初始備份之後所做的所有增量備份映射。

-   差異 (VSS \_ BS \_ 差異) -指出寫入器使用 vss API 來協助要求者確保只會將上次完整備份之後變更或新增的檔案複製到儲存媒體; 所有的中繼備份資訊都會被忽略。

    還原差異備份需要原始備份映射，以及自上次完整備份之後所做的最新差異備份映射。

-   增量/差異： (VSS BS 有時間戳記) 的時間戳記支援 \_ \_ -指出寫入器支援使用 VSS 時間戳記機制，在增量或差異作業中包含檔案。 在備份時，寫入器必須使用 [**>ivsscomponent：： SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)方法儲存檔案 [*集的*](vssgloss-f.md)備份戳記，並在還原時使用 [**>ivsscomponent：： GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)來取得它。
-   累加/差異：上次修改的時間支援 (VSS \_ BS \_ 上次 \_ 修改) —表示在以差異檔案執行增量或差異備份時，寫入器可以獨立提供最後修改時間資訊。 您可以透過 [**>ivsscomponent：： AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) 方法，將這種資訊提供給要求者。
-   增量/差異： (VSS \_ BS 獨佔累加 \_ \_ \_ 差異) 的支援限制-指出差異或增量備份架構的寫入器支援，但僅限專用：例如，您不能遵循增量備份和差異備份。
-   獨立系統狀態 (VSS \_ BS \_ 獨立 \_ 系統 \_ 狀態) -指出寫入器支援備份屬於系統狀態的資料，但也可獨立于系統狀態時進行備份。

    **Windows Server 2003 和 Windows XP：** 在 Windows Vista 之前，不支援這個值。

-   Roll-Forward Restore (VSS \_ BS \_ 向前復原 \_ Restore) -指出寫入器支援使用 [**IVssBackupComponentsEx2：： SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward)設定向前復原還原點的要求者。

    **Windows Server 2003 和 Windows XP：** 在 Windows Vista 之前，不支援這個值。

-   還原重新命名 (VSS \_ BS \_ 還原 \_ 重新命名) -表示寫入器支援要求者設定使用 [**IVssBackupComponentsEx2：： SetRestoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename)的還原名稱。

    **Windows Server 2003 和 Windows XP：** 在 Windows Vista 之前，不支援這個值。

-   授權還原 (VSS \_ BS \_ 授權 \_ 還原) -指出寫入器支援要求者使用 [**IVssBackupComponentsEx2：： SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore)設定授權還原。

寫入器會使用 [**IVssCreateWriterMetadata：： SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) 方法來設定其架構，而要求者會藉由呼叫 [**IVssExamineWriterMetadata：： GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)來取得每個寫入器的架構。

 

 



