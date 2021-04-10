---
description: CIM \_ CreateDirectoryAction 類別會為要安裝在本機的軟體元素建立空的目錄。
ms.assetid: e8587534-4bb3-44de-98a1-8d777f1da1b3
ms.tgt_platform: multiple
title: CIM_CreateDirectoryAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction
- CIM_CreateDirectoryAction.ActionID
- CIM_CreateDirectoryAction.Caption
- CIM_CreateDirectoryAction.Description
- CIM_CreateDirectoryAction.Direction
- CIM_CreateDirectoryAction.Name
- CIM_CreateDirectoryAction.SoftwareElementID
- CIM_CreateDirectoryAction.SoftwareElementState
- CIM_CreateDirectoryAction.TargetOperatingSystem
- CIM_CreateDirectoryAction.Version
- CIM_CreateDirectoryAction.DirectoryName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f7d0c2fb8d255a02d6df6f6677a31fa3366dfa6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847371"
---
# <a name="cim_createdirectoryaction-class"></a><span data-ttu-id="af58b-103">CIM \_ CreateDirectoryAction 類別</span><span class="sxs-lookup"><span data-stu-id="af58b-103">CIM\_CreateDirectoryAction class</span></span>

<span data-ttu-id="af58b-104">**CIM \_ CreateDirectoryAction** 類別會為要安裝在本機的軟體元素建立空的目錄。</span><span class="sxs-lookup"><span data-stu-id="af58b-104">The **CIM\_CreateDirectoryAction** class creates empty directories for software elements to be installed locally.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af58b-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="af58b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="af58b-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="af58b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="af58b-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="af58b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="af58b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="af58b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af58b-109">語法</span><span class="sxs-lookup"><span data-stu-id="af58b-109">Syntax</span></span>

``` syntax
[UUID("{87946AAC-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CreateDirectoryAction : CIM_DirectoryAction
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
  string DirectoryName;
};
```

## <a name="members"></a><span data-ttu-id="af58b-110">成員</span><span class="sxs-lookup"><span data-stu-id="af58b-110">Members</span></span>

<span data-ttu-id="af58b-111">**CIM \_ CreateDirectoryAction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="af58b-111">The **CIM\_CreateDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="af58b-112">方法</span><span class="sxs-lookup"><span data-stu-id="af58b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="af58b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="af58b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="af58b-114">方法</span><span class="sxs-lookup"><span data-stu-id="af58b-114">Methods</span></span>

<span data-ttu-id="af58b-115">**CIM \_ CreateDirectoryAction** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="af58b-115">The **CIM\_CreateDirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="af58b-116">方法</span><span class="sxs-lookup"><span data-stu-id="af58b-116">Method</span></span>                                                             | <span data-ttu-id="af58b-117">描述</span><span class="sxs-lookup"><span data-stu-id="af58b-117">Description</span></span>                                                                                                                                  |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af58b-118">**調用**</span><span class="sxs-lookup"><span data-stu-id="af58b-118">**Invoke**</span></span>](invoke-method-in-class-cim-createdirectoryaction.md) | <span data-ttu-id="af58b-119">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="af58b-119">Takes a particular action.</span></span> <span data-ttu-id="af58b-120">方法執行動作的詳細資料是實作為特定的。</span><span class="sxs-lookup"><span data-stu-id="af58b-120">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="af58b-121">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="af58b-121">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="af58b-122">屬性</span><span class="sxs-lookup"><span data-stu-id="af58b-122">Properties</span></span>

<span data-ttu-id="af58b-123">**CIM \_ CreateDirectoryAction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="af58b-123">The **CIM\_CreateDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af58b-124">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="af58b-124">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-127">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="af58b-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="af58b-128">指派給軟體元素特定動作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="af58b-128">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="af58b-129">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-129">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="af58b-130">**標題**</span><span class="sxs-lookup"><span data-stu-id="af58b-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-133">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="af58b-133">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af58b-134">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="af58b-134">Short textual description of the object.</span></span>

