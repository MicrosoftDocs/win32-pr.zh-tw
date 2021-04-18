---
description: 用於 Msvm VssService 類別中的 QueryGuestClusterInformation 方法 \_ ，以抓取 VM 所屬之來賓叢集的相關資訊。
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971257"
---
# <a name="msvm_guestclusterinformation-class"></a><span data-ttu-id="2d67a-103">Msvm \_ GuestClusterInformation 類別</span><span class="sxs-lookup"><span data-stu-id="2d67a-103">Msvm\_GuestClusterInformation class</span></span>

<span data-ttu-id="2d67a-104">用於 [**Msvm \_ VssService**](msvm-vssservice.md)類別中的 [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md)方法，以抓取 VM 所屬之來賓叢集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d67a-104">Used in the [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) method in the [**Msvm\_VssService**](msvm-vssservice.md) class to retrieve information about the guest cluster the VM is part of.</span></span>

<span data-ttu-id="2d67a-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d67a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d67a-106">語法</span><span class="sxs-lookup"><span data-stu-id="2d67a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a><span data-ttu-id="2d67a-107">成員</span><span class="sxs-lookup"><span data-stu-id="2d67a-107">Members</span></span>

<span data-ttu-id="2d67a-108">**Msvm \_ GuestClusterInformation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2d67a-108">The **Msvm\_GuestClusterInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="2d67a-109">屬性</span><span class="sxs-lookup"><span data-stu-id="2d67a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d67a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2d67a-110">Properties</span></span>

<span data-ttu-id="2d67a-111">**Msvm \_ GuestClusterInformation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2d67a-111">The **Msvm\_GuestClusterInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d67a-112">**ClusterId**</span><span class="sxs-lookup"><span data-stu-id="2d67a-112">**ClusterId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d67a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-115">VM 的客體作業系統所屬之容錯移轉叢集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d67a-115">The identifier of the failover cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-116">**ClusterSize**</span><span class="sxs-lookup"><span data-stu-id="2d67a-116">**ClusterSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2d67a-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-119">VM 的客體作業系統所屬叢集中的節點數目。</span><span class="sxs-lookup"><span data-stu-id="2d67a-119">Number of nodes in the cluster the VM's guest Operating System is a part of.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-120">**IsActiveActive**</span><span class="sxs-lookup"><span data-stu-id="2d67a-120">**IsActiveActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-121">資料類型： **布林** 陣列</span><span class="sxs-lookup"><span data-stu-id="2d67a-121">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-123">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="2d67a-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-124">布林值陣列，對應至每個共用虛擬硬碟，指出是否在主動/主動模式的 Vm 之間共用來賓叢集中對應的磁片資源。</span><span class="sxs-lookup"><span data-stu-id="2d67a-124">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is shared between VMs in active/active mode.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-125">**IsClustered**</span><span class="sxs-lookup"><span data-stu-id="2d67a-125">**IsClustered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-126">資料類型： **布林** 陣列</span><span class="sxs-lookup"><span data-stu-id="2d67a-126">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-128">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="2d67a-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-129">布林值陣列，對應至每個共用虛擬硬碟，指出對應的磁片是否為來賓叢集中的叢集資源。</span><span class="sxs-lookup"><span data-stu-id="2d67a-129">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk is a cluster resource in the guest cluster.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-130">**IsOnline**</span><span class="sxs-lookup"><span data-stu-id="2d67a-130">**IsOnline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-131">資料類型： **布林** 陣列</span><span class="sxs-lookup"><span data-stu-id="2d67a-131">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-133">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="2d67a-133">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-134">布林值陣列，對應至每個共用虛擬硬碟，指出來賓叢集中對應的磁片資源是否在線上。</span><span class="sxs-lookup"><span data-stu-id="2d67a-134">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is online.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-135">**IsOwned**</span><span class="sxs-lookup"><span data-stu-id="2d67a-135">**IsOwned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-136">資料類型： **布林** 陣列</span><span class="sxs-lookup"><span data-stu-id="2d67a-136">Data type: **boolean** array</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-138">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="2d67a-138">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-139">布林值陣列，對應至每個共用虛擬硬碟，指出來賓叢集中對應的磁片資源是否為此 VM 所擁有的目前。</span><span class="sxs-lookup"><span data-stu-id="2d67a-139">An array of booleans corresponding to each shared virtual hard disk indicating if the corresponding disk resource in the guest cluster is currenly owned by this VM.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-140">**LastResourceMoveTime**</span><span class="sxs-lookup"><span data-stu-id="2d67a-140">**LastResourceMoveTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="2d67a-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-143">上次移動其中一個共用磁片資源時的時鐘滴答計數。</span><span class="sxs-lookup"><span data-stu-id="2d67a-143">The clock tick count when one of the shared disk resources last moved.</span></span>

> [!Note]  
> <span data-ttu-id="2d67a-144">這個屬性是在 Windows 10、1703版和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="2d67a-144">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="2d67a-145">**SharedVirtualHardDiskPaths**</span><span class="sxs-lookup"><span data-stu-id="2d67a-145">**SharedVirtualHardDiskPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-146">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2d67a-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-148">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="2d67a-148">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-149">連線至 VM 的共用虛擬硬碟路徑陣列。</span><span class="sxs-lookup"><span data-stu-id="2d67a-149">An array of shared virtual hard disk paths connected to the VM.</span></span>

</dd> <dt>

<span data-ttu-id="2d67a-150">**SharedVirtualHardDisks**</span><span class="sxs-lookup"><span data-stu-id="2d67a-150">**SharedVirtualHardDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d67a-151">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2d67a-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2d67a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d67a-153">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="2d67a-153">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="2d67a-154">資源配置設定資料 (RASD) 的陣列，代表連線至 VM 的共用虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="2d67a-154">An array of Resource Allocation Setting Data (RASD) representing the shared virtual hard disks connected to the VM.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d67a-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d67a-155">Requirements</span></span>



| <span data-ttu-id="2d67a-156">需求</span><span class="sxs-lookup"><span data-stu-id="2d67a-156">Requirement</span></span> | <span data-ttu-id="2d67a-157">值</span><span class="sxs-lookup"><span data-stu-id="2d67a-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d67a-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d67a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="2d67a-159">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d67a-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2d67a-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d67a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="2d67a-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2d67a-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2d67a-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d67a-162">Namespace</span></span><br/>                | <span data-ttu-id="2d67a-163">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d67a-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d67a-164">MOF</span><span class="sxs-lookup"><span data-stu-id="2d67a-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d67a-165"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2d67a-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d67a-166">DLL</span><span class="sxs-lookup"><span data-stu-id="2d67a-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d67a-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d67a-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

