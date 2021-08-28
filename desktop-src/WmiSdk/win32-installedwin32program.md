---
title: Win32 \_ InstalledWin32Program 類別
description: Win32 \_ InstalledWin32Program 類別代表已安裝的 win32 應用程式。
ms.assetid: 2eef00da-8597-4852-b4fb-4276d05fd724
keywords:
- Win32_InstalledWin32Program 類別應用程式和裝置清查提供者
- Win32_InstalledWin32Program 類別應用程式和裝置清查提供者，說明
topic_type:
- apiref
api_name:
- Win32_InstalledWin32Program
- Win32_InstalledWin32Program.ProgramId
- Win32_InstalledWin32Program.Name
- Win32_InstalledWin32Program.Vendor
- Win32_InstalledWin32Program.Version
- Win32_InstalledWin32Program.Language
- Win32_InstalledWin32Program.MsiPackageCode
- Win32_InstalledWin32Program.MsiProductCode
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
ms.openlocfilehash: 51cfbf56591bca71f8364d97a9a4adb0d995c4c3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917880"
---
# <a name="win32_installedwin32program-class"></a>Win32 \_ InstalledWin32Program 類別

**Win32 \_ InstalledWin32Program** 類別代表已安裝的 win32 應用程式。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Win32_InstalledWin32Program
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string MsiPackageCode;
  string MsiProductCode;
};
```

## <a name="members"></a>成員

**Win32 \_ InstalledWin32Program** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ InstalledWin32Program** 類別具有這些屬性。

<dl> <dt>

**Language**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已安裝的 Win32 應用程式所支援的語言。

</dd> <dt>

**MsiPackageCode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

MSI 封裝程式碼，如果 Win32 應用程式是使用 MSI 安裝的。

</dd> <dt>

**MsiProductCode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

MSI 產品代碼，如果 Win32 應用程式是使用 MSI 安裝的。

</dd> <dt>

名稱
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已安裝的 Win32 應用程式名稱。

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

已安裝之 Win32 應用程式的唯一識別碼。 此值有助於將 **win32 \_ InstalledWin32Program** 與 [**win32 \_ InstalledProgramFramework**](win32-installedprogramframework.md)相互關聯。

</dd> <dt>

**廠商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已安裝之 Win32 應用程式的發行者。

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已安裝之 Win32 應用程式的版本。

</dd> </dl>

## <a name="requirements"></a>規格需求



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv mof</dt> </dl> |



 

 





