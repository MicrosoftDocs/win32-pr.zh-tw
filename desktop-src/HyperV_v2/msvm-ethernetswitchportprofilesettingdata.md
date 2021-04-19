---
description: 代表通訊埠設定檔設定。
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Msvm_EthernetSwitchPortProfileSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988505"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a><span data-ttu-id="a4515-103">Msvm \_ EthernetSwitchPortProfileSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="a4515-103">Msvm\_EthernetSwitchPortProfileSettingData class</span></span>

<span data-ttu-id="a4515-104">代表通訊埠設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="a4515-104">Represents the port profile settings.</span></span>

<span data-ttu-id="a4515-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a4515-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4515-106">語法</span><span class="sxs-lookup"><span data-stu-id="a4515-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a><span data-ttu-id="a4515-107">成員</span><span class="sxs-lookup"><span data-stu-id="a4515-107">Members</span></span>

<span data-ttu-id="a4515-108">**Msvm \_ EthernetSwitchPortProfileSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a4515-108">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a4515-109">屬性</span><span class="sxs-lookup"><span data-stu-id="a4515-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4515-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a4515-110">Properties</span></span>

<span data-ttu-id="a4515-111">**Msvm \_ EthernetSwitchPortProfileSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a4515-111">The **Msvm\_EthernetSwitchPortProfileSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4515-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="a4515-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a4515-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4515-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a4515-115">A short description of the object.</span></span> <span data-ttu-id="a4515-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠設定檔設定」。</span><span class="sxs-lookup"><span data-stu-id="a4515-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a4515-117">**CdnLabelId**</span><span class="sxs-lookup"><span data-stu-id="a4515-117">**CdnLabelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4515-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-120">限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-120">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-121">CDN 標籤識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4515-121">The CDN label identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-122">**CdnLabelString**</span><span class="sxs-lookup"><span data-stu-id="a4515-122">**CdnLabelString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-125">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (12) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (12), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-126">CDN 標籤字串。</span><span class="sxs-lookup"><span data-stu-id="a4515-126">The CDN label string.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-127">**說明**</span><span class="sxs-lookup"><span data-stu-id="a4515-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a4515-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4515-130">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a4515-130">A description of the object.</span></span> <span data-ttu-id="a4515-131">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「代表通訊埠設定檔設定」。</span><span class="sxs-lookup"><span data-stu-id="a4515-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port profile settings.".</span></span>

</dd> <dt>

<span data-ttu-id="a4515-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a4515-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a4515-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4515-135">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a4515-135">A display name for the object.</span></span> <span data-ttu-id="a4515-136">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器通訊埠設定檔設定」。</span><span class="sxs-lookup"><span data-stu-id="a4515-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Profile Settings".</span></span>

</dd> <dt>

<span data-ttu-id="a4515-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a4515-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a4515-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4515-140">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a4515-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a4515-141">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a4515-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a4515-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a4515-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a4515-143">**NetCfgInstanceId**</span><span class="sxs-lookup"><span data-stu-id="a4515-143">**NetCfgInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-146">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-147">子介面的唯一裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4515-147">An unique device identifier of the subinterface.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-148">**PciBusNumber**</span><span class="sxs-lookup"><span data-stu-id="a4515-148">**PciBusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4515-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-151">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-151">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-152">PCI 匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="a4515-152">The PCI bus number.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-153">**PciDeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="a4515-153">**PciDeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4515-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-156">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-156">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-157">PCI 裝置編號。</span><span class="sxs-lookup"><span data-stu-id="a4515-157">The PCI device number.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-158">**PciFunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="a4515-158">**PciFunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4515-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-161">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-161">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-162">PCI 函數編號。</span><span class="sxs-lookup"><span data-stu-id="a4515-162">The PCI function number.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-163">**PciSegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="a4515-163">**PciSegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-164">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4515-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-166">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-166">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-167">PCI 區段編號。</span><span class="sxs-lookup"><span data-stu-id="a4515-167">The PCI segment number.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-168">**ProfileData**</span><span class="sxs-lookup"><span data-stu-id="a4515-168">**ProfileData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-169">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4515-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-171">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-171">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-172">通訊埠設定檔的其他資料。</span><span class="sxs-lookup"><span data-stu-id="a4515-172">Additional data for the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-173">**ProfileId**</span><span class="sxs-lookup"><span data-stu-id="a4515-173">**ProfileId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-176">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-177">通訊埠設定檔的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4515-177">The identifier of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-178">**ProfileName**</span><span class="sxs-lookup"><span data-stu-id="a4515-178">**ProfileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-181">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-182">通訊埠設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4515-182">The name of the port profile.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-183">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="a4515-183">**VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-186">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38) 、 **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-187">定義設定檔的供應商識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4515-187">The identifier of the vendor defining the profile.</span></span>

</dd> <dt>

<span data-ttu-id="a4515-188">**VendorName**</span><span class="sxs-lookup"><span data-stu-id="a4515-188">**VendorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4515-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a4515-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4515-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4515-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a4515-191">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127) 、 **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="a4515-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="a4515-192">定義設定檔的廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="a4515-192">The name of the vendor defining the profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a4515-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4515-193">Requirements</span></span>



| <span data-ttu-id="a4515-194">需求</span><span class="sxs-lookup"><span data-stu-id="a4515-194">Requirement</span></span> | <span data-ttu-id="a4515-195">值</span><span class="sxs-lookup"><span data-stu-id="a4515-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4515-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4515-196">Minimum supported client</span></span><br/> | <span data-ttu-id="a4515-197">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4515-197">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4515-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4515-198">Minimum supported server</span></span><br/> | <span data-ttu-id="a4515-199">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4515-199">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4515-200">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4515-200">Namespace</span></span><br/>                | <span data-ttu-id="a4515-201">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a4515-201">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4515-202">MOF</span><span class="sxs-lookup"><span data-stu-id="a4515-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4515-203"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a4515-203"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4515-204">DLL</span><span class="sxs-lookup"><span data-stu-id="a4515-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4515-205"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4515-205"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