<span data-ttu-id="af58b-135">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-135">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="af58b-136">**說明**</span><span class="sxs-lookup"><span data-stu-id="af58b-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af58b-139">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="af58b-139">Description of the object.</span></span>

<span data-ttu-id="af58b-140">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-140">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="af58b-141">[方向]</span><span class="sxs-lookup"><span data-stu-id="af58b-141">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="af58b-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af58b-144">指出特定 [**CIM \_ 動作**](cim-action.md) 物件是否為一連串動作的一部分，以將目前的軟體專案轉換為下一個狀態，例如 "Install"，或移除目前的 software 元素，例如 "Uninstall"。</span><span class="sxs-lookup"><span data-stu-id="af58b-144">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="af58b-145">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-145">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="af58b-146">**安裝** (0) </span><span class="sxs-lookup"><span data-stu-id="af58b-146">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="af58b-147">**卸載** (1) </span><span class="sxs-lookup"><span data-stu-id="af58b-147">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af58b-148">**DirectoryName**</span><span class="sxs-lookup"><span data-stu-id="af58b-148">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-151">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="af58b-151">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="af58b-152">動作套用的目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="af58b-152">Name of the directory to which the action applies.</span></span>

<span data-ttu-id="af58b-153">這個屬性繼承自 [**CIM \_ DirectoryAction**](cim-directoryaction.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-153">This property is inherited from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

</dd> <dt>

<span data-ttu-id="af58b-154">**名稱**</span><span class="sxs-lookup"><span data-stu-id="af58b-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-157">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="af58b-157">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="af58b-158">識別軟體元素。</span><span class="sxs-lookup"><span data-stu-id="af58b-158">Identifies the software element.</span></span>

<span data-ttu-id="af58b-159">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-159">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="af58b-160">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="af58b-160">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-163">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="af58b-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="af58b-164">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="af58b-164">Identifier for the software element.</span></span>

<span data-ttu-id="af58b-165">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-165">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="af58b-166">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="af58b-166">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="af58b-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-169">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af58b-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af58b-170">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="af58b-170">State of a software element.</span></span>

<span data-ttu-id="af58b-171">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-171">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="af58b-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="af58b-172"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-173">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="af58b-173">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="af58b-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="af58b-174"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-175">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="af58b-175">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="af58b-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="af58b-176"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-177">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="af58b-177">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="af58b-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="af58b-178"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-179">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="af58b-179">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af58b-180">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="af58b-180">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-181">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="af58b-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-183">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="af58b-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="af58b-184">擁有軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="af58b-184">Target operating system of the owning software element.</span></span>

<span data-ttu-id="af58b-185">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-185">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af58b-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="af58b-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af58b-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="af58b-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="af58b-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="af58b-188"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-189">Mac OS</span><span class="sxs-lookup"><span data-stu-id="af58b-189">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="af58b-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="af58b-190"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="af58b-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="af58b-191"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="af58b-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="af58b-192"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="af58b-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="af58b-193"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="af58b-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="af58b-194"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-195">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="af58b-195">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="af58b-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="af58b-196"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-197">HP-UX</span><span class="sxs-lookup"><span data-stu-id="af58b-197">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="af58b-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="af58b-198"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="af58b-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="af58b-199"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="af58b-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="af58b-200"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="af58b-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="af58b-201"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="af58b-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="af58b-202"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-203">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="af58b-203">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="af58b-204"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="af58b-204"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="af58b-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="af58b-205"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-206">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="af58b-206">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="af58b-207"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="af58b-207"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-208">Windows 95</span><span class="sxs-lookup"><span data-stu-id="af58b-208">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="af58b-209"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="af58b-209"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-210">Windows 98</span><span class="sxs-lookup"><span data-stu-id="af58b-210">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="af58b-211"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="af58b-211"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-212">Windows NT</span><span class="sxs-lookup"><span data-stu-id="af58b-212">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="af58b-213"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="af58b-213"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-214">Windows CE</span><span class="sxs-lookup"><span data-stu-id="af58b-214">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="af58b-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="af58b-215"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-216">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="af58b-216">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="af58b-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="af58b-217"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="af58b-218"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="af58b-218"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="af58b-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="af58b-219"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="af58b-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="af58b-220"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="af58b-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="af58b-221"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="af58b-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="af58b-222"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="af58b-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="af58b-223"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="af58b-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="af58b-224"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="af58b-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="af58b-225"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="af58b-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="af58b-226"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="af58b-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="af58b-227"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="af58b-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="af58b-228"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-229">系列</span><span class="sxs-lookup"><span data-stu-id="af58b-229">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="af58b-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="af58b-230"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-231">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="af58b-231">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="af58b-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="af58b-232"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-233">將 NT</span><span class="sxs-lookup"><span data-stu-id="af58b-233">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="af58b-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="af58b-234"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-235">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="af58b-235">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="af58b-236"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="af58b-236"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="af58b-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="af58b-237"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="af58b-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="af58b-238"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="af58b-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="af58b-239"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="af58b-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="af58b-240"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="af58b-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="af58b-241"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-242">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="af58b-242">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="af58b-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="af58b-243"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="af58b-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="af58b-244"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="af58b-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="af58b-245"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="af58b-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="af58b-246"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-247">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="af58b-247">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="af58b-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="af58b-248"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="af58b-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="af58b-249"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="af58b-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="af58b-250"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="af58b-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="af58b-251"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="af58b-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="af58b-252"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="af58b-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="af58b-253"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="af58b-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="af58b-254"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="af58b-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="af58b-255"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-256">為 OS</span><span class="sxs-lookup"><span data-stu-id="af58b-256">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="af58b-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="af58b-257"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="af58b-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="af58b-258"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="af58b-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="af58b-259"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="af58b-260">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="af58b-260">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="af58b-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="af58b-261"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="af58b-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="af58b-262"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="af58b-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="af58b-263"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="af58b-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="af58b-264"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="af58b-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="af58b-265"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af58b-266">**版本**</span><span class="sxs-lookup"><span data-stu-id="af58b-266">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af58b-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="af58b-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af58b-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="af58b-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af58b-269">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="af58b-269">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="af58b-270">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="af58b-270">Version of the operation.</span></span>

<span data-ttu-id="af58b-271">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="af58b-271">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="af58b-272"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="af58b-272"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="af58b-273"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="af58b-273"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="af58b-274">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-274">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af58b-275">備註</span><span class="sxs-lookup"><span data-stu-id="af58b-275">Remarks</span></span>

<span data-ttu-id="af58b-276">**Cim \_ CreateDirectoryAction** 類別衍生自 [**cim \_ DirectoryAction**](cim-directoryaction.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-276">The **CIM\_CreateDirectoryAction** class is derived from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

<span data-ttu-id="af58b-277">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="af58b-277">WMI does not implement this class.</span></span> <span data-ttu-id="af58b-278">針對衍生自 **CIM \_ CreateDirectoryAction** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="af58b-278">For classes derived from **CIM\_CreateDirectoryAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="af58b-279">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="af58b-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="af58b-280">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="af58b-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="af58b-281">規格需求</span><span class="sxs-lookup"><span data-stu-id="af58b-281">Requirements</span></span>



| <span data-ttu-id="af58b-282">需求</span><span class="sxs-lookup"><span data-stu-id="af58b-282">Requirement</span></span> | <span data-ttu-id="af58b-283">值</span><span class="sxs-lookup"><span data-stu-id="af58b-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af58b-284">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af58b-284">Minimum supported client</span></span><br/> | <span data-ttu-id="af58b-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af58b-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af58b-286">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af58b-286">Minimum supported server</span></span><br/> | <span data-ttu-id="af58b-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af58b-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af58b-288">命名空間</span><span class="sxs-lookup"><span data-stu-id="af58b-288">Namespace</span></span><br/>                | <span data-ttu-id="af58b-289">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="af58b-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af58b-290">MOF</span><span class="sxs-lookup"><span data-stu-id="af58b-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af58b-291"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="af58b-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af58b-292">DLL</span><span class="sxs-lookup"><span data-stu-id="af58b-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af58b-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af58b-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af58b-294">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af58b-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af58b-295">**CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="af58b-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

