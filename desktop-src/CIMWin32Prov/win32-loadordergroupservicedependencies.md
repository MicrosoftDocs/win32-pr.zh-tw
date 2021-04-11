---
description: Win32 \_ LoadOrderGroupServiceDependencies 關聯 WMI 類別會將服務相依的基底服務和載入順序群組關聯至開始執行。
ms.assetid: 56739b80-9028-4a2e-85ed-973a078860c1
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceDependencies 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceDependencies
- Win32_LoadOrderGroupServiceDependencies.Antecedent
- Win32_LoadOrderGroupServiceDependencies.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b95d1aa01def951802434e787931ce348d04ccb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111365"
---
# <a name="win32_loadordergroupservicedependencies-class"></a>Win32 \_ LoadOrderGroupServiceDependencies 類別

**Win32 \_ LoadOrderGroupServiceDependencies** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會將服務相依的基底服務和載入順序群組關聯至開始執行。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceDependencies : CIM_Dependency
{
  Win32_LoadOrderGroup REF Antecedent;
  Win32_BaseService    REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ LoadOrderGroupServiceDependencies** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ LoadOrderGroupServiceDependencies** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LoadOrderGroup**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ LoadOrderGroup" ) 
</dt> </dl>

代表載入順序群組之屬性的實例的參考，該群組必須在這個類別的相依基底服務可以啟動之前啟動。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ BaseService**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 BaseService」 \_ ) 
</dt> </dl>

此實例的參考，代表相依于載入順序群組以開始執行的基底服務屬性。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ LoadOrderGroupServiceDependencies** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

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

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

