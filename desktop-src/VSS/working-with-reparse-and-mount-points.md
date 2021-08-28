---
description: 處理元件的其中一個檔案集時，可能需要要求者以遞迴方式遍歷目錄樹狀結構，而這可能需要要求者處理掛接的資料夾和重新分析點 (例如指向不在目前磁片區上之資料的連結) 。
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: 使用裝載的資料夾和重新分析點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1162d1d7da5869f588ae61d9235ec3d5827265c5eb9deaa23c38b8b9e85db68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905058"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>使用裝載的資料夾和重新分析點

處理元件的其中一個檔案集時，可能需要要求者以遞迴方式遍歷目錄樹狀結構，而這可能需要要求者處理掛接的資料夾和重新分析點 (例如指向不在目前磁片區上之資料的連結) 。

要求者在遍歷目錄樹狀結構時，應該遵循掛接的資料夾和重新分析點，而 VSS 則有妥善定義的指導方針來處理它們來進行備份和還原作業。

若要說明這些指導方針，請考慮下列範例：

-   磁片區 \\ \\ ？ \\磁片區 {GUID \_ 1} 具有磁碟機號 C： \\ 。
-   檔案集的路徑為 C： \\ WriterData。
-   檔案規格 \* 。此檔案會使用 dat。
-   檔案集的遞迴會設定為 **TRUE**。
-   目錄 C： \\ WriterData 位於磁片區 \\ \\ ？ \\磁片區 {GUID \_ 1}。
-   目錄 C： \\ WriterData \\ Archive 是掛接的資料夾。
-   磁片區 \\ \\ ？ \\磁片區 {GUID \_ 2} 與裝載的資料夾 C： \\ WriterData Archive 相關聯 \\ 。

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>在備份期間處理裝載的資料夾和重新分析點

執行遞迴備份時，在 VSS 下處理裝載的資料夾和重新分析點的基本規則，可摘要如下：

-   路徑會在已裝載的資料夾和重新分析點上遵循。
-   如果載入的資料夾或重新分析點指向磁片區，該磁片區應該會被陰影複製。
-   如果磁片區包含已掛接的資料夾或重新分析點，這些資料夾將會出現在磁片區的陰影複製中。
-   裝載的資料夾或重新分析點下的資料會在掛接的資料夾或重新分析點指向之磁片區的陰影複製中捕捉。

為了說明使用上述範例，因為已設定遞迴旗標，要求者必須檢查 C： WriterData Archive 下的所有資料， \\ \\ 以及以下的資料。

要求者必須新增磁碟機號 C： (的磁片區 \\ \\ \\ ？ \\磁片區 {GUID \_ 1} ) ，以及與裝載的資料夾 C： \\ WriterData Archive (相關聯的磁片區 \\ \\ \\ ？ \\磁片區 {GUID \_ 2} 使用 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)) 至陰影複製集。

載入的資料夾 C： \\ WriterData \\ Archive 會出現在磁片區的陰影複製中 \\ \\ ？ \\磁片區 {GUID \_ 1}，其具有名為 deviceObject1 的裝置物件。

不過，VSS 不會在該掛接的資料夾下複製任何資料 (資料 \\ \\ 嗎？ \\磁片區 {GUID \_ 2} ) 到 deviceObject1 所參考的陰影複製。 而是在的陰影複製中捕捉該資料 \\ \\ 嗎？ \\磁片區 {GUID \_ 2}，其具有名為 deviceObject2 的裝置物件。

因此，在 C： WriterData 下備份陰影複製檔案的要求者 \\ 將會使用 deviceObject1 WriterData 的路徑 \\ 來搜尋符合 C： WriterData 的檔案 \\ \\ \* 。

若要備份 C： WriterData Archive 下的陰影複製 \\ \\ 檔案，要求者將會使用 deviceObject2 (的路徑，因為根目錄是 \\ \\ ？ \\磁片區 {GUID \_ 2} 與裝載的資料夾 C： Writer 封存) 建立關聯 \\ \\ ，以搜尋符合 C： \\ WriterData Archive 的檔案 \\ \\ \* 。

請注意，重新分析點的處理方式與裝載的資料夾相同。 重新分析點會出現在第一個磁片區的陰影複製中。 重新分析點下的資料會出現在第二個磁片區的陰影複製中。

在備份期間，要求者應儲存掛接的資料夾及其相關聯之磁片區的相關資訊，以及重新分析點及其目標，以確保所有資料都已正確備份和還原。

## <a name="handling-mount-and-reparse-points-during-restore"></a>在還原期間處理掛接和重新分析點

還原檔案時，要求者必須遵循與備份期間不同的指導方針 (忽略 [*替代位置對應*](vssgloss-a.md) 和 [*新的目標位置*](vssgloss-n.md)) 等問題：

-   如同之前，如果需要遞迴，則會在裝載的資料夾和重新分析點上遵循路徑。
-   已載入的資料夾將會還原。
-   裝載的資料夾和重新分析點的還原位置是由其原始路徑所決定。

如果備份與還原之間有磁片區名稱，也就是說，您不需要重新建立磁片區，則還原的已載入資料夾和重新分析點應該指向正確的磁片區。

因此，在上述範例中，如果已將裝載的資料夾 C： \\ WriterData \\ Archive 還原至 (\\ \\ ？ \\磁片區 {GUID \_ 1} ) ，且先前與其相關聯的磁片區已還原到 (\\ \\ 嗎？ \\磁片區 {GUID \_ 2} ) ，還原的檔案和檔案結構會是正確且一致的。

資料可能會在磁片區名稱變更的系統上還原。 這可能是因為磁片損毀，而您可能需要手動執行系統復原並重新建立磁片區。 在這種情況下，在還原之後，裝載的資料夾和重新分析點將不再有效。 若要在還原的磁片區上重新建立檔案和檔案結構，將需要刪除已還原的已掛接資料夾和重新分析點，然後在磁片上重新建立它們。 備份應用程式會決定是否適當。

請注意，已載入之資料夾的還原目的地可能已被佔用。 例如，C： \\ WriterData \\ Archive 可能已經包含一些檔案。 備份應用程式會決定如何處理這種情況。

 

 



