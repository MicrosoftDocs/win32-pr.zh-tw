---
title: Pwd-Properties 屬性
description: 密碼屬性。 網域原則的一部分。 用來表示複雜性和儲存限制的位位。
ms.assetid: 9d73595f-508f-4562-a928-4833df977ab3
ms.tgt_platform: multiple
keywords:
- Pwd-Properties 屬性 AD 架構
- pwdProperties 屬性 AD 架構
topic_type:
- apiref
api_name:
- Pwd-Properties
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03595e219fdc5d204ba1c730cd7a1063f2ea018b25bd2a5872778879ecc4f5f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118011612"
---
# <a name="pwd-properties-attribute"></a>Pwd-Properties 屬性

密碼屬性。 網域原則的一部分。 用來表示複雜性和儲存限制的位位。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Pwd-Properties                                                                                                                                                                                                           |
| Ldap-顯示名稱 | pwdProperties                                                                                                                                                                                                            |
| 大小              | 整數。 網域 \_ 密碼 \_ 複雜1，網域 \_ 密碼 \_ 無 \_ ANON \_ 變更2，網域 \_ 密碼 \_ 無 \_ 明確 \_ 變更4，網域 \_ 鎖定 \_ 管理員8，網域 \_ 密碼 \_ 存放區 \_ 明文16，網域 \_ 拒絕 \_ 密碼 \_ 變更32 |
| 更新許可權  | 網域系統管理員                                                                                                                                                                                                     |
| 更新頻率  | 當使用者的原則變更時。                                                                                                                                                                                      |
| Attribute-Id      | 1.2.840.113556.1.4.93                                                                                                                                                                                                    |
| 系統識別碼-Guid    | bf967a0b-0de6-11d0-a285-00aa003049e2                                                                                                                                                                                     |
| Syntax            | [**列舉型別**](s-enumeration.md)                                                                                                                                                                                     |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | 否                                                                                                                                                 |
| 是-單一值       | 是                                                                                                                                                  |
| 已編制索引             | 否                                                                                                                                                 |
| 在通用類別目錄中      | 否                                                                                                                                                 |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| 中使用的類別        | [**網域原則**](c-domainpolicy.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**Sam-網域-基礎**](c-samdomainbase.md)<br/> |



 

 





