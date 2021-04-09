---
description: Win32 \_ 時區&\# 8194;WMI 類別代表執行 Windows 之電腦系統的時區資訊，其中包含轉換成日光節約時間轉換所需的變更。
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Win32_TimeZone 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847240"
---
# <a name="win32_timezone-class"></a><span data-ttu-id="069c9-103">Win32 \_ 時區類別</span><span class="sxs-lookup"><span data-stu-id="069c9-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="069c9-104">**Win32 \_ 時區** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 之電腦系統的時區資訊，其中包含轉換成日光節約時間轉換所需的變更。</span><span class="sxs-lookup"><span data-stu-id="069c9-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="069c9-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="069c9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="069c9-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="069c9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="069c9-107">語法</span><span class="sxs-lookup"><span data-stu-id="069c9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a><span data-ttu-id="069c9-108">成員</span><span class="sxs-lookup"><span data-stu-id="069c9-108">Members</span></span>

<span data-ttu-id="069c9-109">**Win32 \_ 時區** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="069c9-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="069c9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="069c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="069c9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="069c9-111">Properties</span></span>

<span data-ttu-id="069c9-112">**Win32 \_ 時區** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="069c9-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="069c9-113">**偏差**</span><span class="sxs-lookup"><span data-stu-id="069c9-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-114">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-116">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| 偏差」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) </span><span class="sxs-lookup"><span data-stu-id="069c9-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-117">本地時間轉譯的目前偏差。</span><span class="sxs-lookup"><span data-stu-id="069c9-117">Current bias for local time translation.</span></span> <span data-ttu-id="069c9-118">偏差是國際標準時間 (UTC) 和本地時間之間的差異。</span><span class="sxs-lookup"><span data-stu-id="069c9-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="069c9-119">UTC 和本地時間之間的所有翻譯都是根據下列公式： UTC = 本地時間偏差。</span><span class="sxs-lookup"><span data-stu-id="069c9-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="069c9-120">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="069c9-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="069c9-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="069c9-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069c9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-124">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="069c9-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="069c9-125">目前物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="069c9-125">Short textual description of the current object.</span></span>

<span data-ttu-id="069c9-126">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="069c9-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="069c9-127">**DaylightBias**</span><span class="sxs-lookup"><span data-stu-id="069c9-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-128">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-130">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightBias」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) </span><span class="sxs-lookup"><span data-stu-id="069c9-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-131">在日光節約時間發生的本地時間轉譯期間所使用的偏差值。</span><span class="sxs-lookup"><span data-stu-id="069c9-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="069c9-132">如果未提供 **DaylightDay** 屬性的值，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="069c9-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="069c9-133">這個屬性的值會新增至 **偏差** 屬性，以形成日光節約時間所使用的偏差。</span><span class="sxs-lookup"><span data-stu-id="069c9-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="069c9-134">在大部分的時區中，此屬性的值為-60。</span><span class="sxs-lookup"><span data-stu-id="069c9-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="069c9-135">**DaylightDay**</span><span class="sxs-lookup"><span data-stu-id="069c9-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-136">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-138">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wDay" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-139">當此作業系統發生從標準時間到日光節約時間的轉換時， **DaylightMonth** 的 **DaylightDayOfWeek** 。</span><span class="sxs-lookup"><span data-stu-id="069c9-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="069c9-140">範例：如果轉換日 (**DaylightDayOfWeek**) 發生在星期日，則值 "1" 表示 **DaylightMonth** 的第一個星期日，"2" 表示第二個星期日，依此類推。</span><span class="sxs-lookup"><span data-stu-id="069c9-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="069c9-141">值 "5" 表示當月的最後一個 **DaylightDayOfWeek** 。</span><span class="sxs-lookup"><span data-stu-id="069c9-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="069c9-142">**DaylightDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="069c9-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-143">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="069c9-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-145">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wDayOfWeek" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-146">從標準時間到日光節約時間的轉換在作業系統上進行轉換時的星期幾。</span><span class="sxs-lookup"><span data-stu-id="069c9-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="069c9-147">**星期日** (0) </span><span class="sxs-lookup"><span data-stu-id="069c9-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="069c9-148">**星期一** (1) </span><span class="sxs-lookup"><span data-stu-id="069c9-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="069c9-149">**星期二** (2) </span><span class="sxs-lookup"><span data-stu-id="069c9-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="069c9-150">**星期三** (3) </span><span class="sxs-lookup"><span data-stu-id="069c9-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="069c9-151">**星期四** (4) </span><span class="sxs-lookup"><span data-stu-id="069c9-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="069c9-152">**星期五** (5) </span><span class="sxs-lookup"><span data-stu-id="069c9-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="069c9-153">**星期六** (6) </span><span class="sxs-lookup"><span data-stu-id="069c9-153">**Saturday** (6)</span></span>


