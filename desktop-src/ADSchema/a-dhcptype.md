---
title: dhcp 類型屬性
description: DHCP 伺服器的類型。
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- dhcp 類型屬性 AD 架構
- dhcpType 屬性 AD 架構
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f4cc64a05db9b88d13a1e7dfb3ce0976391b9d2514388ae9045eb11d97a5b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049648"
---
# <a name="dhcp-type-attribute"></a>dhcp 類型屬性

DHCP 伺服器的類型。 這個屬性是在 objectClass [**dHCPClass**](c-dhcpclass.md)的所有物件上設定的。 它的值會定義物件的類型：

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| 進入 | 值 |
|-------------------|--------------------------------------------------------|
| CN                | dhcp 類型                                              |
| Ldap-顯示名稱 | dhcpType                                               |
| 大小              | 4 個位元組                                                |
| 更新許可權  | 網域系統管理員。                                  |
| 更新頻率  | 在樹系中新增或移除新的伺服器時。 |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| 系統識別碼-Guid    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
| Syntax            | [**列舉型別**](s-enumeration.md)                   |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 是                                         |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**DHCP 類別**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 是                                         |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**DHCP 類別**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 是                                         |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**DHCP 類別**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 是                                         |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**DHCP 類別**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 是                                         |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**DHCP 類別**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 是                                         |
| 已編制索引             | 是                                         |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**DHCP 類別**](c-dhcpclass.md)<br/> |



 

 





