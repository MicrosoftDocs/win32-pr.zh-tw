---
description: 指出機器檢查架構 (MCA) PCI 元件錯誤。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: MSMCAEvent_PCIComponentError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996906"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="d2bab-104">MSMCAEvent \_ PCIComponentError 類別</span><span class="sxs-lookup"><span data-stu-id="d2bab-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="d2bab-105">**MSMCAEvent \_ PCIComponentError** 類別指出電腦檢查架構 (MCA) PCI 元件錯誤。</span><span class="sxs-lookup"><span data-stu-id="d2bab-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="d2bab-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="d2bab-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="d2bab-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d2bab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d2bab-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="d2bab-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2bab-109">語法</span><span class="sxs-lookup"><span data-stu-id="d2bab-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="d2bab-110">成員</span><span class="sxs-lookup"><span data-stu-id="d2bab-110">Members</span></span>

<span data-ttu-id="d2bab-111">**MSMCAEvent \_ PCIComponentError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d2bab-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="d2bab-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d2bab-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2bab-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d2bab-113">Properties</span></span>

<span data-ttu-id="d2bab-114">**MSMCAEvent \_ PCIComponentError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d2bab-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2bab-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="d2bab-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d2bab-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d2bab-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="d2bab-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d2bab-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-122">記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="d2bab-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-123">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="d2bab-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d2bab-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-126">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="d2bab-126">CPU that reported the error.</span></span> <span data-ttu-id="d2bab-127">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="d2bab-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="d2bab-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-131">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="d2bab-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="d2bab-132">值</span><span class="sxs-lookup"><span data-stu-id="d2bab-132">Value</span></span>                                                                                                | <span data-ttu-id="d2bab-133">意義</span><span class="sxs-lookup"><span data-stu-id="d2bab-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="d2bab-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="d2bab-135">可復原</span><span class="sxs-lookup"><span data-stu-id="d2bab-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="d2bab-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d2bab-137">嚴重</span><span class="sxs-lookup"><span data-stu-id="d2bab-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="d2bab-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d2bab-139">時發生</span><span class="sxs-lookup"><span data-stu-id="d2bab-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2bab-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="d2bab-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d2bab-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d2bab-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-144">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2bab-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="d2bab-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d2bab-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-148">如果 0 (零) 則不會將此事件記錄到系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d2bab-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-149">**PCI \_ 複合 \_ 錯誤 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d2bab-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-150">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d2bab-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-152">內部錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d2bab-152">Internal error code.</span></span>

