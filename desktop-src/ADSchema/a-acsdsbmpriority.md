---
title: ACS-DSBM-Priority 屬性
description: 此屬性包含此子網路頻寬管理員 (SBM) 的優先順序。
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-Priority 屬性 AD 架構
- aCSDSBMPriority 屬性 AD 架構
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104108324"
---
# <a name="acs-dsbm-priority-attribute"></a>ACS-DSBM-Priority 屬性

此屬性包含此子網路頻寬管理員 (SBM) 的優先順序。 若需要選擇新的指定子網路頻寬管理員 (DSBM) ，此值會傳送至網域中的其他 SBMs，作為 DSBM 的 \_ 訊息。 具有最高優先順序的 SBM 會被選擇為新的 DSBM。



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-Priority                    |
| Ldap-顯示名稱 | aCSDSBMPriority                      |
| 大小              | 4 個位元組                              |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| 系統識別碼-Guid    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**ACS-子網**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**ACS-子網**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**ACS-子網**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**ACS-子網**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**ACS-子網**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|----------------------------------------------|
| 連結識別碼                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | 否                                        |
| 是-單一值       | 對                                         |
| 已編制索引             | 否                                        |
| 在通用類別目錄中      | 否                                        |
| NT-Security-描述元 | O:BAG：不正確： S：                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| 中使用的類別        | [**ACS-子網**](c-acssubnet.md)<br/> |



 

 





