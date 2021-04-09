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
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="cca2b-104">CIM \_ LogicalDiskBasedOnVolumeSet 類別</span><span class="sxs-lookup"><span data-stu-id="cca2b-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="cca2b-105">**CIM \_ LogicalDiskBasedOnVolumeSet** 關聯會將邏輯磁片與找到它們的磁片區相關聯。</span><span class="sxs-lookup"><span data-stu-id="cca2b-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="cca2b-106">邏輯磁片可根據單一磁片區 (例如，由軟體磁片區管理員) 或磁碟分割所公開。</span><span class="sxs-lookup"><span data-stu-id="cca2b-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cca2b-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cca2b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cca2b-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cca2b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cca2b-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cca2b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cca2b-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cca2b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca2b-111">語法</span><span class="sxs-lookup"><span data-stu-id="cca2b-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="cca2b-112">成員</span><span class="sxs-lookup"><span data-stu-id="cca2b-112">Members</span></span>

<span data-ttu-id="cca2b-113">**CIM \_ LogicalDiskBasedOnVolumeSet** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cca2b-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="cca2b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="cca2b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cca2b-115">屬性</span><span class="sxs-lookup"><span data-stu-id="cca2b-115">Properties</span></span>

<span data-ttu-id="cca2b-116">**CIM \_ LogicalDiskBasedOnVolumeSet** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cca2b-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cca2b-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="cca2b-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca2b-118">資料類型： **CIM \_ VolumeSet**</span><span class="sxs-lookup"><span data-stu-id="cca2b-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="cca2b-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cca2b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cca2b-120">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="cca2b-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cca2b-121">描述磁片區集的 [**CIM \_ VolumeSet**](cim-volumeset.md) 。</span><span class="sxs-lookup"><span data-stu-id="cca2b-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="cca2b-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="cca2b-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca2b-123">資料類型： **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="cca2b-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="cca2b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cca2b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cca2b-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="cca2b-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cca2b-126">[**CIM \_ LogicalDisk**](cim-logicaldisk.md) ，描述建立于磁片區組上的邏輯磁片。</span><span class="sxs-lookup"><span data-stu-id="cca2b-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="cca2b-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="cca2b-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca2b-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cca2b-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cca2b-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cca2b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cca2b-130">指出較低層級儲存體中的高階範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="cca2b-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="cca2b-131">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="cca2b-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="cca2b-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="cca2b-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cca2b-133">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="cca2b-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="cca2b-134">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="cca2b-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cca2b-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cca2b-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cca2b-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cca2b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cca2b-137">表示較低層級儲存體中的高階範圍開始。</span><span class="sxs-lookup"><span data-stu-id="cca2b-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="cca2b-138">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="cca2b-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="cca2b-139">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="cca2b-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cca2b-140">備註</span><span class="sxs-lookup"><span data-stu-id="cca2b-140">Remarks</span></span>

<span data-ttu-id="cca2b-141">**Cim \_ LogicalDiskBasedOnVolumeSet** 類別衍生自 [**cim \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="cca2b-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="cca2b-142">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cca2b-142">WMI does not implement this class.</span></span>

<span data-ttu-id="cca2b-143">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cca2b-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cca2b-144">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cca2b-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca2b-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="cca2b-145">Requirements</span></span>



| <span data-ttu-id="cca2b-146">需求</span><span class="sxs-lookup"><span data-stu-id="cca2b-146">Requirement</span></span> | <span data-ttu-id="cca2b-147">值</span><span class="sxs-lookup"><span data-stu-id="cca2b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cca2b-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cca2b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cca2b-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cca2b-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cca2b-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cca2b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cca2b-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cca2b-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cca2b-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="cca2b-152">Namespace</span></span><br/>                | <span data-ttu-id="cca2b-153">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cca2b-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cca2b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="cca2b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cca2b-155"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cca2b-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cca2b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="cca2b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cca2b-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cca2b-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca2b-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cca2b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca2b-159">**CIM \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="cca2b-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

