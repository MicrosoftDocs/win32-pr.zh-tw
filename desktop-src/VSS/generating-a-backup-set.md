---
description: 備份組是要備份的所有檔案、其位置，以及備份方式的清單。
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: 正在產生備份組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d9ecb90ac376aa9818b61e8dab65550ff8c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988745"
---
# <a name="generating-a-backup-set"></a>正在產生備份組

備份組是要備份的所有檔案、其位置，以及備份方式的清單。

在 >ivssbackupcomponents 之後，要求者必須使用陰影複製磁片區上包含的檔案 [**：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 成功傳回，以產生要備份之檔案的完整清單。

此外，要求者必須處理某些檔案具有 [*替代路徑*](vssgloss-a.md) ，且已排除某些檔案的可能性。

用來選取要備份之檔案的演算法應該依照寫入 [*器實例*](vssgloss-w.md) 、個別元件的方式 (，如同還原期間的情況一樣：請參閱 [產生還原集](generating-a-restore-set.md)) ，並可執行下列動作：

1.  判斷包含寫入器檔案和對應裝置物件的磁片區
2.  使用 [**IVssExamineWriterMetadata：：) GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)所傳回 [**之 IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)物件中所包含的檔案 [*集*](vssgloss-f.md)資訊 (，以建立明確排除的檔案清單（如有必要使用 **FindFileFirst**、 **FindFileFirstEx** 和 **FindNextFile**）。
3.  使用 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)逐一查看寫入器的所有元件。 如果選取了可選取的元件，請使用 [*邏輯路徑*](vssgloss-l.md) 來取得元件集內與其相關聯的其元件。  (，請參閱 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。 ) 
4.  使用 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)介面（對應至它所包含的每個元件）取得每個選取元件中包含的檔案 [*集*](vssgloss-f.md)。
5.  從規格產生檔案清單（如有必要，請使用 **FindFileFirst**、 **FindFileFirstEx** 和 **FindNextFile**）。
6.  從元件資訊所產生清單中的每個檔案，針對上述產生的排除檔案清單進行檢查。 這應該使用 [**IVssWMFiledesc：：) GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) 所傳回之檔案 (的預設路徑，而不是 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) 所傳回的替代路徑。 如果檔案符合排除的清單，將不會備份。
7.  選擇要用來備份 (的實際位置（若已設定）) 
8.  此時，可以使用完整的檔案及其位置清單，而且可以開始備份。

針對系統上的所有寫入器產生初始備份組之後，要求者接著會檢查下列登錄機碼：

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**

要求者會使用此機碼下的子機碼，如下所示：

-   如果系統上有寫入器，且有一個子機碼的名稱符合寫入器的名稱，則必須忽略該子機碼。
-   如果寫入器存在於系統上，但目前不存在於備份組內，而且有相符的子機碼，就會排除子機碼資料中指定的任何檔案，而且必須從備份組移除。
-   備份應用程式會建立多個 \_ SZ 值，其中包含不得備份之檔案的檔案規格清單，藉以將檔案新增至子機碼資料。 多個 SZ 值中的每個字串 \_ 都應該包含一個檔案規格。
-   檔案規格可以包含？ 和 \* 萬用字元。 您可以藉由將/s 附加至結尾，將規格設為遞迴。 例如，指定 "% TEMP% \\ \* /s" 會導致% temp% 目錄及其所有子目錄中的所有檔案都不會進行備份。

 

 