<span data-ttu-id="d2bab-153">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d2bab-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-154">**PCI \_ COMP \_ 資訊 \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="d2bab-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-155">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-157">PCI 元件的匯流排編號。</span><span class="sxs-lookup"><span data-stu-id="d2bab-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-158">**PCI \_ COMP \_ 資訊 \_ ClassCodeBaseClass**</span><span class="sxs-lookup"><span data-stu-id="d2bab-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-159">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-161">PCI 元件之基類的類別代碼。</span><span class="sxs-lookup"><span data-stu-id="d2bab-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-162">**PCI \_ COMP \_ 資訊 \_ ClassCodeInterface**</span><span class="sxs-lookup"><span data-stu-id="d2bab-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-163">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-165">PCI 元件的類別程式碼介面。</span><span class="sxs-lookup"><span data-stu-id="d2bab-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-166">**PCI \_ COMP \_ 資訊 \_ ClassCodeSubClass**</span><span class="sxs-lookup"><span data-stu-id="d2bab-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-167">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-169">PCI 元件的類別程式碼子類別。</span><span class="sxs-lookup"><span data-stu-id="d2bab-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-170">**PCI \_ 複合 \_ 資訊 \_ DeviceId**</span><span class="sxs-lookup"><span data-stu-id="d2bab-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-171">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d2bab-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-173">PCI 元件的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2bab-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-174">**PCI \_ COMP \_ 資訊 \_ DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="d2bab-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-175">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-177">PCI 元件的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="d2bab-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-178">**PCI \_ COMP \_ 資訊 \_ FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="d2bab-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-179">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-181">PCI 元件的功能編號。</span><span class="sxs-lookup"><span data-stu-id="d2bab-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-182">**PCI \_ COMP \_ 資訊 \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="d2bab-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-183">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="d2bab-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-185">PCI 元件的區段編號。</span><span class="sxs-lookup"><span data-stu-id="d2bab-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-186">**PCI \_ COMP \_ INFO \_ VendorId**</span><span class="sxs-lookup"><span data-stu-id="d2bab-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d2bab-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-189">PCI 元件的廠商識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2bab-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-190">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="d2bab-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-191">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="d2bab-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-193">包含原始錯誤記錄的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="d2bab-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="d2bab-194">陣列中 **Size** 屬性指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d2bab-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-195">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="d2bab-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-196">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d2bab-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-198">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2bab-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="d2bab-199">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d2bab-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-200">**大小**</span><span class="sxs-lookup"><span data-stu-id="d2bab-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-201">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d2bab-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-203">原始錯誤記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="d2bab-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-204">**型別**</span><span class="sxs-lookup"><span data-stu-id="d2bab-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-205">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d2bab-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-207">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="d2bab-207">Type of event log message.</span></span> <span data-ttu-id="d2bab-208">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="d2bab-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="d2bab-209">**驗證 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="d2bab-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2bab-210">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d2bab-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2bab-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d2bab-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2bab-212">用來指出後續欄位有效性的驗證位。</span><span class="sxs-lookup"><span data-stu-id="d2bab-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="d2bab-213">值</span><span class="sxs-lookup"><span data-stu-id="d2bab-213">Values</span></span>                                                                               | <span data-ttu-id="d2bab-214">意義</span><span class="sxs-lookup"><span data-stu-id="d2bab-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d2bab-215"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="d2bab-216">PCI \_ 複合 \_ 錯誤 \_ 狀態為有效。</span><span class="sxs-lookup"><span data-stu-id="d2bab-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="d2bab-217"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="d2bab-218">PCI \_ COMP \_ 資訊是有效的。</span><span class="sxs-lookup"><span data-stu-id="d2bab-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="d2bab-219"><dt>4 (0x4) </dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="d2bab-220">PCI \_ COMP \_ MEM \_ NUM 是有效的。</span><span class="sxs-lookup"><span data-stu-id="d2bab-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="d2bab-221"><dt>8 (0x8) </dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="d2bab-222">PCI \_ 複合 \_ IO \_ NUM 是有效的。</span><span class="sxs-lookup"><span data-stu-id="d2bab-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="d2bab-223"><dt>16 (0x10) </dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="d2bab-224">PCI \_ COMP \_ REGS \_ 資料 \_ 配對有效。</span><span class="sxs-lookup"><span data-stu-id="d2bab-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="d2bab-225">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d2bab-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2bab-226">備註</span><span class="sxs-lookup"><span data-stu-id="d2bab-226">Remarks</span></span>

<span data-ttu-id="d2bab-227">**MSMCAEvent \_ PCIComponentError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="d2bab-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2bab-228">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2bab-228">Requirements</span></span>



| <span data-ttu-id="d2bab-229">需求</span><span class="sxs-lookup"><span data-stu-id="d2bab-229">Requirement</span></span> | <span data-ttu-id="d2bab-230">值</span><span class="sxs-lookup"><span data-stu-id="d2bab-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2bab-231">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2bab-231">Minimum supported client</span></span><br/> | <span data-ttu-id="d2bab-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2bab-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="d2bab-233">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2bab-233">Minimum supported server</span></span><br/> | <span data-ttu-id="d2bab-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2bab-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="d2bab-235">命名空間</span><span class="sxs-lookup"><span data-stu-id="d2bab-235">Namespace</span></span><br/>                | <span data-ttu-id="d2bab-236">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="d2bab-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="d2bab-237">MOF</span><span class="sxs-lookup"><span data-stu-id="d2bab-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2bab-238"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2bab-239">DLL</span><span class="sxs-lookup"><span data-stu-id="d2bab-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2bab-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2bab-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2bab-241">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2bab-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2bab-242">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="d2bab-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="d2bab-243">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="d2bab-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

