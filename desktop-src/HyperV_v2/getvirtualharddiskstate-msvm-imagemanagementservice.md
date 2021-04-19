---
description: 捕獲虛擬硬碟檔案的狀態資訊。
ms.assetid: 398b098b-dc1a-45e0-abcb-37b4b0a32290
title: Msvm_ImageManagementService 類別的 GetVirtualHardDiskState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e608078b88415eb683a95e3ba41d81b99014961d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975380"
---
# <a name="getvirtualharddiskstate-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="731f4-103">Msvm ImageManagementService 類別的 GetVirtualHardDiskState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="731f4-103">GetVirtualHardDiskState method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="731f4-104">捕獲虛擬硬碟檔案的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="731f4-104">Retrieves state information for a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="731f4-105">語法</span><span class="sxs-lookup"><span data-stu-id="731f4-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskState(
  [in]  string              Path,
  [out] string              State,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="731f4-106">參數</span><span class="sxs-lookup"><span data-stu-id="731f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="731f4-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="731f4-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="731f4-108">磁片影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="731f4-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="731f4-109">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="731f4-109">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="731f4-110">如果成功，則會收到 [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md) 類別的內嵌實例，其中包含虛擬硬碟的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="731f4-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskState**](msvm-virtualharddiskstate.md) class that contains the state information for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="731f4-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="731f4-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="731f4-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="731f4-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="731f4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="731f4-113">Return value</span></span>

<span data-ttu-id="731f4-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="731f4-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="731f4-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="731f4-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="731f4-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="731f4-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="731f4-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="731f4-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="731f4-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="731f4-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="731f4-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="731f4-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="731f4-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="731f4-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="731f4-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="731f4-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="731f4-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="731f4-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="731f4-129">備註</span><span class="sxs-lookup"><span data-stu-id="731f4-129">Remarks</span></span>

<span data-ttu-id="731f4-130">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="731f4-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="731f4-131">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="731f4-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="731f4-132">範例</span><span class="sxs-lookup"><span data-stu-id="731f4-132">Examples</span></span>

<span data-ttu-id="731f4-133">下列 c # 範例顯示如何呼叫 **GetVirtualHardDiskState** 方法。</span><span class="sxs-lookup"><span data-stu-id="731f4-133">The following C# example shows how to call the **GetVirtualHardDiskState** method.</span></span> <span data-ttu-id="731f4-134">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="731f4-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskState(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskState");

    inParams["Path"] = vhdPath;
    
    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskState", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskState was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskState was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["State"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="731f4-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="731f4-135">Requirements</span></span>



| <span data-ttu-id="731f4-136">需求</span><span class="sxs-lookup"><span data-stu-id="731f4-136">Requirement</span></span> | <span data-ttu-id="731f4-137">值</span><span class="sxs-lookup"><span data-stu-id="731f4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731f4-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="731f4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="731f4-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="731f4-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="731f4-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="731f4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="731f4-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="731f4-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="731f4-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="731f4-142">Namespace</span></span><br/>                | <span data-ttu-id="731f4-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="731f4-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="731f4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="731f4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="731f4-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="731f4-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="731f4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="731f4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="731f4-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="731f4-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="731f4-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="731f4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731f4-149">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="731f4-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

