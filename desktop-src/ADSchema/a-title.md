---
title: Title 屬性
description: 包含使用者職稱。 這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。 它通常不會用於尾碼標題（例如 Esq）。 或 DDS。
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Title 屬性 AD 架構
- title 屬性 AD 架構
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8885a557e8fbec17d6d58d68fdea0f99039f0e09e34a8da01954dc7b4979fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645028"
---
# <a name="title-attribute-ad-schema"></a>標題屬性 (AD 架構) 

包含使用者職稱。 這個屬性通常用來指出正式的職稱，例如資深程式設計師，而非 occupational 類別，例如程式設計師。 它通常不會用於尾碼標題（例如 Esq）。 或 DDS。



| 進入 | 值 |
|-------------------|---------------------------------------------------------------------------|
| CN                | 標題                                                                     |
| Ldap-顯示名稱 | title                                                                     |
| 大小              | \-                                                                        |
| 更新許可權  | 網域系統管理員或帳戶擁有者。                                    |
| 更新頻率  | 當使用者的記錄建立時，以及每次需要變更標題時。 |
| Attribute-Id      | 2.5.4.12                                                                  |
| 系統識別碼-Guid    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | 否                                                                                                                           |
| 是-單一值       | 是                                                                                                                            |
| 已編制索引             | 否                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | 否                                                                                                                           |
| 是-單一值       | 是                                                                                                                            |
| 已編制索引             | 否                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | 否                                                                                                                           |
| 是-單一值       | 是                                                                                                                            |
| 已編制索引             | 否                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | 否                                                                                                                           |
| 是-單一值       | 是                                                                                                                            |
| 已編制索引             | 否                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | 否                                                                                                                           |
| 是-單一值       | 是                                                                                                                            |
| 已編制索引             | 否                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | 否                                                                                                                           |
| 是-單一值       | 是                                                                                                                            |
| 已編制索引             | 否                                                                                                                           |
| 在通用類別目錄中      | 否                                                                                                                           |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| 中使用的類別        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**居住人**](c-residentialperson.md)<br/> |



 

 





