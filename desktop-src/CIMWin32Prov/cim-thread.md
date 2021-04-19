---
description: CIM \_ 執行緒類別代表能夠以平行方式執行進程或工作的單位。 一個處理常式可以有許多執行緒，每個執行緒都是進程的弱式。
ms.assetid: 57222d57-61bd-4641-a77c-805263be04b7
ms.tgt_platform: multiple
title: CIM_Thread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Thread
- CIM_Thread.Caption
- CIM_Thread.CreationClassName
- CIM_Thread.CSCreationClassName
- CIM_Thread.CSName
- CIM_Thread.Description
- CIM_Thread.ExecutionState
- CIM_Thread.Handle
- CIM_Thread.InstallDate
- CIM_Thread.KernelModeTime
- CIM_Thread.Name
- CIM_Thread.OSCreationClassName
- CIM_Thread.OSName
- CIM_Thread.Priority
- CIM_Thread.ProcessCreationClassName
- CIM_Thread.ProcessHandle
- CIM_Thread.Status
- CIM_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0a69554ef50a82695d2904b11f4189c3aab11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973186"
---
# <a name="cim_thread-class"></a><span data-ttu-id="5e1b1-104">CIM \_ 執行緒類別</span><span class="sxs-lookup"><span data-stu-id="5e1b1-104">CIM\_Thread class</span></span>