<span data-ttu-id="069c9-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="069c9-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="069c9-155">範例：1</span><span class="sxs-lookup"><span data-stu-id="069c9-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="069c9-156">**DaylightHour**</span><span class="sxs-lookup"><span data-stu-id="069c9-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-159">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wHour" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-160">從標準時間到日光節約時間的轉換在作業系統上進行轉換的一天中的小時。</span><span class="sxs-lookup"><span data-stu-id="069c9-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-161">範例：2</span><span class="sxs-lookup"><span data-stu-id="069c9-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="069c9-162">**DaylightMillisecond**</span><span class="sxs-lookup"><span data-stu-id="069c9-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-163">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-165">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wMilliseconds" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-166">從標準時間到日光節約時間的轉換在作業系統上進行轉換時的 **DaylightSecond** 毫秒。</span><span class="sxs-lookup"><span data-stu-id="069c9-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="069c9-167">**DaylightMinute**</span><span class="sxs-lookup"><span data-stu-id="069c9-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-170">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wMinute" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-171">從標準時間到日光節約時間的轉換在作業系統上進行轉換時的 **DaylightHour** 分鐘。</span><span class="sxs-lookup"><span data-stu-id="069c9-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-172">範例：59</span><span class="sxs-lookup"><span data-stu-id="069c9-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="069c9-173">**DaylightMonth**</span><span class="sxs-lookup"><span data-stu-id="069c9-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-176">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wMonth" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-177">從標準時間到日光節約時間的轉換發生在作業系統上的月份。</span><span class="sxs-lookup"><span data-stu-id="069c9-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="069c9-178">1 **月** (1) </span><span class="sxs-lookup"><span data-stu-id="069c9-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="069c9-179">**二月** (2) </span><span class="sxs-lookup"><span data-stu-id="069c9-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="069c9-180">3 **月** (3) </span><span class="sxs-lookup"><span data-stu-id="069c9-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="069c9-181">**四月** (4) </span><span class="sxs-lookup"><span data-stu-id="069c9-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="069c9-182">5 **月** (5) </span><span class="sxs-lookup"><span data-stu-id="069c9-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="069c9-183">6 **月** (6) </span><span class="sxs-lookup"><span data-stu-id="069c9-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="069c9-184">7 **月** (7) </span><span class="sxs-lookup"><span data-stu-id="069c9-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="069c9-185">8 **月** (8) </span><span class="sxs-lookup"><span data-stu-id="069c9-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="069c9-186">9 **月** (9) </span><span class="sxs-lookup"><span data-stu-id="069c9-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="069c9-187">10 **月** (10) </span><span class="sxs-lookup"><span data-stu-id="069c9-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="069c9-188">11 **月** (11) </span><span class="sxs-lookup"><span data-stu-id="069c9-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="069c9-189">12 **月** (12) </span><span class="sxs-lookup"><span data-stu-id="069c9-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069c9-190">**DaylightName**</span><span class="sxs-lookup"><span data-stu-id="069c9-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069c9-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-193">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| DaylightName" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-194">當日光節約時間生效時，所要表示的時區。</span><span class="sxs-lookup"><span data-stu-id="069c9-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="069c9-195">範例： "EDT" (東部日光節約時間) </span><span class="sxs-lookup"><span data-stu-id="069c9-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="069c9-196">**DaylightSecond**</span><span class="sxs-lookup"><span data-stu-id="069c9-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-199">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| wSecond" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-200">從標準時間到日光節約時間的轉換在作業系統上進行轉換時， **DaylightMinute** 的第二個。</span><span class="sxs-lookup"><span data-stu-id="069c9-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-201">範例：59</span><span class="sxs-lookup"><span data-stu-id="069c9-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="069c9-202">**DaylightYear**</span><span class="sxs-lookup"><span data-stu-id="069c9-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-203">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-205">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| daylightdate.wyear \| daylightdate.wyear" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-206">日光節約時間生效的年份。</span><span class="sxs-lookup"><span data-stu-id="069c9-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="069c9-207">這個屬性不是必要的。</span><span class="sxs-lookup"><span data-stu-id="069c9-207">This property is not required.</span></span>

