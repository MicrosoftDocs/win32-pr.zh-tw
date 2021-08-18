---
description: 元件是由寫入器元資料檔案中的寫入器所定義和具現化，以回應在備份作業開始時的識別事件 (查看填入寫入器元資料檔案時) 備份初始化的總覽。
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: 作者的元件定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fa08acba3c49cd99e83a5dcc901d4a12108a9dc6dde9891add93bcc54e3566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136375"
---
# <a name="definition-of-components-by-writers"></a>作者的元件定義

元件是由寫入器元資料檔案中的寫入器所定義和具現化，以回應在備份作業開始時的 [*識別事件*](vssgloss-i.md) (查看填入寫入器元資料檔案時) [備份初始化的總覽](overview-of-backup-initialization.md) 。

使用 [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) 和 [**IVssCreateWriterMetadata：： AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)在其寫入器元資料檔案中建立元件時，寫入器必須指定：

-   是否可選取元件 [*以進行備份*](vssgloss-s.md)
-   元件類型
-   元件名稱 (在指定的 [*寫入器實例*](vssgloss-w.md) 內必須是唯一的，但在所有的寫入器實例中必須是唯一的) 
-   元件是否有任何與其相關聯的寫入器特定中繼資料
-   寫入器是否需要成功備份之後的通知

寫入器可以選擇性地指定：

-   元件的 [*邏輯路徑*](vssgloss-l.md) (必須是唯一的，但不能只在指定的寫入器實例內，而是在所有的寫入器實例中) 
-   元件描述 (或標題) 
-   用於 Gui 以表示元件的圖示

元件不需要實際包含任何檔案。 這類空白或「虛擬」元件在組織元件方面很有用。 這類元件可以用來定義 [*元件集*](vssgloss-c.md) 和寫入器的元件 (請參閱) [元件的邏輯路徑](logical-pathing-of-components.md) 。

## <a name="setting-up-component-organization"></a>設定元件組織

設定元件的 [*selectability*](vssgloss-s.md) (其 [*selectability 進行備份*](vssgloss-s.md)，並將它的 [*selectability 用於還原*](/windows)) 與其 [*邏輯路徑*](vssgloss-l.md) ，可讓寫入器在備份或還原作業中，強制或選擇性地包含特定元件，並將元件組成 [*元件集*](vssgloss-c.md) ，並將一個可選取的元件當做整個群組的進入點。

這些群組中的成員資格會決定在備份和還原作業期間將使用哪些元件。 使用「可選取」表示可針對備份作業選取，並可為還原作業選取還原，開發人員應該瞭解：

-   如果由指定的寫入器管理任何元件，則要求者必須 [*明確地包含*](vssgloss-e.md) 所有其 [*元件*](vssgloss-c.md) ，而不需要在其對備份元件檔的 [*邏輯路徑*](vssgloss-l.md) 中選取祖系，然後以群組的方式備份和還原這些元件。
-   要求者可以選擇在備份和還原作業期間，將可選取的元件明確新增至備份元件檔;新增之後，必須備份或還原元件。
-   如果元件是可選取的，則元件及其所有 [*子*](vssgloss-s.md) 元件 (如邏輯路徑所定義) 形成元件集，可視為可選擇性參與備份和還原作業的單一單位。
-   要求者絕對不會明確地在備份和還原作業期間，將可選取的祖系（元件集中的子元件）新增至其備份元件檔的其元件。 如果已明確加入這些元件，則必須以 [*隱含方式包含*](/windows) 這些元件，在此情況下，必須備份或還原它們 (請參閱要求 [者) 使用元件](use-of-components-by-the-requestor.md) 。
-   具有可選取上階的可選取元件仍然是元件 () 元件集的 [*子*](vssgloss-s.md) 元件，而且如果其可選取的上階明確包含在作業中，則可能會隱含地包含該元件。 在此情況下，其資訊不會加入至備份元件檔。 如果作業中未包含可選取的上階，則可以明確選取該元件以包含在作業中，在這種情況下，它的資訊會包含在備份元件檔中。
-   如果任何可選取的上階是可選擇進行還原的，則可以明確地將包含在備份中的子元件包含在還原作業中，不論是否有任何可選取的上階狀態。 還原作業期間所包含的任何可選取的還原子元件，都必須將其資訊新增至備份元件檔。
-   在產生 [*PrepareForBackup*](vssgloss-p.md) 和 [*PreRestore*](vssgloss-p.md) 事件之前，未明確將任何元件新增至備份元件檔的寫入器，將不會收到任何進一步的 VSS 事件。

