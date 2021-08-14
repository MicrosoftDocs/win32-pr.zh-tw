---
title: Address-Type 屬性
description: 描述使用者位址格式的字元字串。 網址類別型會對應至位址格式。 也就是說，藉由查看收件者的網址類別型，用戶端應用程式可以決定如何格式化適合收件者的位址。
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Address-Type 屬性 AD 架構
- addressType 屬性 AD 架構
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2ce0ff9651350803a05b3b3bf3dda663419c9948617b706688bf78057ad72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118688485"
---
# <a name="address-type-attribute"></a>Address-Type 屬性

描述使用者位址格式的字元字串。 網址類別型會對應至位址格式。 也就是說，藉由查看收件者的網址類別型，用戶端應用程式可以決定如何格式化適合收件者的位址。



| 進入 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| CN                | Address-Type                                                                                                              |
| Ldap-顯示名稱 | addressType                                                                                                               |
| 大小              | 網址類別型：3COM、ATT、CCMAIL、COMPUSERVE、EX、FAX、MSFAX、MCI、MHS、MS、MSA、MSN、PROFS、SMTP、SNADS、電傳、X400、X500 |
| 更新許可權  | 此值是由系統所設定。                                                                                          |
| 更新頻率  | 在建立物件時設定。                                                                                           |
| Attribute-Id      | 1.2.840.113556.1.2.350                                                                                                    |
| 系統識別碼-Guid    | 5fd42464-1262-11d0-a060-00aa006c33ed                                                                                      |
| Syntax            | [**String(Teletex)**](s-string-teletex.md)                                                                               |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|----------------------------------------------------------|
| 連結識別碼                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | 否                                                    |
| 是-單一值       | 是                                                     |
| 已編制索引             | 否                                                    |
| 在通用類別目錄中      | 否                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| 中使用的類別        | [**位址範本**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------------|
| 連結識別碼                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | 否                                                    |
| 是-單一值       | 是                                                     |
| 已編制索引             | 否                                                    |
| 在通用類別目錄中      | 否                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| 中使用的類別        | [**位址範本**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------|
| 連結識別碼                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | 否                                                    |
| 是-單一值       | 是                                                     |
| 已編制索引             | 否                                                    |
| 在通用類別目錄中      | 否                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| 中使用的類別        | [**位址範本**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------|
| 連結識別碼                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | 否                                                    |
| 是-單一值       | 是                                                     |
| 已編制索引             | 否                                                    |
| 在通用類別目錄中      | 否                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| 中使用的類別        | [**位址範本**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------|
| 連結識別碼                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | 否                                                    |
| 是-單一值       | 是                                                     |
| 已編制索引             | 否                                                    |
| 在通用類別目錄中      | 否                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| 中使用的類別        | [**位址範本**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------|
| 連結識別碼                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | 否                                                    |
| 是-單一值       | 是                                                     |
| 已編制索引             | 否                                                    |
| 在通用類別目錄中      | 否                                                    |
| NT-Security-描述元 | O:BAG：不正確： S：                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| 中使用的類別        | [**位址範本**](c-addresstemplate.md)<br/> |



 

 





