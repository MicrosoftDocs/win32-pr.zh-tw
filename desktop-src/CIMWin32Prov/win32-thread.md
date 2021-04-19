---
description: Win32 \_ 執行緒&\# 8194;WMI 類別代表執行的執行緒。
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Win32_Thread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997475"
---
# <a name="win32_thread-class"></a><span data-ttu-id="e7727-103">Win32 \_ 執行緒類別</span><span class="sxs-lookup"><span data-stu-id="e7727-103">Win32\_Thread class</span></span>

<span data-ttu-id="e7727-104">**Win32 \_ 執行緒** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e7727-104">The **Win32\_Thread** [WMI class](../wmisdk/retrieving-a-class.md) represents a thread of execution.</span></span> <span data-ttu-id="e7727-105">雖然進程必須有一個執行中的執行緒，但是進程可以建立其他執行緒，以平行方式執行工作。</span><span class="sxs-lookup"><span data-stu-id="e7727-105">While a process must have one thread of execution, the process can create other threads to execute tasks in parallel.</span></span> <span data-ttu-id="e7727-106">執行緒共用進程環境，因此同一個進程下的多個執行緒所使用的記憶體會比相同數目的進程更少。</span><span class="sxs-lookup"><span data-stu-id="e7727-106">Threads share the process environment, thus multiple threads under the same process use less memory than the same number of processes.</span></span>

<span data-ttu-id="e7727-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e7727-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e7727-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="e7727-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7727-109">語法</span><span class="sxs-lookup"><span data-stu-id="e7727-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="e7727-110">成員</span><span class="sxs-lookup"><span data-stu-id="e7727-110">Members</span></span>

<span data-ttu-id="e7727-111">**Win32 \_ 執行緒** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e7727-111">The **Win32\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="e7727-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e7727-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7727-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e7727-113">Properties</span></span>

<span data-ttu-id="e7727-114">**Win32 \_ 執行緒** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e7727-114">The **Win32\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7727-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="e7727-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-118">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-119">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e7727-119">Short description of the object.</span></span>

