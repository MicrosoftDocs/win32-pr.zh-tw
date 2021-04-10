---
description: CIM \_ LogicalDiskBasedOnVolumeSet 關聯會將邏輯磁片與找到它們的磁片區相關聯。 邏輯磁片可根據單一磁片區 (例如，由軟體磁片區管理員) 或磁碟分割所公開。
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnVolumeSet 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110269"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="7d54a-104">CIM \_ LogicalDiskBasedOnVolumeSet 類別</span><span class="sxs-lookup"><span data-stu-id="7d54a-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="7d54a-105">**CIM \_ LogicalDiskBasedOnVolumeSet** 關聯會將邏輯磁片與找到它們的磁片區相關聯。</span><span class="sxs-lookup"><span data-stu-id="7d54a-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="7d54a-106">邏輯磁片可根據單一磁片區 (例如，由軟體磁片區管理員) 或磁碟分割所公開。</span><span class="sxs-lookup"><span data-stu-id="7d54a-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d54a-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7d54a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7d54a-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7d54a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7d54a-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7d54a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7d54a-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7d54a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d54a-111">語法</span><span class="sxs-lookup"><span data-stu-id="7d54a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7d54a-112">成員</span><span class="sxs-lookup"><span data-stu-id="7d54a-112">Members</span></span>

<span data-ttu-id="7d54a-113">**CIM \_ LogicalDiskBasedOnVolumeSet** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7d54a-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="7d54a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7d54a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d54a-115">屬性</span><span class="sxs-lookup"><span data-stu-id="7d54a-115">Properties</span></span>

<span data-ttu-id="7d54a-116">**CIM \_ LogicalDiskBasedOnVolumeSet** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7d54a-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d54a-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="7d54a-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d54a-118">資料類型： **CIM \_ VolumeSet**</span><span class="sxs-lookup"><span data-stu-id="7d54a-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="7d54a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7d54a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d54a-120">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="7d54a-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7d54a-121">描述磁片區集的 [**CIM \_ VolumeSet**](cim-volumeset.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d54a-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="7d54a-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="7d54a-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d54a-123">資料類型： **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="7d54a-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="7d54a-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7d54a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d54a-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="7d54a-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7d54a-126">[**CIM \_ LogicalDisk**](cim-logicaldisk.md) ，描述建立于磁片區組上的邏輯磁片。</span><span class="sxs-lookup"><span data-stu-id="7d54a-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="7d54a-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="7d54a-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d54a-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7d54a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d54a-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7d54a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d54a-130">指出較低層級儲存體中的高階範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="7d54a-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="7d54a-131">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="7d54a-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="7d54a-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="7d54a-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="7d54a-133">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="7d54a-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d54a-134">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="7d54a-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d54a-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="7d54a-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7d54a-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="7d54a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d54a-137">表示較低層級儲存體中的高階範圍開始。</span><span class="sxs-lookup"><span data-stu-id="7d54a-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="7d54a-138">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="7d54a-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="7d54a-139">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="7d54a-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d54a-140">備註</span><span class="sxs-lookup"><span data-stu-id="7d54a-140">Remarks</span></span>

<span data-ttu-id="7d54a-141">**Cim \_ LogicalDiskBasedOnVolumeSet** 類別衍生自 [**cim \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="7d54a-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="7d54a-142">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="7d54a-142">WMI does not implement this class.</span></span>

<span data-ttu-id="7d54a-143">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7d54a-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7d54a-144">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7d54a-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d54a-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d54a-145">Requirements</span></span>



| <span data-ttu-id="7d54a-146">需求</span><span class="sxs-lookup"><span data-stu-id="7d54a-146">Requirement</span></span> | <span data-ttu-id="7d54a-147">值</span><span class="sxs-lookup"><span data-stu-id="7d54a-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d54a-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d54a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7d54a-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d54a-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d54a-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d54a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7d54a-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d54a-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d54a-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d54a-152">Namespace</span></span><br/>                | <span data-ttu-id="7d54a-153">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d54a-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d54a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="7d54a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d54a-155"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d54a-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d54a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7d54a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d54a-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d54a-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d54a-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d54a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d54a-159">**CIM \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="7d54a-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

