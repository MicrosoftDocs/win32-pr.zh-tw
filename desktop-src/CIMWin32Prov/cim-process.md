---
description: CIM \_ 進程類別代表執行中程式的單一實例。 使用者通常會將進程視為應用程式或工作。
ms.assetid: 8b00ef6e-5c7f-410c-9e48-1205ea6e5a4c
ms.tgt_platform: multiple
title: CIM_Process 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Process
- CIM_Process.Caption
- CIM_Process.CreationClassName
- CIM_Process.CreationDate
- CIM_Process.CSCreationClassName
- CIM_Process.CSName
- CIM_Process.Description
- CIM_Process.ExecutionState
- CIM_Process.Handle
- CIM_Process.InstallDate
- CIM_Process.KernelModeTime
- CIM_Process.Name
- CIM_Process.OSCreationClassName
- CIM_Process.OSName
- CIM_Process.Priority
- CIM_Process.Status
- CIM_Process.TerminationDate
- CIM_Process.UserModeTime
- CIM_Process.WorkingSetSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 355e29929dc05a701a2beac0919a28aca573ca9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936491"
---
# <a name="cim_process-class"></a><span data-ttu-id="619f6-104">CIM \_ 進程類別</span><span class="sxs-lookup"><span data-stu-id="619f6-104">CIM\_Process class</span></span>

