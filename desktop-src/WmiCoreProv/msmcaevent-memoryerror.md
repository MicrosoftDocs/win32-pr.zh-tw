---
description: 表示機器檢查架構 (MCA) 記憶體錯誤事件。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: MSMCAEvent_MemoryError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988365"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="cf8a1-104">MSMCAEvent \_ MemoryError 類別</span><span class="sxs-lookup"><span data-stu-id="cf8a1-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="cf8a1-105">**MSMCAEvent \_ MemoryError** 類別代表 (MCA) 記憶體錯誤事件的機器檢查架構。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="cf8a1-106">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="cf8a1-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cf8a1-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8a1-109">語法</span><span class="sxs-lookup"><span data-stu-id="cf8a1-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="cf8a1-110">成員</span><span class="sxs-lookup"><span data-stu-id="cf8a1-110">Members</span></span>

<span data-ttu-id="cf8a1-111">**MSMCAEvent \_ MemoryError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cf8a1-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="cf8a1-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cf8a1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf8a1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cf8a1-113">Properties</span></span>

<span data-ttu-id="cf8a1-114">**MSMCAEvent \_ MemoryError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf8a1-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-122">MCA 記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-123">**匯流排 \_ 特定 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-126">OEM 特定、與匯流排相關的資料。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="cf8a1-127">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-128">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-129">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-131">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-131">CPU that reported the error.</span></span> <span data-ttu-id="cf8a1-132">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-133">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-134">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-136">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="cf8a1-137">值</span><span class="sxs-lookup"><span data-stu-id="cf8a1-137">Value</span></span>                                                                                                | <span data-ttu-id="cf8a1-138">意義</span><span class="sxs-lookup"><span data-stu-id="cf8a1-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="cf8a1-139"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="cf8a1-140">可復原</span><span class="sxs-lookup"><span data-stu-id="cf8a1-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="cf8a1-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="cf8a1-142">嚴重</span><span class="sxs-lookup"><span data-stu-id="cf8a1-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="cf8a1-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="cf8a1-144">時發生</span><span class="sxs-lookup"><span data-stu-id="cf8a1-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cf8a1-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-148">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cf8a1-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-149">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-150">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-151">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-153">如果為零，則此事件不會記錄到系統事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-154">**記憶體 \_ BANK**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-157">記憶體錯誤位置的模組或順位數位。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-158">**記憶體 \_ 位 \_ 位置**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-159">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-161">包含錯誤之記憶體字組中的位位置。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-162">**記憶體 \_ 卡**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-165">記憶體錯誤位置的卡片號碼。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-166">**記憶體資料 \_ 行**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-169">記憶體錯誤位置的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-170">**記憶體 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-171">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-173">記憶體錯誤位置的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-174">**記憶體 \_ 錯誤 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-175">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-177">記憶體錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-177">Memory error status.</span></span>

<span data-ttu-id="cf8a1-178">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-179">**記憶體 \_ 模組**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-180">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-182">記憶體錯誤位置的模組或排名編號。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-183">**記憶體 \_ 節點**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-186">包含記憶體錯誤的節點。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-186">Node that contains the memory error.</span></span> <span data-ttu-id="cf8a1-187">這個屬性只適用于多節點系統。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="cf8a1-188">這個屬性是廠商特定的。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-189">**記憶體 \_ 實體 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-190">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-192">記憶體錯誤的實體位址。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-192">Physical address of the memory error.</span></span>

