---
description: 調整現有虛擬硬碟的大小。
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Msvm_ImageManagementService 類別的 ResizeVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972249"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="dafc4-103">Msvm ImageManagementService 類別的 ResizeVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dafc4-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="dafc4-104">調整現有虛擬硬碟的大小。</span><span class="sxs-lookup"><span data-stu-id="dafc4-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="dafc4-105">虛擬硬碟必須離線。</span><span class="sxs-lookup"><span data-stu-id="dafc4-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="dafc4-106">請參閱此方法使用限制的備註。</span><span class="sxs-lookup"><span data-stu-id="dafc4-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dafc4-107">語法</span><span class="sxs-lookup"><span data-stu-id="dafc4-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dafc4-108">參數</span><span class="sxs-lookup"><span data-stu-id="dafc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dafc4-109">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dafc4-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dafc4-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dafc4-110">Type: **string**</span></span>

<span data-ttu-id="dafc4-111">虛擬硬碟檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="dafc4-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="dafc4-112">*MaxInternalSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dafc4-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dafc4-113">類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="dafc4-113">Type: **uint64**</span></span>

<span data-ttu-id="dafc4-114">虛擬機器可看見的虛擬硬碟大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dafc4-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="dafc4-115">*MaxInternalSize* 最小值為 *DiskSize* + 512- (*DiskSize* mod 512) 。</span><span class="sxs-lookup"><span data-stu-id="dafc4-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="dafc4-116">*DiskSize* 是虛擬硬碟檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="dafc4-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="dafc4-117">如果指定的 *MaxInternalSize* 值小於最小值，則會傳回 InvalidParameter 錯誤 (32773) 。</span><span class="sxs-lookup"><span data-stu-id="dafc4-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="dafc4-118">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dafc4-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dafc4-119">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="dafc4-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="dafc4-120">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="dafc4-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dafc4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="dafc4-121">Return value</span></span>

<span data-ttu-id="dafc4-122">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dafc4-122">Type: **uint32**</span></span>

<span data-ttu-id="dafc4-123">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dafc4-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dafc4-124">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="dafc4-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-125">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="dafc4-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-126">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="dafc4-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-127">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="dafc4-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-128">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="dafc4-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-129">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="dafc4-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-130">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="dafc4-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-131">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="dafc4-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-132">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="dafc4-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-133">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="dafc4-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-134">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="dafc4-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-135">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="dafc4-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-136">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="dafc4-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="dafc4-137">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="dafc4-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="dafc4-138">備註</span><span class="sxs-lookup"><span data-stu-id="dafc4-138">Remarks</span></span>

<span data-ttu-id="dafc4-139">當虛擬硬碟的大小增加時，只有下列類型的虛擬硬碟可搭配此方法使用：</span><span class="sxs-lookup"><span data-stu-id="dafc4-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="dafc4-140">修正 VHD</span><span class="sxs-lookup"><span data-stu-id="dafc4-140">Fixed VHD</span></span>
-   <span data-ttu-id="dafc4-141">固定 VHDX</span><span class="sxs-lookup"><span data-stu-id="dafc4-141">Fixed VHDX</span></span>
-   <span data-ttu-id="dafc4-142">動態 VHD</span><span class="sxs-lookup"><span data-stu-id="dafc4-142">Dynamic VHD</span></span>
-   <span data-ttu-id="dafc4-143">動態 VHDX</span><span class="sxs-lookup"><span data-stu-id="dafc4-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="dafc4-144">差異 VHDX</span><span class="sxs-lookup"><span data-stu-id="dafc4-144">Differencing VHDX</span></span>

<span data-ttu-id="dafc4-145">當虛擬硬碟的大小減少時，您只能使用下列類型的虛擬硬碟搭配此方法：</span><span class="sxs-lookup"><span data-stu-id="dafc4-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="dafc4-146">固定 VHDX</span><span class="sxs-lookup"><span data-stu-id="dafc4-146">Fixed VHDX</span></span>
-   <span data-ttu-id="dafc4-147">動態 VHDX</span><span class="sxs-lookup"><span data-stu-id="dafc4-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="dafc4-148">差異 VHDX</span><span class="sxs-lookup"><span data-stu-id="dafc4-148">Differencing VHDX</span></span>

<span data-ttu-id="dafc4-149">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="dafc4-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dafc4-150">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="dafc4-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="dafc4-151">範例</span><span class="sxs-lookup"><span data-stu-id="dafc4-151">Examples</span></span>

<span data-ttu-id="dafc4-152">下列 c # 範例會展開虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="dafc4-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="dafc4-153">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="dafc4-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="dafc4-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="dafc4-154">Requirements</span></span>



| <span data-ttu-id="dafc4-155">需求</span><span class="sxs-lookup"><span data-stu-id="dafc4-155">Requirement</span></span> | <span data-ttu-id="dafc4-156">值</span><span class="sxs-lookup"><span data-stu-id="dafc4-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dafc4-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dafc4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="dafc4-158">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dafc4-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dafc4-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dafc4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="dafc4-160">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dafc4-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dafc4-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="dafc4-161">Namespace</span></span><br/>                | <span data-ttu-id="dafc4-162">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="dafc4-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dafc4-163">MOF</span><span class="sxs-lookup"><span data-stu-id="dafc4-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dafc4-164"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="dafc4-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dafc4-165">DLL</span><span class="sxs-lookup"><span data-stu-id="dafc4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dafc4-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dafc4-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dafc4-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dafc4-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="dafc4-168">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dafc4-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dafc4-169">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="dafc4-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

