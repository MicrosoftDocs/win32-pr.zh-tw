---
description: 壓縮虛擬硬碟檔案。
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Msvm_ImageManagementService 類別的 CompactVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971475"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="2d8b5-103">Msvm ImageManagementService 類別的 CompactVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2d8b5-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="2d8b5-104">壓縮虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="2d8b5-105">壓縮是釋放虛擬硬碟未使用部分的進程。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="2d8b5-106">系統不會自動裝載虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="2d8b5-107">請參閱此方法使用限制的備註。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8b5-108">語法</span><span class="sxs-lookup"><span data-stu-id="2d8b5-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2d8b5-109">參數</span><span class="sxs-lookup"><span data-stu-id="2d8b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d8b5-110">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d8b5-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8b5-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2d8b5-111">Type: **string**</span></span>

<span data-ttu-id="2d8b5-112">指定合併檔位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="2d8b5-113">*模式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d8b5-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8b5-114">類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2d8b5-114">Type: **uint16**</span></span>

<span data-ttu-id="2d8b5-115">指定 compact 操作的模式。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="2d8b5-116">這必須是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="2d8b5-117">**Full** (0) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="2d8b5-118">**快速** (1) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="2d8b5-119">**Retrim** (2) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="2d8b5-120">**Pretrimmed** (3) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="2d8b5-121">**Prezeroed** (4) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2d8b5-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2d8b5-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d8b5-123">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2d8b5-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="2d8b5-124">如果工作已完成) ，則作業 (的參考可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d8b5-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d8b5-125">Return value</span></span>

<span data-ttu-id="2d8b5-126">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2d8b5-126">Type: **uint32**</span></span>

<span data-ttu-id="2d8b5-127">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2d8b5-128">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-129">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-130">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-131">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-132">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-133">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-134">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-135">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-136">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-137">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-138">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-139">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-140">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2d8b5-141">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="2d8b5-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2d8b5-142">備註</span><span class="sxs-lookup"><span data-stu-id="2d8b5-142">Remarks</span></span>

<span data-ttu-id="2d8b5-143">只有下列類型的虛擬硬碟可搭配此方法使用：</span><span class="sxs-lookup"><span data-stu-id="2d8b5-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="2d8b5-144">固定 VHDX</span><span class="sxs-lookup"><span data-stu-id="2d8b5-144">Fixed VHDX</span></span>
-   <span data-ttu-id="2d8b5-145">動態 VHD</span><span class="sxs-lookup"><span data-stu-id="2d8b5-145">Dynamic VHD</span></span>
-   <span data-ttu-id="2d8b5-146">動態 VHDX</span><span class="sxs-lookup"><span data-stu-id="2d8b5-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="2d8b5-147">差異 VHD</span><span class="sxs-lookup"><span data-stu-id="2d8b5-147">Differencing VHD</span></span>
-   <span data-ttu-id="2d8b5-148">差異 VHDX</span><span class="sxs-lookup"><span data-stu-id="2d8b5-148">Differencing VHDX</span></span>

<span data-ttu-id="2d8b5-149">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2d8b5-150">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="2d8b5-151">範例</span><span class="sxs-lookup"><span data-stu-id="2d8b5-151">Examples</span></span>

<span data-ttu-id="2d8b5-152">下列 c # 範例會壓縮虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="2d8b5-153">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="2d8b5-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="2d8b5-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d8b5-154">Requirements</span></span>



| <span data-ttu-id="2d8b5-155">需求</span><span class="sxs-lookup"><span data-stu-id="2d8b5-155">Requirement</span></span> | <span data-ttu-id="2d8b5-156">值</span><span class="sxs-lookup"><span data-stu-id="2d8b5-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8b5-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d8b5-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8b5-158">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d8b5-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2d8b5-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d8b5-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8b5-160">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d8b5-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d8b5-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d8b5-161">Namespace</span></span><br/>                | <span data-ttu-id="2d8b5-162">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2d8b5-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2d8b5-163">MOF</span><span class="sxs-lookup"><span data-stu-id="2d8b5-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d8b5-164"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2d8b5-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d8b5-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2d8b5-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d8b5-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d8b5-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d8b5-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d8b5-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d8b5-168">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d8b5-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2d8b5-169">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="2d8b5-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

