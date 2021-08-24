---
title: 知名物件屬性
description: 此屬性包含依 GUID 和辨別名稱的已知物件容器清單。
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- 知名物件屬性的 AD 架構
- wellKnownObjects 屬性 AD 架構
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5417b35ef821b1d84377c39eb4408eea57cf0dcc901ae0728a50ba48b88d6779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702408"
---
# <a name="well-known-objects-attribute"></a>知名物件屬性

此屬性包含依 GUID 和辨別名稱的已知物件容器清單。 已知的物件是系統容器。 這項資訊是用來在只使用 GUID 和功能變數名稱移動之後，用來取出物件。 當移動物件時，系統會自動更新參考物件之已知物件值的分辨名稱部分。 Ntdsapi 檔案包含下列定義，可用來取出物件 (與這些物件相關聯的 Guid 會包含在 Ntdsapi 中) ：

-   GUID \_ 使用者 \_ 容器 \_ W
-   GUID \_ COMPUTRS \_ 容器 \_ W
-   GUID \_ 系統 \_ 容器 \_ W
-   GUID \_ 域 \_ 控制器 \_ 容器 \_ W
-   GUID \_ 基礎結構 \_ 容器 \_ W
-   GUID \_ 刪除的 \_ 物件 \_ 容器 \_ W
-   GUID \_ LOSTANDFOUND \_ 容器 \_ W
-   GUID \_ FOREIGNSECURITYPRINCIPALS \_ 容器 \_ W
-   GUID \_ 程式 \_ 資料 \_ 容器 \_ W
-   GUID \_ MICROSOFT \_ 程式 \_ 資料 \_ 容器 \_ W
-   GUID \_ NTDS \_ 配額 \_ 容器 \_ W



| 進入 | 值 |
|-------------------|-------------------------------------------------|
| CN                | 知名物件                              |
| Ldap-顯示名稱 | wellKnownObjects                                |
| 大小              | \-                                              |
| 更新許可權  | 此值是由系統所設定。                |
| 更新頻率  | 每次移動其中一個系統容器時。 |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| 系統識別碼-Guid    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|---------------------------------|
| 連結識別碼                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | 是                            |
| 是-單一值       | 否                           |
| 已編制索引             | 否                           |
| 在通用類別目錄中      | 是                            |
| NT-Security-描述元 | O:BAG：不正確： S：                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| 中使用的類別        | [**返回頁首**](c-top.md)<br/> |



 

 





