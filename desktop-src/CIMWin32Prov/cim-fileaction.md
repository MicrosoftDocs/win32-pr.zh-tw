---
description: CIM \_ FileAction 類別可讓作者找出使用者電腦上已存在的檔案，然後將這些檔案移動或複製到新的位置。
ms.assetid: 0576e73f-08e1-4f80-af5a-f5d497f57632
ms.tgt_platform: multiple
title: CIM_FileAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileAction
- CIM_FileAction.ActionID
- CIM_FileAction.Caption
- CIM_FileAction.Description
- CIM_FileAction.Direction
- CIM_FileAction.Name
- CIM_FileAction.SoftwareElementID
- CIM_FileAction.SoftwareElementState
- CIM_FileAction.TargetOperatingSystem
- CIM_FileAction.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c4c73a5021efb4fc86c6cbc21d5b6bdc97aec07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936317"
---
# <a name="cim_fileaction-class"></a><span data-ttu-id="17fa7-103">CIM \_ FileAction 類別</span><span class="sxs-lookup"><span data-stu-id="17fa7-103">CIM\_FileAction class</span></span>

<span data-ttu-id="17fa7-104">**CIM \_ FileAction** 類別可讓作者找出使用者電腦上已存在的檔案，然後將這些檔案移動或複製到新的位置。</span><span class="sxs-lookup"><span data-stu-id="17fa7-104">The **CIM\_FileAction** class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17fa7-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="17fa7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17fa7-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17fa7-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="17fa7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="17fa7-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="17fa7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fa7-109">語法</span><span class="sxs-lookup"><span data-stu-id="17fa7-109">Syntax</span></span>

