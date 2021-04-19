---
description: 指出 (MCA) 無效錯誤的機器檢查架構。 不正確 MCA 錯誤會識別不符合 Windows 規格的錯誤格式。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: MSMCAEvent_InvalidError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973264"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="030be-105">MSMCAEvent \_ InvalidError 類別</span><span class="sxs-lookup"><span data-stu-id="030be-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="030be-106">**MSMCAEvent \_ InvalidError** 類別指出電腦檢查架構 (MCA) 不正確錯誤。</span><span class="sxs-lookup"><span data-stu-id="030be-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="030be-107">不正確 MCA 錯誤會識別不符合 Windows 規格的錯誤格式。</span><span class="sxs-lookup"><span data-stu-id="030be-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="030be-108">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="030be-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="030be-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="030be-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="030be-110">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="030be-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="030be-111">語法</span><span class="sxs-lookup"><span data-stu-id="030be-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="030be-112">成員</span><span class="sxs-lookup"><span data-stu-id="030be-112">Members</span></span>

<span data-ttu-id="030be-113">**MSMCAEvent \_ InvalidError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="030be-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="030be-114">屬性</span><span class="sxs-lookup"><span data-stu-id="030be-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="030be-115">屬性</span><span class="sxs-lookup"><span data-stu-id="030be-115">Properties</span></span>

<span data-ttu-id="030be-116">**MSMCAEvent \_ InvalidError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="030be-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="030be-117">**使用中**</span><span class="sxs-lookup"><span data-stu-id="030be-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-118">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="030be-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="030be-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-120">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="030be-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="030be-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="030be-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="030be-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="030be-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-124">MCA 記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="030be-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="030be-125">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="030be-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="030be-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="030be-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-128">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="030be-128">CPU that reported the error.</span></span> <span data-ttu-id="030be-129">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="030be-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="030be-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="030be-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-131">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="030be-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="030be-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-133">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="030be-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="030be-134">值</span><span class="sxs-lookup"><span data-stu-id="030be-134">Value</span></span>                                                                                                | <span data-ttu-id="030be-135">意義</span><span class="sxs-lookup"><span data-stu-id="030be-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="030be-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="030be-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="030be-137">可復原</span><span class="sxs-lookup"><span data-stu-id="030be-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="030be-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="030be-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="030be-139">嚴重</span><span class="sxs-lookup"><span data-stu-id="030be-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="030be-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="030be-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="030be-141">時發生</span><span class="sxs-lookup"><span data-stu-id="030be-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="030be-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="030be-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="030be-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="030be-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="030be-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="030be-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="030be-146">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="030be-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="030be-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="030be-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="030be-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="030be-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-150">如果 0 (零) 則不會將此事件記錄到系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="030be-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="030be-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="030be-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-152">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="030be-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="030be-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-154">位元組陣列，其中包含系統抽象層 (SAL) 呈現給 Windows 的原始錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="030be-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="030be-155">陣列中的元素數目是由 **Size** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="030be-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="030be-156">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="030be-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-157">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="030be-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="030be-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-159">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="030be-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="030be-160">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="030be-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="030be-161">**大小**</span><span class="sxs-lookup"><span data-stu-id="030be-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="030be-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="030be-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-164">原始錯誤記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="030be-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="030be-165">**型別**</span><span class="sxs-lookup"><span data-stu-id="030be-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="030be-166">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="030be-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="030be-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="030be-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="030be-168">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="030be-168">Type of event log message.</span></span> <span data-ttu-id="030be-169">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="030be-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="030be-170">備註</span><span class="sxs-lookup"><span data-stu-id="030be-170">Remarks</span></span>

<span data-ttu-id="030be-171">**MSMCAEvent \_ InvalidError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="030be-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="030be-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="030be-172">Requirements</span></span>



| <span data-ttu-id="030be-173">需求</span><span class="sxs-lookup"><span data-stu-id="030be-173">Requirement</span></span> | <span data-ttu-id="030be-174">值</span><span class="sxs-lookup"><span data-stu-id="030be-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="030be-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="030be-175">Minimum supported client</span></span><br/> | <span data-ttu-id="030be-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="030be-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="030be-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="030be-177">Minimum supported server</span></span><br/> | <span data-ttu-id="030be-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="030be-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="030be-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="030be-179">Namespace</span></span><br/>                | <span data-ttu-id="030be-180">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="030be-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="030be-181">MOF</span><span class="sxs-lookup"><span data-stu-id="030be-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="030be-182"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="030be-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="030be-183">DLL</span><span class="sxs-lookup"><span data-stu-id="030be-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="030be-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="030be-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="030be-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="030be-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="030be-186">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="030be-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="030be-187">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="030be-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

