---
title: Win32 \_ InstalledProgramFramework 類別
description: Win32 \_ InstalledProgramFramework 類別代表 win32 \_ InstalledWin32Program 實例編譯或在執行時間使用的技術架構。
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Win32_InstalledProgramFramework 類別應用程式和裝置清查提供者
- Win32_InstalledProgramFramework 類別應用程式和裝置清查提供者，說明
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
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
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917878"
---
# <a name="win32_installedprogramframework-class"></a>Win32 \_ InstalledProgramFramework 類別

**Win32 \_ InstalledProgramFramework** 類別代表 [**win32 \_ InstalledWin32Program**](win32-installedwin32program.md)實例編譯或在執行時間使用的技術架構。 此類別目前可以報告的架構為 OpenSSL、Visual Basic、Visual C++ .net、Visual C++、java (只會偵測 java 執行時間二進位檔) 和 CLR。

> [!Note]  
> 此類別可以偵測的架構集合可能會隨著時間更新。

 

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>成員

**Win32 \_ InstalledProgramFramework** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ InstalledProgramFramework** 類別具有這些屬性。

<dl> <dt>

**FrameworkName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

**ProgramId** 所識別的應用程式所依賴的架構名稱。

</dd> <dt>

**FrameworkPublisher**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

架構的發行者。

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

應用程式相依的 framework 版本。

</dd> <dt>

**FrameworkVersionActual**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

如果可以偵測到架構，應用程式在執行時間實際使用的架構版本。

</dd> <dt>

**IsPrivate**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果應用程式會組合架構的私用複本，則為 TRUE。

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

與 framework 資料相關聯之 [**Win32 \_ InstalledWin32Program**](win32-installedwin32program.md) 實例的唯一識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv mof</dt> </dl> |



 

 





