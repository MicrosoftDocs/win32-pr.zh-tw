---
description: 指出電腦檢查架構 (MCA) 系統 BIOS 錯誤。 此類別僅適用于64位的 Windows 系統。
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194355"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="02b6a-104">MSMCAEvent \_ SMBIOSError 類別</span><span class="sxs-lookup"><span data-stu-id="02b6a-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="02b6a-105">**MSMCAEvent \_ SMBIOSError** 類別指出電腦檢查架構 (MCA) 系統 BIOS 錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="02b6a-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="02b6a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="02b6a-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="02b6a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="02b6a-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="02b6a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b6a-109">語法</span><span class="sxs-lookup"><span data-stu-id="02b6a-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="02b6a-110">成員</span><span class="sxs-lookup"><span data-stu-id="02b6a-110">Members</span></span>

<span data-ttu-id="02b6a-111">**MSMCAEvent \_ SMBIOSError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="02b6a-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="02b6a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="02b6a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02b6a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="02b6a-113">Properties</span></span>

<span data-ttu-id="02b6a-114">**MSMCAEvent \_ SMBIOSError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="02b6a-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02b6a-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="02b6a-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="02b6a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="02b6a-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="02b6a-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="02b6a-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-122">記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="02b6a-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-123">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="02b6a-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="02b6a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-126">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="02b6a-126">CPU that reported the error.</span></span> <span data-ttu-id="02b6a-127">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="02b6a-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="02b6a-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="02b6a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-131">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="02b6a-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="02b6a-132">值</span><span class="sxs-lookup"><span data-stu-id="02b6a-132">Value</span></span>                                                                                                | <span data-ttu-id="02b6a-133">意義</span><span class="sxs-lookup"><span data-stu-id="02b6a-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="02b6a-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="02b6a-135">可復原</span><span class="sxs-lookup"><span data-stu-id="02b6a-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="02b6a-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="02b6a-137">嚴重</span><span class="sxs-lookup"><span data-stu-id="02b6a-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="02b6a-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="02b6a-139">時發生</span><span class="sxs-lookup"><span data-stu-id="02b6a-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="02b6a-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="02b6a-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="02b6a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="02b6a-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-144">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="02b6a-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="02b6a-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="02b6a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-148">如果 0 (零) ，則此事件不會記錄到系統事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="02b6a-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-149">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="02b6a-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-150">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="02b6a-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-152">包含原始錯誤記錄的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="02b6a-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="02b6a-153">陣列中 **Size** 屬性指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="02b6a-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-154">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="02b6a-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-155">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="02b6a-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-157">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="02b6a-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="02b6a-158">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="02b6a-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-159">**大小**</span><span class="sxs-lookup"><span data-stu-id="02b6a-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-160">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="02b6a-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-162">原始錯誤記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="02b6a-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-163">**SMBIOS \_ 事件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="02b6a-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-164">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="02b6a-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-166">事件類型。</span><span class="sxs-lookup"><span data-stu-id="02b6a-166">Event type.</span></span>



