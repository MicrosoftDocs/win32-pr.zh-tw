---
description: CIM \_ MemoryCheck 類別會指定系統上必須可用的最小記憶體數量的條件。
ms.assetid: a7d22f31-a285-41c4-b069-47c54865ddf5
ms.tgt_platform: multiple
title: CIM_MemoryCheck 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck
- CIM_MemoryCheck.CheckID
- CIM_MemoryCheck.Caption
- CIM_MemoryCheck.Description
- CIM_MemoryCheck.CheckMode
- CIM_MemoryCheck.Name
- CIM_MemoryCheck.TargetOperatingSystem
- CIM_MemoryCheck.Version
- CIM_MemoryCheck.SoftwareElementID
- CIM_MemoryCheck.SoftwareElementState
- CIM_MemoryCheck.MemorySize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4265b108bd57bcb91aa903fd163ff14bd91311ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973780"
---
# <a name="cim_memorycheck-class"></a><span data-ttu-id="89f7e-103">CIM \_ MemoryCheck 類別</span><span class="sxs-lookup"><span data-stu-id="89f7e-103">CIM\_MemoryCheck class</span></span>

<span data-ttu-id="89f7e-104">**CIM \_ MemoryCheck** 類別會指定系統上必須可用的最小記憶體數量的條件。</span><span class="sxs-lookup"><span data-stu-id="89f7e-104">The **CIM\_MemoryCheck** class specifies a condition for the minimum amount of memory that must be available on a system.</span></span> <span data-ttu-id="89f7e-105">數量是在 **MemorySize** 屬性中指定的。</span><span class="sxs-lookup"><span data-stu-id="89f7e-105">The amount is specified in the **MemorySize** property.</span></span> <span data-ttu-id="89f7e-106">檢查的詳細資料會與 cim [**\_ InstalledOS**](cim-installedos.md)關聯的 cim [**\_ 作業系統**](cim-operatingsystem.md)物件的 **FreePhysicalMemory** 屬性值進行比較，該物件是描述環境的 [**cim \_**](cim-computersystem.md)系統系統物件。</span><span class="sxs-lookup"><span data-stu-id="89f7e-106">Details of the checks are compared with the value of the **FreePhysicalMemory** property of the [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="89f7e-107">當 **FreePhysicalMemory** 屬性的值大於或等於 **MemorySize** 中指定的值時，就會滿足條件。</span><span class="sxs-lookup"><span data-stu-id="89f7e-107">When the value of the **FreePhysicalMemory** property is greater than or equal to the value specified in **MemorySize**, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89f7e-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="89f7e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89f7e-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89f7e-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="89f7e-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="89f7e-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="89f7e-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f7e-112">語法</span><span class="sxs-lookup"><span data-stu-id="89f7e-112">Syntax</span></span>

``` syntax
[UUID("{DC0E96FE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_MemoryCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint64  MemorySize;
};
```

## <a name="members"></a><span data-ttu-id="89f7e-113">成員</span><span class="sxs-lookup"><span data-stu-id="89f7e-113">Members</span></span>

<span data-ttu-id="89f7e-114">**CIM \_ MemoryCheck** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89f7e-114">The **CIM\_MemoryCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="89f7e-115">方法</span><span class="sxs-lookup"><span data-stu-id="89f7e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="89f7e-116">屬性</span><span class="sxs-lookup"><span data-stu-id="89f7e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="89f7e-117">方法</span><span class="sxs-lookup"><span data-stu-id="89f7e-117">Methods</span></span>

<span data-ttu-id="89f7e-118">**CIM \_ MemoryCheck** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="89f7e-118">The **CIM\_MemoryCheck** class has these methods.</span></span>



| <span data-ttu-id="89f7e-119">方法</span><span class="sxs-lookup"><span data-stu-id="89f7e-119">Method</span></span>                                                   | <span data-ttu-id="89f7e-120">描述</span><span class="sxs-lookup"><span data-stu-id="89f7e-120">Description</span></span>                                                   |
|:---------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="89f7e-121">**調用**</span><span class="sxs-lookup"><span data-stu-id="89f7e-121">**Invoke**</span></span>](invoke-method-in-class-cim-memorycheck.md) | <span data-ttu-id="89f7e-122">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="89f7e-122">Takes a particular action.</span></span> <span data-ttu-id="89f7e-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="89f7e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="89f7e-124">屬性</span><span class="sxs-lookup"><span data-stu-id="89f7e-124">Properties</span></span>

