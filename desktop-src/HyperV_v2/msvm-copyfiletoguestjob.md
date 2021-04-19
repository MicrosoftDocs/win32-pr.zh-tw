---
description: 代表來賓檔案服務作業。
ms.assetid: 3750707e-e8c8-4188-aed8-1a394d142140
title: Msvm_CopyFileToGuestJob 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob
- Msvm_CopyFileToGuestJob.StartService
- Msvm_CopyFileToGuestJob.StopService
- Msvm_CopyFileToGuestJob.Caption
- Msvm_CopyFileToGuestJob.CreationClassName
- Msvm_CopyFileToGuestJob.Description
- Msvm_CopyFileToGuestJob.InstallDate
- Msvm_CopyFileToGuestJob.Name
- Msvm_CopyFileToGuestJob.Started
- Msvm_CopyFileToGuestJob.StartMode
- Msvm_CopyFileToGuestJob.Status
- Msvm_CopyFileToGuestJob.SystemCreationClassName
- Msvm_CopyFileToGuestJob.SystemName
- Msvm_CopyFileToGuestJob.CopyFileToGuestSettingData
- Msvm_CopyFileToGuestJob.Cancellable
- Msvm_CopyFileToGuestJob.ErrorSummaryDescription
- Msvm_CopyFileToGuestJob.VirtualSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57e27b4ba610eea4559f3b045b2d823661cf4cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990318"
---
# <a name="msvm_copyfiletoguestjob-class"></a><span data-ttu-id="956fc-103">Msvm \_ CopyFileToGuestJob 類別</span><span class="sxs-lookup"><span data-stu-id="956fc-103">Msvm\_CopyFileToGuestJob class</span></span>

<span data-ttu-id="956fc-104">代表來賓檔案服務作業。</span><span class="sxs-lookup"><span data-stu-id="956fc-104">Represents a guest file service operation job.</span></span> <span data-ttu-id="956fc-105">這個類別衍生自 [**Msvm \_ GuestFileService**](msvm-guestfileservice.md)。</span><span class="sxs-lookup"><span data-stu-id="956fc-105">This class derives from [**Msvm\_GuestFileService**](msvm-guestfileservice.md).</span></span>