<span data-ttu-id="e7727-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e7727-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-124">限定詞： [**Cim \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e7727-124">Qualifiers: [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7727-125">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="e7727-125">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e7727-126">搭配類別的其他索引鍵屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e7727-126">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e7727-127">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-127">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-128">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e7727-128">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-131">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**CSCreationClassName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e7727-131">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7727-132">範圍電腦系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e7727-132">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="e7727-133">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-133">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="e7727-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-137">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**CSName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e7727-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7727-138">範圍電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7727-138">Name of the scoping computer system.</span></span>

<span data-ttu-id="e7727-139">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-139">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-140">**說明**</span><span class="sxs-lookup"><span data-stu-id="e7727-140">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-143">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-143">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-144">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e7727-144">Description of the object.</span></span>

<span data-ttu-id="e7727-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-146">**經過時間**</span><span class="sxs-lookup"><span data-stu-id="e7727-146">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-147">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e7727-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-149">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Performance Data 結構 Performance \| [**\_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-150">自建立之後，提供給這個執行緒的總執行時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e7727-150">Total execution time, in milliseconds, given to this thread since its creation.</span></span>

<span data-ttu-id="e7727-151">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-151">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-152">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="e7727-152">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e7727-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7727-155">執行緒的目前操作狀況。</span><span class="sxs-lookup"><span data-stu-id="e7727-155">Current operating condition of the thread.</span></span>

<span data-ttu-id="e7727-156">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-156">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7727-157">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e7727-157">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e7727-158">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e7727-158">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="e7727-159">**就緒** (2) </span><span class="sxs-lookup"><span data-stu-id="e7727-159">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="e7727-160">**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="e7727-160">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="e7727-161">**封鎖** (4) </span><span class="sxs-lookup"><span data-stu-id="e7727-161">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="e7727-162">**擱置** 的已封鎖 (5) </span><span class="sxs-lookup"><span data-stu-id="e7727-162">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="e7727-163">已 **暫止就緒** (6) </span><span class="sxs-lookup"><span data-stu-id="e7727-163">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7727-164">**Handle**</span><span class="sxs-lookup"><span data-stu-id="e7727-164">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-167">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ，覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Handle" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Tool Help 結構 \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-167">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32ThreadID")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-168">執行緒的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e7727-168">Handle to a thread.</span></span> <span data-ttu-id="e7727-169">控制碼預設具有完整存取權限。</span><span class="sxs-lookup"><span data-stu-id="e7727-169">The handle has full access rights by default.</span></span> <span data-ttu-id="e7727-170">使用正確的安全性存取時，控制碼可用於接受執行緒控制碼的任何函數。</span><span class="sxs-lookup"><span data-stu-id="e7727-170">With the correct security access, the handle can be used in any function that accepts a thread handle.</span></span> <span data-ttu-id="e7727-171">根據建立時所指定的繼承旗標，這個控制碼可由子進程繼承。</span><span class="sxs-lookup"><span data-stu-id="e7727-171">Depending on the inheritance flag specified when it is created, this handle can be inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="e7727-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e7727-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-173">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e7727-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-175">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e7727-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-176">已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e7727-176">Object was installed.</span></span> <span data-ttu-id="e7727-177">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e7727-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e7727-178">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-179">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="e7727-179">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-180">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e7727-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-182">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "KernelModeTime" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 效能資料結構效能 \| [**\_ 物件 \_ 類型**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-182">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-183">在核心模式中的時間，以100毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="e7727-183">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="e7727-184">如果無法使用這項資訊，則應使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="e7727-184">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="e7727-185">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-186">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e7727-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-189">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-189">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-190">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e7727-190">Label by which the object is known.</span></span> <span data-ttu-id="e7727-191">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e7727-191">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e7727-192">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-193">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e7727-193">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-196">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**OSCreationClassName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e7727-196">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7727-197">範圍作業系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="e7727-197">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="e7727-198">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-198">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-199">**OSName**</span><span class="sxs-lookup"><span data-stu-id="e7727-199">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-202">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**OSName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e7727-202">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7727-203">範圍作業系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7727-203">Name of the scoping operating system.</span></span>

<span data-ttu-id="e7727-204">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-204">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-205">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="e7727-205">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-206">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7727-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-208">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Priority" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Tool Help 結構 \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-208">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|tpDeltaPri")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-209">執行緒的動態優先權。</span><span class="sxs-lookup"><span data-stu-id="e7727-209">Dynamic priority of the thread.</span></span> <span data-ttu-id="e7727-210">每個執行緒都有動態優先權，讓排程器用來判斷要執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e7727-210">Each thread has a dynamic priority that the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="e7727-211">一開始，執行緒的動態優先權與其基底優先權相同。</span><span class="sxs-lookup"><span data-stu-id="e7727-211">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="e7727-212">系統可以提高和降低動態優先順序，以確保它的回應速度 (保證不會耗盡處理器時間) 的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e7727-212">The system can raise and lower the dynamic priority, to ensure that it is responsive (guaranteeing that no threads are starved for processor time).</span></span> <span data-ttu-id="e7727-213">系統不會提高基底優先權層級介於16到31之間的執行緒優先順序。</span><span class="sxs-lookup"><span data-stu-id="e7727-213">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="e7727-214">只有基底優先順序介於0和15之間的執行緒才能獲得動態優先權。</span><span class="sxs-lookup"><span data-stu-id="e7727-214">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span> <span data-ttu-id="e7727-215">數位愈高表示優先順序較高。</span><span class="sxs-lookup"><span data-stu-id="e7727-215">Higher numbers indicate higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="e7727-216">**PriorityBase**</span><span class="sxs-lookup"><span data-stu-id="e7727-216">**PriorityBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-217">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7727-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-219">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Performance Data 結構 Performance \| [**\_ OBJECT \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|PerfPriorityBase")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-220">執行緒的目前基本優先權。</span><span class="sxs-lookup"><span data-stu-id="e7727-220">Current base priority of a thread.</span></span> <span data-ttu-id="e7727-221">如果執行緒正在處理使用者輸入，作業系統可能會將執行緒的動態優先順序提高到基底優先順序以上，如果執行緒變成計算系結，則會將它降低到基底優先順序。</span><span class="sxs-lookup"><span data-stu-id="e7727-221">The operating system may raise the thread's dynamic priority above the base priority if the thread is handling user input, or lower it toward the base priority if the thread becomes compute-bound.</span></span> <span data-ttu-id="e7727-222">**PriorityBase** 屬性可以有0到31之間的值。</span><span class="sxs-lookup"><span data-stu-id="e7727-222">The **PriorityBase** property can have a value between 0 and 31.</span></span>

</dd> <dt>

<span data-ttu-id="e7727-223">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e7727-223">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-226">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**CreationClassName**") ， [**Cim \_ Key**](../wmisdk/standard-wmi-qualifiers.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="e7727-226">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e7727-227">範圍處理常式 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e7727-227">Value of the scoping process **CreationClassName** property.</span></span>

<span data-ttu-id="e7727-228">這個屬性繼承自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-228">This property is inherited from [**CIM\_Thread**](cim-thread.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7727-229">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="e7727-229">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-232">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ，覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "ProcessHandle" ) ，[**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 進程**](cim-process.md)」。**處理**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" Win32API \| Tool Help 結構 \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ") </span><span class="sxs-lookup"><span data-stu-id="e7727-232">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32)\|th32OwnerProcessID")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-233">建立執行緒的進程。</span><span class="sxs-lookup"><span data-stu-id="e7727-233">Process that created the thread.</span></span> <span data-ttu-id="e7727-234">Windows 應用程式開發介面可以使用這個屬性的內容 (API) 元素。</span><span class="sxs-lookup"><span data-stu-id="e7727-234">The contents of this property can be used by Windows application programming interface (API) elements.</span></span>

</dd> <dt>

<span data-ttu-id="e7727-235">**StartAddress**</span><span class="sxs-lookup"><span data-stu-id="e7727-235">**StartAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-236">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7727-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-238">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WIn32API \| Thread Object \| LPTHREAD \_ START \_ 常式 \| lpStartAddress" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIn32API\|Thread Object\|LPTHREAD\_START\_ROUTINE\|lpStartAddress")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-239">執行緒的起始位址。</span><span class="sxs-lookup"><span data-stu-id="e7727-239">Starting address of the thread.</span></span> <span data-ttu-id="e7727-240">由於具有適當存取執行緒的任何應用程式都可以變更執行緒的內容，因此這個值可能只是執行緒起始位址的近似值。</span><span class="sxs-lookup"><span data-stu-id="e7727-240">Because any application with appropriate access to the thread can change the thread's context, this value may only be an approximation of the thread's starting address.</span></span>

