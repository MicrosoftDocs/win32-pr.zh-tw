---
description: CIM \_ CopyFileAction 類別代表將檔案從電腦系統移動或複製到新位置。
ms.assetid: c80b5002-d489-4b7e-b9a2-4460c3596958
ms.tgt_platform: multiple
title: CIM_CopyFileAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction
- CIM_CopyFileAction.ActionID
- CIM_CopyFileAction.Caption
- CIM_CopyFileAction.Description
- CIM_CopyFileAction.Direction
- CIM_CopyFileAction.Name
- CIM_CopyFileAction.SoftwareElementID
- CIM_CopyFileAction.SoftwareElementState
- CIM_CopyFileAction.TargetOperatingSystem
- CIM_CopyFileAction.Version
- CIM_CopyFileAction.DeleteAfterCopy
- CIM_CopyFileAction.Destination
- CIM_CopyFileAction.Source
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0303f4696d1baa5129d93cd2e6a7703be611ed9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973390"
---
# <a name="cim_copyfileaction-class"></a><span data-ttu-id="2c8ec-103">CIM \_ CopyFileAction 類別</span><span class="sxs-lookup"><span data-stu-id="2c8ec-103">CIM\_CopyFileAction class</span></span>

<span data-ttu-id="2c8ec-104">**CIM \_ CopyFileAction** 類別代表將檔案從電腦系統移動或複製到新位置。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-104">The **CIM\_CopyFileAction** class represents moving or copying files from a computer system to a new location.</span></span>

<span data-ttu-id="2c8ec-105">您可以使用 [**cim \_ ToDirectorySpecification**](cim-todirectoryspecification.md) 和 [**Cim \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) 關聯或 [**cim \_ ToDirectoryAction**](cim-todirectoryaction.md) 和 [**cim \_ FromDirectoryAction**](cim-fromdirectoryaction.md) 關聯來指定複製的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-105">Location information for copying is specified by using either the [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) and [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) associations, or the [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) and [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) associations.</span></span> <span data-ttu-id="2c8ec-106">第一個集合是在採取任何動作之前，當來源或目標存在時使用。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-106">The first set is used when the source or target are to exist before any actions are taken.</span></span> <span data-ttu-id="2c8ec-107">當來源或目標建立為先前動作的一部分時，就會使用第二個集合。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-107">The second set is used when the source or target are created as a part of a previous action.</span></span> <span data-ttu-id="2c8ec-108">在後者的情況下，建立目錄的動作必須在 **CIM \_ CopyFileAction** 物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-108">In the latter case, the action to create the directory must occur prior to the **CIM\_CopyFileAction** object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c8ec-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2c8ec-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2c8ec-111">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2c8ec-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8ec-113">語法</span><span class="sxs-lookup"><span data-stu-id="2c8ec-113">Syntax</span></span>

``` syntax
[UUID("{73553260-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CopyFileAction : CIM_FileAction
{
  string  ActionID;
  string  Caption;
  string  Description;
  uint16  Direction;
  string  Name;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
  boolean DeleteAfterCopy;
  string  Destination;
  string  Source;
};
```

## <a name="members"></a><span data-ttu-id="2c8ec-114">成員</span><span class="sxs-lookup"><span data-stu-id="2c8ec-114">Members</span></span>

<span data-ttu-id="2c8ec-115">**CIM \_ CopyFileAction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2c8ec-115">The **CIM\_CopyFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="2c8ec-116">方法</span><span class="sxs-lookup"><span data-stu-id="2c8ec-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c8ec-117">屬性</span><span class="sxs-lookup"><span data-stu-id="2c8ec-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c8ec-118">方法</span><span class="sxs-lookup"><span data-stu-id="2c8ec-118">Methods</span></span>

<span data-ttu-id="2c8ec-119">**CIM \_ CopyFileAction** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-119">The **CIM\_CopyFileAction** class has these methods.</span></span>