<span data-ttu-id="89f7e-125">**CIM \_ MemoryCheck** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89f7e-125">The **CIM\_MemoryCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89f7e-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="89f7e-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89f7e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-129">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="89f7e-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-130">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="89f7e-130">A short textual description of the subject.</span></span>

<span data-ttu-id="89f7e-131">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="89f7e-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89f7e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-135">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="89f7e-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-136">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="89f7e-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="89f7e-137">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="89f7e-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="89f7e-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-141">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="89f7e-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="89f7e-142">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="89f7e-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="89f7e-143">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="89f7e-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="89f7e-144">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="89f7e-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="89f7e-145">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-146">**說明**</span><span class="sxs-lookup"><span data-stu-id="89f7e-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89f7e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-149">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="89f7e-149">A description of the objects.</span></span>

<span data-ttu-id="89f7e-150">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-151">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="89f7e-151">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-152">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="89f7e-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-154">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**FreePhysicalMemory**") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="89f7e-154">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-155">電腦系統上必須存在的記憶體數量，軟體元素才能正常執行。</span><span class="sxs-lookup"><span data-stu-id="89f7e-155">Amount of memory that needs to exist on a computer system for a software element to execute properly.</span></span>

<span data-ttu-id="89f7e-156">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-157">**名稱**</span><span class="sxs-lookup"><span data-stu-id="89f7e-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89f7e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-160">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="89f7e-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-161">用來識別軟體元素的名稱</span><span class="sxs-lookup"><span data-stu-id="89f7e-161">Name used to identify the software element</span></span>

<span data-ttu-id="89f7e-162">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="89f7e-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89f7e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-166">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="89f7e-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-167">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="89f7e-167">This is an identifier for this software element.</span></span>

<span data-ttu-id="89f7e-168">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f7e-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="89f7e-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-170">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89f7e-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-172">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="89f7e-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-173">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="89f7e-173">The software element state of a software element.</span></span>

<span data-ttu-id="89f7e-174">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-174">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="89f7e-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="89f7e-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-176">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="89f7e-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="89f7e-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="89f7e-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-178">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="89f7e-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="89f7e-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="89f7e-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-180">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="89f7e-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="89f7e-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="89f7e-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-182">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89f7e-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="89f7e-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="89f7e-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89f7e-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-186">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="89f7e-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-187">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="89f7e-187">Target operating system of the software element.</span></span>

