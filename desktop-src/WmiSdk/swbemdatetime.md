---
description: SWbemDateTime 物件是一個協助程式物件，用來剖析和設定通用訊息模型 (CIM) 日期時間值。
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: 'SWbemDateTime 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986975"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="614ae-103">SWbemDateTime 物件</span><span class="sxs-lookup"><span data-stu-id="614ae-103">SWbemDateTime object</span></span>

<span data-ttu-id="614ae-104">**SWbemDateTime** 物件是一個協助程式物件，用來剖析和設定通用訊息模型 (CIM) [日期時間](datetime.md)值。</span><span class="sxs-lookup"><span data-stu-id="614ae-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="614ae-105">它扮演類似于 [**SWbemObjectPath**](swbemobjectpath.md)的角色，可協助您格式化及解讀物件路徑。</span><span class="sxs-lookup"><span data-stu-id="614ae-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="614ae-106">您可以使用 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫來建立 **SWbemDateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="614ae-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="614ae-107">您可以使用物件上的方法，從 **VT \_ 日期** 或 **FILETIME** 值初始化 **SWbemDateTime** 物件，並將其格式化。</span><span class="sxs-lookup"><span data-stu-id="614ae-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="614ae-108">使用物件的屬性，可將值剖析為 component year、month、day、hour、分、秒或微秒。</span><span class="sxs-lookup"><span data-stu-id="614ae-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="614ae-109">**SWbemDateTime** 物件可以格式化為 local 或國際標準時間 (UTC) 值。</span><span class="sxs-lookup"><span data-stu-id="614ae-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="614ae-110">如需詳細資訊，請參閱 [日期和時間格式](date-and-time-format.md)。</span><span class="sxs-lookup"><span data-stu-id="614ae-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="614ae-111">**SWbemDateTime** 是唯一的 WINDOWS MANAGEMENT INSTRUMENTATION (WMI) 腳本物件，該物件標示為安全的初始化和在 Internet Explorer 中的 HTML 網頁上執行的腳本。</span><span class="sxs-lookup"><span data-stu-id="614ae-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="614ae-112">成員</span><span class="sxs-lookup"><span data-stu-id="614ae-112">Members</span></span>

<span data-ttu-id="614ae-113">**SWbemDateTime** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="614ae-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="614ae-114">方法</span><span class="sxs-lookup"><span data-stu-id="614ae-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="614ae-115">屬性</span><span class="sxs-lookup"><span data-stu-id="614ae-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="614ae-116">方法</span><span class="sxs-lookup"><span data-stu-id="614ae-116">Methods</span></span>

<span data-ttu-id="614ae-117">**SWbemDateTime** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="614ae-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="614ae-118">方法</span><span class="sxs-lookup"><span data-stu-id="614ae-118">Method</span></span>                                           | <span data-ttu-id="614ae-119">描述</span><span class="sxs-lookup"><span data-stu-id="614ae-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="614ae-120">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="614ae-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="614ae-121">將 **FILETIME** 日期和時間（以 **BSTR** 表示）轉換為 WMI [日期時間](datetime.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="614ae-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="614ae-122">**GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="614ae-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="614ae-123">將 WMI [DATETIME](datetime.md) 格式化日期和時間值轉換成 **VT \_ 日期**。</span><span class="sxs-lookup"><span data-stu-id="614ae-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="614ae-124">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="614ae-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="614ae-125">將 WMI [DATETIME](datetime.md) 格式轉換為 **FILETIME** 日期和時間，以 **BSTR** 表示。</span><span class="sxs-lookup"><span data-stu-id="614ae-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="614ae-126">**SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="614ae-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="614ae-127">將 **VT \_ 日期** 格式的日期和時間轉換為 WMI 日期 [時間](datetime.md)。</span><span class="sxs-lookup"><span data-stu-id="614ae-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="614ae-128">屬性</span><span class="sxs-lookup"><span data-stu-id="614ae-128">Properties</span></span>

