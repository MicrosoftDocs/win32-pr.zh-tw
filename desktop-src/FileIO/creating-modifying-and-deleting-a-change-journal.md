---
description: 系統管理員可以建立、刪除及重新建立變更日誌。
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: 建立、修改和刪除變更日誌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c8cf7296f93549e7d9ec05f5d614131cc342ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978319"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>建立、修改和刪除變更日誌

系統管理員可以建立、刪除及重新建立變更日誌。 當目前的更新序號 (USN) 值接近最大可能 USN 值（由 [**usn \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)結構的 **MaxUsn** 成員表示）時，系統管理員應該刪除日誌。 系統管理員也可以刪除並重新建立變更日誌來回收磁碟空間。 若要執行這個程式和所有其他非程式設計的變更日誌作業，您必須擁有系統管理員許可權。 也就是說，您必須是 Administrators 群組的成員。

若要以程式設計方式建立或修改指定磁片區上的變更日誌，請使用 [**FSCTL \_ 建立 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) 控制項程式碼。

當您建立新的變更日誌或修改現有的變更日誌時，NTFS 檔案系統會從 [**建立 \_ usn \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) 結構中的資訊設定該變更日誌的資訊， [**FSCTL \_ 建立的 \_ usn \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) 會將其視為輸入。 **建立 \_USN \_ 日誌 \_ 資料** 具有 **MaximumSize** 和 **AllocationDelta** 的成員。

**MaximumSize** 是變更日誌的目標最大大小（以位元組為單位）。 變更日誌的成長超過此值，但在 NTFS 檔案系統檢查點，NTFS 檔案系統會檢查日誌，並在其大小超過 **MaximumSize** 的值加上 **AllocationDelta** 的值時加以修剪。  (在 NTFS 檔案系統檢查點上，作業系統會將記錄寫入 NTFS 檔案系統記錄檔，以允許 NTFS 檔案系統判斷從失敗復原所需的處理。 ) 

**AllocationDelta** 是在每次配置或解除配置記憶體時，新增至結尾並從變更日誌的開頭移除的位元組數目。 換句話說，配置和解除配置會以此大小的單位來進行。 叢集大小的整數倍數是此成員的合理值。

如果系統管理員將現有的變更日誌修改為具有較大的 **MaximumSize** 值（例如，如果磁片區太頻繁地重新編制索引），變更日誌只會收到新的專案，直到超過新的大小上限為止。

若要刪除變更日誌，請使用 [**FSCTL \_ delete \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) 控制項程式碼。 當您使用這項作業時，它會逐步解說磁片區上的所有檔案，並將每個檔案的 USN 重設為零。 作業接著會刪除現有的變更日誌。 此作業會在系統重新開機後持續，直到完成為止。 在此程式期間嘗試讀取、建立或修改變更日誌的任何嘗試都會失敗，並 **刪除錯誤碼 \_ 錯誤 \_ 日誌 \_ \_**。

您也可以使用 [**FSCTL \_ DELETE \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) 控制項程式碼，判斷是否有其他進程啟動的刪除作業正在進行中。 例如，當您的應用程式啟動時，可以判斷刪除是否正在進行中。 因為日誌刪除會在系統重新開機時持續保存，所以在系統重新開機時啟動的服務和應用程式應該會檢查是否正在進行刪除。

在啟動時，不一定會建立變更日誌。 若要建立變更日誌，系統管理員可以明確地進行，或啟動另一個需要變更日誌的服務。

 

 
