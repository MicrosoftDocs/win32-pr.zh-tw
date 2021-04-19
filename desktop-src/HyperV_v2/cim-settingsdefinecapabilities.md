---
description: 代表 CIM \_ SettingData 實例和 cim 功能實例的屬性之間的關聯 \_ 。
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: CIM_SettingsDefineCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980549"
---
# <a name="cim_settingsdefinecapabilities-class"></a>CIM \_ SettingsDefineCapabilities 類別

代表 [**cim \_ SettingData**](cim-settingdata.md) 實例和 [**cim \_ 功能**](cim-capabilities.md) 實例的屬性之間的關聯。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>成員

**CIM \_ SettingsDefineCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SettingsDefineCapabilities** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 功能**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

[**CIM \_ 功能**](cim-capabilities.md)實例的參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

用來定義 [**cim \_ 功能**](cim-capabilities.md)實例之 [**cim \_ SettingData**](cim-settingdata.md)實例的參考。

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SettingsDefineCapabilities**.**ValueRole**"，"**CIM \_ SettingsDefineCapabilities**.**ValueRange**") 
</dt> </dl>

指出相關聯之 [**CIM \_ SettingData**](cim-settingdata.md) 實例的非 null、非索引鍵屬性是獨立處理或關聯的集合。 比方說，當每個屬性之間沒有任何關聯性時，可能會定義一組獨立的最大屬性。 相反地，當每個屬性的最大值相依于其他部分時，可能需要定義數個相關的最大屬性集合。

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**獨立** (0) 


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

相互 **關聯** 的 (1) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**"，"**CIM \_ SettingsDefineCapabilities**.**ValueRole**") 
</dt> </dl>

指出 [**CIM \_ SettingData**](cim-settingdata.md) 實例的非 null、非索引鍵屬性所使用的值範圍類型。

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**點** (0) 


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**最低** (1) 


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

最 **大 (2**) 


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

 (3) **遞增**


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**"，"**CIM \_ SettingsDefineCapabilities**.**ValueRange**") 
</dt> </dl>

[**CIM \_ SettingData**](cim-settingdata.md)實例的非 null、非索引鍵屬性之解釋的額外語義。

「預設」表示建立新的 SettingData 實例，針對其功能由相關聯的功能實例定義的專案時，將會使用此元件的屬性值做為預設值。

在不同的 settingdata 實例上，針對具有相同語義用途的特定屬性，最多隻能指定一個此類的 settingdata 實例作為預設值。

「最佳」表示在與相關聯的功能實例相關聯的元素中，使用最適合的設定值。 可以將多個元件的 SettingData 實例宣告為最佳。」Mean "表示相關聯的 SettingData 實例的非 null、非索引鍵、非列舉、非布林值的數值屬性，代表沿著某個維度的平均點。 針對不同的 SettingData 屬性組合，可以將多個元件的 SettingData 實例宣告為「Mean」。 「支援」表示元件 SettingData 實例的非 null、非索引鍵屬性工作表示一組不具限定的支援屬性值。

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**預設** (0) 


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**最佳** (1) 


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Mean** (2) 


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**支援** (3) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


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

[**CIM \_ 元件**](cim-component.md)
</dt> </dl>

 

