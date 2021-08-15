---
title: " (AD 架構) 的 Description 屬性"
description: 包含要針對物件顯示的描述。 在某些情況下，此值會限制為單一值，以提供回溯相容性，但在其他情況下允許多重值。 請參閱＜備註＞。
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Description 屬性 AD 架構
- description 屬性 AD 架構
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f53c344b026a89a3f579d1eb7fc7002a8a0410d28fd9b43d05882a4285eb73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961726"
---
# <a name="description-attribute-ad-schema"></a> (AD 架構) 的 Description 屬性

包含要針對物件顯示的描述。 在某些情況下，此值會限制為單一值，以提供回溯相容性，但在其他情況下允許多重值。 請參閱＜備註＞。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | Description                                 |
| Ldap-顯示名稱 | description                                 |
| 大小              | \-                                          |
| 更新許可權  | 網域系統管理員或帳戶擁有者。      |
| 更新頻率  | 當描述需要變更時。   |
| Attribute-Id      | 2.5.4.13                                    |
| 系統識別碼-Guid    | bf967950-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | 否                                                                        |
| 是-單一值       | 否                                                                        |
| 已編制索引             | 否                                                                        |
| 在通用類別目錄中      | 是                                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| 中使用的類別        | [**Sam-網域**](c-samdomain.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | 否                                                                                                                                      |
| 是-單一值       | 否                                                                                                                                      |
| 已編制索引             | 否                                                                                                                                      |
| 在通用類別目錄中      | 是                                                                                                                                       |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| 中使用的類別        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | 否                           |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 中使用的類別        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**返回頁首**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 中使用的類別        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**返回頁首**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 中使用的類別        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**返回頁首**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 是-單一值       | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 已編制索引             | 否                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 中使用的類別        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-網域**](c-samdomain.md)<br/> [**返回頁首**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>備註

在允許的情況下，description 屬性會實作為架構中的多重值屬性。 對於不是 SAM managed 類別的物件，描述是多重值。 如果是 SAM managed 類別的屬性，description 屬性是單一值。 SAM managed 類別適用于安全性主體之類的事項，因此，如果您擁有容器或自己的類別，則架構可讓您使用多個值。 Description 屬性的行為是為了與舊版作業系統回溯相容，因為在 AD 存在之前，屬性會存在於 SAM Api 中。

 

 





