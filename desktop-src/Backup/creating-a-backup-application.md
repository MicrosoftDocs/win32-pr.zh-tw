---
title: 建立備份應用程式
description: 若要在磁帶上執行輸入或輸出，備份應用程式必須先取得磁帶裝置的控制碼。 下列程式碼範例說明如何使用 CreateFile 函式來開啟磁帶裝置。
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- 備份應用程式備份
- 建立備份應用程式備份
- 備份備份，建立應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023846"
---
# <a name="creating-a-backup-application"></a>建立備份應用程式

若要在磁帶上執行輸入或輸出，備份應用程式必須先取得磁帶裝置的控制碼。 下列程式碼範例說明如何使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟磁帶裝置。


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



若要將目錄樹狀目錄備份到磁帶，應用程式必須使用 [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) 和 [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) 函式來跨越目錄樹狀目錄。 每次找到檔案時，應用程式都應該使用 [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) 函式來取得檔案屬性。

如果有永久連結，應用程式應該決定連結數目，並將檔案的唯一識別碼儲存在資料表中，以供日後比較。 第一次找到檔案時，應用程式應該使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 來開啟檔案，並使用 [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) 函式來開始備份。 然後，它可以重複使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式，將 **BackupRead** 所使用的緩衝區中的所有資訊傳送至磁帶。 第二次發現檔案時 (在) 有永久連結時，根據檔案識別碼的表格進行檢查，應用程式可以將一般檔案資訊寫入磁帶，然後再以具有 **備份 \_ 連結** 識別碼的資料流程來寫入。

從磁帶還原檔案到磁片時，應用程式必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)和 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 功能。 針對磁帶上的每個檔案，應用程式應該使用 **CreateFile** 在磁片上建立新的檔案，並使用 **BackupWrite** 來開始還原檔案。 然後，應用程式應該重複使用 **ReadFile** ，直到檔案的所有資訊都從磁帶讀取到由 **BackupWrite** 填滿的緩衝區為止。

如果 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) 緩衝區中的其中一個資料流程有 **備份 \_ 連結** 資料流程識別碼，應用程式必須建立永久連結。 如果建立連結所需的資料不存在， **BackupWrite** 就會失敗。 應用程式可以使用預先存在的目錄來找出並還原原始資料，也可以通知使用者要還原的檔案資料位於不同的位置。

 

 