</dd> <dt>

<span data-ttu-id="e7727-241">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e7727-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e7727-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-244">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-244">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-245">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e7727-245">Current status of the object.</span></span> <span data-ttu-id="e7727-246">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="e7727-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e7727-247">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="e7727-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e7727-248">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="e7727-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e7727-249">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="e7727-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e7727-250">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="e7727-250">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e7727-251">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e7727-252">值如下：</span><span class="sxs-lookup"><span data-stu-id="e7727-252">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e7727-253">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e7727-253">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e7727-254">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-254">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e7727-255">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-255">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7727-256">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-256">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e7727-257">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-257">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e7727-258">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-258">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e7727-259">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-259">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e7727-260">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-260">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e7727-261">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-261">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e7727-262">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-262">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e7727-263">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-263">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e7727-264">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e7727-264">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7727-265">**ThreadState**</span><span class="sxs-lookup"><span data-stu-id="e7727-265">**ThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-266">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7727-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-268">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Thread State" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread State")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-269">執行緒的目前執行狀態。</span><span class="sxs-lookup"><span data-stu-id="e7727-269">Current execution state for the thread.</span></span>

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span data-ttu-id="e7727-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**初始化** (0) </span><span class="sxs-lookup"><span data-stu-id="e7727-270"><span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Initialized** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-271">已初始化-種微核心可辨識它。</span><span class="sxs-lookup"><span data-stu-id="e7727-271">Initialized — It is recognized by the microkernel.</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="e7727-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**就緒** (1) </span><span class="sxs-lookup"><span data-stu-id="e7727-272"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-273">就緒—準備好在下一個可用的處理器上執行。</span><span class="sxs-lookup"><span data-stu-id="e7727-273">Ready — It is prepared to run on the next available processor.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="e7727-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (2) </span><span class="sxs-lookup"><span data-stu-id="e7727-274"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-275">正在執行中-正在執行。</span><span class="sxs-lookup"><span data-stu-id="e7727-275">Running — It is executing.</span></span>

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span data-ttu-id="e7727-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**待命** (3) </span><span class="sxs-lookup"><span data-stu-id="e7727-276"><span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>**Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-277">待命-即將執行，一次只能有一個執行緒處於此狀態。</span><span class="sxs-lookup"><span data-stu-id="e7727-277">Standby — It is about to run, only one thread may be in this state at a time.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="e7727-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>已 **終止** (4) </span><span class="sxs-lookup"><span data-stu-id="e7727-278"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-279">已終止-它已完成執行。</span><span class="sxs-lookup"><span data-stu-id="e7727-279">Terminated — It is finished executing.</span></span>

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span data-ttu-id="e7727-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**正在等候** (5) </span><span class="sxs-lookup"><span data-stu-id="e7727-280"><span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Waiting** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-281">等候中-它尚未準備好供處理器進行，將會重新排定。</span><span class="sxs-lookup"><span data-stu-id="e7727-281">Waiting — It is not ready for the processor, when ready, it will be rescheduled.</span></span>

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span data-ttu-id="e7727-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**轉換** (6) </span><span class="sxs-lookup"><span data-stu-id="e7727-282"><span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transition** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-283">轉換—執行緒正在等候處理器以外的資源，</span><span class="sxs-lookup"><span data-stu-id="e7727-283">Transition — The thread is waiting for resources other than the processor,</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7727-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (7) </span><span class="sxs-lookup"><span data-stu-id="e7727-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-285">未知-執行緒狀態不明。</span><span class="sxs-lookup"><span data-stu-id="e7727-285">Unknown — The thread state is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e7727-286">**ThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="e7727-286">**ThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-287">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e7727-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-289">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Thread Wait Reason" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-289">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Thread Wait Reason")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-290">執行緒正在等候的原因。</span><span class="sxs-lookup"><span data-stu-id="e7727-290">Reason why the thread is waiting.</span></span> <span data-ttu-id="e7727-291">只有當 **ThreadState** 成員設定為轉換 (6) 時，此值才有效。</span><span class="sxs-lookup"><span data-stu-id="e7727-291">This value is only valid if the **ThreadState** member is set to Transition (6).</span></span> <span data-ttu-id="e7727-292">事件配對允許與受保護子系統進行通訊。</span><span class="sxs-lookup"><span data-stu-id="e7727-292">Event pairs allow communication with protected subsystems.</span></span>

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="e7727-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**主管** (0) </span><span class="sxs-lookup"><span data-stu-id="e7727-293"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="e7727-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1) </span><span class="sxs-lookup"><span data-stu-id="e7727-294"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e7727-295">FreePage</span><span class="sxs-lookup"><span data-stu-id="e7727-295">FreePage</span></span>

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="e7727-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2) </span><span class="sxs-lookup"><span data-stu-id="e7727-296"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="e7727-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3) </span><span class="sxs-lookup"><span data-stu-id="e7727-297"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="e7727-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4) </span><span class="sxs-lookup"><span data-stu-id="e7727-298"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="e7727-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5) </span><span class="sxs-lookup"><span data-stu-id="e7727-299"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="e7727-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6) </span><span class="sxs-lookup"><span data-stu-id="e7727-300"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="e7727-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7) </span><span class="sxs-lookup"><span data-stu-id="e7727-301"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="e7727-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8) </span><span class="sxs-lookup"><span data-stu-id="e7727-302"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="e7727-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9) </span><span class="sxs-lookup"><span data-stu-id="e7727-303"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span data-ttu-id="e7727-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10) </span><span class="sxs-lookup"><span data-stu-id="e7727-304"><span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span data-ttu-id="e7727-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11) </span><span class="sxs-lookup"><span data-stu-id="e7727-305"><span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span data-ttu-id="e7727-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12) </span><span class="sxs-lookup"><span data-stu-id="e7727-306"><span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span data-ttu-id="e7727-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13) </span><span class="sxs-lookup"><span data-stu-id="e7727-307"><span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span data-ttu-id="e7727-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14) </span><span class="sxs-lookup"><span data-stu-id="e7727-308"><span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span data-ttu-id="e7727-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15) </span><span class="sxs-lookup"><span data-stu-id="e7727-309"><span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span data-ttu-id="e7727-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16) </span><span class="sxs-lookup"><span data-stu-id="e7727-310"><span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span data-ttu-id="e7727-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17) </span><span class="sxs-lookup"><span data-stu-id="e7727-311"><span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span data-ttu-id="e7727-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18) </span><span class="sxs-lookup"><span data-stu-id="e7727-312"><span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span data-ttu-id="e7727-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19) </span><span class="sxs-lookup"><span data-stu-id="e7727-313"><span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e7727-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (20) </span><span class="sxs-lookup"><span data-stu-id="e7727-314"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (20)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7727-315">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="e7727-315">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7727-316">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e7727-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7727-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e7727-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7727-318">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "UserModeTime" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 效能資料結構效能 \| [**\_ 物件 \_ 類型**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "100 毫微秒" ) </span><span class="sxs-lookup"><span data-stu-id="e7727-318">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Performance Data Structures\|[**PERF\_OBJECT\_TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type)\|UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="e7727-319">在使用者模式下的時間，以100毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="e7727-319">Time in user mode, in 100 nanoseconds units.</span></span> <span data-ttu-id="e7727-320">如果無法使用這項資訊，則應使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="e7727-320">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="e7727-321">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7727-322">備註</span><span class="sxs-lookup"><span data-stu-id="e7727-322">Remarks</span></span>

