---
title: Domain-Component 屬性
description: 網域和 DNS 物件的命名屬性。 通常會顯示為 dc DomainName。
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Domain-Component 屬性 AD 架構
- dc 屬性 AD 架構
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe93b6629ac176452edbe5cdf13bf35afa955890cde369273f87990034bcd3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177764"
---
# <a name="domain-component-attribute"></a>Domain-Component 屬性

網域和 DNS 物件的命名屬性。 通常會顯示為 dc = DomainName。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| Ldap-顯示名稱 | dc                                          |
| 大小              | \-                                          |
| 更新許可權  | 網域系統管理員                        |
| 更新頻率  | 建立網域時。                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| 系統識別碼-Guid    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | 否                                                                                                                   |
| 是-單一值       | 是                                                                                                                    |
| 已編制索引             | 否                                                                                                                   |
| 在通用類別目錄中      | 是                                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| 中使用的類別        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-區域**](c-dnszone.md)<br/> [**域**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | 否                                                                                                                   |
| 是-單一值       | 是                                                                                                                    |
| 已編制索引             | 否                                                                                                                   |
| 在通用類別目錄中      | 是                                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| 中使用的類別        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-區域**](c-dnszone.md)<br/> [**域**](c-domain.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------------|
| 連結識別碼                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | 否                                 |
| 是-單一值       | 是                                  |
| 已編制索引             | 否                                 |
| 在通用類別目錄中      | 是                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| 中使用的類別        | [**域**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | 否                                                                                                                   |
| 是-單一值       | 是                                                                                                                    |
| 已編制索引             | 否                                                                                                                   |
| 在通用類別目錄中      | 是                                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| 中使用的類別        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-區域**](c-dnszone.md)<br/> [**域**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | 否                                                                                                                   |
| 是-單一值       | 是                                                                                                                    |
| 已編制索引             | 否                                                                                                                   |
| 在通用類別目錄中      | 是                                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| 中使用的類別        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-區域**](c-dnszone.md)<br/> [**域**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | 否                                                                                                                   |
| 是-單一值       | 是                                                                                                                    |
| 已編制索引             | 否                                                                                                                   |
| 在通用類別目錄中      | 是                                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| 中使用的類別        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-區域**](c-dnszone.md)<br/> [**域**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | 否                                                                                                                   |
| 是-單一值       | 是                                                                                                                    |
| 已編制索引             | 否                                                                                                                   |
| 在通用類別目錄中      | 是                                                                                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| 中使用的類別        | [**Dns-Node**](c-dnsnode.md)<br/> [**Dns-區域**](c-dnszone.md)<br/> [**域**](c-domain.md)<br/> |



 

 





