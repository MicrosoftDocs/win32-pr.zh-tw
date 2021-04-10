---
description: CIM \_ SoftwareElementVersionCheck 類別代表必須存在於環境中的 software 元素類型。
ms.assetid: a1c0f0d5-2586-499c-bd82-bbb107570d81
ms.tgt_platform: multiple
title: CIM_SoftwareElementVersionCheck 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementVersionCheck
- CIM_SoftwareElementVersionCheck.Caption
- CIM_SoftwareElementVersionCheck.CheckID
- CIM_SoftwareElementVersionCheck.CheckMode
- CIM_SoftwareElementVersionCheck.Description
- CIM_SoftwareElementVersionCheck.LowerSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Name
- CIM_SoftwareElementVersionCheck.SoftwareElementID
- CIM_SoftwareElementVersionCheck.SoftwareElementName
- CIM_SoftwareElementVersionCheck.SoftwareElementState
- CIM_SoftwareElementVersionCheck.SoftwareElementStateDesired
- CIM_SoftwareElementVersionCheck.TargetOperatingSystem
- CIM_SoftwareElementVersionCheck.TargetOperatingSystemDesired
- CIM_SoftwareElementVersionCheck.UpperSoftwareElementVersion
- CIM_SoftwareElementVersionCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb55a44a3aba9092567cdc91b668ba1b63e33174
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187604"
---
# <a name="cim_softwareelementversioncheck-class"></a><span data-ttu-id="3bcde-103">CIM \_ SoftwareElementVersionCheck 類別</span><span class="sxs-lookup"><span data-stu-id="3bcde-103">CIM\_SoftwareElementVersionCheck class</span></span>

