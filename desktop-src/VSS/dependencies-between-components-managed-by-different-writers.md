---
description: 有些情況下，來自某個寫入器的資料相依于其他寫入器所管理的資料。 在這些情況下，您應該備份或還原來自兩個寫入器的資料。
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: 不同寫入器所管理元件之間的相依性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba3be6a2c2f0a722c4c5f06ca95351e004e1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320684"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>不同寫入器所管理元件之間的相依性

有些情況下，來自某個寫入器的資料相依于其他寫入器所管理的資料。 在這些情況下，您應該備份或還原來自兩個寫入器的資料。

VSS 會透過明確的寫入器元件相依性和 [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) 介面的概念來處理這個問題。

寫入器會在使用 [**IVssCreateWriterMetadata：： AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) 方法建立寫入器元資料檔案時，新增一個或多個相依性。 寫入器會將其所) 管理之相依元件 (的名稱和邏輯路徑傳遞給方法，以及名稱和邏輯路徑，以及 [*寫入器類別識別碼*](vssgloss-w.md) (GUID，以識別其相依元件) 的類別。

一旦建立之後，此相依性會通知要求者在任何備份或還原作業期間，相依元件和其相依性的目標都必須參與。

給定的元件可以有多個相依性，這會要求它及其所有相依的目標同時參與備份和還原。

相依元件和（或）目標 (s) 其相依性可以 [*明確*](vssgloss-e.md) 或 [*隱含*](vssgloss-i.md) 地包含在備份或還原作業中。

明確的寫入器元件相依性機制不應用來建立相同寫入器上兩個元件之間的相依性。 選取規則可以更有效率地提供相同的功能，而不會有迴圈相依性的風險。

例如，您可以使用 [**IVssCreateWriterMetadata：： AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) 來定義元件 writerData (的相依性，其為元件 internetData (上的寫入器 MyWriter 的邏輯路徑 "" ) ，而且具有寫入器類別識別碼 X 之寫入器的邏輯路徑 "" ) 為 InternetConnector。 (雖然可能有多個具有相同類別識別碼的寫入器同時在系統上，但會避免混淆，因為邏輯路徑和元件名稱的組合在 VSS 下的系統上是唯一的。 ) 

寫入器會將多個相依性加入至指定的元件，只要呼叫 [**IVssCreateWriterMetadata：： AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) ，就可以從不同的寫入器重複使用不同的元件。 您可以藉由檢查 [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)結構的 **cDependencies** 成員，找到指定元件相依的其他元件數目。

寫入器或要求者會使用 [**IVssWMComponent：： GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)來抓取 [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)介面的實例。 **IVssWMDependency** 會傳回管理相依性目標群組件之寫入器的元件名稱、邏輯路徑和類別識別碼。

相依性機制不規定相依元件與其相依性目標之間的任何特殊喜好設定順序。 如上所述，所有的相依性都是指每當指定的元件是備份或還原時，它所相依的元件或元件也必須一併進行備份或還原。 確切的相依性實作為備份應用程式的判斷。

例如，在上述案例中，元件 writerData (邏輯路徑 "" ) 相依于元件 InternetConnector (邏輯路徑「連接」 ) 。 要求者可以用下列其中一種方式來解讀：

-   如果選取了相依元件 writerData， (隱含或明確) 進行備份或還原，要求者必須以隱含或明確的方式選取 (，) 其相依性的目標，internetData
-   如果未選取要進行備份的相依性（internetData）目標，則不應選取相依元件 writerData。

不過，在開發相依性的支援時，要求者開發人員應該注意，沒有任何方法可讓寫入器判斷其中一個元件是否為相依性的目標。

## <a name="declaring-remote-dependencies"></a>宣告遠端相依性

分散式應用程式是一種應用程式，可以設定為一次使用一或多部電腦。 應用程式通常會在一或多部應用程式伺服器電腦上執行，並與 (通訊，但不一定會在一或多部資料庫伺服器電腦) 上執行。 這項設定有時稱為多重系統部署。 通常相同的應用程式也可以設定為在執行應用程式伺服器和資料庫伺服器的單一電腦上執行。 這種設定稱為單一系統部署。 在這兩種設定中，應用程式伺服器和資料庫伺服器各自都有各自獨立的 VSS 寫入器。

在多重系統部署中，如果應用程式寫入器所管理的元件相依于由資料庫伺服器寫入器管理的遠端元件，這就稱為遠端相依性。 相較之下， (單一系統部署，只有本機相依性。 ) 

作為多系統部署的範例，請考慮使用 SQL Server 資料庫伺服器作為資料存放區的應用程式伺服器。 應用程式特定的資料（包括 web 元件、web 內容檔案和 IIS 中繼資料）位於一或多部電腦上，稱為前端網頁伺服器。 實際的 SQL 資料存放區（包括 Config 資料庫和多個內容資料庫）位於一或多部其他電腦（稱為後端資料庫伺服器）。 每一部前端網頁伺服器都會包含相同的應用程式專屬內容和設定。 每個後端資料庫伺服器都可以裝載任何內容資料庫或設定資料庫。 應用程式軟體只會在前端網頁伺服器上執行，而不會在資料庫伺服器上執行。 在此設定中，應用程式的 VSS 寫入器對 SQL 寫入器所管理的元件具有遠端相依性。

寫入器可以宣告遠端相依性，方法是呼叫 [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)方法，並在前面加上 " \\ \\ *RemoteComputerName* \\ "，其中 *RemoteComputerName* 是遠端元件所在的電腦名稱稱，而是 *wszOnLogicalPath* 參數中的邏輯路徑。 *RemoteComputerName* 的值可以是 IP 位址或 [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)函數所傳回的電腦名稱稱。

**Windows Server 2003：** 在 Windows Server 2003 Service Pack 1 (SP1) 之前，寫入器無法宣告遠端相依性。

為了識別相依性，要求者會呼叫 [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)介面的 [**GetWriterId**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid)、 [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)和 [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname)方法。 要求者必須檢查 **GetComponentName** 在 *pbstrComponentName* 參數中傳回的元件名稱。 如果元件名稱的開頭是 " \\ \\ "，則要求者必須假設它指定遠端相依性，而 "" 後面的第一個元件 \\ \\ 是在寫入器呼叫 [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)時所指定的 *RemoteComputerName* 。 如果元件名稱的開頭不 \\ \\ 是 ""，則要求者應假設它指定本機相依性。

如果有遠端相依性，要求者在備份本機組件時，必須備份遠端元件。 若要備份遠端元件，要求者應該在遠端電腦上有代理程式，並在遠端電腦上起始備份。

## <a name="structuring-remote-dependencies"></a>結構化遠端相依性

請務必瞭解相依性並非本身的元件。 需要元件才能保存相依性。

下列範例示範兩種結構一組相依性的方式。

``` syntax
Example 1:
    Writer 1
        Component A
            File A
            File B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")

Example 2:
    Writer 2
        Component A
            File A
            File B
        Component B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")
```

在範例1中，相依性是由元件 A 所持有。由於只能選取元件，而不是個別檔案，因此以這種方式來結構化元件 A 的相依性時，必須一律將整個元件（包括檔案和相依性）同時備份和還原。 它們無法個別備份或還原。

在範例2中，個別元件 (元件 A 和 B) 保存每個相依性。 在此情況下，您可以獨立選取這兩個元件，因此會獨立備份和還原。 以這種方式來結構化相依性，可讓分散式應用程式更有彈性地管理其遠端相依性。

## <a name="supporting-remote-dependencies"></a>支援遠端相依性

要求者可以提供遠端相依性的完整或部分支援。

若要提供完整的支援，要求者應在備份和還原時間進行下列動作。

在備份時，要求者必須在前端 (本機) 電腦上啟動備份、判斷存在的相依性，以及多工緩衝處理其他備份工作來捕捉後端資料庫。 要求者必須等到遠端電腦上的後端備份工作完成後，再呼叫 [**>ivssbackupcomponents：： SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) 和 [**>ivssbackupcomponents：： BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) 方法。 如果要求者等到後端元件的備份完成，然後再呼叫 **BackupComplete**，這將會產生更容易復原的寫入器備份，以在備份期間執行其他增強功能（例如拓撲鎖定）。 下列程式概述要求者應執行的動作：

1.  在本機電腦上，要求者會呼叫 [**>ivssbackupcomponents：： InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)、 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)、 [**>ivssbackupcomponents：:P Repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)和 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) 方法。
2.  完成本機陰影複製，但在備份完成之前，要求者將要求傳送至遠端電腦上的代理程式，以將額外的備份工作多工緩衝。
3.  在遠端電腦上，要求者的代理程式會藉由呼叫 [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)、 [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)、 [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)、 [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)、 [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)和 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)，來執行多工緩衝處理的備份順序。
4.  當要求者的代理程式已完成遠端電腦上的多工緩衝處理工作時，要求者會藉由呼叫 [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) 和 [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)來完成備份順序。

