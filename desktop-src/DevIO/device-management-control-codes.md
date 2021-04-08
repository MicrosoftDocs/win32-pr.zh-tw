---
description: 下列控制碼可搭配更換器裝置使用。
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: 裝置管理控制代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025974"
---
# <a name="device-management-control-codes"></a>裝置管理控制代碼

下列控制碼可搭配更換器裝置使用。



| 值                                                                                          | 意義                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**將 IOCTL 變更為 \_ \_ EXCHANGE \_ MEDIUM**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | 將來源專案的媒體移至一個目的地，而將一段媒體從最初在第一個目的地移至第二個目的地。 |
| [**IOCTL \_ 變換器 \_ 取得 \_ 元素 \_ 狀態**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | 抓取所有元素的狀態，或特定類型的指定專案數。                                                         |
| [**IOCTL \_ 轉換器 \_ 取得 \_ 參數**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | 捕獲指定裝置的參數。                                                                                                    |
| [**IOCTL \_ 轉換器 \_ 取得 \_ 產品 \_ 資料**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | 抓取指定裝置的產品資料。                                                                                                 |
| [**IOCTL 變更器 \_ \_ 取得 \_ 狀態**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | 抓取指定裝置的目前狀態。                                                                                                |
| [**IOCTL 變更器 \_ \_ 初始化 \_ 元素 \_ 狀態**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | 初始化所有元素的狀態或特定類型的指定專案。                                                               |
| [**IOCTL \_ 轉換器 \_ 移動 \_ 媒體**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | 將媒體片段移至目的地。                                                                                                             |
| [**IOCTL \_ 變換器 \_ 查詢 \_ 磁片區 \_ 標記**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | 抓取所指定元素的磁片區標記資訊。                                                                                     |
| [**IOCTL \_ 轉換器重新 \_ 初始化 \_ 傳輸**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | 實際 recalibrates 傳輸元素。                                                                                                         |
| [**IOCTL \_ 轉換器 \_ 設定 \_ 存取權**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | 設定裝置的插入/退出埠、大門或鍵盤的狀態。                                                                                   |
| [**IOCTL \_ 變換器 \_ 設定 \_ 位置**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | 將轉換器的機器人傳輸機制設定為指定的專案位址。                                                                     |



 

下列控制碼適用于裝置管理。



| 控制程式代碼                                                                                      | 作業                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IOCTL \_ 儲存體 \_ 檢查 \_ 驗證**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | 檢查卸除式媒體裝置中的變更。                                                               |
| [**IOCTL \_ 儲存體 \_ 退出 \_ 媒體**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | 從 SCSI 裝置彈出媒體。                                                                             |
| [**IOCTL \_ 儲存體 \_ 彈出 \_ 控制項**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | 啟用或停用彈出媒體的機制。                                                         |
| [**IOCTL \_ 儲存體 \_ 取得 \_ 裝置 \_ 編號**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | 抓取裝置的裝置類型、裝置號碼，以及可分割裝置的磁碟分割編號。 |
| [**IOCTL \_ 儲存體 \_ 取得 \_ 熱插拔 \_ 資訊**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | 抓取指定裝置的熱設定。                                                 |
| [**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號 \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | 抓取 USB 裝置的序號。                                                                 |
| [**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 類型**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | 抓取裝置的幾何資訊。                                                            |
| [**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 類型（ \_ 例如**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | 抓取裝置所支援媒體類型的相關資訊。                                        |
| [**IOCTL \_ 儲存體 \_ 載入 \_ 媒體**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | 將媒體載入裝置。                                                                                   |
| [**IOCTL \_ 儲存區 \_ 管理 \_ 資料 \_ 集 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**IOCTL \_ 儲存體 \_ MCN \_ 控制項**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | 啟用或停用媒體變更通知。                                                               |
| [**將 IOCTL \_ 儲存體 \_ 媒體 \_ 移除**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | 啟用或停用媒體退出機制。                                                               |
| [**IOCTL \_ 儲存體 \_ 讀取 \_ 容量**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | 抓取裝置的幾何資訊。                                                           |
| [**IOCTL \_ 儲存 \_ 集 \_ 熱 \_ 資訊**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | 設定指定裝置的熱設定。                                                      |



 

 

 



