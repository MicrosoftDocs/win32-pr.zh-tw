---
description: 代表存在於單一主機系統上的虛擬化服務。 Msvm \_ VirtualEthernetSwitchManagementService 是用來控制虛擬乙太網路交換器的定義、修改和刪除。
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Msvm_VirtualEthernetSwitchManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981903"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="881fc-104">Msvm \_ VirtualEthernetSwitchManagementService 類別</span><span class="sxs-lookup"><span data-stu-id="881fc-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="881fc-105">代表存在於單一主機系統上的虛擬化服務。</span><span class="sxs-lookup"><span data-stu-id="881fc-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="881fc-106">Msvm \_ VirtualEthernetSwitchManagementService 是用來控制虛擬乙太網路交換器的定義、修改和刪除。</span><span class="sxs-lookup"><span data-stu-id="881fc-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="881fc-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="881fc-108">語法</span><span class="sxs-lookup"><span data-stu-id="881fc-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="881fc-109">成員</span><span class="sxs-lookup"><span data-stu-id="881fc-109">Members</span></span>

<span data-ttu-id="881fc-110">**Msvm \_ VirtualEthernetSwitchManagementService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="881fc-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="881fc-111">方法</span><span class="sxs-lookup"><span data-stu-id="881fc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="881fc-112">屬性</span><span class="sxs-lookup"><span data-stu-id="881fc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="881fc-113">方法</span><span class="sxs-lookup"><span data-stu-id="881fc-113">Methods</span></span>

<span data-ttu-id="881fc-114">**Msvm \_ VirtualEthernetSwitchManagementService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="881fc-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="881fc-115">方法</span><span class="sxs-lookup"><span data-stu-id="881fc-115">Method</span></span>                                                                                               | <span data-ttu-id="881fc-116">描述</span><span class="sxs-lookup"><span data-stu-id="881fc-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="881fc-117">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="881fc-118">將功能設定新增至乙太網路交換器埠的設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="881fc-119">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="881fc-120">將資源新增至虛擬交換器設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="881fc-121">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="881fc-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="881fc-122">建立新的虛擬交換器。</span><span class="sxs-lookup"><span data-stu-id="881fc-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="881fc-123">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="881fc-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="881fc-124">終結虛擬交換器。</span><span class="sxs-lookup"><span data-stu-id="881fc-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="881fc-125">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="881fc-126">修改 Ethernet 交換器埠的功能設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="881fc-127">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="881fc-128">修改虛擬交換器的資源設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="881fc-129">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="881fc-130">修改虛擬交換器設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="881fc-131">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="881fc-132">從乙太網路交換器埠移除功能設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="881fc-133">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="881fc-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="881fc-134">從虛擬交換器設定移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="881fc-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="881fc-135">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="881fc-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="881fc-136">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="881fc-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="881fc-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="881fc-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="881fc-138">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="881fc-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="881fc-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="881fc-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="881fc-140">停止服務。</span><span class="sxs-lookup"><span data-stu-id="881fc-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="881fc-141">屬性</span><span class="sxs-lookup"><span data-stu-id="881fc-141">Properties</span></span>