<span data-ttu-id="069c9-208">範例：1997</span><span class="sxs-lookup"><span data-stu-id="069c9-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="069c9-209">**說明**</span><span class="sxs-lookup"><span data-stu-id="069c9-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069c9-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="069c9-212">目前物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="069c9-212">Textual description of the current object.</span></span>

<span data-ttu-id="069c9-213">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="069c9-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="069c9-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="069c9-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069c9-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-217">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) </span><span class="sxs-lookup"><span data-stu-id="069c9-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="069c9-218">已知目前物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="069c9-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="069c9-219">這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="069c9-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="069c9-220">**StandardBias**</span><span class="sxs-lookup"><span data-stu-id="069c9-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-221">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-223">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 時間結構 \| [**時區 \_ \_ 資訊**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardBias」 ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「分鐘」 ) </span><span class="sxs-lookup"><span data-stu-id="069c9-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-224">日光節約時間未生效時要使用的偏差值。</span><span class="sxs-lookup"><span data-stu-id="069c9-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="069c9-225">如果未提供 **StandardDay** 的值，則會忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="069c9-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="069c9-226">這個屬性的值會加入至 **偏差** 屬性，以在標準時間內形成偏差。</span><span class="sxs-lookup"><span data-stu-id="069c9-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="069c9-227">範例：0</span><span class="sxs-lookup"><span data-stu-id="069c9-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="069c9-228">**StandardDay**</span><span class="sxs-lookup"><span data-stu-id="069c9-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-229">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-231">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wDay" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-232">當作業系統上的日光節約時間轉換成標準時間時， **StandardMonth** 的 **StandardDayOfWeek** 。</span><span class="sxs-lookup"><span data-stu-id="069c9-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-233">如果轉換日 (**StandardDayOfWeek**) 發生在星期日，則值 "1" 表示 **StandardMonth** 的第一個星期日，"2" 表示第二個星期日，依此類推。</span><span class="sxs-lookup"><span data-stu-id="069c9-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="069c9-234">值 "5" 表示當月的最後一個 **StandardDayOfWeek** 。</span><span class="sxs-lookup"><span data-stu-id="069c9-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="069c9-235">**StandardDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="069c9-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-236">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="069c9-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-238">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wDayOfWeek" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-239">當作業系統上的日光節約時間轉換為標準時間時，該周的第幾天。</span><span class="sxs-lookup"><span data-stu-id="069c9-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="069c9-240">**星期日** (0) </span><span class="sxs-lookup"><span data-stu-id="069c9-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="069c9-241">**星期一** (1) </span><span class="sxs-lookup"><span data-stu-id="069c9-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="069c9-242">**星期二** (2) </span><span class="sxs-lookup"><span data-stu-id="069c9-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="069c9-243">**星期三** (3) </span><span class="sxs-lookup"><span data-stu-id="069c9-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="069c9-244">**星期四** (4) </span><span class="sxs-lookup"><span data-stu-id="069c9-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="069c9-245">**星期五** (5) </span><span class="sxs-lookup"><span data-stu-id="069c9-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="069c9-246">**星期六** (6) </span><span class="sxs-lookup"><span data-stu-id="069c9-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069c9-247">**StandardHour**</span><span class="sxs-lookup"><span data-stu-id="069c9-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-248">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-250">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wHour" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-251">從日光節約時間轉換到標準時間時，在作業系統上進行轉換的一天中的小時。</span><span class="sxs-lookup"><span data-stu-id="069c9-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-252">範例：11</span><span class="sxs-lookup"><span data-stu-id="069c9-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="069c9-253">**StandardMillisecond**</span><span class="sxs-lookup"><span data-stu-id="069c9-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-254">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-256">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wMilliseconds" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-257">從日光節約時間轉換到標準時間時的 **StandardSecond** 毫秒。</span><span class="sxs-lookup"><span data-stu-id="069c9-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="069c9-258">**StandardMinute**</span><span class="sxs-lookup"><span data-stu-id="069c9-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-259">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-261">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wMinute" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-262">從日光節約時間轉換到標準時間的 **StandardDay** 時，在作業系統上進行轉換時的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="069c9-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-263">範例：59</span><span class="sxs-lookup"><span data-stu-id="069c9-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="069c9-264">**StandardMonth**</span><span class="sxs-lookup"><span data-stu-id="069c9-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-265">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-267">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wMonth" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-268">從日光節約時間轉換到標準時間時，在作業系統上進行轉換的月份。</span><span class="sxs-lookup"><span data-stu-id="069c9-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="069c9-269">1 **月** (1) </span><span class="sxs-lookup"><span data-stu-id="069c9-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="069c9-270">**二月** (2) </span><span class="sxs-lookup"><span data-stu-id="069c9-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="069c9-271">3 **月** (3) </span><span class="sxs-lookup"><span data-stu-id="069c9-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="069c9-272">**四月** (4) </span><span class="sxs-lookup"><span data-stu-id="069c9-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="069c9-273">5 **月** (5) </span><span class="sxs-lookup"><span data-stu-id="069c9-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="069c9-274">6 **月** (6) </span><span class="sxs-lookup"><span data-stu-id="069c9-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="069c9-275">7 **月** (7) </span><span class="sxs-lookup"><span data-stu-id="069c9-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="069c9-276">8 **月** (8) </span><span class="sxs-lookup"><span data-stu-id="069c9-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="069c9-277">9 **月** (9) </span><span class="sxs-lookup"><span data-stu-id="069c9-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="069c9-278">10 **月** (10) </span><span class="sxs-lookup"><span data-stu-id="069c9-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="069c9-279">11 **月** (11) </span><span class="sxs-lookup"><span data-stu-id="069c9-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="069c9-280">12 **月** (12) </span><span class="sxs-lookup"><span data-stu-id="069c9-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="069c9-281">**StandardName**</span><span class="sxs-lookup"><span data-stu-id="069c9-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="069c9-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-284">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-285">標準時間生效時所表示的時區名稱。</span><span class="sxs-lookup"><span data-stu-id="069c9-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="069c9-286">範例： "EST" (東部標準時間) </span><span class="sxs-lookup"><span data-stu-id="069c9-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="069c9-287">**StandardSecond**</span><span class="sxs-lookup"><span data-stu-id="069c9-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-288">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-290">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| wSecond" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-291">**StandardMinute** 從日光節約時間轉換到標準時間時，在作業系統上進行轉換的第二個。</span><span class="sxs-lookup"><span data-stu-id="069c9-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="069c9-292">範例：59</span><span class="sxs-lookup"><span data-stu-id="069c9-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="069c9-293">**StandardYear**</span><span class="sxs-lookup"><span data-stu-id="069c9-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="069c9-294">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="069c9-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="069c9-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="069c9-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="069c9-296">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| time 結構 \| [**time \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| standarddate.wyear \| daylightdate.wyear" ) </span><span class="sxs-lookup"><span data-stu-id="069c9-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="069c9-297">當標準時間生效時的年份。</span><span class="sxs-lookup"><span data-stu-id="069c9-297">Year when standard time is in effect.</span></span> <span data-ttu-id="069c9-298">這個屬性不是必要的。</span><span class="sxs-lookup"><span data-stu-id="069c9-298">This property is not required.</span></span>