<span data-ttu-id="89f7e-188">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="89f7e-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="89f7e-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="89f7e-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="89f7e-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="89f7e-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="89f7e-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="89f7e-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="89f7e-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="89f7e-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="89f7e-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="89f7e-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="89f7e-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="89f7e-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="89f7e-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="89f7e-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="89f7e-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="89f7e-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="89f7e-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-199">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="89f7e-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="89f7e-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="89f7e-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="89f7e-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="89f7e-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="89f7e-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="89f7e-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="89f7e-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="89f7e-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="89f7e-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="89f7e-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="89f7e-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="89f7e-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="89f7e-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-207">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="89f7e-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="89f7e-208"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="89f7e-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="89f7e-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="89f7e-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-210">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="89f7e-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="89f7e-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="89f7e-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="89f7e-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="89f7e-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="89f7e-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="89f7e-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="89f7e-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="89f7e-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="89f7e-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="89f7e-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="89f7e-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="89f7e-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="89f7e-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="89f7e-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="89f7e-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="89f7e-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="89f7e-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="89f7e-222"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="89f7e-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="89f7e-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="89f7e-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="89f7e-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="89f7e-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="89f7e-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="89f7e-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="89f7e-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="89f7e-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="89f7e-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="89f7e-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="89f7e-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="89f7e-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="89f7e-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="89f7e-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="89f7e-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="89f7e-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="89f7e-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="89f7e-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="89f7e-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="89f7e-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-233">系列</span><span class="sxs-lookup"><span data-stu-id="89f7e-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="89f7e-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="89f7e-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-235">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="89f7e-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="89f7e-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="89f7e-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-237">將 NT</span><span class="sxs-lookup"><span data-stu-id="89f7e-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="89f7e-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="89f7e-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="89f7e-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="89f7e-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="89f7e-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="89f7e-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="89f7e-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="89f7e-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="89f7e-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="89f7e-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="89f7e-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="89f7e-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="89f7e-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="89f7e-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="89f7e-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-246">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="89f7e-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="89f7e-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="89f7e-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="89f7e-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="89f7e-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="89f7e-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="89f7e-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="89f7e-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="89f7e-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="89f7e-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="89f7e-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="89f7e-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="89f7e-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="89f7e-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="89f7e-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="89f7e-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="89f7e-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="89f7e-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="89f7e-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="89f7e-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="89f7e-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="89f7e-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="89f7e-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="89f7e-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="89f7e-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="89f7e-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="89f7e-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="89f7e-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="89f7e-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="89f7e-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="89f7e-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="89f7e-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="89f7e-263">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="89f7e-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="89f7e-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="89f7e-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="89f7e-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="89f7e-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="89f7e-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="89f7e-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="89f7e-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="89f7e-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="89f7e-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="89f7e-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="89f7e-269">**版本**</span><span class="sxs-lookup"><span data-stu-id="89f7e-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89f7e-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89f7e-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89f7e-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89f7e-272">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="89f7e-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="89f7e-273">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="89f7e-273">Version of the operation.</span></span>

<span data-ttu-id="89f7e-274">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="89f7e-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="89f7e-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="89f7e-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="89f7e-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="89f7e-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="89f7e-277">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89f7e-278">備註</span><span class="sxs-lookup"><span data-stu-id="89f7e-278">Remarks</span></span>

<span data-ttu-id="89f7e-279">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="89f7e-279">WMI does not implement this class.</span></span>

<span data-ttu-id="89f7e-280">**Cim \_ MemoryCheck** 類別繼承自 [**cim \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="89f7e-280">The **CIM\_MemoryCheck** class is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<span data-ttu-id="89f7e-281">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="89f7e-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89f7e-282">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="89f7e-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f7e-283">規格需求</span><span class="sxs-lookup"><span data-stu-id="89f7e-283">Requirements</span></span>



| <span data-ttu-id="89f7e-284">需求</span><span class="sxs-lookup"><span data-stu-id="89f7e-284">Requirement</span></span> | <span data-ttu-id="89f7e-285">值</span><span class="sxs-lookup"><span data-stu-id="89f7e-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89f7e-286">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89f7e-286">Minimum supported client</span></span><br/> | <span data-ttu-id="89f7e-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89f7e-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89f7e-288">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89f7e-288">Minimum supported server</span></span><br/> | <span data-ttu-id="89f7e-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89f7e-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89f7e-290">命名空間</span><span class="sxs-lookup"><span data-stu-id="89f7e-290">Namespace</span></span><br/>                | <span data-ttu-id="89f7e-291">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89f7e-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89f7e-292">MOF</span><span class="sxs-lookup"><span data-stu-id="89f7e-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89f7e-293"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="89f7e-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89f7e-294">DLL</span><span class="sxs-lookup"><span data-stu-id="89f7e-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f7e-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f7e-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f7e-296">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89f7e-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f7e-297">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="89f7e-297">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

