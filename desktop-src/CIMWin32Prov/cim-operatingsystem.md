---
description: CIM 作業系統 \_ 類別代表電腦作業系統，由軟體和固件組成，可讓電腦系統的硬體可用。
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: CIM_OperatingSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510597"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="37f2a-103">CIM \_ 作業系統類別</span><span class="sxs-lookup"><span data-stu-id="37f2a-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="37f2a-104">**CIM 作業系統 \_** 類別代表電腦作業系統，由軟體和固件組成，可讓電腦系統的硬體可用。</span><span class="sxs-lookup"><span data-stu-id="37f2a-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37f2a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="37f2a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="37f2a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="37f2a-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="37f2a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="37f2a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="37f2a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f2a-109">語法</span><span class="sxs-lookup"><span data-stu-id="37f2a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="37f2a-110">成員</span><span class="sxs-lookup"><span data-stu-id="37f2a-110">Members</span></span>

<span data-ttu-id="37f2a-111">**CIM \_ 作業系統** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="37f2a-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="37f2a-112">方法</span><span class="sxs-lookup"><span data-stu-id="37f2a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="37f2a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="37f2a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="37f2a-114">方法</span><span class="sxs-lookup"><span data-stu-id="37f2a-114">Methods</span></span>

<span data-ttu-id="37f2a-115">**CIM \_ 作業系統** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="37f2a-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="37f2a-116">方法</span><span class="sxs-lookup"><span data-stu-id="37f2a-116">Method</span></span>                                                           | <span data-ttu-id="37f2a-117">描述</span><span class="sxs-lookup"><span data-stu-id="37f2a-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37f2a-118">**重新啟動**</span><span class="sxs-lookup"><span data-stu-id="37f2a-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="37f2a-119">關閉電腦系統的類別方法，然後重新開機它。</span><span class="sxs-lookup"><span data-stu-id="37f2a-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="37f2a-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="37f2a-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="37f2a-121">**關閉**</span><span class="sxs-lookup"><span data-stu-id="37f2a-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="37f2a-122">將程式和 Dll 卸載至安全關閉電腦之點的類別方法。</span><span class="sxs-lookup"><span data-stu-id="37f2a-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="37f2a-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="37f2a-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="37f2a-124">屬性</span><span class="sxs-lookup"><span data-stu-id="37f2a-124">Properties</span></span>

<span data-ttu-id="37f2a-125">**CIM \_ 作業系統** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="37f2a-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37f2a-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="37f2a-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-129">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-130">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="37f2a-130">Short textual description of the object.</span></span>

<span data-ttu-id="37f2a-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37f2a-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-135">限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="37f2a-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-136">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="37f2a-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="37f2a-137">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="37f2a-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37f2a-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-141">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**CreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="37f2a-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-142">設定電腦系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="37f2a-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="37f2a-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-146">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_**](cim-computersystem.md)未執行」。**Name**") 、 [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="37f2a-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-147">設定電腦系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="37f2a-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-148">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="37f2a-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-149">資料類型： **sint16**</span><span class="sxs-lookup"><span data-stu-id="37f2a-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-151">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "分鐘" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-152">作業系統從格林尼治平均時間 (GMT) 位移的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="37f2a-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="37f2a-153">此數位為正數、負數或零。</span><span class="sxs-lookup"><span data-stu-id="37f2a-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-154">**說明**</span><span class="sxs-lookup"><span data-stu-id="37f2a-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-157">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-158">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="37f2a-158">Textual description of the object.</span></span>

