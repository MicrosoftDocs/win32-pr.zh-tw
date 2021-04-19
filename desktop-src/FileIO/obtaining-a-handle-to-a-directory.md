---
description: 只要進程建立或開啟目錄物件，它就會收到物件的控制碼。
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: 目錄控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987821"
---
# <a name="directory-handles"></a>目錄控制碼

只要進程建立或開啟目錄物件，它就會收到物件的控制碼。

若要取得現有目錄的控制碼，請使用檔案 **\_ 旗標 \_ 備份 \_ 語義** 旗標來呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函數。

您可以將目錄控制碼傳遞給下列函式。



| 函式                                                         | 描述                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)                              | 備份檔案或目錄，包括安全性資訊。<br/>                                                                                      |
| [**BackupSeek**](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | 在一開始使用 [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) 或 [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) 函數來存取資料流程時，向前搜尋。<br/> |
| [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | 還原使用 [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread)備份的檔案或目錄。<br/>                                                             |
| [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | 抓取指定檔案的檔案資訊。<br/>                                                                                                    |
| [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | 捕獲指定檔案的大小（以位元組為單位）。<br/>                                                                                                   |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | 抓取檔案或目錄的建立日期和時間、上次存取的時間，以及上次修改的日期和時間。<br/>                                                   |
| [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | 抓取指定之檔案的檔案類型。<br/>                                                                                                        |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | 抓取描述指定目錄內變更的資訊。<br/>                                                                      |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | 設定指定檔案或目錄的建立日期和時間、上次存取時間或上次修改時間。<br/>                                             |



 

 

