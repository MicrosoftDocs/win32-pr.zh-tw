---
description: Win32 \_ PageFileSetting&\# 8194;WMI 類別代表分頁檔的設定。
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Win32_PageFileSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985590"
---
# <a name="win32_pagefilesetting-class"></a>Win32 \_ PageFileSetting 類別

**Win32 \_ PageFileSetting** [WMI 類別](../wmisdk/retrieving-a-class.md)代表分頁檔的設定。 從這個類別所具現化的物件內所包含的資訊會指定在系統啟動時建立檔案時所使用的分頁檔參數。 此類別中的屬性可以修改並延後到啟動。 這些設定與透過相關類別 [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)表示之分頁檔的執行時間狀態不同。

若要建立這個類別的實例，請啟用 **SeCreatePagefilePrivilege** 許可權。 如需詳細資訊，請參閱 [**許可權常數**](../wmisdk/privilege-constants.md) 和 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a>成員

**Win32 \_ PageFileSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PageFileSetting** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) 
</dt> </dl>

分頁檔案的初始大小。

範例：139

</dd> <dt>

**MaximumSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "mb" ) 
</dt> </dl>

分頁檔案的大小上限。

範例：178

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

分頁檔案的路徑和檔案名。

範例： "C： \\PAGEFILE.SYS"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PageFileSetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
