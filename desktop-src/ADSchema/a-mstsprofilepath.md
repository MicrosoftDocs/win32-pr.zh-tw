---
title: ms-TS-設定檔-Path 屬性
description: 終端機服務設定檔路徑指定當使用者登入終端機伺服器時，所要使用的漫遊或強制設定檔路徑。 設定檔路徑採用下列網路路徑格式： \\ \\ ServerName \\ ProfilesFolderName \\ UserName。
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- ms-TS-設定檔-Path 屬性 AD 架構
- msTSProfilePath 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ee0a712581bf122d3ee8bdb5a2c035a088008d6a0841c26fd0a0b9f3d90ecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924288"
---
# <a name="ms-ts-profile-path-attribute"></a>ms-TS-設定檔-Path 屬性

終端機服務設定檔路徑指定當使用者登入終端機伺服器時，所要使用的漫遊或強制設定檔路徑。 設定檔路徑採用下列網路路徑格式： **\\\\** _ServerName_ *_\\_* _ProfilesFolderName_ *_\\_* _UserName_。



| 進入 | 值 |
|-------------------|---------------------------------------------|
| CN                | ms-TS-Profile-Path                          |
| Ldap-顯示名稱 | msTSProfilePath                             |
| 大小              | \-                                          |
| 更新許可權  | \-                                          |
| 更新頻率  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1976                     |
| 系統識別碼-Guid    | e65c30db-316c-4060-a3a0-387b083f09cd        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>實作

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------|
| 連結識別碼                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | 否                             |
| 是-單一值       | 是                              |
| 已編制索引             | 否                             |
| 在通用類別目錄中      | 否                             |
| NT-Security-描述元 | O:BAG：不正確： S：                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| 中使用的類別        | [**User**](c-user.md)<br/> |



 

 





