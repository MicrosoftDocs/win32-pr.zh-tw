---
description: 提供乙太網路交換器功能實例與資源的最小值、最大值、增量和預設設定之間的連結。
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Msvm_FeatureSettingsDefineCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983324"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a>Msvm \_ FeatureSettingsDefineCapabilities 類別

提供乙太網路交換器功能實例與資源的最小值、最大值、增量和預設設定之間的連結。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ FeatureSettingsDefineCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ FeatureSettingsDefineCapabilities** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 
</dt> </dl>

代表乙太網路交換器功能的 [**Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) 類別之實例的參考。 這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

代表資源設定之 [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) 類別實例的參考。 這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否將 **PartComponent** 的非 **Null**、非索引鍵屬性單獨處理，或視為相互關聯的集合。 例如，可能會定義一組獨立的最大屬性，但每個屬性之間並沒有關聯性。 另一方面，當每個屬性的最大值相依于其他部分時，可能需要定義數個相互關聯的最大屬性集合。

這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。

<dl> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**獨立** (0) 
</dt> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>相互 **關聯** 的 (1) 
</dt> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

表示對設定資料的所有非 **Null**、非索引鍵屬性的解讀進行進一步的語法。

下列值只會針對設定資料的非 **Null**、非索引鍵、非列舉、非布林值的數值屬性進行評估。 該集合的每個屬性都必須以數學方式與該屬性的其他實例比較。

這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。



| 值                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**點**</dt> <dt>0</dt> </dl>                     | 這個設定資料實例會提供一組值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <dt>**最低**</dt> <dt>1</dt> </dl>         | 這種設定資料提供評估屬性的最小值。 搭配 **PropertyPolicy** = "獨立" 使用時，必須為每個特定的設定資料實例只指定一種這類設定。 除非受限於相同屬性集的最大值，否則比較高於指定值的所有值也會被視為相關聯的功能實例所支援的值。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <dt></dt>最大<dt>2</dt> </dl>         | 這種設定資料提供評估屬性的最大值。 搭配 **PropertyPolicy** = "獨立" 使用時，必須為每個特定的設定資料實例只指定一種這類設定。 除非受限於相同屬性集的最小值，否則比較小於指定值的所有值也會被視為相關聯的功能實例所支援的值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <dt>**遞增**</dt> <dt>3</dt> </dl> | 這種設定資料會提供評估屬性的遞增值。 針對相關聯的功能，如果評估的屬性目前沒有對應的最小值或最大值，則屬性不會有任何影響。 否則，針對每個評估的屬性，其值 (*x*) 必須介於 *MinimumValue* 和 *MaximumValue* 之間（含），而且必須具有 *MaximumValue* 減 *x* 的結果和 *x* 減去 *MinimumValue* 的結果兩者都是 *遞增* 的整數倍數的屬性。 如果未指定 *MinimumValue* 或 *MaximumValue* ，而另一個是，則必須將遺漏值分別假設為屬性資料類型的最低或最高支援值。 此外，如果已針對評估的屬性指定 *MinimumValue* 和 *MaximumValue* ，則 *MaximumValue* 減去 *MinimumValue* 的結果必須是 *遞增* 的整數倍數。 <br/> |



 

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

針對設定資料之非 **Null**、非索引鍵屬性的解讀指定進一步的語法。 這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。



| 值                                                                                                                                                                                                                               | 意義                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**預設值**</dt> <dt>0</dt> </dl>         | 當針對功能由相關聯的功能定義的專案建立新的設定資料實例時，設定資料的屬性值將會當做預設值使用。 在設定資料的實例中，針對具有相同語義用途的特定屬性，最多隻能將這類設定資料實例指定為預設值。<br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <dt>**最佳**</dt> <dt>1</dt> </dl>         | 設定資料實例代表與相關聯的功能相關聯之元素的最佳設定值。 多個元件設定資料實例可能會宣告為最佳。<br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <dt>**平均**</dt> <dt>2</dt> </dl>                     | 關聯設定資料實例的非 **Null**、非索引鍵、非列舉、非布林值的數值屬性，代表沿著某個維度的平均點。 針對不同的設定資料屬性組合，可以將多個元件設定資料實例宣告為 **Mean**。 <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <dt>**支援**</dt>的 <dt>3</dt> </dl> | 設定資料的非 **Null**、非索引鍵屬性工作表示一組不合格的支援屬性值。 <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