<span data-ttu-id="956fc-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="956fc-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="956fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="956fc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CopyFileToGuestJob : CIM_ConcreteJob
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   CopyFileToGuestSettingData[];
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  string   VirtualSystemName;
};
```

## <a name="members"></a><span data-ttu-id="956fc-108">成員</span><span class="sxs-lookup"><span data-stu-id="956fc-108">Members</span></span>

<span data-ttu-id="956fc-109">**Msvm \_ CopyFileToGuestJob** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="956fc-109">The **Msvm\_CopyFileToGuestJob** class has these types of members:</span></span>

-   [<span data-ttu-id="956fc-110">方法</span><span class="sxs-lookup"><span data-stu-id="956fc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="956fc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="956fc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="956fc-112">方法</span><span class="sxs-lookup"><span data-stu-id="956fc-112">Methods</span></span>

<span data-ttu-id="956fc-113">**Msvm \_ CopyFileToGuestJob** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="956fc-113">The **Msvm\_CopyFileToGuestJob** class has these methods.</span></span>



| <span data-ttu-id="956fc-114">方法</span><span class="sxs-lookup"><span data-stu-id="956fc-114">Method</span></span>                                                                   | <span data-ttu-id="956fc-115">描述</span><span class="sxs-lookup"><span data-stu-id="956fc-115">Description</span></span>                                                           |
|:-------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="956fc-116">**CopyFilesToGuest**</span><span class="sxs-lookup"><span data-stu-id="956fc-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md)       | <span data-ttu-id="956fc-117">將檔案從 Hyper-v 主機複製到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="956fc-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> |
| [<span data-ttu-id="956fc-118">**GetError**</span><span class="sxs-lookup"><span data-stu-id="956fc-118">**GetError**</span></span>](geterror-msvm-copyfiletoguestjob.md)                     | <span data-ttu-id="956fc-119">捕獲作業的錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="956fc-119">Retrieves the error object for the job.</span></span><br/>                    |
| [<span data-ttu-id="956fc-120">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="956fc-120">**GetErrorEx**</span></span>](geterrorex-msvm-copyfiletoguestjob.md)                 | <span data-ttu-id="956fc-121">捕獲作業的錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="956fc-121">Retrieves the error objects for the job.</span></span><br/>                   |
| [<span data-ttu-id="956fc-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="956fc-122">**RequestStateChange**</span></span>](requeststatechange-msvm-copyfiletoguestjob.md) | <span data-ttu-id="956fc-123">變更作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="956fc-123">Changes the state of the job.</span></span><br/>                              |
| <span data-ttu-id="956fc-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="956fc-124">**StartService**</span></span>                                                         | <span data-ttu-id="956fc-125">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="956fc-125">This method is not supported.</span></span><br/>                              |
| <span data-ttu-id="956fc-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="956fc-126">**StopService**</span></span>                                                          | <span data-ttu-id="956fc-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="956fc-127">This method is not supported.</span></span><br/>                              |



 

### <a name="properties"></a><span data-ttu-id="956fc-128">屬性</span><span class="sxs-lookup"><span data-stu-id="956fc-128">Properties</span></span>

<span data-ttu-id="956fc-129">**Msvm \_ CopyFileToGuestJob** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="956fc-129">The **Msvm\_CopyFileToGuestJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="956fc-130">**可取消**</span><span class="sxs-lookup"><span data-stu-id="956fc-130">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-131">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="956fc-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-133">指出是否可以取消作業。</span><span class="sxs-lookup"><span data-stu-id="956fc-133">Indicates whether the job can be cancelled.</span></span> <span data-ttu-id="956fc-134">這個屬性的值不保證取消作業的要求將會成功。</span><span class="sxs-lookup"><span data-stu-id="956fc-134">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span> <span data-ttu-id="956fc-135">若 **為 TRUE**，則工作可以取消;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="956fc-135">If **TRUE**, the job can be cancelled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="956fc-136">**標題**</span><span class="sxs-lookup"><span data-stu-id="956fc-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-139">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="956fc-139">Short textual description of the object.</span></span> <span data-ttu-id="956fc-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="956fc-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="956fc-141">**CopyFileToGuestSettingData**</span><span class="sxs-lookup"><span data-stu-id="956fc-141">**CopyFileToGuestSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-142">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="956fc-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="956fc-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-144">設定用來複製檔案的資料。</span><span class="sxs-lookup"><span data-stu-id="956fc-144">Setting data that is used to copy a file.</span></span>

</dd> <dt>

<span data-ttu-id="956fc-145">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="956fc-145">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-148">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="956fc-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="956fc-149">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="956fc-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="956fc-150">**說明**</span><span class="sxs-lookup"><span data-stu-id="956fc-150">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-153">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="956fc-153">Textual description of the object.</span></span> <span data-ttu-id="956fc-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="956fc-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="956fc-155">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="956fc-155">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="956fc-158">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業**](cim-job.md)」。**ErrorCode**") </span><span class="sxs-lookup"><span data-stu-id="956fc-158">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="956fc-159">錯誤的摘要描述（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="956fc-159">A summary description of the error, if present.</span></span> <span data-ttu-id="956fc-160">這個屬性繼承自 [**CIM \_ 工作**](/windows/desktop/CIMWin32Prov/cim-job)。</span><span class="sxs-lookup"><span data-stu-id="956fc-160">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="956fc-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="956fc-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-162">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="956fc-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-164">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="956fc-164">Date and time the object was installed.</span></span> <span data-ttu-id="956fc-165">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="956fc-165">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="956fc-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="956fc-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="956fc-167">**名稱**</span><span class="sxs-lookup"><span data-stu-id="956fc-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-170">服務的唯一識別碼，也會提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="956fc-170">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="956fc-171">如需功能的詳細資訊，請參閱物件的 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="956fc-171">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="956fc-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="956fc-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="956fc-173">**已開始**</span><span class="sxs-lookup"><span data-stu-id="956fc-173">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-174">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="956fc-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-176">若 **為 TRUE**，表示服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="956fc-176">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="956fc-177">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="956fc-177">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-180">指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="956fc-180">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="956fc-181">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="956fc-181">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="956fc-182">**自動**</span><span class="sxs-lookup"><span data-stu-id="956fc-182">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="956fc-183">**》**</span><span class="sxs-lookup"><span data-stu-id="956fc-183">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="956fc-184">**狀態**</span><span class="sxs-lookup"><span data-stu-id="956fc-184">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-187">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="956fc-187">Current status of the object.</span></span> <span data-ttu-id="956fc-188">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="956fc-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="956fc-189">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="956fc-189">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="956fc-190">**正常**</span><span class="sxs-lookup"><span data-stu-id="956fc-190">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="956fc-191">**錯誤**</span><span class="sxs-lookup"><span data-stu-id="956fc-191">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="956fc-192">**降級**</span><span class="sxs-lookup"><span data-stu-id="956fc-192">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="956fc-193">**不明**</span><span class="sxs-lookup"><span data-stu-id="956fc-193">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="956fc-194">**「Pred 失敗」**</span><span class="sxs-lookup"><span data-stu-id="956fc-194">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="956fc-195">**入門**</span><span class="sxs-lookup"><span data-stu-id="956fc-195">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="956fc-196">**從而**</span><span class="sxs-lookup"><span data-stu-id="956fc-196">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="956fc-197">**維護**</span><span class="sxs-lookup"><span data-stu-id="956fc-197">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="956fc-198">**強調**</span><span class="sxs-lookup"><span data-stu-id="956fc-198">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="956fc-199">**"NonRecover"**</span><span class="sxs-lookup"><span data-stu-id="956fc-199">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="956fc-200">**「無連絡人」**</span><span class="sxs-lookup"><span data-stu-id="956fc-200">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="956fc-201">**「遺失通訊」**</span><span class="sxs-lookup"><span data-stu-id="956fc-201">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="956fc-202">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="956fc-202">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-205">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="956fc-205">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="956fc-206">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="956fc-206">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-209">裝載服務的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="956fc-209">Name of the system that hosts the service.</span></span>

</dd> <dt>

<span data-ttu-id="956fc-210">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="956fc-210">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="956fc-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="956fc-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="956fc-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="956fc-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="956fc-213">受影響之虛擬系統的 GUID。</span><span class="sxs-lookup"><span data-stu-id="956fc-213">GUID of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="956fc-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="956fc-214">Requirements</span></span>



| <span data-ttu-id="956fc-215">需求</span><span class="sxs-lookup"><span data-stu-id="956fc-215">Requirement</span></span> | <span data-ttu-id="956fc-216">值</span><span class="sxs-lookup"><span data-stu-id="956fc-216">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="956fc-217">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="956fc-217">Minimum supported client</span></span><br/> | <span data-ttu-id="956fc-218">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="956fc-218">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="956fc-219">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="956fc-219">Minimum supported server</span></span><br/> | <span data-ttu-id="956fc-220">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="956fc-220">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="956fc-221">命名空間</span><span class="sxs-lookup"><span data-stu-id="956fc-221">Namespace</span></span><br/>                | <span data-ttu-id="956fc-222">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="956fc-222">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="956fc-223">MOF</span><span class="sxs-lookup"><span data-stu-id="956fc-223">MOF</span></span><br/>                      | <dl> <span data-ttu-id="956fc-224"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="956fc-224"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="956fc-225">DLL</span><span class="sxs-lookup"><span data-stu-id="956fc-225">DLL</span></span><br/>                      | <dl> <span data-ttu-id="956fc-226"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="956fc-226"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="956fc-227">另請參閱</span><span class="sxs-lookup"><span data-stu-id="956fc-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="956fc-228">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="956fc-228">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

[<span data-ttu-id="956fc-229">**Msvm \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="956fc-229">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> <dt>

[<span data-ttu-id="956fc-230">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="956fc-230">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

