---
description: 以回送模式連接虛擬硬碟檔案。
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Msvm_ImageManagementService 類別的 AttachVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849342"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="cb43c-103">Msvm ImageManagementService 類別的 AttachVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cb43c-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="cb43c-104">以回送模式連接虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="cb43c-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb43c-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb43c-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cb43c-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb43c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb43c-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb43c-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb43c-108">完整路徑，指定要附加之虛擬硬碟檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="cb43c-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="cb43c-109">*AssignDriveLetter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb43c-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb43c-110">指出是否將磁碟機號指派給磁片的磁片區。</span><span class="sxs-lookup"><span data-stu-id="cb43c-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="cb43c-111">*ReadOnly* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb43c-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb43c-112">指出連接的硬碟是否應該是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="cb43c-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="cb43c-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cb43c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb43c-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="cb43c-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb43c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb43c-115">Return value</span></span>

<span data-ttu-id="cb43c-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cb43c-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cb43c-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="cb43c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="cb43c-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="cb43c-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="cb43c-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="cb43c-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="cb43c-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="cb43c-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="cb43c-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="cb43c-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="cb43c-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="cb43c-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="cb43c-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="cb43c-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="cb43c-130">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="cb43c-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cb43c-131">備註</span><span class="sxs-lookup"><span data-stu-id="cb43c-131">Remarks</span></span>

<span data-ttu-id="cb43c-132">若要卸離虛擬硬碟，請使用 [**Msvm \_ MountedStorageImage. DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cb43c-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="cb43c-133">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="cb43c-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cb43c-134">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="cb43c-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="cb43c-135">範例</span><span class="sxs-lookup"><span data-stu-id="cb43c-135">Examples</span></span>

<span data-ttu-id="cb43c-136">下列 c # 範例顯示如何連接虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="cb43c-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="cb43c-137">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="cb43c-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="cb43c-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb43c-138">Requirements</span></span>



| <span data-ttu-id="cb43c-139">需求</span><span class="sxs-lookup"><span data-stu-id="cb43c-139">Requirement</span></span> | <span data-ttu-id="cb43c-140">值</span><span class="sxs-lookup"><span data-stu-id="cb43c-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb43c-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cb43c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cb43c-142">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb43c-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cb43c-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cb43c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cb43c-144">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb43c-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb43c-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="cb43c-145">Namespace</span></span><br/>                | <span data-ttu-id="cb43c-146">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="cb43c-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cb43c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cb43c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb43c-148"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cb43c-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb43c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cb43c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb43c-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb43c-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb43c-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb43c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb43c-152">**Msvm \_ MountedStorageImage. DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="cb43c-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="cb43c-153">**掛接 (V1)**</span><span class="sxs-lookup"><span data-stu-id="cb43c-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="cb43c-154">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="cb43c-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

