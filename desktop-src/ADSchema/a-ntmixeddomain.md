---
title: NT-混合網域屬性
description: 指出網域處於原生模式或混合模式。 這個屬性是在網域的 domainDNS (head) 物件中找到。
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- NT-Mixed-Domain attribute AD 架構
- nTMixedDomain 屬性 AD 架構
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971891"
---
# <a name="nt-mixed-domain-attribute"></a>NT-混合網域屬性

指出網域處於原生模式或混合模式。 這個屬性是在網域的 domainDNS (head) 物件中找到。



| 進入 | 值 |
|-------------------|---------------------------------------|
| CN                | NT-混合網域                       |
| Ldap-顯示名稱 | nTMixedDomain                         |
| 大小              | 4個位元組。 混合模式1，原生模式0。 |
| 更新許可權  | \-                                    |
| 更新頻率  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| 系統識別碼-Guid    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
| Syntax            | [**列舉型別**](s-enumeration.md)  |



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
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | 否                                                                                   |
| 是-單一值       | 對                                                                                    |
| 已編制索引             | 否                                                                                   |
| 在通用類別目錄中      | 否                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | 否                                                                                   |
| 是-單一值       | 對                                                                                    |
| 已編制索引             | 否                                                                                   |
| 在通用類別目錄中      | 否                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | 否                                                                                   |
| 是-單一值       | 對                                                                                    |
| 已編制索引             | 否                                                                                   |
| 在通用類別目錄中      | 否                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | 否                                                                                   |
| 是-單一值       | 對                                                                                    |
| 已編制索引             | 否                                                                                   |
| 在通用類別目錄中      | 否                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | 否                                                                                   |
| 是-單一值       | 對                                                                                    |
| 已編制索引             | 否                                                                                   |
| 在通用類別目錄中      | 否                                                                                   |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| 中使用的類別        | [**交叉參考**](c-crossref.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> |



 

 





