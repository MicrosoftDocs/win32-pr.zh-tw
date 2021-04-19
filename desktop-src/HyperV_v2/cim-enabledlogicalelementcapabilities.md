---
description: 描述相關聯之 CIM EnabledLogicalElement 物件屬性的限制 \_ 。
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991868"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>CIM \_ EnabledLogicalElementCapabilities 類別

描述相關聯之 [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md) 物件屬性的限制。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>成員

**CIM \_ EnabledLogicalElementCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ EnabledLogicalElementCapabilities** 類別具有這些屬性。

<dl> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "FC-SWAPI。INCITS-T11 \| SWAPI \_ UNIT \_ CONFIG \_ CAPS \_ T \| EditName ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedElement**](cim-managedelement.md)。**ElementName**") 
</dt> </dl>

如果已啟用的邏輯元素的 **ElementName** 屬性可以修改，則 **為 true** ;否則 **為 false**。

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**") 
</dt> </dl>

正則運算式，指出 enable 邏輯專案之 **ElementName** 屬性的限制。 See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.

> [!Note]  
> 如果這個屬性和 enable 邏輯元素的 **ElementNameMask** 屬性描述 **ElementName** 的最大長度，則會使用較小的值。

 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**int32.maxvalue**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "FC-SWAPI。INCITS-T11 \| SWAPI \_ UNIT \_ CONFIG \_ CAPS \_ T \| MaxNameChars ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" cim \_ FCSwitchCapabilities. ElementNameEditSupported "，"**cim \_ EnabledLogicalElementCapabilities**.**ElementNameMask**") 
</dt> </dl>

已啟用之邏輯元素的 **ElementName** 屬性支援的最大長度。

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**」 ) 
</dt> </dl>

可由 [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) 方法在啟用的邏輯元素上要求的可能狀態。

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**已啟用** (2) 


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**停用** (3) 


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**關機** (4) 


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**離線** (6) 


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**測試** (7) 


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**延** 後 (8) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**靜止** (9) 


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**重新開機** (10) 


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**重設** (11) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 功能**](cim-capabilities.md)
</dt> </dl>

 