| <span data-ttu-id="2c8ec-120">方法</span><span class="sxs-lookup"><span data-stu-id="2c8ec-120">Method</span></span>                                                      | <span data-ttu-id="2c8ec-121">描述</span><span class="sxs-lookup"><span data-stu-id="2c8ec-121">Description</span></span>                                                                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c8ec-122">**調用**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-122">**Invoke**</span></span>](invoke-method-in-class-cim-copyfileaction.md) | <span data-ttu-id="2c8ec-123">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-123">Takes a particular action.</span></span> <span data-ttu-id="2c8ec-124">方法執行動作的詳細資料是實作為特定的。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-124">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="2c8ec-125">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2c8ec-126">屬性</span><span class="sxs-lookup"><span data-stu-id="2c8ec-126">Properties</span></span>

<span data-ttu-id="2c8ec-127">**CIM \_ CopyFileAction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-127">The **CIM\_CopyFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c8ec-128">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-128">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-131">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-132">指派給軟體元素特定動作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-132">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="2c8ec-133">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-133">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-134">**標題**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-137">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-137">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-138">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-138">Short textual description of the object.</span></span>

<span data-ttu-id="2c8ec-139">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-140">**DeleteAfterCopy**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-140">**DeleteAfterCopy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-141">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-143">若 **為 TRUE**，則會在複製作業之後刪除原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-143">If **TRUE**, the source file is deleted after the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-144">**說明**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-147">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-147">Description of the object.</span></span>

<span data-ttu-id="2c8ec-148">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-149">**目的地**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-149">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-152">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-153">完整的目的地檔案名。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-153">Fully qualified destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-154">[方向]</span><span class="sxs-lookup"><span data-stu-id="2c8ec-154">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-157">指出特定 [**CIM \_ 動作**](cim-action.md) 物件是否為一連串動作的一部分，以將目前的軟體專案轉換為下一個狀態，例如 "Install"，或移除目前的 software 元素，例如 "Uninstall"。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-157">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="2c8ec-158">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-158">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="2c8ec-159">**安裝** (0) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-159">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="2c8ec-160">**卸載** (1) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-160">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c8ec-161">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-164">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-164">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-165">識別軟體元素。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-165">Identifies the software element.</span></span>

<span data-ttu-id="2c8ec-166">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-166">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-167">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-167">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-170">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-170">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-171">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-171">Identifier for the software element.</span></span>

<span data-ttu-id="2c8ec-172">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-172">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-173">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-173">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-174">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-176">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2c8ec-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-177">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-177">State of a software element.</span></span>

<span data-ttu-id="2c8ec-178">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-178">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="2c8ec-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-180">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-180">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="2c8ec-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-182">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-182">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="2c8ec-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-184">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-184">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="2c8ec-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-186">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-186">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2c8ec-187">**來源**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-187">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-190">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-190">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-191">完整的原始碼檔案名。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-191">Fully qualified source file name.</span></span>

</dd> <dt>

<span data-ttu-id="2c8ec-192">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-192">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-195">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="2c8ec-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-196">擁有軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-196">Target operating system of the owning software element.</span></span>