| <span data-ttu-id="02b6a-167">值</span><span class="sxs-lookup"><span data-stu-id="02b6a-167">Value</span></span>                                                                                                  | <span data-ttu-id="02b6a-168">意義</span><span class="sxs-lookup"><span data-stu-id="02b6a-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="02b6a-169"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-170">保留的。</span><span class="sxs-lookup"><span data-stu-id="02b6a-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="02b6a-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-172">單一位 ECC 記憶體錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="02b6a-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-174">多個位 ECC 記憶體錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="02b6a-175"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-176">同位記憶體錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="02b6a-177"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-178">匯流排超時時間。</span><span class="sxs-lookup"><span data-stu-id="02b6a-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="02b6a-179"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-180">I/o 通道檢查。</span><span class="sxs-lookup"><span data-stu-id="02b6a-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="02b6a-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-182">軟體 NMI。</span><span class="sxs-lookup"><span data-stu-id="02b6a-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="02b6a-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-184">張貼記憶體調整大小。</span><span class="sxs-lookup"><span data-stu-id="02b6a-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="02b6a-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-186">POST 錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="02b6a-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="02b6a-188">PCI 同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="02b6a-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="02b6a-190">PCI 系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="02b6a-191"><dt>**rj-11**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="02b6a-192">CPU 失敗。</span><span class="sxs-lookup"><span data-stu-id="02b6a-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="02b6a-193"><dt>**全年**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="02b6a-194">EISA 安全計時器超時時間。</span><span class="sxs-lookup"><span data-stu-id="02b6a-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="02b6a-195"><dt>**.13**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="02b6a-196">已停用可更正的記憶體記錄檔。</span><span class="sxs-lookup"><span data-stu-id="02b6a-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="02b6a-197"><dt>**日**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="02b6a-198">已停用特定事件種類的記錄。</span><span class="sxs-lookup"><span data-stu-id="02b6a-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="02b6a-199">在短時間內收到太多相同型別的錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="02b6a-200"><dt>**15**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="02b6a-201">保留的。</span><span class="sxs-lookup"><span data-stu-id="02b6a-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="02b6a-202"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="02b6a-203">超過系統限制 (例如，超過電壓或溫度閾值) 。</span><span class="sxs-lookup"><span data-stu-id="02b6a-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="02b6a-204"><dt>**至**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="02b6a-205">非同步硬體計時器已過期，並已發出系統重設。</span><span class="sxs-lookup"><span data-stu-id="02b6a-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="02b6a-206"><dt>**達**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="02b6a-207">系統組態資訊。</span><span class="sxs-lookup"><span data-stu-id="02b6a-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="02b6a-208"><dt>**診斷**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="02b6a-209">硬碟資訊。</span><span class="sxs-lookup"><span data-stu-id="02b6a-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="02b6a-210"><dt>**名**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="02b6a-211">系統重新設定。</span><span class="sxs-lookup"><span data-stu-id="02b6a-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="02b6a-212"><dt>**21**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="02b6a-213">無法修復的 CPU-複雜錯誤。</span><span class="sxs-lookup"><span data-stu-id="02b6a-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="02b6a-214"><dt>**日**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="02b6a-215">記錄區域重設或已清除。</span><span class="sxs-lookup"><span data-stu-id="02b6a-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="02b6a-216"><dt>**上午**</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="02b6a-217">系統開機。</span><span class="sxs-lookup"><span data-stu-id="02b6a-217">System boot.</span></span> <span data-ttu-id="02b6a-218">如果已執行，則會保證此記錄專案是在任何系統開機時所寫入的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="02b6a-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="02b6a-219">**型別**</span><span class="sxs-lookup"><span data-stu-id="02b6a-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-220">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="02b6a-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-222">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="02b6a-222">Type of event log message.</span></span> <span data-ttu-id="02b6a-223">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="02b6a-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="02b6a-224">**驗證 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="02b6a-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02b6a-225">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="02b6a-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02b6a-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="02b6a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02b6a-227">用來指出後續欄位有效性的驗證位。</span><span class="sxs-lookup"><span data-stu-id="02b6a-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="02b6a-228">1 (0x1) 值表示 **SMBIOS \_ 事件** 有效。</span><span class="sxs-lookup"><span data-stu-id="02b6a-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="02b6a-229">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="02b6a-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02b6a-230">備註</span><span class="sxs-lookup"><span data-stu-id="02b6a-230">Remarks</span></span>

<span data-ttu-id="02b6a-231">**MSMCAEvent \_ SMBIOSError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="02b6a-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02b6a-232">規格需求</span><span class="sxs-lookup"><span data-stu-id="02b6a-232">Requirements</span></span>



| <span data-ttu-id="02b6a-233">需求</span><span class="sxs-lookup"><span data-stu-id="02b6a-233">Requirement</span></span> | <span data-ttu-id="02b6a-234">值</span><span class="sxs-lookup"><span data-stu-id="02b6a-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02b6a-235">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02b6a-235">Minimum supported client</span></span><br/> | <span data-ttu-id="02b6a-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="02b6a-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="02b6a-237">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02b6a-237">Minimum supported server</span></span><br/> | <span data-ttu-id="02b6a-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="02b6a-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="02b6a-239">命名空間</span><span class="sxs-lookup"><span data-stu-id="02b6a-239">Namespace</span></span><br/>                | <span data-ttu-id="02b6a-240">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="02b6a-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="02b6a-241">MOF</span><span class="sxs-lookup"><span data-stu-id="02b6a-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02b6a-242"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="02b6a-243">DLL</span><span class="sxs-lookup"><span data-stu-id="02b6a-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02b6a-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02b6a-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b6a-245">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02b6a-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b6a-246">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="02b6a-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="02b6a-247">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="02b6a-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

