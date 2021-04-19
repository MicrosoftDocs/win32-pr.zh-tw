---
description: 控制與 NTFS 檔案系統更新序號搭配使用的代碼和結構 (USN) 變更日誌。
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: 變更日誌作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988992"
---
# <a name="change-journal-operations"></a>變更日誌作業

下列清單會識別使用 NTFS 檔案系統更新序號的控制程式代碼 (USN) 變更日誌。

-   [**FSCTL \_ 建立 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [**FSCTL \_ 刪除 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [**FSCTL \_ 列舉 \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [**FSCTL \_ MARK \_ 把手**](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [**FSCTL \_ 查詢 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [**FSCTL \_ 讀取 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

下列清單會識別與 NTFS 檔案系統 USN 變更日誌相關的結構資訊。

-   [**建立 \_ USN \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [**刪除 \_ USN \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [**標記 \_ 控點 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [**MFT \_ 列舉 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [**讀取 \_ USN \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [**USN \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [**USN \_ 記錄**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
