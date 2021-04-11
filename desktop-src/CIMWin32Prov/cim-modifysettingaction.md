---
description: CIM \_ ModifySettingAction 類別代表針對特定專案（具有特定值）修改特定設定檔案的資訊。
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: CIM_ModifySettingAction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689023"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="e597a-103">CIM \_ ModifySettingAction 類別</span><span class="sxs-lookup"><span data-stu-id="e597a-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="e597a-104">**CIM \_ ModifySettingAction** 類別代表針對特定專案（具有特定值）修改特定設定檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="e597a-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e597a-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e597a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e597a-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e597a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e597a-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e597a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e597a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e597a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e597a-109">語法</span><span class="sxs-lookup"><span data-stu-id="e597a-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
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
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="e597a-110">成員</span><span class="sxs-lookup"><span data-stu-id="e597a-110">Members</span></span>

<span data-ttu-id="e597a-111">**CIM \_ ModifySettingAction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e597a-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="e597a-112">方法</span><span class="sxs-lookup"><span data-stu-id="e597a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e597a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e597a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e597a-114">方法</span><span class="sxs-lookup"><span data-stu-id="e597a-114">Methods</span></span>

<span data-ttu-id="e597a-115">**CIM \_ ModifySettingAction** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e597a-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="e597a-116">方法</span><span class="sxs-lookup"><span data-stu-id="e597a-116">Method</span></span>                                                           | <span data-ttu-id="e597a-117">描述</span><span class="sxs-lookup"><span data-stu-id="e597a-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="e597a-118">**調用**</span><span class="sxs-lookup"><span data-stu-id="e597a-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="e597a-119">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="e597a-119">Takes a specific action.</span></span> <span data-ttu-id="e597a-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e597a-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e597a-121">屬性</span><span class="sxs-lookup"><span data-stu-id="e597a-121">Properties</span></span>

<span data-ttu-id="e597a-122">**CIM \_ ModifySettingAction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e597a-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e597a-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="e597a-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-126">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e597a-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-127">指派給軟體元素特定動作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e597a-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="e597a-128">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-129">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="e597a-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e597a-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-132">要在指定的設定專案上執行的動作類型。</span><span class="sxs-lookup"><span data-stu-id="e597a-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="e597a-133">系統會假設新增專案區分大小寫;不過，移除會假設為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e597a-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="e597a-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**建立** (0) </span><span class="sxs-lookup"><span data-stu-id="e597a-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-135">建立指定的專案。</span><span class="sxs-lookup"><span data-stu-id="e597a-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="e597a-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**刪除** (1) </span><span class="sxs-lookup"><span data-stu-id="e597a-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-137">刪除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="e597a-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="e597a-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**附加** (2) </span><span class="sxs-lookup"><span data-stu-id="e597a-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-139">附加至指定專案的結尾。</span><span class="sxs-lookup"><span data-stu-id="e597a-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="e597a-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**移除** (3) </span><span class="sxs-lookup"><span data-stu-id="e597a-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-141">從指定的專案中移除值。</span><span class="sxs-lookup"><span data-stu-id="e597a-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-142">**標題**</span><span class="sxs-lookup"><span data-stu-id="e597a-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-145">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="e597a-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-146">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="e597a-146">Short textual description of the object.</span></span>

<span data-ttu-id="e597a-147">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-148">**說明**</span><span class="sxs-lookup"><span data-stu-id="e597a-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-151">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e597a-151">Description of the object.</span></span>

<span data-ttu-id="e597a-152">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-153">[方向]</span><span class="sxs-lookup"><span data-stu-id="e597a-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e597a-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-156">指出特定 [**CIM \_ 動作**](cim-action.md) 物件是否為一連串動作的一部分，以將目前的軟體專案轉換為下一個狀態，例如 "Install"，或移除目前的 software 元素，例如 "Uninstall"。</span><span class="sxs-lookup"><span data-stu-id="e597a-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="e597a-157">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="e597a-158">**安裝** (0) </span><span class="sxs-lookup"><span data-stu-id="e597a-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="e597a-159">**卸載** (1) </span><span class="sxs-lookup"><span data-stu-id="e597a-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-160">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="e597a-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-163">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e597a-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-164">要修改之專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e597a-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-165">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="e597a-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e597a-168">要加入、附加或取代指定設定的值。</span><span class="sxs-lookup"><span data-stu-id="e597a-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="e597a-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-172">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="e597a-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-173">要修改之設定檔案專案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e597a-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-174">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e597a-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-177">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e597a-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-178">識別軟體元素。</span><span class="sxs-lookup"><span data-stu-id="e597a-178">Identifies the software element.</span></span>

<span data-ttu-id="e597a-179">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-180">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="e597a-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-183">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e597a-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-184">要修改之設定專案的區段索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e597a-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="e597a-185">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="e597a-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-188">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="e597a-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-189">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e597a-189">Identifier for the software element.</span></span>

