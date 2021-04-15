---
description: 代表 CPU 錯誤事件。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: MSMCAEvent_CPUError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511400"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="1eb46-104">MSMCAEvent \_ CPUError 類別</span><span class="sxs-lookup"><span data-stu-id="1eb46-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="1eb46-105">**MSMCAEvent \_ CPUError** 類別代表 CPU 錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="1eb46-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="1eb46-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="1eb46-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="1eb46-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1eb46-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1eb46-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="1eb46-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb46-109">語法</span><span class="sxs-lookup"><span data-stu-id="1eb46-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="1eb46-110">成員</span><span class="sxs-lookup"><span data-stu-id="1eb46-110">Members</span></span>

<span data-ttu-id="1eb46-111">**MSMCAEvent \_ CPUError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1eb46-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="1eb46-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1eb46-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1eb46-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1eb46-113">Properties</span></span>

<span data-ttu-id="1eb46-114">**MSMCAEvent \_ CPUError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1eb46-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1eb46-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="1eb46-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1eb46-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1eb46-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="1eb46-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eb46-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-122">MCA 記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="1eb46-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-123">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="1eb46-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eb46-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-126">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="1eb46-126">CPU that reported the error.</span></span> <span data-ttu-id="1eb46-127">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="1eb46-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="1eb46-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="1eb46-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-131">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="1eb46-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="1eb46-132">值</span><span class="sxs-lookup"><span data-stu-id="1eb46-132">Value</span></span>                                                                                                | <span data-ttu-id="1eb46-133">意義</span><span class="sxs-lookup"><span data-stu-id="1eb46-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="1eb46-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="1eb46-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="1eb46-135">可復原</span><span class="sxs-lookup"><span data-stu-id="1eb46-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="1eb46-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1eb46-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1eb46-137">嚴重</span><span class="sxs-lookup"><span data-stu-id="1eb46-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="1eb46-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1eb46-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1eb46-139">時發生</span><span class="sxs-lookup"><span data-stu-id="1eb46-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1eb46-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="1eb46-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1eb46-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1eb46-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-144">這個類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="1eb46-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-145">**Level**</span><span class="sxs-lookup"><span data-stu-id="1eb46-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eb46-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-148">限定詞： **WmiMissingData** (-1) </span><span class="sxs-lookup"><span data-stu-id="1eb46-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-149">發生錯誤之快取、轉譯緩衝區 (TLB) 或微架構結構的層級。</span><span class="sxs-lookup"><span data-stu-id="1eb46-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="1eb46-150">值為 0 (零) 表示第一個層級。</span><span class="sxs-lookup"><span data-stu-id="1eb46-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-151">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="1eb46-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eb46-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-154">如果為零，則此事件不會記錄到系統事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="1eb46-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-155">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="1eb46-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-156">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="1eb46-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-158">包含原始錯誤記錄的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="1eb46-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="1eb46-159">陣列中 **Size** 屬性指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1eb46-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-160">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="1eb46-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-161">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1eb46-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-163">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="1eb46-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="1eb46-164">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1eb46-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-165">**大小**</span><span class="sxs-lookup"><span data-stu-id="1eb46-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eb46-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-168">原始錯誤記錄的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1eb46-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1eb46-169">**型別**</span><span class="sxs-lookup"><span data-stu-id="1eb46-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1eb46-170">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1eb46-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1eb46-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1eb46-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1eb46-172">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="1eb46-172">Type of event log message.</span></span> <span data-ttu-id="1eb46-173">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="1eb46-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1eb46-174">備註</span><span class="sxs-lookup"><span data-stu-id="1eb46-174">Remarks</span></span>

<span data-ttu-id="1eb46-175">**MSMCAEvent \_ CPUError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="1eb46-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb46-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eb46-176">Requirements</span></span>



| <span data-ttu-id="1eb46-177">需求</span><span class="sxs-lookup"><span data-stu-id="1eb46-177">Requirement</span></span> | <span data-ttu-id="1eb46-178">值</span><span class="sxs-lookup"><span data-stu-id="1eb46-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb46-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1eb46-179">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb46-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1eb46-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1eb46-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1eb46-181">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb46-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1eb46-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1eb46-183">命名空間</span><span class="sxs-lookup"><span data-stu-id="1eb46-183">Namespace</span></span><br/>                | <span data-ttu-id="1eb46-184">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="1eb46-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1eb46-185">MOF</span><span class="sxs-lookup"><span data-stu-id="1eb46-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eb46-186"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eb46-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eb46-187">DLL</span><span class="sxs-lookup"><span data-stu-id="1eb46-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eb46-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eb46-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb46-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1eb46-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb46-190">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="1eb46-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="1eb46-191">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="1eb46-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