``` syntax
[UUID("{2B590C72-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_FileAction : CIM_Action
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

## <a name="members"></a><span data-ttu-id="17fa7-110">成員</span><span class="sxs-lookup"><span data-stu-id="17fa7-110">Members</span></span>

<span data-ttu-id="17fa7-111">**CIM \_ FileAction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17fa7-111">The **CIM\_FileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="17fa7-112">方法</span><span class="sxs-lookup"><span data-stu-id="17fa7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="17fa7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="17fa7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="17fa7-114">方法</span><span class="sxs-lookup"><span data-stu-id="17fa7-114">Methods</span></span>

<span data-ttu-id="17fa7-115">**CIM \_ FileAction** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="17fa7-115">The **CIM\_FileAction** class has these methods.</span></span>



| <span data-ttu-id="17fa7-116">方法</span><span class="sxs-lookup"><span data-stu-id="17fa7-116">Method</span></span>                                                  | <span data-ttu-id="17fa7-117">描述</span><span class="sxs-lookup"><span data-stu-id="17fa7-117">Description</span></span>                                                   |
|:--------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="17fa7-118">**調用**</span><span class="sxs-lookup"><span data-stu-id="17fa7-118">**Invoke**</span></span>](invoke-method-in-class-cim-fileaction.md) | <span data-ttu-id="17fa7-119">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="17fa7-119">Takes a particular action.</span></span> <span data-ttu-id="17fa7-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="17fa7-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="17fa7-121">屬性</span><span class="sxs-lookup"><span data-stu-id="17fa7-121">Properties</span></span>

<span data-ttu-id="17fa7-122">**CIM \_ FileAction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17fa7-122">The **CIM\_FileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17fa7-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="17fa7-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17fa7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-126">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="17fa7-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-127">指派給軟體元素特定動作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="17fa7-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="17fa7-128">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fa7-129">**標題**</span><span class="sxs-lookup"><span data-stu-id="17fa7-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17fa7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-132">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="17fa7-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-133">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="17fa7-133">Short textual description of the object.</span></span>

<span data-ttu-id="17fa7-134">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fa7-135">**說明**</span><span class="sxs-lookup"><span data-stu-id="17fa7-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17fa7-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-138">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="17fa7-138">Description of the object.</span></span>

<span data-ttu-id="17fa7-139">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fa7-140">[方向]</span><span class="sxs-lookup"><span data-stu-id="17fa7-140">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="17fa7-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-143">指出特定 [**CIM \_ 動作**](cim-action.md) 物件是否為一連串動作的一部分，以將目前的軟體專案轉換為下一個狀態，例如 "Install"，或移除目前的 software 元素，例如 "Uninstall"。</span><span class="sxs-lookup"><span data-stu-id="17fa7-143">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="17fa7-144">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-144">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="17fa7-145">**安裝** (0) </span><span class="sxs-lookup"><span data-stu-id="17fa7-145">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="17fa7-146">**卸載** (1) </span><span class="sxs-lookup"><span data-stu-id="17fa7-146">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17fa7-147">**名稱**</span><span class="sxs-lookup"><span data-stu-id="17fa7-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17fa7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-150">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="17fa7-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-151">識別軟體元素。</span><span class="sxs-lookup"><span data-stu-id="17fa7-151">Identifies the software element.</span></span>

<span data-ttu-id="17fa7-152">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fa7-153">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="17fa7-153">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17fa7-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-156">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="17fa7-156">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-157">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="17fa7-157">Identifier for the software element.</span></span>

<span data-ttu-id="17fa7-158">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-158">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="17fa7-159">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="17fa7-159">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-160">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="17fa7-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-162">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="17fa7-162">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-163">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="17fa7-163">State of a software element.</span></span>

<span data-ttu-id="17fa7-164">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-164">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="17fa7-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="17fa7-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-166">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="17fa7-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="17fa7-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="17fa7-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-168">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="17fa7-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="17fa7-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="17fa7-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-170">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="17fa7-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="17fa7-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="17fa7-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-172">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="17fa7-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="17fa7-173">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="17fa7-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-174">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="17fa7-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-176">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="17fa7-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-177">擁有軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="17fa7-177">Target operating system of the owning software element.</span></span>

<span data-ttu-id="17fa7-178">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-178">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17fa7-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="17fa7-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="17fa7-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="17fa7-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="17fa7-181"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="17fa7-181"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-182">Mac OS</span><span class="sxs-lookup"><span data-stu-id="17fa7-182">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="17fa7-183"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="17fa7-183"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="17fa7-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="17fa7-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="17fa7-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="17fa7-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="17fa7-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="17fa7-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="17fa7-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="17fa7-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-188">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="17fa7-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="17fa7-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="17fa7-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="17fa7-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="17fa7-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="17fa7-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="17fa7-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="17fa7-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="17fa7-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="17fa7-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="17fa7-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="17fa7-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="17fa7-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="17fa7-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-196">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="17fa7-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="17fa7-197"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="17fa7-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="17fa7-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="17fa7-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-199">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="17fa7-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="17fa7-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="17fa7-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="17fa7-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="17fa7-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="17fa7-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="17fa7-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="17fa7-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="17fa7-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="17fa7-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="17fa7-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="17fa7-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="17fa7-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="17fa7-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="17fa7-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-209">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="17fa7-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="17fa7-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="17fa7-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="17fa7-211"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="17fa7-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="17fa7-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="17fa7-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="17fa7-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="17fa7-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="17fa7-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="17fa7-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="17fa7-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="17fa7-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="17fa7-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="17fa7-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="17fa7-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="17fa7-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="17fa7-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="17fa7-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="17fa7-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="17fa7-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="17fa7-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="17fa7-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="17fa7-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="17fa7-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-222">系列</span><span class="sxs-lookup"><span data-stu-id="17fa7-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="17fa7-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="17fa7-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-224">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="17fa7-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="17fa7-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="17fa7-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-226">將 NT</span><span class="sxs-lookup"><span data-stu-id="17fa7-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="17fa7-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="17fa7-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="17fa7-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="17fa7-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="17fa7-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="17fa7-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="17fa7-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="17fa7-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="17fa7-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="17fa7-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="17fa7-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="17fa7-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="17fa7-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="17fa7-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="17fa7-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-235">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="17fa7-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="17fa7-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="17fa7-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="17fa7-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="17fa7-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="17fa7-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="17fa7-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="17fa7-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="17fa7-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="17fa7-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="17fa7-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="17fa7-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="17fa7-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="17fa7-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="17fa7-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="17fa7-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="17fa7-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="17fa7-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="17fa7-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="17fa7-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="17fa7-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="17fa7-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="17fa7-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="17fa7-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="17fa7-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="17fa7-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-249">為 OS</span><span class="sxs-lookup"><span data-stu-id="17fa7-249">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="17fa7-250"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="17fa7-250"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="17fa7-251"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="17fa7-251"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="17fa7-252"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="17fa7-252"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="17fa7-253">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="17fa7-253">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="17fa7-254"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="17fa7-254"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="17fa7-255"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="17fa7-255"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="17fa7-256"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="17fa7-256"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="17fa7-257"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="17fa7-257"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="17fa7-258"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="17fa7-258"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17fa7-259">**版本**</span><span class="sxs-lookup"><span data-stu-id="17fa7-259">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17fa7-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17fa7-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17fa7-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17fa7-262">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="17fa7-262">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="17fa7-263">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="17fa7-263">Version of the operation.</span></span>

<span data-ttu-id="17fa7-264">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="17fa7-264">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="17fa7-265"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="17fa7-265"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="17fa7-266"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="17fa7-266"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="17fa7-267">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-267">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17fa7-268">備註</span><span class="sxs-lookup"><span data-stu-id="17fa7-268">Remarks</span></span>

<span data-ttu-id="17fa7-269">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="17fa7-269">WMI does not implement this class.</span></span> <span data-ttu-id="17fa7-270">針對衍生自 **CIM \_ FileAction** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="17fa7-270">For classes derived from **CIM\_FileAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="17fa7-271">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="17fa7-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17fa7-272">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="17fa7-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17fa7-273">規格需求</span><span class="sxs-lookup"><span data-stu-id="17fa7-273">Requirements</span></span>



| <span data-ttu-id="17fa7-274">需求</span><span class="sxs-lookup"><span data-stu-id="17fa7-274">Requirement</span></span> | <span data-ttu-id="17fa7-275">值</span><span class="sxs-lookup"><span data-stu-id="17fa7-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17fa7-276">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17fa7-276">Minimum supported client</span></span><br/> | <span data-ttu-id="17fa7-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17fa7-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17fa7-278">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17fa7-278">Minimum supported server</span></span><br/> | <span data-ttu-id="17fa7-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17fa7-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17fa7-280">命名空間</span><span class="sxs-lookup"><span data-stu-id="17fa7-280">Namespace</span></span><br/>                | <span data-ttu-id="17fa7-281">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17fa7-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17fa7-282">MOF</span><span class="sxs-lookup"><span data-stu-id="17fa7-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17fa7-283"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="17fa7-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17fa7-284">DLL</span><span class="sxs-lookup"><span data-stu-id="17fa7-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17fa7-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fa7-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fa7-286">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17fa7-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fa7-287">**CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="17fa7-287">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