<span data-ttu-id="069c9-299">範例：1997</span><span class="sxs-lookup"><span data-stu-id="069c9-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="069c9-300">備註</span><span class="sxs-lookup"><span data-stu-id="069c9-300">Remarks</span></span>

<span data-ttu-id="069c9-301">**Win32 \_ 時區** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。</span><span class="sxs-lookup"><span data-stu-id="069c9-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="069c9-302">撰寫 WMI 查詢時，您不能使用標準日期時間格式，例如10/18/2002。</span><span class="sxs-lookup"><span data-stu-id="069c9-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="069c9-303">相反地，您必須將查詢中使用的任何日期轉換為 UTC 格式。</span><span class="sxs-lookup"><span data-stu-id="069c9-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="069c9-304">這需要兩個步驟： 1) 您必須判斷您的時區和格林威治標準時間之間的時差 (差異（以分鐘為) 單位），以及 2) 您必須將10/18/2002 轉換成 UTC 值。</span><span class="sxs-lookup"><span data-stu-id="069c9-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="069c9-305">判斷與格林尼治平均時間的位移</span><span class="sxs-lookup"><span data-stu-id="069c9-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="069c9-306">無可否認地，WMI 讓您難以處理日期和時間;幸運的是，WMI 至少能讓您輕鬆判斷您的時區和格林威治標準時間之間的時差。</span><span class="sxs-lookup"><span data-stu-id="069c9-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="069c9-307">WMI 類別 Win32 \_ 時區包含會傳回 GMT 位移的屬性偏差。</span><span class="sxs-lookup"><span data-stu-id="069c9-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



