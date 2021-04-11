---
description: CIM \_ BasedOn 類別代表一種關聯，描述如何從較低層級的範圍組合儲存區。
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: 'CIM_BasedOn 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190974"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="67431-103">CIM_BasedOn 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="67431-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="67431-104">**CIM \_ BasedOn** 類別代表一種關聯，描述如何從較低層級的範圍組合儲存區。</span><span class="sxs-lookup"><span data-stu-id="67431-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="67431-105">例如，實體範圍包含受保護的空間範圍。</span><span class="sxs-lookup"><span data-stu-id="67431-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="67431-106">因此，系統會從一或多個實體或受保護的空間範圍組合磁片區集合。</span><span class="sxs-lookup"><span data-stu-id="67431-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="67431-107">快取記憶體可以獨立定義並在實體元素中實現，也可以根據暫時性或非暫時性的儲存區。</span><span class="sxs-lookup"><span data-stu-id="67431-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="67431-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="67431-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="67431-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="67431-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="67431-110">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="67431-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67431-111">語法</span><span class="sxs-lookup"><span data-stu-id="67431-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="67431-112">成員</span><span class="sxs-lookup"><span data-stu-id="67431-112">Members</span></span>

<span data-ttu-id="67431-113">**CIM \_ BasedOn** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="67431-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="67431-114">屬性</span><span class="sxs-lookup"><span data-stu-id="67431-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67431-115">屬性</span><span class="sxs-lookup"><span data-stu-id="67431-115">Properties</span></span>

<span data-ttu-id="67431-116">**CIM \_ BasedOn** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="67431-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67431-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="67431-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67431-118">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="67431-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="67431-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67431-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67431-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="67431-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="67431-121">描述較低層級儲存區的 [**CIM \_ StorageExtent**](cim-storageextent.md) 。</span><span class="sxs-lookup"><span data-stu-id="67431-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="67431-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="67431-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67431-123">資料類型： **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="67431-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="67431-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67431-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67431-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="67431-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="67431-126">描述較高層級儲存區的 [**CIM \_ StorageExtent**](cim-storageextent.md) 。</span><span class="sxs-lookup"><span data-stu-id="67431-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="67431-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="67431-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67431-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="67431-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67431-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67431-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67431-130">指出較低層級儲存體中的高階範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="67431-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="67431-131">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="67431-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="67431-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="67431-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="67431-133">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="67431-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67431-134">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="67431-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67431-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67431-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67431-136">表示較低層級儲存體中的高階範圍開始。</span><span class="sxs-lookup"><span data-stu-id="67431-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="67431-137">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="67431-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67431-138">備註</span><span class="sxs-lookup"><span data-stu-id="67431-138">Remarks</span></span>

<span data-ttu-id="67431-139">**Cim \_ BasedOn** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。</span><span class="sxs-lookup"><span data-stu-id="67431-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="67431-140">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="67431-140">WMI does not implement this class.</span></span>

<span data-ttu-id="67431-141">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="67431-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="67431-142">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="67431-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="67431-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="67431-143">Requirements</span></span>



| <span data-ttu-id="67431-144">需求</span><span class="sxs-lookup"><span data-stu-id="67431-144">Requirement</span></span> | <span data-ttu-id="67431-145">值</span><span class="sxs-lookup"><span data-stu-id="67431-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67431-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67431-146">Minimum supported client</span></span><br/> | <span data-ttu-id="67431-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67431-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67431-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67431-148">Minimum supported server</span></span><br/> | <span data-ttu-id="67431-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67431-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67431-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="67431-150">Namespace</span></span><br/>                | <span data-ttu-id="67431-151">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67431-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67431-152">MOF</span><span class="sxs-lookup"><span data-stu-id="67431-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67431-153"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="67431-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67431-154">DLL</span><span class="sxs-lookup"><span data-stu-id="67431-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67431-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67431-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67431-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67431-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67431-157">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="67431-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

