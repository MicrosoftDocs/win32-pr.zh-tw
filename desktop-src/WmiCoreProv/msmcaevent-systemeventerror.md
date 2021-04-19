---
description: 指出已發生 (IPMI) 系統事件的智慧型平臺管理介面。 此錯誤會寫入 SMBIOS 系統事件記錄檔中， (SEL) 。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: MSMCAEvent_SystemEventError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978312"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="1994e-105">MSMCAEvent \_ SystemEventError 類別</span><span class="sxs-lookup"><span data-stu-id="1994e-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="1994e-106">**MSMCAEvent \_ SystemEventError** 類別指出已發生智慧型平臺管理介面 (IPMI) 系統事件。</span><span class="sxs-lookup"><span data-stu-id="1994e-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="1994e-107">此錯誤會寫入 SMBIOS 系統事件記錄檔中， (SEL) 。</span><span class="sxs-lookup"><span data-stu-id="1994e-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="1994e-108">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="1994e-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="1994e-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1994e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1994e-110">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="1994e-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1994e-111">語法</span><span class="sxs-lookup"><span data-stu-id="1994e-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="1994e-112">成員</span><span class="sxs-lookup"><span data-stu-id="1994e-112">Members</span></span>

<span data-ttu-id="1994e-113">**MSMCAEvent \_ SystemEventError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1994e-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="1994e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1994e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1994e-115">屬性</span><span class="sxs-lookup"><span data-stu-id="1994e-115">Properties</span></span>

<span data-ttu-id="1994e-116">**MSMCAEvent \_ SystemEventError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1994e-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1994e-117">**使用中**</span><span class="sxs-lookup"><span data-stu-id="1994e-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-118">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1994e-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-120">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1994e-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="1994e-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1994e-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-124">記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="1994e-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-125">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="1994e-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1994e-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-128">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="1994e-128">CPU that reported the error.</span></span> <span data-ttu-id="1994e-129">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="1994e-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="1994e-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-131">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-133">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="1994e-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="1994e-134">值</span><span class="sxs-lookup"><span data-stu-id="1994e-134">Value</span></span>                                                                                                | <span data-ttu-id="1994e-135">意義</span><span class="sxs-lookup"><span data-stu-id="1994e-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="1994e-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="1994e-137">可復原</span><span class="sxs-lookup"><span data-stu-id="1994e-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="1994e-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1994e-139">嚴重</span><span class="sxs-lookup"><span data-stu-id="1994e-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="1994e-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1994e-141">時發生</span><span class="sxs-lookup"><span data-stu-id="1994e-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1994e-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1994e-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1994e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1994e-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1994e-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1994e-146">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1994e-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="1994e-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1994e-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-150">如果 0 (零) 則不會將此事件記錄到系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="1994e-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="1994e-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-152">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="1994e-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1994e-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-154">包含原始錯誤記錄的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="1994e-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="1994e-155">陣列中 **Size** 屬性指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1994e-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-156">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="1994e-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-157">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1994e-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-159">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="1994e-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="1994e-160">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1994e-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1994e-161">**SEL \_ DATA1**</span><span class="sxs-lookup"><span data-stu-id="1994e-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-162">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-164">事件資料欄位1。</span><span class="sxs-lookup"><span data-stu-id="1994e-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-165">**SEL \_ DATA2**</span><span class="sxs-lookup"><span data-stu-id="1994e-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-166">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-168">事件資料欄位2。</span><span class="sxs-lookup"><span data-stu-id="1994e-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-169">**SEL \_ DATA3**</span><span class="sxs-lookup"><span data-stu-id="1994e-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-170">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-172">事件資料欄位3。</span><span class="sxs-lookup"><span data-stu-id="1994e-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-173">**SEL \_ 事件 \_ DIR \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1994e-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-174">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-176">事件目錄類型。</span><span class="sxs-lookup"><span data-stu-id="1994e-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-177">**SEL \_ EVM \_ REV**</span><span class="sxs-lookup"><span data-stu-id="1994e-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-178">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-180">錯誤訊息的格式版本。</span><span class="sxs-lookup"><span data-stu-id="1994e-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-181">**SEL 產生器 \_ \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="1994e-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1994e-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-184">軟體識別碼（如果事件是軟體產生的話）。</span><span class="sxs-lookup"><span data-stu-id="1994e-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-185">**選取 \_ 記錄 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="1994e-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-186">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1994e-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-188">用於 SMBIOS 系統事件記錄檔的記錄識別碼， (SEL) 存取權。</span><span class="sxs-lookup"><span data-stu-id="1994e-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-189">**選取 \_ 記錄 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1994e-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-190">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-192">記錄類型。</span><span class="sxs-lookup"><span data-stu-id="1994e-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-193">**SEL \_ 感應器 \_ NUM**</span><span class="sxs-lookup"><span data-stu-id="1994e-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-194">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-196">產生事件的感應器編號。</span><span class="sxs-lookup"><span data-stu-id="1994e-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-197">**SEL \_ 感應器 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="1994e-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-198">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1994e-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-200">產生事件之感應器的感應器類型代碼。</span><span class="sxs-lookup"><span data-stu-id="1994e-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-201">**選取 \_ 時間 \_ 戳**</span><span class="sxs-lookup"><span data-stu-id="1994e-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-202">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1994e-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-204">事件記錄檔的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="1994e-204">Timestamp of the event log.</span></span>

