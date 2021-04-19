---
description: VDS 列舉代表 VDS 物件模型中的物件類型、旗標、狀態和其他實體。 如需 VDS 物件及其相關列舉的詳細資訊，請參閱 VDS 物件模型。
ms.assetid: 30ee6e39-c1e5-4173-a3dd-5644632140d1
title: VDS 列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da784104c939a99f7341e7c9d5043824c6eeaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975920"
---
# <a name="vds-enumerations"></a>VDS 列舉

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

VDS 列舉代表 VDS 物件模型中的物件類型、旗標、狀態和其他實體。 如需 VDS 物件及其相關列舉的詳細資訊，請參閱 [Vds 物件模型](vds-object-model.md)。



| 列舉型別                                                                                      | 描述                                                                                                                                             |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**標記 \_ VDS \_ 分割區 \_ 樣式**](/windows/win32/api/vds/ne-vds-__vds_partition_style)                                    | 保留的列舉。                                                                                                                                   |
| [**VDS \_ 非同步 \_ 輸出 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type)                                        | 指定可以非同步處理的作業。                                                                                              |
| [**VDS \_ 控制器 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_controller_status)                                         | 指定控制器的有效物件狀態值。                                                                                               |
| [**VDS \_ 磁片 \_ 區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type)                                          | 指定磁片範圍物件類型值。                                                                                                           |
| [**VDS \_ 磁片 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag)                                                         | 指定磁片旗標值。                                                                                                                            |
| [**VDS \_ 磁片 \_ 離線 \_ 原因**](/windows/desktop/api/Vds/ne-vds-vds_disk_offline_reason)                                    | 定義磁片離線的原因集。                                                                                                    |
| [**VDS \_ 磁片 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_disk_status)                                                     | 指定磁片狀態值。                                                                                                                           |
| [**VDS \_ 磁片磁碟機 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag)                                                       | 指定磁片磁碟機的有效旗標。                                                                                                                   |
| [**VDS \_ 磁碟機 \_ 號 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag)                                        | 指定磁碟機號旗標值。                                                                                                                     |
| [**VDS \_ 磁片磁碟機 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)                                                   | 指定磁片磁碟機的有效物件狀態值。                                                                                                    |
| [**VDS \_ 檔 \_ 系統 \_ 格式 \_ 支援 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_file_system_format_support_flag)          | 定義支援格式化磁片區的檔案系統屬性。                                                                       |
| [**VDS \_ 檔 \_ 系統 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag)                                          | 指定檔案系統旗標值。                                                                                                                      |
| [**VDS \_ 檔 \_ 系統的 \_ 主張 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag)                               | 指定檔案系統屬性旗標值。                                                                                                             |
| [**VDS \_ 檔 \_ 系統 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type)                                          | 定義檔案系統的一組有效類型。                                                                                                       |
| [**VDS \_ 格式 \_ 選項 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_format_option_flags)                                    | 為 [**IVdsDiskPartitionMF2：： FormatPartitionEx2**](/windows/desktop/api/Vds/nf-vds-ivdsdiskpartitionmf2-formatpartitionex2) 方法定義有效的格式化選項組。 |
| [**VDS \_ HBAPORT \_ 速度 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag)                                      | 指定 HBA 埠所支援的速度集合。                                                                                                   |
| [**VDS \_ HBAPORT \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status)                                               | 指定 HBA 埠的有效狀態集。                                                                                                    |
| [**VDS \_ HBAPORT \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type)                                                   | 針對 HBA 埠指定一組有效的類型。                                                                                                       |
| [**VDS \_ 健康情況**](/windows/desktop/api/Vds/ne-vds-vds_health)                                                                | 為 VDS 物件定義有效的健康狀態值集。                                                                                         |
| [**VDS \_ HWPROVIDER \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type)                                             | 定義硬體提供者的一組有效類型。                                                                                                 |
| [**VDS \_ 互連 \_ 位址 \_ 類型**](/windows/desktop/api/VdsLun/ne-vdslun-vds_interconnect_address_type)                        | 指定實體互連的有效網址類別型。                                                                                           |
| [**VDS \_ 互連 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_interconnect_flag)                                         | 定義子系統可以支援的一組互連類型。                                                                                      |
| [**VDS \_ IPADDRESS \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_ipaddress_type)                                               | 定義 IP 位址的一組有效類型。                                                                                                       |
| [**VDS \_ ISCSI \_ 驗證 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type)                                            | 定義登入 iSCSI 目標時驗證的有效類型集合。                                                                    |
| [**VDS \_ ISCSI \_ IPSEC \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag)                                          | 定義一組有效的旗標，以指出建立目標入口網站的 TCP 連線時所使用的 IPSEC 類型。                           |
| [**VDS \_ ISCSI \_ 登入 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag)                                          | 定義一組有效的旗標，指出 iSCSI 啟動器應如何登入目標。                                                         |
| [**VDS \_ ISCSI \_ 登入 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type)                                          | 定義用於登入 iSCSI 目標的一組有效類型。                                                                                        |
| [**VDS \_ ISCSI \_ 入口網站 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status)                                    | 定義 iSCSI 入口網站的有效狀態值集。                                                                                             |
| [**VDS \_ LOADBALANCE \_ 原則 \_ 列舉**](/windows/desktop/api/Vds/ne-vds-vds_loadbalance_policy_enum)                            | 為路徑指定一組有效的負載平衡原則。                                                                                              |
| [**VDS \_ LUN \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag)                                                           | 指定 LUN 的有效旗標。                                                                                                                     |
| [**VDS \_ LUN \_ PLEX \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag)                                                | 指定 LUN plex 的有效旗標。                                                                                                                |
| [**VDS \_ LUN \_ PLEX \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)                                            | 指定 LUN plex 的有效物件狀態值。                                                                                                 |
| [**VDS \_ LUN \_ PLEX \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type)                                                | 指定 LUN plex 的有效類型。                                                                                                                |
| [**VDS \_ LUN \_ 保留 \_ 模式**](/windows/desktop/api/Vds/ne-vds-vds_lun_reserve_mode)                                          | 此列舉保留供日後使用。                                                                                                            |
| [**VDS \_ LUN \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)                                                       | 指定 LUN 的有效物件狀態值。                                                                                                      |
| [**VDS \_ LUN \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                           | 指定 LUN 的有效類型。                                                                                                                     |
| [**VDS \_ 維護 \_ 作業**](/windows/desktop/api/Vds/ne-vds-vds_maintenance_operation)                                 | 指定有效的維護作業。                                                                                                                 |
| [**VDS \_ 通知 \_ 目標 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_notification_target_type)                          | 為 VDS 通知 (主體) 指定有效的目標型別。                                                                                      |
| [**VDS \_ 物件 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_object_type)                                                     | 指定 VDS 物件的有效類型。                                                                                                              |
| [**VDS \_ 套件 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag)                                                         | 指定套件旗標值。                                                                                                                             |
| [**VDS \_ 套件 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_pack_status)                                                     | 指定套件狀態值。                                                                                                                           |
| [**VDS \_ 分割區 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag)                                               | 指定資料分割旗標值。                                                                                                                        |
| [**VDS \_ 分割區 \_ 樣式**](/windows/desktop/api/Vds/ne-vds-vds_partition_style)                                             | 指定資料分割樣式值。                                                                                                                       |
| [**VDS \_ 路徑 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_path_status)                                                     | 指定埠的有效狀態值集。                                                                                                    |
| [**VDS \_ 埠 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                     | 指定埠的有效物件狀態值。                                                                                                     |
| [**VDS \_ 提供者 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag)                                                 | 指定提供者旗標值。                                                                                                                         |
| [**VDS \_ 提供者 \_ LBSUPPORT \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_provider_lbsupport_flag)                            | 指定一組有效的旗標，指出硬體提供者所支援的負載平衡原則。                                               |
| [**VDS \_ 提供者 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_provider_type)                                                 | 指定提供者類型值。                                                                                                                     |
| [**VDS \_ 查詢 \_ 提供者 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)                                    | 指定提供者查詢作業的有效旗標。                                                                                               |
| [**VDS \_ RAID \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_raid_type)                                                         | 定義可搭配 [儲存集區](storage-pool-object.md)使用的 RAID 層級集合。                                                          |
| [**VDS \_ 復原 \_ 動作**](/windows/desktop/api/Vds/ne-vds-vds_recover_action)                                               | 此列舉是保留供系統使用。                                                                                                            |
| [**VDS \_ SAN \_ 原則**](/windows/desktop/api/Vds/ne-vds-vds_san_policy)                                                       | 定義有效的磁片 SAN 原則旗標集合。                                                                                                         |
| [**VDS \_ 服務 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_service_flag)                                                   | 指定服務旗標值。                                                                                                                          |
| [**VDS \_ 儲存體 \_ 匯流排 \_ 類型**](/windows/desktop/api/VdsLun/ne-vdslun-vds_storage_bus_type)                                          | 指定儲存裝置的有效匯流排類型。                                                                                                      |
| [**VDS \_ 儲存體 \_ 識別碼程式 \_ 代碼 \_ 集**](/windows/desktop/api/VdsLun/ne-vdslun-vds_storage_identifier_code_set)                   | 指定有效的程式碼集 (編碼) 儲存識別碼。                                                                                       |
| [**VDS \_ 儲存區 \_ 識別碼 \_ 類型**](/windows/desktop/api/VdsLun/ne-vdslun-vds_storage_identifier_type)                            | 指定儲存識別碼的有效類型。                                                                                                      |
| [**VDS \_ 儲存 \_ 集區 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)                                    | 定義 [存放集區](storage-pool-object.md)的物件狀態值集。                                                                  |
| [**VDS \_ 儲存 \_ 集區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)                                        | 定義一組 [儲存集區](storage-pool-object.md) 類型。                                                                                       |
| [**VDS \_ 子 \_ 系統 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag)                                            | 指定子系統的有效旗標。                                                                                                               |
| [**VDS \_ 子系統 \_ 系統 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status)                                        | 指定子系統的有效物件狀態值。                                                                                                |
| [**VDS \_ SUB \_ SYSTEM \_ 支援 \_ RAID \_ TYPE \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_supported_raid_type_flag) | 定義子系統可以支援的一組 RAID 層級。                                                                                     |
| [**VDS \_ 轉換 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_transition_state)                                           | 定義 VDS 物件的有效轉換狀態值集。                                                                                  |
| [**VDS \_ VDISK \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_vdisk_state)                                                     | 定義虛擬磁片物件的狀態值集。                                                                                             |
| [**VDS \_ 版本 \_ 支援 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag)                                  | 指定支援的 VDS 介面版本。                                                                                             |
| [**VDS \_ 磁片區 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag)                                                     | 指定磁片區旗標值。                                                                                                                           |
| [**VDS \_ 磁片區 \_ PLEX \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status)                                      | 指定磁片區 plex 狀態值。                                                                                                                    |
| [**VDS \_ 磁片區 \_ PLEX \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)                                          | 指定磁片區-plex 類型值。                                                                                                                      |
| [**VDS \_ 磁片區 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_volume_status)                                                 | 指定磁片區狀態值。                                                                                                                         |
| [**VDS \_ 磁片區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)                                                     | 指定磁片區類型值。                                                                                                                           |



 

 

 
