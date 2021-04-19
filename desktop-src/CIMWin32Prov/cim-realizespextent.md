---
description: CIM \_ RealizesPExtent 關聯表示在實體媒體上實現實體範圍的關聯性。 此外，也會指定實體媒體上實體範圍的起始位址。
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: CIM_RealizesPExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973575"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="1d62c-104">CIM \_ RealizesPExtent 類別</span><span class="sxs-lookup"><span data-stu-id="1d62c-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="1d62c-105">**CIM \_ RealizesPExtent** 關聯表示在實體媒體上實現實體範圍的關聯性。</span><span class="sxs-lookup"><span data-stu-id="1d62c-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="1d62c-106">此外，也會指定實體媒體上實體範圍的起始位址。</span><span class="sxs-lookup"><span data-stu-id="1d62c-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d62c-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1d62c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1d62c-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1d62c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1d62c-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d62c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1d62c-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1d62c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d62c-111">語法</span><span class="sxs-lookup"><span data-stu-id="1d62c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="1d62c-112">成員</span><span class="sxs-lookup"><span data-stu-id="1d62c-112">Members</span></span>

<span data-ttu-id="1d62c-113">**CIM \_ RealizesPExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1d62c-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="1d62c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1d62c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d62c-115">屬性</span><span class="sxs-lookup"><span data-stu-id="1d62c-115">Properties</span></span>

<span data-ttu-id="1d62c-116">**CIM \_ RealizesPExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1d62c-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d62c-117">**先行**</span><span class="sxs-lookup"><span data-stu-id="1d62c-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d62c-118">資料類型： **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="1d62c-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="1d62c-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d62c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d62c-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Antecedent」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) </span><span class="sxs-lookup"><span data-stu-id="1d62c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1d62c-121">[**CIM \_ PhysicalMedia**](cim-physicalmedia.md) ，描述已實現範圍的實體媒體。</span><span class="sxs-lookup"><span data-stu-id="1d62c-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="1d62c-122">**依賴**</span><span class="sxs-lookup"><span data-stu-id="1d62c-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d62c-123">資料類型： **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="1d62c-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="1d62c-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d62c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d62c-125">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="1d62c-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1d62c-126">[**CIM \_ PhysicalExtent**](cim-physicalextent.md) ，描述位於媒體上的實體範圍。</span><span class="sxs-lookup"><span data-stu-id="1d62c-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="1d62c-127">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="1d62c-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d62c-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1d62c-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d62c-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d62c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d62c-130">實體範圍開始處的實體媒體上的起始位址。</span><span class="sxs-lookup"><span data-stu-id="1d62c-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="1d62c-131">實體範圍的結束位址是使用 [**CIM \_ PhysicalExtent**](cim-physicalextent.md)物件的 **NumberOfBlocks** 和 **區塊** 屬性來決定。</span><span class="sxs-lookup"><span data-stu-id="1d62c-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="1d62c-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="1d62c-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d62c-133">備註</span><span class="sxs-lookup"><span data-stu-id="1d62c-133">Remarks</span></span>

<span data-ttu-id="1d62c-134">**Cim \_ RealizesPExtent** 類別衍生自 [**cim \_**](cim-realizes.md)。</span><span class="sxs-lookup"><span data-stu-id="1d62c-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="1d62c-135">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1d62c-135">WMI does not implement this class.</span></span>

<span data-ttu-id="1d62c-136">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1d62c-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1d62c-137">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1d62c-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d62c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d62c-138">Requirements</span></span>



| <span data-ttu-id="1d62c-139">需求</span><span class="sxs-lookup"><span data-stu-id="1d62c-139">Requirement</span></span> | <span data-ttu-id="1d62c-140">值</span><span class="sxs-lookup"><span data-stu-id="1d62c-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d62c-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d62c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1d62c-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d62c-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d62c-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d62c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1d62c-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d62c-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d62c-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d62c-145">Namespace</span></span><br/>                | <span data-ttu-id="1d62c-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1d62c-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d62c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="1d62c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d62c-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d62c-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d62c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1d62c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d62c-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d62c-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d62c-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d62c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d62c-152">**CIM \_ 意識**</span><span class="sxs-lookup"><span data-stu-id="1d62c-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

