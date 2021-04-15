---
description: CIM \_ SwapSpaceCheck 類別會指定系統上必須可用的交換空間量。
ms.assetid: c5e5ec68-bc62-4bdf-93b7-ce868e738dee
ms.tgt_platform: multiple
title: CIM_SwapSpaceCheck 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwapSpaceCheck
- CIM_SwapSpaceCheck.CheckID
- CIM_SwapSpaceCheck.Caption
- CIM_SwapSpaceCheck.Description
- CIM_SwapSpaceCheck.CheckMode
- CIM_SwapSpaceCheck.Name
- CIM_SwapSpaceCheck.TargetOperatingSystem
- CIM_SwapSpaceCheck.Version
- CIM_SwapSpaceCheck.SoftwareElementID
- CIM_SwapSpaceCheck.SoftwareElementState
- CIM_SwapSpaceCheck.SwapSpaceSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992d8a314797c7a977e9a672ecb9d3dcdb561292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510614"
---
# <a name="cim_swapspacecheck-class"></a><span data-ttu-id="53a29-103">CIM \_ SwapSpaceCheck 類別</span><span class="sxs-lookup"><span data-stu-id="53a29-103">CIM\_SwapSpaceCheck class</span></span>

<span data-ttu-id="53a29-104">**CIM \_ SwapSpaceCheck** 類別會指定系統上必須可用的交換空間量。</span><span class="sxs-lookup"><span data-stu-id="53a29-104">The **CIM\_SwapSpaceCheck** class specifies the amount of swap space that must be available on the system.</span></span> <span data-ttu-id="53a29-105">數量是在 **SwapSpaceSize** 屬性中指定的。</span><span class="sxs-lookup"><span data-stu-id="53a29-105">The amount is specified in the **SwapSpaceSize** property.</span></span> <span data-ttu-id="53a29-106">這項檢查的詳細資料會與在 cim [**\_ InstalledOS**](cim-installedos.md)關聯的 [**cim \_ 作業系統**](cim-operatingsystem.md)物件中找到的對應詳細資料，與描述該環境的 cim 系統類型物件進行比較。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="53a29-106">Details of this check are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by the [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="53a29-107">當 **TotalSwapSpaceSize** 屬性的值大於或等於 **SwapSpaceSize** 屬性中指定的值時，就會滿足條件。</span><span class="sxs-lookup"><span data-stu-id="53a29-107">When the value of the **TotalSwapSpaceSize** property is greater than or equal to the value specified in the **SwapSpaceSize** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53a29-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="53a29-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="53a29-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="53a29-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="53a29-110">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="53a29-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="53a29-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="53a29-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a29-112">語法</span><span class="sxs-lookup"><span data-stu-id="53a29-112">Syntax</span></span>

``` syntax
[UUID("{A5AE701E-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SwapSpaceCheck : CIM_Check
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
  uint64  SwapSpaceSize;
};
```

## <a name="members"></a><span data-ttu-id="53a29-113">成員</span><span class="sxs-lookup"><span data-stu-id="53a29-113">Members</span></span>

<span data-ttu-id="53a29-114">**CIM \_ SwapSpaceCheck** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="53a29-114">The **CIM\_SwapSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="53a29-115">方法</span><span class="sxs-lookup"><span data-stu-id="53a29-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="53a29-116">屬性</span><span class="sxs-lookup"><span data-stu-id="53a29-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="53a29-117">方法</span><span class="sxs-lookup"><span data-stu-id="53a29-117">Methods</span></span>

<span data-ttu-id="53a29-118">**CIM \_ SwapSpaceCheck** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="53a29-118">The **CIM\_SwapSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="53a29-119">方法</span><span class="sxs-lookup"><span data-stu-id="53a29-119">Method</span></span>                                                      | <span data-ttu-id="53a29-120">描述</span><span class="sxs-lookup"><span data-stu-id="53a29-120">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="53a29-121">**調用**</span><span class="sxs-lookup"><span data-stu-id="53a29-121">**Invoke**</span></span>](invoke-method-in-class-cim-swapspacecheck.md) | <span data-ttu-id="53a29-122">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="53a29-122">Takes a particular action.</span></span> <span data-ttu-id="53a29-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="53a29-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="53a29-124">屬性</span><span class="sxs-lookup"><span data-stu-id="53a29-124">Properties</span></span>

<span data-ttu-id="53a29-125">**CIM \_ SwapSpaceCheck** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="53a29-125">The **CIM\_SwapSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53a29-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="53a29-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53a29-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-129">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="53a29-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="53a29-130">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="53a29-130">A short textual description of the subject.</span></span>

<span data-ttu-id="53a29-131">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="53a29-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53a29-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-135">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53a29-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53a29-136">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="53a29-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="53a29-137">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="53a29-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="53a29-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53a29-141">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="53a29-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="53a29-142">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="53a29-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="53a29-143">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="53a29-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="53a29-144">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="53a29-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="53a29-145">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-146">**說明**</span><span class="sxs-lookup"><span data-stu-id="53a29-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53a29-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53a29-149">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="53a29-149">A description of the objects.</span></span>

<span data-ttu-id="53a29-150">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-151">**名稱**</span><span class="sxs-lookup"><span data-stu-id="53a29-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53a29-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-154">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53a29-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53a29-155">用來識別軟體元素的名稱</span><span class="sxs-lookup"><span data-stu-id="53a29-155">Name used to identify the software element</span></span>

