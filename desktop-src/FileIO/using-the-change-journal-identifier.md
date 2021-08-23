---
description: NTFS 檔案系統會將不帶正負號的64位識別碼與每個變更日誌產生關聯。
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: 使用變更日誌識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483c171b69bcee0faf8df9f325d4ee8ffcb6e904f6aa0cd3c720b83df326e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015066"
---
# <a name="using-the-change-journal-identifier"></a>使用變更日誌識別碼

NTFS 檔案系統會將不帶正負號的64位識別碼與每個變更日誌產生關聯。 建立時，會使用此識別碼來標記日誌。 檔案系統會使用新的識別碼來標記日誌，其中現有的更新序號 (USN) 記錄是或可能無法使用。

例如，當磁片區從某個 NTFS 版本移至另一個版本時，NTFS 檔案系統會以新的識別碼 restamps 變更日誌。 這類移動可能會在雙重開機環境中發生，或在使用卸載式媒體時進行。

若要取得指定磁片區上目前變更日誌的識別碼，請使用 [**FSCTL \_ QUERY \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) 控制項程式碼。 若要執行此作業和所有其他變更日誌作業，您必須擁有系統管理員許可權。 也就是說，您必須是 Administrators 群組的成員。

當系統管理員刪除並重新建立變更日誌時（例如，當目前的 USN 值接近最大可能的 USN 值）時，USN 值會從零開始。 當 NTFS 檔案系統使用新的識別碼來標記日誌，而不是重新建立日誌時，它不會將 USN 重設為零，但會從目前的 USN 繼續。 無論是哪一種情況，所有現有的 Usn 都小於未來的 Usn。

當您需要一組特定記錄的資訊時，請使用 [**FSCTL \_ 查詢 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) 控制程式代碼來取得變更日誌識別碼。 然後使用 [**FSCTL \_ 讀取 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) 控制程式代碼來讀取感興趣的日誌記錄。 NTFS 檔案系統只會傳回識別碼所指定之日誌的有效記錄。

您的應用程式需要記錄的 Usn 和識別碼來讀取日誌。 如果您的應用程式應該忽略檔案中的現有記錄，且記錄是針對相同磁片區在日誌的先前實例中寫入，則這項需求會提供完整性檢查。

若要取得您感興趣的記錄，您必須從最舊的記錄開始 (也就是最低的 USN) 並向前掃描，直到您找到感興趣的第一筆記錄為止。

 

 
