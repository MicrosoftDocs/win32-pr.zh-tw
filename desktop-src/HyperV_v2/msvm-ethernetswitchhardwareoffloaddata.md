---
description: 代表交換器硬體卸載狀態。
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Msvm_EthernetSwitchHardwareOffloadData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985167"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="42eca-103">Msvm \_ EthernetSwitchHardwareOffloadData 類別</span><span class="sxs-lookup"><span data-stu-id="42eca-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="42eca-104">代表交換器硬體卸載狀態。</span><span class="sxs-lookup"><span data-stu-id="42eca-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="42eca-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="42eca-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42eca-106">語法</span><span class="sxs-lookup"><span data-stu-id="42eca-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="42eca-107">成員</span><span class="sxs-lookup"><span data-stu-id="42eca-107">Members</span></span>

<span data-ttu-id="42eca-108">**Msvm \_ EthernetSwitchHardwareOffloadData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42eca-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="42eca-109">屬性</span><span class="sxs-lookup"><span data-stu-id="42eca-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42eca-110">屬性</span><span class="sxs-lookup"><span data-stu-id="42eca-110">Properties</span></span>

<span data-ttu-id="42eca-111">**Msvm \_ EthernetSwitchHardwareOffloadData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42eca-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42eca-112">**標題**</span><span class="sxs-lookup"><span data-stu-id="42eca-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eca-115">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="42eca-115">A short description of the object.</span></span> <span data-ttu-id="42eca-116">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="42eca-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42eca-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-120">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="42eca-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-121">建立這個實例時所使用的類別或子類別名稱。</span><span class="sxs-lookup"><span data-stu-id="42eca-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="42eca-122">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="42eca-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-123">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="42eca-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-124">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="42eca-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-126">限定詞： **WmiDataId** (11) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-127">預設佇列的目前 VMMQ 設定</span><span class="sxs-lookup"><span data-stu-id="42eca-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="42eca-128">在 Windows 10 1703 版中加入的屬性。</span><span class="sxs-lookup"><span data-stu-id="42eca-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-129">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="42eca-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-132">限定詞： **WmiDataId** (12) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-133">目前配置給預設佇列的佇列數目</span><span class="sxs-lookup"><span data-stu-id="42eca-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="42eca-134">在 Windows 10 1703 版中加入的屬性。</span><span class="sxs-lookup"><span data-stu-id="42eca-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-135">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="42eca-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="42eca-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-138">限定詞： **WmiDataId** (10) 、 **InterfaceVersion** (3) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-139">預設佇列的目前 VRss 設定</span><span class="sxs-lookup"><span data-stu-id="42eca-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="42eca-140">在 Windows 10 1703 版中加入的屬性。</span><span class="sxs-lookup"><span data-stu-id="42eca-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-141">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="42eca-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-142">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="42eca-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-144">限定詞： **WmiDataId** (15) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-145">指出是否從 VRSS/VMMQ 間接資料表排除主要 VMQ CPU。</span><span class="sxs-lookup"><span data-stu-id="42eca-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="42eca-146">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="42eca-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-147">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="42eca-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="42eca-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-150">限定詞： **WmiDataId** (16) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-151">指出是否一律針對預設佇列進行 VRSS 分配，不論外部 vPort 的 RSS 狀態為何。</span><span class="sxs-lookup"><span data-stu-id="42eca-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="42eca-152">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="42eca-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-153">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="42eca-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-154">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-156">限定詞： **WmiDataId** (13) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-157">指出用於 VRSS/VMMQ 的佇列數目下限。</span><span class="sxs-lookup"><span data-stu-id="42eca-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="42eca-158">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="42eca-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-159">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="42eca-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-162">限定詞： **WmiDataId** (14) 、 **InterfaceVersion** (4) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-163">指出如何將 VRSS/VMMQ 佇列操縱至不同的主機處理器。</span><span class="sxs-lookup"><span data-stu-id="42eca-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="42eca-164">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="42eca-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-165">**說明**</span><span class="sxs-lookup"><span data-stu-id="42eca-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eca-168">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="42eca-168">A description of the object.</span></span> <span data-ttu-id="42eca-169">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="42eca-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="42eca-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eca-173">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="42eca-173">A display name for the object.</span></span> <span data-ttu-id="42eca-174">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="42eca-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42eca-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-178">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="42eca-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42eca-179">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="42eca-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="42eca-180">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="42eca-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-181">**IovQueuePairCapacity**</span><span class="sxs-lookup"><span data-stu-id="42eca-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-184">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-185">參數所支援的佇列配對數目上限。</span><span class="sxs-lookup"><span data-stu-id="42eca-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-186">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="42eca-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-189">限定詞： **WmiDataId** (8) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-190">參數目前正在使用的佇列組數。</span><span class="sxs-lookup"><span data-stu-id="42eca-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-191">**IovVfCapacity**</span><span class="sxs-lookup"><span data-stu-id="42eca-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-192">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-194">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-195">參數支援的虛擬函式數目上限。</span><span class="sxs-lookup"><span data-stu-id="42eca-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-196">**IovVfUsage**</span><span class="sxs-lookup"><span data-stu-id="42eca-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-199">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-200">目前參數正在使用的虛擬函式數目。</span><span class="sxs-lookup"><span data-stu-id="42eca-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-201">**IPsecSACapacity**</span><span class="sxs-lookup"><span data-stu-id="42eca-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-202">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-204">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-205">交換器支援的 IPsec 安全性關聯卸載數目上限。</span><span class="sxs-lookup"><span data-stu-id="42eca-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-206">**IPsecSAUsage**</span><span class="sxs-lookup"><span data-stu-id="42eca-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-207">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-209">限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-210">交換器正在使用的目前 IPsec 安全性關聯的數目。</span><span class="sxs-lookup"><span data-stu-id="42eca-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-211">**名稱**</span><span class="sxs-lookup"><span data-stu-id="42eca-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-214">限定詞： **Key**、 **Override**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="42eca-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-215">資源的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="42eca-215">The unique name of the resource.</span></span> <span data-ttu-id="42eca-216">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="42eca-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-217">**PacketDirectInUse**</span><span class="sxs-lookup"><span data-stu-id="42eca-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-218">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="42eca-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-220">限定詞： **WmiDataId** (9) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-221">指出交換器是否正在使用封包直接存取</span><span class="sxs-lookup"><span data-stu-id="42eca-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="42eca-222">在 Windows 10 中新增的屬性。</span><span class="sxs-lookup"><span data-stu-id="42eca-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eca-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="42eca-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-226">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="42eca-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-227">裝載系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="42eca-227">The hosting system's creation class name.</span></span> <span data-ttu-id="42eca-228">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="42eca-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="42eca-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="42eca-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-232">限定詞： **Key**、 **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="42eca-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-233">相關聯的資源實例所系結之虛擬交換器的名稱。</span><span class="sxs-lookup"><span data-stu-id="42eca-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="42eca-234">這個屬性繼承自 [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)。</span><span class="sxs-lookup"><span data-stu-id="42eca-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="42eca-235">**VmqCapacity**</span><span class="sxs-lookup"><span data-stu-id="42eca-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-236">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-238">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-239">交換器支援的虛擬機器佇列卸載數目上限。</span><span class="sxs-lookup"><span data-stu-id="42eca-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="42eca-240">**VmqUsage**</span><span class="sxs-lookup"><span data-stu-id="42eca-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eca-241">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="42eca-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eca-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42eca-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eca-243">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="42eca-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="42eca-244">交換器正在使用的目前虛擬機器佇列數目。</span><span class="sxs-lookup"><span data-stu-id="42eca-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42eca-245">規格需求</span><span class="sxs-lookup"><span data-stu-id="42eca-245">Requirements</span></span>



| <span data-ttu-id="42eca-246">需求</span><span class="sxs-lookup"><span data-stu-id="42eca-246">Requirement</span></span> | <span data-ttu-id="42eca-247">值</span><span class="sxs-lookup"><span data-stu-id="42eca-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42eca-248">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42eca-248">Minimum supported client</span></span><br/> | <span data-ttu-id="42eca-249">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42eca-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42eca-250">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42eca-250">Minimum supported server</span></span><br/> | <span data-ttu-id="42eca-251">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42eca-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42eca-252">命名空間</span><span class="sxs-lookup"><span data-stu-id="42eca-252">Namespace</span></span><br/>                | <span data-ttu-id="42eca-253">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="42eca-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42eca-254">MOF</span><span class="sxs-lookup"><span data-stu-id="42eca-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42eca-255"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="42eca-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42eca-256">DLL</span><span class="sxs-lookup"><span data-stu-id="42eca-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42eca-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42eca-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

