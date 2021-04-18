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
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="42711-103">Msvm \_ FeatureSettingsDefineCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="42711-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="42711-104">提供乙太網路交換器功能實例與資源的最小值、最大值、增量和預設設定之間的連結。</span><span class="sxs-lookup"><span data-stu-id="42711-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="42711-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="42711-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42711-106">語法</span><span class="sxs-lookup"><span data-stu-id="42711-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="42711-107">成員</span><span class="sxs-lookup"><span data-stu-id="42711-107">Members</span></span>

<span data-ttu-id="42711-108">**Msvm \_ FeatureSettingsDefineCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42711-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="42711-109">屬性</span><span class="sxs-lookup"><span data-stu-id="42711-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42711-110">屬性</span><span class="sxs-lookup"><span data-stu-id="42711-110">Properties</span></span>

<span data-ttu-id="42711-111">**Msvm \_ FeatureSettingsDefineCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42711-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42711-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="42711-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42711-113">資料類型： **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="42711-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="42711-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42711-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42711-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) </span><span class="sxs-lookup"><span data-stu-id="42711-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="42711-116">代表乙太網路交換器功能的 [**Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) 類別之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="42711-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="42711-117">這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。</span><span class="sxs-lookup"><span data-stu-id="42711-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="42711-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="42711-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42711-119">資料類型： **[ **Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="42711-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="42711-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42711-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42711-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="42711-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="42711-122">代表資源設定之 [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) 類別實例的參考。</span><span class="sxs-lookup"><span data-stu-id="42711-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="42711-123">這個屬性繼承自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。</span><span class="sxs-lookup"><span data-stu-id="42711-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="42711-124">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="42711-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42711-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="42711-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42711-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42711-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42711-127">指定是否將 **PartComponent** 的非 **Null**、非索引鍵屬性單獨處理，或視為相互關聯的集合。</span><span class="sxs-lookup"><span data-stu-id="42711-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="42711-128">例如，可能會定義一組獨立的最大屬性，但每個屬性之間並沒有關聯性。</span><span class="sxs-lookup"><span data-stu-id="42711-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="42711-129">另一方面，當每個屬性的最大值相依于其他部分時，可能需要定義數個相互關聯的最大屬性集合。</span><span class="sxs-lookup"><span data-stu-id="42711-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="42711-130">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="42711-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="42711-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**獨立** (0) </span><span class="sxs-lookup"><span data-stu-id="42711-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42711-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>相互 **關聯** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="42711-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="42711-133">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="42711-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42711-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="42711-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42711-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42711-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42711-136">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="42711-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42711-137">表示對設定資料的所有非 **Null**、非索引鍵屬性的解讀進行進一步的語法。</span><span class="sxs-lookup"><span data-stu-id="42711-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="42711-138">下列值只會針對設定資料的非 **Null**、非索引鍵、非列舉、非布林值的數值屬性進行評估。</span><span class="sxs-lookup"><span data-stu-id="42711-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="42711-139">該集合的每個屬性都必須以數學方式與該屬性的其他實例比較。</span><span class="sxs-lookup"><span data-stu-id="42711-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="42711-140">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="42711-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="42711-141">值</span><span class="sxs-lookup"><span data-stu-id="42711-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="42711-142">意義</span><span class="sxs-lookup"><span data-stu-id="42711-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="42711-143"><dt>**點**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42711-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="42711-144">這個設定資料實例會提供一組值。</span><span class="sxs-lookup"><span data-stu-id="42711-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="42711-145"><dt>**最低**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="42711-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="42711-146">這種設定資料提供評估屬性的最小值。</span><span class="sxs-lookup"><span data-stu-id="42711-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="42711-147">搭配 **PropertyPolicy** = "獨立" 使用時，必須為每個特定的設定資料實例只指定一種這類設定。</span><span class="sxs-lookup"><span data-stu-id="42711-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="42711-148">除非受限於相同屬性集的最大值，否則比較高於指定值的所有值也會被視為相關聯的功能實例所支援的值。</span><span class="sxs-lookup"><span data-stu-id="42711-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="42711-149"><dt></dt>最大<dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="42711-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="42711-150">這種設定資料提供評估屬性的最大值。</span><span class="sxs-lookup"><span data-stu-id="42711-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="42711-151">搭配 **PropertyPolicy** = "獨立" 使用時，必須為每個特定的設定資料實例只指定一種這類設定。</span><span class="sxs-lookup"><span data-stu-id="42711-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="42711-152">除非受限於相同屬性集的最小值，否則比較小於指定值的所有值也會被視為相關聯的功能實例所支援的值。</span><span class="sxs-lookup"><span data-stu-id="42711-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="42711-153"><dt>**遞增**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="42711-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="42711-154">這種設定資料會提供評估屬性的遞增值。</span><span class="sxs-lookup"><span data-stu-id="42711-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="42711-155">針對相關聯的功能，如果評估的屬性目前沒有對應的最小值或最大值，則屬性不會有任何影響。</span><span class="sxs-lookup"><span data-stu-id="42711-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="42711-156">否則，針對每個評估的屬性，其值 (*x*) 必須介於 *MinimumValue* 和 *MaximumValue* 之間（含），而且必須具有 *MaximumValue* 減 *x* 的結果和 *x* 減去 *MinimumValue* 的結果兩者都是 *遞增* 的整數倍數的屬性。</span><span class="sxs-lookup"><span data-stu-id="42711-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="42711-157">如果未指定 *MinimumValue* 或 *MaximumValue* ，而另一個是，則必須將遺漏值分別假設為屬性資料類型的最低或最高支援值。</span><span class="sxs-lookup"><span data-stu-id="42711-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="42711-158">此外，如果已針對評估的屬性指定 *MinimumValue* 和 *MaximumValue* ，則 *MaximumValue* 減去 *MinimumValue* 的結果必須是 *遞增* 的整數倍數。</span><span class="sxs-lookup"><span data-stu-id="42711-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="42711-159">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="42711-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42711-160">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="42711-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42711-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42711-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42711-162">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="42711-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42711-163">針對設定資料之非 **Null**、非索引鍵屬性的解讀指定進一步的語法。</span><span class="sxs-lookup"><span data-stu-id="42711-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="42711-164">這個屬性繼承自 [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="42711-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="42711-165">值</span><span class="sxs-lookup"><span data-stu-id="42711-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="42711-166">意義</span><span class="sxs-lookup"><span data-stu-id="42711-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="42711-167"><dt>**預設值**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42711-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="42711-168">當針對功能由相關聯的功能定義的專案建立新的設定資料實例時，設定資料的屬性值將會當做預設值使用。</span><span class="sxs-lookup"><span data-stu-id="42711-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="42711-169">在設定資料的實例中，針對具有相同語義用途的特定屬性，最多隻能將這類設定資料實例指定為預設值。</span><span class="sxs-lookup"><span data-stu-id="42711-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="42711-170"><dt>**最佳**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="42711-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="42711-171">設定資料實例代表與相關聯的功能相關聯之元素的最佳設定值。</span><span class="sxs-lookup"><span data-stu-id="42711-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="42711-172">多個元件設定資料實例可能會宣告為最佳。</span><span class="sxs-lookup"><span data-stu-id="42711-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="42711-173"><dt>**平均**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="42711-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="42711-174">關聯設定資料實例的非 **Null**、非索引鍵、非列舉、非布林值的數值屬性，代表沿著某個維度的平均點。</span><span class="sxs-lookup"><span data-stu-id="42711-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="42711-175">針對不同的設定資料屬性組合，可以將多個元件設定資料實例宣告為 **Mean**。</span><span class="sxs-lookup"><span data-stu-id="42711-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="42711-176"><dt>**支援**</dt>的 <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="42711-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="42711-177">設定資料的非 **Null**、非索引鍵屬性工作表示一組不合格的支援屬性值。</span><span class="sxs-lookup"><span data-stu-id="42711-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42711-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="42711-178">Requirements</span></span>



| <span data-ttu-id="42711-179">需求</span><span class="sxs-lookup"><span data-stu-id="42711-179">Requirement</span></span> | <span data-ttu-id="42711-180">值</span><span class="sxs-lookup"><span data-stu-id="42711-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42711-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42711-181">Minimum supported client</span></span><br/> | <span data-ttu-id="42711-182">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42711-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42711-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42711-183">Minimum supported server</span></span><br/> | <span data-ttu-id="42711-184">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42711-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42711-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="42711-185">Namespace</span></span><br/>                | <span data-ttu-id="42711-186">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="42711-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42711-187">MOF</span><span class="sxs-lookup"><span data-stu-id="42711-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42711-188"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="42711-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42711-189">DLL</span><span class="sxs-lookup"><span data-stu-id="42711-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42711-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42711-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

