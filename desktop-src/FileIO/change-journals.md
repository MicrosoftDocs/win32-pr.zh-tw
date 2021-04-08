---
description: 對磁片區中的檔案或目錄進行任何變更時，該磁片區的 USN 變更日誌會以變更的描述和檔案或目錄的名稱進行更新。
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: 變更日誌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5052ec87830a822270071a6ee00f1c3f7cffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852139"
---
# <a name="change-journals"></a>變更日誌

自動備份應用程式是程式的其中一個範例，必須檢查磁片區狀態的變更，以執行其工作。 檢查目錄或檔案中之變更的暴力密碼破解方法是掃描整個磁片區。 不過，這通常不是可行的方法，因為系統效能會降低。 另一種方法是讓應用程式藉由呼叫 [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) 或 [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) 函式來註冊目錄通知 (，) 以備份目錄。 這比第一個方法更有效率，不過，它需要應用程式隨時執行。 此外，如果必須備份大量的目錄和檔案，則這類應用程式的處理和記憶體額外負荷可能也會導致作業系統的效能降低。

為了避免這些缺點，NTFS 檔案系統會維持更新序號 (USN) 變更日誌。 對磁片區中的檔案或目錄進行任何變更時，該磁片區的 USN 變更日誌會以變更的描述和檔案或目錄的名稱進行更新。

您也需要變更日誌來復原檔案系統索引，例如在電腦或磁片區失敗之後。 復原索引的能力，是指檔案系統可避免在這種情況下重新編制整個磁片區的耗時處理常式。

下列主題討論變更日誌。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                             | 描述                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [變更日誌記錄](change-journal-records.md)<br/>                                                                   | 新增、刪除和修改檔案、目錄和其他 NTFS 檔案系統物件時，NTFS 檔案系統會在資料流程中輸入變更日誌記錄，電腦上的每個磁片區都會有一個記錄。<br/>                                           |
| [使用變更日誌識別碼](using-the-change-journal-identifier.md)<br/>                                         | NTFS 檔案系統會將不帶正負號的64位識別碼與每個變更日誌產生關聯。<br/>                                                                                                                                                   |
| [建立、修改和刪除變更日誌](creating-modifying-and-deleting-a-change-journal.md)<br/>             | 系統管理員可以建立、刪除及重新建立變更日誌。<br/>                                                                                                                                                                         |
| [取得變更日誌作業的磁片區控制碼](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | 若要取得磁片區的控制碼以用於更新序號 (USN) 變更日誌作業，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式，並將 *lpFileName* 參數設定為下列格式的字串： \\ \\ 。 \\*X*。<br/> |
| [變更日誌作業](change-journal-operations.md)<br/>                                                             | 控制與 NTFS 檔案系統更新序號搭配使用的代碼和結構 (USN) 變更日誌。<br/>                                                                                                                                |



 

 

 




