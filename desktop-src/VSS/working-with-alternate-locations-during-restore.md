---
description: 要求者不應該（或可能無法）將檔案從備份媒體還原至其原始位置的原因有很多。
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: 在還原期間使用替代位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907732c7b4b97668f1a317f9e03c3ea35bdec9618ff0e3e3c1a2f1e319eb19fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056146"
---
# <a name="working-with-alternate-locations-during-restore"></a>在還原期間使用替代位置

要求者不應該（或可能無法）將檔案從備份媒體還原至其原始位置的原因有很多。 例如，還原方法或目標可能需要這樣的還原，否則可能會佔用並資料流程目前的還原位置。

為了處理這類情況，寫入器可能已定義 [*替代位置對應*](vssgloss-a.md)，這是用於特殊情況的非標準還原目的地。

替代位置對應的詞彙（與 VSS 搭配使用）不應該與「 [*替代路徑*](vssgloss-a.md)」一詞混淆。 替代位置對應只會在還原作業期間使用，並參考還原作業的替代目的地。 替代路徑只會在備份作業期間使用，並參考要備份的來源替代來源。

若要在還原期間使用替代位置對應，要求者會執行下列 (通常會在產生 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) 事件) 之後：

1.  使用透過抓取預存寫入器取得的 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 介面實例，要求者會使用 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) 方法，取得寫入器的替代位置對應，作為 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 介面的實例。

    > [!Note]  
    > 要求者會使用 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)，而不是 [**>ivsscomponent：： GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)。 前者會傳回可供要求者使用的替代位置對應。 後者可用來表示要求者實際使用的替代位置對應。

     

2.  [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)的呼叫會傳回 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)介面的實例。 此實例包含檔案集資訊（由 [**IVssWMFiledesc：： GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)指定的路徑、透過 [**IVssWMFiledesc：： GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)傳回的檔案規格，以及從 [**IVssWMFiledesc：： GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)取得的遞迴旗標），以比對將使用 [**IVssCreateWriterMetadata：： AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)、 [**IVssCreateWriterMetadata：： AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)或 [**IVssCreateWriterMetadata：： AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) 所 (新增的其中一個檔集，) 為寫入器所管理的其中一個元件。

    [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)所傳回的值是此檔案集的替代位置對應。

3.  替代位置對應不包含元件資訊，因此必須比較檔案集資訊 (路徑、檔案規格和遞迴旗標，) 由呼叫 [**IVssExamineWriterMetadata：： GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) 取得寫入器元件所包含的檔案。

    您可以逐一查看寫入器的元件並呼叫 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) 來取得 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面的實例，並使用 [**IVssWMComponent：： GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) 取得包含元件檔案集資訊的 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 實例，以找到這項資訊。

    當取自 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)和 [**IVssWMComponent：： GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile)的 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)實例所傳回的檔案集合資訊符合從 IVssWMFiledesc [**：： IVssWMFiledesc**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)衍生的 **GetAlternateLocation** 實例所取得的檔案時，就會發現管理具有特定替代位置對應之檔案的元件。

4.  在找出元件之後，要求者可以藉由執行下列動作來判斷應使用替代位置對應的條件：

    -   檢查元件的還原方法，這是藉由呼叫 [**IVssExamineWriterMetadata：： GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)所取得。
    -   藉由呼叫 [**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)，檢查還原目標是否覆寫還原方法。

        如果在寫入器元資料檔案中找到的元件已 [*明確包含*](vssgloss-e.md) 在備份中， [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 介面的實例將會對應至該元件。 如果元件已 [*隱含地包含*](vssgloss-i.md) 在備份中，則 **>ivsscomponent** 的實例會對應至定義元件集的元件，而寫入器元資料檔案中的元件是子元件。

5.  有了這項資訊，如果需要將指定元件的指定檔案集還原至替代位置對應所定義的目的地，則要求者可以依元件逐一決定。

6.  使用替代位置對應時，要求者會遵循檔案集的檔案描述元和遞迴旗標，並使用替代位置對應所提供的路徑。

    要求者表示在還原作業期間使用替代位置對應，方法是呼叫 [**>ivssbackupcomponents：： AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) ，並使用檔案集的預設位置資訊、使用的替代還原目的地，以及元件名稱。

    如果檔案集是由已明確包含在備份中的元件所管理，則會使用該元件名稱。 如果檔案集是由已隱含包含在備份中的元件所管理，則使用的名稱將會是元件的元件，該元件會定義管理檔案集的元件是子元件的元件集。

寫入器會藉由呼叫 [**>ivsscomponent：： GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)，確認其中一個元件的檔案集是否已還原至替代位置對應。

 

 



