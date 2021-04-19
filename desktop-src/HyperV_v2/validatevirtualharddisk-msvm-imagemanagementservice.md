---
description: 判斷虛擬硬碟檔案是否有效。
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Msvm_ImageManagementService 類別的 ValidateVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975876"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="90016-103">Msvm ImageManagementService 類別的 ValidateVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="90016-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="90016-104">判斷虛擬硬碟檔案是否有效。</span><span class="sxs-lookup"><span data-stu-id="90016-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="90016-105">語法</span><span class="sxs-lookup"><span data-stu-id="90016-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="90016-106">參數</span><span class="sxs-lookup"><span data-stu-id="90016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90016-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90016-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90016-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="90016-108">Type: **string**</span></span>

<span data-ttu-id="90016-109">指定虛擬硬碟檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="90016-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="90016-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="90016-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90016-111">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="90016-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="90016-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="90016-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90016-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="90016-113">Return value</span></span>

<span data-ttu-id="90016-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="90016-114">Type: **uint32**</span></span>

<span data-ttu-id="90016-115">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="90016-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="90016-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="90016-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90016-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="90016-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="90016-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="90016-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="90016-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="90016-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="90016-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="90016-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="90016-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="90016-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="90016-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="90016-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="90016-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="90016-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="90016-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="90016-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="90016-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="90016-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="90016-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="90016-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="90016-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="90016-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="90016-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="90016-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="90016-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="90016-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="90016-130">偵測 **到 Vhd 差異鏈迴圈** (32787) </span><span class="sxs-lookup"><span data-stu-id="90016-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="90016-131">備註</span><span class="sxs-lookup"><span data-stu-id="90016-131">Remarks</span></span>

<span data-ttu-id="90016-132">如果虛擬硬碟是差異磁片，則會開啟整個虛擬磁片鏈。</span><span class="sxs-lookup"><span data-stu-id="90016-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="90016-133">如果連結在磁片鏈中中斷，則會傳回一個工作物件，並初始化適當的錯誤，並將子系和父屬性初始化至連結中斷的位置。</span><span class="sxs-lookup"><span data-stu-id="90016-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="90016-134">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="90016-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="90016-135">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="90016-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="90016-136">範例</span><span class="sxs-lookup"><span data-stu-id="90016-136">Examples</span></span>

<span data-ttu-id="90016-137">下列 c # 範例會驗證虛擬硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="90016-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="90016-138">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="90016-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="90016-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="90016-139">Requirements</span></span>



| <span data-ttu-id="90016-140">需求</span><span class="sxs-lookup"><span data-stu-id="90016-140">Requirement</span></span> | <span data-ttu-id="90016-141">值</span><span class="sxs-lookup"><span data-stu-id="90016-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90016-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90016-142">Minimum supported client</span></span><br/> | <span data-ttu-id="90016-143">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90016-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="90016-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90016-144">Minimum supported server</span></span><br/> | <span data-ttu-id="90016-145">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90016-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90016-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="90016-146">Namespace</span></span><br/>                | <span data-ttu-id="90016-147">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="90016-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="90016-148">MOF</span><span class="sxs-lookup"><span data-stu-id="90016-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90016-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="90016-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90016-150">DLL</span><span class="sxs-lookup"><span data-stu-id="90016-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90016-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90016-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90016-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90016-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90016-153">**ValidateVirtualHardDisk (V1)**</span><span class="sxs-lookup"><span data-stu-id="90016-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="90016-154">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90016-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="90016-155">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="90016-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