在還原時，要求者必須啟動牽涉到前端 (本機) 電腦的還原、選取要還原的元件及其相依性，然後藉由呼叫 **>ivssbackupcomponents：:P rerestore** 方法來傳送 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)事件。 接著，要求者應該在遠端電腦上將後端還原工作多工緩衝處理，並在後端還原完成時呼叫 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 方法。 這項需求讓前端寫入器可以更充分掌控還原體驗和整體的系統管理員使用者體驗。 由於每個系統上的備份都不會在相同的時間點發生，因此前端寫入器必須執行一些清除後端資料。 在先前「宣告遠端相依性」中所討論的範例應用程式中，寫入器應該在還原其中一個後端資料庫完成之後，起始網站重新對應或重新編制索引。 若要這樣做，寫入器必須在前端伺服器上接收事件。 下列程式概述要求者應執行的動作：

1.  在本機電腦上，要求者會呼叫 [**>ivssbackupcomponents：： InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)、 [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)、 [**>ivssbackupcomponents：： SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (或 [**IVssBackupComponentsEx：： SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) 和 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)。
2.  在 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 階段完成之後，但在 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 階段開始之前，要求者會將要求傳送至遠端電腦上的代理程式，以將額外的還原工作多工緩衝。
3.  在遠端電腦上，要求者的代理程式會藉由呼叫 [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)、 [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)、 [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)、 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)、 [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (或 [**SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) 和 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)，來執行多工緩衝處理還原作業。
4.  當要求者的代理程式已完成遠端電腦上的多工緩衝處理工作時，要求者會藉由呼叫 [**>ivssbackupcomponents：： SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) 和 [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)來完成還原順序。

為了提供遠端相依性的部分支援，要求者必須遵循遠端相依性，並將它們包含在備份中，但是前端和後端系統上的事件順序並不是必要項。 對於僅執行部分支援的要求者，要求者應該參考寫入器應用程式的備份/還原檔，以瞭解可以支援的案例。

 

 
