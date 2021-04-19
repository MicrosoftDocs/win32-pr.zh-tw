---
description: CIM \_ SettingCheck 類別會指定針對包含值等於指定值的特定專案檢查特定設定檔案所需的資訊。 所有的比較都會假設為不區分大小寫。
ms.assetid: 0e40276c-e794-4ea1-8937-c6d7f110f97d
ms.tgt_platform: multiple
title: CIM_SettingCheck 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck
- CIM_SettingCheck.Caption
- CIM_SettingCheck.CheckID
- CIM_SettingCheck.CheckMode
- CIM_SettingCheck.CheckType
- CIM_SettingCheck.Description
- CIM_SettingCheck.EntryName
- CIM_SettingCheck.EntryValue
- CIM_SettingCheck.FileName
- CIM_SettingCheck.Name
- CIM_SettingCheck.SectionKey
- CIM_SettingCheck.SoftwareElementID
- CIM_SettingCheck.SoftwareElementState
- CIM_SettingCheck.TargetOperatingSystem
- CIM_SettingCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4b360833f216d9feb839a4ed84a0e1ba4cd61ebf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972130"
---
# <a name="cim_settingcheck-class"></a><span data-ttu-id="145c5-104">CIM \_ SettingCheck 類別</span><span class="sxs-lookup"><span data-stu-id="145c5-104">CIM\_SettingCheck class</span></span>

<span data-ttu-id="145c5-105">**CIM \_ SettingCheck** 類別會指定針對包含值等於指定值的特定專案檢查特定設定檔案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="145c5-105">The **CIM\_SettingCheck** class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="145c5-106">所有的比較都會假設為不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="145c5-106">All comparisons are assumed to be case insensitive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="145c5-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="145c5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="145c5-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="145c5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="145c5-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="145c5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="145c5-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="145c5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="145c5-111">語法</span><span class="sxs-lookup"><span data-stu-id="145c5-111">Syntax</span></span>

