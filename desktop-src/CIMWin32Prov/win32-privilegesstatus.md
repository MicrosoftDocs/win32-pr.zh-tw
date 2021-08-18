---
description: Win32 \_ PrivilegesStatus&\# 8194;WMI 類別會報告完成作業所需許可權的相關資訊。 當作業失敗或已傳回部分填入的實例時，可能會傳回它。
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: 'Win32_PrivilegesStatus 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e2c2b2329884b22eecdc00a629abb8d05bc87435ce06d35e51907cb4095c8fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020086"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a>Win32_PrivilegesStatus 類別 (CIMWin32 WMI 提供者) 

**Win32 \_ PrivilegesStatus** [WMI 類別](../wmisdk/retrieving-a-class.md)會報告完成作業所需許可權的相關資訊。 當作業失敗或已傳回部分填入的實例時，可能會傳回它。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>成員

**Win32 \_ PrivilegesStatus** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PrivilegesStatus** 類別具有這些屬性。

<dl> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述錯誤或操作狀態的任何使用者定義字串。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。

</dd> <dt>

**運算**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

發生失敗或異常時所發生的作業。 一般來說，Windows Management Instrumentation (wmi) 會將這個屬性設定為 wmi 方法的 COM API 名稱，如下所示： [**IWbemServices：： CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum)。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤或狀態變更所涉及的參數。 例如，如果應用程式嘗試取得不存在的類別，這個屬性會設定為違規的類別名稱。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| AccessControl \| Windows NT 許可權" ) 
</dt> </dl>

列出完成操作所缺少的必要存取權限。 您可以在 Windows 許可權下找到存取權限的類型。

範例：「SE \_ 關機 \_ 名稱」

</dd> <dt>

**PrivilegesRequired**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| AccessControl \| Windows NT 許可權" ) 
</dt> </dl>

列出執行作業所需的擁有權限。 這包括 **PrivilegesNotHeld** 屬性中的值。

範例：「SE \_ 關機 \_ 名稱」

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別導致或報告錯誤或狀態變更的提供者。 如果不牽涉到提供者，此字串會設定為「Windows 管理」。

這個屬性繼承自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

包含作業的錯誤或資訊代碼。 這可以是提供者所定義的任何值，但值 0 (零) 通常會保留以表示成功。

這個屬性繼承自 [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PrivilegesStatus** 類別衍生自 [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)。

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

[**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
