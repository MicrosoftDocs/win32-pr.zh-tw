---
title: ms-chap-已具現化-Nc 屬性
description: DS 複寫狀態資訊，類似于 (，以及) 現有屬性 hasMasterNCs 和 hasPartialReplicaNCs 的超集合。 供 KCC 在設定複寫夥伴時使用。
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- ms-chap-已具現化-Nc 屬性 AD 架構
- HasInstantiatedNCs 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efde9ef1cd9a7230e4493d3e542e1f5f661ed33027ad3e9a88ded9679df812c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804049"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>ms-chap-已具現化-Nc 屬性

DS 複寫狀態資訊，類似于 (，以及) 現有屬性 hasMasterNCs 和 hasPartialReplicaNCs 的超集合。 供 KCC 在設定複寫夥伴時使用。



| 進入 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-具現化-Nc                                                                                                                                                                                  |
| Ldap-顯示名稱 | HasInstantiatedNCs                                                                                                                                                                                     |
| 大小              | 4 個位元組                                                                                                                                                                                                     |
| 更新許可權  | 此值是由系統所設定。                                                                                                                                                                            |
| 更新頻率  | 大約兩倍的 hasMasterNCs/hasPartialReplicaNCs。 只有當 DC 新增或移除分割區時，才會更新這些現有的屬性 (例如，從 DC 變更為 GC 時，) 。 |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| 系統識別碼-Guid    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | 是                                     |
| 是-單一值       | 否                                    |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | 是                                     |
| 是-單一值       | 否                                    |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | 是                                     |
| 是-單一值       | 否                                    |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | 是                                     |
| 是-單一值       | 否                                    |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | 是                                     |
| 是-單一值       | 否                                    |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------|
| 連結識別碼                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | 是                                     |
| 是-單一值       | 否                                    |
| 已編制索引             | 否                                    |
| 在通用類別目錄中      | 否                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| 中使用的類別        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





