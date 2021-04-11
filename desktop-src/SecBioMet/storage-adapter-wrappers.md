---
title: 儲存體介面卡包裝函式
description: 您可以用來在儲存體介面卡上呼叫函式的函式。 這些函式定義于 Winbio \_ adapter. h 中。
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf562546e1520ee85c5a9a0164acdff53904
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372248"
---
# <a name="storage-adapter-wrappers"></a>儲存體介面卡包裝函式

下列包裝函式是在 Winbio \_ adapter. h 中定義。 您可以使用它們來呼叫儲存體介面卡上的函式。



| 函式                                    | 描述                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | 呼叫 [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                   |
| WbioStorageAddRecord<br/>             | 呼叫 [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) 函數。<br/>                                                                                       |
| WbioStorageAttach<br/>                | 呼叫 [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) 函數。<br/>                                                                                             |
| WbioStorageClearCoNtext<br/>          | 呼叫 [**StorageAdapterClearCoNtext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) 函數。<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | 呼叫 [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) 函數。<br/>                                                                               |
| WbioStorageControlUnit<br/>           | 呼叫 [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) 函數。<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | 呼叫 [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) 函數。<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | 呼叫 [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) 函數。<br/>                                                                             |
| WbioStorageDeactivate<br/>            | 呼叫 [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>               |
| WbioStorageDeleteRecord<br/>          | 呼叫 [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) 函數。<br/>                                                                                 |
| WbioStorageDetach<br/>                | 呼叫 [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) 函數。<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | 呼叫 [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) 函數。<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | 呼叫 [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) 函數。<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | 呼叫 [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) 函數。<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | 呼叫 [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) 函數。<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | 呼叫 [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) 函數。<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | 呼叫 [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) 函數。<br/>                                                                             |
| WbioStorageNextRecord<br/>            | 呼叫 [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) 函數。<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | 呼叫 [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) 函數。<br/> 從 Windows 8 開始，支援這個包裝函式函數。<br/>    |
| WbioStorageOpenDatabase<br/>          | 呼叫 [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) 函數。<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | 呼叫 [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>     |
| WbioStoragePipelineInit<br/>          | 呼叫 [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>           |
| WbioStorageQueryByContent<br/>        | 呼叫 [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) 函數。<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | 呼叫 [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) 函數。<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | 呼叫 [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[儲存體介面卡功能](storage-adapter-functions.md)
</dt> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> </dl>

 

 





