---
description: 控制大量管理中使用的代碼。
ms.assetid: 87f39e1c-3ebf-4c6f-a842-699ec3c45e76
title: 磁碟區管理控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cccb73559826b8b0b3001588458a4cf34863f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979299"
---
# <a name="volume-management-control-codes"></a>磁碟區管理控制碼

控制大量管理中使用的代碼。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                                      | 描述                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ 建立 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)<br/>                                                                 | 在目標磁片區上 (USN) 變更日誌串流，或修改現有的變更日誌串流，以建立更新序號。<br/>                                                                                                                               |
| [**FSCTL \_ CSV \_ 查詢 \_ 下移 \_ 層級 \_ 檔 \_ 系統 \_ 特性**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_query_down_level_file_system_characteristics)<br/> | 抓取 CSVFS 為 proxy 之檔案系統的相關資訊。<br/>                                                                                                                                                                                          |
| [**FSCTL \_ 刪除 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)<br/>                                                                 | 刪除磁片區上 (USN) 變更日誌的更新序號，或等候變更日誌刪除的通知。<br/>                                                                                                                                     |
| [**FSCTL \_ 卸載 \_ 磁片區**](/windows/win32/api/winioctl/ni-winioctl-fsctl_dismount_volume)<br/>                                                                        | 無論磁片區目前是否正在使用中，都要卸載磁片區。 如需詳細資訊，請參閱＜備註＞一節。<br/>                                                                                                                                 |
| [**FSCTL \_ 列舉 \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)<br/>                                                                           | 列舉兩個指定界限之間 (USN) 資料的更新序號，以取得主要檔案資料表 (MFT) 記錄。<br/>                                                                                                                                   |
| [**FSCTL \_ 延伸 \_ 磁片區**](/windows/win32/api/winioctl/ni-winioctl-fsctl_extend_volume)<br/>                                                                            | 增加載入的磁片區大小。<br/>                                                                                                                                                                                                                        |
| [**FSCTL \_ 取得 \_ 開機 \_ 區域 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_boot_area_info)<br/>                                                                | 抓取磁片區的開機磁區位置。 <br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/>                                                                      |
| [**FSCTL \_ 取得 \_ 完整性 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_integrity_information)<br/>                                                   | 抓取 ReFS 磁片區上的檔案或目錄的完整性狀態。<br/>                                                                                                                                                                                        |
| [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)<br/>                                                            | 抓取指定 NTFS 檔案系統磁片區的相關資訊。<br/>                                                                                                                                                                                             |
| [**FSCTL \_ 取得 \_ 抓取 \_ 指標 \_ 基底**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointer_base)<br/>                                                | 將磁區位移傳回至相對於磁片區開頭之檔案系統 (LCN) 的第一個邏輯群集編號。<br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/> |
| [**FSCTL \_ 取得 \_ 抓取 \_ 指標**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers)<br/>                                                         | 指定檔案控制代碼時，會抓取描述特定檔案磁片上配置和位置的資料結構，或者，指定磁片區控制碼，磁片區上的錯誤叢集位置。<br/>                                                                   |
| [**FSCTL \_ 取得 \_ 磁片區 \_ 點陣圖**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap)<br/>                                                                   | 抓取磁片區上已佔用和可用叢集的點陣圖。<br/>                                                                                                                                                                                             |
| [**FSCTL \_ 是 \_ CSV \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_is_csv_file)<br/>                                                                               | 判斷檔案是否儲存在 CSVFS 磁片區上，或抓取命名空間資訊。<br/>                                                                                                                                                                     |
| [**FSCTL \_ 是 \_ \_ \_ CSV 磁片區 \_ 上的檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_is_file_on_csv_volume)<br/>                                                         | 判斷檔案是否儲存在 CSVFS 磁片區上，或抓取命名空間資訊。<br/>                                                                                                                                                                     |
| [**FSCTL \_ 已 \_ 裝載磁片區 \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_is_volume_mounted)<br/>                                                                   | 判斷指定的磁片區是否已掛接，或指定的檔案或目錄是否在載入的磁片區上。<br/>                                                                                                                                              |
| [**FSCTL \_ 是 \_ 磁片區 \_ 擁有的 \_ BYCSVFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_is_volume_owned_bycsvfs)<br/>                                                      | 判斷是否已由 CSVFS 鎖定磁片區。<br/>                                                                                                                                                                                                                |
| [**FSCTL \_ 鎖定 \_ 音量**](/windows/win32/api/winioctl/ni-winioctl-fsctl_lock_volume)<br/>                                                                                | 鎖定未使用的磁片區。<br/>                                                                                                                                                                                                                            |
| [**從叢集 FSCTL \_ 查閱 \_ 資料流程 \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster)<br/>                                                | 如果 ntfs 磁片區或 NTFS 磁片區上的檔案有控制碼，就會傳回一系列的資料結構，描述佔用指定叢集的資料流程。<br/>                                                                                                      |
| [**FSCTL \_ MARK \_ 把手**](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)<br/>                                                                                | 將指定的檔案或目錄及其變更日誌記錄標記為檔案或目錄的變更相關資訊。<br/>                                                                                                                                    |
| [**FSCTL \_ 移動 \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file)<br/>                                                                                    | 將檔案的一或多個虛擬叢集重新放置於相同磁片區中的另一個邏輯群集。 這項作業會在 [磁碟重組](defragmenting-files.md)期間使用。<br/>                                                                         |
| [**FSCTL \_ 查詢 \_ 檔 \_ 系統 \_ 識別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)<br/>                                          | 查詢磁片區上的檔案系統識別資訊。<br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/>                                                                |
| [**FSCTL \_ 查詢 \_ 區域 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_region_info)<br/>                                                                   | 抓取針對支援資料階層式磁片區所定義的儲存層區域。<br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/>                                         |
| [**FSCTL \_ 查詢 \_ 儲存體 \_ 類別**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_storage_classes)<br/>                                                           | 抓取針對支援資料階層式磁片區所定義的儲存層。<br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/>                                                |
| [**FSCTL \_ 查詢 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)<br/>                                                                   | 查詢目前更新序號 (USN) 變更日誌、其記錄和容量的相關資訊。<br/>                                                                                                                                             |
| [**FSCTL \_ READ \_ FILE \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_file_usn_data)<br/>                                                                | 抓取 (USN) 指定檔案或目錄的變更日誌資訊更新序號。<br/>                                                                                                                                                     |
| [**FSCTL \_ 讀取 \_ 自 \_ PLEX**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_from_plex)<br/>                                                                         | 從指定的 plex 讀取。<br/>                                                                                                                                                                                                                                 |
| [**FSCTL \_ 讀取 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)<br/>                                                                     | 抓取 (USN 的更新序號集) 變更兩個指定 USN 值之間的日誌記錄。<br/>                                                                                                                                                     |
| [**FSCTL \_ 修復 \_ 複本**](/windows/win32/api/winioctl/ni-winioctl-fsctl_repair_copies)<br/>                                                                            | 選取要使用的適當複本來修復資料損毀。<br/>                                                                                                                                                                                                    |
| [**FSCTL \_ 設定 \_ 完整性 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_integrity_information)<br/>                                                   | 抓取 ReFS 磁片區上的檔案或目錄的完整性狀態。<br/>                                                                                                                                                                                        |
| [**FSCTL \_ 壓縮 \_ 音量**](/windows/win32/api/winioctl/ni-winioctl-fsctl_shrink_volume)<br/>                                                                            | 指出磁片區準備執行壓縮作業、壓縮作業已被認可，或壓縮作業將會終止。<br/>                                                                                               |
| [**FSCTL \_ 解除鎖定 \_ 音量**](/windows/win32/api/winioctl/ni-winioctl-fsctl_unlock_volume)<br/>                                                                            | 解除鎖定磁片區。<br/>                                                                                                                                                                                                                                              |
| [**FSCTL \_ USN \_ 追蹤 \_ 修改過的 \_ 範圍**](/windows/win32/api/winioctl/ni-winioctl-fsctl_usn_track_modified_ranges)<br/>                                                  | 啟用更新序號的範圍追蹤功能 (USN) 變更目標磁片區上的日誌串流，或修改已啟用的範圍追蹤參數。<br/>                                                                                               |
| [**FSCTL \_ 寫入 \_ USN \_ 關閉 \_ 記錄**](/windows/win32/api/winioctl/ni-winioctl-fsctl_write_usn_close_record)<br/>                                                        | 以更新序號產生記錄， (USN) 變更輸入檔的日誌串流。<br/>                                                                                                                                                               |
| [**IOCTL \_ 磁片區 \_ 取得 \_ GPT \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_gpt_attributes)<br/>                                                  | 抓取磁片區的屬性。<br/> 若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。<br/>                                                                                      |
| [**IOCTL \_ VOLUME \_ 取得 \_ \_ 磁片 \_ 區磁片區**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents)<br/>                                       | 在一或多個磁片上，抓取指定磁片區的實體位置。<br/>                                                                                                                                                                                    |
| [**IOCTL \_ 磁片區 \_ 已叢集 \_ 化**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_is_clustered)<br/>                                                               | 判斷指定的磁片區是否已叢集化。<br/>                                                                                                                                                                                                          |
| [**IOCTL \_ 磁片區 \_ 是 \_ CSV**](ioctl-volume-is-csv.md)<br/>                                                                           | 判斷磁片區是否為 CSV 磁片區。<br/>                                                                                                                                                                                                                   |
| [**IOCTL \_ 磁片區 \_ 離線**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_offline)<br/>                                                                          | 使磁片區離線。<br/>                                                                                                                                                                                                                                        |
| [**IOCTL \_ 磁片區 \_ 上線**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_online)<br/>                                                                            | 使磁片區上線。<br/>                                                                                                                                                                                                                                        |



 

