---
description: 代表切換頻寬資源狀態。
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Msvm_EthernetSwitchBandwidthData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985406"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="c041a-103">Msvm \_ EthernetSwitchBandwidthData 類別</span><span class="sxs-lookup"><span data-stu-id="c041a-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="c041a-104">代表切換頻寬資源狀態。</span><span class="sxs-lookup"><span data-stu-id="c041a-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="c041a-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c041a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c041a-106">語法</span><span class="sxs-lookup"><span data-stu-id="c041a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="c041a-107">成員</span><span class="sxs-lookup"><span data-stu-id="c041a-107">Members</span></span>

<span data-ttu-id="c041a-108">**Msvm \_ EthernetSwitchBandwidthData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c041a-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="c041a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="c041a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c041a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c041a-110">Properties</span></span>

<span data-ttu-id="c041a-111">**Msvm \_ EthernetSwitchBandwidthData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c041a-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c041a-112">**容量**</span><span class="sxs-lookup"><span data-stu-id="c041a-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-113">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c041a-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-115">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="c041a-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-116">交換器可用的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="c041a-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="c041a-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c041a-120">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c041a-120">A short description of the object.</span></span> <span data-ttu-id="c041a-121">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c041a-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c041a-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c041a-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-125">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c041a-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-126">建立這個實例時所使用的類別或子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c041a-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-127">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="c041a-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c041a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-130">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="c041a-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-131">預設流程在交換器上保留的目前絕對頻寬。</span><span class="sxs-lookup"><span data-stu-id="c041a-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-132">**DefaultFlowReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="c041a-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c041a-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-135">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="c041a-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-136">預設流程在交換器上保留的目前頻寬百分比。</span><span class="sxs-lookup"><span data-stu-id="c041a-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-137">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="c041a-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-138">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c041a-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-140">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="c041a-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-141">切換上預設流程的目前加權。</span><span class="sxs-lookup"><span data-stu-id="c041a-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-142">**說明**</span><span class="sxs-lookup"><span data-stu-id="c041a-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c041a-145">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c041a-145">A description of the object.</span></span> <span data-ttu-id="c041a-146">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c041a-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c041a-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c041a-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c041a-150">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c041a-150">A display name for the object.</span></span> <span data-ttu-id="c041a-151">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c041a-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c041a-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c041a-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-155">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="c041a-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c041a-156">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c041a-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c041a-157">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c041a-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c041a-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c041a-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-161">限定詞： **Key**、 **Override**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c041a-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-162">資源的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="c041a-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-163">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="c041a-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-164">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c041a-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-166">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="c041a-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-167">目前保留在交換器上的頻寬。</span><span class="sxs-lookup"><span data-stu-id="c041a-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="c041a-168">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c041a-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-171">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c041a-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-172">裝載系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c041a-172">The hosting system's creation class name.</span></span> <span data-ttu-id="c041a-173">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="c041a-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c041a-174">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c041a-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c041a-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c041a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c041a-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c041a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c041a-177">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c041a-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c041a-178">相關聯的資源實例所系結之虛擬交換器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c041a-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c041a-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="c041a-179">Requirements</span></span>



| <span data-ttu-id="c041a-180">需求</span><span class="sxs-lookup"><span data-stu-id="c041a-180">Requirement</span></span> | <span data-ttu-id="c041a-181">值</span><span class="sxs-lookup"><span data-stu-id="c041a-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c041a-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c041a-182">Minimum supported client</span></span><br/> | <span data-ttu-id="c041a-183">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c041a-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c041a-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c041a-184">Minimum supported server</span></span><br/> | <span data-ttu-id="c041a-185">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c041a-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c041a-186">命名空間</span><span class="sxs-lookup"><span data-stu-id="c041a-186">Namespace</span></span><br/>                | <span data-ttu-id="c041a-187">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c041a-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c041a-188">MOF</span><span class="sxs-lookup"><span data-stu-id="c041a-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c041a-189"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c041a-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c041a-190">DLL</span><span class="sxs-lookup"><span data-stu-id="c041a-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c041a-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c041a-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