<span data-ttu-id="e597a-190">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="e597a-191">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="e597a-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-192">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e597a-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-194">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e597a-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e597a-195">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="e597a-195">State of a software element.</span></span>

<span data-ttu-id="e597a-196">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="e597a-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e597a-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-198">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="e597a-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="e597a-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="e597a-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-200">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="e597a-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="e597a-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="e597a-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-202">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="e597a-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="e597a-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="e597a-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-204">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e597a-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-205">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="e597a-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-206">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e597a-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-208">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="e597a-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-209">擁有軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="e597a-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="e597a-210">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e597a-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e597a-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e597a-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e597a-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="e597a-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="e597a-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-214">Mac OS</span><span class="sxs-lookup"><span data-stu-id="e597a-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="e597a-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="e597a-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="e597a-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="e597a-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="e597a-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="e597a-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="e597a-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="e597a-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="e597a-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="e597a-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-220">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="e597a-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="e597a-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="e597a-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="e597a-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="e597a-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="e597a-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="e597a-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="e597a-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="e597a-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="e597a-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="e597a-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="e597a-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="e597a-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="e597a-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-228">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="e597a-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="e597a-229"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="e597a-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="e597a-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="e597a-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-231">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="e597a-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="e597a-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="e597a-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="e597a-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="e597a-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="e597a-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e597a-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="e597a-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="e597a-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="e597a-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="e597a-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="e597a-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="e597a-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="e597a-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="e597a-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-241">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="e597a-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="e597a-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="e597a-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="e597a-243"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="e597a-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="e597a-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="e597a-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="e597a-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="e597a-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="e597a-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="e597a-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="e597a-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="e597a-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="e597a-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="e597a-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="e597a-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="e597a-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="e597a-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="e597a-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="e597a-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="e597a-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="e597a-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="e597a-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="e597a-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="e597a-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-254">系列</span><span class="sxs-lookup"><span data-stu-id="e597a-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="e597a-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="e597a-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-256">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="e597a-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="e597a-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="e597a-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-258">將 NT</span><span class="sxs-lookup"><span data-stu-id="e597a-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="e597a-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="e597a-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="e597a-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="e597a-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="e597a-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="e597a-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="e597a-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="e597a-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="e597a-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="e597a-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="e597a-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="e597a-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="e597a-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="e597a-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="e597a-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-267">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="e597a-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="e597a-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="e597a-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="e597a-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="e597a-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="e597a-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="e597a-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="e597a-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="e597a-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="e597a-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="e597a-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="e597a-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="e597a-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="e597a-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="e597a-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="e597a-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="e597a-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="e597a-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="e597a-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="e597a-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="e597a-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="e597a-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="e597a-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="e597a-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="e597a-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="e597a-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-281">為 OS</span><span class="sxs-lookup"><span data-stu-id="e597a-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="e597a-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="e597a-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="e597a-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="e597a-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="e597a-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="e597a-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="e597a-285">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="e597a-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="e597a-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="e597a-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="e597a-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="e597a-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="e597a-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="e597a-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="e597a-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="e597a-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="e597a-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="e597a-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e597a-291">**版本**</span><span class="sxs-lookup"><span data-stu-id="e597a-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e597a-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e597a-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e597a-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e597a-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e597a-294">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="e597a-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="e597a-295">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="e597a-295">Version of the operation.</span></span>

<span data-ttu-id="e597a-296">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="e597a-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="e597a-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="e597a-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="e597a-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="e597a-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="e597a-299">這個屬性繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e597a-300">備註</span><span class="sxs-lookup"><span data-stu-id="e597a-300">Remarks</span></span>

<span data-ttu-id="e597a-301">**Cim \_ ModifySettingAction** 類別衍生自 [**cim \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="e597a-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="e597a-302">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="e597a-302">WMI does not implement this class.</span></span>

<span data-ttu-id="e597a-303">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e597a-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e597a-304">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e597a-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e597a-305">規格需求</span><span class="sxs-lookup"><span data-stu-id="e597a-305">Requirements</span></span>



| <span data-ttu-id="e597a-306">需求</span><span class="sxs-lookup"><span data-stu-id="e597a-306">Requirement</span></span> | <span data-ttu-id="e597a-307">值</span><span class="sxs-lookup"><span data-stu-id="e597a-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e597a-308">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e597a-308">Minimum supported client</span></span><br/> | <span data-ttu-id="e597a-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e597a-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e597a-310">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e597a-310">Minimum supported server</span></span><br/> | <span data-ttu-id="e597a-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e597a-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e597a-312">命名空間</span><span class="sxs-lookup"><span data-stu-id="e597a-312">Namespace</span></span><br/>                | <span data-ttu-id="e597a-313">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e597a-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e597a-314">MOF</span><span class="sxs-lookup"><span data-stu-id="e597a-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e597a-315"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e597a-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e597a-316">DLL</span><span class="sxs-lookup"><span data-stu-id="e597a-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e597a-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e597a-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e597a-318">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e597a-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e597a-319">**CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="e597a-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