<span data-ttu-id="614ae-129">**SWbemDateTime** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="614ae-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="614ae-130">屬性</span><span class="sxs-lookup"><span data-stu-id="614ae-130">Property</span></span>                                                                        | <span data-ttu-id="614ae-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="614ae-131">Access type</span></span>           | <span data-ttu-id="614ae-132">Description</span><span class="sxs-lookup"><span data-stu-id="614ae-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="614ae-133">**天**</span><span class="sxs-lookup"><span data-stu-id="614ae-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="614ae-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-134">Read/write</span></span><br/> | <span data-ttu-id="614ae-135">CIM [日期時間](datetime.md) 值的日元件。</span><span class="sxs-lookup"><span data-stu-id="614ae-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="614ae-136">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="614ae-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-137">Read/write</span></span><br/> | <span data-ttu-id="614ae-138">指出日期是否指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="614ae-139">**小時**</span><span class="sxs-lookup"><span data-stu-id="614ae-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="614ae-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-140">Read/write</span></span><br/> | <span data-ttu-id="614ae-141">CIM [datetime](datetime.md) 值之 day 元件的時數。</span><span class="sxs-lookup"><span data-stu-id="614ae-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="614ae-142">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="614ae-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-143">Read/write</span></span><br/> | <span data-ttu-id="614ae-144">指出小時是否指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="614ae-145">**IsInterval**</span><span class="sxs-lookup"><span data-stu-id="614ae-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="614ae-146">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-146">Read/write</span></span><br/> | <span data-ttu-id="614ae-147">指出至少有一個 CIM [datetime](datetime.md) 的元件代表間隔，而不是日期。</span><span class="sxs-lookup"><span data-stu-id="614ae-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="614ae-148">**微秒**</span><span class="sxs-lookup"><span data-stu-id="614ae-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="614ae-149">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-149">Read/write</span></span><br/> | <span data-ttu-id="614ae-150">CIM [datetime](datetime.md) 值的微秒部分。</span><span class="sxs-lookup"><span data-stu-id="614ae-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="614ae-151">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="614ae-152">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-152">Read/write</span></span><br/> | <span data-ttu-id="614ae-153">指出是否將微秒元件指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="614ae-154">**分鐘**</span><span class="sxs-lookup"><span data-stu-id="614ae-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="614ae-155">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-155">Read/write</span></span><br/> | <span data-ttu-id="614ae-156">CIM [日期時間](datetime.md) 值的分鐘元件。</span><span class="sxs-lookup"><span data-stu-id="614ae-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="614ae-157">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="614ae-158">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-158">Read/write</span></span><br/> | <span data-ttu-id="614ae-159">指出分鐘元件是否指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="614ae-160">**月**</span><span class="sxs-lookup"><span data-stu-id="614ae-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="614ae-161">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-161">Read/write</span></span><br/> | <span data-ttu-id="614ae-162">CIM [日期時間](datetime.md) 值的月份元件。</span><span class="sxs-lookup"><span data-stu-id="614ae-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="614ae-163">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="614ae-164">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-164">Read/write</span></span><br/> | <span data-ttu-id="614ae-165">指出月份是否已指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="614ae-166">**秒**</span><span class="sxs-lookup"><span data-stu-id="614ae-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="614ae-167">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-167">Read/write</span></span><br/> | <span data-ttu-id="614ae-168">CIM [日期時間](datetime.md) 值的秒陣列件。</span><span class="sxs-lookup"><span data-stu-id="614ae-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="614ae-169">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="614ae-170">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-170">Read/write</span></span><br/> | <span data-ttu-id="614ae-171">指出秒元件是否指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="614ae-172">**Utc**</span><span class="sxs-lookup"><span data-stu-id="614ae-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="614ae-173">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-173">Read/write</span></span><br/> | <span data-ttu-id="614ae-174">CIM [datetime](datetime.md) 值的 UTC 元件。</span><span class="sxs-lookup"><span data-stu-id="614ae-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="614ae-175">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="614ae-176">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-176">Read/write</span></span><br/> | <span data-ttu-id="614ae-177">指出 UTC 元件是否指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="614ae-178">**值**</span><span class="sxs-lookup"><span data-stu-id="614ae-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="614ae-179">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-179">Read/write</span></span><br/> | <span data-ttu-id="614ae-180">完整的 CIM [日期時間](datetime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="614ae-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="614ae-181">**年**</span><span class="sxs-lookup"><span data-stu-id="614ae-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="614ae-182">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-182">Read/write</span></span><br/> | <span data-ttu-id="614ae-183">CIM [日期時間](datetime.md) 值的年份元件。</span><span class="sxs-lookup"><span data-stu-id="614ae-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="614ae-184">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="614ae-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="614ae-185">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="614ae-185">Read/write</span></span><br/> | <span data-ttu-id="614ae-186">指出年份是否指定或保留為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="614ae-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="614ae-187">備註</span><span class="sxs-lookup"><span data-stu-id="614ae-187">Remarks</span></span>

<span data-ttu-id="614ae-188">以國際標準時間座標 (UTC) 格式的 WMI 記錄時間戳記。</span><span class="sxs-lookup"><span data-stu-id="614ae-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="614ae-189">UTC 並非大部分開發人員和 IT 系統管理員使用的格式。</span><span class="sxs-lookup"><span data-stu-id="614ae-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="614ae-190">因此，常見的問題是決定如何將 UTC 轉譯成更容易讀取的內容。</span><span class="sxs-lookup"><span data-stu-id="614ae-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="614ae-191">如需如何使用 UTC 的詳細資訊，請參閱 [wmi 工作：日期和時間](wmi-tasks--dates-and-times.md) ，以及 [使用 wmi 處理日期和時間](/previous-versions/tn-archive/ee198928(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="614ae-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="614ae-192">您也可以閱讀 (喔的 [相關時間，以及有關日期的) ](/previous-versions/technet-magazine/cc160973(v=msdn.10)) ，以及 [如何從 UTC 值減去指定的天數？](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog 文章以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="614ae-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="614ae-193">如果 [**IsInterval**](swbemdatetime-isinterval.md) 屬性設定為 **FALSE**，任何數值欄位都可以有萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="614ae-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="614ae-194">具有萬用字元值的欄位包含整個欄位中的星號。</span><span class="sxs-lookup"><span data-stu-id="614ae-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="614ae-195">每個屬性（例如 [**Day**](swbemdatetime-day.md)）都有對應的指定布林值，例如 [**DaySpecified**](swbemdatetime-dayspecified.md)。</span><span class="sxs-lookup"><span data-stu-id="614ae-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="614ae-196">當 **DaySpecified** 為 **FALSE** 時，會將值視為間隔，而不是1到31之間的數位。</span><span class="sxs-lookup"><span data-stu-id="614ae-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="614ae-197">如果在 CIM [datetime](datetime.md) 值的任何地方使用間隔，則 [**IsInterval**](swbemdatetime-isinterval.md) 也會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="614ae-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="614ae-198">預設值是讓 CIM datetime 值包含日期，而不是一或多個間隔。</span><span class="sxs-lookup"><span data-stu-id="614ae-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="614ae-199">例如，如果 [**SWbemDateTime**](swbemdatetime-dayspecified.md) 為 **TRUE**，則 [**SWbemDateTime。值**](swbemdatetime-value.md) 會包含 [**SWbemDateTime**](swbemdatetime-day.md)的目前值，否則為萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="614ae-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="614ae-200">在任何一種情況下， [**IsInterval**](swbemdatetime-isinterval.md) 屬性都是 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="614ae-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="614ae-201">範例</span><span class="sxs-lookup"><span data-stu-id="614ae-201">Examples</span></span>

<span data-ttu-id="614ae-202">下列腳本範例示範如何使用 **SWbemDateTime** 物件來剖析從 WMI 儲存機制讀取的 datetime 屬性值（ [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)中的 **InstallDate** 屬性）。</span><span class="sxs-lookup"><span data-stu-id="614ae-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="614ae-203">下列範例示範如何建立 **SWbemDateTime** 物件、將日期值儲存在物件中、將日期顯示為本機和國際標準時間 (UTC) ，然後將值儲存在新建立的類別和屬性中。</span><span class="sxs-lookup"><span data-stu-id="614ae-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="614ae-204">如需有關常數 **wbemCimtypeDatetime** 的詳細資訊，請參閱 [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)。</span><span class="sxs-lookup"><span data-stu-id="614ae-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="614ae-205">下列腳本程式碼範例示範如何使用 **SWbemDateTime** 物件來修改從 WMI 儲存機制讀取之屬性的間隔值。</span><span class="sxs-lookup"><span data-stu-id="614ae-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="614ae-206">下列腳本程式碼範例示範如何使用 **SWbemDate** 物件來讀取 **FILETIME** 值。</span><span class="sxs-lookup"><span data-stu-id="614ae-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="614ae-207">下列 PowerShell 程式碼會建立 SWbemDateTime 物件的實例、捕獲 OS 安裝日期，並將日期轉換成不同的格式</span><span class="sxs-lookup"><span data-stu-id="614ae-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="614ae-208">下列 Powershell 程式碼會將程式碼轉譯成可供 CIM 提供者使用的格式。</span><span class="sxs-lookup"><span data-stu-id="614ae-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="614ae-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="614ae-209">Requirements</span></span>



| <span data-ttu-id="614ae-210">需求</span><span class="sxs-lookup"><span data-stu-id="614ae-210">Requirement</span></span> | <span data-ttu-id="614ae-211">值</span><span class="sxs-lookup"><span data-stu-id="614ae-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="614ae-212">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="614ae-212">Minimum supported client</span></span><br/> | <span data-ttu-id="614ae-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="614ae-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="614ae-214">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="614ae-214">Minimum supported server</span></span><br/> | <span data-ttu-id="614ae-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="614ae-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="614ae-216">標頭</span><span class="sxs-lookup"><span data-stu-id="614ae-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="614ae-217"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="614ae-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="614ae-218">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="614ae-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="614ae-219"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="614ae-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="614ae-220">DLL</span><span class="sxs-lookup"><span data-stu-id="614ae-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="614ae-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="614ae-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="614ae-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="614ae-222">CLSID</span></span><br/>                    | <span data-ttu-id="614ae-223">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="614ae-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="614ae-224">IID</span><span class="sxs-lookup"><span data-stu-id="614ae-224">IID</span></span><br/>                      | <span data-ttu-id="614ae-225">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="614ae-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="614ae-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="614ae-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614ae-227">WbemCimtypeEnum</span><span class="sxs-lookup"><span data-stu-id="614ae-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="614ae-228">Datetime</span><span class="sxs-lookup"><span data-stu-id="614ae-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="614ae-229">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="614ae-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

