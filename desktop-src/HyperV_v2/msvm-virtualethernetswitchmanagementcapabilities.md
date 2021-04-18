---
description: 描述相關聯 Msvm VirtualEthernetSwitchManagementService 的功能 \_ 。
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Msvm_VirtualEthernetSwitchManagementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978197"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="193d4-103">Msvm \_ VirtualEthernetSwitchManagementCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="193d4-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="193d4-104">描述相關聯 [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="193d4-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="193d4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="193d4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="193d4-106">語法</span><span class="sxs-lookup"><span data-stu-id="193d4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="193d4-107">成員</span><span class="sxs-lookup"><span data-stu-id="193d4-107">Members</span></span>

<span data-ttu-id="193d4-108">**Msvm \_ VirtualEthernetSwitchManagementCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="193d4-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="193d4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="193d4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="193d4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="193d4-110">Properties</span></span>

<span data-ttu-id="193d4-111">**Msvm \_ VirtualEthernetSwitchManagementCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="193d4-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="193d4-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="193d4-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-113">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="193d4-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="193d4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="193d4-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported" ) </span><span class="sxs-lookup"><span data-stu-id="193d4-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="193d4-116">方法識別碼的陣列，每個都識別 [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) 類別的方法，此方法是由實作為非同步支援。</span><span class="sxs-lookup"><span data-stu-id="193d4-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="193d4-117">這個屬性繼承自 **CIM \_ VirtualSystemManagementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="193d4-118">**DefineSystem** (2) </span><span class="sxs-lookup"><span data-stu-id="193d4-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="193d4-119">**DestroySystem** (3) </span><span class="sxs-lookup"><span data-stu-id="193d4-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="193d4-120">**DestroySystemConfiguration** (4) </span><span class="sxs-lookup"><span data-stu-id="193d4-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="193d4-121">**ModifyResourceSettings** (5) </span><span class="sxs-lookup"><span data-stu-id="193d4-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="193d4-122">**ModifySystemSettings** (6) </span><span class="sxs-lookup"><span data-stu-id="193d4-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="193d4-123">**RemoveResources** (7) </span><span class="sxs-lookup"><span data-stu-id="193d4-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="193d4-124">**SelectSystemConfiguration** (8) </span><span class="sxs-lookup"><span data-stu-id="193d4-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="193d4-125">**SnapshotSystem** (9) </span><span class="sxs-lookup"><span data-stu-id="193d4-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="193d4-126">**AddResources** (10) </span><span class="sxs-lookup"><span data-stu-id="193d4-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="193d4-127">**AddFeatureSettingsSupported** (32779) </span><span class="sxs-lookup"><span data-stu-id="193d4-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="193d4-128">**ModifyFeatureSettingsSupported** (32780) </span><span class="sxs-lookup"><span data-stu-id="193d4-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="193d4-129">**RemoveFeatureSettingsSupported** (32781) </span><span class="sxs-lookup"><span data-stu-id="193d4-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="193d4-130">**AddFeatureSettingsSupported** (32779) </span><span class="sxs-lookup"><span data-stu-id="193d4-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="193d4-131">**ModifyFeatureSettingsSupported** (32780) </span><span class="sxs-lookup"><span data-stu-id="193d4-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="193d4-132">**RemoveFeatureSettingsSupported** (32781) </span><span class="sxs-lookup"><span data-stu-id="193d4-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="193d4-133">**標題**</span><span class="sxs-lookup"><span data-stu-id="193d4-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="193d4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-136">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="193d4-136">A short description of the object.</span></span> <span data-ttu-id="193d4-137">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「hyper-v 虛擬乙太網路交換器管理服務功能」。</span><span class="sxs-lookup"><span data-stu-id="193d4-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="193d4-138">**說明**</span><span class="sxs-lookup"><span data-stu-id="193d4-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="193d4-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-141">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="193d4-141">A description of the object.</span></span> <span data-ttu-id="193d4-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「定義虛擬乙太網路交換器管理服務功能」。</span><span class="sxs-lookup"><span data-stu-id="193d4-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="193d4-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="193d4-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="193d4-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-146">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="193d4-146">A display name for the object.</span></span> <span data-ttu-id="193d4-147">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「hyper-v 虛擬乙太網路交換器管理服務功能」。</span><span class="sxs-lookup"><span data-stu-id="193d4-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="193d4-148">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="193d4-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-149">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="193d4-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-151">指出是否可以修改 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="193d4-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="193d4-152">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="193d4-153">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="193d4-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="193d4-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-156">指定 **ElementName** 的限制，以正則運算式表示。</span><span class="sxs-lookup"><span data-stu-id="193d4-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="193d4-157">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="193d4-158">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="193d4-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-159">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="193d4-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="193d4-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-161">指示識別碼的陣列，每個識別碼都會識別執行所支援的指示。</span><span class="sxs-lookup"><span data-stu-id="193d4-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="193d4-162">這個屬性繼承自 **CIM \_ VirtualSystemManagementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="193d4-163">值</span><span class="sxs-lookup"><span data-stu-id="193d4-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="193d4-164">意義</span><span class="sxs-lookup"><span data-stu-id="193d4-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="193d4-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="193d4-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="193d4-166">指出實作為虛擬系統資源之 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 實例的狀態變更是否支援通知。</span><span class="sxs-lookup"><span data-stu-id="193d4-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="193d4-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="193d4-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="193d4-168">指出執行是否支援 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) 實例之狀態變更的通知。</span><span class="sxs-lookup"><span data-stu-id="193d4-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="193d4-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="193d4-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="193d4-170">指出此實作為表示虛擬系統之 CIM 系統 [**實例 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 的狀態變更時，是否支援通知。</span><span class="sxs-lookup"><span data-stu-id="193d4-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="193d4-171">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="193d4-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="193d4-172"><dt>**廠商保留**</dt>的 <dt>32767-65535</dt></span><span class="sxs-lookup"><span data-stu-id="193d4-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="193d4-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="193d4-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="193d4-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="193d4-176">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="193d4-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="193d4-177">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="193d4-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="193d4-178">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="193d4-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="193d4-179">**IOVSupport**</span><span class="sxs-lookup"><span data-stu-id="193d4-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="193d4-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-182">布林值，指出平臺是否支援 i/o 虛擬化 (的) 。</span><span class="sxs-lookup"><span data-stu-id="193d4-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="193d4-183">如果值為 **True**，則平臺會支援 sr-iov，且 **IOVSupportReasons** 會是空的。</span><span class="sxs-lookup"><span data-stu-id="193d4-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="193d4-184">否則， **IOVSupportReasons** 屬性將會有無法支援 sr-iov 的原因。</span><span class="sxs-lookup"><span data-stu-id="193d4-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="193d4-185">**IOVSupportReasons**</span><span class="sxs-lookup"><span data-stu-id="193d4-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-186">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="193d4-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="193d4-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-188">字串陣列，指出不支援 SR-IOV 的可能原因。</span><span class="sxs-lookup"><span data-stu-id="193d4-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="193d4-189">如果 **IOVSupport** 的值為 **True**，此陣列將會是空的。</span><span class="sxs-lookup"><span data-stu-id="193d4-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="193d4-190">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="193d4-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-191">資料類型： **unit16**</span><span class="sxs-lookup"><span data-stu-id="193d4-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="193d4-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="193d4-193">限定詞： **int32.maxvalue** (256) </span><span class="sxs-lookup"><span data-stu-id="193d4-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="193d4-194">指定 **ElementName** 屬性支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="193d4-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="193d4-195">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="193d4-196">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="193d4-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-197">資料類型： **unit16** 陣列</span><span class="sxs-lookup"><span data-stu-id="193d4-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="193d4-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-199">指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。</span><span class="sxs-lookup"><span data-stu-id="193d4-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="193d4-200">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities** ，而且一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="193d4-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="193d4-201">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="193d4-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-202">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="193d4-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="193d4-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-204">方法識別碼的陣列，每個都識別 [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) 類別的方法，此方法會由實作為同步支援。</span><span class="sxs-lookup"><span data-stu-id="193d4-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="193d4-205">這個屬性繼承自 **CIM \_ VirtualSystemManagementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="193d4-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2) </span><span class="sxs-lookup"><span data-stu-id="193d4-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3) </span><span class="sxs-lookup"><span data-stu-id="193d4-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4) </span><span class="sxs-lookup"><span data-stu-id="193d4-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5) </span><span class="sxs-lookup"><span data-stu-id="193d4-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6) </span><span class="sxs-lookup"><span data-stu-id="193d4-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7) </span><span class="sxs-lookup"><span data-stu-id="193d4-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8) </span><span class="sxs-lookup"><span data-stu-id="193d4-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9) </span><span class="sxs-lookup"><span data-stu-id="193d4-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10) </span><span class="sxs-lookup"><span data-stu-id="193d4-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779) </span><span class="sxs-lookup"><span data-stu-id="193d4-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780) </span><span class="sxs-lookup"><span data-stu-id="193d4-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="193d4-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 ) </span><span class="sxs-lookup"><span data-stu-id="193d4-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="193d4-218">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="193d4-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="193d4-219">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="193d4-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="193d4-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="193d4-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="193d4-221">字串的陣列，每個字串都指定執行所支援的虛擬系統類型。</span><span class="sxs-lookup"><span data-stu-id="193d4-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="193d4-222">每個非 **Null** 陣列元素的值必須符合針對 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的 **VirtualSystemType** 屬性所定義的格式。</span><span class="sxs-lookup"><span data-stu-id="193d4-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="193d4-223">這個屬性繼承自 **CIM \_ VirtualSystemManagementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="193d4-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="193d4-224">規格需求</span><span class="sxs-lookup"><span data-stu-id="193d4-224">Requirements</span></span>



| <span data-ttu-id="193d4-225">需求</span><span class="sxs-lookup"><span data-stu-id="193d4-225">Requirement</span></span> | <span data-ttu-id="193d4-226">值</span><span class="sxs-lookup"><span data-stu-id="193d4-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="193d4-227">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="193d4-227">Minimum supported client</span></span><br/> | <span data-ttu-id="193d4-228">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="193d4-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="193d4-229">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="193d4-229">Minimum supported server</span></span><br/> | <span data-ttu-id="193d4-230">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="193d4-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="193d4-231">命名空間</span><span class="sxs-lookup"><span data-stu-id="193d4-231">Namespace</span></span><br/>                | <span data-ttu-id="193d4-232">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="193d4-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="193d4-233">MOF</span><span class="sxs-lookup"><span data-stu-id="193d4-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="193d4-234"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="193d4-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="193d4-235">DLL</span><span class="sxs-lookup"><span data-stu-id="193d4-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="193d4-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="193d4-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

