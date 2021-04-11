---
description: CIM \_ OSVersionCheck 類別會指定可支援軟體元素的作業系統版本。
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: CIM_OSVersionCheck 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025938"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="49c60-103">CIM \_ OSVersionCheck 類別</span><span class="sxs-lookup"><span data-stu-id="49c60-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="49c60-104">**CIM \_ OSVersionCheck** 類別會指定可支援軟體元素的作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="49c60-105">您可以針對特定、最小值、最大值或作業系統版本範圍執行檢查。</span><span class="sxs-lookup"><span data-stu-id="49c60-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="49c60-106">若要指定特定的作業系統版本，最小和最大版本必須相等。</span><span class="sxs-lookup"><span data-stu-id="49c60-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="49c60-107">若要指定最小版本，必須指定最小版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="49c60-108">若要指定最大版本，則只需要指定最大版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="49c60-109">若要指定範圍，必須指定最小和最大版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="49c60-110">作業系統的類型是在擁有的 software 專案的 **TargetOperatingSystem** 屬性中指定的。</span><span class="sxs-lookup"><span data-stu-id="49c60-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="49c60-111">檢查的詳細資料會與在 cim [**\_ InstalledOS**](cim-installedos.md)關聯的 cim [**\_ 作業系統**](cim-operatingsystem.md)物件中找到的對應詳細資料，與描述該環境的 cim 系統系統物件相關。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="49c60-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="49c60-112">至少有一個 **CIM \_ 作業系統** 類別必須滿足要滿足的檢查條件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="49c60-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="49c60-113">換句話說，並非所有相關電腦系統上的作業系統都必須滿足該條件。</span><span class="sxs-lookup"><span data-stu-id="49c60-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="49c60-114">此外， **CIM \_ 作業系統** 類別的 **OSType** 屬性必須符合 **TargetOperatingSystem** 屬性的類型。</span><span class="sxs-lookup"><span data-stu-id="49c60-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49c60-115">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="49c60-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49c60-116">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="49c60-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49c60-117">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="49c60-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="49c60-118">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="49c60-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c60-119">語法</span><span class="sxs-lookup"><span data-stu-id="49c60-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
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
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="49c60-120">成員</span><span class="sxs-lookup"><span data-stu-id="49c60-120">Members</span></span>

<span data-ttu-id="49c60-121">**CIM \_ OSVersionCheck** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="49c60-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="49c60-122">方法</span><span class="sxs-lookup"><span data-stu-id="49c60-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="49c60-123">屬性</span><span class="sxs-lookup"><span data-stu-id="49c60-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49c60-124">方法</span><span class="sxs-lookup"><span data-stu-id="49c60-124">Methods</span></span>

<span data-ttu-id="49c60-125">**CIM \_ OSVersionCheck** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="49c60-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="49c60-126">方法</span><span class="sxs-lookup"><span data-stu-id="49c60-126">Method</span></span>                                                      | <span data-ttu-id="49c60-127">描述</span><span class="sxs-lookup"><span data-stu-id="49c60-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="49c60-128">**調用**</span><span class="sxs-lookup"><span data-stu-id="49c60-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="49c60-129">採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="49c60-129">Takes a particular action.</span></span> <span data-ttu-id="49c60-130">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="49c60-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49c60-131">屬性</span><span class="sxs-lookup"><span data-stu-id="49c60-131">Properties</span></span>

<span data-ttu-id="49c60-132">**CIM \_ OSVersionCheck** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="49c60-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49c60-133">**標題**</span><span class="sxs-lookup"><span data-stu-id="49c60-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-136">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="49c60-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="49c60-137">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="49c60-137">A short textual description of the subject.</span></span>

<span data-ttu-id="49c60-138">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c60-139">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="49c60-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-142">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="49c60-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49c60-143">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49c60-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="49c60-144">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c60-145">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="49c60-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-146">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="49c60-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c60-148">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="49c60-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="49c60-149">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="49c60-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="49c60-150">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="49c60-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="49c60-151">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="49c60-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="49c60-152">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c60-153">**說明**</span><span class="sxs-lookup"><span data-stu-id="49c60-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c60-156">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="49c60-156">A description of the objects.</span></span>

