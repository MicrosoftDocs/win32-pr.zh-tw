---
title: Win32 \_ InstalledStoreProgram 類別
description: Win32 \_ InstalledStoreProgram 類別代表安裝的 Windows 存放區應用程式。
ms.assetid: 154c19c7-f2e5-48bd-b05b-3022e45f2aa4
keywords:
- Win32_InstalledStoreProgram 類別應用程式和裝置清查提供者
- Win32_InstalledStoreProgram 類別應用程式和裝置清查提供者，說明
topic_type:
- apiref
api_name:
- Win32_InstalledStoreProgram
- Win32_InstalledStoreProgram.ProgramId
- Win32_InstalledStoreProgram.Name
- Win32_InstalledStoreProgram.Vendor
- Win32_InstalledStoreProgram.Version
- Win32_InstalledStoreProgram.Language
- Win32_InstalledStoreProgram.Architecture
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 613baba9990da8403417aa4f8639ed7e9b5a7a5f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917882"
---
# <a name="win32_installedstoreprogram-class"></a>Win32 \_ InstalledStoreProgram 類別

**Win32 \_ InstalledStoreProgram** 類別代表安裝的 Windows 存放區應用程式。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_InstalledStoreProgram
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string Architecture;
};
```

## <a name="members"></a>成員

**Win32 \_ InstalledStoreProgram** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ InstalledStoreProgram** 類別具有這些屬性。

<dl> <dt>

**架構**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows 存放區應用程式支援的處理器架構。

</dd> <dt>

**Language**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows 存放區應用程式支援的語言。

</dd> <dt>

名稱
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows 存放區應用程式的名稱。

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

Windows 存放區應用程式的唯一識別碼。

</dd> <dt>

**廠商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows 存放區應用程式的發行者。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Windows 存放區應用程式的版本。

</dd> </dl>

## <a name="requirements"></a>規格需求



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv mof</dt> </dl> |



 

 