<span data-ttu-id="619f6-105">**CIM \_ 進程** 類別代表執行中程式的單一實例。</span><span class="sxs-lookup"><span data-stu-id="619f6-105">The **CIM\_Process** class represents a single instance of a running program.</span></span> <span data-ttu-id="619f6-106">使用者通常會將進程視為應用程式或工作。</span><span class="sxs-lookup"><span data-stu-id="619f6-106">A user typically sees a process as an application or task.</span></span> <span data-ttu-id="619f6-107">處理常式是由配置給它的記憶體資源工作區和環境設定所定義。</span><span class="sxs-lookup"><span data-stu-id="619f6-107">A process is defined by a workspace of memory resources and environmental settings that are allocated to it.</span></span> <span data-ttu-id="619f6-108">在多工系統上，工作區會防止其他進程入侵資源。</span><span class="sxs-lookup"><span data-stu-id="619f6-108">On a multitasking system, the workspace prevents intrusion of resources by other processes.</span></span> <span data-ttu-id="619f6-109">此外，程式可以執行為多個執行緒，而這些執行緒都是在相同的工作區中執行。</span><span class="sxs-lookup"><span data-stu-id="619f6-109">Additionally, a process can execute as multiple threads, all which run within the same workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="619f6-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="619f6-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="619f6-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="619f6-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="619f6-112">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="619f6-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="619f6-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="619f6-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="619f6-114">語法</span><span class="sxs-lookup"><span data-stu-id="619f6-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C566-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes (CIM)"), AMENDMENT]
class CIM_Process : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  datetime CreationDate;
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
  string   Status;
  datetime TerminationDate;
  uint64   UserModeTime;
  uint64   WorkingSetSize;
};
```

## <a name="members"></a><span data-ttu-id="619f6-115">成員</span><span class="sxs-lookup"><span data-stu-id="619f6-115">Members</span></span>

<span data-ttu-id="619f6-116">**CIM \_ 進程** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="619f6-116">The **CIM\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="619f6-117">屬性</span><span class="sxs-lookup"><span data-stu-id="619f6-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="619f6-118">屬性</span><span class="sxs-lookup"><span data-stu-id="619f6-118">Properties</span></span>

<span data-ttu-id="619f6-119">**CIM \_ 進程** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="619f6-119">The **CIM\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="619f6-120">**標題**</span><span class="sxs-lookup"><span data-stu-id="619f6-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-123">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-124">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="619f6-124">Short textual description of the object.</span></span>

<span data-ttu-id="619f6-125">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="619f6-126">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="619f6-126">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-129">限定詞： [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Class Name" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-129">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-130">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="619f6-130">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="619f6-131">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="619f6-131">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-132">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="619f6-132">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-133">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="619f6-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-135">限定詞： [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CreationDate" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-135">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-136">進程開始執行的時間。</span><span class="sxs-lookup"><span data-stu-id="619f6-136">Time that the process began executing.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-137">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="619f6-137">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-140">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CSCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 電腦系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="619f6-140">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-141">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="619f6-141">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-142">**CSName**</span><span class="sxs-lookup"><span data-stu-id="619f6-142">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-145">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CSName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ") </span><span class="sxs-lookup"><span data-stu-id="619f6-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-146">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="619f6-146">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-147">**說明**</span><span class="sxs-lookup"><span data-stu-id="619f6-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-150">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-151">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="619f6-151">Textual description of the object.</span></span>

<span data-ttu-id="619f6-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="619f6-153">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="619f6-153">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="619f6-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-156">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「執行狀態」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-156">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-157">進程目前的操作狀況。</span><span class="sxs-lookup"><span data-stu-id="619f6-157">Current operating condition of the process.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="619f6-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="619f6-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="619f6-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="619f6-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="619f6-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**就緒** (2) </span><span class="sxs-lookup"><span data-stu-id="619f6-160"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="619f6-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="619f6-161"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="619f6-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**封鎖** (4) </span><span class="sxs-lookup"><span data-stu-id="619f6-162"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="619f6-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**擱置** 的已封鎖 (5) </span><span class="sxs-lookup"><span data-stu-id="619f6-163"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd>

<span data-ttu-id="619f6-164">已封鎖暫停</span><span class="sxs-lookup"><span data-stu-id="619f6-164">Suspended blocked</span></span>

</dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="619f6-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>已 **暫止就緒** (6) </span><span class="sxs-lookup"><span data-stu-id="619f6-165"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd>

<span data-ttu-id="619f6-166">暫止就緒</span><span class="sxs-lookup"><span data-stu-id="619f6-166">Suspended ready</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="619f6-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**終止** (7) </span><span class="sxs-lookup"><span data-stu-id="619f6-167"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="619f6-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (8) </span><span class="sxs-lookup"><span data-stu-id="619f6-168"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="619f6-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span> (9) **成長**</span><span class="sxs-lookup"><span data-stu-id="619f6-169"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="619f6-170">**Handle**</span><span class="sxs-lookup"><span data-stu-id="619f6-170">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-173">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、 [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Handle" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-173">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-174">識別處理常式。</span><span class="sxs-lookup"><span data-stu-id="619f6-174">Identifies the process.</span></span> <span data-ttu-id="619f6-175">處理序識別碼是一種進程控制碼。</span><span class="sxs-lookup"><span data-stu-id="619f6-175">A process identifier is a kind of process handle.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-176">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="619f6-176">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-177">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="619f6-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-179">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="619f6-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-180">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="619f6-180">Date and time the object was installed.</span></span> <span data-ttu-id="619f6-181">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="619f6-181">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="619f6-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="619f6-183">**KernelModeTime**</span><span class="sxs-lookup"><span data-stu-id="619f6-183">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-184">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="619f6-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-186">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「核心模型時間」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kernel Model Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-187">在核心模式中的時間，以100毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="619f6-187">Time in kernel mode, in 100 nanosecond units.</span></span> <span data-ttu-id="619f6-188">如果無法使用這項資訊，則應使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="619f6-188">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="619f6-189">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="619f6-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="619f6-190">**名稱**</span><span class="sxs-lookup"><span data-stu-id="619f6-190">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-193">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-193">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-194">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="619f6-194">Label by which the object is known.</span></span> <span data-ttu-id="619f6-195">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="619f6-195">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="619f6-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="619f6-197">**OSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="619f6-197">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-200">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 作業系統類別名稱 ") </span><span class="sxs-lookup"><span data-stu-id="619f6-200">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-201">設定作業系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="619f6-201">Scoping operating system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-202">**OSName**</span><span class="sxs-lookup"><span data-stu-id="619f6-202">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-205">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**Name**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 作業系統 Name ") </span><span class="sxs-lookup"><span data-stu-id="619f6-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-206">設定作業系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="619f6-206">Scoping operating system's name.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-207">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="619f6-207">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-208">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="619f6-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-210">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Priority" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-210">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-211">進程執行的緊急或重要性。</span><span class="sxs-lookup"><span data-stu-id="619f6-211">Urgency or importance for process execution.</span></span> <span data-ttu-id="619f6-212">如果未針對進程定義優先權，則應該使用 0 (零) 值。</span><span class="sxs-lookup"><span data-stu-id="619f6-212">If a priority is not defined for a process, a value of 0 (zero) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-213">**狀態**</span><span class="sxs-lookup"><span data-stu-id="619f6-213">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="619f6-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-216">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-217">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="619f6-217">Current status of the object.</span></span>

<span data-ttu-id="619f6-218">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="619f6-219">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="619f6-219">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="619f6-220">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="619f6-220">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="619f6-221">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-221">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="619f6-222">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-222">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="619f6-223">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-223">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="619f6-224">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-224">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="619f6-225">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-225">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="619f6-226">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-226">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="619f6-227">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-227">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="619f6-228">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-228">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="619f6-229">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-229">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="619f6-230">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-230">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="619f6-231">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="619f6-231">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="619f6-232">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="619f6-232">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-233">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="619f6-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-235">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "終止日期" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-235">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-236">停止或終止進程的時間。</span><span class="sxs-lookup"><span data-stu-id="619f6-236">Time that the process was stopped or terminated.</span></span>

</dd> <dt>

<span data-ttu-id="619f6-237">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="619f6-237">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-238">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="619f6-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-240">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "使用者模式時間" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-240">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("User Mode Time"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-241">使用者模式中的時間，以100的毫微秒數單位表示。</span><span class="sxs-lookup"><span data-stu-id="619f6-241">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="619f6-242">如果無法使用這項資訊，則應使用 0 (零) 的值。</span><span class="sxs-lookup"><span data-stu-id="619f6-242">If this information is not available, a value of 0 (zero) should be used.</span></span>

<span data-ttu-id="619f6-243">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="619f6-243">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="619f6-244">**WorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="619f6-244">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="619f6-245">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="619f6-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="619f6-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="619f6-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="619f6-247">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "工作集大小" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="619f6-247">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Working Set Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="619f6-248">以位元組為單位的記憶體數量（以位元組為單位），針對使用以頁面為基礎的記憶體管理的作業系統，必須有效率地執行進程。</span><span class="sxs-lookup"><span data-stu-id="619f6-248">Amount of memory, in bytes, that a process needs to execute efficiently for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="619f6-249">如果系統沒有足夠的記憶體 (小於) 的工作集大小，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="619f6-249">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="619f6-250">如果工作集的大小不是已知的，請使用 **Null** 或 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="619f6-250">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="619f6-251">如果提供了工作集資料，您可以監視資訊，以瞭解進程的變更記憶體需求。</span><span class="sxs-lookup"><span data-stu-id="619f6-251">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="619f6-252">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="619f6-252">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="619f6-253">備註</span><span class="sxs-lookup"><span data-stu-id="619f6-253">Remarks</span></span>

<span data-ttu-id="619f6-254">**Cim \_ 進程** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-254">The **CIM\_Process** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="619f6-255">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="619f6-255">WMI does not implement this class.</span></span> <span data-ttu-id="619f6-256">針對衍生自 **CIM \_ 進程** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="619f6-256">For WMI classes derived from **CIM\_Process**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="619f6-257">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="619f6-257">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="619f6-258">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="619f6-258">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="619f6-259">規格需求</span><span class="sxs-lookup"><span data-stu-id="619f6-259">Requirements</span></span>



| <span data-ttu-id="619f6-260">需求</span><span class="sxs-lookup"><span data-stu-id="619f6-260">Requirement</span></span> | <span data-ttu-id="619f6-261">值</span><span class="sxs-lookup"><span data-stu-id="619f6-261">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="619f6-262">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="619f6-262">Minimum supported client</span></span><br/> | <span data-ttu-id="619f6-263">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="619f6-263">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="619f6-264">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="619f6-264">Minimum supported server</span></span><br/> | <span data-ttu-id="619f6-265">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="619f6-265">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="619f6-266">命名空間</span><span class="sxs-lookup"><span data-stu-id="619f6-266">Namespace</span></span><br/>                | <span data-ttu-id="619f6-267">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="619f6-267">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="619f6-268">MOF</span><span class="sxs-lookup"><span data-stu-id="619f6-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="619f6-269"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="619f6-269"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="619f6-270">DLL</span><span class="sxs-lookup"><span data-stu-id="619f6-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="619f6-271"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="619f6-271"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="619f6-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="619f6-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619f6-273">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="619f6-273">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

