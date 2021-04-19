---
description: 表示埠頻寬功能的狀態資料。
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Msvm_EthernetSwitchPortBandwidthData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970647"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="4acf4-103">Msvm \_ EthernetSwitchPortBandwidthData 類別</span><span class="sxs-lookup"><span data-stu-id="4acf4-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="4acf4-104">表示埠頻寬功能的狀態資料。</span><span class="sxs-lookup"><span data-stu-id="4acf4-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="4acf4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4acf4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4acf4-106">語法</span><span class="sxs-lookup"><span data-stu-id="4acf4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="4acf4-107">成員</span><span class="sxs-lookup"><span data-stu-id="4acf4-107">Members</span></span>

<span data-ttu-id="4acf4-108">**Msvm \_ EthernetSwitchPortBandwidthData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4acf4-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="4acf4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="4acf4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4acf4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4acf4-110">Properties</span></span>

<span data-ttu-id="4acf4-111">**Msvm \_ EthernetSwitchPortBandwidthData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4acf4-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4acf4-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="4acf4-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4acf4-115">A short description of the object.</span></span> <span data-ttu-id="4acf4-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠頻寬功能狀態」。</span><span class="sxs-lookup"><span data-stu-id="4acf4-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4acf4-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-120">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="4acf4-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-121">建立此埠資料實例時所使用的子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="4acf4-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="4acf4-122">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)，而且一律設定為 "Msvm \_ EthernetSwitchPortBandwidthData"。</span><span class="sxs-lookup"><span data-stu-id="4acf4-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-123">**CurrentBandwidthReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="4acf4-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4acf4-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4acf4-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-126">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="4acf4-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-127">為此埠保留的目前頻寬百分比。</span><span class="sxs-lookup"><span data-stu-id="4acf4-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="4acf4-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-131">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4acf4-131">A description of the object.</span></span> <span data-ttu-id="4acf4-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，且一律設定為「代表埠頻寬功能狀態資料」。</span><span class="sxs-lookup"><span data-stu-id="4acf4-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-133">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4acf4-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-136">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="4acf4-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-137">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="4acf4-137">The scoping system's creation class name.</span></span> <span data-ttu-id="4acf4-138">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)，而且一律設定為 "Msvm \_ EthernetSwitchPort"。</span><span class="sxs-lookup"><span data-stu-id="4acf4-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-139">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4acf4-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-142">限定詞： **Key**、 **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="4acf4-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-143">範圍此埠資料實例之埠的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="4acf4-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="4acf4-144">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)。</span><span class="sxs-lookup"><span data-stu-id="4acf4-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4acf4-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-148">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4acf4-148">A display name for the object.</span></span> <span data-ttu-id="4acf4-149">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠頻寬功能狀態」。</span><span class="sxs-lookup"><span data-stu-id="4acf4-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4acf4-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-153">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="4acf4-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-154">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4acf4-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4acf4-155">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4acf4-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-156">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4acf4-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-159">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="4acf4-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-160">在切換和埠範圍內唯一識別此埠資料實例的字串。</span><span class="sxs-lookup"><span data-stu-id="4acf4-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="4acf4-161">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)。</span><span class="sxs-lookup"><span data-stu-id="4acf4-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-162">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4acf4-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-165">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="4acf4-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-166">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="4acf4-166">The scoping system's creation class name.</span></span> <span data-ttu-id="4acf4-167">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)，而且一律設定為 "Msvm \_ VirtualEthernetSwitch"。</span><span class="sxs-lookup"><span data-stu-id="4acf4-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="4acf4-168">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4acf4-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4acf4-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4acf4-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4acf4-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4acf4-171">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="4acf4-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4acf4-172">範圍此埠資料實例的虛擬交換器名稱。</span><span class="sxs-lookup"><span data-stu-id="4acf4-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="4acf4-173">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)。</span><span class="sxs-lookup"><span data-stu-id="4acf4-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4acf4-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="4acf4-174">Requirements</span></span>



| <span data-ttu-id="4acf4-175">需求</span><span class="sxs-lookup"><span data-stu-id="4acf4-175">Requirement</span></span> | <span data-ttu-id="4acf4-176">值</span><span class="sxs-lookup"><span data-stu-id="4acf4-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4acf4-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4acf4-177">Minimum supported client</span></span><br/> | <span data-ttu-id="4acf4-178">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4acf4-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4acf4-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4acf4-179">Minimum supported server</span></span><br/> | <span data-ttu-id="4acf4-180">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4acf4-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4acf4-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="4acf4-181">Namespace</span></span><br/>                | <span data-ttu-id="4acf4-182">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4acf4-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4acf4-183">MOF</span><span class="sxs-lookup"><span data-stu-id="4acf4-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4acf4-184"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4acf4-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4acf4-185">DLL</span><span class="sxs-lookup"><span data-stu-id="4acf4-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4acf4-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4acf4-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

