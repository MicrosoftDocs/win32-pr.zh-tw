---
description: 代表切換卸載設定。
ms.assetid: 4e00544e-a8db-4337-af3f-f651bfcf6b05
title: Msvm_EthernetSwitchHardwareOffloadSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadSettingData
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadSettingData.DefaultQueueVrssMinQueuePairs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ef0e22143ffd424ee3acee616504e45d8125bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988082"
---
# <a name="msvm_ethernetswitchhardwareoffloadsettingdata-class"></a><span data-ttu-id="47a8d-103">Msvm \_ EthernetSwitchHardwareOffloadSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="47a8d-103">Msvm\_EthernetSwitchHardwareOffloadSettingData class</span></span>

<span data-ttu-id="47a8d-104">代表切換卸載設定。</span><span class="sxs-lookup"><span data-stu-id="47a8d-104">Represents the switch offload settings.</span></span>

<span data-ttu-id="47a8d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="47a8d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47a8d-106">語法</span><span class="sxs-lookup"><span data-stu-id="47a8d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1550e863-4337-4917-a040-5a27dbc58b59"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("2"), InterfaceRevision("0"), DisplayName("Ethernet Switch Hardware Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  boolean DefaultQueueVrssEnabled = TRUE;
  boolean DefaultQueueVmmqEnabled = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 16;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 2;
  uint32  DefaultQueueVrssMinQueuePairs = 1;
};
```

## <a name="members"></a><span data-ttu-id="47a8d-107">成員</span><span class="sxs-lookup"><span data-stu-id="47a8d-107">Members</span></span>

<span data-ttu-id="47a8d-108">**Msvm \_ EthernetSwitchHardwareOffloadSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="47a8d-108">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="47a8d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="47a8d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47a8d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="47a8d-110">Properties</span></span>

<span data-ttu-id="47a8d-111">**Msvm \_ EthernetSwitchHardwareOffloadSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="47a8d-111">The **Msvm\_EthernetSwitchHardwareOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47a8d-112">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="47a8d-112">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="47a8d-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47a8d-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-115">限定詞： **WmiDataId** (2) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-116">指定 vswitch 預設佇列的 VMMQ 設定。</span><span class="sxs-lookup"><span data-stu-id="47a8d-116">Specifies the VMMQ settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="47a8d-117">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="47a8d-117">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="47a8d-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47a8d-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-120">限定詞： **WmiDataId** (3) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-120">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-121">指定預設佇列的佇列數目。</span><span class="sxs-lookup"><span data-stu-id="47a8d-121">Specifies the number of queues for the default queue.</span></span>

</dd> <dt>

<span data-ttu-id="47a8d-122">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="47a8d-122">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="47a8d-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47a8d-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-125">限定詞： **WmiDataId** (1) 、 **InterfaceVersion** (1) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-125">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-126">指定 vswitch 預設佇列的 VRss 設定。</span><span class="sxs-lookup"><span data-stu-id="47a8d-126">Specifies the VRss settings for the default queue of the vswitch.</span></span>

</dd> <dt>

<span data-ttu-id="47a8d-127">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="47a8d-127">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="47a8d-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47a8d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-130">限定詞： **WmiDataId** (6) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-130">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-131">指出是否從 VRSS/VMMQ 間接資料表排除主要 VMQ CPU。</span><span class="sxs-lookup"><span data-stu-id="47a8d-131">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="47a8d-132">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="47a8d-132">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="47a8d-133">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="47a8d-133">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="47a8d-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47a8d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-136">限定詞： **WmiDataId** (7) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-136">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-137">指出是否一律針對預設佇列進行 VRSS 分配，不論外部 vPort 的 RSS 狀態為何。</span><span class="sxs-lookup"><span data-stu-id="47a8d-137">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="47a8d-138">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="47a8d-138">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="47a8d-139">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="47a8d-139">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="47a8d-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47a8d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-142">限定詞： **WmiDataId** (4) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-142">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-143">指出用於 VRSS/VMMQ 的佇列數目下限。</span><span class="sxs-lookup"><span data-stu-id="47a8d-143">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="47a8d-144">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="47a8d-144">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="47a8d-145">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="47a8d-145">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47a8d-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="47a8d-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47a8d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47a8d-148">限定詞： **WmiDataId** (5) 、 **InterfaceVersion** (2) 、 **InterfaceRevision** (0) </span><span class="sxs-lookup"><span data-stu-id="47a8d-148">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="47a8d-149">指出如何將 VRSS/VMMQ 佇列操縱至不同的主機處理器。</span><span class="sxs-lookup"><span data-stu-id="47a8d-149">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="47a8d-150">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="47a8d-150">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47a8d-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="47a8d-151">Requirements</span></span>



| <span data-ttu-id="47a8d-152">需求</span><span class="sxs-lookup"><span data-stu-id="47a8d-152">Requirement</span></span> | <span data-ttu-id="47a8d-153">值</span><span class="sxs-lookup"><span data-stu-id="47a8d-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a8d-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47a8d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="47a8d-155">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47a8d-155">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="47a8d-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47a8d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="47a8d-157">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="47a8d-157">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="47a8d-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="47a8d-158">Namespace</span></span><br/>                | <span data-ttu-id="47a8d-159">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="47a8d-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="47a8d-160">MOF</span><span class="sxs-lookup"><span data-stu-id="47a8d-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47a8d-161"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="47a8d-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="47a8d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="47a8d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47a8d-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="47a8d-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="47a8d-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47a8d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a8d-165">**Msvm \_ EthernetSwitchFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="47a8d-165">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




