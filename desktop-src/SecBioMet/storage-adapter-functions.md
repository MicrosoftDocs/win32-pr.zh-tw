---
title: 儲存體介面卡功能
description: 儲存體介面卡會管理範本資料庫。
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7072847c6d1ca653bd9e8edad9c51b7736354b447feeafda7c465973d4c25aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911800"
---
# <a name="storage-adapter-functions"></a>儲存體介面卡功能

儲存體介面卡會管理範本資料庫。 介面卡開發人員必須執行下列函數。 Windows 生物特徵辨識服務會呼叫它們。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                         | 描述                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | 讓儲存體的介面卡有機會執行任何需要的工作，以將儲存體元件移出閒置狀態。<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | 將範本加入至資料庫。<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | 將儲存體介面卡新增至生物特徵辨識設備的處理管線。<br/>                                                     |
| [**StorageAdapterClearCoNtext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | 準備新作業的生物特徵辨識單位處理管線。<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | 關閉與管線相關聯的資料庫，並釋出所有相關資源。<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | 執行不需要較高許可權的廠商定義控制項作業。<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | 執行需要更高許可權的廠商定義控制項作業。<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | 建立並設定新的資料庫。<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | 讓儲存體的介面卡有機會執行任何需要的工作，以將儲存元件置於閒置狀態。<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | 從資料庫中刪除一個或多個範本。<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | 釋放附加至管線的介面卡特定資源。<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | 清除資料庫，並將其標示為刪除。<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | 將結果集資料指標放置在集合中的第一筆記錄。<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | 抓取管線結果集中目前記錄的內容。<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | 抓取資料庫大小和可用空間。<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | 抓取與管線相關聯之目前資料庫所使用的格式和版本資訊。<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | 捕獲管線結果集中的範本記錄數目。<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | 將結果集資料指標前進一筆記錄。<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | 接收有關電腦電源狀態變更的通知，並據以準備存放裝置介面卡。<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | 開啟資料庫以供儲存體介面卡使用。<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | 讓儲存體的介面卡有機會執行任何清理，以準備關閉範本資料庫。<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | 讓儲存體的介面卡有機會執行任何未完成的初始化。<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | 查詢目前開啟的資料庫，以取得與指定之索引向量相關聯的範本。<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | 查詢目前開啟的資料庫，以取得與指定之身分識別和子因數相關聯的範本。<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | 決定生物特徵辨識儲存元件的功能和限制。<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | 抓取儲存體介面卡的 [**WINBIO \_ 儲存體 \_ 介面**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) 結構指標。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> </dl>

 

 





