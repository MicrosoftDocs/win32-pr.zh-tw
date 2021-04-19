---
description: 表示埠卸載功能設定資料。
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Msvm_EthernetSwitchPortOffloadSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988081"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="ad08f-103">Msvm \_ EthernetSwitchPortOffloadSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="ad08f-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="ad08f-104">表示埠卸載功能設定資料。</span><span class="sxs-lookup"><span data-stu-id="ad08f-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="ad08f-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad08f-106">語法</span><span class="sxs-lookup"><span data-stu-id="ad08f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a><span data-ttu-id="ad08f-107">成員</span><span class="sxs-lookup"><span data-stu-id="ad08f-107">Members</span></span>

<span data-ttu-id="ad08f-108">**Msvm \_ EthernetSwitchPortOffloadSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ad08f-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ad08f-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ad08f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad08f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ad08f-110">Properties</span></span>

<span data-ttu-id="ad08f-111">**Msvm \_ EthernetSwitchPortOffloadSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad08f-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="ad08f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad08f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad08f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ad08f-115">A short description of the object.</span></span> <span data-ttu-id="ad08f-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠卸載設定」。</span><span class="sxs-lookup"><span data-stu-id="ad08f-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-117">**說明**</span><span class="sxs-lookup"><span data-stu-id="ad08f-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad08f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad08f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-120">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ad08f-120">A description of the object.</span></span> <span data-ttu-id="ad08f-121">這個屬性會繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，而且一律會設定為「代表埠卸載功能設定資料」。</span><span class="sxs-lookup"><span data-stu-id="ad08f-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ad08f-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad08f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad08f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-125">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ad08f-125">A display name for the object.</span></span> <span data-ttu-id="ad08f-126">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「乙太網路交換器埠卸載設定」。</span><span class="sxs-lookup"><span data-stu-id="ad08f-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad08f-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad08f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad08f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-130">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ad08f-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-131">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ad08f-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ad08f-132">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ad08f-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-133">**IOVInterruptModeration**</span><span class="sxs-lookup"><span data-stu-id="ad08f-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-134">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-136">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-137">I/o 虛擬化的中斷仲裁值 (插) 卸載。</span><span class="sxs-lookup"><span data-stu-id="ad08f-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="ad08f-138">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="ad08f-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="ad08f-139">**預設** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="ad08f-140">**適應性** (1) </span><span class="sxs-lookup"><span data-stu-id="ad08f-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="ad08f-141">**關閉** (2) </span><span class="sxs-lookup"><span data-stu-id="ad08f-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="ad08f-142">**低** (100) </span><span class="sxs-lookup"><span data-stu-id="ad08f-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="ad08f-143">**中型** (200) </span><span class="sxs-lookup"><span data-stu-id="ad08f-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="ad08f-144">**高** (300) </span><span class="sxs-lookup"><span data-stu-id="ad08f-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad08f-145">**IOVOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="ad08f-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-148">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-149">指派給此埠以進行 i/o 虛擬化 (的權數) 卸載。</span><span class="sxs-lookup"><span data-stu-id="ad08f-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="ad08f-150">權數是指派的 SR-IOV 資源時的相對重要性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="ad08f-151">將 **IOVOffloadWeight** 屬性設定為0會停用埠上的 sr-iov 卸載。</span><span class="sxs-lookup"><span data-stu-id="ad08f-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="ad08f-152">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="ad08f-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-153">**IOVQueuePairsRequested**</span><span class="sxs-lookup"><span data-stu-id="ad08f-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-156">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-157">針對此埠 (的 i/o 虛擬化所要求的佇列配對數目) 卸載。</span><span class="sxs-lookup"><span data-stu-id="ad08f-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="ad08f-158">預設值是 1。</span><span class="sxs-lookup"><span data-stu-id="ad08f-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-159">**IPSecOffloadLimit**</span><span class="sxs-lookup"><span data-stu-id="ad08f-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-162">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-163">允許從埠 (SA) 卸載位置的安全性關聯數目上限。</span><span class="sxs-lookup"><span data-stu-id="ad08f-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-164">**PacketDirectModerationCount**</span><span class="sxs-lookup"><span data-stu-id="ad08f-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-165">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-167">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-168">封包直接 (PD) 的中斷仲裁計數值。預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ad08f-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-169">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-170">**PacketDirectModerationInterval**</span><span class="sxs-lookup"><span data-stu-id="ad08f-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-173">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-174">封包直接 (PD) 的中斷仲裁間隔值。預設值為0。</span><span class="sxs-lookup"><span data-stu-id="ad08f-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-175">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-176">**PacketDirectNumProcs**</span><span class="sxs-lookup"><span data-stu-id="ad08f-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-179">限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-180">主機用來處理封包直接模式中從此埠傳送之封包的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="ad08f-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="ad08f-181">預設值是 1。</span><span class="sxs-lookup"><span data-stu-id="ad08f-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-182">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-183">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="ad08f-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad08f-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-186">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-187">如果硬體支援，請啟用 VMMQ 卸載。預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="ad08f-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-188">這個屬性是在 Windows 10、1703版和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="ad08f-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-189">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="ad08f-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-190">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-191">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-192">限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-193">啟用 VRSS 時要配置的佇列數目。</span><span class="sxs-lookup"><span data-stu-id="ad08f-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="ad08f-194">預設值是 16。</span><span class="sxs-lookup"><span data-stu-id="ad08f-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-195">這個屬性是在 Windows 10、1703版和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="ad08f-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-196">**VMQOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="ad08f-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-199">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-200">指派給此埠的虛擬機器佇列 (VMQ) 卸載的加權。</span><span class="sxs-lookup"><span data-stu-id="ad08f-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="ad08f-201">加權是指派 VMQ 資源時的相對重要性。</span><span class="sxs-lookup"><span data-stu-id="ad08f-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="ad08f-202">將 **VMQOffloadWeight** 屬性設定為0會停用埠上的 VMQ。</span><span class="sxs-lookup"><span data-stu-id="ad08f-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="ad08f-203">預設值為 100。</span><span class="sxs-lookup"><span data-stu-id="ad08f-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="ad08f-204">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="ad08f-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-205">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad08f-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-206">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-207">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-208">啟用 VRSS。</span><span class="sxs-lookup"><span data-stu-id="ad08f-208">Enable VRSS.</span></span> <span data-ttu-id="ad08f-209">預設值是 true。</span><span class="sxs-lookup"><span data-stu-id="ad08f-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-210">這個屬性是在 Windows 10、1703版和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="ad08f-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-211">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="ad08f-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-212">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad08f-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-213">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-214">限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-215">是否要在啟用 VRSS 時，從 VRSS 間接資料表中排除主要 VMQ 處理器。預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="ad08f-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-216">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="ad08f-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-217">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="ad08f-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-218">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad08f-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-219">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-220">限定詞： **WmiDataId** (15) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-221">無論虛擬 NIC 的 RSS 設定為何，都要在啟用 VRSS 時一律進行主機端 VRSS。預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="ad08f-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-222">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="ad08f-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-223">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="ad08f-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-224">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-225">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-226">限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-227">啟用 VRSS 時要配置的佇列數目下限。預設值為1。</span><span class="sxs-lookup"><span data-stu-id="ad08f-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-228">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="ad08f-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-229">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="ad08f-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-230">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-231">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-232">限定詞： **WmiDataId** (13) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-233">啟用 VRSS 時要使用的佇列排程模式。預設值為靜態排程。</span><span class="sxs-lookup"><span data-stu-id="ad08f-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-234">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="ad08f-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="ad08f-235">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="ad08f-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad08f-236">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad08f-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-237">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ad08f-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ad08f-238">限定詞： **WmiDataId** (16) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="ad08f-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ad08f-239">啟用 VRSS 時要使用的 vmbus 通道親和性原則。預設值為 [強式]。</span><span class="sxs-lookup"><span data-stu-id="ad08f-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="ad08f-240">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="ad08f-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad08f-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad08f-241">Requirements</span></span>



| <span data-ttu-id="ad08f-242">需求</span><span class="sxs-lookup"><span data-stu-id="ad08f-242">Requirement</span></span> | <span data-ttu-id="ad08f-243">值</span><span class="sxs-lookup"><span data-stu-id="ad08f-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad08f-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad08f-244">Minimum supported client</span></span><br/> | <span data-ttu-id="ad08f-245">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad08f-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ad08f-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad08f-246">Minimum supported server</span></span><br/> | <span data-ttu-id="ad08f-247">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad08f-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad08f-248">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad08f-248">Namespace</span></span><br/>                | <span data-ttu-id="ad08f-249">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ad08f-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ad08f-250">MOF</span><span class="sxs-lookup"><span data-stu-id="ad08f-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad08f-251"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ad08f-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad08f-252">DLL</span><span class="sxs-lookup"><span data-stu-id="ad08f-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad08f-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad08f-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

