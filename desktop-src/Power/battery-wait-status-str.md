---
description: 包含要取出電池狀態的條件相關資訊。
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: 'BATTERY_WAIT_STATUS 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996734"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="aa977-103">電池 \_ 等待 \_ 狀態結構</span><span class="sxs-lookup"><span data-stu-id="aa977-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="aa977-104">包含要取出電池狀態的條件相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa977-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="aa977-105">此結構是由 [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md) 控制程式代碼使用。</span><span class="sxs-lookup"><span data-stu-id="aa977-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa977-106">語法</span><span class="sxs-lookup"><span data-stu-id="aa977-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="aa977-107">成員</span><span class="sxs-lookup"><span data-stu-id="aa977-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa977-108">**BatteryTag**</span><span class="sxs-lookup"><span data-stu-id="aa977-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="aa977-109">電池目前的電池標記。</span><span class="sxs-lookup"><span data-stu-id="aa977-109">The current battery tag for the battery.</span></span> <span data-ttu-id="aa977-110">只會傳回符合標記之電池的資訊。</span><span class="sxs-lookup"><span data-stu-id="aa977-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="aa977-111">每當此值與電池的目前標籤不相符時， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 作業將會失敗，並出現錯誤檔案的錯誤碼 \_ \_ \_ ，這會向呼叫者指出其具有標記的電池已不再安裝，呼叫者可能會選擇使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業來判斷新安裝電池的標記（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="aa977-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="aa977-112">此外，如果在移除電池或標記變更時要求正在進行中，則作業會中止，並出現 [ \_ \_ 找不到錯誤檔案] 的狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="aa977-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="aa977-113"> (查看 [電池標記](battery-information.md) 以取得詳細資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="aa977-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="aa977-114">**逾時**</span><span class="sxs-lookup"><span data-stu-id="aa977-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="aa977-115">在完成之前，要求會等待 **>powerstate**、 **LowCapacity** 和 **HighCapacity** 成員所指定之條件的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="aa977-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="aa977-116">值為-1 表示要求將會無限期等候，以滿足條件。</span><span class="sxs-lookup"><span data-stu-id="aa977-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="aa977-117">值為零表示要求的電池資訊會立即傳回，而不考慮其他狀況。</span><span class="sxs-lookup"><span data-stu-id="aa977-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="aa977-118">任何其他值則表示要求應該等候該時間長度，或直到滿足任何其他條件為止。</span><span class="sxs-lookup"><span data-stu-id="aa977-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="aa977-119">如果電腦進入睡眠模式，時鐘將會繼續執行，但耗盡計數不會喚醒電腦。</span><span class="sxs-lookup"><span data-stu-id="aa977-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="aa977-120">如果在電腦喚醒時，計數會耗盡，且符合其他條件，則呼叫會立即在喚醒上傳回。</span><span class="sxs-lookup"><span data-stu-id="aa977-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="aa977-121">**>powerstate**</span><span class="sxs-lookup"><span data-stu-id="aa977-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="aa977-122">零、一或多個下列狀態位，表示電池的狀態。</span><span class="sxs-lookup"><span data-stu-id="aa977-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="aa977-123">它等同于 [**電池 \_ 狀態**](battery-status-str.md)結構的 **>powerstate** 成員。</span><span class="sxs-lookup"><span data-stu-id="aa977-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="aa977-124">值</span><span class="sxs-lookup"><span data-stu-id="aa977-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="aa977-125">意義</span><span class="sxs-lookup"><span data-stu-id="aa977-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="aa977-126"><dt>**電池 \_充電**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="aa977-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="aa977-127">指出電池目前正在充電。</span><span class="sxs-lookup"><span data-stu-id="aa977-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="aa977-128"><dt>**電池 \_重大**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="aa977-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="aa977-129">指出電池故障即將發生。</span><span class="sxs-lookup"><span data-stu-id="aa977-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="aa977-130">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="aa977-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="aa977-131"><dt>**電池 \_放電**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="aa977-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="aa977-132">指出電池目前正在進行放電。</span><span class="sxs-lookup"><span data-stu-id="aa977-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="aa977-133"><dt>**電池 \_\_第 0x00000001 \_ 行電源**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aa977-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="aa977-134">指出電池可存取 AC 電源。</span><span class="sxs-lookup"><span data-stu-id="aa977-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="aa977-135">**LowCapacity**</span><span class="sxs-lookup"><span data-stu-id="aa977-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="aa977-136">目前的電池容量，以 mWh (或相對) 。</span><span class="sxs-lookup"><span data-stu-id="aa977-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="aa977-137">此值與 [**電池 \_ 狀態**](battery-status-str.md)結構的 **容量** 成員相同。</span><span class="sxs-lookup"><span data-stu-id="aa977-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aa977-138">**HighCapacity**</span><span class="sxs-lookup"><span data-stu-id="aa977-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="aa977-139">目前的電池容量，以 mWh (或相對) 。</span><span class="sxs-lookup"><span data-stu-id="aa977-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="aa977-140">此值與 [**電池 \_ 狀態**](battery-status-str.md)結構的 **容量** 成員相同。</span><span class="sxs-lookup"><span data-stu-id="aa977-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa977-141">備註</span><span class="sxs-lookup"><span data-stu-id="aa977-141">Remarks</span></span>