<span data-ttu-id="e7727-323">**Win32 \_ 執行緒** 類別衍生自 [**CIM \_ 執行緒**](cim-thread.md)。</span><span class="sxs-lookup"><span data-stu-id="e7727-323">The **Win32\_Thread** class is derived from [**CIM\_Thread**](cim-thread.md).</span></span>

<span data-ttu-id="e7727-324">**概觀**</span><span class="sxs-lookup"><span data-stu-id="e7727-324">**Overview**</span></span>

<span data-ttu-id="e7727-325">針對例行的日常監視，通常會有很多原因會有詳細的執行緒清單及其相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="e7727-325">For routine day-to-day monitoring, there is usually little reason to have a detailed list of threads and their associated properties.</span></span> <span data-ttu-id="e7727-326">電腦會在一天中建立及刪除上千個執行緒，而且這些建立或刪除動作對撰寫軟體的開發人員而言有意義。</span><span class="sxs-lookup"><span data-stu-id="e7727-326">Computers create and delete thousands of threads during the course of a day, and few of these creations or deletions are meaningful to anyone but the developer who wrote the software.</span></span>

<span data-ttu-id="e7727-327">但是，當您針對應用程式的問題進行疑難排解時，追蹤進程的個別執行緒可讓您識別建立執行緒的時間，以及在 (時或) 終結的時機。</span><span class="sxs-lookup"><span data-stu-id="e7727-327">However, when you are troubleshooting problems with an application, tracking the individual threads for a process allows you to identify when threads are created and when (or if) they are destroyed.</span></span> <span data-ttu-id="e7727-328">因為建立但未終結的執行緒會造成記憶體流失，所以追蹤個別執行緒可能是支援技術人員的實用資訊。</span><span class="sxs-lookup"><span data-stu-id="e7727-328">Because threads that are created but not destroyed cause memory leaks, tracking individual threads can be useful information for support technicians.</span></span> <span data-ttu-id="e7727-329">同樣地，識別執行緒優先順序有助於找出以異常高優先順序執行的執行緒，這是其他執行緒和其他進程所需的優先 CPU 週期。</span><span class="sxs-lookup"><span data-stu-id="e7727-329">Likewise, identifying thread priorities can help pinpoint threads that, by running at an abnormally high priority, are preempting CPU cycles needed by other threads and other processes.</span></span>

