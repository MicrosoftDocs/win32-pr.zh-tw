---
description: 描述相關聯 Msvm VirtualSystemManagementService 的功能 \_ 。
ms.assetid: 3a167b06-bddd-4bac-95c0-ecf14e01eec0
title: Msvm_VirtualSystemManagementCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementCapabilities
- Msvm_VirtualSystemManagementCapabilities.InstanceID
- Msvm_VirtualSystemManagementCapabilities.Caption
- Msvm_VirtualSystemManagementCapabilities.Description
- Msvm_VirtualSystemManagementCapabilities.ElementName
- Msvm_VirtualSystemManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualSystemManagementCapabilities.MaxElementNameLen
- Msvm_VirtualSystemManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualSystemManagementCapabilities.ElementNameMask
- Msvm_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24bc8ce66393a5e9ccd13848ab74640aec8d1760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318092"
---
# <a name="msvm_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="3346d-103">Msvm \_ VirtualSystemManagementCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="3346d-103">Msvm\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="3346d-104">描述相關聯 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)的功能。</span><span class="sxs-lookup"><span data-stu-id="3346d-104">Describes the capabilities of the associated [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md).</span></span>

<span data-ttu-id="3346d-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3346d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3346d-106">語法</span><span class="sxs-lookup"><span data-stu-id="3346d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual System Management Service Capabilities";
  string  Description = "Defines Virtual System Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual System Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="3346d-107">成員</span><span class="sxs-lookup"><span data-stu-id="3346d-107">Members</span></span>

<span data-ttu-id="3346d-108">**Msvm \_ VirtualSystemManagementCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3346d-108">The **Msvm\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="3346d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3346d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3346d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3346d-110">Properties</span></span>

<span data-ttu-id="3346d-111">**Msvm \_ VirtualSystemManagementCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3346d-111">The **Msvm\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3346d-112">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="3346d-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-113">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3346d-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3346d-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3346d-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported" ) </span><span class="sxs-lookup"><span data-stu-id="3346d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="3346d-116">指定執行非同步支援的 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3346d-116">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3346d-117">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3346d-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="3346d-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767) </span><span class="sxs-lookup"><span data-stu-id="3346d-118">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="3346d-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770) </span><span class="sxs-lookup"><span data-stu-id="3346d-119">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="3346d-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771) </span><span class="sxs-lookup"><span data-stu-id="3346d-120">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="3346d-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772) </span><span class="sxs-lookup"><span data-stu-id="3346d-121">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="3346d-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778) </span><span class="sxs-lookup"><span data-stu-id="3346d-122">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="3346d-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779) </span><span class="sxs-lookup"><span data-stu-id="3346d-123">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="3346d-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780) </span><span class="sxs-lookup"><span data-stu-id="3346d-124">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="3346d-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781) </span><span class="sxs-lookup"><span data-stu-id="3346d-125">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="3346d-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782) </span><span class="sxs-lookup"><span data-stu-id="3346d-126">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="3346d-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783) </span><span class="sxs-lookup"><span data-stu-id="3346d-127">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="3346d-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784) </span><span class="sxs-lookup"><span data-stu-id="3346d-128">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="3346d-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785) </span><span class="sxs-lookup"><span data-stu-id="3346d-129">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="3346d-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786) </span><span class="sxs-lookup"><span data-stu-id="3346d-130">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="3346d-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787) </span><span class="sxs-lookup"><span data-stu-id="3346d-131">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="3346d-132">**[**造成 stringbuilder.formaterror**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788) </span><span class="sxs-lookup"><span data-stu-id="3346d-132">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="3346d-133">**RequestStateChangeSupported** (32789) </span><span class="sxs-lookup"><span data-stu-id="3346d-133">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="3346d-134">**StartServiceSupported** (32790) </span><span class="sxs-lookup"><span data-stu-id="3346d-134">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="3346d-135">**StopServiceSupported** (32791) </span><span class="sxs-lookup"><span data-stu-id="3346d-135">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="3346d-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792) </span><span class="sxs-lookup"><span data-stu-id="3346d-136">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="3346d-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793) </span><span class="sxs-lookup"><span data-stu-id="3346d-137">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="3346d-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794) </span><span class="sxs-lookup"><span data-stu-id="3346d-138">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="3346d-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795) </span><span class="sxs-lookup"><span data-stu-id="3346d-139">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="3346d-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796) </span><span class="sxs-lookup"><span data-stu-id="3346d-140">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="3346d-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797) </span><span class="sxs-lookup"><span data-stu-id="3346d-141">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="3346d-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798) </span><span class="sxs-lookup"><span data-stu-id="3346d-142">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3346d-143">**廠商保留** (32799： 65535) </span><span class="sxs-lookup"><span data-stu-id="3346d-143">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3346d-144">**標題**</span><span class="sxs-lookup"><span data-stu-id="3346d-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3346d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-147">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3346d-147">A short description of the object.</span></span> <span data-ttu-id="3346d-148">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3346d-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3346d-149">**說明**</span><span class="sxs-lookup"><span data-stu-id="3346d-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3346d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-152">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3346d-152">A description of the object.</span></span> <span data-ttu-id="3346d-153">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3346d-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3346d-154">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3346d-154">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3346d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-157">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3346d-157">A display name for the object.</span></span> <span data-ttu-id="3346d-158">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3346d-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3346d-159">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="3346d-159">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-160">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3346d-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-162">指出是否可以修改 **ElementName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3346d-162">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="3346d-163">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="3346d-163">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="3346d-164">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="3346d-164">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3346d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-167">指定 **ElementName** 的限制，以正則運算式表示。</span><span class="sxs-lookup"><span data-stu-id="3346d-167">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="3346d-168">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="3346d-168">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="3346d-169">**IndicationsSupported**</span><span class="sxs-lookup"><span data-stu-id="3346d-169">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-170">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3346d-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3346d-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3346d-172">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ VirtualSystemManagementCapabilities. IndicationsSupported" ) </span><span class="sxs-lookup"><span data-stu-id="3346d-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.IndicationsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="3346d-173">指定執行所支援的指示。</span><span class="sxs-lookup"><span data-stu-id="3346d-173">Specifies the indications supported by the implementation.</span></span>

