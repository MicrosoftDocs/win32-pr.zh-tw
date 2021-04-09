---
title: Extra-Columns 屬性
description: 這是一個多重值屬性，其值包含5個元組 (屬性名稱) 、 (資料行標題) 、 (預設可見度 (0、1) ) 、 (資料行寬度 ( \ 8211; 1 代表自動寬度) ) ，0 (保留供日後使用，則必須為零) 。
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Extra-Columns 屬性 AD 架構
- extraColumns 屬性 AD 架構
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103686867"
---
# <a name="extra-columns-attribute"></a>Extra-Columns 屬性

這是一個多重值屬性，其值包含5個元組： (的屬性名稱) 、 (的資料行標題) 、 (預設可見度 (0、1) ) 、 (資料行寬度 ( 1 表示自動寬度) ) 、0 (保留供日後使用，則必須為零) 。 [AD 使用者和電腦] 主控台會使用這個值。



| 進入 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| Ldap-顯示名稱 | extraColumns                                                                                                                                                         |
| 大小              | 每個值都是上述5個元組的字串大小。 根據預設，DisplaySpecifier 容器中的預設顯示物件上會有22個值。 |
| 更新許可權  | 網域系統管理員                                                                                                                                                 |
| 更新頻率  | 只有在已安裝 Exchange 之類的服務時，才會更新此項。                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| 系統識別碼-Guid    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------|
| 連結識別碼                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | 否                                                      |
| 是-單一值       | 否                                                      |
| 已編制索引             | 否                                                      |
| 在通用類別目錄中      | 否                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| 中使用的類別        | [**顯示規範**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------|
| 連結識別碼                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | 否                                                      |
| 是-單一值       | 否                                                      |
| 已編制索引             | 否                                                      |
| 在通用類別目錄中      | 否                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| 中使用的類別        | [**顯示規範**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------|
| 連結識別碼                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | 否                                                      |
| 是-單一值       | 否                                                      |
| 已編制索引             | 否                                                      |
| 在通用類別目錄中      | 否                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| 中使用的類別        | [**顯示規範**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------|
| 連結識別碼                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | 否                                                      |
| 是-單一值       | 否                                                      |
| 已編制索引             | 否                                                      |
| 在通用類別目錄中      | 否                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| 中使用的類別        | [**顯示規範**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------|
| 連結識別碼                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | 否                                                      |
| 是-單一值       | 否                                                      |
| 已編制索引             | 否                                                      |
| 在通用類別目錄中      | 否                                                      |
| NT-Security-描述元 | O:BAG：不正確： S：                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| 中使用的類別        | [**顯示規範**](c-displayspecifier.md)<br/> |



 

 