<span data-ttu-id="53a29-156">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-156">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-157">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="53a29-157">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53a29-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-160">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="53a29-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="53a29-161">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="53a29-161">This is an identifier for this software element.</span></span>

<span data-ttu-id="53a29-162">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-163">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="53a29-163">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="53a29-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-166">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="53a29-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="53a29-167">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="53a29-167">The software element state of a software element.</span></span>

<span data-ttu-id="53a29-168">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="53a29-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="53a29-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-170">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="53a29-170">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="53a29-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="53a29-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-172">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="53a29-172">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="53a29-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="53a29-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-174">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="53a29-174">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="53a29-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="53a29-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-176">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="53a29-176">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="53a29-177">**SwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="53a29-177">**SwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-178">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="53a29-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-180">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 作業系統**](cim-operatingsystem.md)」。**TotalSwapSpaceSize**") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" kb ") </span><span class="sxs-lookup"><span data-stu-id="53a29-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="53a29-181">目標系統上必須有的最小交換空間大小（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="53a29-181">Minimum swap-space size, in kilobytes, that must be available on the target system.</span></span>

<span data-ttu-id="53a29-182">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="53a29-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="53a29-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="53a29-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="53a29-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-186">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="53a29-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="53a29-187">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="53a29-187">Target operating system of the software element.</span></span>

<span data-ttu-id="53a29-188">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="53a29-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="53a29-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="53a29-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="53a29-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="53a29-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="53a29-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="53a29-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="53a29-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="53a29-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="53a29-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="53a29-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="53a29-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="53a29-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="53a29-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="53a29-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="53a29-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="53a29-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="53a29-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-199">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="53a29-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="53a29-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="53a29-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="53a29-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="53a29-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="53a29-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="53a29-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="53a29-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="53a29-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="53a29-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="53a29-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="53a29-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="53a29-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="53a29-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-207">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="53a29-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="53a29-208"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="53a29-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="53a29-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="53a29-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-210">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="53a29-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="53a29-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="53a29-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="53a29-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="53a29-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="53a29-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="53a29-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="53a29-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="53a29-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="53a29-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="53a29-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="53a29-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="53a29-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="53a29-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="53a29-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="53a29-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="53a29-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="53a29-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="53a29-222"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="53a29-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="53a29-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="53a29-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="53a29-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="53a29-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="53a29-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="53a29-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="53a29-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="53a29-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="53a29-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="53a29-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="53a29-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="53a29-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="53a29-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="53a29-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="53a29-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="53a29-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="53a29-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="53a29-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="53a29-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="53a29-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-233">系列</span><span class="sxs-lookup"><span data-stu-id="53a29-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="53a29-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="53a29-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-235">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="53a29-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="53a29-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="53a29-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-237">將 NT</span><span class="sxs-lookup"><span data-stu-id="53a29-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="53a29-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="53a29-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="53a29-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="53a29-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="53a29-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="53a29-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="53a29-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="53a29-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="53a29-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="53a29-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="53a29-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="53a29-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="53a29-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="53a29-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="53a29-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-246">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="53a29-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="53a29-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="53a29-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="53a29-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="53a29-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="53a29-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="53a29-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="53a29-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="53a29-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="53a29-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="53a29-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="53a29-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="53a29-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="53a29-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="53a29-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="53a29-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="53a29-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="53a29-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="53a29-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="53a29-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="53a29-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="53a29-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="53a29-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="53a29-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="53a29-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="53a29-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="53a29-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="53a29-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="53a29-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="53a29-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="53a29-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="53a29-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="53a29-263">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="53a29-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="53a29-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="53a29-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="53a29-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="53a29-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="53a29-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="53a29-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="53a29-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="53a29-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="53a29-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="53a29-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="53a29-269">**版本**</span><span class="sxs-lookup"><span data-stu-id="53a29-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53a29-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53a29-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53a29-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53a29-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53a29-272">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="53a29-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="53a29-273">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="53a29-273">Version of the operation.</span></span>

<span data-ttu-id="53a29-274">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="53a29-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="53a29-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="53a29-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="53a29-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="53a29-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="53a29-277">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="53a29-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53a29-278">備註</span><span class="sxs-lookup"><span data-stu-id="53a29-278">Remarks</span></span>

<span data-ttu-id="53a29-279">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="53a29-279">WMI does not implement this class.</span></span>

<span data-ttu-id="53a29-280">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="53a29-280">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="53a29-281">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="53a29-281">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a29-282">規格需求</span><span class="sxs-lookup"><span data-stu-id="53a29-282">Requirements</span></span>



| <span data-ttu-id="53a29-283">需求</span><span class="sxs-lookup"><span data-stu-id="53a29-283">Requirement</span></span> | <span data-ttu-id="53a29-284">值</span><span class="sxs-lookup"><span data-stu-id="53a29-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53a29-285">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53a29-285">Minimum supported client</span></span><br/> | <span data-ttu-id="53a29-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53a29-286">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53a29-287">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53a29-287">Minimum supported server</span></span><br/> | <span data-ttu-id="53a29-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53a29-288">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53a29-289">命名空間</span><span class="sxs-lookup"><span data-stu-id="53a29-289">Namespace</span></span><br/>                | <span data-ttu-id="53a29-290">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="53a29-290">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53a29-291">MOF</span><span class="sxs-lookup"><span data-stu-id="53a29-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53a29-292"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="53a29-292"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53a29-293">DLL</span><span class="sxs-lookup"><span data-stu-id="53a29-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53a29-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a29-294"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a29-295">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53a29-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a29-296">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="53a29-296">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