<span data-ttu-id="3346d-174">列舉指示識別碼的列舉，每個識別碼都會識別此實作為支援的指示。</span><span class="sxs-lookup"><span data-stu-id="3346d-174">Enumeration of indication identifiers each identifying an indication that is supported by the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="3346d-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2) </span><span class="sxs-lookup"><span data-stu-id="3346d-175"><span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3346d-176">此實 LogicalDevice 代表虛擬系統資源之 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 實例的狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="3346d-176">The implementation supports notification of state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances representing resources of virtual systems.</span></span>

</dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="3346d-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3) </span><span class="sxs-lookup"><span data-stu-id="3346d-177"><span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3346d-178">此執行支援 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) 實例的狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="3346d-178">The implementation supports notification of state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span>

</dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="3346d-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4) </span><span class="sxs-lookup"><span data-stu-id="3346d-179"><span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3346d-180">此實體系支援表示虛擬系統之 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 系統實例的狀態變更通知。</span><span class="sxs-lookup"><span data-stu-id="3346d-180">The implementation supports notification of state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances representing virtual systems.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3346d-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3346d-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3346d-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="3346d-182"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3346d-183">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3346d-183">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3346d-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3346d-186">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3346d-186">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3346d-187">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3346d-187">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3346d-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3346d-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3346d-189">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="3346d-189">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-190">資料類型： **unit16**</span><span class="sxs-lookup"><span data-stu-id="3346d-190">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="3346d-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3346d-192">限定詞： **int32.maxvalue** (256) </span><span class="sxs-lookup"><span data-stu-id="3346d-192">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3346d-193">指定 **ElementName** 屬性支援的最大長度。</span><span class="sxs-lookup"><span data-stu-id="3346d-193">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="3346d-194">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="3346d-194">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="3346d-195">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="3346d-195">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-196">資料類型： **unit16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3346d-196">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="3346d-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-198">指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。</span><span class="sxs-lookup"><span data-stu-id="3346d-198">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="3346d-199">這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。</span><span class="sxs-lookup"><span data-stu-id="3346d-199">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="3346d-200">值</span><span class="sxs-lookup"><span data-stu-id="3346d-200">Value</span></span>                                                                         | <span data-ttu-id="3346d-201">意義</span><span class="sxs-lookup"><span data-stu-id="3346d-201">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="3346d-202"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-202"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="3346d-203">已啟用</span><span class="sxs-lookup"><span data-stu-id="3346d-203">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="3346d-204"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-204"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="3346d-205">禁用</span><span class="sxs-lookup"><span data-stu-id="3346d-205">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="3346d-206"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-206"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="3346d-207">關閉</span><span class="sxs-lookup"><span data-stu-id="3346d-207">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="3346d-208"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-208"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="3346d-209">離線</span><span class="sxs-lookup"><span data-stu-id="3346d-209">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="3346d-210"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-210"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="3346d-211">測試</span><span class="sxs-lookup"><span data-stu-id="3346d-211">Test</span></span><br/>      |
| <dl> <span data-ttu-id="3346d-212"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-212"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="3346d-213">推遲</span><span class="sxs-lookup"><span data-stu-id="3346d-213">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="3346d-214"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-214"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="3346d-215">靜止</span><span class="sxs-lookup"><span data-stu-id="3346d-215">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="3346d-216"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-216"><dt>10</dt></span></span> </dl> | <span data-ttu-id="3346d-217">重新啟動</span><span class="sxs-lookup"><span data-stu-id="3346d-217">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="3346d-218"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-218"><dt>11</dt></span></span> </dl> | <span data-ttu-id="3346d-219">重設</span><span class="sxs-lookup"><span data-stu-id="3346d-219">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="3346d-220">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="3346d-220">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-221">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3346d-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3346d-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3346d-223">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ VirtualSystemManagementCapabilities. SynchronousMethodsSupported" ) </span><span class="sxs-lookup"><span data-stu-id="3346d-223">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.SynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="3346d-224">指定執行同步支援的 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3346d-224">Specifies the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) methods that are supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3346d-225">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="3346d-225">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="ValidatePlannedSystem"></span><span id="validateplannedsystem"></span><span id="VALIDATEPLANNEDSYSTEM"></span>

