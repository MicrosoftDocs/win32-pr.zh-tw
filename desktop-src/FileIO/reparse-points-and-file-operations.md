---
description: 描述重新剖析點如何啟用從大部分 Windows 開發人員預期的行為離開的檔案系統行為。
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: 重新分析點和檔案作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d18b42c2bc51617e185c2d8f13fde15952ad83d2c2c635d312d589677ee8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015176"
---
# <a name="reparse-points-and-file-operations"></a>重新分析點和檔案作業

重新 *分析點* 可讓您從大部分 Windows 開發人員可能習慣的行為離開檔案系統行為，因此，在撰寫操作檔案的應用程式時，若要存取支援重新分析點的檔案系統，就必須知道這些行為是非常重要的。 這些考慮的範圍取決於特定的重新分析點（可供使用者定義）的特定執行和相關檔案系統篩選器行為。 如需詳細資訊，請參閱重新 [分析點](reparse-points.md)。

請考慮下列有關 NTFS 重新分析點執行的範例，其中包括掛接的資料夾、連結的檔案，以及 Microsoft 遠端儲存體伺服器：

-   使用檔案 [資料流程](file-streams.md)的備份應用程式應該在使用重新分析點來備份檔案時，指定 [**WIN32 \_ 資料流程 \_ 識別碼**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id)結構中的 **備份重新 \_ 分析 \_ 資料**。
-   使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式的應用程式應該在開啟檔案時，指定檔案 **旗標開啟重新 \_ \_ \_ 分析 \_ 點** 旗標（如果它是重新分析點）。 如需詳細資訊，請參閱 [建立及開啟](creating-and-opening-files.md)檔案。
-   重新 [整理](defragmenting-files.md) 檔案的程式需要對重新剖析點進行特殊處理。
-   病毒偵測應用程式應該搜尋指出連結檔案的重新分析點。
-   大部分的應用程式都應該針對已移至長期儲存的檔案採取特殊動作，如果只是通知使用者可能需要一段時間才能取出檔案。
-   [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid)函式會根據檔案 **旗標開啟重新 \_ \_ \_ 分析 \_ 點** 旗標的使用，開啟檔案或重新分析點。
-   符號連結（作為重新分析點）有特定的程式 [設計考慮](symbolic-link-programming-considerations.md) 。
-   讀取更新序號的磁片區管理活動 (USN) 變更日誌記錄在使用 [**USN \_ 記錄**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 和 [**讀取 \_ usn \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) 結構時，需要重新剖析點的特殊處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[判斷目錄是否為裝載的資料夾](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[建立載入的資料夾](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[檔案系統函數的符號連結效果](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