<span data-ttu-id="cf8a1-193">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-194">**記憶體 \_ 實體 \_ 遮罩**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-195">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-197">記憶體錯誤64位實體位址中的有效位址位。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="cf8a1-198">實體遮罩會指定實體位址的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="cf8a1-199">記憶體錯誤的實體位址取決於硬體的執行因素。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="cf8a1-200">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-201">**MEM 資料 \_ 列**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-204">記憶體錯誤位置的資料列編號。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-205">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-206">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="cf8a1-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-208">位元組陣列，其中包含系統抽象層 (SAL) 呈現給 Windows 的原始錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="cf8a1-209">陣列中的元素數目是由 **Size** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-210">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-211">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-213">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="cf8a1-214">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-215">**要求者 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-216">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-218">起始交易之裝置或元件的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="cf8a1-219">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-220">**回應程式 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-221">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-223">交易回應者的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="cf8a1-224">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-225">**大小**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-226">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-227">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-228">原始錯誤記錄的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-229">**目標 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-230">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-232">交易預定目標的硬體位址。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="cf8a1-233">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-234">**型別**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-235">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-237">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-237">Type of event log message.</span></span> <span data-ttu-id="cf8a1-238">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="cf8a1-239">**驗證 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf8a1-240">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cf8a1-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf8a1-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf8a1-242">用來指出後續欄位有效性的驗證位。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="cf8a1-243">值</span><span class="sxs-lookup"><span data-stu-id="cf8a1-243">Values</span></span>                                                                                     | <span data-ttu-id="cf8a1-244">意義</span><span class="sxs-lookup"><span data-stu-id="cf8a1-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="cf8a1-245"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="cf8a1-246">記憶體 \_ 錯誤 \_ 狀態為有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="cf8a1-247"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="cf8a1-248">MEM \_ 實體 \_ 位址有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="cf8a1-249"><dt>4 (0x4) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="cf8a1-250">MEM \_ 位址 \_ 遮罩有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="cf8a1-251"><dt>8 (0x8) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="cf8a1-252">記憶體 \_ 節點有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="cf8a1-253"><dt>16 (0x10) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="cf8a1-254">記憶體 \_ 卡有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="cf8a1-255"><dt>32 (0x20) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="cf8a1-256">記憶體 \_ 模組有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="cf8a1-257"><dt>64 (0x40) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="cf8a1-258">記憶體 \_ BANK 有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="cf8a1-259"><dt>128 (0x80) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="cf8a1-260">記憶體 \_ 裝置有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="cf8a1-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="cf8a1-262">記憶體資料 \_ 列有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="cf8a1-263"><dt>512 (0x200) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="cf8a1-264">記憶體資料 \_ 行有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="cf8a1-265"><dt>1024 (0x400) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="cf8a1-266">記憶體 \_ 位位 \_ 位置有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="cf8a1-267"><dt>2048 (0x800) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="cf8a1-268">記憶體 \_ 平臺要求者 \_ \_ 識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="cf8a1-269"><dt>4096 (0x1000) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="cf8a1-270">記憶體 \_ 平臺 \_ 回應 \_ 程式識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="cf8a1-271"><dt>8192 (0x2000) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="cf8a1-272">記憶體 \_ 平臺 \_ 目標有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="cf8a1-273"><dt>16384 (0x4000) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="cf8a1-274">記憶體 \_ 平臺 \_ 匯流排 \_ 特定 \_ 資料有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="cf8a1-275"><dt>32768 (0x8000) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="cf8a1-276">記憶體 \_ 平臺 \_ OEM \_ 識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="cf8a1-277"><dt>65536 (0x10000) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="cf8a1-278">記憶體 \_ 平臺 \_ OEM \_ 資料 \_ 結構有效。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="cf8a1-279">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf8a1-280">備註</span><span class="sxs-lookup"><span data-stu-id="cf8a1-280">Remarks</span></span>

<span data-ttu-id="cf8a1-281">**MSMCAEvent \_ MemoryError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="cf8a1-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8a1-282">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf8a1-282">Requirements</span></span>



| <span data-ttu-id="cf8a1-283">需求</span><span class="sxs-lookup"><span data-stu-id="cf8a1-283">Requirement</span></span> | <span data-ttu-id="cf8a1-284">值</span><span class="sxs-lookup"><span data-stu-id="cf8a1-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8a1-285">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf8a1-285">Minimum supported client</span></span><br/> | <span data-ttu-id="cf8a1-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf8a1-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="cf8a1-287">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf8a1-287">Minimum supported server</span></span><br/> | <span data-ttu-id="cf8a1-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf8a1-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="cf8a1-289">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf8a1-289">Namespace</span></span><br/>                | <span data-ttu-id="cf8a1-290">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="cf8a1-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="cf8a1-291">MOF</span><span class="sxs-lookup"><span data-stu-id="cf8a1-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf8a1-292"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf8a1-293">DLL</span><span class="sxs-lookup"><span data-stu-id="cf8a1-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf8a1-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf8a1-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8a1-295">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf8a1-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8a1-296">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="cf8a1-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="cf8a1-297">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="cf8a1-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