<span data-ttu-id="3346d-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767) </span><span class="sxs-lookup"><span data-stu-id="3346d-226">**[**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)** (32767)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSystemDefinition"></span><span id="importsystemdefinition"></span><span id="IMPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="3346d-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770) </span><span class="sxs-lookup"><span data-stu-id="3346d-227">**[**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="ImportSnapshotDefinitions"></span><span id="importsnapshotdefinitions"></span><span id="IMPORTSNAPSHOTDEFINITIONS"></span>

<span data-ttu-id="3346d-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771) </span><span class="sxs-lookup"><span data-stu-id="3346d-228">**[**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="RealizePlannedSystem"></span><span id="realizeplannedsystem"></span><span id="REALIZEPLANNEDSYSTEM"></span>

<span data-ttu-id="3346d-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772) </span><span class="sxs-lookup"><span data-stu-id="3346d-229">**[**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)** (32772)</span></span>


</dt> <dd></dd> <dt>

<span id="ExportSystemDefinition"></span><span id="exportsystemdefinition"></span><span id="EXPORTSYSTEMDEFINITION"></span>

<span data-ttu-id="3346d-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778) </span><span class="sxs-lookup"><span data-stu-id="3346d-230">**[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)** (32778)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>

<span data-ttu-id="3346d-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779) </span><span class="sxs-lookup"><span data-stu-id="3346d-231">**[**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>

<span data-ttu-id="3346d-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780) </span><span class="sxs-lookup"><span data-stu-id="3346d-232">**[**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>

<span data-ttu-id="3346d-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781) </span><span class="sxs-lookup"><span data-stu-id="3346d-233">**[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="GetVirtualSystemThumbnailImage"></span><span id="getvirtualsystemthumbnailimage"></span><span id="GETVIRTUALSYSTEMTHUMBNAILIMAGE"></span>

<span data-ttu-id="3346d-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782) </span><span class="sxs-lookup"><span data-stu-id="3346d-234">**[**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyServiceSettings"></span><span id="modifyservicesettings"></span><span id="MODIFYSERVICESETTINGS"></span>

<span data-ttu-id="3346d-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783) </span><span class="sxs-lookup"><span data-stu-id="3346d-235">**[**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSummaryInformation"></span><span id="getsummaryinformation"></span><span id="GETSUMMARYINFORMATION"></span>

<span data-ttu-id="3346d-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784) </span><span class="sxs-lookup"><span data-stu-id="3346d-236">**[**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="AddKvpItems"></span><span id="addkvpitems"></span><span id="ADDKVPITEMS"></span>

<span data-ttu-id="3346d-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785) </span><span class="sxs-lookup"><span data-stu-id="3346d-237">**[**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyKvpItems"></span><span id="modifykvpitems"></span><span id="MODIFYKVPITEMS"></span>

<span data-ttu-id="3346d-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786) </span><span class="sxs-lookup"><span data-stu-id="3346d-238">**[**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveKvpItems"></span><span id="removekvpitems"></span><span id="REMOVEKVPITEMS"></span>

<span data-ttu-id="3346d-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787) </span><span class="sxs-lookup"><span data-stu-id="3346d-239">**[**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="FormatError"></span><span id="formaterror"></span><span id="FORMATERROR"></span>

<span data-ttu-id="3346d-240">**[**造成 stringbuilder.formaterror**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788) </span><span class="sxs-lookup"><span data-stu-id="3346d-240">**[**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="RequestStateChangeSupported"></span><span id="requeststatechangesupported"></span><span id="REQUESTSTATECHANGESUPPORTED"></span>

<span data-ttu-id="3346d-241">**RequestStateChangeSupported** (32789) </span><span class="sxs-lookup"><span data-stu-id="3346d-241">**RequestStateChangeSupported** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="StartServiceSupported"></span><span id="startservicesupported"></span><span id="STARTSERVICESUPPORTED"></span>

<span data-ttu-id="3346d-242">**StartServiceSupported** (32790) </span><span class="sxs-lookup"><span data-stu-id="3346d-242">**StartServiceSupported** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="StopServiceSupported"></span><span id="stopservicesupported"></span><span id="STOPSERVICESUPPORTED"></span>

<span data-ttu-id="3346d-243">**StopServiceSupported** (32791) </span><span class="sxs-lookup"><span data-stu-id="3346d-243">**StopServiceSupported** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyDiskMergeSettings"></span><span id="modifydiskmergesettings"></span><span id="MODIFYDISKMERGESETTINGS"></span>

<span data-ttu-id="3346d-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792) </span><span class="sxs-lookup"><span data-stu-id="3346d-244">**[**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)** (32792)</span></span>


</dt> <dd></dd> <dt>

<span id="GenerateWwpn"></span><span id="generatewwpn"></span><span id="GENERATEWWPN"></span>

<span data-ttu-id="3346d-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793) </span><span class="sxs-lookup"><span data-stu-id="3346d-245">**[**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)** (32793)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFibreChannelChap"></span><span id="addfibrechannelchap"></span><span id="ADDFIBRECHANNELCHAP"></span>

<span data-ttu-id="3346d-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794) </span><span class="sxs-lookup"><span data-stu-id="3346d-246">**[**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32794)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFibreChannelChap"></span><span id="removefibrechannelchap"></span><span id="REMOVEFIBRECHANNELCHAP"></span>

<span data-ttu-id="3346d-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795) </span><span class="sxs-lookup"><span data-stu-id="3346d-247">**[**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)** (32795)</span></span>


</dt> <dd></dd> <dt>

<span id="SetGuestNetworkAdapterConfiguration"></span><span id="setguestnetworkadapterconfiguration"></span><span id="SETGUESTNETWORKADAPTERCONFIGURATION"></span>

<span data-ttu-id="3346d-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796) </span><span class="sxs-lookup"><span data-stu-id="3346d-248">**[**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md)** (32796)</span></span>


</dt> <dd></dd> <dt>

<span id="GetSizeOfSystemFiles"></span><span id="getsizeofsystemfiles"></span><span id="GETSIZEOFSYSTEMFILES"></span>

<span data-ttu-id="3346d-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797) </span><span class="sxs-lookup"><span data-stu-id="3346d-249">**[**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)** (32797)</span></span>


</dt> <dd></dd> <dt>

<span id="GetCurrentWwpnFromGenerator"></span><span id="getcurrentwwpnfromgenerator"></span><span id="GETCURRENTWWPNFROMGENERATOR"></span>

<span data-ttu-id="3346d-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798) </span><span class="sxs-lookup"><span data-stu-id="3346d-250">**[**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)** (32798)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3346d-251">**廠商保留** (32799： 65535) </span><span class="sxs-lookup"><span data-stu-id="3346d-251">**Vendor Reserved** (32799..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3346d-252">**VirtualSystemTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="3346d-252">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3346d-253">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3346d-253">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3346d-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3346d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3346d-255">字串的陣列，每個字串都指定執行所支援的虛擬系統類型。</span><span class="sxs-lookup"><span data-stu-id="3346d-255">An array of strings each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="3346d-256">每個非 **Null** 陣列元素的值必須符合針對 [**Msvm \_ VirtualSystemSettingData. VirtualSystemType**](msvm-virtualsystemsettingdata.md) 屬性定義的字串。</span><span class="sxs-lookup"><span data-stu-id="3346d-256">The value of each non-**NULL** array element must conform to the strings defined for the [**Msvm\_VirtualSystemSettingData.VirtualSystemType**](msvm-virtualsystemsettingdata.md) property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3346d-257">規格需求</span><span class="sxs-lookup"><span data-stu-id="3346d-257">Requirements</span></span>



| <span data-ttu-id="3346d-258">需求</span><span class="sxs-lookup"><span data-stu-id="3346d-258">Requirement</span></span> | <span data-ttu-id="3346d-259">值</span><span class="sxs-lookup"><span data-stu-id="3346d-259">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3346d-260">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3346d-260">Minimum supported client</span></span><br/> | <span data-ttu-id="3346d-261">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3346d-261">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3346d-262">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3346d-262">Minimum supported server</span></span><br/> | <span data-ttu-id="3346d-263">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3346d-263">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3346d-264">命名空間</span><span class="sxs-lookup"><span data-stu-id="3346d-264">Namespace</span></span><br/>                | <span data-ttu-id="3346d-265">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3346d-265">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3346d-266">MOF</span><span class="sxs-lookup"><span data-stu-id="3346d-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3346d-267"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-267"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3346d-268">DLL</span><span class="sxs-lookup"><span data-stu-id="3346d-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3346d-269"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3346d-269"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

