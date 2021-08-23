---
description: 在備份作業期間，要求者會使用 >ivssbackupcomponents：： SetBackupState 來定義進行中的作業類型。
ms.assetid: 43dcdac7-ed8e-4150-83eb-585e0e92f13c
title: VSS 備份狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35701e1b576d9ea2e5464516589ae419dc73b74898768af06e974da05afffa8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056216"
---
# <a name="vss-backup-state"></a>VSS 備份狀態

在備份作業期間，要求者會使用 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) 來定義進行中的作業類型。

這項資訊不包含在備份元件檔中可輕易取出的表單中，因此，要求者開發人員應該在任何備份媒體上獨立儲存此資訊。

備份狀態包含下列各項：

<dl> <dt>

<span id="Backup_Type"></span><span id="backup_type"></span><span id="BACKUP_TYPE"></span>備份類型
</dt> <dd>

備份類型會指定用來識別要備份之檔案的準則。 這些準則的評估必須使用 VSS API 來進行。

當您決定要採用的備份類型，以及要使用哪個寫入器時，要求者應該檢查 (或架構的種類，請參閱 [寫入器備份架構支援](writer-backup-schema-support.md)) 每個系統寫入器支援的備份作業。 VSS 下的備份可以是下列類型：

-   Full (VSS \_ BT \_ full) —無論上次備份日期為何，都會備份檔案。 將會更新每個檔案的備份歷程記錄，而這種類型的備份可作為增量或差異備份的基礎使用。 還原完整備份只需要單一備份映射。
-   複本備份 (VSS \_ bt \_ 複製) （例如 vss \_ bt \_ 完整備份類型），不論其上次備份日期為何，都會備份檔案。 不過，每個檔案的備份歷程記錄將不會更新，而且這類備份無法當做增量或差異備份的基礎。
-   增量 (VSS \_ BT \_ 增量) -vss API 是用來確保只有在上一次完整或增量備份之後已變更或新增的檔案才會複製到儲存媒體。 還原增量備份需要原始備份映射，以及自初始備份之後所做的所有增量備份映射。
-   差異 (VSS \_ BT \_ 差異) -vss API 是用來確保只有在上一次完整備份之後變更或新增的檔案會複製到儲存媒體; 所有的中繼備份資訊都會被忽略。 還原差異備份需要原始備份映射，以及自上次完整備份之後所做的最新差異備份映射。
-   記錄檔 (VSS \_ BT \_ 記錄檔) -只有寫入器的記錄檔 (以 [**IVssCreateWriterMetadata：： AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 方法新增至元件的記錄檔，並藉由呼叫 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) 進行取出。 這是 VSS 專用的備份類型。

要求者可以使用 VSS 以外的資訊和方法來執行這些備份。 只有當要求者使用 VSS API 來執行備份時，才應該將其視為具有其中一個列出的備份類型。 比方說， \_ \_ 只有當要求者使用 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) 所傳回的資訊來識別記錄檔時，才會參與 VSS BT 記錄類型的備份。 同樣地，VSS \_ bt \_ 增量和 vss \_ bt \_ 差異類型只適用于增量或差異作業，如 [增量和差異備份](incremental-and-differential-backups.md)中所述。

</dd> <dt>

<span id="Specification_about_Selectability"></span><span id="specification_about_selectability"></span><span id="SPECIFICATION_ABOUT_SELECTABILITY"></span>Selectability 的規格
</dt> <dd>

VSS 備份可能會選擇使用元件 selectability 的 VSS 概念（這稱為「 [*元件模式*](vssgloss-c.md)」），或忽略它們。

未在元件模式中執行的範例將會執行系統映射備份，其中備份應用程式需要寫入合作以確保資料穩定性，但在這種情況下，不會有相關的元件選取。

</dd> <dt>

<span id="Saving_Bootable_State"></span><span id="saving_bootable_state"></span><span id="SAVING_BOOTABLE_STATE"></span>正在儲存可開機狀態
</dt> <dd>

VSS 支援在完全可開機的設定中儲存正在執行的系統狀態。 不過，這不一定是必要的，而寫入器準備儲存可開機狀態有時可能會降低執行中系統的即時效能。

因此，要求者會指出備份是否包含可開機的系統狀態，作為 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)的引數。 寫入器會藉由呼叫 [**CVssWriter：： IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)來判斷是否必須支援儲存可開機的系統狀態。

即使未選取 [可開機的系統狀態]，也會建立系統檔案的陰影複製，而且可能會備份檔案案。

但是，如果備份未儲存可開機的系統狀態，請務必小心還原系統檔案 (查看[Windows Server 2003 R2 和 Windows server 2003 SP1) 中的系統狀態備份和還原](backing-up-and-restoring-system-state-under-vss.md)。

您無法從已抓取的備份元件檔中復原這項資訊，因此要求者作者應儲存系統是否以可開機的系統狀態備份。

</dd> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>部分檔案支援
</dt> <dd>

有些寫入器支援透過覆寫所管理之檔案的部分來還原檔。 要求者可以設計來利用這種方式，如果是，則會藉由設定 [**>ivssbackupcomponents：： SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)中的資訊來指出這一點。

</dd> </dl>

 

 



