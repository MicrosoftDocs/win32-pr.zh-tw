---
description: 磁片區是由稱為磁片區管理員的設備磁碟機所執行。
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: 關於磁片區管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994514"
---
# <a name="about-volume-management"></a>關於磁片區管理

磁片區是由稱為磁片區管理員的設備磁碟機所執行。 範例包括 FtDisk Manager、邏輯磁片管理員 (LDM) ，以及 VERITAS Logical Volume Manager (LVM) 。 磁片區管理員提供一層實體抽象化、資料保護 (使用某種形式的 RAID) 和效能。

## <a name="in-this-section"></a>本節內容



| 主題                                                                       | 描述                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [檔案系統識別](file-system-recognition.md)<br/>           | 檔案系統辨識的目標是要讓 Windows 作業系統擁有一個額外的選項，以供有效但無法辨識的檔案系統（非「原始」）使用。<br/>                                                                                                         |
| [命名磁片區](naming-a-volume.md)<br/>                           | 標籤是指派給磁片區（通常是由使用者使用）的易記名稱，可讓您更容易辨識。 磁片區可以有標籤、磁碟機號、兩者或兩者皆有。 若要設定磁片區的標籤，請使用 [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) 函數。<br/> |
| [列舉磁片區](enumerating-volumes.md)<br/>                   | 若要在電腦上建立磁片區的完整清單，或輪流操作每個磁片區，您可以列舉磁片區。<br/>                                                                                                                                                       |
| [取得磁片區資訊](obtaining-volume-information.md)<br/> | 存取指定磁片區上的檔案和目錄之前，您應該使用 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式來判斷檔案系統的功能。<br/>                                                                              |
| [變更日誌](change-journals.md)<br/>                           | 對磁片區中的檔案或目錄進行任何變更時，該磁片區的 USN 變更日誌會以變更的描述和檔案或目錄的名稱進行更新。<br/>                                                                                        |
| [裝載的資料夾](volume-mount-points.md)<br/>                       | 您可以使用掛接的資料夾，將不同的檔案系統（例如 NTFS 檔案系統、16位 FAT 檔案系統，以及在 CD-ROM 光碟機上的 ISO-9660 檔案系統）統一成單一 NTFS 磁片區上的一個邏輯檔案系統。<br/>                                                      |
| [主檔案資料表](master-file-table.md)<br/>                       | 檔案的所有相關資訊，包括其大小、時間和日期戳記、許可權和資料內容，都會儲存在主要檔案資料表中 (MFT) 專案，或儲存在 mft 專案所描述之 MFT 以外的空間中。<br/>                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本磁碟和磁片區技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[動態磁碟與磁片區技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[磁片區管理參考](volume-management-reference.md)
</dt> </dl>

 

