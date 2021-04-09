---
description: 代表 (MCA) PCI 匯流排錯誤的機器檢查架構。 此類別僅適用于在64位 Windows 作業系統上執行的電腦。
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690368"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="9c0c0-104">MSMCAEvent \_ PCIBusError 類別</span><span class="sxs-lookup"><span data-stu-id="9c0c0-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="9c0c0-105">**MSMCAEvent \_ PCIBusError** 類別代表 (MCA) PCI 匯流排錯誤的機器檢查架構。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="9c0c0-106">此類別僅適用于在64位 Windows 作業系統上執行的電腦。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="9c0c0-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9c0c0-108">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c0c0-109">語法</span><span class="sxs-lookup"><span data-stu-id="9c0c0-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="9c0c0-110">成員</span><span class="sxs-lookup"><span data-stu-id="9c0c0-110">Members</span></span>

<span data-ttu-id="9c0c0-111">**MSMCAEvent \_ PCIBusError** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9c0c0-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="9c0c0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9c0c0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c0c0-113">屬性</span><span class="sxs-lookup"><span data-stu-id="9c0c0-113">Properties</span></span>

<span data-ttu-id="9c0c0-114">**MSMCAEvent \_ PCIBusError** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c0c0-115">**使用中**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-116">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-118">如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-120">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-122">記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-123">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-126">回報錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-126">CPU that reported the error.</span></span> <span data-ttu-id="9c0c0-127">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-129">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-131">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="9c0c0-132">值</span><span class="sxs-lookup"><span data-stu-id="9c0c0-132">Value</span></span>                                                                                                | <span data-ttu-id="9c0c0-133">意義</span><span class="sxs-lookup"><span data-stu-id="9c0c0-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9c0c0-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-135">可復原</span><span class="sxs-lookup"><span data-stu-id="9c0c0-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="9c0c0-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-137">嚴重</span><span class="sxs-lookup"><span data-stu-id="9c0c0-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="9c0c0-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-139">時發生</span><span class="sxs-lookup"><span data-stu-id="9c0c0-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c0c0-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9c0c0-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-144">此類別實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-148">如果 0 (零) ，則此事件不會記錄到系統事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-149">**PCI \_ 匯流排 \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-150">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-152">在發生事件時 PCI 匯流排上的記憶體或 i/o 位址。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="9c0c0-153">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-154">**PCI \_ 匯流排 \_ CMD**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-155">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-157">發生事件時的匯流排命令或作業。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="9c0c0-158">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-159">**PCI \_ 匯流排 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-160">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-162">發生事件時 PCI 匯流排上的資料。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="9c0c0-163">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-164">**PCI \_ 匯流排 \_ 錯誤 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-165">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-167">發生錯誤時的匯流排狀態。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="9c0c0-168">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-169">**PCI \_ 匯流排 \_ 錯誤 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-170">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-172">PCI 匯流排錯誤的類型。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="9c0c0-173">值</span><span class="sxs-lookup"><span data-stu-id="9c0c0-173">Value</span></span>                                                                                                | <span data-ttu-id="9c0c0-174">意義</span><span class="sxs-lookup"><span data-stu-id="9c0c0-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="9c0c0-175"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-176">未知或 OEM 系統的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="9c0c0-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-178">資料同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="9c0c0-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-180">系統錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="9c0c0-181"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-182">Master Abort。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="9c0c0-183"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-184">沒有任何 DEVSEL)  (的匯流排超時或裝置不存在 \# 。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="9c0c0-185"><dt>**5**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-186">主要資料同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="9c0c0-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-188">位址同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="9c0c0-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="9c0c0-190">命令同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="9c0c0-191">**PCI \_ 匯流排 \_ 識別碼 \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-192">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-194">發生錯誤之 PCI 匯流排指定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-195">**PCI \_ 匯流排 \_ 識別碼 \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-196">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-198">發生錯誤之 PCI 匯流排的指定區段識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-199">**PCI \_ 匯流排要求者 \_ \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-200">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-202">事件時的 PCI 匯流排要求者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="9c0c0-203">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-204">**PCI \_ 匯流排 \_ 回應程式 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-205">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-207">事件當時的 PCI 匯流排回應程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="9c0c0-208">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-209">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-210">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="9c0c0-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-212">位元組陣列，其中包含系統抽象層 (SAL) 呈現給 Windows 的原始錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="9c0c0-213">陣列中的元素數目是由 **Size** 屬性指定。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-214">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-215">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-217">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="9c0c0-218">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-219">**大小**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-220">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-222">原始錯誤記錄的大小。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-223">**型別**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-224">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-226">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-226">Type of event log message.</span></span> <span data-ttu-id="9c0c0-227">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="9c0c0-228">**驗證 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c0c0-229">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9c0c0-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9c0c0-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c0c0-231">用來指出後續欄位有效性的驗證位。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="9c0c0-232">值</span><span class="sxs-lookup"><span data-stu-id="9c0c0-232">Values</span></span>                                                                                  | <span data-ttu-id="9c0c0-233">意義</span><span class="sxs-lookup"><span data-stu-id="9c0c0-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="9c0c0-234"><dt>1 (0x1) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="9c0c0-235">PCI \_ 匯流排 \_ 錯誤 \_ 狀態為有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="9c0c0-236"><dt>2 (0x2) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="9c0c0-237">PCI \_ 匯流排 \_ 錯誤 \_ 類型有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="9c0c0-238"><dt>4 (0x4) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="9c0c0-239">PCI \_ 匯流排 \_ 識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="9c0c0-240"><dt>8 (0x8) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="9c0c0-241">PCI \_ 匯流排 \_ 位址有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="9c0c0-242"><dt>16 (0x10) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="9c0c0-243">PCI \_ 匯流排 \_ 資料有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="9c0c0-244"><dt>32 (0x20) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="9c0c0-245">PCI \_ 匯流排 \_ CMD 有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="9c0c0-246"><dt>64 (0x40) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="9c0c0-247">PCI \_ 匯流排要求者 \_ \_ 識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="9c0c0-248"><dt>128 (0x80) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="9c0c0-249">PCI \_ 匯流排 \_ 回應 \_ 程式識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="9c0c0-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="9c0c0-251">PCI \_ 匯流排 \_ 目標 \_ 識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="9c0c0-252"><dt>512 (0x200) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="9c0c0-253">PCI \_ 匯流排 \_ OEM \_ 識別碼有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="9c0c0-254"><dt>1024 (0x400) </dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="9c0c0-255">PCI \_ 匯流排 \_ OEM \_ 資料 \_ 結構有效。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="9c0c0-256">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c0c0-257">備註</span><span class="sxs-lookup"><span data-stu-id="9c0c0-257">Remarks</span></span>

<span data-ttu-id="9c0c0-258">**MSMCAEvent \_ PCIBusError** 類別衍生自 [**>register-wmievent**](wmievent.md)。</span><span class="sxs-lookup"><span data-stu-id="9c0c0-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c0c0-259">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c0c0-259">Requirements</span></span>



| <span data-ttu-id="9c0c0-260">需求</span><span class="sxs-lookup"><span data-stu-id="9c0c0-260">Requirement</span></span> | <span data-ttu-id="9c0c0-261">值</span><span class="sxs-lookup"><span data-stu-id="9c0c0-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c0c0-262">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c0c0-262">Minimum supported client</span></span><br/> | <span data-ttu-id="9c0c0-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9c0c0-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="9c0c0-264">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c0c0-264">Minimum supported server</span></span><br/> | <span data-ttu-id="9c0c0-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9c0c0-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="9c0c0-266">命名空間</span><span class="sxs-lookup"><span data-stu-id="9c0c0-266">Namespace</span></span><br/>                | <span data-ttu-id="9c0c0-267">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="9c0c0-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9c0c0-268">MOF</span><span class="sxs-lookup"><span data-stu-id="9c0c0-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c0c0-269"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c0c0-270">DLL</span><span class="sxs-lookup"><span data-stu-id="9c0c0-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c0c0-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c0c0-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c0c0-272">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c0c0-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c0c0-273">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="9c0c0-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9c0c0-274">**>register-wmievent**</span><span class="sxs-lookup"><span data-stu-id="9c0c0-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