如需詳細資訊，請參閱 [使用 Selectability 和邏輯路徑](working-with-selectability-and-logical-paths.md)。

## <a name="adding-files-to-a-component"></a>將檔案新增至元件

元件包含檔案格式的檔案資訊，其中包含下列檔案的檔 [*集*](vssgloss-f.md) ：

-   元件中檔案的根目錄。
-   元件中檔案的檔案規格。
-   指出元件規格是否為遞迴的旗標。

視元件類型而定，它可以是資料庫或檔案群組，而在資料庫元件的案例中 () 是否要載入的檔案是資料或記錄檔，寫入器會呼叫 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)、 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)或 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) 來新增檔案集。

使用這些函式時，您應該指定要加入檔案集的檔案，如下所示：

-   *wszPath*：這是包含要新增至檔案集之檔案的目錄路徑。 如果 *bRecursive* 參數設定為 **true**， *wszPath* 參數會指定要以遞迴方式進行往返的目錄階層，並應重新建立所有目錄，包括空的目錄。
-   *wszFilespec*：這個字串會指定要新增至檔案集之每個目錄中的檔案。

例如，假設下列目錄結構存在：

<dl> C： \\ Directory1 \\File1.txt  
C： \\ Directory1 \\File2.txt  
C： \\ Directory1 \\ Directory2 \\File1.txt  
C： \\ Directory1 \\ Directory2 \\File2.txt  
C： \\ Directory1 \\ Directory3\\  
</dl>

如果寫入器針對 WszPath 指定 "C： \\ Directory1 **"，針對 WszFilespec 指定 "File1."，若為 bRecursive，則要求者 \* 應包含這些檔案：   

<dl> C： \\ Directory1 \\File1.txt  
C： \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

如果寫入器針對 WszPath 指定 "C： \\ Directory1" **，針對 wszFilespec 指定 ""，如果是 \* *bRecursive*，則要求者應包含這些檔案：  

<dl> C： \\ Directory1 \\File1.txt  
C： \\ Directory1 \\File2.txt  
C： \\ Directory1 \\ Directory2 \\File1.txt  
C： \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

如果寫入器針對 WszPath 指定 "C： \\ Directory1 **"，針對 wszFilespec 指定 ""，如果 bRecursive，則要求者 \* 應包含下列檔案：  

<dl> C： \\ Directory1 \\File1.txt  
C： \\ Directory1 \\File2.txt  
</dl>

在上述所有範例中，每當寫入器針對 *bRecursive* 指定 **true** 時， \\ \\ 都應該重新建立空的目錄 C： Directory1 Directory3 \\ 。

針對新增至檔案群組元件的檔案集，如果目前位於磁片上的檔案不在寫入器會考慮適當或預設位置的情況下，寫入器可以選擇新增替代路徑。 在這些情況下，檔案集的路徑定義會包含檔案的一般位置和檔案的還原位置，而替代路徑則包含要備份之檔案的目前位置。

檔案集中的所有檔案都必須在備份時存在。 要求者必須假設檔案集中所列的所有檔案都需要進行備份，而且如果遺失任何檔案，備份將會失敗。 請注意，為 \* *wszFilespec* 參數指定 "" 時，它可以比對零或多個檔案。

請注意，這類寫入器元資料檔案屬性是替代位置對應、明確包含和排除的檔案，而 restore 方法則是在寫入器層級設定，而不是在元件層級設定。  (需詳細資訊，請參閱 [使用寫入器元資料檔案](working-with-the-writer-metadata-document.md)。 ) 

## <a name="component-definition-for-backup-and-restore-operations"></a>備份和還原作業的元件定義

還原和備份作業都必須產生 [*識別事件*](vssgloss-i.md)，而針對這兩個備份和還原，則會由相同的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 方法來處理。

在備份作業期間，要求者會使用寫入器的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 方法所傳回的資訊，來判斷系統上有哪些寫入器，然後判斷要備份的檔案。

在還原作業期間，寫入器的 [**CVssWriter：： OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) 事件所傳回的資訊只會用來建立目前存在於系統上之寫入器的身分識別和狀態;不會使用在還原期間產生的檔案規格資訊。 相反地，在備份時儲存的寫入器元資料檔案會用來取得此資料。

一旦在備份作業期間產生，就會儲存寫入器元件資訊以及其餘的寫入器資訊，以支援還原作業。 要求者必須負責儲存這項資訊。

 

 