<span data-ttu-id="069c9-308">將日期轉換為 UTC 值</span><span class="sxs-lookup"><span data-stu-id="069c9-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="069c9-309">決定 GMT 時差之後，您必須將標準日期（例如10/18/2002）轉換成 UTC 日期。</span><span class="sxs-lookup"><span data-stu-id="069c9-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="069c9-310">若要將標準日期轉換成 UTC 日期，您可以使用 VBScript 日期函數（例如年、月和日）來隔離組成 UTC 日期的個別元件。</span><span class="sxs-lookup"><span data-stu-id="069c9-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="069c9-311">當這些元件有個別值之後，您可以使用與任何其他字串值相同的方式來串連它們。</span><span class="sxs-lookup"><span data-stu-id="069c9-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="069c9-312">UTC 日期會視為字串，因為 GMT 位移必須附加至結尾。</span><span class="sxs-lookup"><span data-stu-id="069c9-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="069c9-313">如果日期顯示為數字，則此值為：</span><span class="sxs-lookup"><span data-stu-id="069c9-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="069c9-314">為了清楚) 起見，會錯誤地將錯誤地視為數學方程式 (括弧：</span><span class="sxs-lookup"><span data-stu-id="069c9-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="069c9-315">例如，在日期10/18/2002 中，個別的元件為：</span><span class="sxs-lookup"><span data-stu-id="069c9-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="069c9-316">年：2002</span><span class="sxs-lookup"><span data-stu-id="069c9-316">Year: 2002</span></span>
-   <span data-ttu-id="069c9-317">月：10</span><span class="sxs-lookup"><span data-stu-id="069c9-317">Month: 10</span></span>
-   <span data-ttu-id="069c9-318">Day：18</span><span class="sxs-lookup"><span data-stu-id="069c9-318">Day: 18</span></span>

<span data-ttu-id="069c9-319">腳本必須結合這三個值，字串 "113047.000000" (代表時間，包括毫秒) ，以及用來衍生 UTC 日期的 GMT 位移。</span><span class="sxs-lookup"><span data-stu-id="069c9-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="069c9-320">例如，為了清楚) 起見，請再次加入 (括弧：</span><span class="sxs-lookup"><span data-stu-id="069c9-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="069c9-321">您可以使用 VBScript 函數 Hour、Minute 和 Second 來轉換 UTC 日期的時間部分。</span><span class="sxs-lookup"><span data-stu-id="069c9-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="069c9-322">因此，時間 11:30:47 A.M。</span><span class="sxs-lookup"><span data-stu-id="069c9-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="069c9-323">會轉換成113047。</span><span class="sxs-lookup"><span data-stu-id="069c9-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="069c9-324">有一個複雜的因素。</span><span class="sxs-lookup"><span data-stu-id="069c9-324">There is one complicating factor.</span></span> <span data-ttu-id="069c9-325">此月份必須在字串中佔用5和6的位置;day 必須花費7和8的位置。</span><span class="sxs-lookup"><span data-stu-id="069c9-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="069c9-326">這在第10天和第18天都沒問題。</span><span class="sxs-lookup"><span data-stu-id="069c9-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="069c9-327">但是，您要如何取得7月5日 (的第5天) 來填滿必要的位置呢？</span><span class="sxs-lookup"><span data-stu-id="069c9-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="069c9-328">答案是將前置零加到每個值，因此將7變更為07，以及5到05。</span><span class="sxs-lookup"><span data-stu-id="069c9-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="069c9-329">若要這樣做，請使用 VBScript Len 函數來檢查月和日) 的字元數 (的長度。</span><span class="sxs-lookup"><span data-stu-id="069c9-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="069c9-330">如果長度為 1 (表示只有一個字元) ，請新增前置零。</span><span class="sxs-lookup"><span data-stu-id="069c9-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="069c9-331">因此：</span><span class="sxs-lookup"><span data-stu-id="069c9-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="069c9-332">範例</span><span class="sxs-lookup"><span data-stu-id="069c9-332">Examples</span></span>

<span data-ttu-id="069c9-333">下列 VBScript 範例會將目前的日期轉換為 UTC 日期。</span><span class="sxs-lookup"><span data-stu-id="069c9-333">The following VBScript example converts the current date to a UTC date.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



<span data-ttu-id="069c9-334">下列 VBScript 會 sampledetermines GMT 位移，然後將指定的目前日期轉換 (在此案例中，10/18/2002) 為 UTC 日期時間格式。</span><span class="sxs-lookup"><span data-stu-id="069c9-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="069c9-335">轉換日期之後，該值會用來搜尋電腦，並傳回在10/18/2002 之後建立的所有資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="069c9-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



<span data-ttu-id="069c9-336">下列 VBScript 程式碼範例會顯示 Win32 \_ 時區實例的設定。</span><span class="sxs-lookup"><span data-stu-id="069c9-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a><span data-ttu-id="069c9-337">規格需求</span><span class="sxs-lookup"><span data-stu-id="069c9-337">Requirements</span></span>



| <span data-ttu-id="069c9-338">需求</span><span class="sxs-lookup"><span data-stu-id="069c9-338">Requirement</span></span> | <span data-ttu-id="069c9-339">值</span><span class="sxs-lookup"><span data-stu-id="069c9-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="069c9-340">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="069c9-340">Minimum supported client</span></span><br/> | <span data-ttu-id="069c9-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="069c9-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="069c9-342">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="069c9-342">Minimum supported server</span></span><br/> | <span data-ttu-id="069c9-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="069c9-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="069c9-344">命名空間</span><span class="sxs-lookup"><span data-stu-id="069c9-344">Namespace</span></span><br/>                | <span data-ttu-id="069c9-345">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="069c9-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="069c9-346">MOF</span><span class="sxs-lookup"><span data-stu-id="069c9-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="069c9-347"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="069c9-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="069c9-348">DLL</span><span class="sxs-lookup"><span data-stu-id="069c9-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="069c9-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="069c9-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="069c9-350">另請參閱</span><span class="sxs-lookup"><span data-stu-id="069c9-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069c9-351">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="069c9-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="069c9-352">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="069c9-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="069c9-353">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="069c9-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="069c9-354">日期和時間格式</span><span class="sxs-lookup"><span data-stu-id="069c9-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="069c9-355">WMI 工作：日期和時間</span><span class="sxs-lookup"><span data-stu-id="069c9-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
