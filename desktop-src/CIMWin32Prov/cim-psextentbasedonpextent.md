---
description: CIM \_ PSExtentBasedOnPExtent 類別會將以實體範圍為基礎的受保護空間範圍產生關聯。
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: CIM_PSExtentBasedOnPExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110616"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="49b79-103">CIM \_ PSExtentBasedOnPExtent 類別</span><span class="sxs-lookup"><span data-stu-id="49b79-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="49b79-104">**CIM \_ PSExtentBasedOnPExtent** 類別會將以實體範圍為基礎的受保護空間範圍產生關聯。</span><span class="sxs-lookup"><span data-stu-id="49b79-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49b79-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="49b79-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49b79-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="49b79-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49b79-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="49b79-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="49b79-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="49b79-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b79-109">語法</span><span class="sxs-lookup"><span data-stu-id="49b79-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="49b79-110">成員</span><span class="sxs-lookup"><span data-stu-id="49b79-110">Members</span></span>

<span data-ttu-id="49b79-111">**CIM \_ PSExtentBasedOnPExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="49b79-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="49b79-112">屬性</span><span class="sxs-lookup"><span data-stu-id="49b79-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49b79-113">屬性</span><span class="sxs-lookup"><span data-stu-id="49b79-113">Properties</span></span>

<span data-ttu-id="49b79-114">**CIM \_ PSExtentBasedOnPExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="49b79-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49b79-115">**先行**</span><span class="sxs-lookup"><span data-stu-id="49b79-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b79-116">資料類型： **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="49b79-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="49b79-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49b79-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b79-118">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="49b79-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="49b79-119">描述實體範圍的 [**CIM \_ PhysicalExtent**](cim-physicalextent.md) 。</span><span class="sxs-lookup"><span data-stu-id="49b79-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="49b79-120">**依賴**</span><span class="sxs-lookup"><span data-stu-id="49b79-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b79-121">資料類型： **CIM \_ ProtectedSpaceExtent**</span><span class="sxs-lookup"><span data-stu-id="49b79-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="49b79-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49b79-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49b79-123">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="49b79-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="49b79-124">[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) ，描述以實體範圍為基礎的受保護空間範圍。</span><span class="sxs-lookup"><span data-stu-id="49b79-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="49b79-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="49b79-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b79-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="49b79-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49b79-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49b79-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49b79-128">指出較低層級儲存體中的高階範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="49b79-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="49b79-129">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="49b79-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="49b79-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="49b79-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="49b79-131">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="49b79-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="49b79-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="49b79-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49b79-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="49b79-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="49b79-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49b79-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49b79-135">表示較低層級儲存體中的高階範圍開始。</span><span class="sxs-lookup"><span data-stu-id="49b79-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="49b79-136">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="49b79-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="49b79-137">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="49b79-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49b79-138">備註</span><span class="sxs-lookup"><span data-stu-id="49b79-138">Remarks</span></span>

<span data-ttu-id="49b79-139">**Cim \_ PSExtentBasedOnPExtent** 類別衍生自 [**cim \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="49b79-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="49b79-140">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="49b79-140">WMI does not implement this class.</span></span>

<span data-ttu-id="49b79-141">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="49b79-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49b79-142">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="49b79-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b79-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b79-143">Requirements</span></span>



| <span data-ttu-id="49b79-144">需求</span><span class="sxs-lookup"><span data-stu-id="49b79-144">Requirement</span></span> | <span data-ttu-id="49b79-145">值</span><span class="sxs-lookup"><span data-stu-id="49b79-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49b79-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49b79-146">Minimum supported client</span></span><br/> | <span data-ttu-id="49b79-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49b79-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49b79-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49b79-148">Minimum supported server</span></span><br/> | <span data-ttu-id="49b79-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49b79-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49b79-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="49b79-150">Namespace</span></span><br/>                | <span data-ttu-id="49b79-151">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49b79-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49b79-152">MOF</span><span class="sxs-lookup"><span data-stu-id="49b79-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49b79-153"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="49b79-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49b79-154">DLL</span><span class="sxs-lookup"><span data-stu-id="49b79-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49b79-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49b79-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b79-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49b79-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b79-157">**CIM \_ BasedOn**</span><span class="sxs-lookup"><span data-stu-id="49b79-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