<span data-ttu-id="3bcde-104">**CIM \_ SoftwareElementVersionCheck** 類別代表必須存在於環境中的 software 元素類型。</span><span class="sxs-lookup"><span data-stu-id="3bcde-104">The **CIM\_SoftwareElementVersionCheck** class represents a type of software element that must exist in the environment.</span></span> <span data-ttu-id="3bcde-105">這項檢查可以是特定、最小值、最大值或版本範圍。</span><span class="sxs-lookup"><span data-stu-id="3bcde-105">This check can be for a specific, minimum, maximum, or a range of versions.</span></span> <span data-ttu-id="3bcde-106">若要指定特定版本，則較低和最高版本必須相同。</span><span class="sxs-lookup"><span data-stu-id="3bcde-106">To specify a specific version, the lower and upper versions must be the same.</span></span> <span data-ttu-id="3bcde-107">若要指定最小版本，請只指定較低的版本。</span><span class="sxs-lookup"><span data-stu-id="3bcde-107">To specify a minimum version, specify only the lower version.</span></span> <span data-ttu-id="3bcde-108">若要指定最大版本，請僅指定最高版本。</span><span class="sxs-lookup"><span data-stu-id="3bcde-108">To specify a maximum version, specify only the upper version.</span></span> <span data-ttu-id="3bcde-109">若要指定範圍，必須指定上限和較低的版本。</span><span class="sxs-lookup"><span data-stu-id="3bcde-109">To specify a range, both upper and lower versions must be specified.</span></span> <span data-ttu-id="3bcde-110">檢查的詳細資料會與 cim SoftwareElement 物件（cim [**\_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)關聯）所 [**參考的 cim \_**](cim-computersystem.md) [**\_**](cim-softwareelement.md)物件中所找到的對應詳細資料進行比較。</span><span class="sxs-lookup"><span data-stu-id="3bcde-110">Details of the checks are compared with the corresponding details found in a [**CIM\_SoftwareElement**](cim-softwareelement.md) object referenced by a [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object.</span></span> <span data-ttu-id="3bcde-111">至少有一個 **CIM \_ SoftwareElement** 需要滿足要滿足的檢查條件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bcde-111">At least one **CIM\_SoftwareElement** needs to satisfy the details of the condition for the check to be satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bcde-112">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="3bcde-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3bcde-113">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3bcde-114">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3bcde-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3bcde-115">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3bcde-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bcde-116">語法</span><span class="sxs-lookup"><span data-stu-id="3bcde-116">Syntax</span></span>

``` syntax
[UUID("{4D23FBD0-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareElementVersionCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  string  Description;
  string  LowerSoftwareElementVersion;
  string  Name;
  string  SoftwareElementID;
  string  SoftwareElementName;
  uint16  SoftwareElementState;
  uint16  SoftwareElementStateDesired;
  uint16  TargetOperatingSystem;
  uint16  TargetOperatingSystemDesired;
  string  UpperSoftwareElementVersion;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="3bcde-117">成員</span><span class="sxs-lookup"><span data-stu-id="3bcde-117">Members</span></span>

<span data-ttu-id="3bcde-118">**CIM \_ SoftwareElementVersionCheck** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3bcde-118">The **CIM\_SoftwareElementVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="3bcde-119">方法</span><span class="sxs-lookup"><span data-stu-id="3bcde-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="3bcde-120">屬性</span><span class="sxs-lookup"><span data-stu-id="3bcde-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3bcde-121">方法</span><span class="sxs-lookup"><span data-stu-id="3bcde-121">Methods</span></span>

<span data-ttu-id="3bcde-122">**CIM \_ SoftwareElementVersionCheck** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3bcde-122">The **CIM\_SoftwareElementVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="3bcde-123">方法</span><span class="sxs-lookup"><span data-stu-id="3bcde-123">Method</span></span>                                                                   | <span data-ttu-id="3bcde-124">描述</span><span class="sxs-lookup"><span data-stu-id="3bcde-124">Description</span></span>                                                   |
|:-------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="3bcde-125">**調用**</span><span class="sxs-lookup"><span data-stu-id="3bcde-125">**Invoke**</span></span>](invoke-method-in-class-cim-softwareelementversioncheck.md) | <span data-ttu-id="3bcde-126">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="3bcde-126">Takes a particular action.</span></span> <span data-ttu-id="3bcde-127">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="3bcde-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3bcde-128">屬性</span><span class="sxs-lookup"><span data-stu-id="3bcde-128">Properties</span></span>

<span data-ttu-id="3bcde-129">**CIM \_ SoftwareElementVersionCheck** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3bcde-129">The **CIM\_SoftwareElementVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bcde-130">**標題**</span><span class="sxs-lookup"><span data-stu-id="3bcde-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-133">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="3bcde-133">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-134">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="3bcde-134">Short textual description of the object.</span></span>

<span data-ttu-id="3bcde-135">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-135">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-136">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="3bcde-136">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-139">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3bcde-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-140">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bcde-140">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="3bcde-141">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-141">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-142">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="3bcde-142">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-143">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3bcde-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-145">若 **為 TRUE**，則條件應該存在於環境中 (例如，如果檔案是在系統上，則叫 [**用方法應該**](invoke-method-in-class-cim-softwareelementversioncheck.md) 會傳回 **TRUE**) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-145">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-softwareelementversioncheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="3bcde-146">如果 **為 FALSE**，則條件不應該存在 (例如，如果檔案不在系統上，則叫用 **方法應該** 會傳回 **FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-146">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="3bcde-147">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-147">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-148">**說明**</span><span class="sxs-lookup"><span data-stu-id="3bcde-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-151">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3bcde-151">Description of the object.</span></span>

<span data-ttu-id="3bcde-152">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-153">**LowerSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="3bcde-153">**LowerSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-156">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**版本**") </span><span class="sxs-lookup"><span data-stu-id="3bcde-156">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-157">要檢查的軟體專案的最小版本。</span><span class="sxs-lookup"><span data-stu-id="3bcde-157">Minimum version of a software elements being checked.</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3bcde-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-161">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3bcde-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-162">用來識別軟體元素的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bcde-162">Name used to identify the software element.</span></span>

<span data-ttu-id="3bcde-163">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-163">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-164">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="3bcde-164">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-167">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3bcde-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-168">Software 元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bcde-168">Identifier for the software element.</span></span>

<span data-ttu-id="3bcde-169">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-169">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-170">**SoftwareElementName**</span><span class="sxs-lookup"><span data-stu-id="3bcde-170">**SoftwareElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-173">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="3bcde-173">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-174">所檢查之軟體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bcde-174">Name of the software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-175">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="3bcde-175">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-176">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3bcde-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-178">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3bcde-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-179">軟體元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="3bcde-179">State of a software element.</span></span>

<span data-ttu-id="3bcde-180">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-180">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="3bcde-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3bcde-181"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-182">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-182">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="3bcde-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="3bcde-183"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-184">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-184">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="3bcde-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="3bcde-185"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-186">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-186">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="3bcde-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="3bcde-187"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-188">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bcde-188">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3bcde-189">**SoftwareElementStateDesired**</span><span class="sxs-lookup"><span data-stu-id="3bcde-189">**SoftwareElementStateDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3bcde-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-192">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") </span><span class="sxs-lookup"><span data-stu-id="3bcde-192">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-193">所檢查之軟體專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="3bcde-193">State of the software element being checked.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="3bcde-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3bcde-194"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-195">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-195">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="3bcde-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="3bcde-196"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-197">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-197">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="3bcde-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="3bcde-198"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-199">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="3bcde-199">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="3bcde-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="3bcde-200"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-201">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3bcde-201">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3bcde-202">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="3bcde-202">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-203">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3bcde-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-205">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="3bcde-205">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-206">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="3bcde-206">Target operating system of the software element.</span></span>

<span data-ttu-id="3bcde-207">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="3bcde-207">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3bcde-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3bcde-208"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3bcde-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3bcde-209"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="3bcde-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="3bcde-210"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-211">Mac OS</span><span class="sxs-lookup"><span data-stu-id="3bcde-211">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="3bcde-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="3bcde-212"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-213">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="3bcde-213">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="3bcde-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="3bcde-214"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="3bcde-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="3bcde-215"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="3bcde-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="3bcde-216"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="3bcde-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="3bcde-217"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-218">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="3bcde-218">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="3bcde-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="3bcde-219"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-220">HP-UX</span><span class="sxs-lookup"><span data-stu-id="3bcde-220">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="3bcde-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="3bcde-221"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="3bcde-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="3bcde-222"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="3bcde-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="3bcde-223"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="3bcde-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="3bcde-224"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="3bcde-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="3bcde-225"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-226">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="3bcde-226">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="3bcde-227"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="3bcde-227"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="3bcde-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="3bcde-228"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-229">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="3bcde-229">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="3bcde-230"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="3bcde-230"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-231">Windows 95</span><span class="sxs-lookup"><span data-stu-id="3bcde-231">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="3bcde-232"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="3bcde-232"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-233">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3bcde-233">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="3bcde-234"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="3bcde-234"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-235">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3bcde-235">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="3bcde-236"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="3bcde-236"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-237">Windows CE</span><span class="sxs-lookup"><span data-stu-id="3bcde-237">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="3bcde-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="3bcde-238"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-239">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="3bcde-239">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="3bcde-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="3bcde-240"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="3bcde-241"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="3bcde-241"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="3bcde-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="3bcde-242"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="3bcde-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="3bcde-243"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="3bcde-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="3bcde-244"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="3bcde-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="3bcde-245"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="3bcde-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="3bcde-246"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="3bcde-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="3bcde-247"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="3bcde-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="3bcde-248"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="3bcde-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="3bcde-249"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="3bcde-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="3bcde-250"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="3bcde-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="3bcde-251"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-252">系列</span><span class="sxs-lookup"><span data-stu-id="3bcde-252">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="3bcde-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="3bcde-253"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-254">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="3bcde-254">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="3bcde-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="3bcde-255"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-256">將 NT</span><span class="sxs-lookup"><span data-stu-id="3bcde-256">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="3bcde-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="3bcde-257"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-258">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="3bcde-258">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="3bcde-259"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="3bcde-259"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="3bcde-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="3bcde-260"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="3bcde-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="3bcde-261"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="3bcde-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="3bcde-262"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="3bcde-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="3bcde-263"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="3bcde-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="3bcde-264"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-265">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="3bcde-265">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="3bcde-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="3bcde-266"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="3bcde-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="3bcde-267"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="3bcde-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="3bcde-268"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="3bcde-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="3bcde-269"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-270">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="3bcde-270">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="3bcde-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="3bcde-271"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="3bcde-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="3bcde-272"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="3bcde-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="3bcde-273"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="3bcde-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="3bcde-274"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="3bcde-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="3bcde-275"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="3bcde-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="3bcde-276"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="3bcde-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="3bcde-277"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="3bcde-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="3bcde-278"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="3bcde-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="3bcde-279"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="3bcde-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="3bcde-280"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="3bcde-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="3bcde-281"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-282">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="3bcde-282">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="3bcde-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="3bcde-283"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="3bcde-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="3bcde-284"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="3bcde-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="3bcde-285"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="3bcde-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="3bcde-286"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="3bcde-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="3bcde-287"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3bcde-288">**TargetOperatingSystemDesired**</span><span class="sxs-lookup"><span data-stu-id="3bcde-288">**TargetOperatingSystemDesired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-289">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3bcde-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-291">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") </span><span class="sxs-lookup"><span data-stu-id="3bcde-291">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-292">要檢查之軟體元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="3bcde-292">Target operating system of the software element being checked.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3bcde-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3bcde-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3bcde-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="3bcde-294"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="3bcde-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="3bcde-295"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-296">Mac OS</span><span class="sxs-lookup"><span data-stu-id="3bcde-296">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="3bcde-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="3bcde-297"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-298">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="3bcde-298">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="3bcde-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="3bcde-299"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="3bcde-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="3bcde-300"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="3bcde-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="3bcde-301"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="3bcde-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="3bcde-302"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-303">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="3bcde-303">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="3bcde-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="3bcde-304"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-305">HP-UX</span><span class="sxs-lookup"><span data-stu-id="3bcde-305">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="3bcde-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="3bcde-306"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="3bcde-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="3bcde-307"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="3bcde-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="3bcde-308"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="3bcde-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="3bcde-309"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="3bcde-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="3bcde-310"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-311">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="3bcde-311">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="3bcde-312"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="3bcde-312"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="3bcde-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="3bcde-313"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-314">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="3bcde-314">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="3bcde-315"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="3bcde-315"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-316">Windows 95</span><span class="sxs-lookup"><span data-stu-id="3bcde-316">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="3bcde-317"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="3bcde-317"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-318">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3bcde-318">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="3bcde-319"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="3bcde-319"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-320">Windows NT</span><span class="sxs-lookup"><span data-stu-id="3bcde-320">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="3bcde-321"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="3bcde-321"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-322">Windows CE</span><span class="sxs-lookup"><span data-stu-id="3bcde-322">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="3bcde-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="3bcde-323"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-324">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="3bcde-324">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="3bcde-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="3bcde-325"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="3bcde-326"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="3bcde-326"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="3bcde-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="3bcde-327"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="3bcde-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="3bcde-328"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="3bcde-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="3bcde-329"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="3bcde-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="3bcde-330"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="3bcde-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="3bcde-331"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="3bcde-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="3bcde-332"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="3bcde-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="3bcde-333"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="3bcde-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="3bcde-334"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="3bcde-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="3bcde-335"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="3bcde-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="3bcde-336"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-337">系列</span><span class="sxs-lookup"><span data-stu-id="3bcde-337">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="3bcde-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="3bcde-338"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-339">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="3bcde-339">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="3bcde-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="3bcde-340"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-341">將 NT</span><span class="sxs-lookup"><span data-stu-id="3bcde-341">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="3bcde-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="3bcde-342"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-343">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="3bcde-343">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="3bcde-344"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="3bcde-344"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="3bcde-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="3bcde-345"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="3bcde-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="3bcde-346"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="3bcde-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="3bcde-347"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="3bcde-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="3bcde-348"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="3bcde-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="3bcde-349"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-350">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="3bcde-350">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="3bcde-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="3bcde-351"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="3bcde-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="3bcde-352"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="3bcde-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="3bcde-353"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="3bcde-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="3bcde-354"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-355">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="3bcde-355">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="3bcde-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="3bcde-356"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="3bcde-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="3bcde-357"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="3bcde-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="3bcde-358"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="3bcde-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="3bcde-359"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="3bcde-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="3bcde-360"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="3bcde-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="3bcde-361"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="3bcde-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="3bcde-362"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="3bcde-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="3bcde-363"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="3bcde-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="3bcde-364"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="3bcde-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="3bcde-365"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="3bcde-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="3bcde-366"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="3bcde-367">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="3bcde-367">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="3bcde-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="3bcde-368"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="3bcde-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="3bcde-369"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="3bcde-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="3bcde-370"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="3bcde-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="3bcde-371"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="3bcde-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="3bcde-372"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3bcde-373">**UpperSoftwareElementVersion**</span><span class="sxs-lookup"><span data-stu-id="3bcde-373">**UpperSoftwareElementVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-376">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**版本**") </span><span class="sxs-lookup"><span data-stu-id="3bcde-376">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-377">要檢查的軟體專案的最大版本。</span><span class="sxs-lookup"><span data-stu-id="3bcde-377">Maximum version of a software element being checked.</span></span>

</dd> <dt>

<span data-ttu-id="3bcde-378">**版本**</span><span class="sxs-lookup"><span data-stu-id="3bcde-378">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bcde-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3bcde-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3bcde-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bcde-381">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="3bcde-381">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3bcde-382">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="3bcde-382">Version of the operation.</span></span>

<span data-ttu-id="3bcde-383">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="3bcde-383">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="3bcde-384"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="3bcde-384"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="3bcde-385"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="3bcde-385"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="3bcde-386">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="3bcde-386">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bcde-387">備註</span><span class="sxs-lookup"><span data-stu-id="3bcde-387">Remarks</span></span>

<span data-ttu-id="3bcde-388">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="3bcde-388">WMI does not implement this class.</span></span>

<span data-ttu-id="3bcde-389">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="3bcde-389">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3bcde-390">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3bcde-390">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bcde-391">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bcde-391">Requirements</span></span>



| <span data-ttu-id="3bcde-392">需求</span><span class="sxs-lookup"><span data-stu-id="3bcde-392">Requirement</span></span> | <span data-ttu-id="3bcde-393">值</span><span class="sxs-lookup"><span data-stu-id="3bcde-393">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bcde-394">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bcde-394">Minimum supported client</span></span><br/> | <span data-ttu-id="3bcde-395">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bcde-395">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bcde-396">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bcde-396">Minimum supported server</span></span><br/> | <span data-ttu-id="3bcde-397">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bcde-397">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bcde-398">命名空間</span><span class="sxs-lookup"><span data-stu-id="3bcde-398">Namespace</span></span><br/>                | <span data-ttu-id="3bcde-399">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3bcde-399">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3bcde-400">MOF</span><span class="sxs-lookup"><span data-stu-id="3bcde-400">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bcde-401"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bcde-401"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bcde-402">DLL</span><span class="sxs-lookup"><span data-stu-id="3bcde-402">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bcde-403"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bcde-403"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bcde-404">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bcde-404">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bcde-405">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="3bcde-405">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

