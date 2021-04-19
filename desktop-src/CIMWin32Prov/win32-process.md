---
Description: Win32 \_ 進程&\# 32;WMI 類別代表作業系統上的進程。
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Win32_Process 類別
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999205"
---
# <a name="win32_process-class"></a><span data-ttu-id="9ae0f-103">Win32 \_ 進程類別</span><span class="sxs-lookup"><span data-stu-id="9ae0f-103">Win32\_Process class</span></span>

<span data-ttu-id="9ae0f-104">**Win32 \_ 進程** [WMI 類別](../wmisdk/retrieving-a-class.md)代表作業系統上的進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="9ae0f-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="9ae0f-106">如需 Windows 內進程和執行緒的一般討論，請參閱「程式 [和執行緒](/ProcThread/processes-and-threads.md)」主題。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae0f-107">語法</span><span class="sxs-lookup"><span data-stu-id="9ae0f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="9ae0f-108">成員</span><span class="sxs-lookup"><span data-stu-id="9ae0f-108">Members</span></span>

<span data-ttu-id="9ae0f-109">**Win32 \_ 進程** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9ae0f-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="9ae0f-110">方法</span><span class="sxs-lookup"><span data-stu-id="9ae0f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ae0f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae0f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ae0f-112">方法</span><span class="sxs-lookup"><span data-stu-id="9ae0f-112">Methods</span></span>

<span data-ttu-id="9ae0f-113">**Win32 \_ 進程** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="9ae0f-114">方法</span><span class="sxs-lookup"><span data-stu-id="9ae0f-114">Method</span></span>                                                                   | <span data-ttu-id="9ae0f-115">描述</span><span class="sxs-lookup"><span data-stu-id="9ae0f-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ae0f-116">**AttachDebugger**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="9ae0f-117">啟動處理常式目前註冊的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="9ae0f-118">**建立**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="9ae0f-119">建立新的進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9ae0f-120">**GetAvailableVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="9ae0f-121">抓取進程可用之可用虛擬位址空間的目前大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="9ae0f-122">**Windows server 2012、Windows 8、windows 7、Windows server 2008 和 Windows Vista：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="9ae0f-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="9ae0f-124">抓取進程執行時所使用的使用者名稱和功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="9ae0f-125">**GetOwnerSid**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="9ae0f-126">抓取進程擁有者 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="9ae0f-127">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="9ae0f-128">變更進程的執行優先權。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="9ae0f-129">**終止**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="9ae0f-130">終止進程及其所有線程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="9ae0f-131">屬性</span><span class="sxs-lookup"><span data-stu-id="9ae0f-131">Properties</span></span>

<span data-ttu-id="9ae0f-132">**Win32 \_ 進程** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ae0f-133">**標題**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-136">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-137">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="9ae0f-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-142">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "命令列以啟動進程" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-143">用來啟動特定進程的命令列（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-144">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-147">限定詞： [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-148">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9ae0f-149">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9ae0f-150">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-152">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-154">限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "CreationDate" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-155">進程開始執行的日期。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-155">Date the process begins executing.</span></span>

<span data-ttu-id="9ae0f-156">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-157">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-160">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CSCreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 電腦系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-161">範圍電腦系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="9ae0f-162">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-166">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CSName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-167">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="9ae0f-168">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-169">**說明**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-172">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-173">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-173">Description of an object.</span></span>

<span data-ttu-id="9ae0f-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-175">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-178">限定詞：[**許可權**](../wmisdk/standard-wmi-qualifiers.md) ( "SeDebugPrivilege" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Tool 說明結構 \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| SzExePath" ) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "可執行檔路徑" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-179">進程可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="9ae0f-180">範例： "C： \\ Windows \\ System \\Explorer.Exe"</span><span class="sxs-lookup"><span data-stu-id="9ae0f-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-184">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「執行狀態」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-185">進程目前的操作狀況。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-185">Current operating condition of the process.</span></span>

