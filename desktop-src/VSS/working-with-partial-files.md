---
description: 有時候只備份和還原部分的檔案會很有用。 VSS 提供部分的檔案機制，如果要求者支援，則允許寫入器指定部分檔案備份和還原。
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: 使用部分檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7194f01df11f6c0e368941e17ef6ab1620b17f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970176"
---
# <a name="working-with-partial-files"></a>使用部分檔案

有時候只備份和還原部分的檔案會很有用。 VSS 提供 [*部分*](vssgloss-p.md) 的檔案機制，如果要求者支援，則允許寫入器指定部分檔案備份和還原。

部分檔案作業通常最適合用來維護非常大型檔案的寫入器，只是備份作業之間變更的一小部分。 就這種情況而言，只複製變更為備份媒體的區段通常會很有説明。 基於這個理由，部分檔案作業通常（但不是專門）是用來支援增量備份和還原作業。

如果寫入器想要執行部分檔案作業，它會使用 [**CVssWriter：： IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) 來判斷它正在處理的要求者是否支援此作業。

如果要求者支援部分檔案作業，而且如果它將管理檔案的元件 (或定義元件的元件，而該元件包含) 至備份元件檔的檔案，則寫入器會指出要儲存的檔案區段 (通常會在處理 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) 或 [*PostSnapshot*](vssgloss-p.md) 事件) 時呼叫 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)。

除了路徑和檔案名之外，寫入器還會提供範圍、選擇性的中繼資料資訊給 [**>ivsscomponent：： AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)。

範圍資訊會以字串的形式提供，其中包含下列其中一項：

-   要 (備份到檔案中的位移組（以位元組為單位）) 以及要 (備份的區段長度（以位元組為單位）) 、以冒號分隔的位移和長度，以及以逗號分隔的每一組（例如 *Offset1 ***：**_array2d.length1_*_、_* * Offset2 ***：**_array3d.length2_）。

    每個值都是十六進位或十進位格式的64位整數 () 分別指定位元組位移和長度（以位元組為單位）。

-   二進位範圍檔案目前系統上的完整路徑（包括檔案名），包含下列各項：
    -    (的數位表示為包含在檔案中之相異檔案範圍的64位整數) 
    -   每個範圍都會以一組64位整數表示：這組的第一個成員是要備份之檔案的位移 (（以位元組) 為單位），而第二個成員是要備份之資料的長度 (以位元組為單位) 

如果寫入器使用範圍檔案來指定部分檔案作業，則要求者必須保證 (備份此檔案，即使檔案不一定是預設備份組的一部分) 或以其他方式在備份媒體上保留範圍資訊。 如果未備份範圍檔案的資訊，則不可能還原部份備份的檔案。

寫入器也可以加入包含中繼資料的字串。 此中繼資料可以是寫入器專屬的格式，因為它的目的是要讓寫入器驗證任何未來的還原。

透過此資訊，支援的要求者可以執行部分檔案備份。

例如，假設有一個大型檔案，其標頭 (位元組 64-512) 包含記錄計數和其他經常更新的資訊，而且最新的資料會在檔案的最後65536個位元組中找到（0x1239E8577A 至0x1239E7577A 的位元組）。

寫入器可以將範圍清單指定為字串 "**64：448，0x1239E8577A： 65536**"。

在還原和實際執行還原作業之前，要求者應該檢查是否有任何檔案需要部分檔案支援。

若要這樣做，要求者會先使用 [**>ivssbackupcomponents：： GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) 和 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)，在其備份元件檔中逐一查看具有預存元件的寫入器。

然後， [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) 介面會用來傳回 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面的實例，其提供 [**IVssWriterComponentsExt：： GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) 和 [**IVssWriterComponentsExt：： GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount)，可讓要求者取得 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例。

這可讓要求者使用 [**>ivsscomponent：： GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) 和 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) 來取得要參與還原的部份備份檔的相關資訊，該實例 [**會對應至**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 管理檔案 (的元件，或是定義包含檔案) 之元件集的元件。

如果部分檔案作業是由範圍檔案所控制，則應該在將資料複製回磁片之前將該檔案還原。 要求者可能會需要將範圍檔案複製回磁片上的新位置。 在此情況下，它會指出它已透過 [**>ivssbackupcomponents：： SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)完成。

然後，要求者會繼續將資料複製到已在磁片上的還原目的地中的適當位置。

寫入器 (處理 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)事件) 時，藉由檢查 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)所指出之檔案的 [**>ivsscomponent：： GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) ，判斷部分檔案作業是否成功。 寫入器應該一律使用位移資訊和備份元件檔中包含的任何中繼資料，嘗試驗證此還原的正確性。

如果要求者必須將範圍檔案還原至新位置，則 VSS 會更新此資訊，讓 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) 所傳回的路徑正確無誤。

 

 