<span data-ttu-id="aa977-142">電池資訊的要求會延後，直到發生下列其中一種情況為止：</span><span class="sxs-lookup"><span data-stu-id="aa977-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="aa977-143">超時時間過期 (假設 **Timeout** 不是-1) 。</span><span class="sxs-lookup"><span data-stu-id="aa977-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="aa977-144">電池的目前狀態與 **>powerstate** 不符。</span><span class="sxs-lookup"><span data-stu-id="aa977-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="aa977-145">電池容量低於 **LowCapacity**。</span><span class="sxs-lookup"><span data-stu-id="aa977-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="aa977-146">電池容量高於 **HighCapacity**。</span><span class="sxs-lookup"><span data-stu-id="aa977-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="aa977-147">電池標記變更。</span><span class="sxs-lookup"><span data-stu-id="aa977-147">The battery tag changes.</span></span>

<span data-ttu-id="aa977-148">當符合上述任一條件時，便會收集資料，而作業會傳回。</span><span class="sxs-lookup"><span data-stu-id="aa977-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="aa977-149">這可讓應用程式監視一般動態電池資訊，而不需輪詢裝置。</span><span class="sxs-lookup"><span data-stu-id="aa977-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="aa977-150">使用兩種容量條件的其中之一之前，請使用 [ [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md) ] 控制項程式碼，並以零為限時，確定電池支援它們。</span><span class="sxs-lookup"><span data-stu-id="aa977-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="aa977-151">檢查結果，以判斷是否支援 **容量** 成員， (也就是，不是電池 \_ 未知 \_ 容量) 。</span><span class="sxs-lookup"><span data-stu-id="aa977-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa977-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa977-152">Requirements</span></span>



| <span data-ttu-id="aa977-153">需求</span><span class="sxs-lookup"><span data-stu-id="aa977-153">Requirement</span></span> | <span data-ttu-id="aa977-154">值</span><span class="sxs-lookup"><span data-stu-id="aa977-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa977-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa977-155">Minimum supported client</span></span><br/> | <span data-ttu-id="aa977-156">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa977-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="aa977-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa977-157">Minimum supported server</span></span><br/> | <span data-ttu-id="aa977-158">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa977-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="aa977-159">標頭</span><span class="sxs-lookup"><span data-stu-id="aa977-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa977-160"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="aa977-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa977-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa977-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa977-162">**電池 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="aa977-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="aa977-163">**IOCTL \_ 電池 \_ 查詢 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="aa977-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="aa977-164">**IOCTL \_ 電池 \_ 查詢 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="aa977-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

