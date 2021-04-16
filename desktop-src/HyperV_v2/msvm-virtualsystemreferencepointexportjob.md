---
description: 此類別代表虛擬系統參考點匯出作業工作。
ms.assetid: 3d8e117c-4863-441a-9264-c33f05fbc5ef
title: Msvm_VirtualSystemReferencePointExportJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob
- Msvm_VirtualSystemReferencePointExportJob.Cancellable
- Msvm_VirtualSystemReferencePointExportJob.ErrorSummaryDescription
- Msvm_VirtualSystemReferencePointExportJob.ExportDirectory
- Msvm_VirtualSystemReferencePointExportJob.VirtualMachineId
- Msvm_VirtualSystemReferencePointExportJob.ReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.BaseReferencePointId
- Msvm_VirtualSystemReferencePointExportJob.ExportedDisks
- Msvm_VirtualSystemReferencePointExportJob.ExportedLogFilePaths
- Msvm_VirtualSystemReferencePointExportJob.ExportedConfigFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedRuntimeFilePath
- Msvm_VirtualSystemReferencePointExportJob.ExportedGuestStateFilePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04b5d8f27efae4817062917541af9bb488cec32c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514296"
---
# <a name="msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="2f4bb-103">Msvm \_ VirtualSystemReferencePointExportJob 類別</span><span class="sxs-lookup"><span data-stu-id="2f4bb-103">Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="2f4bb-104">此類別代表虛擬系統參考點匯出作業工作。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-104">This class represents a virtual system reference point export operation job.</span></span>

<span data-ttu-id="2f4bb-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4bb-106">語法</span><span class="sxs-lookup"><span data-stu-id="2f4bb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointExportJob : CIM_ConcreteJob
{
  boolean Cancellable;
  string  ErrorSummaryDescription;
  string  ExportDirectory;
  string  VirtualMachineId;
  string  ReferencePointId;
  string  BaseReferencePointId;
  string  ExportedDisks[];
  string  ExportedLogFilePaths[];
  string  ExportedConfigFilePath;
  string  ExportedRuntimeFilePath;
  string  ExportedGuestStateFilePath;
};
```

## <a name="members"></a><span data-ttu-id="2f4bb-107">成員</span><span class="sxs-lookup"><span data-stu-id="2f4bb-107">Members</span></span>

<span data-ttu-id="2f4bb-108">**Msvm \_ VirtualSystemReferencePointExportJob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2f4bb-108">The **Msvm\_VirtualSystemReferencePointExportJob** class has these types of members:</span></span>

-   [<span data-ttu-id="2f4bb-109">方法</span><span class="sxs-lookup"><span data-stu-id="2f4bb-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f4bb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2f4bb-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f4bb-111">方法</span><span class="sxs-lookup"><span data-stu-id="2f4bb-111">Methods</span></span>

<span data-ttu-id="2f4bb-112">**Msvm \_ VirtualSystemReferencePointExportJob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-112">The **Msvm\_VirtualSystemReferencePointExportJob** class has these methods.</span></span>



| <span data-ttu-id="2f4bb-113">方法</span><span class="sxs-lookup"><span data-stu-id="2f4bb-113">Method</span></span>                                                                                     | <span data-ttu-id="2f4bb-114">描述</span><span class="sxs-lookup"><span data-stu-id="2f4bb-114">Description</span></span>                                        |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="2f4bb-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-115">**GetError**</span></span>](msvm-virtualsystemreferencepointexportjob-geterror.md)                     | <span data-ttu-id="2f4bb-116">捕獲錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-116">Retrieves the error.</span></span><br/>                    |
| [<span data-ttu-id="2f4bb-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-117">**GetErrorEx**</span></span>](msvm-virtualsystemreferencepointexportjob-geterrorex.md)                 | <span data-ttu-id="2f4bb-118">抓取其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-118">Retrieves additional error information.</span></span><br/> |
| [<span data-ttu-id="2f4bb-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-119">**RequestStateChange**</span></span>](msvm-virtualsystemreferencepointexportjob-requeststatechange.md) | <span data-ttu-id="2f4bb-120">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-120">Requests a state change.</span></span><br/>                |



 

### <a name="properties"></a><span data-ttu-id="2f4bb-121">屬性</span><span class="sxs-lookup"><span data-stu-id="2f4bb-121">Properties</span></span>

<span data-ttu-id="2f4bb-122">**Msvm \_ VirtualSystemReferencePointExportJob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-122">The **Msvm\_VirtualSystemReferencePointExportJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f4bb-123">**BaseReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-123">**BaseReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-126">在匯出作業中當做基底使用之參考點的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-126">GUID of the reference point which is used as the base in the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-127">**可取消**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-127">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-130">指出是否可以取消作業。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-130">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="2f4bb-131">這個屬性的值不保證取消作業的要求將會成功。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-131">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-132">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-132">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-135">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="2f4bb-135">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-136">包含錯誤摘要描述。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-136">Contains an error summary description.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-137">**ExportDirectory**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-137">**ExportDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-140">匯出位置。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-140">The export location.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-141">**ExportedConfigFilePath**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-141">**ExportedConfigFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-144">匯出設定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-144">Path of the exported config file.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-145">**ExportedDisks**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-145">**ExportedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-146">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f4bb-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-148">已匯出記錄檔之虛擬磁片的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-148">Instance IDs of virtual disks for which log files were exported.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-149">**ExportedGuestStateFilePath**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-149">**ExportedGuestStateFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-152">匯出的來賓狀態檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-152">Path of the exported guest state file.</span></span>

> [!Note]  
> <span data-ttu-id="2f4bb-153">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-153">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="2f4bb-154">**ExportedLogFilePaths**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-154">**ExportedLogFilePaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-155">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f4bb-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-157">已匯出之記錄檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-157">Paths of the log files which were exported.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-158">**ExportedRuntimeFilePath**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-158">**ExportedRuntimeFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-161">匯出之執行時間狀態檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-161">Path of the exported runtime state file.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-162">**ReferencePointId**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-162">**ReferencePointId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-165">匯出之參考點的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-165">GUID of the reference point which is exported.</span></span>

</dd> <dt>

<span data-ttu-id="2f4bb-166">**VirtualMachineId**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-166">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f4bb-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f4bb-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f4bb-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f4bb-169">已匯出記錄檔之虛擬機器的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2f4bb-169">GUID of the virtual machine for which log files were exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f4bb-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f4bb-170">Requirements</span></span>



| <span data-ttu-id="2f4bb-171">需求</span><span class="sxs-lookup"><span data-stu-id="2f4bb-171">Requirement</span></span> | <span data-ttu-id="2f4bb-172">值</span><span class="sxs-lookup"><span data-stu-id="2f4bb-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4bb-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f4bb-173">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4bb-174">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f4bb-174">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f4bb-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f4bb-175">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4bb-176">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2f4bb-176">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2f4bb-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f4bb-177">Namespace</span></span><br/>                | <span data-ttu-id="2f4bb-178">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f4bb-178">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2f4bb-179">MOF</span><span class="sxs-lookup"><span data-stu-id="2f4bb-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f4bb-180"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2f4bb-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f4bb-181">DLL</span><span class="sxs-lookup"><span data-stu-id="2f4bb-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f4bb-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f4bb-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f4bb-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f4bb-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4bb-184">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="2f4bb-184">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

