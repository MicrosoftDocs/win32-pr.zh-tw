---
description: 代表設定資料的虛擬 LAN (VLAN) 。
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Msvm_EthernetSwitchPortVlanSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992617"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="92eef-103">Msvm \_ EthernetSwitchPortVlanSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="92eef-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="92eef-104">代表設定資料的虛擬 LAN (VLAN) 。</span><span class="sxs-lookup"><span data-stu-id="92eef-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="92eef-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="92eef-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92eef-106">語法</span><span class="sxs-lookup"><span data-stu-id="92eef-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="92eef-107">成員</span><span class="sxs-lookup"><span data-stu-id="92eef-107">Members</span></span>

<span data-ttu-id="92eef-108">**Msvm \_ EthernetSwitchPortVlanSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="92eef-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="92eef-109">屬性</span><span class="sxs-lookup"><span data-stu-id="92eef-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92eef-110">屬性</span><span class="sxs-lookup"><span data-stu-id="92eef-110">Properties</span></span>

<span data-ttu-id="92eef-111">**Msvm \_ EthernetSwitchPortVlanSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="92eef-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92eef-112">**AccessVlanId**</span><span class="sxs-lookup"><span data-stu-id="92eef-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92eef-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-115">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-116">在存取模式中指定 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="92eef-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="92eef-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="92eef-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92eef-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92eef-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92eef-120">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="92eef-120">A short description of the object.</span></span> <span data-ttu-id="92eef-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠 VLAN 設定」。</span><span class="sxs-lookup"><span data-stu-id="92eef-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="92eef-122">**說明**</span><span class="sxs-lookup"><span data-stu-id="92eef-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92eef-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92eef-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92eef-125">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="92eef-125">A description of the object.</span></span> <span data-ttu-id="92eef-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「代表 vlan 設定資料」。</span><span class="sxs-lookup"><span data-stu-id="92eef-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="92eef-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="92eef-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92eef-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92eef-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92eef-130">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="92eef-130">A display name for the object.</span></span> <span data-ttu-id="92eef-131">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠 VLAN 設定」。</span><span class="sxs-lookup"><span data-stu-id="92eef-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="92eef-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="92eef-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="92eef-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="92eef-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92eef-135">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="92eef-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="92eef-136">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="92eef-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="92eef-137">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="92eef-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92eef-138">**NativeVlanId**</span><span class="sxs-lookup"><span data-stu-id="92eef-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92eef-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-141">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-142">指定主幹模式中的 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="92eef-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="92eef-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="92eef-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-144">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92eef-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-146">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-147">指定 VLAN 操作模式。</span><span class="sxs-lookup"><span data-stu-id="92eef-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="92eef-148">**存取** (1) </span><span class="sxs-lookup"><span data-stu-id="92eef-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="92eef-149">**主幹** (2) </span><span class="sxs-lookup"><span data-stu-id="92eef-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="92eef-150">**私** 用 (3) </span><span class="sxs-lookup"><span data-stu-id="92eef-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92eef-151">**PrimaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="92eef-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-152">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92eef-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-154">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-155">以私用模式指定主要 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="92eef-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="92eef-156">**PruneVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="92eef-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-157">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="92eef-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="92eef-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-159">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-160">指定主幹模式中的剪除 VLAN 識別碼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="92eef-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="92eef-161">**PvlanMode**</span><span class="sxs-lookup"><span data-stu-id="92eef-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="92eef-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-164">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-165">指定私用 VLAN 模式。</span><span class="sxs-lookup"><span data-stu-id="92eef-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="92eef-166">**隔離** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="92eef-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="92eef-167">**社區** (2) </span><span class="sxs-lookup"><span data-stu-id="92eef-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="92eef-168">**混合** (3) </span><span class="sxs-lookup"><span data-stu-id="92eef-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92eef-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="92eef-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-170">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="92eef-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92eef-171">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-172">限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-173">指定私用模式中的次要 VLAN 識別碼。</span><span class="sxs-lookup"><span data-stu-id="92eef-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="92eef-174">**SecondaryVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="92eef-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-175">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="92eef-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="92eef-176">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-177">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-178">指定私用模式中的次要 VLAN 識別碼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="92eef-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="92eef-179">**TrunkVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="92eef-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92eef-180">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="92eef-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="92eef-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92eef-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92eef-182">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="92eef-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="92eef-183">指定主幹模式中的主幹 VLAN 識別碼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="92eef-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92eef-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="92eef-184">Requirements</span></span>



| <span data-ttu-id="92eef-185">需求</span><span class="sxs-lookup"><span data-stu-id="92eef-185">Requirement</span></span> | <span data-ttu-id="92eef-186">值</span><span class="sxs-lookup"><span data-stu-id="92eef-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92eef-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92eef-187">Minimum supported client</span></span><br/> | <span data-ttu-id="92eef-188">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92eef-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="92eef-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92eef-189">Minimum supported server</span></span><br/> | <span data-ttu-id="92eef-190">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92eef-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92eef-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="92eef-191">Namespace</span></span><br/>                | <span data-ttu-id="92eef-192">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="92eef-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="92eef-193">MOF</span><span class="sxs-lookup"><span data-stu-id="92eef-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92eef-194"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="92eef-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92eef-195">DLL</span><span class="sxs-lookup"><span data-stu-id="92eef-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92eef-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92eef-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

