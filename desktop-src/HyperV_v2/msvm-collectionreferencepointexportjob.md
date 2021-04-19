---
description: 此類別代表集合參考點匯出作業工作。
ms.assetid: c752ff1d-163c-4aa9-b29e-76478a18a08c
title: Msvm_CollectionReferencePointExportJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob
- Msvm_CollectionReferencePointExportJob.Cancellable
- Msvm_CollectionReferencePointExportJob.ErrorSummaryDescription
- Msvm_CollectionReferencePointExportJob.CollectionId
- Msvm_CollectionReferencePointExportJob.ReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.BaseReferencePointGroupId
- Msvm_CollectionReferencePointExportJob.VirtualMachineId
- Msvm_CollectionReferencePointExportJob.ExportDirectory
- Msvm_CollectionReferencePointExportJob.ExportedDisks
- Msvm_CollectionReferencePointExportJob.ExportedLogFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedConfigFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedRuntimeFilePaths
- Msvm_CollectionReferencePointExportJob.ExportedGuestStateFilePaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d21fab1519664471bdc2bb5d7102d94cbe3dde1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982763"
---
# <a name="msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="8b0c2-103">Msvm \_ CollectionReferencePointExportJob 類別</span><span class="sxs-lookup"><span data-stu-id="8b0c2-103">Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="8b0c2-104">此類別代表集合參考點匯出作業工作。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-104">This class represents a collection reference point export operation job.</span></span>

<span data-ttu-id="8b0c2-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b0c2-106">語法</span><span class="sxs-lookup"><span data-stu-id="8b0c2-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  CollectionId;
  string  ReferencePointGroupId;
  string  BaseReferencePointGroupId;
  string  VirtualMachineId[];
  string  ExportDirectory;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePaths[];
  string  ExportedRuntimeFilePaths[];
  string  ExportedGuestStateFilePaths[];
};
```

## <a name="members"></a><span data-ttu-id="8b0c2-107">成員</span><span class="sxs-lookup"><span data-stu-id="8b0c2-107">Members</span></span>

<span data-ttu-id="8b0c2-108">**Msvm \_ CollectionReferencePointExportJob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8b0c2-108">The **Msvm\_CollectionReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="8b0c2-109">方法</span><span class="sxs-lookup"><span data-stu-id="8b0c2-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b0c2-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8b0c2-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b0c2-111">方法</span><span class="sxs-lookup"><span data-stu-id="8b0c2-111">Methods</span></span>

<span data-ttu-id="8b0c2-112">**Msvm \_ CollectionReferencePointExportJob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-112">The **Msvm\_CollectionReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="8b0c2-113">方法</span><span class="sxs-lookup"><span data-stu-id="8b0c2-113">Method</span></span>                                                                                  | <span data-ttu-id="8b0c2-114">描述</span><span class="sxs-lookup"><span data-stu-id="8b0c2-114">Description</span></span>                                        |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="8b0c2-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-115">**GetError**</span></span>](msvm-collectionreferencepointexportjob-geterror.md)                     | <span data-ttu-id="8b0c2-116">捕獲錯誤。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-116">Retrieves an error.</span></span><br/>                     |
| [<span data-ttu-id="8b0c2-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-117">**GetErrorEx**</span></span>](msvm-collectionreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="8b0c2-118">抓取其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="8b0c2-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-119">**RequestStateChange**</span></span>](msvm-collectionreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="8b0c2-120">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="8b0c2-121">屬性</span><span class="sxs-lookup"><span data-stu-id="8b0c2-121">Properties</span></span>

<span data-ttu-id="8b0c2-122">**Msvm \_ CollectionReferencePointExportJob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-122">The **Msvm\_CollectionReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b0c2-123">**BaseReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-123">**BaseReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-126">在 exportoperation 中當做基底使用之集合參考點的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-126">GUID of the collection reference point which is used as the base in the exportoperation.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-127">**可取消**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-130">指出是否可以取消作業。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="8b0c2-131">這個屬性的值不保證取消作業的要求將會成功。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-132">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-132">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-135">Wereexported 記錄檔之虛擬機器群組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-135">GUID of the virtual machine group for which log files wereexported.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-136">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-136">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-139">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="8b0c2-139">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-140">包含錯誤摘要描述。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-140">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-141">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-141">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-144">匯出位置。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-144">Export Location.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-145">**ExportedConfigFilePaths**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-145">**ExportedConfigFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-146">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8b0c2-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-148">匯出之虛擬機器組態檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-148">Path of the exported virtual machine config file.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-149">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-149">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-150">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8b0c2-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-152">已匯出記錄檔之虛擬磁片的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-152">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-153">**ExportedGuestStateFilePaths**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-153">**ExportedGuestStateFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-154">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8b0c2-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-156">匯出的虛擬機器來賓狀態檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-156">Path of the exported virtual machine guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="8b0c2-157">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-157">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="8b0c2-158">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-158">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-159">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8b0c2-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-161">已匯出之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-161">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-162">**ExportedRuntimeFilePaths**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-162">**ExportedRuntimeFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-163">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8b0c2-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-165">匯出的虛擬機器執行時間狀態檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-165">Path of the exported virtual machine runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-166">**ReferencePointGroupId**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-166">**ReferencePointGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-169">匯出之集合參考點的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-169">GUID of the collection reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="8b0c2-170">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-170">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b0c2-171">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8b0c2-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b0c2-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8b0c2-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b0c2-173">已執行匯出作業之虛擬機器的 GUID。</span><span class="sxs-lookup"><span data-stu-id="8b0c2-173">GUID of the virtual machines for which export operation has been performed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b0c2-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b0c2-174">Requirements</span></span>



| <span data-ttu-id="8b0c2-175">需求</span><span class="sxs-lookup"><span data-stu-id="8b0c2-175">Requirement</span></span> | <span data-ttu-id="8b0c2-176">值</span><span class="sxs-lookup"><span data-stu-id="8b0c2-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0c2-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b0c2-177">Minimum supported client</span></span><br/> | <span data-ttu-id="8b0c2-178">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b0c2-178">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8b0c2-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b0c2-179">Minimum supported server</span></span><br/> | <span data-ttu-id="8b0c2-180">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8b0c2-180">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8b0c2-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="8b0c2-181">Namespace</span></span><br/>                | <span data-ttu-id="8b0c2-182">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b0c2-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8b0c2-183">MOF</span><span class="sxs-lookup"><span data-stu-id="8b0c2-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b0c2-184"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8b0c2-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b0c2-185">DLL</span><span class="sxs-lookup"><span data-stu-id="8b0c2-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b0c2-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b0c2-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b0c2-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b0c2-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b0c2-188">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="8b0c2-188">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

