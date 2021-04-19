---
description: 下列列舉定義于磁片區陰影複製 API 中。
ms.assetid: f2f09791-b17e-4f54-9d29-83a4189bffc1
title: 磁片區陰影複製 API 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ade0af4637e9c057c9743dfaf0778e86b3d81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973280"
---
# <a name="volume-shadow-copy-api-enumerations"></a>磁片區陰影複製 API 列舉

下列列舉定義于磁片區陰影複製 API 中。



| Name                                                                           | 描述                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VSS \_ 替代 \_ 寫入器 \_ 狀態**](/windows/desktop/api/VsWriter/ne-vswriter-vss_alternate_writer_state)            | 定義用來指出寫入器是否有相關聯替代寫入器的有效狀態集。                                                              |
| [**VSS \_ 應用 \_ 層級**](/windows/desktop/api/Vss/ne-vss-vss_application_level)                       | 定義有效應用層級的集合。                                                                                                                       |
| [**VSS \_ 備份 \_ 架構**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)                               | 定義一組備份架構，也就是寫入器可以參與的作業。                                                                                          |
| [**VSS \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)                                   | 定義一組備份類型。                                                                                                                                   |
| [**VSS \_ 元件 \_ 旗標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)                           | 指出支援自動復原。                                                                                                                               |
| [**VSS \_ 元件 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)                             | 定義一組元件類型。                                                                                                                                |
| [**VSS \_ 檔 \_ 還原 \_ 狀態**](/windows/desktop/api/VsWriter/ne-vswriter-vss_file_restore_status)                  | 定義檔案還原作業的狀態集。                                                                                                           |
| [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)             | 定義寫入器支援的備份作業集。                                                                                                         |
| [**\_VSS \_ 硬體 \_ 選項**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)                      | 定義陰影複製 LUN 旗標。                                                                                                                                     |
| [**VSS \_ 管理 \_ 物件 \_ 類型**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_mgmt_object_type)                        | [**Vss 管理物件架構中 \_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) [**vss \_ 管理 \_ 物件 \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)聯集的判別。 |
| [**VSS \_ 物件 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_object_type)                                   | 用來將物件識別為陰影複製集、陰影複製或提供者。                                                                                         |
| [**VSS \_ 保護 \_ 錯誤**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)                         | 定義陰影禁止複製錯誤的集合。                                                                                                                  |
| [**VSS \_ 保護 \_ 層級**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)                         | 定義磁片區陰影禁止複製層級的集合。                                                                                                           |
| [**VSS \_ 提供者 \_ 功能**](/windows/desktop/api/vss/ne-vss-vss_provider_capabilities)              | 保留供未來使用。                                                                                                                                           |
| [**VSS \_ 提供者 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_provider_type)                               | 定義一組提供者類型。                                                                                                                                 |
| [**VSS \_ 修復 \_ 選項**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)                         | 由要求者用來指定重新同步處理作業的執行方式。                                                                               |
| [**VSS \_ 還原 \_ 目標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)                             | 定義還原目標集。                                                                                                                                |
| [**VSS \_ 還原 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)                                 | 定義要執行的一組還原作業。                                                                                                              |
| [**VSS \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)                     | 定義寫入器的一組預設檔案還原方法。                                                                                                      |
| [**VSS \_ 向前復原 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)                         | 由要求者用來指出即將執行的向前復原操作類型。                                                                         |
| [**VSS \_ 快照 \_ 相容性**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_compatibility)             | 定義磁片區控制或檔案 i/o 作業的集合，這些作業可以針對已陰影複製的磁片區停用。                                            |
| [**\_VSS \_ 快照集 \_ 內容**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)                      | 指定如何建立、查詢或刪除陰影複製，以及寫入器的參與程度。                                                            |
| [**VSS \_ 快照集 \_ 狀態**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)                             | 定義陰影複製作業的狀態集。                                                                                                              |
| [**VSS \_ 來源 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)                                   | 定義寫入器可以管理的一組資料類型。                                                                                                         |
| [**VSS \_ 訂閱 \_ 遮罩**](/windows/desktop/api/VsWriter/ne-vswriter-vss_subscribe_mask)                             | 定義寫入器可以接收的事件集。                                                                                                               |
| [**VSS \_ 使用 \_ 類型**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)                                     | 指定主機系統如何使用寫入器所管理的資料。                                                                                                   |
| [**\_VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) | 定義陰影複製的屬性集。                                                                                                                    |
| [**VSS \_ 寫入器 \_ 狀態**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)                                 | 定義寫入器的狀態集。                                                                                                                           |
| [**VSS \_ WRITERRESTORE \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_writerrestore_enum)                     | 定義一組條件，在這些條件下，寫入器將處理還原作業期間所產生的事件。                                                        |



 

 

 



