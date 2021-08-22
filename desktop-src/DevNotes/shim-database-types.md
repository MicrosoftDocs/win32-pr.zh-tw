---
description: 代表主要和自訂填充碼資料庫的類型。
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: 填充碼資料庫類型
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cc36cbb198570618fbd1a6524e4e7c6dc6812fb01bd74fe04cf1bd91b31f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075922"
---
# <a name="shim-database-types"></a>填充碼資料庫類型

代表主要和自訂填充碼資料庫的類型。



| 常數/值                                                                                                                                                                                                                                                | 描述                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_資料庫 \_ 主要**</dt> <dt>0x80000000</dt> </dl>                    | 主資料庫。 如果這個旗標不存在，則表示資料庫是自訂資料庫。<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_資料庫 \_ 填充碼**</dt> <dt>0x00010000</dt> </dl>                    | 資料庫包含要填充的應用程式專案。<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_資料庫 \_ MSI**</dt> <dt>0x00020000</dt> </dl>                       | 資料庫包含 MSI 專案。<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_資料庫 \_ 驅動程式**</dt> <dt>0x00040000</dt> </dl>           | 資料庫包含驅動程式區塊專案。<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_資料庫 \_ 詳細資料**</dt> <dt>0x00080000</dt> </dl>           | 資料庫包含 Apphelp 詳細資料。<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_資料庫 \_ SP \_ 詳細資料**</dt> <dt>0x00100000</dt> </dl> | 資料庫包含 SP Apphelp 詳細資料。<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_資料庫 \_ 資源**</dt> <dt>0x00200000</dt> </dl>        | 資源 DLL 包含 Apphelp 詳細資料。<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0xF02F0000</dt> </dl>    | 用來解壓縮主要資料庫資訊的遮罩。<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ 資料庫 \_ 主要 \_ 填充碼**</dt> </dl>                                                                    | SDB \_ 資料庫 \_ 填充碼 \| SDB \_ 資料庫 \_ MSI \| SDB \_ 資料庫 \_ 主資料庫<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ 資料庫 \_ 主要 \_ MSI**</dt> </dl>                                                                       | SDB \_ 資料庫 \_ MSI \| SDB \_ 資料庫 \_ 主資料庫<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_ 資料庫 \_ 主要 \_ 驅動程式**</dt> </dl>                                                           | SDB \_ 資料庫 \_ 驅動程式 \| SDB \_ 資料庫 \_ 主要<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**SDB \_ 資料庫 \_ 主要 \_ 詳細資料**</dt> </dl>                                                           | SDB \_ 資料庫 \_ 詳細說明 \| SDB \_ 資料庫 \_ 主資料庫<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**SDB \_ 資料庫 \_ 主要的 \_ SP \_ 詳細資料**</dt> </dl>                                                 | SDB \_ 資料庫 \_ SP \_ 詳細資料 \| SDB \_ 資料庫 \_ 主資料庫<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**SDB \_ 資料庫 \_ 主要 \_ 資源**</dt> </dl>                                                        | SDB \_ 資料庫 \_ 資源 \| SDB \_ 資料庫 \_ 主資料庫<br/>                                     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




