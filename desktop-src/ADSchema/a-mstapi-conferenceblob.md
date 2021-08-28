---
title: ms-TAPI-會議-Blob 屬性
description: 描述 TAPI 多播會議各項屬性之資料的二進位 BLOB。 其格式和內容是由相同物件中 Protocol-Id 屬性值所決定。 一般而言，此 BLOB 中的資料會符合 RFC2327。
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- ms-TAPI-會議-Blob 屬性 AD 架構
- msTAPI-ConferenceBlob 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51e7e8dc85b2de12bce4a520f9bd491d5c865037f56c1ae0cf43800fe2f4fe96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802788"
---
# <a name="ms-tapi-conference-blob-attribute"></a>ms-TAPI-會議-Blob 屬性

描述 TAPI 多播會議各項屬性之資料的二進位 BLOB。 其格式和內容是由相同物件中 Protocol-Id 屬性值所決定。 一般而言，此 BLOB 中的資料會符合 RFC2327。



| 進入 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| CN                | ms-TAPI-會議-Blob                                                                                      |
| Ldap-顯示名稱 | msTAPI-ConferenceBlob                                                                                        |
| 大小              | 可以是任意長度。                                                                                  |
| 更新許可權  | 不需要任何特殊許可權。                                                                              |
| 更新頻率  | 當會議的一些資料需要變更時，可能會因為 TAPI 會議擁有者而變更。 |
| Attribute-Id      | 1.2.840.113556.1.4.1700                                                                                      |
| 系統識別碼-Guid    | 4cc4601e-7201-4141-abc8-3e529ae88863                                                                         |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                        |



## <a name="implementations"></a>實作

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 是                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 是                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 是                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 是                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|-------------------------------------------------------------------|
| 連結識別碼                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | 否                                                             |
| 是-單一值       | 是                                                              |
| 已編制索引             | 否                                                             |
| 在通用類別目錄中      | 否                                                             |
| NT-Security-描述元 | O:BAG：不正確： S：                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| 中使用的類別        | [**ms-TAPI-Rt-會議**](c-mstapi-rtconference.md)<br/> |



 

 





