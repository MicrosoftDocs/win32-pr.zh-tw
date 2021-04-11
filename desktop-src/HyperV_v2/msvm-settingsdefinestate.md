---
description: 將虛擬機器及其裝置與 CIM SettingData 的實例產生關聯 \_ ，以代表適用于這些物件的目前設定。
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193508"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="eeb3e-103">Msvm \_ SettingsDefineState 類別</span><span class="sxs-lookup"><span data-stu-id="eeb3e-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="eeb3e-104">將虛擬機器及其裝置與 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) 的實例產生關聯，以代表適用于這些物件的目前設定。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="eeb3e-105">更明確地說，它會將 Msvm 的程式設計與 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)的實例產生關聯，並將 \**Msvm \_ \** _ 衍生的 [_ *cim \_ LogicalDevice* \*](/windows/desktop/CIMWin32Prov/cim-logicaldevice)與 \**Msvm \_ \** _ 衍生的 [_ *cim \_ ResourceAllocationSettingData* \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)產生關聯。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="eeb3e-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="eeb3e-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb3e-107">語法</span><span class="sxs-lookup"><span data-stu-id="eeb3e-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="eeb3e-108">成員</span><span class="sxs-lookup"><span data-stu-id="eeb3e-108">Members</span></span>

<span data-ttu-id="eeb3e-109">**Msvm \_ SettingsDefineState** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eeb3e-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="eeb3e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="eeb3e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eeb3e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="eeb3e-111">Properties</span></span>

<span data-ttu-id="eeb3e-112">**Msvm \_ SettingsDefineState** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eeb3e-113">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="eeb3e-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb3e-114">資料類型： **[ **Msvm \_**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="eeb3e-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="eeb3e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eeb3e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb3e-116">虛擬機器的參考。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="eeb3e-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="eeb3e-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb3e-118">資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="eeb3e-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="eeb3e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eeb3e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb3e-120">虛擬機器目前使用中設定的參考。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeb3e-121">備註</span><span class="sxs-lookup"><span data-stu-id="eeb3e-121">Remarks</span></span>

<span data-ttu-id="eeb3e-122">存取 **Msvm \_ SettingsDefineState** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eeb3e-123">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="eeb3e-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb3e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeb3e-124">Requirements</span></span>



| <span data-ttu-id="eeb3e-125">需求</span><span class="sxs-lookup"><span data-stu-id="eeb3e-125">Requirement</span></span> | <span data-ttu-id="eeb3e-126">值</span><span class="sxs-lookup"><span data-stu-id="eeb3e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb3e-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeb3e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb3e-128">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeb3e-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eeb3e-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeb3e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb3e-130">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeb3e-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eeb3e-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="eeb3e-131">Namespace</span></span><br/>                | <span data-ttu-id="eeb3e-132">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="eeb3e-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eeb3e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="eeb3e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeb3e-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="eeb3e-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeb3e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="eeb3e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeb3e-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eeb3e-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eeb3e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeb3e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb3e-138">**CIM \_ SettingsDefineState**</span><span class="sxs-lookup"><span data-stu-id="eeb3e-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="eeb3e-139">**CIM \_ SettingsDefineState**</span><span class="sxs-lookup"><span data-stu-id="eeb3e-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="eeb3e-140">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="eeb3e-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

