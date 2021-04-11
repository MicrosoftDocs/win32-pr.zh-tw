---
description: CIM \_ RealizesDiskPartition 類別代表實體媒體上的磁碟分割，此磁碟分割會建立原始 SCSI 或 IDE 磁片磁碟機上磁碟分割的建立模型。
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: CIM_RealizesDiskPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110613"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="451d1-103">CIM \_ RealizesDiskPartition 類別</span><span class="sxs-lookup"><span data-stu-id="451d1-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="451d1-104">**CIM \_ RealizesDiskPartition** 類別代表實體媒體上的磁碟分割，此磁碟分割會建立原始 SCSI 或 IDE 磁片磁碟機上磁碟分割的建立模型。</span><span class="sxs-lookup"><span data-stu-id="451d1-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="451d1-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="451d1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="451d1-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="451d1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="451d1-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="451d1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="451d1-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="451d1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="451d1-109">語法</span><span class="sxs-lookup"><span data-stu-id="451d1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="451d1-110">成員</span><span class="sxs-lookup"><span data-stu-id="451d1-110">Members</span></span>

<span data-ttu-id="451d1-111">**CIM \_ RealizesDiskPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="451d1-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="451d1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="451d1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="451d1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="451d1-113">Properties</span></span>

<span data-ttu-id="451d1-114">**CIM \_ RealizesDiskPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="451d1-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="451d1-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="451d1-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451d1-116">資料類型： **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="451d1-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="451d1-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="451d1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="451d1-118">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="451d1-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="451d1-119">[**CIM \_ PhysicalMedia**](cim-physicalmedia.md) ，描述已實現範圍的實體媒體。</span><span class="sxs-lookup"><span data-stu-id="451d1-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="451d1-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="451d1-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451d1-121">資料類型： **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="451d1-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="451d1-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="451d1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="451d1-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="451d1-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="451d1-124">[**CIM \_ DiskPartition**](cim-diskpartition.md) ，描述位於媒體上的磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="451d1-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="451d1-125">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="451d1-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451d1-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="451d1-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="451d1-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="451d1-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="451d1-128">開始磁碟分割的實體媒體上的起始位址。</span><span class="sxs-lookup"><span data-stu-id="451d1-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="451d1-129">分割區的結束位址是使用 [**CIM \_ DiskPartition**](cim-diskpartition.md)物件的 **NumberOfBlocks** 和 **區塊** 屬性來決定。</span><span class="sxs-lookup"><span data-stu-id="451d1-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="451d1-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="451d1-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="451d1-131">備註</span><span class="sxs-lookup"><span data-stu-id="451d1-131">Remarks</span></span>

<span data-ttu-id="451d1-132">**Cim \_ RealizesDiskPartition** 類別衍生自 [**cim \_**](cim-realizes.md)。</span><span class="sxs-lookup"><span data-stu-id="451d1-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="451d1-133">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="451d1-133">WMI does not implement this class.</span></span>

<span data-ttu-id="451d1-134">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="451d1-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="451d1-135">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="451d1-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="451d1-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="451d1-136">Requirements</span></span>



| <span data-ttu-id="451d1-137">需求</span><span class="sxs-lookup"><span data-stu-id="451d1-137">Requirement</span></span> | <span data-ttu-id="451d1-138">值</span><span class="sxs-lookup"><span data-stu-id="451d1-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="451d1-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="451d1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="451d1-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="451d1-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="451d1-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="451d1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="451d1-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="451d1-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="451d1-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="451d1-143">Namespace</span></span><br/>                | <span data-ttu-id="451d1-144">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="451d1-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="451d1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="451d1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="451d1-146"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="451d1-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="451d1-147">DLL</span><span class="sxs-lookup"><span data-stu-id="451d1-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="451d1-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="451d1-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="451d1-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="451d1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451d1-150">**CIM \_ 意識**</span><span class="sxs-lookup"><span data-stu-id="451d1-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

