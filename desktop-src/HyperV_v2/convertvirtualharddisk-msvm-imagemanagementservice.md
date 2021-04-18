---
description: 將現有的虛擬硬碟轉換成不同的類型或格式。
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Msvm_ImageManagementService 類別的 ConvertVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978221"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="bb15d-103">Msvm ImageManagementService 類別的 ConvertVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bb15d-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="bb15d-104">將現有的虛擬硬碟轉換成不同的類型或格式。</span><span class="sxs-lookup"><span data-stu-id="bb15d-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="bb15d-105">這個方法會建立新的虛擬硬碟，而且不會就地轉換來源虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="bb15d-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="bb15d-106">請參閱此方法使用限制的備註。</span><span class="sxs-lookup"><span data-stu-id="bb15d-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb15d-107">語法</span><span class="sxs-lookup"><span data-stu-id="bb15d-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bb15d-108">參數</span><span class="sxs-lookup"><span data-stu-id="bb15d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb15d-109">*SourcePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb15d-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb15d-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bb15d-110">Type: **string**</span></span>

<span data-ttu-id="bb15d-111">要轉換的來源虛擬硬碟檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="bb15d-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="bb15d-112">這項作業不會修改此檔案。</span><span class="sxs-lookup"><span data-stu-id="bb15d-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="bb15d-113">*VirtualDiskSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb15d-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb15d-114">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bb15d-114">Type: **string**</span></span>

<span data-ttu-id="bb15d-115">[**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)類別的字串表示，指定新虛擬硬碟的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb15d-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="bb15d-116">必須設定 **Path**、 **Type**、 **Format**、 **ParentPath**、 **區塊** 和 **LogicalSectorSize** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bb15d-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="bb15d-117">如果不需要， **ParentPath** 屬性可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bb15d-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="bb15d-118">將 [ **區塊** ] 和 [ **LogicalSectorSize** ] 屬性設定為0，以使用預設值。</span><span class="sxs-lookup"><span data-stu-id="bb15d-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="bb15d-119">若要指定新虛擬硬碟 (VHD 或 VHDX) 的格式，請將 **路徑** 的副檔名設定為適當的值 ( ".vhd" 或 ".vhdx" ) 。</span><span class="sxs-lookup"><span data-stu-id="bb15d-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="bb15d-120">**Format** 屬性必須符合 **路徑** 中的副檔名。</span><span class="sxs-lookup"><span data-stu-id="bb15d-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="bb15d-121">**LogicalSectorSize** 屬性將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="bb15d-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="bb15d-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bb15d-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb15d-123">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bb15d-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="bb15d-124">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bb15d-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb15d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb15d-125">Return value</span></span>

<span data-ttu-id="bb15d-126">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bb15d-126">Type: **uint32**</span></span>

<span data-ttu-id="bb15d-127">這個方法可能會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bb15d-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bb15d-128">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="bb15d-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-129">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="bb15d-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-130">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="bb15d-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-131">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="bb15d-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-132">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="bb15d-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-133">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="bb15d-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-134">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="bb15d-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-135">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="bb15d-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-136">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="bb15d-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-137">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="bb15d-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-138">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="bb15d-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-139">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="bb15d-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-140">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="bb15d-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bb15d-141">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="bb15d-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bb15d-142">備註</span><span class="sxs-lookup"><span data-stu-id="bb15d-142">Remarks</span></span>

<span data-ttu-id="bb15d-143">只有下列類型的虛擬硬碟可搭配此方法使用：</span><span class="sxs-lookup"><span data-stu-id="bb15d-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="bb15d-144">修正 VHD</span><span class="sxs-lookup"><span data-stu-id="bb15d-144">Fixed VHD</span></span>
-   <span data-ttu-id="bb15d-145">固定 VHDX</span><span class="sxs-lookup"><span data-stu-id="bb15d-145">Fixed VHDX</span></span>
-   <span data-ttu-id="bb15d-146">動態 VHD</span><span class="sxs-lookup"><span data-stu-id="bb15d-146">Dynamic VHD</span></span>
-   <span data-ttu-id="bb15d-147">動態 VHDX</span><span class="sxs-lookup"><span data-stu-id="bb15d-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="bb15d-148">差異 VHD</span><span class="sxs-lookup"><span data-stu-id="bb15d-148">Differencing VHD</span></span>
-   <span data-ttu-id="bb15d-149">差異 VHDX</span><span class="sxs-lookup"><span data-stu-id="bb15d-149">Differencing VHDX</span></span>

<span data-ttu-id="bb15d-150">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="bb15d-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bb15d-151">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="bb15d-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="bb15d-152">範例</span><span class="sxs-lookup"><span data-stu-id="bb15d-152">Examples</span></span>

<span data-ttu-id="bb15d-153">下列 c # 範例會轉換虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="bb15d-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="bb15d-154">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="bb15d-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="bb15d-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb15d-155">Requirements</span></span>



| <span data-ttu-id="bb15d-156">需求</span><span class="sxs-lookup"><span data-stu-id="bb15d-156">Requirement</span></span> | <span data-ttu-id="bb15d-157">值</span><span class="sxs-lookup"><span data-stu-id="bb15d-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb15d-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb15d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="bb15d-159">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb15d-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb15d-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb15d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="bb15d-161">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb15d-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb15d-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="bb15d-162">Namespace</span></span><br/>                | <span data-ttu-id="bb15d-163">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bb15d-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb15d-164">MOF</span><span class="sxs-lookup"><span data-stu-id="bb15d-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb15d-165"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bb15d-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb15d-166">DLL</span><span class="sxs-lookup"><span data-stu-id="bb15d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb15d-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb15d-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb15d-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb15d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb15d-169">**ConvertVirtualHardDisk (V1)**</span><span class="sxs-lookup"><span data-stu-id="bb15d-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="bb15d-170">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bb15d-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bb15d-171">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="bb15d-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

