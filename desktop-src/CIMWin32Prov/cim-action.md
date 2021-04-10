---
description: CIM \_ 動作類別是一項作業，屬於進程的一部分，可在其下一個狀態下建立軟體專案，或刪除目前狀態中的 software 元素。
ms.assetid: d1f72aaf-7e26-414f-99e7-ff8f14d66360
ms.tgt_platform: multiple
title: CIM_Action 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action
- CIM_Action.ActionID
- CIM_Action.Caption
- CIM_Action.Description
- CIM_Action.Direction
- CIM_Action.Name
- CIM_Action.SoftwareElementID
- CIM_Action.SoftwareElementState
- CIM_Action.TargetOperatingSystem
- CIM_Action.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5f37fa4b62c1e8b678533de4abaa7f6a172904e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110528"
---
# <a name="cim_action-class"></a><span data-ttu-id="e0985-103">CIM \_ 動作類別</span><span class="sxs-lookup"><span data-stu-id="e0985-103">CIM\_Action class</span></span>

<span data-ttu-id="e0985-104">**CIM \_ 動作** 類別是一項作業，屬於進程的一部分，可在其下一個狀態下建立軟體專案，或刪除目前狀態中的 software 元素。</span><span class="sxs-lookup"><span data-stu-id="e0985-104">A **CIM\_Action** class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0985-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e0985-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e0985-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e0985-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e0985-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e0985-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e0985-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e0985-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0985-109">語法</span><span class="sxs-lookup"><span data-stu-id="e0985-109">Syntax</span></span>

``` syntax
[UUID("{2F156260-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Action
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
};
```

## <a name="members"></a><span data-ttu-id="e0985-110">成員</span><span class="sxs-lookup"><span data-stu-id="e0985-110">Members</span></span>

<span data-ttu-id="e0985-111">**CIM \_ 動作** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e0985-111">The **CIM\_Action** class has these types of members:</span></span>

-   [<span data-ttu-id="e0985-112">方法</span><span class="sxs-lookup"><span data-stu-id="e0985-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e0985-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e0985-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e0985-114">方法</span><span class="sxs-lookup"><span data-stu-id="e0985-114">Methods</span></span>

<span data-ttu-id="e0985-115">**CIM \_ 動作** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e0985-115">The **CIM\_Action** class has these methods.</span></span>



| <span data-ttu-id="e0985-116">方法</span><span class="sxs-lookup"><span data-stu-id="e0985-116">Method</span></span>                                              | <span data-ttu-id="e0985-117">描述</span><span class="sxs-lookup"><span data-stu-id="e0985-117">Description</span></span>                                                   |
|:----------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="e0985-118">**調用**</span><span class="sxs-lookup"><span data-stu-id="e0985-118">**Invoke**</span></span>](invoke-method-in-class-cim-action.md) | <span data-ttu-id="e0985-119">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="e0985-119">Takes a particular action.</span></span> <span data-ttu-id="e0985-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e0985-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e0985-121">屬性</span><span class="sxs-lookup"><span data-stu-id="e0985-121">Properties</span></span>

<span data-ttu-id="e0985-122">**CIM \_ 動作** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e0985-122">The **CIM\_Action** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0985-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="e0985-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0985-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-126">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e0985-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e0985-127">指派給軟體元素特定動作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0985-127">Unique identifier assigned to a particular action for a software element.</span></span>

</dd> <dt>

<span data-ttu-id="e0985-128">**標題**</span><span class="sxs-lookup"><span data-stu-id="e0985-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0985-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-131">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e0985-131">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e0985-132">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e0985-132">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e0985-133">**說明**</span><span class="sxs-lookup"><span data-stu-id="e0985-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0985-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0985-136">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e0985-136">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e0985-137">[方向]</span><span class="sxs-lookup"><span data-stu-id="e0985-137">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-138">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e0985-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0985-140">指出特定 **CIM \_ 動作** 物件是否為一連串動作的一部分，以將目前的軟體專案轉換為下一個狀態，例如 "Install"，或移除目前的 software 元素，例如 "Uninstall"。</span><span class="sxs-lookup"><span data-stu-id="e0985-140">Indicates whether a particular **CIM\_Action** object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="e0985-141">**安裝** (0) </span><span class="sxs-lookup"><span data-stu-id="e0985-141">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="e0985-142">**卸載** (1) </span><span class="sxs-lookup"><span data-stu-id="e0985-142">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e0985-143">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e0985-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0985-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-146">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e0985-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e0985-147">識別軟體元素。</span><span class="sxs-lookup"><span data-stu-id="e0985-147">Identifies the software element.</span></span>

</dd> <dt>

<span data-ttu-id="e0985-148">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="e0985-148">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0985-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-151">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e0985-151">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e0985-152">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0985-152">Identifier for the software element.</span></span>

</dd> <dt>