<span data-ttu-id="1994e-205">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1994e-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1994e-206">**大小**</span><span class="sxs-lookup"><span data-stu-id="1994e-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-207">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1994e-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-209">原始錯誤記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="1994e-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-210">**型別**</span><span class="sxs-lookup"><span data-stu-id="1994e-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-211">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1994e-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-213">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="1994e-213">Type of event log message.</span></span> <span data-ttu-id="1994e-214">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="1994e-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="1994e-215">**驗證 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="1994e-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1994e-216">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1994e-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1994e-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1994e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1994e-218">用來指出後續欄位有效性的驗證位。</span><span class="sxs-lookup"><span data-stu-id="1994e-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="1994e-219">值</span><span class="sxs-lookup"><span data-stu-id="1994e-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="1994e-220">意義</span><span class="sxs-lookup"><span data-stu-id="1994e-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="1994e-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="1994e-222">**SEL \_記錄 \_ 識別碼** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="1994e-223"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="1994e-224">**SEL \_記錄 \_ 類型** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="1994e-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="1994e-226">**SEL \_產生器 \_ 識別碼** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="1994e-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="1994e-228">**SEL \_EVM \_ REV** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="1994e-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="1994e-230">**SEL \_感應器 \_ 類型** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="1994e-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="1994e-232">**SEL \_感應器 \_ NUM** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="1994e-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="1994e-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="1994e-234">**SEL \_事件 \_ 目錄** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="1994e-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="1994e-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="1994e-236">**SEL \_事件 \_ DATA1** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="1994e-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="1994e-238">**SEL \_事件 \_ DATA2** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="1994e-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="1994e-240">**SEL \_事件 \_ DATA3** 有效。</span><span class="sxs-lookup"><span data-stu-id="1994e-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="1994e-241">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1994e-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1994e-242">備註</span><span class="sxs-lookup"><span data-stu-id="1994e-242">Remarks</span></span>

<span data-ttu-id="1994e-243">**MSMCAEvent \_ SystemEventError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="1994e-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1994e-244">規格需求</span><span class="sxs-lookup"><span data-stu-id="1994e-244">Requirements</span></span>



| <span data-ttu-id="1994e-245">需求</span><span class="sxs-lookup"><span data-stu-id="1994e-245">Requirement</span></span> | <span data-ttu-id="1994e-246">值</span><span class="sxs-lookup"><span data-stu-id="1994e-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1994e-247">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1994e-247">Minimum supported client</span></span><br/> | <span data-ttu-id="1994e-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1994e-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1994e-249">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1994e-249">Minimum supported server</span></span><br/> | <span data-ttu-id="1994e-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1994e-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1994e-251">命名空間</span><span class="sxs-lookup"><span data-stu-id="1994e-251">Namespace</span></span><br/>                | <span data-ttu-id="1994e-252">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="1994e-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1994e-253">MOF</span><span class="sxs-lookup"><span data-stu-id="1994e-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1994e-254"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1994e-255">DLL</span><span class="sxs-lookup"><span data-stu-id="1994e-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1994e-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1994e-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1994e-257">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1994e-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1994e-258">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="1994e-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="1994e-259">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="1994e-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

