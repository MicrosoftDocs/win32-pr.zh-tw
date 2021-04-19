---
description: 在某些情況下，要備份的檔案不是這些檔案的預設位置。
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: 在備份期間使用替代路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98e93af4d12b804032a64841542e731ff77e048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973470"
---
# <a name="working-with-alternate-paths-during-backup"></a>在備份期間使用替代路徑

在某些情況下，要備份的檔案不是這些檔案的預設位置。

例如，有些寫入器無法保證在 [*凍結*](vssgloss-f.md) 和 [*解除*](vssgloss-t.md) 凍結事件之間的時間範圍內，將其資料排清。 這類寫入器可能會選擇在非預設的來原始目錄或 [*替代路徑*](vssgloss-a.md)中，產生包含最後一次已知正確設定的重複檔案。

與 VSS 搭配使用的「替代路徑」詞彙不應該與「 [*替代位置對應*](vssgloss-a.md)」這一詞混淆。 替代路徑只會在備份作業期間使用，並參考要備份的來源替代來源。 替代位置對應只會在還原作業期間使用，並參考還原作業的替代目的地。

**在備份期間使用替代路徑**

1.  在備份作業的探索階段 (請參閱 [備份探索階段的總覽](overview-of-the-backup-discovery-phase.md)) 要求者會使用 [**IVssExamineWriterMetadata：： GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) 檢查每個寫入器的元件資料，並取得 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) 介面的實例。
2.  然後，要求者會藉由呼叫 [**IVssWMComponent：： GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile)方法，取得每個元件所管理的檔案 [*集*](vssgloss-f.md)（由 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)介面的實例表示）。
3.  除了路徑 ([**IVssWMFiledesc：： GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)) 、檔案規格 ([**IVssWMFiledesc：： GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) ，以及 ([**IVssWMFiledesc：： GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) 的遞迴旗標， [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) 物件可能會包含替代的位置 (做為備份作業的替代路徑，而使用 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 方法) 還原作業的替代位置對應。
4.  如果 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 所傳回的值為非 Null，則備份應用程式會使用該值，而不是從 [**IVssWMFiledesc：： GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) 取得的值，以選取並尋找要備份的檔案。
5.  儘管使用替代路徑，要求者仍應遵守 [**IVssWMFiledesc：： GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) 和 [**IVssWMFiledesc：： GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)所傳回的檔案規格和遞迴設定。

請注意，在還原時，不會在還原期間使用任何替代路徑，也就是 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) 實例所傳回的替代位置，而此實例是從 [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)的實例取得，而後者則是從取得已儲存的寫入器元資料檔案的 [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) 實例取得。

相同 [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)實例之 [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)方法所傳回的預設路徑 () 用來定義還原位置，或使用 [**IVssWMFiledesc：： GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)方法找到的替代位置對應，表示要還原檔案的位置 (請參閱 [還原期間使用替代位置](working-with-alternate-locations-during-restore.md)) 。

 

 



