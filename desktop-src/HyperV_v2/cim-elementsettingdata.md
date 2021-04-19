---
description: 代表 managed 元素與其相關聯設定資料之間的關聯。 此關聯也會說明這是預設值還是目前的設定。
ms.assetid: 0df2b235-76d9-4899-938b-274ec5471324
title: CIM_ElementSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSettingData
- CIM_ElementSettingData.ManagedElement
- CIM_ElementSettingData.SettingData
- CIM_ElementSettingData.IsDefault
- CIM_ElementSettingData.IsCurrent
- CIM_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e22dbd221f2e83009e4268cc0de337374e04298a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979179"
---
# <a name="cim_elementsettingdata-class"></a><span data-ttu-id="16b74-104">CIM \_ ElementSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="16b74-104">CIM\_ElementSettingData class</span></span>

<span data-ttu-id="16b74-105">代表 managed 元素與其相關聯設定資料之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="16b74-105">Represents an association between a managed element and its associated setting data.</span></span> <span data-ttu-id="16b74-106">此關聯也會說明這是預設值還是目前的設定。</span><span class="sxs-lookup"><span data-stu-id="16b74-106">This association also describes whether this is a default or current setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b74-107">語法</span><span class="sxs-lookup"><span data-stu-id="16b74-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.19.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault;
  uint16                 IsCurrent;
  uint16                 IsNext;
};
```

## <a name="members"></a><span data-ttu-id="16b74-108">成員</span><span class="sxs-lookup"><span data-stu-id="16b74-108">Members</span></span>

<span data-ttu-id="16b74-109">**CIM \_ ElementSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="16b74-109">The **CIM\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="16b74-110">屬性</span><span class="sxs-lookup"><span data-stu-id="16b74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16b74-111">屬性</span><span class="sxs-lookup"><span data-stu-id="16b74-111">Properties</span></span>

<span data-ttu-id="16b74-112">**CIM \_ ElementSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="16b74-112">The **CIM\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16b74-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="16b74-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b74-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="16b74-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16b74-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b74-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16b74-116">指出參考的設定目前是否由元素使用中。</span><span class="sxs-lookup"><span data-stu-id="16b74-116">Indicates whether the referenced setting is currently being used by the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16b74-117">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="16b74-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>

<span data-ttu-id="16b74-118">**為目前的** (1) </span><span class="sxs-lookup"><span data-stu-id="16b74-118">**Is Current** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>

<span data-ttu-id="16b74-119">**不是目前的** (2) </span><span class="sxs-lookup"><span data-stu-id="16b74-119">**Is Not Current** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16b74-120">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="16b74-120">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b74-121">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="16b74-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16b74-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b74-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16b74-123">指出此設定是否為元素的預設設定。</span><span class="sxs-lookup"><span data-stu-id="16b74-123">Indicating whether the setting is a default setting for the element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16b74-124">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="16b74-124">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>

<span data-ttu-id="16b74-125">**預設** (1) </span><span class="sxs-lookup"><span data-stu-id="16b74-125">**Is Default** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>

<span data-ttu-id="16b74-126">**不是預設值** (2) </span><span class="sxs-lookup"><span data-stu-id="16b74-126">**Is Not Default** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16b74-127">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="16b74-127">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b74-128">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="16b74-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16b74-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b74-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16b74-130">旗標，指出套用設定的時間和頻率。</span><span class="sxs-lookup"><span data-stu-id="16b74-130">A flag that indicates when and how often to apply the setting.</span></span>

<span data-ttu-id="16b74-131">例如，您可以在重新初始化、重設、重新設定要求上套用設定。</span><span class="sxs-lookup"><span data-stu-id="16b74-131">For example, the setting could be applied on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="16b74-132">這可能是永久設定，或是僅使用一次的設定，如旗標所示。</span><span class="sxs-lookup"><span data-stu-id="16b74-132">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="16b74-133">如果是永久設定，則會在每次受控元素重新初始化時套用設定，直到以手動方式重設此旗標為止。</span><span class="sxs-lookup"><span data-stu-id="16b74-133">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="16b74-134">但是，如果是單一使用，則會在套用設定之後自動清除旗標。</span><span class="sxs-lookup"><span data-stu-id="16b74-134">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="16b74-135">此外，如果此旗標設定為0以外的值 (未知的) ，則會優先于設定為 "Default" 的 **SettingData** 屬性。</span><span class="sxs-lookup"><span data-stu-id="16b74-135">In addition, if this flag is set to value other than 0 (Unknown), then this takes precedence over a **SettingData** property that is set to "Default".</span></span>

<span data-ttu-id="16b74-136">如果受管理元素是電腦系統，且此旗標的值為「下一步」，則此設定將會在系統下次重設時生效。</span><span class="sxs-lookup"><span data-stu-id="16b74-136">If the managed element is a computer system, and the value of this flag is "Is Next", then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="16b74-137">而且，除非此旗標已變更，否則後續的系統重設會保存此旗標。</span><span class="sxs-lookup"><span data-stu-id="16b74-137">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="16b74-138">但是，如果此旗標設定為 [單一使用的下一步]，則此設定只會使用一次，而且旗標會在之後重設為 2 (不) 下一次。</span><span class="sxs-lookup"><span data-stu-id="16b74-138">However, if this flag is set to "Is Next For Single Use", then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="16b74-139">因此，在上述範例中，如果系統快速地連續重新開機，則在第二次重新開機時不會使用此設定。</span><span class="sxs-lookup"><span data-stu-id="16b74-139">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16b74-140">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="16b74-140">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>

<span data-ttu-id="16b74-141">**接下來** (1) </span><span class="sxs-lookup"><span data-stu-id="16b74-141">**Is Next** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>

<span data-ttu-id="16b74-142">**不是接下來的** (2) </span><span class="sxs-lookup"><span data-stu-id="16b74-142">**Is Not Next** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>

<span data-ttu-id="16b74-143">**下一步是用於單一用途** (3) </span><span class="sxs-lookup"><span data-stu-id="16b74-143">**Is Next For Single Use** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16b74-144">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="16b74-144">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b74-145">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="16b74-145">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="16b74-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b74-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16b74-147">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16b74-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="16b74-148">Managed 元素。</span><span class="sxs-lookup"><span data-stu-id="16b74-148">The managed element.</span></span>

</dd> <dt>

<span data-ttu-id="16b74-149">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="16b74-149">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16b74-150">資料類型： **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="16b74-150">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="16b74-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="16b74-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16b74-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="16b74-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="16b74-153">與元素相關聯的設定資料。</span><span class="sxs-lookup"><span data-stu-id="16b74-153">The setting data associated with the element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16b74-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b74-154">Requirements</span></span>



| <span data-ttu-id="16b74-155">需求</span><span class="sxs-lookup"><span data-stu-id="16b74-155">Requirement</span></span> | <span data-ttu-id="16b74-156">值</span><span class="sxs-lookup"><span data-stu-id="16b74-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b74-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16b74-157">Minimum supported client</span></span><br/> | <span data-ttu-id="16b74-158">Windows 8</span><span class="sxs-lookup"><span data-stu-id="16b74-158">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="16b74-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16b74-159">Minimum supported server</span></span><br/> | <span data-ttu-id="16b74-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16b74-160">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="16b74-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="16b74-161">Namespace</span></span><br/>                | <span data-ttu-id="16b74-162">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="16b74-162">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16b74-163">MOF</span><span class="sxs-lookup"><span data-stu-id="16b74-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16b74-164"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="16b74-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16b74-165">DLL</span><span class="sxs-lookup"><span data-stu-id="16b74-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b74-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16b74-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

