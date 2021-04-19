---
description: 描述 WMI 的本機安裝。
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977990"
---
# <a name="__cimomidentification-class"></a>\_\_CIMOMIdentification 類別

**\_ \_ CIMOMIdentification** 系統類別描述 WMI 的本機安裝。 這是單一類別，只有一個實例。 **\_ \_ CIMOMIdentification** 類別僅適用于 **根目錄** 和 **根 \\ 預設** 命名空間。 使用者查詢實例以取得 WMI 安裝的相關資訊。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>成員

**\_ \_ CIMOMIdentification** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ CIMOMIdentification** 類別具有這些屬性。

<dl> <dt>

**SetupDateTime**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安裝的日期和時間。 第一次安裝作業系統之後，這個屬性是空的。

如果 WMI 存放庫已刪除，然後再次建立，則此屬性會包含重新建立存放庫的日期和時間。

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實際映射的版本，其中包含建立通用訊息模型 (CIM) 儲存機制的 WMI 服務。 由於存放庫格式可能會在 WMI 版本之間變更，因此，此屬性可讓未來的 WMI 升級判斷是否必須升級資料庫。 其格式為：

"1.00.183.0000"

其中第一個數位是主要版本，接下來的兩個數字是次要版本，而接下來的三個數字則是組建編號。 不使用剩餘的數位。

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出實際映射的版本，其中包含建立 CIM 儲存機制的 WMI 服務。 由於存放庫格式可能會在 WMI 版本之間變更，因此，此屬性可讓未來的 WMI 升級判斷是否必須升級資料庫。 其格式為：

"1.00.183.0000"

其中第一個數位是主要版本，接下來的兩個數字是次要版本，而接下來的三個數字則是組建編號。 不使用剩餘的數位。

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

安裝目錄。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ CIMOMIdentification** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)，但沒有屬性。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例說明如何顯示 CIM 物件模型識別資訊，並取自 \\ \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ sysmgmt \\ wmi \\ 腳本的範例目錄。


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



下列 Perl 程式碼範例說明如何顯示 CIM 物件模型識別資訊，並取自 \\ \\ 程式檔 \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ \\ sysmgmt \\ wmi \\ 腳本範例目錄。


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | Root<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

