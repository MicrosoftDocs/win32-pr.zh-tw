---
title: 磁帶輸入和輸出
description: 有幾個函數可讓應用程式用來在磁帶機上 (i/o) 執行輸入和輸出。 磁帶 i/o 類似于在通訊裝置上執行的 i/o。
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- 磁帶輸入和輸出備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281eb6104cb71fbd5e7f0b3d9072cefe562ac7b9cc54e05ede53bece8755178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021267"
---
# <a name="tape-input-and-output"></a>磁帶輸入和輸出

有幾個函數可讓應用程式用來在磁帶機上 (i/o) 執行輸入和輸出。 磁帶 i/o 類似于在通訊裝置上執行的 i/o。

執行磁帶 i/o 時，有些磁帶機會將磁帶固件資訊儲存在磁帶上的前幾個區塊中，通常會使用第一個100區塊的部分。 應用程式不應該使用這些區塊。 您可以從個別的磁帶系統製造商取得此主題的更具體資訊。 一般情況下，略過磁帶上第一個100區塊的應用程式會避免磁帶機的特性。

[**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)和 [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition)函式會取出目前的磁帶位置並進行移動。 [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark)函式會寫入指定數目的 setmarks、格式標記、簡短的標記和長的標記。 [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape)函式會清除所有或部分的磁帶。

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)函式會從磁帶讀取和寫入檔案資料。 資料是以完整區塊讀取和寫入。 如果磁帶的區塊大小為512個位元組，則所有讀取和寫入作業都必須使用屬於該區塊大小之簡單整數倍數的緩衝區：512、1024、1536、2048等等。 大部分（如果不是全部），磁片磁碟機只允許在磁帶倒轉或讀取作業產生資料結束錯誤訊息之後，進行寫入操作。

若要在可變長度的區塊模式中，讀取或寫入磁帶的檔案資料，請執行下列步驟：

1.  藉由呼叫 [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)函式，並檢查 \_ \_ \_ 所傳回 [**磁帶 \_ 取得 \_ 磁片磁碟機 \_ 參數**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters)結構之 **FeaturesLow** 成員的磁帶機變數區塊位，判斷磁帶機是否支援可變長度的封鎖模式。
2.  藉由呼叫 [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)函式，將 [**磁帶 \_ 組 \_ 媒體 \_ 參數**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters)結構的 **區塊** 成員設定為零，以指定變數區塊大小模式。 然後，使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 或 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 來讀取或寫入檔案資料。

如果 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 遇到標記標記，就會讀取到標記最多的資料，且函式會失敗。  ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤碼，指出所遇到的標記類型。 ) 作業系統會將磁帶移出標記後，應用程式可以再次呼叫 **ReadFile** 以繼續讀取。

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 只會讀取和寫入資料流程。 [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)和 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)函式會讀取和寫入與檔案相關聯的所有資料流程。 這些包括資料、擴充屬性、安全性和替代資料流程。 安全性和替代資料流程只與 NTFS 檔案系統磁碟分割相關。

[**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek)函式會向前搜尋 [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread)或 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)一開始所存取的檔案。 此函式可讓應用程式略過導致存取錯誤的資訊。

如果應用程式只需要存取檔案資料，則應該使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)。 如果資料流程是使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數所建立，則這些函式也可以讀取替代資料流程。

磁帶備份應用程式必須使用 [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) 和 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) 來複製與檔案相關的所有資訊。 不過，這些函式不會讀取或寫入檔案特性，例如屬性、檔案建立時間等等。 應用程式必須使用檔案輸入和輸出函式（例如 [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) 和 [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa)）來取得和設定這些值。

 

 