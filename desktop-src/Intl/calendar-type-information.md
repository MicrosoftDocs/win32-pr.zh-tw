---
description: 本主題描述 EnumCalendarInfo、EnumCalendarInfoEx、EnumCalendarInfoExEx、GetCalendarInfo 和 GetCalendarInfoEx 函式中所使用 (CALTYPE 資料類型) 的行事曆類型資訊。
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: 行事曆類型資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851831"
---
# <a name="calendar-type-information"></a><span data-ttu-id="97990-103">行事曆類型資訊</span><span class="sxs-lookup"><span data-stu-id="97990-103">Calendar Type Information</span></span>

<span data-ttu-id="97990-104">本主題描述 [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)、 [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)、 [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)、 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)和 [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) 函式中所使用 (CALTYPE 資料類型) 的行事曆類型資訊。</span><span class="sxs-lookup"><span data-stu-id="97990-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="97990-105">[**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)函式也會使用其中的一些值。</span><span class="sxs-lookup"><span data-stu-id="97990-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="97990-106">下列 CALTYPE 常數可以與任何其他 CALTYPE 常數一起使用。</span><span class="sxs-lookup"><span data-stu-id="97990-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="97990-107">常數</span><span class="sxs-lookup"><span data-stu-id="97990-107">Constant</span></span>                     | <span data-ttu-id="97990-108">描述</span><span class="sxs-lookup"><span data-stu-id="97990-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97990-109">CAL \_ NOUSEROVERRIDE</span><span class="sxs-lookup"><span data-stu-id="97990-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="97990-110">**Windows Me/98、windows 2000：** 使用系統預設值，而不是使用者的選擇。</span><span class="sxs-lookup"><span data-stu-id="97990-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="97990-111">CAL \_ 傳回 \_ 所有格 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="97990-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="97990-112">**Windows 7 和更新版本：** 以每月的所有格名稱形式取出 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) 的結果，這是月份名稱與其他專案合併時所使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="97990-113">例如，在「烏克蘭」中，當月份單獨命名時，1月的對等專案會寫入「Січень」。</span><span class="sxs-lookup"><span data-stu-id="97990-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="97990-114">不過，當月份名稱用於組合時（例如，在2003年1月5日的日期）中，會使用名稱的所有格形式。</span><span class="sxs-lookup"><span data-stu-id="97990-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="97990-115">針對烏克蘭範例，所有格月份名稱會顯示為 "5 січня 2003"。</span><span class="sxs-lookup"><span data-stu-id="97990-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="97990-116">如需詳細資訊，請參閱 [LOCALE 傳回 \_ 所屬的 \_ \_ 名稱](locale-return-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="97990-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="97990-117">CAL \_ 傳回 \_ 編號</span><span class="sxs-lookup"><span data-stu-id="97990-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="97990-118">**Windows Me/98、windows 2000：** 以數位而非字串形式取出 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) 的結果。</span><span class="sxs-lookup"><span data-stu-id="97990-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="97990-119">這僅適用于從 CAL I 開始的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97990-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="97990-120">CAL \_ 使用 \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="97990-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="97990-121">**Windows Me/98、windows 2000：** 使用系統 ANSI 字碼頁 (ACP) ，而不是字串轉譯的地區設定字碼頁。</span><span class="sxs-lookup"><span data-stu-id="97990-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="97990-122">這僅適用于 ANSI 版本的函式，例如 **EnumCalendarInfoA**。</span><span class="sxs-lookup"><span data-stu-id="97990-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="97990-123">下列 CALTYPE 常數是互斥的，無法在函式呼叫中彼此組合使用。</span><span class="sxs-lookup"><span data-stu-id="97990-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="97990-124">常數</span><span class="sxs-lookup"><span data-stu-id="97990-124">Constant</span></span></th>
<th><span data-ttu-id="97990-125">描述</span><span class="sxs-lookup"><span data-stu-id="97990-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="97990-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="97990-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="97990-127">整數值，表示替代日曆的行事曆類型。</span><span class="sxs-lookup"><span data-stu-id="97990-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="97990-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="97990-129"><strong>Windows Me/98、windows 2000：</strong> 整數值，指出兩位數年份範圍的上限。</span><span class="sxs-lookup"><span data-stu-id="97990-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="97990-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="97990-131">一或多個以 null 終止的字串，指定每個紀元範圍的年份位移。</span><span class="sxs-lookup"><span data-stu-id="97990-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="97990-132">最後一個字串有額外的終止 null 字元。</span><span class="sxs-lookup"><span data-stu-id="97990-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="97990-133">此值的格式會視選用行事曆的類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="97990-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="97990-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="97990-135">一周第一天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="97990-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="97990-137">一周中第二天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="97990-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="97990-139">一周第三天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="97990-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="97990-141">一周第四天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="97990-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="97990-143">一周第五天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="97990-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="97990-145">一周第六天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="97990-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="97990-147">一周第七天的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="97990-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="97990-149"><strong>Windows 7 和更新版本：</strong> 紀元的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="97990-150">完整的紀元是由 CAL_SERASTRING 常數表示。</span><span class="sxs-lookup"><span data-stu-id="97990-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="97990-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="97990-152">年度第一個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="97990-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="97990-154">年度第二個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="97990-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="97990-156">年度第三個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="97990-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="97990-158">年度第四個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="97990-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="97990-160">年度第五個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="97990-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="97990-162">年度第六個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="97990-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="97990-164">年度第七個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="97990-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="97990-166">年度第八個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="97990-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="97990-168">年度第九個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="97990-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="97990-170">年度第十個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="97990-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="97990-172">年度第十個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="97990-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="97990-174">年度第十二個月的縮寫原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="97990-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="97990-176">年度第十三個月的縮寫原生名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="97990-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="97990-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="97990-178">替代行事曆的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="97990-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="97990-180">一周第一天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="97990-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="97990-182">一周中第二天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="97990-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="97990-184">一周第三天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="97990-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="97990-186">一周第四天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="97990-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="97990-188">一周第五天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="97990-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="97990-190">一周第六天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="97990-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="97990-192">一周第七天的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="97990-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="97990-194">一或多個以 null 終止的字串，指定每個 Unicode 程式碼點，指定與 CAL_IYEAROFFSETRANGE 相關聯的紀元。</span><span class="sxs-lookup"><span data-stu-id="97990-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="97990-195">最後一個字串有額外的終止 null 字元。</span><span class="sxs-lookup"><span data-stu-id="97990-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="97990-196">此值的格式會視選用行事曆的類型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="97990-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="97990-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="97990-198">行事曆類型的完整日期格式。</span><span class="sxs-lookup"><span data-stu-id="97990-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="97990-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="97990-200"><strong>Windows 7 和更新版本：</strong> 行事曆類型的月份和日期格式。</span><span class="sxs-lookup"><span data-stu-id="97990-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="97990-201">格式與 CAL_SLONGDATE 的格式類似。</span><span class="sxs-lookup"><span data-stu-id="97990-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="97990-202">例如，如果月/日模式是完整月份名稱，後面加上前置零的日號，例如 &quot; 9 月 3 &quot; 日，則格式為 &quot; MMMM dd &quot; 。</span><span class="sxs-lookup"><span data-stu-id="97990-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="97990-203">單引號可以用來插入非格式的字元，例如，以西班牙文表示的「de」。</span><span class="sxs-lookup"><span data-stu-id="97990-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="97990-204">這個行事曆類型只支援一種格式。</span><span class="sxs-lookup"><span data-stu-id="97990-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="97990-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="97990-206">年度第一個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="97990-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="97990-208">年度第二個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="97990-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="97990-210">年度第三個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="97990-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="97990-212">年度第四個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="97990-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="97990-214">年度第五個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="97990-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="97990-216">年度第六個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="97990-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="97990-218">年度第七個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="97990-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="97990-220">年度第八個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="97990-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="97990-222">年度第九個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="97990-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="97990-224">年度第十個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="97990-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="97990-226">年度第十個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="97990-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="97990-228">年度第十二個月的原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="97990-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="97990-230">年度第十三個月的原生名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="97990-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="97990-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="97990-232">行事曆類型的簡短日期格式。</span><span class="sxs-lookup"><span data-stu-id="97990-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="97990-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="97990-234"><strong>Windows Vista 和更新版本：</strong> 一周第一天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="97990-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="97990-236"><strong>Windows Vista 和更新版本：</strong> 一周中第二天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="97990-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="97990-238"><strong>Windows Vista 和更新版本：</strong> 一周第三天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="97990-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="97990-240"><strong>Windows Vista 和更新版本：</strong> 一周第四天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="97990-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="97990-242"><strong>Windows Vista 和更新版本：</strong> 一周第五天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="97990-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="97990-244"><strong>Windows Vista 和更新版本：</strong> 一周第六天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="97990-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="97990-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="97990-246"><strong>Windows Vista 和更新版本：</strong> 一周第七天的簡短原生名稱。</span><span class="sxs-lookup"><span data-stu-id="97990-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="97990-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="97990-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="97990-248"><strong>Windows Me/98、windows 2000：</strong> 指定行事曆的年/月格式。</span><span class="sxs-lookup"><span data-stu-id="97990-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="97990-249">如果一周或某個月份的原生名稱是空字串，則該名稱與對應地區設定資訊中指定的名稱相同，因此不會在此處重複。</span><span class="sxs-lookup"><span data-stu-id="97990-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




