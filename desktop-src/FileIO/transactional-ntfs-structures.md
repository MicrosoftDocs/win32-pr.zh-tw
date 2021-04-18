---
description: 交易式 NTFS (TxF) 結構。
ms.assetid: 85b3cf8e-bff3-4693-b00e-64bf5d1f5065
title: TxF 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d490f608ef9ebfa6906d1acffa374a0c9327489b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983342"
---
# <a name="txf-structures"></a>TxF 結構

交易式 NTFS (TxF) 提供下列結構。

## <a name="in-this-section"></a>本節內容



| 結構                                                                                                    | Description                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TXFS \_ 建立 \_ 迷你迷你 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_create_miniversion_info)<br/>                           | 包含 [**FSCTL \_ TXFS \_ CREATE \_ 迷你**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion)版所建立之迷你版的相關版本資訊。<br/>                                            |
| [**TXFS \_ 取得 \_ 中繼資料 \_ 資訊 \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_metadata_info_out)<br/>                              | 包含有關所建立之迷你版的版本資訊。<br/>                                                                                                                 |
| [**TXF \_ 識別碼**](/windows/desktop/api/TxfW32/ns-txfw32-txf_id)<br/>                                                                         | 代表 Resource Manager 內容中的唯一識別碼。<br/>                                                                                                              |
| [**TXFS \_ 取得 \_ 交易 \_ 版本**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version)<br/>                             | 包含指定檔案之基底和最新版本的相關資訊。<br/>                                                                                                      |
| [**TXFS \_ 列出 \_ 交易 \_ 鎖定 \_ 的檔案**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files)<br/>              | 包含由交易寫入器鎖定的檔案清單。<br/>                                                                                                                                 |
| [**TXFS \_ 列出 \_ 交易 \_ 鎖定 \_ 檔案 \_ 專案**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transaction_locked_files_entry)<br/> | 包含鎖定交易的相關資訊。<br/>                                                                                                                                        |
| [**TXFS \_ 列出 \_ 交易**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions)<br/>                                        | 包含交易清單。<br/>                                                                                                                                                        |
| [**TXFS \_ 列出 \_ 交易 \_ 專案**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_list_transactions_entry)<br/>                           | 包含交易的相關資訊。<br/>                                                                                                                                               |
| [**TXF \_ \_ 記錄檔記錄 \_ 受影響 \_ 的檔案**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_affected_file)<br/>                          | 包含受交易影響之檔案的資訊。<br/>                                                                                                                     |
| [**TXF 記錄檔 \_ \_ 記錄 \_ 基底**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_base)<br/>                                             | 包含基本記錄資訊。<br/>                                                                                                                                                  |
| [**TXF \_ \_ 記錄 \_ 截斷**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_truncate)<br/>                                     | 包含截斷作業的記錄。<br/>                                                                                                                                           |
| [**TXF \_ \_ 記錄檔記錄 \_ 寫入**](/windows/desktop/api/TxfW32/ns-txfw32-txf_log_record_write)<br/>                                           | 包含寫入作業的記錄。<br/>                                                                                                                                              |
| [**TXFS \_ 修改 \_ RM**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_modify_rm)<br/>                                                        | 包含修改次要資源管理員的記錄參數和記錄模式時所需的資訊。<br/>                                                                      |
| [**TXFS \_ 查詢 \_ RM \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_query_rm_information)<br/>                                 | 包含 resource manager (RM) 的相關資訊。<br/>                                                                                                                                   |
| [**TXFS \_ 讀取 \_ 備份 \_ 資訊 \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)<br/>                  | 包含交易式 NTFS (TxF) 特定結構。 只有在呼叫 [**TXFS \_ 寫入 \_ 備份 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)時，才應該使用這種資訊。<br/>    |
| [**TXFS 儲存 \_ 點 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)<br/>                                | [**FSCTL \_ TXFS 儲存 \_ 點 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_savepoint_information)結構會指定要執行的動作，以及在哪個交易上執行的動作。<br/>                                      |
| [**TXFS \_ 交易使用中 \_ \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_transaction_active_info)<br/>                           | 包含旗標，這個旗標會指出交易是否在使用中，或在取得快照集時不是作用中。<br/>                                                                                     |
| [**TXFS \_ 寫入 \_ 備份 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)<br/>                         | 包含交易式 NTFS (TxF) 特定結構。 只有在呼叫 [**TXFS \_ 寫入 \_ 備份 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)時，才應該使用這種資訊。<br/> |



 

 

