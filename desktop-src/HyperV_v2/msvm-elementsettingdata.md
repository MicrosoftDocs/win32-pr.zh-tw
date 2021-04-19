---
description: 將 managed 元素與其設定資料產生關聯。
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Msvm_ElementSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970843"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="8f563-103">Msvm \_ ElementSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="8f563-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="8f563-104">將 managed 元素與其設定資料產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8f563-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="8f563-105">這項關聯的一些較值得注意的應用程式，是用來連結虛擬機器和已指派給該系統的邏輯裝置及其快照集設定資訊。</span><span class="sxs-lookup"><span data-stu-id="8f563-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="8f563-106">目前的設定資訊會透過 [**Msvm \_ SettingsDefineState**](msvm-settingsdefinestate.md) 關聯，與虛擬機器及其裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8f563-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="8f563-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8f563-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f563-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f563-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="8f563-109">成員</span><span class="sxs-lookup"><span data-stu-id="8f563-109">Members</span></span>

<span data-ttu-id="8f563-110">**Msvm \_ ElementSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f563-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8f563-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8f563-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f563-112">屬性</span><span class="sxs-lookup"><span data-stu-id="8f563-112">Properties</span></span>

<span data-ttu-id="8f563-113">**Msvm \_ ElementSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8f563-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f563-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="8f563-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f563-115">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f563-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f563-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f563-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f563-117">指出參考的設定目前用於專案的作業，或這項資訊未知。</span><span class="sxs-lookup"><span data-stu-id="8f563-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="8f563-118">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8f563-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="8f563-119">預設值為 0 (未知) 。</span><span class="sxs-lookup"><span data-stu-id="8f563-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="8f563-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8f563-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**為目前的** (1) </span><span class="sxs-lookup"><span data-stu-id="8f563-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**不是目前的** (2) </span><span class="sxs-lookup"><span data-stu-id="8f563-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f563-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="8f563-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f563-124">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f563-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f563-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f563-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f563-126">指出參考的設定是專案的預設設定，或這項資訊未知。</span><span class="sxs-lookup"><span data-stu-id="8f563-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="8f563-127">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8f563-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="8f563-128">預設值為 0 (未知) 。</span><span class="sxs-lookup"><span data-stu-id="8f563-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="8f563-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8f563-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**預設** (1) </span><span class="sxs-lookup"><span data-stu-id="8f563-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**不是預設值** (2) </span><span class="sxs-lookup"><span data-stu-id="8f563-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f563-132">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="8f563-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f563-133">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8f563-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f563-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f563-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f563-135">指出參考的設定是否為下一個要套用的設定。</span><span class="sxs-lookup"><span data-stu-id="8f563-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="8f563-136">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8f563-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="8f563-137">預設值為 0 (未知) 。</span><span class="sxs-lookup"><span data-stu-id="8f563-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="8f563-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8f563-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**接下來** (1) </span><span class="sxs-lookup"><span data-stu-id="8f563-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**不是接下來的** (2) </span><span class="sxs-lookup"><span data-stu-id="8f563-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f563-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**下一步是用於單一用途** (3) </span><span class="sxs-lookup"><span data-stu-id="8f563-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f563-142">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="8f563-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f563-143">資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="8f563-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="8f563-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f563-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f563-145">虛擬機器或虛擬裝置的參考。</span><span class="sxs-lookup"><span data-stu-id="8f563-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="8f563-146">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8f563-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8f563-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="8f563-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f563-148">資料類型： **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="8f563-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="8f563-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f563-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f563-150">虛擬機器或虛擬裝置的快照設定參考。</span><span class="sxs-lookup"><span data-stu-id="8f563-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="8f563-151">這個屬性繼承自 [**CIM \_ ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8f563-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f563-152">備註</span><span class="sxs-lookup"><span data-stu-id="8f563-152">Remarks</span></span>

<span data-ttu-id="8f563-153">存取 **Msvm \_ ElementSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="8f563-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8f563-154">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="8f563-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8f563-155">範例</span><span class="sxs-lookup"><span data-stu-id="8f563-155">Examples</span></span>

<span data-ttu-id="8f563-156">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="8f563-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f563-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f563-157">Requirements</span></span>



| <span data-ttu-id="8f563-158">需求</span><span class="sxs-lookup"><span data-stu-id="8f563-158">Requirement</span></span> | <span data-ttu-id="8f563-159">值</span><span class="sxs-lookup"><span data-stu-id="8f563-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f563-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f563-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8f563-161">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f563-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8f563-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f563-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8f563-163">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f563-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f563-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f563-164">Namespace</span></span><br/>                | <span data-ttu-id="8f563-165">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8f563-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8f563-166">MOF</span><span class="sxs-lookup"><span data-stu-id="8f563-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f563-167"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8f563-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f563-168">DLL</span><span class="sxs-lookup"><span data-stu-id="8f563-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f563-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f563-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f563-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f563-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f563-171">**CIM \_ ElementSettingData**</span><span class="sxs-lookup"><span data-stu-id="8f563-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="8f563-172">**CIM \_ ElementSettingData**</span><span class="sxs-lookup"><span data-stu-id="8f563-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="8f563-173">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="8f563-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

