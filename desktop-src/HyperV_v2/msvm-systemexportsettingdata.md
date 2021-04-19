---
description: 建立虛擬機器與其匯出設定資料的關聯。
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974011"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="a47d8-103">Msvm \_ SystemExportSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="a47d8-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="a47d8-104">建立虛擬機器與其匯出設定資料的關聯。</span><span class="sxs-lookup"><span data-stu-id="a47d8-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="a47d8-105">在呼叫 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)方法之前，可以使用此關聯來抓取 [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="a47d8-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="a47d8-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a47d8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a47d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="a47d8-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="a47d8-108">成員</span><span class="sxs-lookup"><span data-stu-id="a47d8-108">Members</span></span>

<span data-ttu-id="a47d8-109">**Msvm \_ SystemExportSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a47d8-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a47d8-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a47d8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a47d8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a47d8-111">Properties</span></span>

<span data-ttu-id="a47d8-112">**Msvm \_ SystemExportSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a47d8-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a47d8-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="a47d8-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47d8-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a47d8-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a47d8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a47d8-116">指出參考的設定目前是否在專案的作業中使用，或這項資訊未知。</span><span class="sxs-lookup"><span data-stu-id="a47d8-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="a47d8-117">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a47d8-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="a47d8-118">值</span><span class="sxs-lookup"><span data-stu-id="a47d8-118">Value</span></span>                                                                        | <span data-ttu-id="a47d8-119">意義</span><span class="sxs-lookup"><span data-stu-id="a47d8-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="a47d8-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a47d8-121">Unknown</span><span class="sxs-lookup"><span data-stu-id="a47d8-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="a47d8-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a47d8-123">目前</span><span class="sxs-lookup"><span data-stu-id="a47d8-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="a47d8-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a47d8-125">非最新</span><span class="sxs-lookup"><span data-stu-id="a47d8-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a47d8-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="a47d8-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47d8-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a47d8-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a47d8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a47d8-129">指出參考的設定是否為專案的預設值，或這項資訊未知。</span><span class="sxs-lookup"><span data-stu-id="a47d8-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="a47d8-130">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a47d8-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="a47d8-131">值</span><span class="sxs-lookup"><span data-stu-id="a47d8-131">Value</span></span>                                                                        | <span data-ttu-id="a47d8-132">意義</span><span class="sxs-lookup"><span data-stu-id="a47d8-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="a47d8-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a47d8-134">Unknown</span><span class="sxs-lookup"><span data-stu-id="a47d8-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="a47d8-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a47d8-136">預設</span><span class="sxs-lookup"><span data-stu-id="a47d8-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="a47d8-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a47d8-138">非預設</span><span class="sxs-lookup"><span data-stu-id="a47d8-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a47d8-139">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="a47d8-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47d8-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a47d8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a47d8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a47d8-142">指出參考的設定是否為下一個要套用的設定。</span><span class="sxs-lookup"><span data-stu-id="a47d8-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="a47d8-143">例如，應用程式可能會在重新初始化、重設、重新設定要求上進行。</span><span class="sxs-lookup"><span data-stu-id="a47d8-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="a47d8-144">這可能是永久設定，或是僅使用一次的設定，如旗標所示。</span><span class="sxs-lookup"><span data-stu-id="a47d8-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="a47d8-145">如果是永久設定，則會在每次受控元素重新初始化時套用設定，直到以手動方式重設此旗標為止。</span><span class="sxs-lookup"><span data-stu-id="a47d8-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="a47d8-146">但是，如果是單一使用，則會在套用設定之後自動清除旗標。</span><span class="sxs-lookup"><span data-stu-id="a47d8-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="a47d8-147">此外，如果指定此旗標 (亦即設定為0以外的值 (未知的) ) ，則會優先于任何可能已指定為預設值的設定資料。</span><span class="sxs-lookup"><span data-stu-id="a47d8-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="a47d8-148">例如：如果 managed 元素是電腦系統，且此旗標的值為 1 (下一步) ，則設定會在系統下次重設時生效。</span><span class="sxs-lookup"><span data-stu-id="a47d8-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="a47d8-149">而且，除非此旗標已變更，否則後續的系統重設會保存此旗標。</span><span class="sxs-lookup"><span data-stu-id="a47d8-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="a47d8-150">但是，如果此旗標設定為 3 (下一步是使用) ，則這項設定只會使用一次，且旗標會在之後重設為 2 (不是下一個) 。</span><span class="sxs-lookup"><span data-stu-id="a47d8-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="a47d8-151">因此，在上述範例中，如果系統快速地連續重新開機，則在第二次重新開機時不會使用此設定。</span><span class="sxs-lookup"><span data-stu-id="a47d8-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="a47d8-152">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a47d8-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="a47d8-153">值</span><span class="sxs-lookup"><span data-stu-id="a47d8-153">Value</span></span>                                                                        | <span data-ttu-id="a47d8-154">意義</span><span class="sxs-lookup"><span data-stu-id="a47d8-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="a47d8-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a47d8-156">Unknown</span><span class="sxs-lookup"><span data-stu-id="a47d8-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="a47d8-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a47d8-158">下一步</span><span class="sxs-lookup"><span data-stu-id="a47d8-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="a47d8-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a47d8-160">不是下一個</span><span class="sxs-lookup"><span data-stu-id="a47d8-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="a47d8-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a47d8-162">下一步是用於單次使用</span><span class="sxs-lookup"><span data-stu-id="a47d8-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a47d8-163">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a47d8-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47d8-164">資料類型： **[ **CIM \_** 未執行](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="a47d8-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a47d8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-166">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ElementSettingData 的 ) </span><span class="sxs-lookup"><span data-stu-id="a47d8-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="a47d8-167">虛擬機器的參考。</span><span class="sxs-lookup"><span data-stu-id="a47d8-167">Reference to the virtual machine.</span></span> <span data-ttu-id="a47d8-168">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a47d8-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="a47d8-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="a47d8-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a47d8-170">資料類型： **[ **Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="a47d8-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a47d8-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a47d8-172">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ ElementSettingData ) </span><span class="sxs-lookup"><span data-stu-id="a47d8-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="a47d8-173">參考虛擬機器的匯出設定資料。</span><span class="sxs-lookup"><span data-stu-id="a47d8-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="a47d8-174">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="a47d8-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a47d8-175">備註</span><span class="sxs-lookup"><span data-stu-id="a47d8-175">Remarks</span></span>

<span data-ttu-id="a47d8-176">存取 **Msvm \_ SystemExportSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a47d8-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a47d8-177">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a47d8-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a47d8-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="a47d8-178">Requirements</span></span>



| <span data-ttu-id="a47d8-179">需求</span><span class="sxs-lookup"><span data-stu-id="a47d8-179">Requirement</span></span> | <span data-ttu-id="a47d8-180">值</span><span class="sxs-lookup"><span data-stu-id="a47d8-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a47d8-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a47d8-181">Minimum supported client</span></span><br/> | <span data-ttu-id="a47d8-182">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a47d8-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a47d8-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a47d8-183">Minimum supported server</span></span><br/> | <span data-ttu-id="a47d8-184">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a47d8-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a47d8-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="a47d8-185">Namespace</span></span><br/>                | <span data-ttu-id="a47d8-186">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a47d8-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a47d8-187">MOF</span><span class="sxs-lookup"><span data-stu-id="a47d8-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a47d8-188"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a47d8-189">DLL</span><span class="sxs-lookup"><span data-stu-id="a47d8-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a47d8-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a47d8-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