下列控制碼可搭配 [變更日誌](change-journals.md)使用。

-   [**FSCTL \_ 建立 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [**FSCTL \_ 刪除 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [**FSCTL \_ 列舉 \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [**FSCTL \_ MARK \_ 把手**](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [**FSCTL \_ 查詢 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [**FSCTL \_ READ \_ FILE \_ USN \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_file_usn_data)
-   [**FSCTL \_ 讀取 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)
-   [**FSCTL \_ 寫入 \_ USN \_ 關閉 \_ 記錄**](/windows/win32/api/winioctl/ni-winioctl-fsctl_write_usn_close_record)

以下是 [磁碟重組](defragmenting-files.md) 控制代碼。

-   [**FSCTL \_ 取得 \_ 抓取 \_ 指標 \_ 基底**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointer_base)
-   [**FSCTL \_ 取得 \_ 抓取 \_ 指標**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers)
-   [**FSCTL \_ 取得 \_ 磁片區 \_ 點陣圖**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap)
-   [**從叢集 FSCTL \_ 查閱 \_ 資料流程 \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_lookup_stream_from_cluster)
-   [**FSCTL \_ 移動 \_ 檔案**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file)
-   [**FSCTL \_ 查詢 \_ 區域 \_ 資訊**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_region_info)
-   [**FSCTL \_ 查詢 \_ USN \_ 日誌**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[目錄管理控制碼](directory-management-control-codes.md)
</dt> <dt>

[檔案管理控制碼](file-management-control-codes.md)
</dt> </dl>

 

