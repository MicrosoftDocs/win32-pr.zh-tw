---
description: CIM \_ LogicalDiskBasedOnPartition 類別會將邏輯磁片與其所在的磁碟分割建立關聯。
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510445"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="3e80b-103">CIM \_ LogicalDiskBasedOnPartition 類別</span><span class="sxs-lookup"><span data-stu-id="3e80b-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="3e80b-104">**CIM \_ LogicalDiskBasedOnPartition** 類別會將邏輯磁片與其所在的磁碟分割建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3e80b-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="3e80b-105">例如，電腦的 C 磁片磁碟機 C 可以位於本機實體媒體的磁碟分割上，這表示邏輯磁片不能跨越多個磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="3e80b-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="3e80b-106">不過，當邏輯磁片可以跨越一個以上的磁碟分割時，邏輯磁片會以 RAID 設定為基礎 (例如，) 的鏡像或等量集。</span><span class="sxs-lookup"><span data-stu-id="3e80b-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="3e80b-107">在此情況下，邏輯磁片是以存放磁片區為基礎。</span><span class="sxs-lookup"><span data-stu-id="3e80b-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="3e80b-108">為了避免不正確地使用 **CIM \_ LogicalDiskBasedOnPartition** 關聯， **(1) 限定詞的最大值** 會放在磁碟分割的 **先前** 參考中。</span><span class="sxs-lookup"><span data-stu-id="3e80b-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e80b-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3e80b-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e80b-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e80b-111">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e80b-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e80b-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3e80b-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e80b-113">語法</span><span class="sxs-lookup"><span data-stu-id="3e80b-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3e80b-114">成員</span><span class="sxs-lookup"><span data-stu-id="3e80b-114">Members</span></span>

<span data-ttu-id="3e80b-115">**CIM \_ LogicalDiskBasedOnPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e80b-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="3e80b-116">屬性</span><span class="sxs-lookup"><span data-stu-id="3e80b-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e80b-117">屬性</span><span class="sxs-lookup"><span data-stu-id="3e80b-117">Properties</span></span>

<span data-ttu-id="3e80b-118">**CIM \_ LogicalDiskBasedOnPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3e80b-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e80b-119">**先行**</span><span class="sxs-lookup"><span data-stu-id="3e80b-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e80b-120">資料類型： **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="3e80b-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="3e80b-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e80b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e80b-122">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="3e80b-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3e80b-123">描述磁碟分割的 [**CIM \_ DiskPartition**](cim-diskpartition.md) 。</span><span class="sxs-lookup"><span data-stu-id="3e80b-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="3e80b-124">**依賴**</span><span class="sxs-lookup"><span data-stu-id="3e80b-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e80b-125">資料類型： **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="3e80b-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="3e80b-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e80b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e80b-127">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="3e80b-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3e80b-128">[**CIM \_ LogicalDisk**](cim-logicaldisk.md) ，描述建立在磁碟分割上的邏輯磁片。</span><span class="sxs-lookup"><span data-stu-id="3e80b-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="3e80b-129">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="3e80b-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e80b-130">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3e80b-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e80b-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e80b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e80b-132">指出較低層級儲存體中的高階範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="3e80b-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="3e80b-133">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="3e80b-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="3e80b-134">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="3e80b-135">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e80b-136">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="3e80b-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e80b-137">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3e80b-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e80b-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e80b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e80b-139">表示較低層級儲存體中的高階範圍開始。</span><span class="sxs-lookup"><span data-stu-id="3e80b-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="3e80b-140">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="3e80b-141">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e80b-142">備註</span><span class="sxs-lookup"><span data-stu-id="3e80b-142">Remarks</span></span>

<span data-ttu-id="3e80b-143">**Cim \_ LogicalDiskBasedOnPartition** 類別衍生自 [**cim \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="3e80b-144">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3e80b-144">WMI does not implement this class.</span></span> <span data-ttu-id="3e80b-145">針對衍生自 **CIM \_ LogicalDiskBasedOnPartition** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3e80b-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3e80b-146">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3e80b-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e80b-147">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3e80b-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e80b-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e80b-148">Requirements</span></span>



| <span data-ttu-id="3e80b-149">需求</span><span class="sxs-lookup"><span data-stu-id="3e80b-149">Requirement</span></span> | <span data-ttu-id="3e80b-150">值</span><span class="sxs-lookup"><span data-stu-id="3e80b-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e80b-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e80b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3e80b-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e80b-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e80b-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e80b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3e80b-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e80b-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e80b-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="3e80b-155">Namespace</span></span><br/>                | <span data-ttu-id="3e80b-156">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3e80b-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e80b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3e80b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e80b-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e80b-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e80b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3e80b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e80b-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e80b-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e80b-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e80b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e80b-162">**CIM \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="3e80b-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

