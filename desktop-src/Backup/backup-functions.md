---
title: 備份功能
description: 下列函式會搭配磁帶備份使用。
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2164958d7261c4c22caf1ac5124f524eca2f7ed355b082bede59d66a2e6fe697
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529608"
---
# <a name="backup-functions"></a>備份功能

下列函式會搭配 [磁帶備份](tape-backup.md)使用。



| 函式                                           | 描述                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | 將與指定檔案或目錄相關聯的資料讀入緩衝區。                                |
| [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | 在資料流程中向前搜尋。                                                                        |
| [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | 從緩衝區將資料串流寫入至指定的檔案或目錄。                                |
| [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | 重新格式化磁帶。                                                                                      |
| [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | 清除所有或部分磁帶。                                                                          |
| [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | 抓取描述磁帶或磁帶機的資訊。                                       |
| [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | 抓取磁帶的目前位址。                                                             |
| [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | 判斷磁帶裝置是否已準備好處理磁帶命令。                                  |
| [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | 準備要存取或移除的磁帶。                                                           |
| [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | 指定磁帶的區塊大小或設定磁帶裝置。                                      |
| [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | 設定指定裝置上的磁帶位置。                                                        |
| [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | 將指定數目的格式標記、setmarks、短格式標記或長標記寫入磁帶裝置。 |



 

下列函式是針對使用 [單一實例存放區和 SIS 備份](single-instance-store-and-sis-backup.md)所提供的功能。



| 函式                                                          | 描述                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**SisCreateBackupStructure**](siscreatebackupstructure.md)      | 根據提供的資訊建立指定的 SIS 備份結構。                      |
| [**SisCreateRestoreStructure**](siscreaterestorestructure.md)    | 根據提供的資訊建立指定的 SIS 還原結構。                     |
| [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)    | 傳回描述指定 SIS 連結指向之通用存放區檔案的資訊。            |
| [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)          | 釋出 SIS API 函數所配置的記憶體。                                                       |
| [**SisFreeBackupStructure**](sisfreebackupstructure.md)          | 釋出指定的 SIS 備份結構。                                                          |
| [**SisFreeRestoreStructure**](sisfreerestorestructure.md)        | 釋出指定的 SIS 還原結構。                                                         |
| [**SisRestoredCommon StoreFile**](sisrestoredcommonstorefile.md) | 報告已寫入一般存放區檔案的 SIS 架構。                         |
| [**SisRestoredLink**](sisrestoredlink.md)                        | 傳回指定的已還原 SIS 連結所指向的通用存放區檔案或檔案的名稱。 |



 

以下是針對加密檔案的 [備份和還原](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)所提供的功能。



| 函式                                                | 描述                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CloseEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | 關閉以 [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)開啟的加密檔案。 |
| [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | 開啟加密的檔案，並存取加密格式的資料。                            |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | 讀取加密的檔案，以加密格式保留其資料。                               |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | 撰寫加密的檔案，以加密格式保留其資料。                              |



 

 

 