---
description: 代表 CIM VirtualSystemManagementService 物件的功能 \_ 。
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: CIM_VirtualSystemManagementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980792"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="960b5-103">CIM \_ VirtualSystemManagementCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="960b5-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="960b5-104">代表 [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) 物件的功能。</span><span class="sxs-lookup"><span data-stu-id="960b5-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="960b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="960b5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="960b5-106">成員</span><span class="sxs-lookup"><span data-stu-id="960b5-106">Members</span></span>

<span data-ttu-id="960b5-107">**CIM \_ VirtualSystemManagementCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="960b5-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="960b5-108">屬性</span><span class="sxs-lookup"><span data-stu-id="960b5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="960b5-109">屬性</span><span class="sxs-lookup"><span data-stu-id="960b5-109">Properties</span></span>

<span data-ttu-id="960b5-110">**CIM \_ VirtualSystemManagementCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="960b5-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="960b5-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="960b5-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960b5-112">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="960b5-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="960b5-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="960b5-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="960b5-114">陣列，其中包含非同步作業所支援之 [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) 類別方法的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="960b5-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="960b5-115">**DefineSystemSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="960b5-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="960b5-116">**DestroySystemSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="960b5-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="960b5-117">**DestroySystemConfigurationSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="960b5-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="960b5-118">**ModifyResourceSettingsSupported** (5) </span><span class="sxs-lookup"><span data-stu-id="960b5-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="960b5-119">**ModifySystemSettingsSupported** (6) </span><span class="sxs-lookup"><span data-stu-id="960b5-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="960b5-120">**RemoveResourcesSupported** (7) </span><span class="sxs-lookup"><span data-stu-id="960b5-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="960b5-121">**SelectSystemConfigurationSupported** (8) </span><span class="sxs-lookup"><span data-stu-id="960b5-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="960b5-122">**SnapshotSystemSupported** (9) </span><span class="sxs-lookup"><span data-stu-id="960b5-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="960b5-123">**AddResourcesSupported** (10) </span><span class="sxs-lookup"><span data-stu-id="960b5-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="960b5-124">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="960b5-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="960b5-125">**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="960b5-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="960b5-126">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="960b5-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960b5-127">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="960b5-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="960b5-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="960b5-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="960b5-129">陣列，其中包含實作為支援的指示類型。</span><span class="sxs-lookup"><span data-stu-id="960b5-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="960b5-130">**VirtualResourceStateChangeIndicationsSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="960b5-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="960b5-131">**ConcreteJobStateChangeIndicationsSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="960b5-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="960b5-132">**VirtualSystemStateChangeIndicationsSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="960b5-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="960b5-133">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="960b5-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="960b5-134">**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="960b5-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="960b5-135">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="960b5-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960b5-136">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="960b5-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="960b5-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="960b5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="960b5-138">陣列，其中包含同步作業支援之 [**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) 類別方法的方法名稱。</span><span class="sxs-lookup"><span data-stu-id="960b5-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="960b5-139">**DefineSystemSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="960b5-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="960b5-140">**DestroySystemSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="960b5-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="960b5-141">**DestroySystemConfigurationSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="960b5-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="960b5-142">**ModifyResourceSettingsSupported** (5) </span><span class="sxs-lookup"><span data-stu-id="960b5-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="960b5-143">**ModifySystemSettingsSupported** (6) </span><span class="sxs-lookup"><span data-stu-id="960b5-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="960b5-144">**RemoveResourcesSupported** (7) </span><span class="sxs-lookup"><span data-stu-id="960b5-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="960b5-145">**SelectSystemConfigurationSupported** (8) </span><span class="sxs-lookup"><span data-stu-id="960b5-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="960b5-146">**SnapshotSystemSupported** (9) </span><span class="sxs-lookup"><span data-stu-id="960b5-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="960b5-147">**AddResourcesSupported** (10) </span><span class="sxs-lookup"><span data-stu-id="960b5-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="960b5-148">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="960b5-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="960b5-149">**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="960b5-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="960b5-150">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="960b5-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="960b5-151">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="960b5-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="960b5-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="960b5-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="960b5-153">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**") </span><span class="sxs-lookup"><span data-stu-id="960b5-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="960b5-154">實作為支援的虛擬系統類型。</span><span class="sxs-lookup"><span data-stu-id="960b5-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="960b5-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="960b5-155">Requirements</span></span>



| <span data-ttu-id="960b5-156">需求</span><span class="sxs-lookup"><span data-stu-id="960b5-156">Requirement</span></span> | <span data-ttu-id="960b5-157">值</span><span class="sxs-lookup"><span data-stu-id="960b5-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960b5-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="960b5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="960b5-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="960b5-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="960b5-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="960b5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="960b5-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="960b5-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="960b5-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="960b5-162">Namespace</span></span><br/>                | <span data-ttu-id="960b5-163">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="960b5-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="960b5-164">MOF</span><span class="sxs-lookup"><span data-stu-id="960b5-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="960b5-165"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="960b5-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="960b5-166">DLL</span><span class="sxs-lookup"><span data-stu-id="960b5-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="960b5-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="960b5-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="960b5-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="960b5-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="960b5-169">**CIM \_ EnabledLogicalElementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="960b5-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

