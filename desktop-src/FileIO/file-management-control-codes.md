---
description: 控制檔案管理中使用的代碼。
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: 檔案管理控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02cc18cb775aa56ade9a417ee22388353b34821d5747abdfd9bc18db958034e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997289"
---
# <a name="file-management-control-codes"></a>檔案管理控制碼

下列控制碼用於檔案管理。

## <a name="in-this-section"></a>本節內容



| 控制程式代碼                                                                                    | 描述                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ 允許 \_ 擴充的 \_ DASD \_ IO**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | 通知檔案系統驅動程式不要針對分割區讀取或寫入呼叫執行任何 i/o 界限檢查。<br/>                                                                                  |
| [**FSCTL \_ 建立 \_ 或 \_ 取得 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | 抓取指定檔案或目錄的物件識別碼。 如果沒有物件識別碼，使用 **FSCTL \_ CREATE \_ 或 \_ GET \_ 物件 \_ ID 就** 會建立一個。<br/>                           |
| [**FSCTL \_ CSV \_ 控制項**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | 抓取 CSV 控制項操作的結果。<br/>                                                                                                                                        |
| [**FSCTL \_ 刪除 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | 從指定的檔案或目錄中移除物件識別碼。<br/>                                                                                                                        |
| [**\_將重複 \_ 的範圍 FSCTL \_ 至 \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | 指示檔案系統代表應用程式複製某範圍的檔案位元組。<br/>                                                                                                     |
| [**FSCTL \_ 檔案 \_ 層級 \_ 修剪**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | 向儲存系統表示不需要儲存檔案中的範圍。<br/>                                                                                                    |
| [**FSCTL \_ FILESYSTEM \_ GET \_ STATISTICS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | 從各種檔案系統效能計數器抓取資訊。<br/>                                                                                                                 |
| [**FSCTL \_ FILESYSTEM \_ GET \_ 統計資料， \_ 例如**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | 從各種檔案系統效能計數器抓取資訊。<br/> 此控制項程式碼的支援已從 Windows 10 開始。<br/>                                               |
| [**FSCTL \_ \_ \_ 依 SID 尋找 \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | 在目錄中搜尋其建立者擁有者符合指定 SID 的檔案。<br/>                                                                                                           |
| [**FSCTL \_ 取得 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | 在檔案系統支援每個資料流程壓縮的磁片區上，抓取檔案或目錄的目前壓縮狀態。<br/>                                                            |
| [**FSCTL \_ 取得 \_ NTFS \_ 檔案 \_ 記錄**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | 抓取正在使用中的第一個檔案記錄，以及所要求檔案參考編號的小於或等於序數值。<br/>                                                    |
| [**FSCTL \_ 取得 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | 抓取指定檔案或目錄的物件識別碼。<br/>                                                                                                                     |
| [**FSCTL \_ 取得 \_ 修復**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | 抓取 NTFS 檔案系統自我修復機制的相關資訊。<br/>                                                                                                               |
| [**FSCTL \_ 起始 \_ 修復**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | 觸發 NTFS 檔案系統，以在單一檔案上啟動自我修復週期。<br/>                                                                                                            |
| [**FSCTL \_ 讓 \_ 媒體 \_ 相容**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | 在一次性寫入媒體上關閉開啟的 UDF 會話，以使媒體 ROM 相容。<br/>                                                                                                         |
| [**FSCTL \_ OPBATCH \_ ACK \_ 關閉 \_ 擱置中**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | 通知伺服器用戶端應用程式已準備好關閉檔案。<br/>                                                                                                                    |
| [**FSCTL \_ OPLOCK \_ 中斷 \_ ACK \_ 無 \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | 回應檔案的隨機鎖定即將中斷的通知。 您可以使用此作業來解除鎖定檔案上的所有隨機鎖定，但讓檔案保持開啟。<br/>            |
| [**FSCTL \_ OPLOCK \_ BREAK \_ 確認**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | 回應對檔案進行獨佔式隨機鎖定即將中斷的通知。 您可以使用此作業來指出檔案應會收到層級2的隨機鎖定。<br/> |
| [**FSCTL \_ OPLOCK \_ 中斷 \_ 通知**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | 讓呼叫的應用程式等候隨機鎖定中斷的完成。<br/>                                                                                                   |
| [**FSCTL \_ 查詢配置的 \_ \_ 範圍**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | 掃描檔案或替代資料流程，以尋找可能包含非零資料的範圍。<br/>                                                                                                       |
| [**\_磁片區 \_ \_ \_ \_ 資訊上的 FSCTL 查詢**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | 要求 UDF 特定的磁片區資訊。<br/>                                                                                                                                                |
| [**FSCTL \_ 查詢的 \_ 備用 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | 抓取磁片區的瑕疵管理屬性。 用於 UDF 檔案系統。<br/>                                                                                                     |
| [**FSCTL \_ 召回 \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | 從遠端儲存體管理的存放裝置媒體重新叫用檔案，也就是階層式存放裝置管理軟體。<br/>                                                                    |
| [**FSCTL \_ 要求 \_ 批次 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | 要求批次檔的批次隨機鎖定。<br/>                                                                                                                                           |
| [**FSCTL \_ 要求 \_ 篩選 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | 要求檔案的篩選隨機鎖定。<br/>                                                                                                                                          |
| [**FSCTL \_ 要求 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | 要求) 檔案上的隨機鎖定 (oplock，並確認已發生 oplock 中斷。<br/>                                                                                    |
| [**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | 要求檔案的層級1隨機鎖定。<br/>                                                                                                                                         |
| [**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | 要求檔案的層級2隨機鎖定。<br/>                                                                                                                                         |
| [**FSCTL \_ 設定 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | 在檔案系統支援每個檔案和每個目錄壓縮的磁片區上，設定檔案或目錄的壓縮狀態。<br/>                                                         |
| [**FSCTL \_ 設定 \_ 瑕疵 \_ 管理**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | 設定指定檔案的軟體瑕疵管理狀態。 用於 UDF 檔案系統。<br/>                                                                                             |
| [**FSCTL \_ 設定 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | 設定指定檔案或目錄的物件識別碼。<br/>                                                                                                                          |
| [**延伸的 FSCTL \_ 集 \_ 物件 \_ 識別碼 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | 修改與指定檔案或目錄的物件識別碼相關聯的使用者資料。<br/>                                                                                            |
| [**FSCTL \_ SET \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | 設定 NTFS 檔案系統的自我修復功能模式。<br/>                                                                                                                          |
| [**FSCTL \_ SET \_ SPARSE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | 將指定的檔案標示為稀疏或非稀疏。 在稀疏檔案中，大範圍的零可能不需要磁片配置。<br/>                                                               |
| [**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | 以零 (0) 填滿指定的檔案範圍。<br/>                                                                                                                                        |
| [**\_ \_ \_ 解除配置時，FSCTL 設定零 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | 指出 NTFS 檔案系統檔案控制代碼在解除配置時，應該將其叢集填滿零。<br/>                                                                             |
| [**FSCTL \_ 等候 \_ \_ 修復**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | 當指定的修復完成時傳回。<br/>                                                                                                                                        |



 

下列控制碼適用于 [檔案壓縮和解壓縮](file-compression-and-decompression.md)。

<dl>

[**FSCTL \_ 取得 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**FSCTL \_ 設定 \_ 壓縮**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

下列控制碼會搭配 [物件識別碼](distributed-link-tracking-and-object-identifiers.md)使用。

<dl>

[**FSCTL \_ 建立 \_ 或 \_ 取得 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**FSCTL \_ 刪除 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**FSCTL \_ 取得 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**FSCTL \_ 設定 \_ 物件 \_ 識別碼**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**延伸的 FSCTL \_ 集 \_ 物件 \_ 識別碼 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

下列控制碼可搭配隨機 [鎖定](opportunistic-locks.md)使用。

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ 關閉 \_ 擱置中**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ OPLOCK \_ 中斷 \_ ACK \_ 無 \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**FSCTL \_ OPLOCK \_ BREAK \_ 確認**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**FSCTL \_ OPLOCK \_ 中斷 \_ 通知**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**FSCTL \_ 要求 \_ 批次 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**FSCTL \_ 要求 \_ 篩選 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**FSCTL \_ 要求 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

下列控制碼可搭配 [稀疏](sparse-files.md)檔案使用。

<dl>

[**FSCTL \_ 查詢配置的 \_ \_ 範圍**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**FSCTL \_ SET \_ SPARSE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**FSCTL \_ 設定 \_ 零 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

下列控制碼可搭配 NTFS 自我修復機制使用。

<dl>

[**FSCTL \_ 取得 \_ 修復**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**FSCTL \_ 起始 \_ 修復**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**FSCTL \_ SET \_ REPAIR**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**FSCTL \_ 等候 \_ \_ 修復**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

下列控制碼適用于 UDF。

<dl>

[**FSCTL \_ 讓 \_ 媒體 \_ 相容**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**\_磁片區 \_ \_ \_ \_ 資訊上的 FSCTL 查詢**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**FSCTL \_ 查詢的 \_ 備用 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**FSCTL \_ 設定 \_ 瑕疵 \_ 管理**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[目錄管理控制碼](directory-management-control-codes.md)
</dt> <dt>

[磁碟區管理控制碼](volume-management-control-codes.md)
</dt> </dl>

 

