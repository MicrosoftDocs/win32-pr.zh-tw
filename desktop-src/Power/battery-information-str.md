---
description: 包含電池資訊。
ms.assetid: 6a236f48-5a06-4537-a769-bd68e5c0eb27
title: 'BATTERY_INFORMATION 結構 (Poclass .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 1e892a14263822ddd009b162c6343975e1689683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981572"
---
# <a name="battery_information-structure"></a><span data-ttu-id="31134-103">電池 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="31134-103">BATTERY\_INFORMATION structure</span></span>

<span data-ttu-id="31134-104">包含電池資訊。</span><span class="sxs-lookup"><span data-stu-id="31134-104">Contains battery information.</span></span> <span data-ttu-id="31134-105">當要求 BatteryInformation 資訊層級時，[ [**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md) ] 控制項程式碼會傳回這個結構。</span><span class="sxs-lookup"><span data-stu-id="31134-105">This structure is returned by the [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) control code when the BatteryInformation information level is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="31134-106">語法</span><span class="sxs-lookup"><span data-stu-id="31134-106">Syntax</span></span>


```C++
typedef struct _BATTERY_INFORMATION {
  ULONG Capabilities;
  UCHAR Technology;
  UCHAR Reserved[3];
  UCHAR Chemistry[4];
  ULONG DesignedCapacity;
  ULONG FullChargedCapacity;
  ULONG DefaultAlert1;
  ULONG DefaultAlert2;
  ULONG CriticalBias;
  ULONG CycleCount;
} BATTERY_INFORMATION, *PBATTERY_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="31134-107">成員</span><span class="sxs-lookup"><span data-stu-id="31134-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31134-108">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="31134-108">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="31134-109">電池功能。</span><span class="sxs-lookup"><span data-stu-id="31134-109">The battery capabilities.</span></span> <span data-ttu-id="31134-110">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="31134-110">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="31134-111">值</span><span class="sxs-lookup"><span data-stu-id="31134-111">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="31134-112">意義</span><span class="sxs-lookup"><span data-stu-id="31134-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CAPACITY_RELATIVE"></span><span id="battery_capacity_relative"></span><dl> <span data-ttu-id="31134-113"><dt>**電池 \_容量 \_ 相對**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="31134-113"><dt>**BATTERY\_CAPACITY\_RELATIVE**</dt> <dt>0x40000000</dt></span></span> </dl>                    | <span data-ttu-id="31134-114">指出電池容量和費率資訊是相對的，而不是任何特定的單位。</span><span class="sxs-lookup"><span data-stu-id="31134-114">Indicates that the battery capacity and rate information are relative, and not in any specific units.</span></span> <span data-ttu-id="31134-115">如果未設定此位，報表單位會是毫瓦時數 (mWh) 的容量和毫瓦 (mW) 的費率。</span><span class="sxs-lookup"><span data-stu-id="31134-115">If this bit is not set, the reporting units are milliwatt-hours (mWh) for capacity and milliwatts (mW) for rate.</span></span> <span data-ttu-id="31134-116">如果設定此位，則可以忽略其他電池檔中的所有單位參考。</span><span class="sxs-lookup"><span data-stu-id="31134-116">If this bit is set, all references to units in the other battery documentation can be ignored.</span></span> <span data-ttu-id="31134-117">所有費率資訊都會以每小時的單位回報。</span><span class="sxs-lookup"><span data-stu-id="31134-117">All rate information is reported in units per hour.</span></span> <span data-ttu-id="31134-118">例如，如果將完全收費的容量回報為100，則速率為200，表示電池將會在半小時內使用其所有容量。</span><span class="sxs-lookup"><span data-stu-id="31134-118">For example, if the fully charged capacity is reported as 100, a rate of 200 indicates that the battery will use all of its capacity in half an hour.</span></span><br/> |
| <span id="BATTERY_IS_SHORT_TERM"></span><span id="battery_is_short_term"></span><dl> <span data-ttu-id="31134-119"><dt>**電池 \_是 \_ 短期 \_**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="31134-119"><dt>**BATTERY\_IS\_SHORT\_TERM**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="31134-120">表示正常作業適用于不安全的函式。</span><span class="sxs-lookup"><span data-stu-id="31134-120">Indicates that the normal operation is for a fail-safe function.</span></span> <span data-ttu-id="31134-121">如果未設定此位，則應該在正常系統使用期間使用電池。</span><span class="sxs-lookup"><span data-stu-id="31134-121">If this bit is not set the battery is expected to be used during normal system usage.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="BATTERY_SET_CHARGE_SUPPORTED"></span><span id="battery_set_charge_supported"></span><dl> <span data-ttu-id="31134-122"><dt>**電池 \_設定 \_ \_ 支援的費用**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="31134-122"><dt>**BATTERY\_SET\_CHARGE\_SUPPORTED**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="31134-123">指出此電池裝置支援 BatteryCharge 類型的設定資訊要求。</span><span class="sxs-lookup"><span data-stu-id="31134-123">Indicates that set information requests of the type BatteryCharge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="BATTERY_SET_DISCHARGE_SUPPORTED"></span><span id="battery_set_discharge_supported"></span><dl> <span data-ttu-id="31134-124"><dt>**電池 \_設定 \_ 放電 \_ 支援**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="31134-124"><dt>**BATTERY\_SET\_DISCHARGE\_SUPPORTED**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="31134-125">指出此電池裝置支援 BatteryDischarge 類型的設定資訊要求。</span><span class="sxs-lookup"><span data-stu-id="31134-125">Indicates that set information requests of the type BatteryDischarge are supported by this battery device.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="BATTERY_SYSTEM_BATTERY"></span><span id="battery_system_battery"></span><dl> <span data-ttu-id="31134-126"><dt>**電池 \_系統 \_ 電池**</dt>的 <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="31134-126"><dt>**BATTERY\_SYSTEM\_BATTERY**</dt> <dt>0x80000000</dt></span></span> </dl>                             | <span data-ttu-id="31134-127">指出電池可提供一般電源來執行系統。</span><span class="sxs-lookup"><span data-stu-id="31134-127">Indicates that the battery can provide general power to run the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="31134-128">**技術**</span><span class="sxs-lookup"><span data-stu-id="31134-128">**Technology**</span></span>
</dt> <dd>

<span data-ttu-id="31134-129">電池技術。</span><span class="sxs-lookup"><span data-stu-id="31134-129">The battery technology.</span></span> <span data-ttu-id="31134-130">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="31134-130">This member can be one of the following values.</span></span>



| <span data-ttu-id="31134-131">值</span><span class="sxs-lookup"><span data-stu-id="31134-131">Value</span></span>                                                                        | <span data-ttu-id="31134-132">意義</span><span class="sxs-lookup"><span data-stu-id="31134-132">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="31134-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31134-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="31134-134">Nonrechargeable 電池，例如，鹼性。</span><span class="sxs-lookup"><span data-stu-id="31134-134">Nonrechargeable battery, for example, alkaline.</span></span><br/> |
| <dl> <span data-ttu-id="31134-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="31134-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="31134-136">充電電池，例如潛在客戶 acid。</span><span class="sxs-lookup"><span data-stu-id="31134-136">Rechargeable battery, for example, lead acid.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="31134-137">**已保留**</span><span class="sxs-lookup"><span data-stu-id="31134-137">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="31134-138">保留的。</span><span class="sxs-lookup"><span data-stu-id="31134-138">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="31134-139">**化學**</span><span class="sxs-lookup"><span data-stu-id="31134-139">**Chemistry**</span></span>
</dt> <dd>

<span data-ttu-id="31134-140">表示電池化學的縮寫字元字串。</span><span class="sxs-lookup"><span data-stu-id="31134-140">An abbreviated character string that indicates the battery's chemistry.</span></span> <span data-ttu-id="31134-141">這個字串不一定是以零結束。</span><span class="sxs-lookup"><span data-stu-id="31134-141">This string is not necessarily zero-terminated.</span></span> <span data-ttu-id="31134-142">以下是可傳回的縮寫部分清單，以及相關聯的 chemistries。</span><span class="sxs-lookup"><span data-stu-id="31134-142">The following is a partial list of abbreviations that can be returned and the associated chemistries.</span></span>



| <span data-ttu-id="31134-143">Unicode 字串</span><span class="sxs-lookup"><span data-stu-id="31134-143">Unicode string</span></span>                                                                                                                                           | <span data-ttu-id="31134-144">意義</span><span class="sxs-lookup"><span data-stu-id="31134-144">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="PbAc"></span><span id="pbac"></span><span id="PBAC"></span><dl> <span data-ttu-id="31134-145"><dt>**PbAc**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-145"><dt>**PbAc**</dt></span></span> </dl> | <span data-ttu-id="31134-146">潛在客戶 Acid</span><span class="sxs-lookup"><span data-stu-id="31134-146">Lead Acid</span></span><br/>                       |
| <span id="LION"></span><span id="lion"></span><dl> <span data-ttu-id="31134-147"><dt>**獅子**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-147"><dt>**LION**</dt></span></span> </dl>                        | <span data-ttu-id="31134-148">鋰離子</span><span class="sxs-lookup"><span data-stu-id="31134-148">Lithium Ion</span></span><br/>                     |
| <span id="Li-I"></span><span id="li-i"></span><span id="LI-I"></span><dl> <span data-ttu-id="31134-149"><dt>**Li**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-149"><dt>**Li-I**</dt></span></span> </dl> | <span data-ttu-id="31134-150">鋰離子</span><span class="sxs-lookup"><span data-stu-id="31134-150">Lithium Ion</span></span><br/>                     |
| <span id="NiCd"></span><span id="nicd"></span><span id="NICD"></span><dl> <span data-ttu-id="31134-151"><dt>**NiCd**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-151"><dt>**NiCd**</dt></span></span> </dl> | <span data-ttu-id="31134-152">五分錢鎘</span><span class="sxs-lookup"><span data-stu-id="31134-152">Nickel Cadmium</span></span><br/>                  |
| <span id="NiMH"></span><span id="nimh"></span><span id="NIMH"></span><dl> <span data-ttu-id="31134-153"><dt>**Nimh**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-153"><dt>**NiMH**</dt></span></span> </dl> | <span data-ttu-id="31134-154">五分錢金屬氫化</span><span class="sxs-lookup"><span data-stu-id="31134-154">Nickel Metal Hydride</span></span><br/>            |
| <span id="NiZn"></span><span id="nizn"></span><span id="NIZN"></span><dl> <span data-ttu-id="31134-155"><dt>**NiZn**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-155"><dt>**NiZn**</dt></span></span> </dl> | <span data-ttu-id="31134-156">五分錢 Zinc</span><span class="sxs-lookup"><span data-stu-id="31134-156">Nickel Zinc</span></span><br/>                     |
| <span id="RAM"></span><span id="ram"></span><dl> <span data-ttu-id="31134-157"><dt>**RAM**</dt></span><span class="sxs-lookup"><span data-stu-id="31134-157"><dt>**RAM**</dt></span></span> </dl>                           | <span data-ttu-id="31134-158">充電 Alkaline-Manganese</span><span class="sxs-lookup"><span data-stu-id="31134-158">Rechargeable Alkaline-Manganese</span></span><br/> |



 

<span data-ttu-id="31134-159">未來可能會出現其他 chemistries，且您的程式碼應該能夠處理它們。</span><span class="sxs-lookup"><span data-stu-id="31134-159">Other chemistries may appear in the future and your code should be able to handle them.</span></span>

</dd> <dt>

<span data-ttu-id="31134-160">**DesignedCapacity**</span><span class="sxs-lookup"><span data-stu-id="31134-160">**DesignedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="31134-161">在 mWh 時的最新電池容量，除非 \_ 已設定電池容量 \_ 相對。</span><span class="sxs-lookup"><span data-stu-id="31134-161">The theoretical capacity of the battery when new, in mWh unless BATTERY\_CAPACITY\_RELATIVE is set.</span></span> <span data-ttu-id="31134-162">在此情況下，單位是未定義的。</span><span class="sxs-lookup"><span data-stu-id="31134-162">In that case, the units are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="31134-163">**FullChargedCapacity**</span><span class="sxs-lookup"><span data-stu-id="31134-163">**FullChargedCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="31134-164">MWh (或相對) 中電池的目前完全收費容量。</span><span class="sxs-lookup"><span data-stu-id="31134-164">The battery's current fully charged capacity in mWh (or relative).</span></span> <span data-ttu-id="31134-165">比較此值與 **DesignedCapacity** ，以預估電池的損耗。</span><span class="sxs-lookup"><span data-stu-id="31134-165">Compare this value to **DesignedCapacity** to estimate the battery's wear.</span></span>

</dd> <dt>

<span data-ttu-id="31134-166">**DefaultAlert1**</span><span class="sxs-lookup"><span data-stu-id="31134-166">**DefaultAlert1**</span></span>
</dt> <dd>

<span data-ttu-id="31134-167">製造商的建議容量（以 mWh），也就是電力偏低的警示。</span><span class="sxs-lookup"><span data-stu-id="31134-167">The manufacturer's suggested capacity, in mWh, at which a low battery alert should occur.</span></span> <span data-ttu-id="31134-168">[低] 的定義會因製造商而異。</span><span class="sxs-lookup"><span data-stu-id="31134-168">Definitions of low vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="31134-169">一般情況下，會在低狀態之前發生警告狀態，但您不應該假設它一律會發生。</span><span class="sxs-lookup"><span data-stu-id="31134-169">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="31134-170">為了降低資料遺失的風險，通常會使用此值做為重大電池警示的預設設定。</span><span class="sxs-lookup"><span data-stu-id="31134-170">To reduce risk of data loss, this value is usually used as the default setting for the critical battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="31134-171">**DefaultAlert2**</span><span class="sxs-lookup"><span data-stu-id="31134-171">**DefaultAlert2**</span></span>
</dt> <dd>

<span data-ttu-id="31134-172">製造商的建議容量（以 mWh），此時會出現警告電池警示。</span><span class="sxs-lookup"><span data-stu-id="31134-172">The manufacturer's suggested capacity, in mWh, at which a warning battery alert should occur.</span></span> <span data-ttu-id="31134-173">警告的定義會因製造商而異。</span><span class="sxs-lookup"><span data-stu-id="31134-173">Definitions of warning vary from manufacturer to manufacturer.</span></span> <span data-ttu-id="31134-174">一般情況下，會在低狀態之前發生警告狀態，但您不應該假設它一律會發生。</span><span class="sxs-lookup"><span data-stu-id="31134-174">In general, a warning state will occur before a low state, but you should not assume that it always will.</span></span> <span data-ttu-id="31134-175">為了降低資料遺失的風險，通常會使用此值做為低電池警示的預設設定。</span><span class="sxs-lookup"><span data-stu-id="31134-175">To reduce risk of data loss, this value is usually used as the default setting for the low battery alarm.</span></span>

</dd> <dt>

<span data-ttu-id="31134-176">**CriticalBias**</span><span class="sxs-lookup"><span data-stu-id="31134-176">**CriticalBias**</span></span>
</dt> <dd>

<span data-ttu-id="31134-177">從零到 mWh 的偏差，這會套用到電池報告。</span><span class="sxs-lookup"><span data-stu-id="31134-177">A bias from zero, in mWh, which is applied to battery reporting.</span></span> <span data-ttu-id="31134-178">某些電池會保留一小部分，並將電池的容量值偏低，以將 "0" 顯示為電力偏高等級。</span><span class="sxs-lookup"><span data-stu-id="31134-178">Some batteries reserve a small charge that is biased out of the battery's capacity values to show "0" as the critical battery level.</span></span> <span data-ttu-id="31134-179">重大偏差類似于設定燃料量測計，以在有數個偏升的燃料時顯示「空白」。</span><span class="sxs-lookup"><span data-stu-id="31134-179">Critical bias is analogous to setting a fuel gauge to show "empty" when there are several liters of fuel left.</span></span>

</dd> <dt>

<span data-ttu-id="31134-180">**CycleCount**</span><span class="sxs-lookup"><span data-stu-id="31134-180">**CycleCount**</span></span>
</dt> <dd>

<span data-ttu-id="31134-181">電池所經歷的收費/放電週期數。</span><span class="sxs-lookup"><span data-stu-id="31134-181">The number of charge/discharge cycles the battery has experienced.</span></span> <span data-ttu-id="31134-182">這提供了一種方法來判斷電池磨損。</span><span class="sxs-lookup"><span data-stu-id="31134-182">This provides a means to determine the battery's wear.</span></span> <span data-ttu-id="31134-183">如果電池不支援迴圈計數器，此成員為零。</span><span class="sxs-lookup"><span data-stu-id="31134-183">If the battery does not support a cycle counter, this member is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31134-184">備註</span><span class="sxs-lookup"><span data-stu-id="31134-184">Remarks</span></span>

<span data-ttu-id="31134-185">警告狀態通常會在低狀態之前發生，但您不應該假設它將會。</span><span class="sxs-lookup"><span data-stu-id="31134-185">Generally, a warning state occurs before a low state, but you should not assume it will.</span></span> <span data-ttu-id="31134-186">您可以輪詢電池並找出未發生警示等級，然後再次輪詢電池，並找出這兩個層級達到的程度。</span><span class="sxs-lookup"><span data-stu-id="31134-186">It is possible to poll a battery and find that neither alert level has occurred, and poll the battery again and find it discharged to the extent that both levels have been achieved.</span></span> <span data-ttu-id="31134-187">這可能表示您的輪詢頻率不足。</span><span class="sxs-lookup"><span data-stu-id="31134-187">This may indicate that you are not polling often enough.</span></span> <span data-ttu-id="31134-188">這也可能表示電池無法維持很長的費用，而且正在進行比預期更快的放電。</span><span class="sxs-lookup"><span data-stu-id="31134-188">It may also indicate that the battery is unable to hold a charge for very long and is discharging more rapidly than you expected.</span></span> <span data-ttu-id="31134-189">這類電池可能會接近其使用年限的結尾，或可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="31134-189">Such a battery may be nearing the end of its useful life, or it may be damaged.</span></span>

## <a name="requirements"></a><span data-ttu-id="31134-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="31134-190">Requirements</span></span>



| <span data-ttu-id="31134-191">需求</span><span class="sxs-lookup"><span data-stu-id="31134-191">Requirement</span></span> | <span data-ttu-id="31134-192">值</span><span class="sxs-lookup"><span data-stu-id="31134-192">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31134-193">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31134-193">Minimum supported client</span></span><br/> | <span data-ttu-id="31134-194">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31134-194">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="31134-195">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31134-195">Minimum supported server</span></span><br/> | <span data-ttu-id="31134-196">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31134-196">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="31134-197">標頭</span><span class="sxs-lookup"><span data-stu-id="31134-197">Header</span></span><br/>                   | <dl> <span data-ttu-id="31134-198"><dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt></span><span class="sxs-lookup"><span data-stu-id="31134-198"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31134-199">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31134-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31134-200">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="31134-200">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)
</dt> </dl>

 

 




