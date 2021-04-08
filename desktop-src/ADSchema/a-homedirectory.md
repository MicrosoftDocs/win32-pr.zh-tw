---
title: Home-Directory 屬性
description: 帳戶的主目錄。
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Home-Directory 屬性 AD 架構
- homeDirectory 屬性 AD 架構
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687103"
---
# <a name="home-directory-attribute"></a>Home-Directory 屬性

帳戶的主目錄。 如果已設定 [**homeDrive**](a-homedrive.md) 並指定磁碟機號， **HOMEDIRECTORY** 必須是 UNC 路徑。 否則， **homeDirectory** 是完整的本機路徑，包括磁碟機號 (例如 *r ***： \\** _Directory_* _\\_ * _資料夾_) 。 這個值可以是 null 字串。



| 進入 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| Ldap-顯示名稱 | homeDirectory                                                                      |
| 大小              | \-                                                                                 |
| 更新許可權  | 網域系統管理員                                                               |
| 更新頻率  | 當使用者的記錄建立時，以及每次主目錄需要變更時。 |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| 系統識別碼-Guid    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                        |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 對                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | 否                                                                               |
| 是-單一值       | 對                                                                                |
| 已編制索引             | 否                                                                               |
| 在通用類別目錄中      | 否                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| 中使用的類別        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | 否                                                                               |
| 是-單一值       | 對                                                                                |
| 已編制索引             | 否                                                                               |
| 在通用類別目錄中      | 否                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| 中使用的類別        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | 否                                                                               |
| 是-單一值       | 對                                                                                |
| 已編制索引             | 否                                                                               |
| 在通用類別目錄中      | 否                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| 中使用的類別        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | 否                                                                               |
| 是-單一值       | 對                                                                                |
| 已編制索引             | 否                                                                               |
| 在通用類別目錄中      | 否                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| 中使用的類別        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





