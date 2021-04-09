---
description: CIM \_ DeviceErrorCounts 類別是一個統計類別，其中包含邏輯裝置的錯誤相關計數器。 錯誤的類型是由 CCITT (Rec 733) 和 ISO (IEC 10164-4) 所定義。
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: CIM_DeviceErrorCounts 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936387"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="b939e-104">CIM \_ DeviceErrorCounts 類別</span><span class="sxs-lookup"><span data-stu-id="b939e-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="b939e-105">**CIM \_ DeviceErrorCounts** 類別是一個統計類別，其中包含邏輯裝置的錯誤相關計數器。</span><span class="sxs-lookup"><span data-stu-id="b939e-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="b939e-106">錯誤的類型是由 CCITT (Rec 733) 和 ISO (IEC 10164-4) 所定義。</span><span class="sxs-lookup"><span data-stu-id="b939e-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b939e-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b939e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b939e-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b939e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b939e-109">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b939e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b939e-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b939e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b939e-111">語法</span><span class="sxs-lookup"><span data-stu-id="b939e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="b939e-112">成員</span><span class="sxs-lookup"><span data-stu-id="b939e-112">Members</span></span>

<span data-ttu-id="b939e-113">**CIM \_ DeviceErrorCounts** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b939e-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="b939e-114">方法</span><span class="sxs-lookup"><span data-stu-id="b939e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b939e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b939e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b939e-116">方法</span><span class="sxs-lookup"><span data-stu-id="b939e-116">Methods</span></span>

<span data-ttu-id="b939e-117">**CIM \_ DeviceErrorCounts** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b939e-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="b939e-118">方法</span><span class="sxs-lookup"><span data-stu-id="b939e-118">Method</span></span>                                                                     | <span data-ttu-id="b939e-119">描述</span><span class="sxs-lookup"><span data-stu-id="b939e-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="b939e-120">**ResetCounter**</span><span class="sxs-lookup"><span data-stu-id="b939e-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="b939e-121">重設錯誤和警告計數器。</span><span class="sxs-lookup"><span data-stu-id="b939e-121">Resets the error and warning counters.</span></span> <span data-ttu-id="b939e-122">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b939e-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b939e-123">屬性</span><span class="sxs-lookup"><span data-stu-id="b939e-123">Properties</span></span>

<span data-ttu-id="b939e-124">**CIM \_ DeviceErrorCounts** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b939e-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b939e-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="b939e-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-128">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b939e-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b939e-129">統計資料或度量的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="b939e-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="b939e-130">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="b939e-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="b939e-131">**CriticalErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b939e-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-132">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b939e-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-134">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.7 ") </span><span class="sxs-lookup"><span data-stu-id="b939e-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="b939e-135">嚴重錯誤的計數。</span><span class="sxs-lookup"><span data-stu-id="b939e-135">Count of the critical errors.</span></span>

<span data-ttu-id="b939e-136">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b939e-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b939e-137">**說明**</span><span class="sxs-lookup"><span data-stu-id="b939e-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b939e-140">統計資料或度量的文字描述。</span><span class="sxs-lookup"><span data-stu-id="b939e-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="b939e-141">這個屬性繼承自 [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)。</span><span class="sxs-lookup"><span data-stu-id="b939e-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="b939e-142">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b939e-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-145">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ LogicalDevice**](cim-logicaldevice.md)。**CreationClassName**") ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b939e-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b939e-146">範圍裝置的 **CreationClassName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b939e-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="b939e-147">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b939e-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-150">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ LogicalDevice**](cim-logicaldevice.md)。**DeviceID**") 、 [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="b939e-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b939e-151">範圍裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b939e-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b939e-152">**IndeterminateErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b939e-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-153">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b939e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b939e-155">不定錯誤的計數。</span><span class="sxs-lookup"><span data-stu-id="b939e-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="b939e-156">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b939e-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b939e-157">**MajorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b939e-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-158">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b939e-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-160">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.8 ") </span><span class="sxs-lookup"><span data-stu-id="b939e-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="b939e-161">主要錯誤的計數。</span><span class="sxs-lookup"><span data-stu-id="b939e-161">Count of the major errors.</span></span>

<span data-ttu-id="b939e-162">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b939e-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b939e-163">**MinorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="b939e-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-164">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b939e-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b939e-166">次要錯誤的計數。</span><span class="sxs-lookup"><span data-stu-id="b939e-166">Count of the minor errors.</span></span>

<span data-ttu-id="b939e-167">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b939e-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b939e-168">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b939e-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-171">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b939e-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b939e-172">「繼承的名稱」屬性會當做 **CIM \_ DeviceErrorCounts** 實例之索引鍵的一部分。</span><span class="sxs-lookup"><span data-stu-id="b939e-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="b939e-173">物件的範圍是套用統計資料的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="b939e-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="b939e-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b939e-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-177">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ LogicalDevice**](cim-logicaldevice.md)。**SystemCreationClassName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b939e-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b939e-178">界定系統的 **CreationClassName**。</span><span class="sxs-lookup"><span data-stu-id="b939e-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="b939e-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b939e-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b939e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-182">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ LogicalDevice**](cim-logicaldevice.md)。**SystemName**") ， [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="b939e-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b939e-183">範圍系統的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b939e-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="b939e-184">**WarningCount**</span><span class="sxs-lookup"><span data-stu-id="b939e-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b939e-185">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b939e-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b939e-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b939e-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b939e-187">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.9 ") </span><span class="sxs-lookup"><span data-stu-id="b939e-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="b939e-188">警告的計數。</span><span class="sxs-lookup"><span data-stu-id="b939e-188">Count of the warnings.</span></span>

<span data-ttu-id="b939e-189">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b939e-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b939e-190">備註</span><span class="sxs-lookup"><span data-stu-id="b939e-190">Remarks</span></span>

<span data-ttu-id="b939e-191">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b939e-191">WMI does not implement this class.</span></span>

<span data-ttu-id="b939e-192">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b939e-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b939e-193">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b939e-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b939e-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="b939e-194">Requirements</span></span>



| <span data-ttu-id="b939e-195">需求</span><span class="sxs-lookup"><span data-stu-id="b939e-195">Requirement</span></span> | <span data-ttu-id="b939e-196">值</span><span class="sxs-lookup"><span data-stu-id="b939e-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b939e-197">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b939e-197">Minimum supported client</span></span><br/> | <span data-ttu-id="b939e-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b939e-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b939e-199">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b939e-199">Minimum supported server</span></span><br/> | <span data-ttu-id="b939e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b939e-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b939e-201">命名空間</span><span class="sxs-lookup"><span data-stu-id="b939e-201">Namespace</span></span><br/>                | <span data-ttu-id="b939e-202">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b939e-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b939e-203">MOF</span><span class="sxs-lookup"><span data-stu-id="b939e-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b939e-204"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b939e-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b939e-205">DLL</span><span class="sxs-lookup"><span data-stu-id="b939e-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b939e-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b939e-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b939e-207">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b939e-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b939e-208">**CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="b939e-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

