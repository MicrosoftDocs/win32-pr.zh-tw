---
description: 您可以使用 WMI 和 CIM 專屬的兩個固定長度格式之一，來存取 WMI 中的所有通用訊息模型 (CIM) 日期和時間。 在腳本中，使用 SWbemDateTime 物件將這些轉換成一般日期和時間。
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983844"
---
# <a name="cim_datetime"></a><span data-ttu-id="57e12-104">CIM \_ DATETIME</span><span class="sxs-lookup"><span data-stu-id="57e12-104">CIM\_DATETIME</span></span>

<span data-ttu-id="57e12-105">您可以使用 WMI 和 CIM 專屬的兩個固定長度格式之一，來存取 WMI 中的所有 [*通用訊息模型 (CIM)*](gloss-c.md) 日期和時間。</span><span class="sxs-lookup"><span data-stu-id="57e12-105">You can access all [*Common Information Model (CIM)*](gloss-c.md) dates and times in WMI by using one of two fixed-length formats specific to WMI and CIM.</span></span> <span data-ttu-id="57e12-106">在腳本中，使用 [**SWbemDateTime**](swbemdatetime.md) 物件將這些轉換成一般日期和時間。</span><span class="sxs-lookup"><span data-stu-id="57e12-106">In scripting, use the [**SWbemDateTime**](swbemdatetime.md) object to convert these to regular dates and times.</span></span>

<span data-ttu-id="57e12-107">下列各節說明如何使用 WMI 日期和時間格式。</span><span class="sxs-lookup"><span data-stu-id="57e12-107">The following sections describe how to use the WMI date and time formats.</span></span>

## <a name="format"></a><span data-ttu-id="57e12-108">格式</span><span class="sxs-lookup"><span data-stu-id="57e12-108">Format</span></span>

<span data-ttu-id="57e12-109">下表列出 WMI 所使用的兩種日期和時間格式。</span><span class="sxs-lookup"><span data-stu-id="57e12-109">The following table lists the two date and time formats used by WMI.</span></span>