<span data-ttu-id="37f2a-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-160">**分散式**</span><span class="sxs-lookup"><span data-stu-id="37f2a-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-161">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="37f2a-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-163">若 **為 TRUE**，則會將作業系統分散到數個電腦系統節點，這些節點應群組為叢集。</span><span class="sxs-lookup"><span data-stu-id="37f2a-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-164">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="37f2a-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-165">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-167">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-168">目前未使用而且可用的實體記憶體的 kb 數。</span><span class="sxs-lookup"><span data-stu-id="37f2a-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="37f2a-169">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-170">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="37f2a-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-171">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-173">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統記憶體設定 \| 001.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-174">可以對應到作業系統分頁檔的 kb 數目，而不會造成其他頁面交換。值為0表示沒有分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="37f2a-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="37f2a-175">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-176">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="37f2a-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-177">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-179">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-180">目前未使用且可用的虛擬記憶體 kb 數目。</span><span class="sxs-lookup"><span data-stu-id="37f2a-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="37f2a-181">例如，您可以將可用 RAM 的數量新增至可用的分頁空間量來計算， (也就是將 **FreePhysicalMemory** 和 **FreeSpaceInPagingFiles** 屬性新增) 。</span><span class="sxs-lookup"><span data-stu-id="37f2a-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="37f2a-182">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="37f2a-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-184">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="37f2a-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-186">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-187">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="37f2a-187">Date and time the object was installed.</span></span> <span data-ttu-id="37f2a-188">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="37f2a-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="37f2a-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="37f2a-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-191">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="37f2a-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-193">作業系統上次開機的時間。</span><span class="sxs-lookup"><span data-stu-id="37f2a-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-194">**>datetimeoffset.localdatetime**</span><span class="sxs-lookup"><span data-stu-id="37f2a-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-195">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="37f2a-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-197">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrSystemDate "，" MIF。DMTF \| 一般資訊 \| 001.6 ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-198">作業系統的本地日期和時間的概念。</span><span class="sxs-lookup"><span data-stu-id="37f2a-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-199">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="37f2a-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-200">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="37f2a-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-202">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrSystemMaxProcesses ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-203">作業系統可支援的進程內容數目上限。</span><span class="sxs-lookup"><span data-stu-id="37f2a-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="37f2a-204">如果沒有固定的最大值，此值應為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="37f2a-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="37f2a-205">在具有固定最大值的系統上，此物件可協助診斷達到上限時所發生的失敗。</span><span class="sxs-lookup"><span data-stu-id="37f2a-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="37f2a-206">如果不明，請輸入-1。</span><span class="sxs-lookup"><span data-stu-id="37f2a-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-207">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="37f2a-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-208">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-210">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-211">可配置給進程的最大記憶體 kb 數。</span><span class="sxs-lookup"><span data-stu-id="37f2a-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="37f2a-212">對於沒有虛擬記憶體的作業系統，此值通常等於實體記憶體的總數量，減去 BIOS 和作業系統所使用的記憶體。</span><span class="sxs-lookup"><span data-stu-id="37f2a-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="37f2a-213">針對某些作業系統，此值可以是無限大，在此情況下應該輸入0。</span><span class="sxs-lookup"><span data-stu-id="37f2a-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="37f2a-214">在其他情況下，此值可以是常數（例如，2 GB 或 4 GB）。</span><span class="sxs-lookup"><span data-stu-id="37f2a-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="37f2a-215">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-216">**名稱**</span><span class="sxs-lookup"><span data-stu-id="37f2a-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-219">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-220">電腦系統內作業系統實例的金鑰。</span><span class="sxs-lookup"><span data-stu-id="37f2a-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="37f2a-221">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-222">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="37f2a-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-223">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="37f2a-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-225">作業系統的使用者授權數目。</span><span class="sxs-lookup"><span data-stu-id="37f2a-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="37f2a-226">如果沒有限制，請輸入0，如果不明，請輸入-1。</span><span class="sxs-lookup"><span data-stu-id="37f2a-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-227">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="37f2a-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-228">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="37f2a-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-230">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrSystemProcesses ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-231">目前已載入或正在作業系統上執行的進程內容數目。</span><span class="sxs-lookup"><span data-stu-id="37f2a-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-232">**Numberofusers 位**</span><span class="sxs-lookup"><span data-stu-id="37f2a-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-233">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="37f2a-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-235">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrSystemNumUsers ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-236">作業系統目前儲存狀態資訊的使用者會話數目。</span><span class="sxs-lookup"><span data-stu-id="37f2a-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="37f2a-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-238">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="37f2a-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-240">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 作業系統**」。**OtherTypeDescription**") </span><span class="sxs-lookup"><span data-stu-id="37f2a-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-241">作業系統的類型。</span><span class="sxs-lookup"><span data-stu-id="37f2a-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37f2a-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="37f2a-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37f2a-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="37f2a-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="37f2a-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="37f2a-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-245">Mac OS</span><span class="sxs-lookup"><span data-stu-id="37f2a-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="37f2a-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="37f2a-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-247">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="37f2a-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="37f2a-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="37f2a-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="37f2a-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="37f2a-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="37f2a-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="37f2a-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="37f2a-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="37f2a-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-252">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="37f2a-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="37f2a-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="37f2a-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="37f2a-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="37f2a-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="37f2a-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="37f2a-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="37f2a-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="37f2a-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="37f2a-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="37f2a-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="37f2a-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="37f2a-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="37f2a-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-260">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="37f2a-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="37f2a-261"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="37f2a-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="37f2a-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="37f2a-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-263">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="37f2a-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="37f2a-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="37f2a-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="37f2a-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="37f2a-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="37f2a-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="37f2a-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="37f2a-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="37f2a-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="37f2a-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="37f2a-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="37f2a-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="37f2a-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="37f2a-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="37f2a-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-273">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="37f2a-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="37f2a-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="37f2a-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="37f2a-275"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="37f2a-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="37f2a-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="37f2a-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="37f2a-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="37f2a-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="37f2a-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="37f2a-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="37f2a-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="37f2a-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="37f2a-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="37f2a-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="37f2a-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="37f2a-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="37f2a-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="37f2a-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="37f2a-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="37f2a-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="37f2a-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="37f2a-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="37f2a-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="37f2a-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-286">系列</span><span class="sxs-lookup"><span data-stu-id="37f2a-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="37f2a-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="37f2a-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-288">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="37f2a-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="37f2a-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="37f2a-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-290">將 NT</span><span class="sxs-lookup"><span data-stu-id="37f2a-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="37f2a-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="37f2a-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="37f2a-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="37f2a-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="37f2a-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="37f2a-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="37f2a-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="37f2a-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="37f2a-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="37f2a-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="37f2a-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="37f2a-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="37f2a-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="37f2a-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="37f2a-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-299">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="37f2a-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="37f2a-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="37f2a-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="37f2a-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="37f2a-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="37f2a-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="37f2a-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="37f2a-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="37f2a-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="37f2a-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="37f2a-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="37f2a-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="37f2a-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="37f2a-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="37f2a-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="37f2a-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="37f2a-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="37f2a-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="37f2a-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="37f2a-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="37f2a-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="37f2a-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="37f2a-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="37f2a-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="37f2a-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="37f2a-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="37f2a-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="37f2a-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="37f2a-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="37f2a-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="37f2a-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="37f2a-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="37f2a-316">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="37f2a-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="37f2a-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="37f2a-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="37f2a-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="37f2a-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="37f2a-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="37f2a-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="37f2a-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60) </span><span class="sxs-lookup"><span data-stu-id="37f2a-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="37f2a-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61) </span><span class="sxs-lookup"><span data-stu-id="37f2a-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="37f2a-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62) </span><span class="sxs-lookup"><span data-stu-id="37f2a-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37f2a-323">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="37f2a-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-326">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ 作業系統**。**OSType**") </span><span class="sxs-lookup"><span data-stu-id="37f2a-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-327">描述當 **OSType** 屬性設定為 1 ( "Other" ) 時的製造商和作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="37f2a-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="37f2a-328">在 **OtherTypeDescription** 中插入的字串格式應該類似于為 **OSType** 定義的 **值** 字串。</span><span class="sxs-lookup"><span data-stu-id="37f2a-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="37f2a-329">當 **OSType** 是 1 (一) 以外的值時，這個屬性應該設為 null。</span><span class="sxs-lookup"><span data-stu-id="37f2a-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-330">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="37f2a-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-331">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-333">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統記憶體設定 \| 001.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="37f2a-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-334">可以儲存在作業系統分頁檔案中的 kb 數。</span><span class="sxs-lookup"><span data-stu-id="37f2a-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="37f2a-335">此數位不代表磁片上分頁檔案的實際實際大小。</span><span class="sxs-lookup"><span data-stu-id="37f2a-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="37f2a-336">值為 0 (零) 表示沒有分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="37f2a-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="37f2a-337">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-338">**狀態**</span><span class="sxs-lookup"><span data-stu-id="37f2a-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-339">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-341">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-342">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="37f2a-342">Current status of the object.</span></span>