``` syntax
[UUID("{DC1D8140-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SettingCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  uint16  CheckType;
  string  Description;
  string  EntryName;
  string  EntryValue;
  string  FileName;
  string  Name;
  string  SectionKey;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="145c5-112">成員</span><span class="sxs-lookup"><span data-stu-id="145c5-112">Members</span></span>

<span data-ttu-id="145c5-113">**CIM \_ SettingCheck** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="145c5-113">The **CIM\_SettingCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="145c5-114">方法</span><span class="sxs-lookup"><span data-stu-id="145c5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="145c5-115">屬性</span><span class="sxs-lookup"><span data-stu-id="145c5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="145c5-116">方法</span><span class="sxs-lookup"><span data-stu-id="145c5-116">Methods</span></span>

<span data-ttu-id="145c5-117">**CIM \_ SettingCheck** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="145c5-117">The **CIM\_SettingCheck** class has these methods.</span></span>



| <span data-ttu-id="145c5-118">方法</span><span class="sxs-lookup"><span data-stu-id="145c5-118">Method</span></span>                                                    | <span data-ttu-id="145c5-119">描述</span><span class="sxs-lookup"><span data-stu-id="145c5-119">Description</span></span>                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="145c5-120">**調用**</span><span class="sxs-lookup"><span data-stu-id="145c5-120">**Invoke**</span></span>](invoke-method-in-class-cim-settingcheck.md) | <span data-ttu-id="145c5-121">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="145c5-121">Takes a particular action.</span></span> <span data-ttu-id="145c5-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="145c5-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="145c5-123">屬性</span><span class="sxs-lookup"><span data-stu-id="145c5-123">Properties</span></span>

<span data-ttu-id="145c5-124">**CIM \_ SettingCheck** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="145c5-124">The **CIM\_SettingCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="145c5-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="145c5-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-128">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="145c5-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-129">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="145c5-129">Short textual description of the object.</span></span>

<span data-ttu-id="145c5-130">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="145c5-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="145c5-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-134">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="145c5-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-135">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="145c5-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span> <span data-ttu-id="145c5-136">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="145c5-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="145c5-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="145c5-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145c5-140">若 **為 TRUE**，則條件應該存在於環境中 (例如，如果檔案是在系統上，則叫 [**用方法應該**](invoke-method-in-class-cim-settingcheck.md) 會傳回 **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="145c5-140">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-settingcheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="145c5-141">如果 **為 FALSE**，則條件不應該存在 (例如，如果檔案不在系統上，則叫用 **方法應該** 會傳回 **FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="145c5-141">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="145c5-142">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="145c5-143">**CheckType**</span><span class="sxs-lookup"><span data-stu-id="145c5-143">**CheckType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="145c5-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145c5-146">設定值的比較方式。</span><span class="sxs-lookup"><span data-stu-id="145c5-146">Way in which the setting value should be compared.</span></span>

<dt>

<span id="Matches"></span><span id="matches"></span><span id="MATCHES"></span>

<span data-ttu-id="145c5-147">**符合** (0) </span><span class="sxs-lookup"><span data-stu-id="145c5-147">**Matches** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Contains"></span><span id="contains"></span><span id="CONTAINS"></span>

<span data-ttu-id="145c5-148">**包含** (1) </span><span class="sxs-lookup"><span data-stu-id="145c5-148">**Contains** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="145c5-149">**說明**</span><span class="sxs-lookup"><span data-stu-id="145c5-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145c5-152">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="145c5-152">Description of the object.</span></span>

<span data-ttu-id="145c5-153">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-153">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="145c5-154">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="145c5-154">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-157">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="145c5-157">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-158">要檢查之專案的名稱</span><span class="sxs-lookup"><span data-stu-id="145c5-158">Name of the entry to be checked</span></span>

</dd> <dt>

<span data-ttu-id="145c5-159">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="145c5-159">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="145c5-162">與要檢查的已命名專案相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="145c5-162">Value that is associated with the named entry to check.</span></span>

</dd> <dt>

<span data-ttu-id="145c5-163">**FileName**</span><span class="sxs-lookup"><span data-stu-id="145c5-163">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-166">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="145c5-166">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-167">要檢查之設定檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="145c5-167">File name of the setting file to check.</span></span>

</dd> <dt>

<span data-ttu-id="145c5-168">**名稱**</span><span class="sxs-lookup"><span data-stu-id="145c5-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-171">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="145c5-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-172">用來識別軟體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="145c5-172">Name used to identify the software element.</span></span> <span data-ttu-id="145c5-173">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="145c5-174">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="145c5-174">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-177">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="145c5-177">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-178">區段的索引鍵，其中包含要檢查的設定。</span><span class="sxs-lookup"><span data-stu-id="145c5-178">Key of section that contains the settings to check.</span></span>

</dd> <dt>

<span data-ttu-id="145c5-179">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="145c5-179">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-182">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="145c5-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-183">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="145c5-183">Identifier for the software element.</span></span>

<span data-ttu-id="145c5-184">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-184">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="145c5-185">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="145c5-185">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-186">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="145c5-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-188">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="145c5-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="145c5-189">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="145c5-189">State of a software element.</span></span>

<span data-ttu-id="145c5-190">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-190">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="145c5-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="145c5-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-192">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="145c5-192">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="145c5-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="145c5-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-194">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="145c5-194">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="145c5-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="145c5-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-196">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="145c5-196">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="145c5-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="145c5-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-198">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="145c5-198">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="145c5-199">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="145c5-199">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-200">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="145c5-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-202">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="145c5-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="145c5-203">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="145c5-203">Target operating system of the software element.</span></span>

<span data-ttu-id="145c5-204">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="145c5-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="145c5-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="145c5-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="145c5-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="145c5-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="145c5-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="145c5-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-208">Mac OS</span><span class="sxs-lookup"><span data-stu-id="145c5-208">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="145c5-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="145c5-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-210">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="145c5-210">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="145c5-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="145c5-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="145c5-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="145c5-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="145c5-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="145c5-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="145c5-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="145c5-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-215">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="145c5-215">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="145c5-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="145c5-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-217">HP-UX</span><span class="sxs-lookup"><span data-stu-id="145c5-217">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="145c5-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="145c5-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="145c5-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="145c5-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="145c5-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="145c5-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="145c5-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="145c5-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="145c5-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="145c5-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-223">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="145c5-223">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="145c5-224"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="145c5-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="145c5-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="145c5-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-226">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="145c5-226">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="145c5-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="145c5-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-228">Windows 95</span><span class="sxs-lookup"><span data-stu-id="145c5-228">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="145c5-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="145c5-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-230">Windows 98</span><span class="sxs-lookup"><span data-stu-id="145c5-230">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="145c5-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="145c5-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-232">Windows NT</span><span class="sxs-lookup"><span data-stu-id="145c5-232">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="145c5-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="145c5-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-234">Windows CE</span><span class="sxs-lookup"><span data-stu-id="145c5-234">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="145c5-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="145c5-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-236">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="145c5-236">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="145c5-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="145c5-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="145c5-238"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="145c5-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="145c5-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="145c5-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="145c5-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="145c5-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="145c5-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="145c5-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="145c5-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="145c5-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="145c5-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="145c5-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="145c5-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="145c5-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="145c5-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="145c5-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="145c5-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="145c5-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="145c5-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="145c5-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="145c5-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="145c5-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-249">系列</span><span class="sxs-lookup"><span data-stu-id="145c5-249">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="145c5-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="145c5-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-251">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="145c5-251">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="145c5-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="145c5-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-253">將 NT</span><span class="sxs-lookup"><span data-stu-id="145c5-253">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="145c5-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="145c5-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-255">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="145c5-255">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="145c5-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="145c5-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="145c5-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="145c5-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="145c5-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="145c5-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="145c5-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="145c5-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="145c5-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="145c5-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="145c5-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="145c5-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-262">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="145c5-262">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="145c5-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="145c5-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="145c5-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="145c5-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="145c5-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="145c5-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="145c5-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="145c5-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-267">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="145c5-267">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="145c5-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="145c5-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="145c5-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="145c5-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="145c5-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="145c5-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="145c5-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="145c5-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="145c5-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="145c5-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="145c5-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="145c5-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="145c5-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="145c5-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="145c5-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="145c5-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="145c5-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="145c5-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="145c5-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="145c5-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="145c5-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="145c5-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="145c5-279">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="145c5-279">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="145c5-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="145c5-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="145c5-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="145c5-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="145c5-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="145c5-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="145c5-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="145c5-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="145c5-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="145c5-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="145c5-285">**版本**</span><span class="sxs-lookup"><span data-stu-id="145c5-285">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="145c5-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="145c5-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="145c5-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="145c5-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="145c5-288">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="145c5-288">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="145c5-289">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="145c5-289">Version of the operation.</span></span>

<span data-ttu-id="145c5-290">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="145c5-290">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="145c5-291"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="145c5-291"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="145c5-292"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="145c5-292"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="145c5-293">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="145c5-293">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="145c5-294">備註</span><span class="sxs-lookup"><span data-stu-id="145c5-294">Remarks</span></span>

<span data-ttu-id="145c5-295">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="145c5-295">WMI does not implement this class.</span></span>

<span data-ttu-id="145c5-296">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="145c5-296">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="145c5-297">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="145c5-297">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="145c5-298">規格需求</span><span class="sxs-lookup"><span data-stu-id="145c5-298">Requirements</span></span>



| <span data-ttu-id="145c5-299">需求</span><span class="sxs-lookup"><span data-stu-id="145c5-299">Requirement</span></span> | <span data-ttu-id="145c5-300">值</span><span class="sxs-lookup"><span data-stu-id="145c5-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="145c5-301">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="145c5-301">Minimum supported client</span></span><br/> | <span data-ttu-id="145c5-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="145c5-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="145c5-303">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="145c5-303">Minimum supported server</span></span><br/> | <span data-ttu-id="145c5-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="145c5-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="145c5-305">命名空間</span><span class="sxs-lookup"><span data-stu-id="145c5-305">Namespace</span></span><br/>                | <span data-ttu-id="145c5-306">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="145c5-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="145c5-307">MOF</span><span class="sxs-lookup"><span data-stu-id="145c5-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="145c5-308"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="145c5-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="145c5-309">DLL</span><span class="sxs-lookup"><span data-stu-id="145c5-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="145c5-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="145c5-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="145c5-311">另請參閱</span><span class="sxs-lookup"><span data-stu-id="145c5-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145c5-312">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="145c5-312">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

