---
title: MS SQL 類型屬性
description: 此 SQL 伺服器所使用的複寫類型。
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- MS SQL 類型屬性 AD 架構
- mS SQL 類型屬性 AD 架構
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15850884b8071fc103abf2c8d3f12ad68d4f5ed946ef2b491b4907b87b1cb524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583288"
---
# <a name="ms-sql-type-attribute"></a>MS SQL 類型屬性

此 SQL 伺服器所使用的複寫類型。 下列值是這個屬性的可能值。



| 值        | 描述                           |
|--------------|---------------------------------------|
| 0<br/> | 異動複寫。<br/> |
| 1<br/> | 快照式複寫。<br/>      |
| 2<br/> | 合併式複寫。<br/>         |



 



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | 毫秒-SQL 類型                                 |
| Ldap-顯示名稱 | 毫秒-SQL 類型                                 |
| 大小              | \-                                          |
| 更新許可權  | 網域系統管理員                        |
| 更新頻率  | 當複寫設定完成時。                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| 系統識別碼-Guid    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | 否                                                                                                                               |
| 是-單一值       | 是                                                                                                                                |
| 已編制索引             | 否                                                                                                                               |
| 在通用類別目錄中      | 否                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| 中使用的類別        | [**毫秒-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**毫秒-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | 否                                                                                                                               |
| 是-單一值       | 是                                                                                                                                |
| 已編制索引             | 否                                                                                                                               |
| 在通用類別目錄中      | 否                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| 中使用的類別        | [**毫秒-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**毫秒-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | 否                                                                                                                               |
| 是-單一值       | 是                                                                                                                                |
| 已編制索引             | 否                                                                                                                               |
| 在通用類別目錄中      | 否                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| 中使用的類別        | [**毫秒-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**毫秒-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | 否                                                                                                                               |
| 是-單一值       | 是                                                                                                                                |
| 已編制索引             | 否                                                                                                                               |
| 在通用類別目錄中      | 否                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| 中使用的類別        | [**毫秒-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**毫秒-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | 否                                                                                                                               |
| 是-單一值       | 是                                                                                                                                |
| 已編制索引             | 否                                                                                                                               |
| 在通用類別目錄中      | 否                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| 中使用的類別        | [**毫秒-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**毫秒-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | 否                                                                                                                               |
| 是-單一值       | 是                                                                                                                                |
| 已編制索引             | 否                                                                                                                               |
| 在通用類別目錄中      | 否                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| 中使用的類別        | [**毫秒-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**毫秒-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



 

 