<span data-ttu-id="5e1b1-105">**CIM \_ 執行緒** 類別代表能夠以平行方式執行進程或工作的單位。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-105">The **CIM\_Thread** class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="5e1b1-106">一個處理常式可以有許多執行緒，每個執行緒都是進程的弱式。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-106">A process can have many threads, each of which is weak to the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e1b1-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5e1b1-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5e1b1-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5e1b1-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1b1-111">語法</span><span class="sxs-lookup"><span data-stu-id="5e1b1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C571-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Thread : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  string   Status;
  uint64   UserModeTime;
};
```

## <a name="members"></a><span data-ttu-id="5e1b1-112">成員</span><span class="sxs-lookup"><span data-stu-id="5e1b1-112">Members</span></span>

<span data-ttu-id="5e1b1-113">**CIM \_ 執行緒** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5e1b1-113">The **CIM\_Thread** class has these types of members:</span></span>

-   [<span data-ttu-id="5e1b1-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5e1b1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e1b1-115">屬性</span><span class="sxs-lookup"><span data-stu-id="5e1b1-115">Properties</span></span>

<span data-ttu-id="5e1b1-116">**CIM \_ 執行緒** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-116">The **CIM\_Thread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e1b1-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-121">Short textual description of the object.</span></span>

<span data-ttu-id="5e1b1-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-126">限定詞： [**Cim \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-126">Qualifiers: [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-127">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5e1b1-128">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-128">When used with other key properties of the class, this property allow all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-132">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 進程**](cim-process.md)」。**CSCreationClassName**") ， [**Cim \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-133">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-133">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-137">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 進程**](cim-process.md)」。**CSName**") ， [**Cim \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-138">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-138">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-142">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-143">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-143">Textual description of the object.</span></span>

<span data-ttu-id="5e1b1-144">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-145">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-145">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-148">表示執行緒目前的操作狀況。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-148">Indicates the current operating condition of the thread.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b1-149">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5e1b1-150">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="5e1b1-151">**就緒** (2) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-151">**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="5e1b1-152">**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-152">**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="5e1b1-153">**封鎖** (4) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-153">**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="5e1b1-154">**擱置** 的已封鎖 (5) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-154">**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="5e1b1-155">已 **暫止就緒** (6) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-155">**Suspended Ready** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b1-156">**Handle**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-156">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-159">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-159">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-160">執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-160">Identifier for the thread.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-161">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-161">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-162">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-164">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="5e1b1-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-165">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-165">Date and time the object was installed.</span></span> <span data-ttu-id="5e1b1-166">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-166">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5e1b1-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-168">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-168">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-169">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-171">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-171">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-172">時間，以核心模式為單位，以100毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-172">Time, in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="5e1b1-173">如果無法使用這項資訊，則應使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-173">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="5e1b1-174">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-174">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-175">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-178">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-178">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-179">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-179">Label by which the object is known.</span></span> <span data-ttu-id="5e1b1-180">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-180">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5e1b1-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-182">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-182">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-185">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 進程**](cim-process.md)」。**OSCreationClassName**") ， [**Cim \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSCreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-186">設定作業系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-186">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-187">**OSName**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-187">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-190">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 進程**](cim-process.md)」。**OSName**") ， [**Cim \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-190">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**OSName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-191">設定作業系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-191">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-192">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-192">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-193">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-195">執行緒執行的緊急。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-195">Urgency for execution of a thread.</span></span> <span data-ttu-id="5e1b1-196">執行緒的優先順序可以與其擁有進程不同。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-196">A thread can have a different priority than its owning process.</span></span> <span data-ttu-id="5e1b1-197">如果執行緒無法使用這項資訊，則應使用 0 (零的值) 。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-197">If this information is not available for a thread, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-198">**ProcessCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-198">**ProcessCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-201">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 進程**](cim-process.md)」。**CreationClassName**") ， [**Cim \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**CreationClassName**"), [**Cim\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-202">範圍處理常式的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-202">Scoping process's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-203">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-203">**ProcessHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-206">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 進程**](cim-process.md)」。**處理**") 、 [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-206">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Process**](cim-process.md).**Handle**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-207">範圍處理常式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-207">Scoping process's handle.</span></span>

</dd> <dt>

<span data-ttu-id="5e1b1-208">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-208">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-211">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-211">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-212">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-212">Current status of the object.</span></span> <span data-ttu-id="5e1b1-213">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5e1b1-214">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="5e1b1-214">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5e1b1-215">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-215">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5e1b1-216">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-216">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5e1b1-217">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-217">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5e1b1-218">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-218">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5e1b1-219">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-219">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5e1b1-220">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-220">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5e1b1-221">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-221">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5e1b1-222">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-222">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5e1b1-223">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-223">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5e1b1-224">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-224">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5e1b1-225">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-225">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5e1b1-226">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-226">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5e1b1-227">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-227">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e1b1-228">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5e1b1-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e1b1-230">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="5e1b1-230">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="5e1b1-231">在使用者模式下的時間，以100毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-231">Time, in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="5e1b1-232">如果無法使用這項資訊，則應使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-232">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="5e1b1-233">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e1b1-234">備註</span><span class="sxs-lookup"><span data-stu-id="5e1b1-234">Remarks</span></span>

<span data-ttu-id="5e1b1-235">**Cim \_ 執行緒** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-235">The **CIM\_Thread** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="5e1b1-236">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-236">WMI does not implement this class.</span></span> <span data-ttu-id="5e1b1-237">針對衍生自 **CIM \_ 執行緒** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-237">For WMI classes derived from **CIM\_Thread**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5e1b1-238">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-238">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5e1b1-239">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5e1b1-239">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1b1-240">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e1b1-240">Requirements</span></span>



| <span data-ttu-id="5e1b1-241">需求</span><span class="sxs-lookup"><span data-stu-id="5e1b1-241">Requirement</span></span> | <span data-ttu-id="5e1b1-242">值</span><span class="sxs-lookup"><span data-stu-id="5e1b1-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e1b1-243">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e1b1-243">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1b1-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e1b1-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e1b1-245">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e1b1-245">Minimum supported server</span></span><br/> | <span data-ttu-id="5e1b1-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e1b1-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e1b1-247">命名空間</span><span class="sxs-lookup"><span data-stu-id="5e1b1-247">Namespace</span></span><br/>                | <span data-ttu-id="5e1b1-248">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5e1b1-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5e1b1-249">MOF</span><span class="sxs-lookup"><span data-stu-id="5e1b1-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e1b1-250"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e1b1-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e1b1-251">DLL</span><span class="sxs-lookup"><span data-stu-id="5e1b1-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e1b1-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e1b1-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e1b1-253">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e1b1-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e1b1-254">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5e1b1-254">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

