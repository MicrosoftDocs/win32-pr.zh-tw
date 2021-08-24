---
title: NT-Security-描述元屬性
description: 架構物件的 Windows NT 安全描述項。 安全描述項是一種資料結構，其中包含物件的安全性資訊，例如物件的擁有權和許可權。
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- NT-Security-描述元屬性 AD 架構
- nTSecurityDescriptor 屬性 AD 架構
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33b5753429b63638f1f1c9a3103aa8d78bd8590b77ceebec4fff05b82e10dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703008"
---
# <a name="nt-security-descriptor-attribute"></a>NT-Security-描述元屬性

架構物件的 Windows NT 安全描述項。 安全描述項是一種資料結構，其中包含物件的安全性資訊，例如物件的擁有權和許可權。

如需此值之格式的相關資訊，請參閱[ (Windows) 的安全描述項字串格式](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx)。



| 進入 | 值 |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-描述元                              |
| Ldap-顯示名稱 | nTSecurityDescriptor                                |
| 大小              | \-                                                  |
| 更新許可權  | \-                                                  |
| 更新頻率  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| 系統識別碼-Guid    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | 否                                                                                                                                              |
| 是-單一值       | 是                                                                                                                                               |
| 已編制索引             | 否                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | 否                                                                                                                                              |
| 是-單一值       | 是                                                                                                                                               |
| 已編制索引             | 否                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | 否                                                                                        |
| 是-單一值       | 是                                                                                         |
| 已編制索引             | 否                                                                                        |
| 在通用類別目錄中      | 是                                                                                         |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| 中使用的類別        | [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | 否                                                                                                                                              |
| 是-單一值       | 是                                                                                                                                               |
| 已編制索引             | 否                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | 否                                                                                                                                              |
| 是-單一值       | 是                                                                                                                                               |
| 已編制索引             | 否                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | 否                                                                                                                                              |
| 是-單一值       | 是                                                                                                                                               |
| 已編制索引             | 否                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 連結識別碼                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | 否                                                                                                                                              |
| 是-單一值       | 是                                                                                                                                               |
| 已編制索引             | 否                                                                                                                                              |
| 在通用類別目錄中      | 是                                                                                                                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| 中使用的類別        | [**Sam-網域-基礎**](c-samdomainbase.md)<br/> [**安全性-主體**](c-securityprincipal.md)<br/> [**返回頁首**](c-top.md)<br/> |



 

 