<span data-ttu-id="881fc-142">**Msvm \_ VirtualEthernetSwitchManagementService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="881fc-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="881fc-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-144">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="881fc-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="881fc-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-146">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="881fc-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="881fc-147">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="881fc-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="881fc-148">**標題**</span><span class="sxs-lookup"><span data-stu-id="881fc-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-151">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="881fc-151">A short description of the object.</span></span> <span data-ttu-id="881fc-152">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬網路管理服務」。</span><span class="sxs-lookup"><span data-stu-id="881fc-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-153">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="881fc-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-156">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="881fc-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="881fc-157">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="881fc-158">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="881fc-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="881fc-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="881fc-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="881fc-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="881fc-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="881fc-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="881fc-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="881fc-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="881fc-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="881fc-166">)</span><span class="sxs-lookup"><span data-stu-id="881fc-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="881fc-167">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="881fc-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-170">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-171">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="881fc-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="881fc-172">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ VirtualEthernetSwitchManagementService"。</span><span class="sxs-lookup"><span data-stu-id="881fc-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-173">**說明**</span><span class="sxs-lookup"><span data-stu-id="881fc-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-176">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="881fc-176">A description of the object.</span></span> <span data-ttu-id="881fc-177">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「提供 hyper-v 網路 WMI 管理」。</span><span class="sxs-lookup"><span data-stu-id="881fc-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="881fc-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-181">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="881fc-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="881fc-182">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="881fc-183">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="881fc-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="881fc-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="881fc-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="881fc-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="881fc-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="881fc-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="881fc-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="881fc-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="881fc-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="881fc-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="881fc-192">)</span><span class="sxs-lookup"><span data-stu-id="881fc-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="881fc-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="881fc-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-196">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="881fc-196">A display name for the object.</span></span> <span data-ttu-id="881fc-197">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 網路管理服務」。</span><span class="sxs-lookup"><span data-stu-id="881fc-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="881fc-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-201">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="881fc-202">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="881fc-203">值</span><span class="sxs-lookup"><span data-stu-id="881fc-203">Value</span></span>                                                                        | <span data-ttu-id="881fc-204">意義</span><span class="sxs-lookup"><span data-stu-id="881fc-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="881fc-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="881fc-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="881fc-206">已啟用</span><span class="sxs-lookup"><span data-stu-id="881fc-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="881fc-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="881fc-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-210">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="881fc-211">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="881fc-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="881fc-212">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="881fc-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="881fc-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-214">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-216">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="881fc-216">The current health of the element.</span></span> <span data-ttu-id="881fc-217">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="881fc-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="881fc-218">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="881fc-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="881fc-219">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="881fc-220">值</span><span class="sxs-lookup"><span data-stu-id="881fc-220">Value</span></span>                                                                        | <span data-ttu-id="881fc-221">意義</span><span class="sxs-lookup"><span data-stu-id="881fc-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="881fc-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="881fc-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="881fc-223">健全狀況狀態為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="881fc-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="881fc-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="881fc-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-225">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="881fc-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-227">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="881fc-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="881fc-228">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="881fc-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="881fc-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="881fc-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-232">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="881fc-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="881fc-233">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="881fc-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="881fc-234">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="881fc-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="881fc-235">**名稱**</span><span class="sxs-lookup"><span data-stu-id="881fc-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-236">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-238">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-239">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="881fc-239">The label by which the object is known.</span></span> <span data-ttu-id="881fc-240">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "vmms"。</span><span class="sxs-lookup"><span data-stu-id="881fc-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-241">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="881fc-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-242">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-244">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="881fc-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="881fc-245">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="881fc-246">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="881fc-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="881fc-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="881fc-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="881fc-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="881fc-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="881fc-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="881fc-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="881fc-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="881fc-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="881fc-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="881fc-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="881fc-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="881fc-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="881fc-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="881fc-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="881fc-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="881fc-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="881fc-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="881fc-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="881fc-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="881fc-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="881fc-266">)</span><span class="sxs-lookup"><span data-stu-id="881fc-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="881fc-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="881fc-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-268">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="881fc-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="881fc-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-270">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-270">The current statuses of the object.</span></span> <span data-ttu-id="881fc-271">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="881fc-272">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="881fc-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-275">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="881fc-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="881fc-276">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="881fc-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="881fc-277">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="881fc-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="881fc-278">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="881fc-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-281">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-282">有關如何聯繫服務主要擁有者的任何資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="881fc-283">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="881fc-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="881fc-284">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="881fc-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-287">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-288">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="881fc-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="881fc-289">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="881fc-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="881fc-290">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="881fc-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="881fc-291">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="881fc-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-292">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-294">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="881fc-294">Provides high level status information.</span></span> <span data-ttu-id="881fc-295">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="881fc-296">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="881fc-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="881fc-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="881fc-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="881fc-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-299"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="881fc-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="881fc-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="881fc-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="881fc-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="881fc-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="881fc-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="881fc-304">)</span><span class="sxs-lookup"><span data-stu-id="881fc-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="881fc-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="881fc-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-306">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-308">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="881fc-309">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="881fc-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="881fc-310">系統會提供這個屬性來比較專案的最後一個要求和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="881fc-311">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="881fc-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="881fc-312">如果發生這種情況，則會使用值 12 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="881fc-313">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="881fc-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="881fc-314">值</span><span class="sxs-lookup"><span data-stu-id="881fc-314">Value</span></span>                                                                         | <span data-ttu-id="881fc-315">意義</span><span class="sxs-lookup"><span data-stu-id="881fc-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="881fc-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="881fc-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="881fc-317">不適用。</span><span class="sxs-lookup"><span data-stu-id="881fc-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="881fc-318">**已開始**</span><span class="sxs-lookup"><span data-stu-id="881fc-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-319">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="881fc-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-321">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="881fc-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="881fc-322">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="881fc-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="881fc-323">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="881fc-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-326">限定詞： **MaxLen** ( 10 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-327">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="881fc-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="881fc-328">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="881fc-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="881fc-329">**狀態**</span><span class="sxs-lookup"><span data-stu-id="881fc-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-332">說明服務目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-332">Describes the current status of the service.</span></span> <span data-ttu-id="881fc-333">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="881fc-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-334">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="881fc-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-335">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="881fc-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="881fc-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-337">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="881fc-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="881fc-338">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="881fc-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-339">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="881fc-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-342">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-343">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="881fc-343">The scoping system's creation class name.</span></span> <span data-ttu-id="881fc-344">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="881fc-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="881fc-345">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="881fc-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="881fc-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="881fc-348">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="881fc-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="881fc-349">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="881fc-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="881fc-350">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="881fc-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="881fc-351">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="881fc-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-352">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="881fc-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-354">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="881fc-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="881fc-355">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="881fc-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="881fc-356">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="881fc-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="881fc-357">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="881fc-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="881fc-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="881fc-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="881fc-359">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="881fc-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="881fc-360">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="881fc-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="881fc-361">規格需求</span><span class="sxs-lookup"><span data-stu-id="881fc-361">Requirements</span></span>



| <span data-ttu-id="881fc-362">需求</span><span class="sxs-lookup"><span data-stu-id="881fc-362">Requirement</span></span> | <span data-ttu-id="881fc-363">值</span><span class="sxs-lookup"><span data-stu-id="881fc-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881fc-364">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="881fc-364">Minimum supported client</span></span><br/> | <span data-ttu-id="881fc-365">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="881fc-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="881fc-366">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="881fc-366">Minimum supported server</span></span><br/> | <span data-ttu-id="881fc-367">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="881fc-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="881fc-368">命名空間</span><span class="sxs-lookup"><span data-stu-id="881fc-368">Namespace</span></span><br/>                | <span data-ttu-id="881fc-369">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="881fc-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="881fc-370">MOF</span><span class="sxs-lookup"><span data-stu-id="881fc-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="881fc-371"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="881fc-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="881fc-372">DLL</span><span class="sxs-lookup"><span data-stu-id="881fc-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="881fc-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="881fc-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

