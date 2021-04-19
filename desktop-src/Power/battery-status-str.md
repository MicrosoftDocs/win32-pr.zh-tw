---
description: 包含電池的目前狀態。
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: 'BATTERY_STATUS 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982423"
---
# <a name="battery_status-structure"></a><span data-ttu-id="a3220-103">電池 \_ 狀態結構</span><span class="sxs-lookup"><span data-stu-id="a3220-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="a3220-104">包含電池的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a3220-104">Contains the current state of the battery.</span></span> <span data-ttu-id="a3220-105">此結構是由 [**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md) 控制程式代碼使用。</span><span class="sxs-lookup"><span data-stu-id="a3220-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3220-106">語法</span><span class="sxs-lookup"><span data-stu-id="a3220-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="a3220-107">成員</span><span class="sxs-lookup"><span data-stu-id="a3220-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a3220-108">**>powerstate**</span><span class="sxs-lookup"><span data-stu-id="a3220-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="a3220-109">電池狀態。</span><span class="sxs-lookup"><span data-stu-id="a3220-109">The battery state.</span></span> <span data-ttu-id="a3220-110">這個成員可以是零、一或多個下列值。</span><span class="sxs-lookup"><span data-stu-id="a3220-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="a3220-111">值</span><span class="sxs-lookup"><span data-stu-id="a3220-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="a3220-112">意義</span><span class="sxs-lookup"><span data-stu-id="a3220-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="a3220-113"><dt>**電池 \_充電**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="a3220-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="a3220-114">指出電池目前正在充電。</span><span class="sxs-lookup"><span data-stu-id="a3220-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="a3220-115"><dt>**電池 \_重大**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="a3220-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="a3220-116">指出電池故障即將發生。</span><span class="sxs-lookup"><span data-stu-id="a3220-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="a3220-117">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="a3220-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="a3220-118"><dt>**電池 \_放電**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="a3220-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="a3220-119">指出電池目前正在進行放電。</span><span class="sxs-lookup"><span data-stu-id="a3220-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="a3220-120"><dt>**電池 \_\_第 0x00000001 \_ 行電源**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3220-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="a3220-121">指出系統可存取 AC 電源，因此沒有電池正在進行放電。</span><span class="sxs-lookup"><span data-stu-id="a3220-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a3220-122">**容量**</span><span class="sxs-lookup"><span data-stu-id="a3220-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="a3220-123">目前的電池容量，以 mWh (或相對) 。</span><span class="sxs-lookup"><span data-stu-id="a3220-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="a3220-124">此值可透過 **FullChargedCapacity** [**電池 \_ 資訊**](battery-information-str.md) 結構的成員除以，來產生「天然氣量測計」顯示。</span><span class="sxs-lookup"><span data-stu-id="a3220-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="a3220-125">如果容量無法使用，此成員會是電池 \_ 未知的 \_ 容量。</span><span class="sxs-lookup"><span data-stu-id="a3220-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="a3220-126">**電壓**</span><span class="sxs-lookup"><span data-stu-id="a3220-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="a3220-127">電池端子的目前電池電壓，以毫伏 (mv) 。</span><span class="sxs-lookup"><span data-stu-id="a3220-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="a3220-128">如果無法使用電壓，此成員會是電池 \_ 未知 \_ 電壓。</span><span class="sxs-lookup"><span data-stu-id="a3220-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="a3220-129">**速率**</span><span class="sxs-lookup"><span data-stu-id="a3220-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="a3220-130">目前的電池計量或放電的速率。</span><span class="sxs-lookup"><span data-stu-id="a3220-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="a3220-131">此值將會在毫瓦中，除非電池速率資訊是相對的，在此情況下，它將會以任意單位每小時為單位。</span><span class="sxs-lookup"><span data-stu-id="a3220-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="a3220-132">若要判斷電池資訊是否為相對，請檢查 \_ \_ [**電池 \_ 資訊**](battery-information-str.md)結構的 **功能** 成員中的電池容量相對旗標。</span><span class="sxs-lookup"><span data-stu-id="a3220-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="a3220-133">非零的正面比率表示充電;負的速率表示已放電。</span><span class="sxs-lookup"><span data-stu-id="a3220-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="a3220-134">某些電池只會報告放電費率。</span><span class="sxs-lookup"><span data-stu-id="a3220-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="a3220-135">如果無法使用速率，此成員會是電池 \_ 未知 \_ 費率。</span><span class="sxs-lookup"><span data-stu-id="a3220-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="a3220-136">如果電池或電源來源的狀態變更，速率可能會變成可用。</span><span class="sxs-lookup"><span data-stu-id="a3220-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3220-137">備註</span><span class="sxs-lookup"><span data-stu-id="a3220-137">Remarks</span></span>

<span data-ttu-id="a3220-138">\_此結構之 **>powerstate** 成員中的電池關鍵性旗標表示硬體「電池關鍵性」條件。</span><span class="sxs-lookup"><span data-stu-id="a3220-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="a3220-139">這個關鍵層級是由電池製造商設定，而不是由使用者在「電力嚴重不足警示」中設定。</span><span class="sxs-lookup"><span data-stu-id="a3220-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="a3220-140">這通常表示電池系統已計算出電池已完全耗盡，而任何正在繪製的電源超出預期。</span><span class="sxs-lookup"><span data-stu-id="a3220-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3220-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3220-141">Requirements</span></span>



| <span data-ttu-id="a3220-142">需求</span><span class="sxs-lookup"><span data-stu-id="a3220-142">Requirement</span></span> | <span data-ttu-id="a3220-143">值</span><span class="sxs-lookup"><span data-stu-id="a3220-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3220-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3220-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a3220-145">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3220-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="a3220-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3220-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a3220-147">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3220-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="a3220-148">標頭</span><span class="sxs-lookup"><span data-stu-id="a3220-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3220-149"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="a3220-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3220-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3220-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3220-151">**電池 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="a3220-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="a3220-152">**IOCTL \_ 電池 \_ 查詢 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="a3220-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 




