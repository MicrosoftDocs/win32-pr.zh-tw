---
description: 當虛擬機器在 VM 電腦系統上執行時， (VM)  (的相容性資訊，) 或在主機電腦系統上執行 (時的主機) 。
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850296"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="b50df-103">Msvm \_ CompatibilityVector 類別</span><span class="sxs-lookup"><span data-stu-id="b50df-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="b50df-104">當虛擬機器在 VM 電腦系統上執行時， (VM)  (的相容性資訊，) 或在主機電腦系統上執行 (時的主機) 。</span><span class="sxs-lookup"><span data-stu-id="b50df-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="b50df-105">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b50df-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50df-106">語法</span><span class="sxs-lookup"><span data-stu-id="b50df-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="b50df-107">成員</span><span class="sxs-lookup"><span data-stu-id="b50df-107">Members</span></span>

<span data-ttu-id="b50df-108">**Msvm \_ CompatibilityVector** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b50df-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="b50df-109">屬性</span><span class="sxs-lookup"><span data-stu-id="b50df-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b50df-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b50df-110">Properties</span></span>

<span data-ttu-id="b50df-111">**Msvm \_ CompatibilityVector** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b50df-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b50df-112">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="b50df-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b50df-113">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b50df-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b50df-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b50df-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b50df-115">識別只有當兩個向量相容時，才會傳回 true 的比較運算。</span><span class="sxs-lookup"><span data-stu-id="b50df-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="b50df-116">VM 的資料位於比較的左側，而該主機的資料位於右邊的位置。</span><span class="sxs-lookup"><span data-stu-id="b50df-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="b50df-117">**等於** (0) </span><span class="sxs-lookup"><span data-stu-id="b50df-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="b50df-118">**超集合** (1) </span><span class="sxs-lookup"><span data-stu-id="b50df-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="b50df-119">**子集** (2) </span><span class="sxs-lookup"><span data-stu-id="b50df-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="b50df-120">無 **交集** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="b50df-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="b50df-121">**GreaterThan** (4) </span><span class="sxs-lookup"><span data-stu-id="b50df-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="b50df-122">**GreaterThanOrEqual** (5) </span><span class="sxs-lookup"><span data-stu-id="b50df-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="b50df-123">**LessThan** (6) </span><span class="sxs-lookup"><span data-stu-id="b50df-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="b50df-124">**LessThanOrEqual** (7) </span><span class="sxs-lookup"><span data-stu-id="b50df-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="b50df-125">**多** (8) </span><span class="sxs-lookup"><span data-stu-id="b50df-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="b50df-126"> (9) **整除**</span><span class="sxs-lookup"><span data-stu-id="b50df-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b50df-127">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="b50df-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b50df-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b50df-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b50df-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b50df-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b50df-130">用於比較的實際相容性屬性資料。</span><span class="sxs-lookup"><span data-stu-id="b50df-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="b50df-131">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="b50df-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b50df-132">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b50df-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b50df-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b50df-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b50df-134">識別表示特定屬性的相容性向量。</span><span class="sxs-lookup"><span data-stu-id="b50df-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="b50df-135">這個屬性是用來比對主機和 VM 之間的對應向量。</span><span class="sxs-lookup"><span data-stu-id="b50df-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b50df-136">備註</span><span class="sxs-lookup"><span data-stu-id="b50df-136">Remarks</span></span>

