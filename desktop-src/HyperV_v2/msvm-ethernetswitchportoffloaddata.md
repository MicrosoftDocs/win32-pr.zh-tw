---
description: 表示埠卸載功能狀態資料。
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Msvm_EthernetSwitchPortOffloadData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981711"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="5ab29-103">Msvm \_ EthernetSwitchPortOffloadData 類別</span><span class="sxs-lookup"><span data-stu-id="5ab29-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="5ab29-104">表示埠卸載功能狀態資料。</span><span class="sxs-lookup"><span data-stu-id="5ab29-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="5ab29-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5ab29-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab29-106">語法</span><span class="sxs-lookup"><span data-stu-id="5ab29-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="5ab29-107">成員</span><span class="sxs-lookup"><span data-stu-id="5ab29-107">Members</span></span>

<span data-ttu-id="5ab29-108">**Msvm \_ EthernetSwitchPortOffloadData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5ab29-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="5ab29-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5ab29-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ab29-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5ab29-110">Properties</span></span>

<span data-ttu-id="5ab29-111">**Msvm \_ EthernetSwitchPortOffloadData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5ab29-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ab29-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="5ab29-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5ab29-115">A short description of the object.</span></span> <span data-ttu-id="5ab29-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠卸載功能狀態」。</span><span class="sxs-lookup"><span data-stu-id="5ab29-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ab29-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-120">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="5ab29-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-121">建立此埠資料實例時所使用的子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab29-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="5ab29-122">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)，而且一律設定為 "Msvm \_ EthernetSwitchPortOffloadData"。</span><span class="sxs-lookup"><span data-stu-id="5ab29-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="5ab29-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-126">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5ab29-126">A description of the object.</span></span> <span data-ttu-id="5ab29-127">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「代表埠卸載功能狀態資料」。</span><span class="sxs-lookup"><span data-stu-id="5ab29-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ab29-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-131">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="5ab29-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-132">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab29-132">The scoping system's creation class name.</span></span> <span data-ttu-id="5ab29-133">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)，而且一律設定為 "Msvm \_ EthernetSwitchPort"。</span><span class="sxs-lookup"><span data-stu-id="5ab29-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5ab29-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-137">限定詞： **Key**、 **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="5ab29-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-138">範圍此埠資料實例之埠的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ab29-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="5ab29-139">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5ab29-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-143">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab29-143">A display name for the object.</span></span> <span data-ttu-id="5ab29-144">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠卸載功能狀態」。</span><span class="sxs-lookup"><span data-stu-id="5ab29-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ab29-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-148">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="5ab29-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-149">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5ab29-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5ab29-150">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-151">**IovOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="5ab29-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-154">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-155">目前的 i/o 虛擬化 (的) 卸載使用方式。</span><span class="sxs-lookup"><span data-stu-id="5ab29-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-156">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="5ab29-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-159">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-160">埠目前正在使用的佇列組數。</span><span class="sxs-lookup"><span data-stu-id="5ab29-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-161">**IovVfDataPathActive**</span><span class="sxs-lookup"><span data-stu-id="5ab29-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-162">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab29-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-164">限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-165">指出是否為使用中的 SR-IOV VF 資料路徑。</span><span class="sxs-lookup"><span data-stu-id="5ab29-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-166">**IovVfId**</span><span class="sxs-lookup"><span data-stu-id="5ab29-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5ab29-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-169">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-170">指派給埠的目前的 SR-IOV VF 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ab29-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="5ab29-171">如果 **IovOffloadUsage** 不是零，這會是有效的。</span><span class="sxs-lookup"><span data-stu-id="5ab29-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-172">**IpsecCurrentOffloadSaCount**</span><span class="sxs-lookup"><span data-stu-id="5ab29-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-173">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-175">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-176">目前在埠上使用的 (SA) 卸載位置的安全性關聯數目。</span><span class="sxs-lookup"><span data-stu-id="5ab29-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-177">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5ab29-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-180">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="5ab29-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-181">在切換和埠範圍內唯一識別此埠資料實例的字串。</span><span class="sxs-lookup"><span data-stu-id="5ab29-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="5ab29-182">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-183">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ab29-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-186">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="5ab29-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-187">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab29-187">The scoping system's creation class name.</span></span> <span data-ttu-id="5ab29-188">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)，而且一律設定為 "Msvm \_ VirtualEthernetSwitch"。</span><span class="sxs-lookup"><span data-stu-id="5ab29-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-189">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5ab29-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5ab29-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-192">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="5ab29-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-193">範圍此埠資料實例的虛擬交換器名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab29-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="5ab29-194">這個屬性繼承自 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-195">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="5ab29-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab29-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-198">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-199">指出 VMMQ 是否作用中。</span><span class="sxs-lookup"><span data-stu-id="5ab29-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-200">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="5ab29-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-201">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="5ab29-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-202">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-204">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-205">指出用於 VRSS/VMMQ 的佇列數目。</span><span class="sxs-lookup"><span data-stu-id="5ab29-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-206">這個屬性是在 Windows 10、1703版和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="5ab29-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-207">**VMQId**</span><span class="sxs-lookup"><span data-stu-id="5ab29-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-209">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-210">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-211">指派給埠的目前虛擬機器佇列識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ab29-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="5ab29-212">如果 **VMQOffloadUsage** 不是零，這會是有效的。</span><span class="sxs-lookup"><span data-stu-id="5ab29-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-213">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="5ab29-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-214">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-215">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab29-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-216">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-217">目前的虛擬機器佇列 (VMQ) 卸載使用情形。</span><span class="sxs-lookup"><span data-stu-id="5ab29-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="5ab29-218">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="5ab29-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab29-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-221">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-222">指出是否已啟用 vRSS。</span><span class="sxs-lookup"><span data-stu-id="5ab29-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-223">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="5ab29-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-224">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="5ab29-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-225">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab29-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-227">限定詞： **WmiDataId** (13) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-228">指出是否從 VRSS/VMMQ 間接資料表排除主要 VMQ CPU。</span><span class="sxs-lookup"><span data-stu-id="5ab29-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-229">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="5ab29-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-230">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="5ab29-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5ab29-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-233">限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-234">指出不論虛擬 NIC 的 RSS 設定為何，是否會發生主機端 VRSS/VMMQ 分配。</span><span class="sxs-lookup"><span data-stu-id="5ab29-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-235">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="5ab29-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-236">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="5ab29-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-237">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-239">限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-240">指出用於 VRSS/VMMQ 的佇列數目下限。</span><span class="sxs-lookup"><span data-stu-id="5ab29-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-241">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="5ab29-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-242">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="5ab29-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-243">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-245">限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-246">指出如何將 VRSS/VMMQ 佇列操縱至不同的主機處理器。</span><span class="sxs-lookup"><span data-stu-id="5ab29-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-247">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="5ab29-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab29-248">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="5ab29-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab29-249">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ab29-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5ab29-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab29-251">限定詞： **WmiDataId** (15) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="5ab29-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5ab29-252">指出如何相似化為 Vmbus 通道來裝載處理器。</span><span class="sxs-lookup"><span data-stu-id="5ab29-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="5ab29-253">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="5ab29-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ab29-254">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ab29-254">Requirements</span></span>



| <span data-ttu-id="5ab29-255">需求</span><span class="sxs-lookup"><span data-stu-id="5ab29-255">Requirement</span></span> | <span data-ttu-id="5ab29-256">值</span><span class="sxs-lookup"><span data-stu-id="5ab29-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab29-257">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ab29-257">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab29-258">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ab29-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5ab29-259">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ab29-259">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab29-260">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ab29-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ab29-261">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ab29-261">Namespace</span></span><br/>                | <span data-ttu-id="5ab29-262">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5ab29-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5ab29-263">MOF</span><span class="sxs-lookup"><span data-stu-id="5ab29-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ab29-264"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5ab29-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ab29-265">DLL</span><span class="sxs-lookup"><span data-stu-id="5ab29-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ab29-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ab29-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