<span data-ttu-id="e7727-330">**使用 Win32 \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="e7727-330">**Using Win32\_Thread**</span></span>

<span data-ttu-id="e7727-331">如同上述語法區塊所暗示， **Win32 \_ 執行緒** 類別不會報告每個執行緒執行時所用的進程名稱。</span><span class="sxs-lookup"><span data-stu-id="e7727-331">As implied in the preceding syntax block, the **Win32\_Thread** class does not report the name of the process under which each thread runs.</span></span> <span data-ttu-id="e7727-332">相反地，它會報告執行緒執行時所用的進程識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7727-332">Instead, it reports the ID of the process under which the thread runs.</span></span> <span data-ttu-id="e7727-333">若要傳回進程的名稱和其所有線程的清單，您的腳本必須：</span><span class="sxs-lookup"><span data-stu-id="e7727-333">To return the name of a process and a list of all its threads, your script must:</span></span>

1.  <span data-ttu-id="e7727-334">連接至 [**Win32 \_ Process**](win32-process.md) 類別，並傳回進程及其處理序識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="e7727-334">Connect to the [**Win32\_Process**](win32-process.md) class and return the list of processes and their process IDs.</span></span>
2.  <span data-ttu-id="e7727-335">將此資訊暫時儲存在陣列或字典物件中。</span><span class="sxs-lookup"><span data-stu-id="e7727-335">Temporarily store this information in an array or Dictionary object.</span></span>
3.  <span data-ttu-id="e7727-336">針對每個處理序識別碼，傳回該進程的執行緒清單，然後顯示進程名稱和執行緒清單。</span><span class="sxs-lookup"><span data-stu-id="e7727-336">For each process ID, return the list of threads for that process, and then display the process name and the list of threads.</span></span>

