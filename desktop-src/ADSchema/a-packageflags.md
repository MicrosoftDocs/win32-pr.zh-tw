---
title: Package-Flags 屬性
description: 包含應用程式之部署狀態旗標的位位。
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Package-Flags 屬性 AD 架構
- packageFlags 屬性 AD 架構
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7202124bdeac22347d727638dc564a145599e9c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103687163"
---
# <a name="package-flags-attribute"></a>Package-Flags 屬性

包含應用程式之部署狀態旗標的位位。

這個屬性可以是零或一或多個下列值的組合。

| 值                 | 描述                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | 在指派之前，必須先卸載此應用程式的非受控版本。 **WINDOWS XP SP1 和更新版本：** 不支援此旗標。<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | 這是已發行的應用程式。<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | 這個套件是在 Windows 2000 的 Beta 3 之後部署的。<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | 您可以使用主控台的 [ **新增或移除程式** ] 功能來安裝此應用程式。<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | 您可以視需要自動安裝此應用程式。<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | 此應用程式是孤立的。 如果系統管理員從可部署的應用程式清單中移除應用程式，則已發佈的應用程式可能會變成孤立。<br/>                                                                                                                                    |
| 0x00000100<br/> | 此應用程式應視為已卸載。<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | 此應用程式僅供試驗之用。<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | 這是指派的應用程式。 使用者無法完全移除指派的應用程式。 如果使用者嘗試使用主控台的 [ **新增或移除程式** ] 功能來卸載應用程式，則在移除完成時，應用程式將會重新公告至電腦。<br/> |
| 0x00000800<br/> | 移除原則時，此應用程式是孤立的。 如果系統管理員移除與此應用程式相關的原則，系統管理員將不再控制應用程式的部署，但已安裝的應用程式將會繼續運作。<br/>                          |
| 0x00001000<br/> | 移除部署原則時，就會卸載此應用程式。<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | 將會執行使用者指派應用程式的完整安裝。<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | 此應用程式的舊版本必須升級為此版本。<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | 此套件僅支援最基本的使用者介面，並提供安裝程式的進度列。<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | 這是32位版 Windows 的套件，不應該在 Windows XP Professional x64 Edition 或64位版本的 Windows Server 2003 上執行。<br/>                                                                                                                                      |
| 0x00020000<br/> | 此封裝適用于任何語言。<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | 此封裝已升級。<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | 此套件具有安裝程式的完整使用者介面。<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | 如果在網域重新命名中重新部署應用程式，則會在重新部署作業期間保留此應用程式的類別。<br/>                                                                                                                                                                       |



 



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| Ldap-顯示名稱 | packageFlags                         |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| 系統識別碼-Guid    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
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
|------------------------|------------------------------------------------------------------|
| 連結識別碼                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | 否                                                            |
| 是-單一值       | 對                                                             |
| 已編制索引             | 對                                                             |
| 在通用類別目錄中      | 否                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| 中使用的類別        | [**套件-註冊**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|------------------------|------------------------------------------------------------------|
| 連結識別碼                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | 否                                                            |
| 是-單一值       | 對                                                             |
| 已編制索引             | 對                                                             |
| 在通用類別目錄中      | 否                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| 中使用的類別        | [**套件-註冊**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------|
| 連結識別碼                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | 否                                                            |
| 是-單一值       | 對                                                             |
| 已編制索引             | 對                                                             |
| 在通用類別目錄中      | 否                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| 中使用的類別        | [**套件-註冊**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|------------------------|------------------------------------------------------------------|
| 連結識別碼                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | 否                                                            |
| 是-單一值       | 對                                                             |
| 已編制索引             | 對                                                             |
| 在通用類別目錄中      | 否                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| 中使用的類別        | [**套件-註冊**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|------------------------|------------------------------------------------------------------|
| 連結識別碼                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | 否                                                            |
| 是-單一值       | 對                                                             |
| 已編制索引             | 對                                                             |
| 在通用類別目錄中      | 否                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| 中使用的類別        | [**套件-註冊**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|------------------------|------------------------------------------------------------------|
| 連結識別碼                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | 否                                                            |
| 是-單一值       | 對                                                             |
| 已編制索引             | 對                                                             |
| 在通用類別目錄中      | 否                                                            |
| NT-Security-描述元 | O:BAG：不正確： S：                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| 中使用的類別        | [**套件-註冊**](c-packageregistration.md)<br/> |



 

 





