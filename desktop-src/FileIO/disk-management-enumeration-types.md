---
description: 搭配磁片管理使用的列舉類型。
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: 磁片管理列舉類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c186a2a722bf9614bb83b19bcaa29be486cf54bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984671"
---
# <a name="disk-management-enumeration-types"></a>磁片管理列舉類型

下列列舉類型用於磁片管理。

## <a name="in-this-section"></a>本節內容



| 列舉型別                                                                              | 描述                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**媒體 \_ 類型**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | 代表裝置媒體的各種形式。<br/>                                                                                                                                                                                                                                                             |
| [**分割區 \_ 樣式**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | 表示資料分割的格式。<br/>                                                                                                                                                                                                                                                                     |
| [**儲存體 \_ 匯流排 \_ 類型**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | 提供表示儲存體匯流排類型的符號表示。<br/>                                                                                                                                                                                                                                              |
| [**儲存體 \_ 元件 \_ 健康情況 \_ 狀態**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | 指定儲存元件的健全狀況狀態。<br/>                                                                                                                                                                                                                                                       |
| [**儲存體 \_ 裝置 \_ \_ 外型規格**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | 指定裝置的外型規格。<br/>                                                                                                                                                                                                                                                                    |
| [**儲存體 \_ 裝置 \_ 電源 \_ 上限 \_ 單位**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | 最大電源閾值的單位。<br/>                                                                                                                                                                                                                                                                 |
| [**儲存體 \_ 埠程式 \_ 代碼 \_ 集**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | 保留供系統使用。 <br/>                                                                                                                                                                                                                                                                                 |
| [**儲存體 \_ 屬性 \_ 識別碼**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | 列舉以輸入形式傳遞至 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property)要求之 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query)結構的 **PropertyId** 成員可能值，以抓取儲存裝置或介面卡的屬性。<br/> |
| [**儲存體 \_ 通訊協定 \_ 類型**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | 指定儲存裝置的通訊協定。<br/>                                                                                                                                                                                                                                                               |
| [**儲存體 \_ 查詢 \_ 類型**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | 由傳遞至 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property)控制項程式碼的 [**儲存體 \_ 屬性 \_ 查詢**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query)結構所使用，指出傳回的儲存裝置或介面卡屬性相關資訊。<br/>                             |
| [**寫入快取 \_ \_ 變更**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | 指出裝置的寫入快取功能是否可變更。<br/>                                                                                                                                                                                                                                    |
| [**啟用寫入快取 \_ \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | 指出是否啟用或停用寫入快取。<br/>                                                                                                                                                                                                                                                 |
| [**寫入快取 \_ \_ 類型**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | 指定快取類型。<br/>                                                                                                                                                                                                                                                                                 |
| [**寫入 \_**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | 指定存放裝置是否支援寫入快取。<br/>                                                                                                                                                                                                                                        |



 

 