<span data-ttu-id="49c60-157">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c60-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="49c60-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-161">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**版本**") </span><span class="sxs-lookup"><span data-stu-id="49c60-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="49c60-162">所需作業系統的最大版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="49c60-163">此值會以下列其中一種形式進行編碼：</span><span class="sxs-lookup"><span data-stu-id="49c60-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="49c60-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="49c60-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="49c60-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="49c60-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="49c60-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="49c60-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-169">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ 作業系統**](cim-operatingsystem.md)。**版本**") </span><span class="sxs-lookup"><span data-stu-id="49c60-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="49c60-170">所需作業系統的最小版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="49c60-171">此值會以下列其中一種形式進行編碼：</span><span class="sxs-lookup"><span data-stu-id="49c60-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="49c60-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="49c60-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="49c60-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="49c60-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="49c60-174">**名稱**</span><span class="sxs-lookup"><span data-stu-id="49c60-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-177">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Name**") 、 [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="49c60-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49c60-178">用來識別軟體元素的名稱</span><span class="sxs-lookup"><span data-stu-id="49c60-178">Name used to identify the software element</span></span>

<span data-ttu-id="49c60-179">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c60-180">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="49c60-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-183">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="49c60-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49c60-184">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="49c60-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="49c60-185">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c60-186">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="49c60-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="49c60-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-189">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="49c60-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="49c60-190">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="49c60-190">The software element state of a software element.</span></span>

<span data-ttu-id="49c60-191">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="49c60-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="49c60-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-193">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="49c60-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="49c60-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="49c60-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-195">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="49c60-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="49c60-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="49c60-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-197">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="49c60-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="49c60-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="49c60-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-199">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="49c60-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49c60-200">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="49c60-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-201">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="49c60-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-203">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="49c60-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="49c60-204">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="49c60-204">Target operating system of the software element.</span></span>

<span data-ttu-id="49c60-205">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49c60-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="49c60-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49c60-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="49c60-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="49c60-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="49c60-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-209">Mac OS</span><span class="sxs-lookup"><span data-stu-id="49c60-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="49c60-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="49c60-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-211">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="49c60-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="49c60-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="49c60-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="49c60-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="49c60-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="49c60-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="49c60-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="49c60-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="49c60-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-216">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="49c60-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="49c60-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="49c60-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="49c60-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="49c60-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="49c60-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="49c60-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="49c60-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="49c60-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="49c60-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="49c60-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="49c60-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="49c60-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="49c60-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-224">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="49c60-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="49c60-225"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="49c60-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="49c60-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="49c60-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-227">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="49c60-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="49c60-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="49c60-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="49c60-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="49c60-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="49c60-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="49c60-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="49c60-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="49c60-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="49c60-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="49c60-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="49c60-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="49c60-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="49c60-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="49c60-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-237">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="49c60-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="49c60-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="49c60-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="49c60-239"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="49c60-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="49c60-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="49c60-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="49c60-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="49c60-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="49c60-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="49c60-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="49c60-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="49c60-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="49c60-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="49c60-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="49c60-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="49c60-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="49c60-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="49c60-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="49c60-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="49c60-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="49c60-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="49c60-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="49c60-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="49c60-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-250">系列</span><span class="sxs-lookup"><span data-stu-id="49c60-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="49c60-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="49c60-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-252">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="49c60-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="49c60-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="49c60-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-254">將 NT</span><span class="sxs-lookup"><span data-stu-id="49c60-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="49c60-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="49c60-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="49c60-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="49c60-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="49c60-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="49c60-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="49c60-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="49c60-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="49c60-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="49c60-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="49c60-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="49c60-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="49c60-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="49c60-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="49c60-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-263">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="49c60-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="49c60-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="49c60-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="49c60-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="49c60-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="49c60-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="49c60-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="49c60-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="49c60-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="49c60-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="49c60-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="49c60-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="49c60-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="49c60-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="49c60-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="49c60-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="49c60-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="49c60-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="49c60-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="49c60-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="49c60-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="49c60-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="49c60-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="49c60-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="49c60-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="49c60-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="49c60-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="49c60-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="49c60-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="49c60-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="49c60-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="49c60-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="49c60-280">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="49c60-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="49c60-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="49c60-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="49c60-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="49c60-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="49c60-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="49c60-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="49c60-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="49c60-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="49c60-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="49c60-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49c60-286">**版本**</span><span class="sxs-lookup"><span data-stu-id="49c60-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c60-287">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49c60-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c60-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49c60-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c60-289">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="49c60-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="49c60-290">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="49c60-290">Version of the operation.</span></span>

<span data-ttu-id="49c60-291">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="49c60-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="49c60-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="49c60-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="49c60-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="49c60-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="49c60-294">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="49c60-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49c60-295">備註</span><span class="sxs-lookup"><span data-stu-id="49c60-295">Remarks</span></span>

<span data-ttu-id="49c60-296">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="49c60-296">WMI does not implement this class.</span></span>

<span data-ttu-id="49c60-297">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="49c60-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49c60-298">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="49c60-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c60-299">規格需求</span><span class="sxs-lookup"><span data-stu-id="49c60-299">Requirements</span></span>



| <span data-ttu-id="49c60-300">需求</span><span class="sxs-lookup"><span data-stu-id="49c60-300">Requirement</span></span> | <span data-ttu-id="49c60-301">值</span><span class="sxs-lookup"><span data-stu-id="49c60-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49c60-302">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49c60-302">Minimum supported client</span></span><br/> | <span data-ttu-id="49c60-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49c60-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49c60-304">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49c60-304">Minimum supported server</span></span><br/> | <span data-ttu-id="49c60-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49c60-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49c60-306">命名空間</span><span class="sxs-lookup"><span data-stu-id="49c60-306">Namespace</span></span><br/>                | <span data-ttu-id="49c60-307">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49c60-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49c60-308">MOF</span><span class="sxs-lookup"><span data-stu-id="49c60-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49c60-309"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="49c60-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49c60-310">DLL</span><span class="sxs-lookup"><span data-stu-id="49c60-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49c60-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49c60-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c60-312">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49c60-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c60-313">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="49c60-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

