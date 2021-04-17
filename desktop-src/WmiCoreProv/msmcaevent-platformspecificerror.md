---
description: 指出電腦檢查架構 (MCA) 平臺特定的錯誤。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: MSMCAEvent_PlatformSpecificError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469041"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="823aa-104">MSMCAEvent \_ PlatformSpecificError 類別</span><span class="sxs-lookup"><span data-stu-id="823aa-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="823aa-105">**MSMCAEvent \_ PlatformSpecificError** 類別指出電腦檢查架構 (MCA) 平臺特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="823aa-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="823aa-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="823aa-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="823aa-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="823aa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="823aa-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="823aa-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="823aa-109">語法</span><span class="sxs-lookup"><span data-stu-id="823aa-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="823aa-110">成員</span><span class="sxs-lookup"><span data-stu-id="823aa-110">Members</span></span>

<span data-ttu-id="823aa-111">**MSMCAEvent \_ PlatformSpecificError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="823aa-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="823aa-112">屬性</span><span class="sxs-lookup"><span data-stu-id="823aa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="823aa-113">屬性</span><span class="sxs-lookup"><span data-stu-id="823aa-113">Properties</span></span>

<span data-ttu-id="823aa-114">**MSMCAEvent \_ PlatformSpecificError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="823aa-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="823aa-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="823aa-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="823aa-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="823aa-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="823aa-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="823aa-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-122">記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="823aa-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-123">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="823aa-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="823aa-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-126">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="823aa-126">CPU that reported the error.</span></span> <span data-ttu-id="823aa-127">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="823aa-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="823aa-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="823aa-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-131">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="823aa-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="823aa-132">值</span><span class="sxs-lookup"><span data-stu-id="823aa-132">Value</span></span>                                                                                                | <span data-ttu-id="823aa-133">意義</span><span class="sxs-lookup"><span data-stu-id="823aa-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="823aa-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="823aa-135">可復原</span><span class="sxs-lookup"><span data-stu-id="823aa-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="823aa-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="823aa-137">嚴重</span><span class="sxs-lookup"><span data-stu-id="823aa-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="823aa-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="823aa-139">時發生</span><span class="sxs-lookup"><span data-stu-id="823aa-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="823aa-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="823aa-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="823aa-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823aa-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="823aa-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="823aa-144">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="823aa-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="823aa-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="823aa-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-148">如果 0 (零) 則不會將此事件記錄到系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="823aa-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-149">**OEM \_ 元件 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="823aa-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-150">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="823aa-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-152">報告錯誤之元件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="823aa-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-153">**平臺 \_ 匯流排 \_ 特定 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="823aa-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-154">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-156">OEM 特定、與匯流排相關的資料。</span><span class="sxs-lookup"><span data-stu-id="823aa-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="823aa-157">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="823aa-158">**平臺 \_ 錯誤 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="823aa-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-159">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-161">一般平臺錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="823aa-161">Generic platform error status.</span></span>

<span data-ttu-id="823aa-162">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="823aa-163">**平臺要求者 \_ \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="823aa-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-164">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-166">事件時的要求者識別碼。</span><span class="sxs-lookup"><span data-stu-id="823aa-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="823aa-167">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="823aa-168">**平臺 \_ 回應程式 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="823aa-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-169">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-171">事件時的回應者識別碼。</span><span class="sxs-lookup"><span data-stu-id="823aa-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="823aa-172">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="823aa-173">**平臺 \_ 目標 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="823aa-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-174">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-176">事件時的目標識別碼。</span><span class="sxs-lookup"><span data-stu-id="823aa-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="823aa-177">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="823aa-178">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="823aa-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-179">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="823aa-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="823aa-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-181">位元組陣列，其中包含系統抽象層 (SAL) 呈現給 Windows 的原始錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="823aa-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="823aa-182">陣列中的元素數目是由 **Size** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="823aa-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-183">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="823aa-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-184">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-186">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="823aa-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="823aa-187">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="823aa-188">**大小**</span><span class="sxs-lookup"><span data-stu-id="823aa-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-189">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="823aa-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-191">原始錯誤記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="823aa-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-192">**型別**</span><span class="sxs-lookup"><span data-stu-id="823aa-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-193">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="823aa-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-195">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="823aa-195">Type of event log message.</span></span> <span data-ttu-id="823aa-196">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="823aa-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-197">**驗證 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="823aa-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823aa-198">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="823aa-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823aa-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="823aa-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823aa-200">用來指出後續欄位有效性的驗證位。</span><span class="sxs-lookup"><span data-stu-id="823aa-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="823aa-201">值</span><span class="sxs-lookup"><span data-stu-id="823aa-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="823aa-202">意義</span><span class="sxs-lookup"><span data-stu-id="823aa-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="823aa-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="823aa-204">**平臺 \_錯誤 \_ 狀態** 為有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="823aa-205"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="823aa-206">**平臺 \_錯誤要求者 \_ \_ 識別碼** 有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="823aa-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="823aa-208">**平臺 \_錯誤 \_ 回應程式 \_ 識別碼** 有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="823aa-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="823aa-210">**平臺 \_錯誤 \_ 目標 \_ 識別碼** 有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="823aa-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="823aa-212">**平臺 \_特定錯誤的 \_ \_ 資料** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="823aa-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="823aa-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="823aa-214">**平臺 \_錯誤 \_ OEM \_ 識別碼** 有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="823aa-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="823aa-216">**平臺 \_錯誤 \_ OEM \_ 資料 \_ 結構** 有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="823aa-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="823aa-218">**平臺 \_錯誤 \_ OEM \_ 裝置 \_ 路徑** 有效。</span><span class="sxs-lookup"><span data-stu-id="823aa-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="823aa-219">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="823aa-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="823aa-220">備註</span><span class="sxs-lookup"><span data-stu-id="823aa-220">Remarks</span></span>

<span data-ttu-id="823aa-221">**MSMCAEvent \_ PlatformSpecificError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="823aa-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="823aa-222">規格需求</span><span class="sxs-lookup"><span data-stu-id="823aa-222">Requirements</span></span>



| <span data-ttu-id="823aa-223">需求</span><span class="sxs-lookup"><span data-stu-id="823aa-223">Requirement</span></span> | <span data-ttu-id="823aa-224">值</span><span class="sxs-lookup"><span data-stu-id="823aa-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="823aa-225">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="823aa-225">Minimum supported client</span></span><br/> | <span data-ttu-id="823aa-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="823aa-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="823aa-227">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="823aa-227">Minimum supported server</span></span><br/> | <span data-ttu-id="823aa-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="823aa-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="823aa-229">命名空間</span><span class="sxs-lookup"><span data-stu-id="823aa-229">Namespace</span></span><br/>                | <span data-ttu-id="823aa-230">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="823aa-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="823aa-231">MOF</span><span class="sxs-lookup"><span data-stu-id="823aa-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="823aa-232"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="823aa-233">DLL</span><span class="sxs-lookup"><span data-stu-id="823aa-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823aa-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="823aa-235">另請參閱</span><span class="sxs-lookup"><span data-stu-id="823aa-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823aa-236">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="823aa-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="823aa-237">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="823aa-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

