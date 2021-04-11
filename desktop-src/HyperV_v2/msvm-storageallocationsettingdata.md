---
description: 表示與虛擬儲存體配置特別相關的設定。
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Msvm_StorageAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193505"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="d11c3-103">Msvm \_ StorageAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="d11c3-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="d11c3-104">表示與虛擬儲存體配置特別相關的設定。</span><span class="sxs-lookup"><span data-stu-id="d11c3-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="d11c3-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d11c3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11c3-106">語法</span><span class="sxs-lookup"><span data-stu-id="d11c3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a><span data-ttu-id="d11c3-107">成員</span><span class="sxs-lookup"><span data-stu-id="d11c3-107">Members</span></span>

<span data-ttu-id="d11c3-108">**Msvm \_ StorageAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d11c3-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d11c3-109">屬性</span><span class="sxs-lookup"><span data-stu-id="d11c3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d11c3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d11c3-110">Properties</span></span>

<span data-ttu-id="d11c3-111">**Msvm \_ StorageAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d11c3-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d11c3-112">**存取**</span><span class="sxs-lookup"><span data-stu-id="d11c3-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-113">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-115">指定存放裝置存取。</span><span class="sxs-lookup"><span data-stu-id="d11c3-115">Specifies the storage access.</span></span> <span data-ttu-id="d11c3-116">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="d11c3-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d11c3-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="d11c3-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="d11c3-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="d11c3-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d11c3-121">**位址**</span><span class="sxs-lookup"><span data-stu-id="d11c3-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-124">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="d11c3-124">The address of the resource.</span></span> <span data-ttu-id="d11c3-125">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-126">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="d11c3-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-129">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="d11c3-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="d11c3-130">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="d11c3-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="d11c3-131">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-132">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d11c3-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-135">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="d11c3-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="d11c3-136">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-137">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="d11c3-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d11c3-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-140">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="d11c3-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="d11c3-141">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-142">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="d11c3-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d11c3-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-145">指出是否將自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="d11c3-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="d11c3-146">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-147">**CachingMode**</span><span class="sxs-lookup"><span data-stu-id="d11c3-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-150">指出是否應該針對此 VHD 使用記憶體中的檔案快取。</span><span class="sxs-lookup"><span data-stu-id="d11c3-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="d11c3-151">預設原則是在 [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別的 **DefaultVirtualHardDiskCachingMode** 欄位中設定。</span><span class="sxs-lookup"><span data-stu-id="d11c3-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="d11c3-152">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="d11c3-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d11c3-153">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d11c3-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="d11c3-154">**預設** (2) </span><span class="sxs-lookup"><span data-stu-id="d11c3-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="d11c3-155">**沒有** 快取 (3) </span><span class="sxs-lookup"><span data-stu-id="d11c3-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="d11c3-156">快取可 **共用** 的父系 (4) </span><span class="sxs-lookup"><span data-stu-id="d11c3-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d11c3-157">**標題**</span><span class="sxs-lookup"><span data-stu-id="d11c3-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-160">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="d11c3-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-161">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d11c3-161">A short description of the object.</span></span> <span data-ttu-id="d11c3-162">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「硬碟映射預設設定」。</span><span class="sxs-lookup"><span data-stu-id="d11c3-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-163">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="d11c3-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-164">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d11c3-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-166">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="d11c3-166">The device to which this resource is connected.</span></span> <span data-ttu-id="d11c3-167">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-168">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="d11c3-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-169">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-171">取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="d11c3-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="d11c3-172">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="d11c3-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d11c3-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**傳遞** (2) </span><span class="sxs-lookup"><span data-stu-id="d11c3-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**虛擬化** (3) </span><span class="sxs-lookup"><span data-stu-id="d11c3-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span> (4) **未表示**</span><span class="sxs-lookup"><span data-stu-id="d11c3-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d11c3-177">**說明**</span><span class="sxs-lookup"><span data-stu-id="d11c3-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-180">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d11c3-180">A description of the object.</span></span> <span data-ttu-id="d11c3-181">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「描述硬碟映射資源的預設設定」。</span><span class="sxs-lookup"><span data-stu-id="d11c3-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d11c3-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-185">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d11c3-185">A display name for the object.</span></span> <span data-ttu-id="d11c3-186">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d11c3-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-187">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="d11c3-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-190">主機範圍的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d11c3-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="d11c3-191">識別的主機範圍會用於儲存體資源配置。</span><span class="sxs-lookup"><span data-stu-id="d11c3-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="d11c3-192">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-193">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="d11c3-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-194">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-196">識別用於 **HostExtentName** 屬性的格式。</span><span class="sxs-lookup"><span data-stu-id="d11c3-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="d11c3-197">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="d11c3-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d11c3-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d11c3-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7) </span><span class="sxs-lookup"><span data-stu-id="d11c3-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9) </span><span class="sxs-lookup"><span data-stu-id="d11c3-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10) </span><span class="sxs-lookup"><span data-stu-id="d11c3-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11) </span><span class="sxs-lookup"><span data-stu-id="d11c3-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS 裝置名稱** (12) </span><span class="sxs-lookup"><span data-stu-id="d11c3-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="d11c3-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d11c3-206">)</span><span class="sxs-lookup"><span data-stu-id="d11c3-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d11c3-207">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="d11c3-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-210">如果主機範圍是 SCSI 磁片區，則 SCSI 磁片區名稱的慣用來源為 SCSI VPD 頁面83回應。</span><span class="sxs-lookup"><span data-stu-id="d11c3-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="d11c3-211">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="d11c3-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d11c3-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d11c3-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2) </span><span class="sxs-lookup"><span data-stu-id="d11c3-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3) </span><span class="sxs-lookup"><span data-stu-id="d11c3-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4) </span><span class="sxs-lookup"><span data-stu-id="d11c3-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5) </span><span class="sxs-lookup"><span data-stu-id="d11c3-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6) </span><span class="sxs-lookup"><span data-stu-id="d11c3-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7) </span><span class="sxs-lookup"><span data-stu-id="d11c3-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS 裝置命名空間** (8) </span><span class="sxs-lookup"><span data-stu-id="d11c3-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="d11c3-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="d11c3-222">)</span><span class="sxs-lookup"><span data-stu-id="d11c3-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d11c3-223">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="d11c3-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-224">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-226">識別主機儲存區的起始位址（由 **HostExtentName** 屬性識別），以用於配置虛擬儲存區。</span><span class="sxs-lookup"><span data-stu-id="d11c3-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="d11c3-227">**Null** 值表示沒有虛擬儲存區的直接對應至參考的主機儲存區。</span><span class="sxs-lookup"><span data-stu-id="d11c3-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="d11c3-228">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-229">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="d11c3-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-230">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d11c3-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-232">只有一個主機資源可以指派給虛擬機器中的每個裝置，因此只能設定此陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="d11c3-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="d11c3-233">針對支援此功能的裝置，請將 **HostResource** 陣列的第一個元素設定為包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="d11c3-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="d11c3-234">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="d11c3-235">這是一個唯讀屬性。</span><span class="sxs-lookup"><span data-stu-id="d11c3-235">This is a read-only property.</span></span> <span data-ttu-id="d11c3-236">但是，如果 **ResourceType** 屬性為 31 (邏輯磁片) 而且 **ResourceSubType** 內容為 "Microsoft： Hyper-v： virtual Hard Disk"、"Microsoft： hyper-v： Virtual CD/DVD Disk" 或 "microsoft： hyper-v： virtual disk disk"，則可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更 **HostResource** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d11c3-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-237">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d11c3-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-238">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-240">此儲存體資源配置或儲存體資源配置要求的結果，在主機上配置之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d11c3-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="d11c3-241">如果區塊大小為變數，則會指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d11c3-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="d11c3-242">如果區塊大小未知或區塊概念未套用，則會使用值1。</span><span class="sxs-lookup"><span data-stu-id="d11c3-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="d11c3-243">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-244">**IgnoreFlushes**</span><span class="sxs-lookup"><span data-stu-id="d11c3-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-245">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d11c3-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-247">如果設定為 true，Hyper-v 將會忽略該特定虛擬機器的回寫。</span><span class="sxs-lookup"><span data-stu-id="d11c3-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="d11c3-248">如果設定為 false，則 Hyper-v 會在每次排清時繼續回寫至磁片。</span><span class="sxs-lookup"><span data-stu-id="d11c3-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="d11c3-249">預設設定是 false。</span><span class="sxs-lookup"><span data-stu-id="d11c3-249">The default setting is false.</span></span>

