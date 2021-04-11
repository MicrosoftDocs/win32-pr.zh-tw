---
description: 代表較高層級 CIM \_ StorageExtent 物件與較低層級 cim StorageExtent 物件之間的關聯 \_ 。 例如，CIM \_ ProtectedSpaceExtent 物件是 cim \_ PhysicalExtent 物件的一部分。
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: 'CIM_BasedOn 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847964"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="b363a-104">CIM_BasedOn 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="b363a-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="b363a-105">代表較高層級 **cim \_ StorageExtent** 物件與較低層級 **cim \_ StorageExtent** 物件之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="b363a-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="b363a-106">例如， [**cim \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) 物件是 [**cim \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) 物件的一部分。</span><span class="sxs-lookup"><span data-stu-id="b363a-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b363a-107">語法</span><span class="sxs-lookup"><span data-stu-id="b363a-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="b363a-108">成員</span><span class="sxs-lookup"><span data-stu-id="b363a-108">Members</span></span>

<span data-ttu-id="b363a-109">**CIM \_ BasedOn** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b363a-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="b363a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b363a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b363a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b363a-111">Properties</span></span>

<span data-ttu-id="b363a-112">**CIM \_ BasedOn** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b363a-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b363a-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="b363a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b363a-114">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="b363a-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b363a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b363a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b363a-116">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="b363a-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b363a-117">較低層級的 **CIM \_ StorageExtent** 物件。</span><span class="sxs-lookup"><span data-stu-id="b363a-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="b363a-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="b363a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b363a-119">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="b363a-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b363a-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b363a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b363a-121">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="b363a-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b363a-122">較高層級的 **CIM \_ StorageExtent** 物件。</span><span class="sxs-lookup"><span data-stu-id="b363a-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="b363a-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b363a-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b363a-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b363a-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b363a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b363a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b363a-126">指出較低層級儲存體中之位置的位址，較高層級的 **CIM \_ StorageExtent** 物件會結束。</span><span class="sxs-lookup"><span data-stu-id="b363a-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="b363a-127">當將非連續的 **CIM \_ StorageExtent** 物件對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="b363a-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="b363a-128">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="b363a-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b363a-129">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b363a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b363a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b363a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b363a-131">用來指定集合中 **CIM \_ BasedOn** 關聯順序的索引，否則為 "0" 表示沒有順序。</span><span class="sxs-lookup"><span data-stu-id="b363a-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="b363a-132">**CIM \_** 具有相同相依值的 BasedOn 實例應該在 **OrderIndex** 屬性中放置唯一值。</span><span class="sxs-lookup"><span data-stu-id="b363a-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="b363a-133">最小的 **OrderIndex** 值會指定集合的第一個成員。</span><span class="sxs-lookup"><span data-stu-id="b363a-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="b363a-134">使用這個屬性的範例是定義3個磁片的 RAID 0 等量陣列。</span><span class="sxs-lookup"><span data-stu-id="b363a-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="b363a-135">結果 RAID 陣列是儲存區，相依于描述3個磁片的每個磁片區的儲存區。</span><span class="sxs-lookup"><span data-stu-id="b363a-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="b363a-136">從磁片區至 RAID 陣列的每個 **CIM \_ BasedOn** 關聯的 **OrderIndex** 值可以指定為1、2和3，以指出磁片區用來存取 RAID 資料的順序。</span><span class="sxs-lookup"><span data-stu-id="b363a-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="b363a-137">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="b363a-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b363a-138">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b363a-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b363a-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b363a-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b363a-140">指出較低層級儲存體中之位置的位址，會開始較高層級的 **CIM \_ StorageExtent** 物件。</span><span class="sxs-lookup"><span data-stu-id="b363a-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b363a-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="b363a-141">Requirements</span></span>



| <span data-ttu-id="b363a-142">需求</span><span class="sxs-lookup"><span data-stu-id="b363a-142">Requirement</span></span> | <span data-ttu-id="b363a-143">值</span><span class="sxs-lookup"><span data-stu-id="b363a-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b363a-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b363a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b363a-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b363a-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b363a-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b363a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b363a-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b363a-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b363a-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="b363a-148">Namespace</span></span><br/>                | <span data-ttu-id="b363a-149">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b363a-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b363a-150">MOF</span><span class="sxs-lookup"><span data-stu-id="b363a-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b363a-151"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b363a-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b363a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b363a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b363a-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b363a-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b363a-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b363a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b363a-155">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="b363a-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