<span data-ttu-id="2c8ec-197">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-197">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c8ec-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2c8ec-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="2c8ec-200"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-200"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-201">Mac OS</span><span class="sxs-lookup"><span data-stu-id="2c8ec-201">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="2c8ec-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="2c8ec-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="2c8ec-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="2c8ec-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="2c8ec-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-207">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="2c8ec-207">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="2c8ec-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-209">HP-UX</span><span class="sxs-lookup"><span data-stu-id="2c8ec-209">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="2c8ec-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="2c8ec-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="2c8ec-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="2c8ec-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="2c8ec-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-215">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-215">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="2c8ec-216"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="2c8ec-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-218">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="2c8ec-218">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="2c8ec-219"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-219"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-220">Windows 95</span><span class="sxs-lookup"><span data-stu-id="2c8ec-220">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="2c8ec-221"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-221"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-222">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2c8ec-222">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="2c8ec-223"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-223"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-224">Windows NT</span><span class="sxs-lookup"><span data-stu-id="2c8ec-224">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="2c8ec-225"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-225"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-226">Windows CE</span><span class="sxs-lookup"><span data-stu-id="2c8ec-226">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="2c8ec-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-228">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="2c8ec-228">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="2c8ec-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="2c8ec-230"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="2c8ec-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="2c8ec-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="2c8ec-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="2c8ec-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="2c8ec-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="2c8ec-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="2c8ec-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="2c8ec-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="2c8ec-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="2c8ec-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-241">系列</span><span class="sxs-lookup"><span data-stu-id="2c8ec-241">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="2c8ec-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-243">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="2c8ec-243">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="2c8ec-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-245">將 NT</span><span class="sxs-lookup"><span data-stu-id="2c8ec-245">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="2c8ec-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-247">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="2c8ec-247">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="2c8ec-248"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-248"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="2c8ec-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="2c8ec-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="2c8ec-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="2c8ec-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="2c8ec-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-254">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="2c8ec-254">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="2c8ec-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="2c8ec-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="2c8ec-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="2c8ec-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-259">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="2c8ec-259">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="2c8ec-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="2c8ec-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="2c8ec-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="2c8ec-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="2c8ec-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="2c8ec-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="2c8ec-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="2c8ec-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-268">為 OS</span><span class="sxs-lookup"><span data-stu-id="2c8ec-268">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="2c8ec-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="2c8ec-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="2c8ec-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="2c8ec-272">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="2c8ec-272">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="2c8ec-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="2c8ec-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="2c8ec-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="2c8ec-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="2c8ec-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="2c8ec-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2c8ec-278">**版本**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-278">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c8ec-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2c8ec-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c8ec-281">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="2c8ec-281">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2c8ec-282">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-282">Version of the operation.</span></span>

<span data-ttu-id="2c8ec-283">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="2c8ec-283">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="2c8ec-284"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="2c8ec-284"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="2c8ec-285"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="2c8ec-285"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="2c8ec-286">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-286">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c8ec-287">備註</span><span class="sxs-lookup"><span data-stu-id="2c8ec-287">Remarks</span></span>

<span data-ttu-id="2c8ec-288">**Cim \_ CopyFileAction** 類別衍生自 [**cim \_ FileAction**](cim-fileaction.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-288">The **CIM\_CopyFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="2c8ec-289">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-289">WMI does not implement this class.</span></span> <span data-ttu-id="2c8ec-290">如需衍生自 **CIM \_ CopyFileAction** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-290">For more information about classes derived from **CIM\_CopyFileAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2c8ec-291">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-291">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2c8ec-292">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2c8ec-292">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8ec-293">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c8ec-293">Requirements</span></span>



| <span data-ttu-id="2c8ec-294">需求</span><span class="sxs-lookup"><span data-stu-id="2c8ec-294">Requirement</span></span> | <span data-ttu-id="2c8ec-295">值</span><span class="sxs-lookup"><span data-stu-id="2c8ec-295">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8ec-296">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c8ec-296">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8ec-297">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c8ec-297">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c8ec-298">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c8ec-298">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8ec-299">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c8ec-299">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c8ec-300">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c8ec-300">Namespace</span></span><br/>                | <span data-ttu-id="2c8ec-301">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2c8ec-301">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c8ec-302">MOF</span><span class="sxs-lookup"><span data-stu-id="2c8ec-302">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c8ec-303"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c8ec-303"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c8ec-304">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8ec-304">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8ec-305"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8ec-305"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8ec-306">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c8ec-306">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8ec-307">**CIM \_ FileAction**</span><span class="sxs-lookup"><span data-stu-id="2c8ec-307">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