| <span data-ttu-id="57e12-110">格式</span><span class="sxs-lookup"><span data-stu-id="57e12-110">Format</span></span>                                                                                                 | <span data-ttu-id="57e12-111">描述</span><span class="sxs-lookup"><span data-stu-id="57e12-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57e12-112">Datetime</span><span class="sxs-lookup"><span data-stu-id="57e12-112">DATETIME</span></span>](datetime.md)<br/> <span data-ttu-id="57e12-113">*Yyyymmddhhmmss.ffffff. mmmmmmsUUU*</span><span class="sxs-lookup"><span data-stu-id="57e12-113">*yyyymmddHHMMSS.mmmmmmsUUU*</span></span><br/>                             | <span data-ttu-id="57e12-114">儲存 CIM [**DATETIME**](datetime.md) 值的格式。</span><span class="sxs-lookup"><span data-stu-id="57e12-114">Format in which CIM [**DATETIME**](datetime.md) values are stored.</span></span> <span data-ttu-id="57e12-115">這種格式與地區設定無關，因此您可以撰寫在任何電腦上執行的腳本。</span><span class="sxs-lookup"><span data-stu-id="57e12-115">This format is locale-independent so you can write a script that runs on any machine.</span></span> <span data-ttu-id="57e12-116">您必須使用此格式來定義 [*受控物件格式 (MOF)*](gloss-m.md)的日期和時間，或使用適用于 Wmi 的 [COM API](com-api-for-wmi.md) 或 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md)寫入至實例時的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="57e12-116">You must use this format to define a date and time in [*Managed Object Format (MOF)*](gloss-m.md), or when writing to an instance using the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="57e12-117">如需詳細資訊，請參閱 [修改實例屬性](modifying-an-instance-property.md)。</span><span class="sxs-lookup"><span data-stu-id="57e12-117">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span> |
| <span data-ttu-id="57e12-118">格式只在 WMI 查詢語言 (WQL) 查詢中有效。</span><span class="sxs-lookup"><span data-stu-id="57e12-118">Format valid only in WMI Query Language (WQL) queries.</span></span><br/> <span data-ttu-id="57e12-119">*yyyy-mm-dd HH： MM： SS： mmm*</span><span class="sxs-lookup"><span data-stu-id="57e12-119">*yyyy-mm-dd HH:MM:SS:mmm*</span></span><br/> | <span data-ttu-id="57e12-120">此格式可用於使用 [**SWbemDateTime**](swbemdatetime.md) 方法的腳本。</span><span class="sxs-lookup"><span data-stu-id="57e12-120">This format can be used in scripts that use the [**SWbemDateTime**](swbemdatetime.md) methods.</span></span> <span data-ttu-id="57e12-121">如需詳細資訊，請參閱[使用 WQL](querying-with-wql.md)[查詢 WMI](querying-wmi.md)或查詢。</span><span class="sxs-lookup"><span data-stu-id="57e12-121">For more information, see [Querying WMI](querying-wmi.md) or [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="57e12-122">此格式與地區設定無關。</span><span class="sxs-lookup"><span data-stu-id="57e12-122">This format is not independent of locale.</span></span> <span data-ttu-id="57e12-123">Year、month 和 day 的順序取決於使用者會話的地區和語言格式設定。</span><span class="sxs-lookup"><span data-stu-id="57e12-123">The order of year, month, and day depends on the regional and language format setting of the user session.</span></span> <span data-ttu-id="57e12-124">例如，美國英文的預設值為 "yyyy-mm-dd hh： mm： ss： mmm"，其他大部分國家或地區的格式為 "yyyy-mm-dd hh： mm： ss： mmm"。</span><span class="sxs-lookup"><span data-stu-id="57e12-124">For example, while the default for United States English is "mm-dd-yyyy hh:mm:ss:mmm", the format for most other countries or regions is "yyyy-mm-dd hh:mm:ss:mmm".</span></span>       |



 

<span data-ttu-id="57e12-125">下表列出這些格式的欄位。</span><span class="sxs-lookup"><span data-stu-id="57e12-125">The following table lists the fields in the formats.</span></span>



| <span data-ttu-id="57e12-126">欄位</span><span class="sxs-lookup"><span data-stu-id="57e12-126">Field</span></span>    | <span data-ttu-id="57e12-127">描述</span><span class="sxs-lookup"><span data-stu-id="57e12-127">Description</span></span>                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e12-128">*yyyy*</span><span class="sxs-lookup"><span data-stu-id="57e12-128">*yyyy*</span></span>   | <span data-ttu-id="57e12-129">四位數年份 (0000 到 9999) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-129">Four-digit year (0000 through 9999).</span></span> <span data-ttu-id="57e12-130">您的執行可以限制支援的範圍。</span><span class="sxs-lookup"><span data-stu-id="57e12-130">Your implementation can restrict the supported range.</span></span> <span data-ttu-id="57e12-131">例如，執行只能支援年1980到2099。</span><span class="sxs-lookup"><span data-stu-id="57e12-131">For example, an implementation can support only the years 1980 through 2099.</span></span>                                                                         |
| <span data-ttu-id="57e12-132">*mm*</span><span class="sxs-lookup"><span data-stu-id="57e12-132">*mm*</span></span>     | <span data-ttu-id="57e12-133">兩位數的月份 (01 到 12) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-133">Two-digit month (01 through 12).</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="57e12-134">*dd*</span><span class="sxs-lookup"><span data-stu-id="57e12-134">*dd*</span></span>     | <span data-ttu-id="57e12-135">月份的兩位數天 (01 到 31) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-135">Two-digit day of the month (01 through 31).</span></span> <span data-ttu-id="57e12-136">此值必須適用于月份。</span><span class="sxs-lookup"><span data-stu-id="57e12-136">This value must be appropriate for the month.</span></span> <span data-ttu-id="57e12-137">例如，2月31日無效。</span><span class="sxs-lookup"><span data-stu-id="57e12-137">For example, February 31 is not valid.</span></span> <span data-ttu-id="57e12-138">不過，您的執行不需要檢查是否有有效的資料。</span><span class="sxs-lookup"><span data-stu-id="57e12-138">However, your implementation does not have to check for valid data.</span></span>                                            |
| <span data-ttu-id="57e12-139">*HH*</span><span class="sxs-lookup"><span data-stu-id="57e12-139">*HH*</span></span>     | <span data-ttu-id="57e12-140">使用24小時制的一天兩位數小時 (00 到 23) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-140">Two-digit hour of the day using the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                              |
| <span data-ttu-id="57e12-141">*毫米*</span><span class="sxs-lookup"><span data-stu-id="57e12-141">*MM*</span></span>     | <span data-ttu-id="57e12-142">小時的兩位數分鐘 (00 到 59) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-142">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="57e12-143">*匯總*</span><span class="sxs-lookup"><span data-stu-id="57e12-143">*SS*</span></span>     | <span data-ttu-id="57e12-144">分鐘 (00 到 59) 的兩位數秒數。</span><span class="sxs-lookup"><span data-stu-id="57e12-144">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="57e12-145">*mmmmmm*</span><span class="sxs-lookup"><span data-stu-id="57e12-145">*mmmmmm*</span></span> | <span data-ttu-id="57e12-146">第二個數字的毫秒數， (000000 到 999999) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-146">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="57e12-147">您的執行不需要使用此欄位來支援評估。</span><span class="sxs-lookup"><span data-stu-id="57e12-147">Your implementation does not have to support evaluation using this field.</span></span> <span data-ttu-id="57e12-148">不過，這個欄位必須一律存在，以保留字元串的固定長度性質。</span><span class="sxs-lookup"><span data-stu-id="57e12-148">However, this field must always be present to preserve the fixed-length nature of the string.</span></span> |
| <span data-ttu-id="57e12-149">*mmm*</span><span class="sxs-lookup"><span data-stu-id="57e12-149">*mmm*</span></span>    | <span data-ttu-id="57e12-150">分鐘 (000 到 999) 的三位數毫秒數。</span><span class="sxs-lookup"><span data-stu-id="57e12-150">Three-digit number of milliseconds in the minute (000 through 999).</span></span>                                                                                                                                                                             |
| <span data-ttu-id="57e12-151">*s*</span><span class="sxs-lookup"><span data-stu-id="57e12-151">*s*</span></span>      | <span data-ttu-id="57e12-152">再加上正負號 (+) 或減號 (-) 表示與國際標準時間之間的正面或負面位移 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-152">Plus sign (+) or minus sign (-) to indicate a positive or negative offset from Coordinated Universal Times (UTC).</span></span>                                                                                                                               |
| <span data-ttu-id="57e12-153">*UUU*</span><span class="sxs-lookup"><span data-stu-id="57e12-153">*UUU*</span></span>    | <span data-ttu-id="57e12-154">三位數位移，表示原始時區偏離 UTC 的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="57e12-154">Three-digit offset indicating the number of minutes that the originating time zone deviates from UTC.</span></span> <span data-ttu-id="57e12-155">針對 WMI，建議您但非必要，將時間轉換為 GMT (UTC 位移為零) 。</span><span class="sxs-lookup"><span data-stu-id="57e12-155">For WMI, it is encouraged, but not required, to convert times to GMT (a UTC offset of zero).</span></span>                                              |



 

<span data-ttu-id="57e12-156">您必須輸入具有指定長度的所有欄位，並使用適用于該類型的前置零。</span><span class="sxs-lookup"><span data-stu-id="57e12-156">You must enter all fields with the indicated length, using leading zeros as appropriate for the type.</span></span> <span data-ttu-id="57e12-157">不過，請使用星號來指出未使用的欄位或萬用字元值。</span><span class="sxs-lookup"><span data-stu-id="57e12-157">However, use asterisks to indicate unused fields or as a wildcard value.</span></span> <span data-ttu-id="57e12-158">\*除了查詢的 **WHERE** 子句以外，您可以在任何地方使用星號 () 。</span><span class="sxs-lookup"><span data-stu-id="57e12-158">You can use an asterisk (\*) everywhere except the **WHERE** clause of a query.</span></span> <span data-ttu-id="57e12-159">例如，具有未指定年份的日期和時間可能會在任何年份發生。</span><span class="sxs-lookup"><span data-stu-id="57e12-159">For example, a date and time with an unspecified year can occur in any year.</span></span> <span data-ttu-id="57e12-160">如果您想要讓欄位保持未指定，則必須將整個欄位取代為星號。</span><span class="sxs-lookup"><span data-stu-id="57e12-160">If you wish to leave a field unspecified, you must replace the entire field with asterisks.</span></span>

<span data-ttu-id="57e12-161">下列範例說明有效和不正確星號用法：</span><span class="sxs-lookup"><span data-stu-id="57e12-161">The following examples describe valid and invalid uses of asterisks:</span></span>

-   <span data-ttu-id="57e12-162">19980416 \* \* \* \* \* \* .000000 + \* \* \* (合法) </span><span class="sxs-lookup"><span data-stu-id="57e12-162">19980416\*\*\*\*\*\*.000000+\*\*\* (Legal)</span></span>
-   <span data-ttu-id="57e12-163">1998-04-16 \* \* \* \* \* \* ： \* \* \* (不合法的) </span><span class="sxs-lookup"><span data-stu-id="57e12-163">1998-04-16 \*\*\*\*\*\*:\*\*\* (Illegal)</span></span>
-   <span data-ttu-id="57e12-164">199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (不合法的) </span><span class="sxs-lookup"><span data-stu-id="57e12-164">199\*0416\*\*\*\*\*\*.000000+\*\*\* (Illegal)</span></span>
-   <span data-ttu-id="57e12-165">199 \* -04-16 \* \* \* \* \* \* ： \* \* \* (不合法的) </span><span class="sxs-lookup"><span data-stu-id="57e12-165">199\*-04-16 \*\*\*\*\*\*:\*\*\* (Illegal)</span></span>

<span data-ttu-id="57e12-166">如果使用 datetime 來代表特定時間點，其所有欄位都應該包含資料。</span><span class="sxs-lookup"><span data-stu-id="57e12-166">If a datetime is used to represent a specific point in time, all of its fields should include data.</span></span> <span data-ttu-id="57e12-167">如果用來表示時間範圍，則只有傳達期間所需的欄位才會包含資料。</span><span class="sxs-lookup"><span data-stu-id="57e12-167">If it is used to represent a range of time, only the fields necessary to convey the duration should include data.</span></span>

<span data-ttu-id="57e12-168">下列範例描述「4月前」：相對於某些未指定年份的日期，但如果測量詳細資料層級為一天，則仍是定義的點。</span><span class="sxs-lookup"><span data-stu-id="57e12-168">The following example describes "April first": a date relative to some unspecified year but still a defined point if the level of measurement detail is one day.</span></span>

-   <span data-ttu-id="57e12-169">\*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*</span><span class="sxs-lookup"><span data-stu-id="57e12-169">\*\*\*\*0401\*\*\*\*\*\*.000000+\*\*\*</span></span>
-   <span data-ttu-id="57e12-170">\*\*\*\*-04-01 \* \* \* \* \* \* ： \* \* \* (不合法的) </span><span class="sxs-lookup"><span data-stu-id="57e12-170">\*\*\*\*-04-01 \*\*\*\*\*\*:\*\*\* (Illegal)</span></span>

## <a name="setting-utc-offset-and-gmt"></a><span data-ttu-id="57e12-171">設定 UTC 時差和 GMT</span><span class="sxs-lookup"><span data-stu-id="57e12-171">Setting UTC Offset and GMT</span></span>

<span data-ttu-id="57e12-172">下列範例說明如何在加號或減號之後將星號放在 UUU 欄位中，以定義沒有時區的時間：</span><span class="sxs-lookup"><span data-stu-id="57e12-172">The following examples describe how you can define a time with no time zone by placing asterisks in the UUU field after either the plus or minus sign:</span></span>

-   <span data-ttu-id="57e12-173">19980401135809.000000 +\*\*\*</span><span class="sxs-lookup"><span data-stu-id="57e12-173">19980401135809.000000+\*\*\*</span></span>
-   <span data-ttu-id="57e12-174">19980401135809.000000-\*\*\*</span><span class="sxs-lookup"><span data-stu-id="57e12-174">19980401135809.000000-\*\*\*</span></span>
-   <span data-ttu-id="57e12-175">1998-04-01 13:58:09： \* \* \* (不合法的) </span><span class="sxs-lookup"><span data-stu-id="57e12-175">1998-04-01 13:58:09:\*\*\* (Illegal)</span></span>

<span data-ttu-id="57e12-176">應用程式會在執行中的作業系統內，將 unzoned 的日期和時間參考解釋為本機的抽象 chronometer。</span><span class="sxs-lookup"><span data-stu-id="57e12-176">An application interprets an unzoned date and time reference to a local, abstract chronometer within the executing operating system.</span></span> <span data-ttu-id="57e12-177">例如，可攜式電腦可以有內部時鐘，其設定可能或不會對應至地理時區。</span><span class="sxs-lookup"><span data-stu-id="57e12-177">For example, portable computers can have internal clocks whose settings may or may not correspond to the geographical time zone.</span></span> <span data-ttu-id="57e12-178">您可以用目前的摘要時間來源（而不是本地時區）來解讀 unzoned 時間。</span><span class="sxs-lookup"><span data-stu-id="57e12-178">You can interpret unzoned time by substituting the time zone of the current abstract time source rather than the local time zone.</span></span>

<span data-ttu-id="57e12-179">您應該特別考慮 UTC 時差與查詢中日期和時間的意義。</span><span class="sxs-lookup"><span data-stu-id="57e12-179">You should give special consideration to the meaning of the UTC offset with dates and times in queries.</span></span> <span data-ttu-id="57e12-180">一般情況下，當日期和時間使用相同的 UTC 位移時，等價、大於或小於比較的工作會在兩個日期和時間之間運作。</span><span class="sxs-lookup"><span data-stu-id="57e12-180">In general, equivalence, greater-than, or less-than comparisons work between two dates and times if the dates and times use the same UTC offset.</span></span> <span data-ttu-id="57e12-181">處理不同時區位移時所發生的日期和時間時，您應該先將日期和時間轉換為 GMT。</span><span class="sxs-lookup"><span data-stu-id="57e12-181">When dealing with dates and times that occur with different time zone offsets, you should first convert the dates and times to GMT.</span></span>

<span data-ttu-id="57e12-182">在一或多個子欄位中使用星號的相關查詢，在比較是否相等時，只對 WMI 有意義。</span><span class="sxs-lookup"><span data-stu-id="57e12-182">Queries that involve relative dates and times with asterisks in one or more subfields are only meaningful to WMI when compared for equivalence.</span></span> <span data-ttu-id="57e12-183">此外，WMI 不允許使用星號作為萬用字元。</span><span class="sxs-lookup"><span data-stu-id="57e12-183">Further, WMI does not allow using asterisks as wildcards.</span></span> <span data-ttu-id="57e12-184">相反地，WMI 會以字元為單位來比較相對的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="57e12-184">Instead, WMI compares relative dates and times on a character-for-character basis.</span></span>

<span data-ttu-id="57e12-185">下列範例說明 WMI 查詢不視為相等的兩個日期：</span><span class="sxs-lookup"><span data-stu-id="57e12-185">The following examples describe two dates that a WMI query does not consider equal:</span></span>

-   <span data-ttu-id="57e12-186">19980401135809.000000 +\*\*\*</span><span class="sxs-lookup"><span data-stu-id="57e12-186">19980401135809.000000+\*\*\*</span></span>
-   <span data-ttu-id="57e12-187">19980401135809.000000 + 000</span><span class="sxs-lookup"><span data-stu-id="57e12-187">19980401135809.000000+000</span></span>

## <a name="converting-to-filetime-or-vt_date-format"></a><span data-ttu-id="57e12-188">轉換成 FILETIME 或 VT \_ 日期格式</span><span class="sxs-lookup"><span data-stu-id="57e12-188">Converting to FILETIME or VT\_DATE format</span></span>

<span data-ttu-id="57e12-189">CIM [**DATETIME**](datetime.md) 格式只會在 WMI 內使用。</span><span class="sxs-lookup"><span data-stu-id="57e12-189">The CIM [**DATETIME**](datetime.md) format is used only within WMI.</span></span> <span data-ttu-id="57e12-190">您可以藉 \_ 由呼叫 [**SWbemDateTime**](swbemdatetime.md) 腳本物件的方法，從 WMI 格式轉換為和，以及使用 FILETIME 或 VT 日期格式。</span><span class="sxs-lookup"><span data-stu-id="57e12-190">You can convert to and from the WMI format and either the FILETIME or VT\_DATE format by calling the methods of the [**SWbemDateTime**](swbemdatetime.md) scripting object.</span></span> <span data-ttu-id="57e12-191">[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) **datetime** 結構是32位 Windows 作業系統所使用的64位值。</span><span class="sxs-lookup"><span data-stu-id="57e12-191">A [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) **datetime** structure is a 64-bit value that the 32-bit Windows operating systems use.</span></span> <span data-ttu-id="57e12-192">VT \_ 日期格式是 Visual Basic 和 ActiveX 使用的 automation variant datetime 值。</span><span class="sxs-lookup"><span data-stu-id="57e12-192">VT\_DATE format is an automation variant datetime value used by Visual Basic and ActiveX.</span></span> <span data-ttu-id="57e12-193">下表列出轉換方法。</span><span class="sxs-lookup"><span data-stu-id="57e12-193">The following table lists the conversion methods.</span></span>



| <span data-ttu-id="57e12-194">方法</span><span class="sxs-lookup"><span data-stu-id="57e12-194">Method</span></span>                                                         | <span data-ttu-id="57e12-195">描述</span><span class="sxs-lookup"><span data-stu-id="57e12-195">Description</span></span>                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57e12-196">**SWbemDateTime.GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="57e12-196">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="57e12-197">取得 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)格式的 [**日期時間**](datetime.md)值。</span><span class="sxs-lookup"><span data-stu-id="57e12-197">Gets a [**DATETIME**](datetime.md) value in [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>                |
| [<span data-ttu-id="57e12-198">**SWbemDateTime. GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="57e12-198">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="57e12-199">取得 VT 日期格式的 [**日期時間**](datetime.md) 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="57e12-199">Gets a [**DATETIME**](datetime.md) value in VT\_DATE format.</span></span>                                         |
| [<span data-ttu-id="57e12-200">**SWbemDateTime.SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="57e12-200">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setvardate.md)  | <span data-ttu-id="57e12-201">使用 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)日期做為輸入，設定 [**DATETIME**](datetime.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="57e12-201">Sets a [**DATETIME**](datetime.md) property using a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) date as input.</span></span> |
| [<span data-ttu-id="57e12-202">**SWbemDateTime.SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="57e12-202">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="57e12-203">使用 VT [](datetime.md) \_ 日期日期做為輸入，設定 DATETIME 屬性。</span><span class="sxs-lookup"><span data-stu-id="57e12-203">Sets a [**DATETIME**](datetime.md) property using a VT\_DATE date as input.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="57e12-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="57e12-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e12-205">日期和時間格式</span><span class="sxs-lookup"><span data-stu-id="57e12-205">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="57e12-206">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="57e12-206">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="57e12-207">WMI 工作：日期和時間</span><span class="sxs-lookup"><span data-stu-id="57e12-207">WMI Tasks: Dates and Times</span></span>](wmi-tasks--dates-and-times.md)
</dt> <dt>

[<span data-ttu-id="57e12-208">間隔格式</span><span class="sxs-lookup"><span data-stu-id="57e12-208">Interval Format</span></span>](interval-format.md)
</dt> <dt>

[<span data-ttu-id="57e12-209">**SWbemObject。 Put\_**</span><span class="sxs-lookup"><span data-stu-id="57e12-209">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="57e12-210">**SWbemServicesEx。 Put**</span><span class="sxs-lookup"><span data-stu-id="57e12-210">**SWbemServicesEx.Put**</span></span>](swbemservicesex-put.md)
</dt> <dt>

[<span data-ttu-id="57e12-211">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="57e12-211">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="57e12-212">**IWbemClassObject：:P 的內容**</span><span class="sxs-lookup"><span data-stu-id="57e12-212">**IWbemClassObject::Put**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[<span data-ttu-id="57e12-213">**IWbemServices：:P utClass**</span><span class="sxs-lookup"><span data-stu-id="57e12-213">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