## <a name="examples"></a><span data-ttu-id="e7727-337">範例</span><span class="sxs-lookup"><span data-stu-id="e7727-337">Examples</span></span>

<span data-ttu-id="e7727-338">下列 VBScript 範例會監視電腦上執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e7727-338">The following VBScript sample monitors the threads running on a computer.</span></span>


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a><span data-ttu-id="e7727-339">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7727-339">Requirements</span></span>



| <span data-ttu-id="e7727-340">需求</span><span class="sxs-lookup"><span data-stu-id="e7727-340">Requirement</span></span> | <span data-ttu-id="e7727-341">值</span><span class="sxs-lookup"><span data-stu-id="e7727-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7727-342">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7727-342">Minimum supported client</span></span><br/> | <span data-ttu-id="e7727-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7727-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e7727-344">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7727-344">Minimum supported server</span></span><br/> | <span data-ttu-id="e7727-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7727-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e7727-346">命名空間</span><span class="sxs-lookup"><span data-stu-id="e7727-346">Namespace</span></span><br/>                | <span data-ttu-id="e7727-347">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e7727-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e7727-348">MOF</span><span class="sxs-lookup"><span data-stu-id="e7727-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7727-349"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7727-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7727-350">DLL</span><span class="sxs-lookup"><span data-stu-id="e7727-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7727-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7727-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7727-352">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7727-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7727-353">**CIM \_ 執行緒**</span><span class="sxs-lookup"><span data-stu-id="e7727-353">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dt>

[<span data-ttu-id="e7727-354">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="e7727-354">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