<span data-ttu-id="9ae0f-186">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ae0f-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9ae0f-188">Unknown</span><span class="sxs-lookup"><span data-stu-id="9ae0f-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ae0f-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ae0f-190">其他</span><span class="sxs-lookup"><span data-stu-id="9ae0f-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="9ae0f-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**就緒** (2) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9ae0f-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="9ae0f-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**封鎖** (4) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9ae0f-194">封鎖</span><span class="sxs-lookup"><span data-stu-id="9ae0f-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="9ae0f-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**擱置** 的已封鎖 (5) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="9ae0f-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>已 **暫止就緒** (6) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="9ae0f-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**終止** (7) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="9ae0f-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (8) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="9ae0f-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span> (9) **成長**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ae0f-200">**Handle**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-203">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Handle" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-204">處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-204">Process identifier.</span></span>

<span data-ttu-id="9ae0f-205">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-207">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-209">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程狀態 \| 系統 \_ 進程 \_ 資訊 \| HandleCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「控制碼計數」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-210">進程所擁有的開啟控制碼總數。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="9ae0f-211">**HandleCount** 是此進程中，每個執行緒目前開啟之控制碼的總和。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="9ae0f-212">控制碼可用來檢查或修改系統資源。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="9ae0f-213">每個控制碼在內部維護的資料表中都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="9ae0f-214">專案包含用來識別資源類型的資源和資料位址。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-216">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-218">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-219">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-219">Date an object is installed.</span></span> <span data-ttu-id="9ae0f-220">可能會在沒有將值寫入這個屬性的情況下安裝物件。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="9ae0f-221">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-222">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-223">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-225">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "KernelModeTime" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-226">核心模式中的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="9ae0f-227">如果無法使用這項資訊，請使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="9ae0f-228">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-229">**MaximumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-230">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-232">限定詞： [**許可權**](../wmisdk/standard-wmi-qualifiers.md) ( "SeDebugPrivilege" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \| WINNT。H \| 配額 \_ 限制 \| MaximumWorkingSetSize ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 工作集大小上限 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-233">進程的工作集大小上限。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-233">Maximum working set size of the process.</span></span> <span data-ttu-id="9ae0f-234">處理常式的工作集是實體 RAM 中處理常式可見的記憶體頁面集。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="9ae0f-235">這些頁面是常駐的，可供應用程式使用，而不會觸發分頁錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="9ae0f-236">範例：1413120</span><span class="sxs-lookup"><span data-stu-id="9ae0f-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-237">**MinimumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-238">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-240">限定詞： [**許可權**](../wmisdk/standard-wmi-qualifiers.md) ( "SeDebugPrivilege" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32 \| WINNT。H \| 配額 \_ 限制 \| MinimumWorkingSetSize ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 工作集大小下限 ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-241">進程的工作集大小下限。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-241">Minimum working set size of the process.</span></span> <span data-ttu-id="9ae0f-242">處理常式的工作集是實體 RAM 中處理常式可見的記憶體頁面集。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="9ae0f-243">這些頁面是常駐的，可供應用程式使用，而不會觸發分頁錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="9ae0f-244">範例：20480</span><span class="sxs-lookup"><span data-stu-id="9ae0f-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-245">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-248">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-249">負責處理常式的可執行檔名稱，相當於工作管理員中的 [映射名稱] 屬性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="9ae0f-250">當子類別繼承時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="9ae0f-251">名稱會硬式編碼為應用程式本身，而不會受到變更的檔案名影響。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="9ae0f-252">例如，即使您將 Calc.exe 重新命名，Calc.exe 的名稱仍會出現在工作管理員以及任何可取出進程名稱的 WMI 腳本中。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="9ae0f-253">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-254">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-257">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CreationClassName**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 作業系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-258">範圍作業系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="9ae0f-259">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-263">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**Name**") ， [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 作業系統 Name ") </span><span class="sxs-lookup"><span data-stu-id="9ae0f-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-264">範圍作業系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="9ae0f-265">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-266">**OtherOperationCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-267">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-269">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| OtherOperationCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「其他作業計數」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-270">未讀取或寫入作業所執行的 i/o 作業數目。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="9ae0f-271">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-272">**OtherTransferCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-273">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-275">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| OtherTransferCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「其他傳輸計數」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-276">作業期間在非讀取或寫入作業期間傳輸的資料量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="9ae0f-277">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-278">**PageFaults**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-279">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-281">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PageFaultCount" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「分頁錯誤數」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-282">進程產生的分頁錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="9ae0f-283">範例：10</span><span class="sxs-lookup"><span data-stu-id="9ae0f-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-284">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-287">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程狀態 \| 系統 \_ 進程 \_ 資訊 \| PagefileUsage」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「分頁檔案使用方式」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-288">進程目前正在使用的分頁檔案空間量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="9ae0f-289">此值與 TaskMgr.exe 中的 **VMSize** 值一致。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="9ae0f-290">範例：102435</span><span class="sxs-lookup"><span data-stu-id="9ae0f-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-291">**ParentProcessId**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-292">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-294">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| InheritedFromUniqueProcessId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "上層處理序識別碼" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-295">建立進程之進程的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="9ae0f-296">系統會重複使用處理序識別碼，因此它們只會在該進程的存留期內找出處理常式。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="9ae0f-297">**ParentProcessId** 所識別的進程可能會終止，因此 **ParentProcessId** 可能不會參考執行中的進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="9ae0f-298">**ParentProcessId** 也可能不正確地參考重複使用處理序識別碼的進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="9ae0f-299">您可以使用 **CreationDate** 屬性來判斷指定的父系是否在建立此 **Win32 \_ 進程** 實例所表示的進程之後建立。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-300">**PeakPageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-301">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-303">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PeakPagefileUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰分頁檔案使用方式」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-304">進程存留期間使用的分頁檔空間數量上限。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="9ae0f-305">範例：102367</span><span class="sxs-lookup"><span data-stu-id="9ae0f-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-306">**PeakVirtualSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-307">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-309">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PeakVirtualSize" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "尖峰虛擬位址空間使用量" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-310">進程一次使用的虛擬位址空間上限。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="9ae0f-311">使用虛擬位址空間不一定表示對應使用的是磁片或主儲存體頁面。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="9ae0f-312">不過，虛擬空間是有限的，而且使用太多進程可能無法載入程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="9ae0f-313">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-314">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-315">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-317">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PeakWorkingSetSize" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰工作集大小」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-318">進程的尖峰工作集大小。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-318">Peak working set size of a process.</span></span>

<span data-ttu-id="9ae0f-319">範例：1413120</span><span class="sxs-lookup"><span data-stu-id="9ae0f-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-320">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-321">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-323">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "priority" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| 根據 basepriority" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Priority" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-324">排程作業系統內進程的優先順序。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="9ae0f-325">值愈高，進程所收到的優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="9ae0f-326">優先權值的範圍可以從 0 (零) ，也就是最高優先順序的最低優先順序為31。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="9ae0f-327">範例：7</span><span class="sxs-lookup"><span data-stu-id="9ae0f-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-328">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-329">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-331">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| PrivatePageCount" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Private Page Count" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-332">目前配置的頁面數目只能供這個 **Win32 \_ 進程** 實例所代表的進程存取。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="9ae0f-333">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-334">**進程**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-337">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| [**處理 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「處理序識別碼」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-338">用來區別某個進程與另一個進程的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="9ae0f-339">ProcessIDs 從處理常式建立到處理終止都有效。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="9ae0f-340">終止時，可以將相同的數值識別碼套用至新的進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="9ae0f-341">這表示您無法單獨使用 ProcessID 來監視特定的進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="9ae0f-342">例如，應用程式的 ProcessID 可能是7，然後失敗。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="9ae0f-343">當新的進程啟動時，可能會將新的進程指派給 ProcessID 7。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="9ae0f-344">只針對指定的 ProcessID 檢查的腳本，因此可以「愚弄」，以為原始應用程式仍在執行中。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-345">**QuotaNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-346">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-348">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaNonPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「非分頁集區使用量配額」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-349">進程的非分頁集區使用量配額量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="9ae0f-350">範例：15</span><span class="sxs-lookup"><span data-stu-id="9ae0f-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-351">**QuotaPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-352">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-354">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "分頁集區使用量配額" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-355">進程的分頁集區使用量配額量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="9ae0f-356">範例：22</span><span class="sxs-lookup"><span data-stu-id="9ae0f-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-357">**QuotaPeakNonPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-358">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-360">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaPeakNonPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰非分頁集區使用量配額」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-361">進程的非分頁集區使用量的尖峰配額量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="9ae0f-362">範例：31</span><span class="sxs-lookup"><span data-stu-id="9ae0f-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-363">**QuotaPeakPagedPoolUsage**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-364">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-366">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| QuotaPeakPagedPoolUsage" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「尖峰分頁集區使用量配額」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-367">進程之分頁集區使用量的尖峰配額量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="9ae0f-368">範例：31</span><span class="sxs-lookup"><span data-stu-id="9ae0f-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-369">**ReadOperationCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-370">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-372">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| ReadOperationCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「讀取作業計數」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-373">執行的讀取作業數。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-373">Number of read operations performed.</span></span>

<span data-ttu-id="9ae0f-374">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-375">**ReadTransferCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-376">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-378">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| ReadTransferCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「讀取傳輸計數」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-379">讀取的資料量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-379">Amount of data read.</span></span>

<span data-ttu-id="9ae0f-380">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-382">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-384">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| SessionId" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Session Id" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-385">當建立會話時，作業系統所產生的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="9ae0f-386">會話會在一段時間內進行登入，直到從特定系統登出為止。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-387">**狀態**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-390">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-391">這個屬性不會執行，也不會填入這個類別的任何實例。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="9ae0f-392">一律為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-392">It is always **NULL**.</span></span>

<span data-ttu-id="9ae0f-393">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9ae0f-394">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="9ae0f-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9ae0f-395">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9ae0f-396">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ae0f-397">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ae0f-398">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9ae0f-399">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9ae0f-400">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9ae0f-401">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9ae0f-402">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9ae0f-403">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9ae0f-404">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9ae0f-405">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9ae0f-406">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ae0f-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-408">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-410">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "終止日期" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-411">進程已停止或終止。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-411">Process was stopped or terminated.</span></span> <span data-ttu-id="9ae0f-412">若要取得終止時間，處理常式的控制碼必須保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="9ae0f-413">否則，此屬性會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="9ae0f-414">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-415">**ThreadCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-416">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-418">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| NumberOfThreads" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Thread Count" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-419">進程中的作用中線程數目。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-419">Number of active threads in a process.</span></span> <span data-ttu-id="9ae0f-420">指令是處理器中的基本執行單位，而執行緒是執行指令的物件。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="9ae0f-421">每個執行中的進程至少都有一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-422">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-423">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-425">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "UserModeTime" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-426">使用者模式中的時間，以100的毫微秒數單位表示。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="9ae0f-427">如果無法使用這項資訊，請使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="9ae0f-428">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-429">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-430">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-432">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Process Status \| SYSTEM \_ process \_ INFORMATION \| VirtualSize" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「虛擬位址空間使用量」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「bytes」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-433">進程正在使用的虛擬位址空間目前的大小，而不是處理常式實際使用的實體或虛擬記憶體。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="9ae0f-434">使用虛擬位址空間不一定表示對應使用的是磁片或主儲存體頁面。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="9ae0f-435">虛擬空間有限，且使用太多，進程可能無法載入程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="9ae0f-436">此值與您在 Perfmon.exe 中看到的值一致。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="9ae0f-437">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-441">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 進程和執行緒函式 \| GetProcessVersion" ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Windows Version" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-442">進程執行所在的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="9ae0f-443">範例：4。0</span><span class="sxs-lookup"><span data-stu-id="9ae0f-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-444">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-445">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-447">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "工作集大小" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-448">進程需要有效率地執行的記憶體數量（以位元組為單位），適用于使用以頁面為基礎的記憶體管理的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="9ae0f-449">如果系統沒有足夠的記憶體 (小於) 的工作集大小，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="9ae0f-450">如果工作集的大小不是已知的，請使用 **Null** 或 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="9ae0f-451">如果提供了工作集資料，您可以監視資訊，以瞭解進程的變更記憶體需求。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="9ae0f-452">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="9ae0f-453">這個屬性繼承自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-454">**WriteOperationCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-455">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-457">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| WriteOperationCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「寫入作業計數」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-458">執行的寫入作業數目。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-458">Number of write operations performed.</span></span>

<span data-ttu-id="9ae0f-459">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ae0f-460">**WriteTransferCount**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ae0f-461">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-462">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ae0f-463">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 進程和執行緒結構 \| 系統 \_ 進程 \_ 資訊 \| WriteTransferCount」 ) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( 「寫入傳輸計數」 ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) </span><span class="sxs-lookup"><span data-stu-id="9ae0f-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ae0f-464">寫入的資料量。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-464">Amount of data written.</span></span>

<span data-ttu-id="9ae0f-465">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ae0f-466">備註</span><span class="sxs-lookup"><span data-stu-id="9ae0f-466">Remarks</span></span>

<span data-ttu-id="9ae0f-467">**Win32 \_ 進程** 類別衍生自 [**CIM \_ 進程**](cim-process.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="9ae0f-468">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="9ae0f-469">如需詳細資訊，請參閱 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="9ae0f-470">概觀</span><span class="sxs-lookup"><span data-stu-id="9ae0f-470">Overview</span></span>

<span data-ttu-id="9ae0f-471">進程幾乎是在電腦上執行的所有作業。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="9ae0f-472">事實上，大部分電腦問題的根本原因可以追蹤至進程;例如，電腦上可能正在執行太多進程 (並且爭用一組有限的資源) ，或單一進程可能使用的資源超過其共用。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="9ae0f-473">這些因素對於在電腦上執行的進程保持密切監看是很重要的。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="9ae0f-474">進程監視是程式管理中的主要活動，可讓您判斷電腦的實際功能、電腦執行的應用程式，以及這些應用程式在運算環境中的變更如何受到影響。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="9ae0f-475">監視進程</span><span class="sxs-lookup"><span data-stu-id="9ae0f-475">Monitoring a Process</span></span>

<span data-ttu-id="9ae0f-476">定期監視程式可協助您確保電腦以尖峰效率執行，而且會如預期般執行其已分配的工作。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="9ae0f-477">例如，藉由監視程式，您可以立即通知任何已停止回應的應用程式，然後採取步驟來結束該進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="9ae0f-478">此外，進程監視還可讓您在問題發生之前加以識別。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="9ae0f-479">例如，藉由重複檢查進程所使用的記憶體數量，您可以找出記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="9ae0f-480">然後，您可以在不當應用程式使用所有可用的記憶體之前停止進程，並讓電腦停止運作。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="9ae0f-481">程式監視也有助於將計畫中斷進行升級和維護所造成的中斷情況降到最低。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="9ae0f-482">例如，藉由檢查用戶端電腦上執行之資料庫應用程式的狀態，您可以判斷讓資料庫離線以升級軟體的影響。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="9ae0f-483">監視進程的可用性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-483">Monitoring process availability.</span></span> <span data-ttu-id="9ae0f-484">測量進程可用的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="9ae0f-485">可用性通常是使用簡單探查來監視，它會報告進程是否仍在執行中。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="9ae0f-486">藉由追蹤每個探查的結果，您可以計算進程的可用性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="9ae0f-487">例如，在這種情況下，會探查100次並回應95的進程，其可用性為95%。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="9ae0f-488">這種類型的監視通常會保留給資料庫、郵件程式，以及預期會在任何時間執行的其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="9ae0f-489">這不適用於每日定期啟動和停止的文字處理程式、試算表或其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="9ae0f-490">您可以建立 [**Win32 \_ ProcessStartup**](win32-processstartup.md) 類別的實例來設定處理常式。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="9ae0f-491">您可以使用 [**Win32 \_ PerfFormattedData \_ perfproc.dll \_ process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) 類別和 WMI 重新整理程式物件（例如 [**SWbemRefresher**](../wmisdk/swbemrefresher.md)）來監視流程效能。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="9ae0f-492">如需詳細資訊，請參閱 [監視效能資料](../wmisdk/monitoring-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ae0f-493">範例</span><span class="sxs-lookup"><span data-stu-id="9ae0f-493">Examples</span></span>

<span data-ttu-id="9ae0f-494">TechNet 元件庫上 [WMI 類別](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell 程式碼範例的內容清單說明 **Win32 \_ Process** 類別，並以 Excel 格式輸出結果。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="9ae0f-495">在 [多部伺服器上終止](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) 執行的進程會終止在單一或多部電腦上執行的處理常式。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="9ae0f-496">在 [範例中：呼叫提供者方法](../wmisdk/example--calling-a-provider-method.md) 主題時，程式碼會使用 c + + 呼叫 **Win32 \_ 進程** 來建立進程。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="9ae0f-497">可用性是最簡單的程式監視形式：使用此方法時，您只需確定進程正在執行中。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="9ae0f-498">當您監視程式可用性時，通常會取出電腦上執行的處理常式清單，然後確認特定進程是否仍在作用中。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="9ae0f-499">如果進程在使用中，則會被視為可用。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="9ae0f-500">如果進程不在使用中，則無法使用。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="9ae0f-501">下列 VBScript 範例會藉由檢查電腦上執行的處理常式清單，並在找不到 Database.exe 進程時發出通知，來監視進程的可用性。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="9ae0f-502">下列 VBScript 範例會使用暫存事件取用者來監視進程建立。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="9ae0f-503">下列 VBScript 會監視進程效能資訊。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="9ae0f-504">下列 VBScript 程式碼範例顯示如何取得本機電腦上每個處理常式的擁有者。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="9ae0f-505">您可以使用此腳本從遠端電腦取得資料，例如，若要判斷哪些使用者有執行終端機伺服器的處理常式，請在第一行以 "." 取代遠端電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="9ae0f-506">您也必須是遠端電腦上的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="9ae0f-507">下列 VBScript 程式碼範例示範如何取得與執行中進程相關聯的登入會話。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="9ae0f-508">處理常式必須在腳本啟動之前 Notepad.exe 執行。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="9ae0f-509">此範例會尋找與代表 Notepad.exe 的 **win32 \_ 進程** 相關聯的 [**win32 \_ LogonSession**](win32-logonsession.md)實例。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="9ae0f-510">[**Win32 \_SessionProcess**](win32-sessionprocess.md) 會指定為 association 類別。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="9ae0f-511">如需詳細資訊，請參閱 [語句的 associators of](../wmisdk/associators-of-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="9ae0f-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="9ae0f-512">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ae0f-512">Requirements</span></span>



| <span data-ttu-id="9ae0f-513">需求</span><span class="sxs-lookup"><span data-stu-id="9ae0f-513">Requirement</span></span> | <span data-ttu-id="9ae0f-514">值</span><span class="sxs-lookup"><span data-stu-id="9ae0f-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae0f-515">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ae0f-515">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae0f-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ae0f-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ae0f-517">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ae0f-517">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae0f-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ae0f-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ae0f-519">命名空間</span><span class="sxs-lookup"><span data-stu-id="9ae0f-519">Namespace</span></span><br/>                | <span data-ttu-id="9ae0f-520">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9ae0f-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ae0f-521">MOF</span><span class="sxs-lookup"><span data-stu-id="9ae0f-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ae0f-522"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ae0f-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ae0f-523">DLL</span><span class="sxs-lookup"><span data-stu-id="9ae0f-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ae0f-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ae0f-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae0f-525">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ae0f-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae0f-526">**CIM \_ 進程**</span><span class="sxs-lookup"><span data-stu-id="9ae0f-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="9ae0f-527">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="9ae0f-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="9ae0f-528">WMI 工作：進程</span><span class="sxs-lookup"><span data-stu-id="9ae0f-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
