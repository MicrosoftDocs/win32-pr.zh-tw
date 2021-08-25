---
description: Win32 \_ SystemSetting 抽象關聯 WMI 類別會關聯電腦系統和該系統上的一般設定。
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Win32_SystemSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c4ee9db2f48d02151c3874cc0ac5775f04e2d119ada972db09826dd1f791c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827788"
---
# <a name="win32_systemsetting-class"></a>Win32 \_ SystemSetting 類別

**Win32 \_ SystemSetting** 抽象關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會關聯電腦系統和該系統上的一般設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>成員

**Win32 \_ SystemSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SystemSetting** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) 
</dt> </dl>

代表可套用此設定之電腦系統屬性的實例參考。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 設定**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「設定」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| cim 設定」 \_ ) 
</dt> </dl>

實例的參考，代表可以套用至電腦系統之設定的屬性。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ SystemSetting** 類別衍生自 [**CIM \_ ElementSetting**](cim-elementsetting.md)。

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

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
