---
title: 支援 ms DS-加密類型屬性
description: 使用者、電腦或信任帳戶所支援的加密演算法。請注意，KDC 會在產生此帳戶的服務票證時使用此資訊。
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- 支援的 ms DS-加密類型屬性 AD 架構
- '>msds-supportedencryptiontypes 屬性 AD 架構'
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106971265"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>支援 ms DS-加密類型屬性

使用者、電腦或信任帳戶支援的加密演算法。

> [!Note]  
> KDC 在產生此帳戶的服務票證時使用此資訊。 服務與電腦可以在 Active Directory 中的個別帳戶上自動更新此屬性，因此需要此屬性的寫入權限。

 



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | 支援的 ms DS-加密類型     |
| Ldap-顯示名稱 | msDS-SupportedEncryptionTypes        |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| 系統識別碼-Guid    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | 否                                                                                  |
| 是-單一值       | 對                                                                                   |
| 已編制索引             | 否                                                                                  |
| 在通用類別目錄中      | 否                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | 否                                                                                  |
| 是-單一值       | 對                                                                                   |
| 已編制索引             | 否                                                                                  |
| 在通用類別目錄中      | 否                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | 否                                                                                  |
| 是-單一值       | 對                                                                                   |
| 已編制索引             | 否                                                                                  |
| 在通用類別目錄中      | 否                                                                                  |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| 中使用的類別        | [**信任網域**](c-trusteddomain.md)<br/> [**User**](c-user.md)<br/> |



 

 





