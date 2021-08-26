---
description: Win32 \_ OperatingSystemQFE 關聯 WMI 類別會將作業系統和套用的產品更新與 Win32 QuickFixEngineering 中的表示相關聯 \_ 。
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60fa11faaf7b6d85ce7d3494e1081afc4742b65e27f11fc2cebcd94949373745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972348"
---
# <a name="win32_operatingsystemqfe-class"></a>Win32 \_ OperatingSystemQFE 類別

**Win32 \_ OperatingSystemQFE** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將作業系統和套用的產品更新與 [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)中的表示相關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ OperatingSystemQFE** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ OperatingSystemQFE** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 作業系統**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ 作業系統" ) 
</dt> </dl>

代表此關聯中的產品更新所影響之系統的實例參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ QuickFixEngineering**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**弱**](../wmisdk/standard-qualifiers.md)式、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「WMI \| Win32 QuickFixEngineering」 \_ ) 
</dt> </dl>

代表在此關聯中套用至作業系統之物件實例的實例參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ OperatingSystemQFE** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

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

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
