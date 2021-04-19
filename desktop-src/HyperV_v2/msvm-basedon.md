---
description: 描述如何從較低層級範圍組合儲存區範圍的關聯。
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983851"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="65d18-103">Msvm \_ BasedOn 類別</span><span class="sxs-lookup"><span data-stu-id="65d18-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="65d18-104">描述如何從較低層級範圍組合儲存區範圍的關聯。</span><span class="sxs-lookup"><span data-stu-id="65d18-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="65d18-105">例如，ProtectedSpaceExtents 是 PhysicalExtents 的一部分，而 VolumeSets 則是從一個或多個實體或 ProtectedSpaceExtents 來組合。</span><span class="sxs-lookup"><span data-stu-id="65d18-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="65d18-106">另一個範例是，CacheMemory 可以獨立定義並在 PhysicalElement 中實現，也可以根據 Volatile 或 NonVolatileStorageExtents。</span><span class="sxs-lookup"><span data-stu-id="65d18-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="65d18-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="65d18-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d18-108">語法</span><span class="sxs-lookup"><span data-stu-id="65d18-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="65d18-109">成員</span><span class="sxs-lookup"><span data-stu-id="65d18-109">Members</span></span>

<span data-ttu-id="65d18-110">**Msvm \_ BasedOn** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65d18-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="65d18-111">屬性</span><span class="sxs-lookup"><span data-stu-id="65d18-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65d18-112">屬性</span><span class="sxs-lookup"><span data-stu-id="65d18-112">Properties</span></span>

<span data-ttu-id="65d18-113">**Msvm \_ BasedOn** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="65d18-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65d18-114">**先行**</span><span class="sxs-lookup"><span data-stu-id="65d18-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d18-115">資料類型： **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="65d18-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="65d18-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65d18-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d18-117">較低層級的儲存區。</span><span class="sxs-lookup"><span data-stu-id="65d18-117">The lower level storage extent.</span></span> <span data-ttu-id="65d18-118">這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。</span><span class="sxs-lookup"><span data-stu-id="65d18-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="65d18-119">**依賴**</span><span class="sxs-lookup"><span data-stu-id="65d18-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d18-120">資料類型： **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="65d18-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="65d18-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65d18-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d18-122">較高層級的儲存區。</span><span class="sxs-lookup"><span data-stu-id="65d18-122">The higher level storage extent.</span></span> <span data-ttu-id="65d18-123">這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。</span><span class="sxs-lookup"><span data-stu-id="65d18-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="65d18-124">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="65d18-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d18-125">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="65d18-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65d18-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65d18-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d18-127">結束位址，在較低層級的儲存體中，較高層級的範圍結束。</span><span class="sxs-lookup"><span data-stu-id="65d18-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="65d18-128">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="65d18-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="65d18-129">這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。</span><span class="sxs-lookup"><span data-stu-id="65d18-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="65d18-130">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="65d18-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d18-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="65d18-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="65d18-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65d18-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d18-133">如果根據描述如何組合較高層級儲存區的關聯來產生訂單， **OrderIndex** 屬性就會指出這一點。</span><span class="sxs-lookup"><span data-stu-id="65d18-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="65d18-134">當訂單存在時，具有相同 **相依** 值 (相同較高層級範圍的實例) 應該會在 **OrderIndex** 屬性中放置唯一值。</span><span class="sxs-lookup"><span data-stu-id="65d18-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="65d18-135">最小值表示較低層級範圍集合的第一個成員，而增加值則表示集合的後續成員。</span><span class="sxs-lookup"><span data-stu-id="65d18-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="65d18-136">如果沒有已排序的關聯性，則應該指定零值。</span><span class="sxs-lookup"><span data-stu-id="65d18-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="65d18-137">使用這個屬性的範例是定義三個磁片的 RAID 0 等量陣列。</span><span class="sxs-lookup"><span data-stu-id="65d18-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="65d18-138">結果 RAID 陣列是一個儲存範圍，相依于描述三個磁片的每個磁片區。</span><span class="sxs-lookup"><span data-stu-id="65d18-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="65d18-139">從磁片區到 RAID 陣列的每個關聯的 **OrderIndex** ，都可以指定為1、2和3，以指出磁片區用來存取 RAID 資料的順序。</span><span class="sxs-lookup"><span data-stu-id="65d18-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="65d18-140">這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。</span><span class="sxs-lookup"><span data-stu-id="65d18-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="65d18-141">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="65d18-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d18-142">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="65d18-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65d18-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="65d18-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d18-144">從較低層級的儲存體開始，較高層級的範圍開始的起始位址。</span><span class="sxs-lookup"><span data-stu-id="65d18-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="65d18-145">這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。</span><span class="sxs-lookup"><span data-stu-id="65d18-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65d18-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="65d18-146">Requirements</span></span>



| <span data-ttu-id="65d18-147">需求</span><span class="sxs-lookup"><span data-stu-id="65d18-147">Requirement</span></span> | <span data-ttu-id="65d18-148">值</span><span class="sxs-lookup"><span data-stu-id="65d18-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d18-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65d18-149">Minimum supported client</span></span><br/> | <span data-ttu-id="65d18-150">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65d18-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="65d18-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65d18-151">Minimum supported server</span></span><br/> | <span data-ttu-id="65d18-152">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65d18-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65d18-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="65d18-153">Namespace</span></span><br/>                | <span data-ttu-id="65d18-154">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="65d18-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="65d18-155">MOF</span><span class="sxs-lookup"><span data-stu-id="65d18-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65d18-156"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="65d18-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65d18-157">DLL</span><span class="sxs-lookup"><span data-stu-id="65d18-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65d18-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65d18-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

