---
description: 交易式 NTFS (TxF) 控制代碼。
ms.assetid: b66d322a-a971-4219-bb5b-dc69b10b2581
title: TxF 控制項碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe432444c7abcc9e31c00a68847f92b177de22a6fbb33dc1b02ad22a732a14ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047858"
---
# <a name="txf-control-codes"></a>TxF 控制項碼

\[Microsoft 強烈建議開發人員利用替代方法來達成您的應用程式需求。 針對 TxF 開發的許多案例，都可以透過更簡單且更容易使用的技術來達成。 此外，Microsoft Windows 的未來版本可能不提供 TxF。 如需詳細資訊以及 TxF 的替代方案，請參閱 [使用交易式 NTFS 的替代方案](deprecation-of-txf.md)。\]

交易式 NTFS (TxF) 提供下列控制項碼。

## <a name="in-this-section"></a>本節內容



| 控制程式代碼                                                                                                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ TXFS \_ 建立 \_ 迷你**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_create_miniversion)<br/>                         | 為指定的檔案建立新的 [迷你版本](glossary.md) 。 <br/> Miniversions 可讓您在交易期間參考檔案的快照集。 認可或回復交易時，將會捨棄 Miniversions。<br/>                                                                                                                                                                      |
| [**FSCTL \_ TXFS \_ 取得 \_ 中繼資料 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_get_metadata_info)<br/>                          | 抓取交易的 NTFS (TxF) 檔案的中繼資料，以及已鎖定所指定檔案之交易的 **GUID** (如果檔案已鎖定) 。 <br/>                                                                                                                                                                                                                                                                         |
| [**FSCTL \_ TXFS \_ 取得 \_ 交易 \_ 版本**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_get_transacted_version)<br/>                | 傳回 [**TXFS \_ 取得 \_ 交易 \_ 版本**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_get_transacted_version) 結構。 結構會識別指定檔案的最新認可版本，也就是控制碼的版本號碼。 <br/>                                                                                                                                                                                                            |
| [**FSCTL \_ TXFS \_ 列出 \_ 交易 \_ 鎖定 \_ 的檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_list_transaction_locked_files)<br/> | 傳回指定之交易目前鎖定的所有檔案清單。 如果傳回值是 **錯誤的 \_ \_ 資料**，它會傳回在此呼叫時保存完整檔案清單所需的緩衝區長度。<br/>                                                                                                                                                                                           |
| [**FSCTL \_ TXFS \_ 列出 \_ 交易**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_list_transactions)<br/>                           | 傳回目前所指定資源管理員所牽涉的所有交易清單。<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**FSCTL \_ TXFS \_ 修改 \_ RM**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_modify_rm)<br/>                                           | 設定次要資源管理員 (RM) 的記錄模式和記錄參數資訊。<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**FSCTL \_ TXFS \_ 查詢 \_ RM \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_query_rm_information)<br/>                    | 取得資源管理員 (RM) 的資訊。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**FSCTL \_ TXFS \_ 讀取 \_ 備份 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_read_backup_information)<br/>              | 傳回交易式 NTFS (TxF) 指定之檔案的特定資訊。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**FSCTL \_ TXFS 儲存 \_ 點 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_savepoint_information)<br/>                   | [**FSCTL \_ TXFS 儲存 \_ 點 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_savepoint_information)控制程式代碼可控制設定、清除和回復至指定的儲存點。<br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/>                                                                                                                 |
| [**FSCTL \_ TXFS \_ 交易使用中 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_transaction_active)<br/>                         | 傳回布林值，這個值會指出建立快照集時，關聯的磁片區上是否有任何作用中的交易。 此呼叫只對唯讀快照集磁片區有效。<br/>                                                                                                                                                                                                                                   |
| [**FSCTL \_ TXFS \_ 寫入 \_ 備份 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_write_backup_information)<br/>            | 將交易式 NTFS (TxF) 特定資訊寫入至指定的檔案。 [**TXFS \_ 寫入 \_ 備份 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_write_backup_information)結構的 **緩衝區** 成員必須是 [**FSCTL \_ TXFS \_ 讀取 \_ 備份 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_txfs_read_backup_information)所傳回之 [**TXFS \_ read \_ backup \_ information \_ OUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-txfs_read_backup_information_out)結構的 **緩衝區** 成員。<br/> |



 

 