<span data-ttu-id="b50df-137">[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)方法會傳回主機 (的 **Msvm \_ CompatibilityVector** 實例陣列，如果在主機) 上執行，或在 vm) 上執行，則為 vm (。</span><span class="sxs-lookup"><span data-stu-id="b50df-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="b50df-138">清單中的每個 **Msvm \_ CompatibilityVector** 專案都會描述相容性屬性向量。</span><span class="sxs-lookup"><span data-stu-id="b50df-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="b50df-139">若要讓 VM 與主機相容，其所有相容性屬性都必須與主機的屬性相容。</span><span class="sxs-lookup"><span data-stu-id="b50df-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="b50df-140">每個 **Msvm \_ CompatibilityVector** 專案都有下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b50df-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="b50df-141">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="b50df-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="b50df-142">唯一識別相容性向量。</span><span class="sxs-lookup"><span data-stu-id="b50df-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="b50df-143">這是用來比對向量，以在主機和 VM 之間進行比較。</span><span class="sxs-lookup"><span data-stu-id="b50df-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="b50df-144">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="b50df-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="b50df-145">識別判斷向量是否相容的比較運算。</span><span class="sxs-lookup"><span data-stu-id="b50df-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="b50df-146">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="b50df-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="b50df-147">包含實際的相容性屬性;這實際上是屬性承載 (例如處理器功能遮罩、快取行排清大小等等 ) </span><span class="sxs-lookup"><span data-stu-id="b50df-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="b50df-148">針對 **CompareOperation** 所定義的作業集合只涉及基本的整數比較和位邏輯。</span><span class="sxs-lookup"><span data-stu-id="b50df-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="b50df-149">這可讓 **CompatibilityInfo** 的實際內容保持不變。</span><span class="sxs-lookup"><span data-stu-id="b50df-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="b50df-150">作業集包括：</span><span class="sxs-lookup"><span data-stu-id="b50df-150">The set of operations include:</span></span>



| <span data-ttu-id="b50df-151">CompareOperation</span><span class="sxs-lookup"><span data-stu-id="b50df-151">CompareOperation</span></span> | <span data-ttu-id="b50df-152">Description</span><span class="sxs-lookup"><span data-stu-id="b50df-152">Description</span></span>                                      | <span data-ttu-id="b50df-153">虛擬虛擬的比較</span><span class="sxs-lookup"><span data-stu-id="b50df-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="b50df-154">VmCcEqual</span><span class="sxs-lookup"><span data-stu-id="b50df-154">VmCcEqual</span></span>        | <span data-ttu-id="b50df-155">VmAttr 必須等於 HostAttr</span><span class="sxs-lookup"><span data-stu-id="b50df-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="b50df-156">如果 (VmAttr = = HostAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="b50df-157">VmCcSuperSet</span><span class="sxs-lookup"><span data-stu-id="b50df-157">VmCcSuperSet</span></span>     | <span data-ttu-id="b50df-158">VmAttr 必須是 HostAttr 的超集合</span><span class="sxs-lookup"><span data-stu-id="b50df-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="b50df-159">如果 ( (VmAttr & HostAttr) = = HostAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="b50df-160">VmCcSubSet</span><span class="sxs-lookup"><span data-stu-id="b50df-160">VmCcSubSet</span></span>       | <span data-ttu-id="b50df-161">VmAttr 必須是 HostAttr 的子集</span><span class="sxs-lookup"><span data-stu-id="b50df-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="b50df-162">如果 ( (VmAttr & HostAttr) = = VmAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="b50df-163">VmCcDisjointSet</span><span class="sxs-lookup"><span data-stu-id="b50df-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="b50df-164">VmAttr 必須是 HostAttr 中的斷續集合</span><span class="sxs-lookup"><span data-stu-id="b50df-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="b50df-165">如果 ( (VmAttr & HostAttr) = = 0) </span><span class="sxs-lookup"><span data-stu-id="b50df-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="b50df-166">VmCcGreater</span><span class="sxs-lookup"><span data-stu-id="b50df-166">VmCcGreater</span></span>      | <span data-ttu-id="b50df-167">VmAttr 必須大於 HostAttr</span><span class="sxs-lookup"><span data-stu-id="b50df-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="b50df-168">如果 (VmAttr > HostAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="b50df-169">VmCcGreaterEqual</span><span class="sxs-lookup"><span data-stu-id="b50df-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="b50df-170">VmAttr 必須大於或等於 HostAttr</span><span class="sxs-lookup"><span data-stu-id="b50df-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="b50df-171">如果 (VmAttr >= HostAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="b50df-172">VmCcLess</span><span class="sxs-lookup"><span data-stu-id="b50df-172">VmCcLess</span></span>         | <span data-ttu-id="b50df-173">VmAttr 必須小於 HostAttr</span><span class="sxs-lookup"><span data-stu-id="b50df-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="b50df-174">如果 (VmAttr < HostAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="b50df-175">VmCcLessEqual</span><span class="sxs-lookup"><span data-stu-id="b50df-175">VmCcLessEqual</span></span>    | <span data-ttu-id="b50df-176">VmAttr 必須小於或等於 HostAttr</span><span class="sxs-lookup"><span data-stu-id="b50df-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="b50df-177">如果 (VmAttr <= HostAttr) </span><span class="sxs-lookup"><span data-stu-id="b50df-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="b50df-178">VmCcMultiple</span><span class="sxs-lookup"><span data-stu-id="b50df-178">VmCcMultiple</span></span>     | <span data-ttu-id="b50df-179">VmAttr 必須是 HostAttr 的倍數</span><span class="sxs-lookup"><span data-stu-id="b50df-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="b50df-180">如果 ( (VmAttr% HostAttr) = = 0) </span><span class="sxs-lookup"><span data-stu-id="b50df-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="b50df-181">VmCcDivisor</span><span class="sxs-lookup"><span data-stu-id="b50df-181">VmCcDivisor</span></span>      | <span data-ttu-id="b50df-182">VmAttr 必須是 HostAttr 的除數</span><span class="sxs-lookup"><span data-stu-id="b50df-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="b50df-183">如果 ( (HostAttr% VmAttr) = = 0) </span><span class="sxs-lookup"><span data-stu-id="b50df-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="b50df-184">SCVMM 必須執行下列步驟，以判斷 VM 是否與主機相容。</span><span class="sxs-lookup"><span data-stu-id="b50df-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="b50df-185">**判斷 VM 是否與主機相容**</span><span class="sxs-lookup"><span data-stu-id="b50df-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="b50df-186">逐一查看 VM 的所有 **Msvm \_ CompatibilityVector** 元素。</span><span class="sxs-lookup"><span data-stu-id="b50df-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="b50df-187">針對每個 **Msvm \_ CompatibilityVector** 專案，使用在 **CompareOperation** 中指定的相容性作業，將 VM 的硬體相容性向量與主機的對應相容性向量進行比較。</span><span class="sxs-lookup"><span data-stu-id="b50df-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="b50df-188">如果 VM 中的所有 **Msvm \_ CompatibilityVector** 元素都被視為相容，則 vm 與主機 (相容) 的處理器功能觀點。</span><span class="sxs-lookup"><span data-stu-id="b50df-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="b50df-189">規格需求</span><span class="sxs-lookup"><span data-stu-id="b50df-189">Requirements</span></span>



| <span data-ttu-id="b50df-190">需求</span><span class="sxs-lookup"><span data-stu-id="b50df-190">Requirement</span></span> | <span data-ttu-id="b50df-191">值</span><span class="sxs-lookup"><span data-stu-id="b50df-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b50df-192">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b50df-192">Minimum supported client</span></span><br/> | <span data-ttu-id="b50df-193">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b50df-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b50df-194">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b50df-194">Minimum supported server</span></span><br/> | <span data-ttu-id="b50df-195">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b50df-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b50df-196">命名空間</span><span class="sxs-lookup"><span data-stu-id="b50df-196">Namespace</span></span><br/>                | <span data-ttu-id="b50df-197">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b50df-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b50df-198">MOF</span><span class="sxs-lookup"><span data-stu-id="b50df-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b50df-199"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b50df-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b50df-200">DLL</span><span class="sxs-lookup"><span data-stu-id="b50df-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b50df-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b50df-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b50df-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b50df-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50df-203">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="b50df-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="b50df-204">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="b50df-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