<span data-ttu-id="e0985-153">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="e0985-153">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e0985-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-156">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0985-156">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0985-157">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="e0985-157">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="e0985-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e0985-158"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-159">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="e0985-159">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="e0985-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="e0985-160"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-161">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="e0985-161">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="e0985-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="e0985-162"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-163">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="e0985-163">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="e0985-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="e0985-164"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-165">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e0985-165">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0985-166">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e0985-166">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e0985-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-169">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="e0985-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="e0985-170">擁有軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="e0985-170">Target operating system of the owning software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e0985-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e0985-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e0985-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e0985-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="e0985-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="e0985-173"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-174">Mac OS</span><span class="sxs-lookup"><span data-stu-id="e0985-174">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="e0985-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="e0985-175"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="e0985-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="e0985-176"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="e0985-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="e0985-177"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="e0985-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="e0985-178"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="e0985-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="e0985-179"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-180">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="e0985-180">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="e0985-181"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="e0985-181"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-182">HP-UX</span><span class="sxs-lookup"><span data-stu-id="e0985-182">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="e0985-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="e0985-183"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="e0985-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="e0985-184"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="e0985-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="e0985-185"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="e0985-186"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="e0985-186"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="e0985-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="e0985-187"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-188">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="e0985-188">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="e0985-189"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="e0985-189"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="e0985-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="e0985-190"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-191">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="e0985-191">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="e0985-192"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="e0985-192"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-193">Windows 95</span><span class="sxs-lookup"><span data-stu-id="e0985-193">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="e0985-194"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="e0985-194"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-195">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e0985-195">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="e0985-196"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="e0985-196"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-197">Windows NT</span><span class="sxs-lookup"><span data-stu-id="e0985-197">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="e0985-198"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="e0985-198"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-199">Windows CE</span><span class="sxs-lookup"><span data-stu-id="e0985-199">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="e0985-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="e0985-200"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-201">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="e0985-201">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="e0985-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="e0985-202"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="e0985-203"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="e0985-203"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="e0985-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="e0985-204"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="e0985-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="e0985-205"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="e0985-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="e0985-206"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="e0985-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="e0985-207"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="e0985-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="e0985-208"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="e0985-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="e0985-209"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="e0985-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="e0985-210"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="e0985-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="e0985-211"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="e0985-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="e0985-212"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="e0985-213"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="e0985-213"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-214">系列</span><span class="sxs-lookup"><span data-stu-id="e0985-214">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="e0985-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="e0985-215"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-216">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="e0985-216">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="e0985-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="e0985-217"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-218">將 NT</span><span class="sxs-lookup"><span data-stu-id="e0985-218">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="e0985-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="e0985-219"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-220">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="e0985-220">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="e0985-221"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="e0985-221"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="e0985-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="e0985-222"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="e0985-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="e0985-223"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="e0985-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="e0985-224"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="e0985-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="e0985-225"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="e0985-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="e0985-226"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-227">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="e0985-227">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="e0985-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="e0985-228"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="e0985-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="e0985-229"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="e0985-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="e0985-230"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="e0985-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="e0985-231"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-232">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="e0985-232">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="e0985-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="e0985-233"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="e0985-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="e0985-234"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="e0985-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="e0985-235"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="e0985-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="e0985-236"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="e0985-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="e0985-237"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="e0985-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="e0985-238"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="e0985-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="e0985-239"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="e0985-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="e0985-240"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-241">為 OS</span><span class="sxs-lookup"><span data-stu-id="e0985-241">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="e0985-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="e0985-242"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="e0985-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="e0985-243"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="e0985-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="e0985-244"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="e0985-245">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="e0985-245">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="e0985-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="e0985-246"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="e0985-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="e0985-247"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="e0985-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="e0985-248"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="e0985-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="e0985-249"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="e0985-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="e0985-250"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e0985-251">**版本**</span><span class="sxs-lookup"><span data-stu-id="e0985-251">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0985-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e0985-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0985-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e0985-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0985-254">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="e0985-254">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e0985-255">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="e0985-255">Version of the operation.</span></span>

<span data-ttu-id="e0985-256">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="e0985-256">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="e0985-257"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="e0985-257"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="e0985-258"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="e0985-258"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0985-259">備註</span><span class="sxs-lookup"><span data-stu-id="e0985-259">Remarks</span></span>

<span data-ttu-id="e0985-260">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e0985-260">WMI does not implement this class.</span></span> <span data-ttu-id="e0985-261">請參閱衍生自 **CIM \_ 動作** 之類別的 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="e0985-261">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_Action**.</span></span>

<span data-ttu-id="e0985-262">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e0985-262">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e0985-263">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e0985-263">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0985-264">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0985-264">Requirements</span></span>



| <span data-ttu-id="e0985-265">需求</span><span class="sxs-lookup"><span data-stu-id="e0985-265">Requirement</span></span> | <span data-ttu-id="e0985-266">值</span><span class="sxs-lookup"><span data-stu-id="e0985-266">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0985-267">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0985-267">Minimum supported client</span></span><br/> | <span data-ttu-id="e0985-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0985-268">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0985-269">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0985-269">Minimum supported server</span></span><br/> | <span data-ttu-id="e0985-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0985-270">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0985-271">命名空間</span><span class="sxs-lookup"><span data-stu-id="e0985-271">Namespace</span></span><br/>                | <span data-ttu-id="e0985-272">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e0985-272">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0985-273">MOF</span><span class="sxs-lookup"><span data-stu-id="e0985-273">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0985-274"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0985-274"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0985-275">DLL</span><span class="sxs-lookup"><span data-stu-id="e0985-275">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0985-276"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0985-276"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0985-277">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0985-277">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0985-278">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="e0985-278">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

