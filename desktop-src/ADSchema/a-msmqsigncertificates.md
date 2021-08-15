---
title: MSMQ 簽署憑證屬性
description: 此屬性包含許多憑證。 使用者可以產生每台電腦的憑證。 我們也會針對每個憑證保留摘要。
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- MSMQ-簽署憑證屬性 AD 架構
- mSMQSignCertificates 屬性 AD 架構
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ee82a5a2bf64acc315dfb535ca6897261ef0cb26f5e249a8c8593cc492b53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081742"
---
# <a name="msmq-sign-certificates-attribute"></a>MSMQ 簽署憑證屬性

此屬性包含許多憑證。 使用者可以產生每台電腦的憑證。 我們也會針對每個憑證保留摘要。



| 進入 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| CN                | MSMQ-簽署憑證                                                                 |
| Ldap-顯示名稱 | mSMQSignCertificates                                                                   |
| 大小              | 屬性類型是 BLOB、大小不受限制，且資料會以我們自己的格式保存。 |
| 更新許可權  | \-                                                                                     |
| 更新頻率  | \-                                                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.947                                                                 |
| 系統識別碼-Guid    | 9a0dc33b-c100-11d1-bbc5-0080c76670c0                                                   |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                  |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | 否                                                                                         |
| 是-單一值       | 是                                                                                          |
| 已編制索引             | 否                                                                                         |
| 在通用類別目錄中      | 是                                                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| 中使用的類別        | [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | 否                                                                                         |
| 是-單一值       | 是                                                                                          |
| 已編制索引             | 否                                                                                         |
| 在通用類別目錄中      | 是                                                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| 中使用的類別        | [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | 否                                                                                         |
| 是-單一值       | 是                                                                                          |
| 已編制索引             | 否                                                                                         |
| 在通用類別目錄中      | 是                                                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| 中使用的類別        | [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | 否                                                                                         |
| 是-單一值       | 是                                                                                          |
| 已編制索引             | 否                                                                                         |
| 在通用類別目錄中      | 是                                                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| 中使用的類別        | [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | 否                                                                                         |
| 是-單一值       | 是                                                                                          |
| 已編制索引             | 否                                                                                         |
| 在通用類別目錄中      | 是                                                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| 中使用的類別        | [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**使用者**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | 否                                                                                         |
| 是-單一值       | 是                                                                                          |
| 已編制索引             | 否                                                                                         |
| 在通用類別目錄中      | 是                                                                                          |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| 中使用的類別        | [**MSMQ 遷移-使用者**](c-msmqmigrateduser.md)<br/> [**User**](c-user.md)<br/> |



 

 





