---
description: 使用鏈中的一或多個父虛擬硬碟，合併差異鏈中的子系虛擬硬碟。
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Msvm_ImageManagementService 類別的 MergeVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513769"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0c5b1-103">Msvm ImageManagementService 類別的 MergeVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0c5b1-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0c5b1-104">使用鏈中的一或多個父虛擬硬碟，合併差異鏈中的子系虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="0c5b1-105">請參閱此方法使用限制的備註。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="0c5b1-106">如果執行此功能的使用者沒有更新虛擬機器的許可權，則此函式將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5b1-107">語法</span><span class="sxs-lookup"><span data-stu-id="0c5b1-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0c5b1-108">參數</span><span class="sxs-lookup"><span data-stu-id="0c5b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c5b1-109">*SourcePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c5b1-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5b1-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c5b1-110">Type: **string**</span></span>

<span data-ttu-id="0c5b1-111">完整路徑，指定要合併之虛擬硬碟檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="0c5b1-112">*DestinationPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c5b1-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5b1-113">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c5b1-113">Type: **string**</span></span>

<span data-ttu-id="0c5b1-114">完整路徑，指定要合併資料的父虛擬硬碟檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="0c5b1-115">這可能是合併檔案的直屬父虛擬硬碟，或是上層磁片映射在差異鏈上的幾個層級。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="0c5b1-116">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0c5b1-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c5b1-117">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0c5b1-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="0c5b1-118">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c5b1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c5b1-119">Return value</span></span>

<span data-ttu-id="0c5b1-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0c5b1-120">Type: **uint32**</span></span>

<span data-ttu-id="0c5b1-121">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0c5b1-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-124">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-125">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-126">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-127">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-128">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-129">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-130">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-131">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-132">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-133">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-134">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0c5b1-135">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="0c5b1-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0c5b1-136">備註</span><span class="sxs-lookup"><span data-stu-id="0c5b1-136">Remarks</span></span>

<span data-ttu-id="0c5b1-137">子虛擬硬碟必須離線。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="0c5b1-138">只有下列類型的虛擬硬碟可搭配此方法使用：</span><span class="sxs-lookup"><span data-stu-id="0c5b1-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="0c5b1-139">差異 VHD</span><span class="sxs-lookup"><span data-stu-id="0c5b1-139">Differencing VHD</span></span>
-   <span data-ttu-id="0c5b1-140">差異 VHDX</span><span class="sxs-lookup"><span data-stu-id="0c5b1-140">Differencing VHDX</span></span>

<span data-ttu-id="0c5b1-141">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0c5b1-142">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0c5b1-143">範例</span><span class="sxs-lookup"><span data-stu-id="0c5b1-143">Examples</span></span>

<span data-ttu-id="0c5b1-144">下列 c # 範例會展開虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="0c5b1-145">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="0c5b1-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="0c5b1-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c5b1-146">Requirements</span></span>



| <span data-ttu-id="0c5b1-147">需求</span><span class="sxs-lookup"><span data-stu-id="0c5b1-147">Requirement</span></span> | <span data-ttu-id="0c5b1-148">值</span><span class="sxs-lookup"><span data-stu-id="0c5b1-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5b1-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c5b1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0c5b1-150">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c5b1-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c5b1-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c5b1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0c5b1-152">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c5b1-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c5b1-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c5b1-153">Namespace</span></span><br/>                | <span data-ttu-id="0c5b1-154">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0c5b1-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c5b1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0c5b1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c5b1-156"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0c5b1-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c5b1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0c5b1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c5b1-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c5b1-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c5b1-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c5b1-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c5b1-160">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c5b1-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c5b1-161">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="0c5b1-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