<span data-ttu-id="37f2a-343">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="37f2a-344">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="37f2a-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="37f2a-345">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="37f2a-346">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37f2a-347">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37f2a-348">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="37f2a-349">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="37f2a-350">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="37f2a-351">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="37f2a-352">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="37f2a-353">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="37f2a-354">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="37f2a-355">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="37f2a-356">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37f2a-357">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="37f2a-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-358">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-360">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-361">交換空間總計（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="37f2a-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="37f2a-362">如果交換空間與分頁檔不區分，則這個值可以是 null (未指定的) 。</span><span class="sxs-lookup"><span data-stu-id="37f2a-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="37f2a-363">不過，有些作業系統會區分這些概念。</span><span class="sxs-lookup"><span data-stu-id="37f2a-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="37f2a-364">例如，當免費頁面清單落在低於指定的數量時，就可以在 UNIX 中「交換」整個進程。</span><span class="sxs-lookup"><span data-stu-id="37f2a-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="37f2a-365">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-366">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="37f2a-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-367">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-369">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-370">虛擬記憶體的 kb 數。</span><span class="sxs-lookup"><span data-stu-id="37f2a-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="37f2a-371">例如，藉由將總 RAM 容量新增至分頁空間量來計算此值 (也就是將電腦系統的記憶體數量新增至 **SizeStoredInPagingFiles** 屬性，或將電腦系統匯總的記憶體數量加總。</span><span class="sxs-lookup"><span data-stu-id="37f2a-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="37f2a-372">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-373">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="37f2a-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-374">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="37f2a-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-376">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-377">作業系統可用的實體記憶體總容量（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="37f2a-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="37f2a-378">此值不一定會指出真正的實體記憶體數量，而是向作業系統回報的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="37f2a-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="37f2a-379">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="37f2a-380">**版本**</span><span class="sxs-lookup"><span data-stu-id="37f2a-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37f2a-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="37f2a-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="37f2a-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37f2a-383">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 作業系統 \| 001.3」 ) </span><span class="sxs-lookup"><span data-stu-id="37f2a-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="37f2a-384">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="37f2a-384">Version of the operation.</span></span>

<span data-ttu-id="37f2a-385">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="37f2a-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="37f2a-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="37f2a-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="37f2a-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="37f2a-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37f2a-388">備註</span><span class="sxs-lookup"><span data-stu-id="37f2a-388">Remarks</span></span>

<span data-ttu-id="37f2a-389">**Cim \_ 作業系統** 類別衍生自 [**cim \_ LogicalElement**](cim-logicalelement.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="37f2a-390">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="37f2a-390">WMI does not implement this class.</span></span> <span data-ttu-id="37f2a-391">針對衍生自 **CIM \_ 作業系統** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="37f2a-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="37f2a-392">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="37f2a-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="37f2a-393">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="37f2a-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="37f2a-394">規格需求</span><span class="sxs-lookup"><span data-stu-id="37f2a-394">Requirements</span></span>



| <span data-ttu-id="37f2a-395">需求</span><span class="sxs-lookup"><span data-stu-id="37f2a-395">Requirement</span></span> | <span data-ttu-id="37f2a-396">值</span><span class="sxs-lookup"><span data-stu-id="37f2a-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37f2a-397">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37f2a-397">Minimum supported client</span></span><br/> | <span data-ttu-id="37f2a-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37f2a-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37f2a-399">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37f2a-399">Minimum supported server</span></span><br/> | <span data-ttu-id="37f2a-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37f2a-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37f2a-401">命名空間</span><span class="sxs-lookup"><span data-stu-id="37f2a-401">Namespace</span></span><br/>                | <span data-ttu-id="37f2a-402">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="37f2a-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37f2a-403">MOF</span><span class="sxs-lookup"><span data-stu-id="37f2a-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37f2a-404"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="37f2a-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37f2a-405">DLL</span><span class="sxs-lookup"><span data-stu-id="37f2a-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37f2a-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37f2a-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37f2a-407">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37f2a-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f2a-408">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="37f2a-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