<span data-ttu-id="d11c3-250">**Windows 10：** 在 Windows 10 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d11c3-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-254">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d11c3-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-255">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d11c3-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d11c3-256">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d11c3-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-257">**IOPSAllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="d11c3-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-260">指定 **IOPSLimit** 和 **IOPSReservation** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="d11c3-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="d11c3-261">這個屬性的值一律為：</span><span class="sxs-lookup"><span data-stu-id="d11c3-261">This property always has the value:</span></span>

<span data-ttu-id="d11c3-262">"count (正規化 i/o) /秒"</span><span class="sxs-lookup"><span data-stu-id="d11c3-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="d11c3-263">輸送量會以每秒正規化的 i/o 作業來測量， (IOPS) 而不是原始 IOPS。</span><span class="sxs-lookup"><span data-stu-id="d11c3-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="d11c3-264">使用標準化 IOPS 時，如果要求的大小小於或等於預先定義的基底大小 (8 KB) ，則會將每個 i/o 要求視為1個正規化 i/o。</span><span class="sxs-lookup"><span data-stu-id="d11c3-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="d11c3-265">大於基底大小的要求會被視為 N i/o 作業，其中 N 是要求大小的進位值除以基底大小。</span><span class="sxs-lookup"><span data-stu-id="d11c3-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="d11c3-266">例如，如果基底大小為 8 KB，則會將 16 KB 的要求視為2個正規化的 i/o 作業，並將 32-KB 的要求視為4個標準化的 i/o 作業，依此類推。</span><span class="sxs-lookup"><span data-stu-id="d11c3-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="d11c3-267">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-268">**IOPSLimit**</span><span class="sxs-lookup"><span data-stu-id="d11c3-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-269">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-271">限定詞： [**int32.maxvalue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000) </span><span class="sxs-lookup"><span data-stu-id="d11c3-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-272">每秒的 i/o 作業數目上限 (IOPS) ，此為此虛擬儲存區的服務。</span><span class="sxs-lookup"><span data-stu-id="d11c3-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="d11c3-273">如果未定義值或為零，則裝置可發出的 IOPS 數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="d11c3-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="d11c3-274">您可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來修改這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="d11c3-275">只有針對虛擬機器要求資源配置的 **Msvm \_ StorageAllocationSettingData** 實例，這個屬性才有意義。</span><span class="sxs-lookup"><span data-stu-id="d11c3-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="d11c3-276">將資源配置給子集區時，它會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d11c3-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="d11c3-277">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-278">**IOPSReservation**</span><span class="sxs-lookup"><span data-stu-id="d11c3-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-279">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-281">限定詞： [**int32.maxvalue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000) </span><span class="sxs-lookup"><span data-stu-id="d11c3-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-282">每秒的 i/o 作業數目下限 (IOPS) ，此為此虛擬儲存區的服務。</span><span class="sxs-lookup"><span data-stu-id="d11c3-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="d11c3-283">如果同時定義了 **IOPSLimit** 和 **IOPSReservation** ，則 **IOPSLimit** 的值必須大於或等於 **IOPSReservation** 的值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="d11c3-284">您可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來修改這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="d11c3-285">只有針對虛擬機器要求資源配置的 **Msvm \_ StorageAllocationSettingData** 實例，這個屬性才有意義。</span><span class="sxs-lookup"><span data-stu-id="d11c3-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="d11c3-286">將資源配置給子集區時，它會被忽略。</span><span class="sxs-lookup"><span data-stu-id="d11c3-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="d11c3-287">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-288">**限制**</span><span class="sxs-lookup"><span data-stu-id="d11c3-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-289">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-291">將在主機上為此儲存體資源配置授與的區塊數目上限。</span><span class="sxs-lookup"><span data-stu-id="d11c3-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="d11c3-292">區塊大小是由 **HostResourceBlockSize** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="d11c3-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="d11c3-293">通常，這個屬性的值會反映所配置主機範圍的大小上限，以符合向取用者呈現的虛擬儲存區大小。</span><span class="sxs-lookup"><span data-stu-id="d11c3-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="d11c3-294">小於該值的值表示預期的稀疏擴展虛擬儲存範圍，其中的填滿速率會受限於 Limit 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="d11c3-295">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-296">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="d11c3-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-297">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-299">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="d11c3-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="d11c3-300">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-301">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="d11c3-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-304">描述 **HostExtentName** 屬性格式的字串（如果 **HostExtentNameFormat** 屬性是 1 (其他) ）。</span><span class="sxs-lookup"><span data-stu-id="d11c3-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="d11c3-305">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-306">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="d11c3-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-309">字串，描述 **HostExtentName** 屬性的命名空間（如果 **HostExtentNameNamespace** 屬性包含 1 (其他) ）。</span><span class="sxs-lookup"><span data-stu-id="d11c3-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="d11c3-310">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-311">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="d11c3-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-314">描述資源類型的字串，當定義完善的值無法使用且 [**ResourceType**](msvm-processorsettingdata.md) 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="d11c3-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="d11c3-315">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-316">**父系**</span><span class="sxs-lookup"><span data-stu-id="d11c3-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-319">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="d11c3-319">The parent of the resource.</span></span> <span data-ttu-id="d11c3-320">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-321">**PersistentReservationsSupported**</span><span class="sxs-lookup"><span data-stu-id="d11c3-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-322">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d11c3-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-324">指出虛擬硬碟是否支援 SCSI-3 持續保留。</span><span class="sxs-lookup"><span data-stu-id="d11c3-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="d11c3-325">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="d11c3-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-326">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="d11c3-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-327">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-329">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="d11c3-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="d11c3-330">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-331">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="d11c3-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-332">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-334">限定詞：覆 **寫** ( "保留" ) ， **MODELCORRESPONDENCE** ( "CIM \_ StorageAllocationSettingData. HostResourceBlockSize" ) </span><span class="sxs-lookup"><span data-stu-id="d11c3-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-335">保證可供主機上的此儲存體資源配置使用的區塊數目。</span><span class="sxs-lookup"><span data-stu-id="d11c3-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="d11c3-336">區塊大小是由 **HostResourceBlockSize** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="d11c3-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="d11c3-337">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-338">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="d11c3-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-339">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-341">字串，描述此資源的實作為特定子類型。</span><span class="sxs-lookup"><span data-stu-id="d11c3-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="d11c3-342">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="d11c3-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="d11c3-343">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="d11c3-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-345">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-347">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="d11c3-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="d11c3-348">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="d11c3-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d11c3-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="d11c3-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="d11c3-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="d11c3-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="d11c3-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="d11c3-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="d11c3-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="d11c3-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="d11c3-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="d11c3-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="d11c3-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="d11c3-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="d11c3-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="d11c3-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="d11c3-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="d11c3-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="d11c3-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="d11c3-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="d11c3-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="d11c3-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="d11c3-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="d11c3-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="d11c3-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="d11c3-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="d11c3-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="d11c3-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="d11c3-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**電源供應** 器 (28) </span><span class="sxs-lookup"><span data-stu-id="d11c3-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**冷卻裝置** (29) </span><span class="sxs-lookup"><span data-stu-id="d11c3-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="d11c3-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="d11c3-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="d11c3-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="d11c3-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (30 32767) </span><span class="sxs-lookup"><span data-stu-id="d11c3-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="d11c3-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d11c3-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="d11c3-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-387">GUID，代表要附加 VHD 設定檔案中的快照集。</span><span class="sxs-lookup"><span data-stu-id="d11c3-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="d11c3-388">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="d11c3-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d11c3-389">**StorageQoSPolicyID**</span><span class="sxs-lookup"><span data-stu-id="d11c3-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-390">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-392">指定要套用至此虛擬儲存區的儲存體 QoS 原則的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d11c3-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="d11c3-393">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="d11c3-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="d11c3-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="d11c3-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-395">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-397">呈現給取用者的區塊數目。</span><span class="sxs-lookup"><span data-stu-id="d11c3-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="d11c3-398">區塊大小是由 **VirtualResourceBlockSize** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="d11c3-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="d11c3-399">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-400">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="d11c3-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d11c3-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-403">指定 **VirtualQuantity** 屬性所使用的單位。</span><span class="sxs-lookup"><span data-stu-id="d11c3-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="d11c3-404">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="d11c3-405">值</span><span class="sxs-lookup"><span data-stu-id="d11c3-405">Value</span></span>                                                                                                | <span data-ttu-id="d11c3-406">意義</span><span class="sxs-lookup"><span data-stu-id="d11c3-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d11c3-407"><dt>"count (固定大社區塊) "</dt></span><span class="sxs-lookup"><span data-stu-id="d11c3-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="d11c3-408">固定區塊大小包含在 **VirtualResourceBlockSize** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="d11c3-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="d11c3-409"><dt>位元組</dt></span><span class="sxs-lookup"><span data-stu-id="d11c3-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="d11c3-410">**VirtualQuantity** 屬性是以位元組為單位來測量。</span><span class="sxs-lookup"><span data-stu-id="d11c3-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="d11c3-411">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d11c3-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-412">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d11c3-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-414">針對此儲存體資源配置或儲存體資源配置要求的結果，向取用者呈現的區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d11c3-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="d11c3-415">如果區塊大小為變數，則會指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d11c3-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="d11c3-416">如果區塊大小未知或區塊概念未套用，則會使用值1。</span><span class="sxs-lookup"><span data-stu-id="d11c3-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="d11c3-417">這個屬性繼承自 **CIM \_ StorageAllocationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="d11c3-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-418">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d11c3-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-419">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d11c3-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-421">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「權數」 ) 、 [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1) [**、int32.maxvalue (10000)**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d11c3-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-422">指定此配置相對於相同資源集區中其他配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="d11c3-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="d11c3-423">這個屬性沒有測量單位，而且只與相同主機資源的其他配置 vying 相關。</span><span class="sxs-lookup"><span data-stu-id="d11c3-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="d11c3-424">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="d11c3-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="d11c3-425">範圍： 1 10000</span><span class="sxs-lookup"><span data-stu-id="d11c3-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="d11c3-426">**WriteHardeningMethod**</span><span class="sxs-lookup"><span data-stu-id="d11c3-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d11c3-427">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d11c3-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d11c3-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d11c3-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d11c3-429">指出磁片所支援的寫入強化方法。</span><span class="sxs-lookup"><span data-stu-id="d11c3-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="d11c3-430">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="d11c3-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="d11c3-431">**預設** (0) </span><span class="sxs-lookup"><span data-stu-id="d11c3-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="d11c3-432">**WriteCacheEnabled** (1) </span><span class="sxs-lookup"><span data-stu-id="d11c3-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="d11c3-433">**WriteCacheandFUAEnabled** (2) </span><span class="sxs-lookup"><span data-stu-id="d11c3-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="d11c3-434">**WriteCacheDisabled** (3) </span><span class="sxs-lookup"><span data-stu-id="d11c3-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="d11c3-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d11c3-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d11c3-436">規格需求</span><span class="sxs-lookup"><span data-stu-id="d11c3-436">Requirements</span></span>



| <span data-ttu-id="d11c3-437">需求</span><span class="sxs-lookup"><span data-stu-id="d11c3-437">Requirement</span></span> | <span data-ttu-id="d11c3-438">值</span><span class="sxs-lookup"><span data-stu-id="d11c3-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d11c3-439">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d11c3-439">Minimum supported client</span></span><br/> | <span data-ttu-id="d11c3-440">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d11c3-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d11c3-441">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d11c3-441">Minimum supported server</span></span><br/> | <span data-ttu-id="d11c3-442">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d11c3-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d11c3-443">命名空間</span><span class="sxs-lookup"><span data-stu-id="d11c3-443">Namespace</span></span><br/>                | <span data-ttu-id="d11c3-444">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d11c3-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d11c3-445">MOF</span><span class="sxs-lookup"><span data-stu-id="d11c3-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d11c3-446"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d11c3-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d11c3-447">DLL</span><span class="sxs-lookup"><span data-stu-id="d11c3-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d11c3-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d11c3-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

