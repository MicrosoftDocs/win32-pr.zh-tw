---
title: 應用程式架構版本屬性
description: 這個屬性會儲存類別存放區的架構版本。 它是用來在架構變更之間提供正確的行為。
ms.assetid: e8c2ab2b-1b7f-4d4f-b9ea-4116a8e30277
ms.tgt_platform: multiple
keywords:
- 應用程式架構版本屬性 AD 架構
- appSchemaVersion 屬性 AD 架構
topic_type:
- apiref
api_name:
- App-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db892ebaa613cf95c016162e12ee3f9de0a101e433a73aa203640be8645f0ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081982"
---
# <a name="app-schema-version-attribute"></a>應用程式架構版本屬性

這個屬性會儲存類別存放區的架構版本。 它是用來在架構變更之間提供正確的行為。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | 應用程式架構版本                   |
| Ldap-顯示名稱 | appSchemaVersion                     |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.848               |
| 系統識別碼-Guid    | 96a7dd65-9118-11d1-aebc-0000f80367c1 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|------------------------------------------------|
| 連結識別碼                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | 否                                          |
| 是-單一值       | 是                                           |
| 已編制索引             | 否                                          |
| 在通用類別目錄中      | 否                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| 中使用的類別        | [**類別存放區**](c-classstore.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| 中使用的類別        | [**應用程式版本**](c-applicationversion.md)<br/> [**類別存放區**](c-classstore.md)<br/> [**服務-連接點**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| 中使用的類別        | [**應用程式版本**](c-applicationversion.md)<br/> [**類別存放區**](c-classstore.md)<br/> [**服務-連接點**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| 中使用的類別        | [**應用程式版本**](c-applicationversion.md)<br/> [**類別存放區**](c-classstore.md)<br/> [**服務-連接點**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| 中使用的類別        | [**應用程式版本**](c-applicationversion.md)<br/> [**類別存放區**](c-classstore.md)<br/> [**服務-連接點**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| 中使用的類別        | [**應用程式版本**](c-applicationversion.md)<br/> [**類別存放區**](c-classstore.md)<br/> [**服務-連接點**](c-serviceconnectionpoint.md)<br/> |



 

 





