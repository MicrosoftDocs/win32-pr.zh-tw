---
title: ms DS-SPN-尾碼屬性
description: 此屬性描述樹系中的伺服器所使用的 DNS 主機名稱尾碼。 這些 DNS 尾碼將與其他與此樹系有跨樹系信任的樹系共用。
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- ms DS-SPN-尾碼屬性 AD 架構
- SPNSuffixes 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c51a0805fefe9dbb8ddbeca3da89e3f5b3e66714b562af57cebc7975875cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544418"
---
# <a name="ms-ds-spn-suffixes-attribute"></a>ms DS-SPN-尾碼屬性

此屬性描述樹系中的伺服器所使用的 DNS 主機名稱尾碼。 這些 DNS 尾碼將與其他與此樹系有跨樹系信任的樹系共用。



| 進入 | 值 |
|-------------------|----------------------------------------------|
| CN                | ms DS-SPN-尾碼                           |
| Ldap-顯示名稱 | SPNSuffixes                             |
| 大小              | 255位元組                                    |
| 更新許可權  | 網域系統管理員                         |
| 更新頻率  | 當樹系中的伺服器取得新的尾碼時。 |
| Attribute-Id      | 1.2.840.113556.1.4.1715                      |
| 系統識別碼-Guid    | 789ee1eb-8c8e-4e4c-8cec-79b31b7617b5         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)  |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 否                                                         |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**交叉參考容器**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 否                                                         |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**交叉參考容器**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 否                                                         |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**交叉參考容器**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 否                                                         |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**交叉參考容器**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------------------------------------|
| 連結識別碼                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | 否                                                         |
| 是-單一值       | 否                                                         |
| 已編制索引             | 否                                                         |
| 在通用類別目錄中      | 否                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| 中使用的類別        | [**交叉參考容器**](c-crossrefcontainer.md)<br/> |



 

 





