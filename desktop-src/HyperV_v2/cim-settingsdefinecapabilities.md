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
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="3b0ac-103">CIM \_ SettingsDefineCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="3b0ac-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="3b0ac-104">代表 [**cim \_ SettingData**](cim-settingdata.md) 實例和 [**cim \_ 功能**](cim-capabilities.md) 實例的屬性之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b0ac-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="3b0ac-106">成員</span><span class="sxs-lookup"><span data-stu-id="3b0ac-106">Members</span></span>

<span data-ttu-id="3b0ac-107">**CIM \_ SettingsDefineCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b0ac-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="3b0ac-108">屬性</span><span class="sxs-lookup"><span data-stu-id="3b0ac-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b0ac-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3b0ac-109">Properties</span></span>

<span data-ttu-id="3b0ac-110">**CIM \_ SettingsDefineCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b0ac-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0ac-112">資料類型： **CIM \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b0ac-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-114">限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3b0ac-115">[**CIM \_ 功能**](cim-capabilities.md)實例的參考。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="3b0ac-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0ac-117">資料類型： **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b0ac-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-119">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3b0ac-120">用來定義 [**cim \_ 功能**](cim-capabilities.md)實例之 [**cim \_ SettingData**](cim-settingdata.md)實例的參考。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="3b0ac-121">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0ac-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b0ac-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-124">限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SettingsDefineCapabilities**.**ValueRole**"，"**CIM \_ SettingsDefineCapabilities**.**ValueRange**") </span><span class="sxs-lookup"><span data-stu-id="3b0ac-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="3b0ac-125">指出相關聯之 [**CIM \_ SettingData**](cim-settingdata.md) 實例的非 null、非索引鍵屬性是獨立處理或關聯的集合。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="3b0ac-126">比方說，當每個屬性之間沒有任何關聯性時，可能會定義一組獨立的最大屬性。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="3b0ac-127">相反地，當每個屬性的最大值相依于其他部分時，可能需要定義數個相關的最大屬性集合。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="3b0ac-128">**獨立** (0) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="3b0ac-129">相互 **關聯** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3b0ac-130">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b0ac-131">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0ac-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b0ac-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-134">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**"，"**CIM \_ SettingsDefineCapabilities**.**ValueRole**") </span><span class="sxs-lookup"><span data-stu-id="3b0ac-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="3b0ac-135">指出 [**CIM \_ SettingData**](cim-settingdata.md) 實例的非 null、非索引鍵屬性所使用的值範圍類型。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="3b0ac-136">**點** (0) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="3b0ac-137">**最低** (1) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="3b0ac-138">最 **大 (2**) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="3b0ac-139"> (3) **遞增**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3b0ac-140">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b0ac-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0ac-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b0ac-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0ac-144">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**"，"**CIM \_ SettingsDefineCapabilities**.**ValueRange**") </span><span class="sxs-lookup"><span data-stu-id="3b0ac-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="3b0ac-145">[**CIM \_ SettingData**](cim-settingdata.md)實例的非 null、非索引鍵屬性之解釋的額外語義。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="3b0ac-146">「預設」表示建立新的 SettingData 實例，針對其功能由相關聯的功能實例定義的專案時，將會使用此元件的屬性值做為預設值。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="3b0ac-147">在不同的 settingdata 實例上，針對具有相同語義用途的特定屬性，最多隻能指定一個此類的 settingdata 實例作為預設值。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="3b0ac-148">「最佳」表示在與相關聯的功能實例相關聯的元素中，使用最適合的設定值。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="3b0ac-149">可以將多個元件的 SettingData 實例宣告為最佳。」Mean "表示相關聯的 SettingData 實例的非 null、非索引鍵、非列舉、非布林值的數值屬性，代表沿著某個維度的平均點。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="3b0ac-150">針對不同的 SettingData 屬性組合，可以將多個元件的 SettingData 實例宣告為「Mean」。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="3b0ac-151">「支援」表示元件 SettingData 實例的非 null、非索引鍵屬性工作表示一組不具限定的支援屬性值。</span><span class="sxs-lookup"><span data-stu-id="3b0ac-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="3b0ac-152">**預設** (0) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="3b0ac-153">**最佳** (1) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="3b0ac-154">**Mean** (2) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="3b0ac-155">**支援** (3) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3b0ac-156">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3b0ac-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="3b0ac-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3b0ac-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3b0ac-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b0ac-158">Requirements</span></span>



| <span data-ttu-id="3b0ac-159">需求</span><span class="sxs-lookup"><span data-stu-id="3b0ac-159">Requirement</span></span> | <span data-ttu-id="3b0ac-160">值</span><span class="sxs-lookup"><span data-stu-id="3b0ac-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0ac-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b0ac-161">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0ac-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3b0ac-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3b0ac-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b0ac-163">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0ac-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3b0ac-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3b0ac-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b0ac-165">Namespace</span></span><br/>                | <span data-ttu-id="3b0ac-166">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="3b0ac-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3b0ac-167">MOF</span><span class="sxs-lookup"><span data-stu-id="3b0ac-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b0ac-168"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3b0ac-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b0ac-169">DLL</span><span class="sxs-lookup"><span data-stu-id="3b0ac-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b0ac-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b0ac-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b0ac-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b0ac-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0ac-172">**CIM \_ 元件**</span><span class="sxs-lookup"><span data-stu-id="3b0ac-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

