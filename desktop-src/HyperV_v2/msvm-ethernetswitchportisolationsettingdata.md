---
description: 表示隔離設定資料。
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Msvm_EthernetSwitchPortIsolationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987598"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="59bd4-103">Msvm \_ EthernetSwitchPortIsolationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="59bd4-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="59bd4-104">表示隔離設定資料。</span><span class="sxs-lookup"><span data-stu-id="59bd4-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="59bd4-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="59bd4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59bd4-106">語法</span><span class="sxs-lookup"><span data-stu-id="59bd4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="59bd4-107">成員</span><span class="sxs-lookup"><span data-stu-id="59bd4-107">Members</span></span>

<span data-ttu-id="59bd4-108">**Msvm \_ EthernetSwitchPortIsolationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="59bd4-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="59bd4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="59bd4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59bd4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="59bd4-110">Properties</span></span>

<span data-ttu-id="59bd4-111">**Msvm \_ EthernetSwitchPortIsolationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="59bd4-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59bd4-112">**AllowUntaggedTraffic**</span><span class="sxs-lookup"><span data-stu-id="59bd4-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59bd4-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59bd4-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="59bd4-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-115">限定詞： **WmiDataId** (2) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="59bd4-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="59bd4-116">是否允許埠傳送/接收未標記的流量。</span><span class="sxs-lookup"><span data-stu-id="59bd4-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="59bd4-117">**DefaultIsolationId**</span><span class="sxs-lookup"><span data-stu-id="59bd4-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59bd4-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="59bd4-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="59bd4-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-120">限定詞： **WmiDataId** (3) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="59bd4-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="59bd4-121">當 **AllowedUntaggedTraffic** 為 **true** 時，將在所有傳送/接收流量上設定的預設 VirtualSubnetId 或 VLAN。</span><span class="sxs-lookup"><span data-stu-id="59bd4-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="59bd4-122">**EnableMultiTenantStack**</span><span class="sxs-lookup"><span data-stu-id="59bd4-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59bd4-123">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="59bd4-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="59bd4-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-125">限定詞： **WmiDataId** (4) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="59bd4-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="59bd4-126">若 **為 true**，VM 中的網路堆疊將能夠存取隔離設定。</span><span class="sxs-lookup"><span data-stu-id="59bd4-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="59bd4-127">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="59bd4-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="59bd4-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="59bd4-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59bd4-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="59bd4-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="59bd4-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="59bd4-131">限定詞： **WmiDataId** (1) 、 [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**修訂**](/windows/desktop/WmiSdk/standard-qualifiers) (0) </span><span class="sxs-lookup"><span data-stu-id="59bd4-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="59bd4-132">埠是否使用 **VLAN** 或 **VirtualSubnetId** 進行隔離。</span><span class="sxs-lookup"><span data-stu-id="59bd4-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="59bd4-133">**NativeVirtualSubnetId** 可用於 WNV VirtualSubnetId 型網路。</span><span class="sxs-lookup"><span data-stu-id="59bd4-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="59bd4-134">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="59bd4-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="59bd4-135">**NativeVirtualSubnetId** (1) </span><span class="sxs-lookup"><span data-stu-id="59bd4-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="59bd4-136">**ExternalVirtualSubnetId** (2) </span><span class="sxs-lookup"><span data-stu-id="59bd4-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="59bd4-137">**VLAN** (3) </span><span class="sxs-lookup"><span data-stu-id="59bd4-137">**VLAN** (3)</span></span>


<span data-ttu-id="59bd4-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="59bd4-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="59bd4-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="59bd4-139">Requirements</span></span>



| <span data-ttu-id="59bd4-140">需求</span><span class="sxs-lookup"><span data-stu-id="59bd4-140">Requirement</span></span> | <span data-ttu-id="59bd4-141">值</span><span class="sxs-lookup"><span data-stu-id="59bd4-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59bd4-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59bd4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="59bd4-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="59bd4-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="59bd4-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59bd4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="59bd4-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="59bd4-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="59bd4-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="59bd4-146">Namespace</span></span><br/>                | <span data-ttu-id="59bd4-147">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="59bd4-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="59bd4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="59bd4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59bd4-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="59bd4-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59bd4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="59bd4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59bd4-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59bd4-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59bd4-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59bd4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bd4-153">**Msvm \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="59bd4-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

