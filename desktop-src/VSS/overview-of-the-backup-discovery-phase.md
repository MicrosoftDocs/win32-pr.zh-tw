---
description: 呼叫 >ivssbackupcomponents：： GatherWriterMetadata 之後，要求者會使用從這個呼叫傳回的 IVssAsync 介面實例，判斷系統上的所有寫入器何時完成其寫入器元資料檔案的建立。
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: 備份探索階段總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3896abae03f9f2e53d353e5c439a5030c44faba943d4b84a04b564c2eef95cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937902"
---
# <a name="overview-of-the-backup-discovery-phase"></a>備份探索階段總覽

呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)之後，要求者會使用從這個呼叫傳回的 [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) 介面實例，判斷系統上的所有寫入器何時完成其寫入器元資料檔案的建立。 如需詳細資訊，請參閱 [在 VSS 下處理備份的總覽](overview-of-processing-a-backup-under-vss.md)。

此時，要求者可以開始探索階段，檢查中繼資料以判斷哪些應用程式正在執行，以及哪些磁片區必須是陰影複製才能取得完整備份。 下表顯示備份探索階段所需的動作和事件的順序。



| 要求者動作                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 事件 | 寫入器動作                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| 取出寫入器元資料檔案 (參閱 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)、 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) 。                                                                                                                                                                                                                                                                                                                                                 | 無  | 在這段期間，寫入器可能仍能繼續正常操作。 |
| 您可以使用元件及其檔案 [*集*](vssgloss-f.md)清單以及已排除的檔案，取得備份所牽涉的磁片區和檔案清單 (參閱 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)、 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) 。                                                                                                                                                                                                                                                                      | 無  | 無                                                                              |
| 選擇要備份的寫入器寫入器元資料檔案中的哪些元件。 針對每個元件呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) ，將它新增至備份元件檔。  (請參閱使用 [Selectability 進行備份](working-with-selectability-for-backup.md) ，並使用 [備份元件檔](working-with-the-backup-components-document.md)。 )                                                                                                                       | 無  | 無                                                                              |
| 初始化陰影複製集、內容和檢查支援的磁片區 (參閱 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)， [**>ivssbackupcomponents：： IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)) 。                                                                                                                                                                                                                                                                                   | 無  | 無                                                                              |
| 如果執行非元件備份，請針對每個磁片區呼叫 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) ，將所需的目標磁片區從寫入器元資料檔案新增至陰影複製集。 否則，針對寫入器元資料檔案中已經加入至備份元件檔的元件 (藉由呼叫 [**AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) ，要求者也必須針對每個受影響的磁片區呼叫 **>ivssbackupcomponents：： AddToSnapshotSet** 。 | 無  | 無                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>探索階段期間的寫入器動作

因為備份的探索階段主要是由要求者處理從寫入器元資料檔案中取出的資訊所組成，所以在寫入器上有一些需求。

理論上，寫入器可能會在此時繼續正常執行。 但是，寫入器可能會開始準備進行陰影複製和備份作業。

## <a name="requester-actions-during-the-discovery-phase"></a>探索階段期間的要求者動作

要求者會使用透過 [**>ivssbackupcomponents：： GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)取得的 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)物件，以反復查看所有寫入器的中繼資料，並選取要備份其資料的寫入器。

此時，要求者必須使用 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)逐一查看寫入器的元件，以產生每個寫入器備份候選項目的初始清單。 這會為要求者提供 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 物件，讓您可以使用 [**IVssWMComponent：： GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile)、 [**IVssWMComponent：： GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)和 [**IVssWMComponent：： GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)來取得要備份之檔案的規格。

由於 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 物件可以使用萬用字元來保存檔案位置資訊，因此可能需要使用 [**FindFirstFile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea)、 [**FindFirstFileEx**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)和 [**FindNextFile**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea)等函數。

在完成陰影複製之前，寫入器仍有可能在工作正常的情況下，從磁片新增或移除檔案，因此您不應該在此時產生實際要備份的檔案清單。

相反地，您可以藉由執行下列動作，在這裡找到要備份的檔案和磁片區的初始清單：

1.  在每個寫入器的寫入器元資料檔案中檢查所有可選取的備份和其元件 (使用 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) 並將它們組織成 [*元件集*](vssgloss-c.md) 使用 [*邏輯路徑*](vssgloss-l.md) (請參閱使用 [Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)) 
2.  [](vssgloss-e.md)使用 [ **>ivssbackupcomponents：： AddComponent** ，包括明確其備份元件的所有必要元件 (，而不是可選擇備份元件檔中的備份父項目)](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  選擇明確包含選用的，可供未使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) 定義元件集 (的備份元件使用) 
4.  藉由使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) （[*隱含地包含*](vssgloss-i.md)元件集的 [*子*](vssgloss-s.md)元件）明確地新增其定義可選取的備份 (元件，來選取要參與備份的 [*元件集*](vssgloss-c.md)。
5.  在選取的寫入器的寫入器元資料檔案和磁片區管理函式中使用檔案 [*集*](vssgloss-f.md) 資訊時，要求者會決定要備份的檔案路徑，以及需要陰影複製的磁片區。

請注意，只有在備份和備份元件檔中使用 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) 明確包含 (的元件，才會有新增至該檔之 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例。 這些實例將用來檢查和修改明確包含的元件及其任何隱含包含子群組件的元件設定 (參閱 [Selectability 和使用元件屬性](selectability-and-working-with-component-properties.md)) 。

如果寫入器包含任何寫入器的元件，則必須加入其所有必要的元件。 不過，要求者也可以完全略過所有寫入器的元件集。 如果未明確選取任何寫入器的元件，則不會選取寫入器，而 VSS 會禁止該寫入器參與備份作業的其餘部分。

要求者會藉由呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset)來起始包含所選磁片區的陰影複製集。

如果磁片區可參與陰影複製 (可使用 [**>ivssbackupcomponents：：) IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported) 檢查，則要求者可以使用 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)，將該磁片區新增至陰影複製集。

雖然通常不會有用處，但要求者有時也可以選擇要為指定的磁片區維持陰影複製的 [*提供者*](vssgloss-p.md) (請參閱 [選取提供者](selecting-providers.md) 以取得詳細資料) 。

請小心處理包含已載入資料夾或重新分析點的磁片區。 載入的資料夾或重新分析點可以出現在陰影複製中，並可進行備份。 但是，無法在陰影複製的磁片區上，執行裝載的資料夾或重新分析點 (請參閱) [使用掛接的資料夾和重新分析點](working-with-reparse-and-mount-points.md) 。

在備份中的這個階段，會將備份元件檔初始化和填滿。 在未來作業中，寫入器和要求者可以使用 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面來彼此通訊。

處理 [*PrepareForBackup*](vssgloss-p.md)、 [*PostSnapshot*](vssgloss-p.md)和 [*BackupComplete*](vssgloss-b.md)事件時，寫入器會獲得 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面的存取權。

 

 
