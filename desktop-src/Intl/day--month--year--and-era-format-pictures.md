---
description: 應用程式會使用本主題中所述的元素，來建立以 null 終止的格式圖片字串。
ms.assetid: c18868a9-6912-46fd-93f5-d8021937b049
title: 日、月、年和年代格式的圖片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83439cc33c1caf067b5c6f41234a6f1ddc4dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851819"
---
# <a name="day-month-year-and-era-format-pictures"></a><span data-ttu-id="4d651-103">日、月、年和年代格式的圖片</span><span class="sxs-lookup"><span data-stu-id="4d651-103">Day, Month, Year, and Era Format Pictures</span></span>

<span data-ttu-id="4d651-104">應用程式會使用本主題中所述的元素，來建立以 null 終止的格式圖片字串。</span><span class="sxs-lookup"><span data-stu-id="4d651-104">The application uses the elements described in this topic to construct a null-terminated format picture string.</span></span> <span data-ttu-id="4d651-105">如果使用空格來分隔字串中的元素，這些空格將會出現在輸出字串中的相同位置。</span><span class="sxs-lookup"><span data-stu-id="4d651-105">If spaces are used to separate the elements in the string, these spaces will appear in the same location in the output string.</span></span>

> [!Note]  
> <span data-ttu-id="4d651-106">格式類型 "d"、"g" 和 "y" 必須是小寫，而且字母 "M" 必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="4d651-106">The format types "d", "g", and "y" must be lowercase and the letter "M" must be uppercase.</span></span>

 

<span data-ttu-id="4d651-107">例如，若要取得日期字串 "週三，31 94 年8月"，應用程式會使用「ddd」、「MMM dd yy」圖片字串。</span><span class="sxs-lookup"><span data-stu-id="4d651-107">For example, to get the date string "Wed, Aug 31 94", the application uses the picture string "ddd',' MMM dd yy".</span></span>

<span data-ttu-id="4d651-108">應用程式會使用單引號來標示要完全依照指定顯示的字元。</span><span class="sxs-lookup"><span data-stu-id="4d651-108">The application uses single quotation marks to mark characters to display exactly as specified.</span></span> <span data-ttu-id="4d651-109">如果應用程式必須顯示單引號，則應該在資料列中放入兩個單引號。</span><span class="sxs-lookup"><span data-stu-id="4d651-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="4d651-110">例如，' abc ' ' bar ' 會顯示為 "abc'bar"。</span><span class="sxs-lookup"><span data-stu-id="4d651-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="4d651-111">下表定義用來表示天數的格式類型。</span><span class="sxs-lookup"><span data-stu-id="4d651-111">The following table defines the format types used to represent days.</span></span>



| <span data-ttu-id="4d651-112">格式類型</span><span class="sxs-lookup"><span data-stu-id="4d651-112">Format type</span></span> | <span data-ttu-id="4d651-113">意義</span><span class="sxs-lookup"><span data-stu-id="4d651-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d651-114">d</span><span class="sxs-lookup"><span data-stu-id="4d651-114">d</span></span>           | <span data-ttu-id="4d651-115">一個月中的日，表示單一位數的天數沒有前置零的數位。</span><span class="sxs-lookup"><span data-stu-id="4d651-115">Day of the month as digits without leading zeros for single-digit days.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4d651-116">dd</span><span class="sxs-lookup"><span data-stu-id="4d651-116">dd</span></span>          | <span data-ttu-id="4d651-117">一個月中的第幾天，表示一位數的天數，前置零。</span><span class="sxs-lookup"><span data-stu-id="4d651-117">Day of the month as digits with leading zeros for single-digit days.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4d651-118">ddd</span><span class="sxs-lookup"><span data-stu-id="4d651-118">ddd</span></span>         | <span data-ttu-id="4d651-119">以 [地區設定 \_ SABBREVDAYNAME \*](locale-sabbrev-constants.md)值指定的一周縮寫日期，例如，英文的 "週一" (美國) 。**Windows Vista 和更新版本：** 如果需要一天的簡短版本，您的應用程式應該使用 [地區設定 \_ SSHORTESTDAYNAME \*](locale-sshortestdayname-constants.md)常數。</span><span class="sxs-lookup"><span data-stu-id="4d651-119">Abbreviated day of the week as specified by a [LOCALE\_SABBREVDAYNAME\*](locale-sabbrev-constants.md) value, for example, "Mon" in English (United States).**Windows Vista and later:** If a short version of the day of the week is required, your application should use the [LOCALE\_SSHORTESTDAYNAME\*](locale-sshortestdayname-constants.md) constants.</span></span><br/> |
| <span data-ttu-id="4d651-120">dddd</span><span class="sxs-lookup"><span data-stu-id="4d651-120">dddd</span></span>        | <span data-ttu-id="4d651-121">依[地區設定 \_ SDAYNAME \* ](locale-sdayname-constants.md)值指定之周中的日。</span><span class="sxs-lookup"><span data-stu-id="4d651-121">Day of the week as specified by a [LOCALE\_SDAYNAME\*](locale-sdayname-constants.md) value.</span></span>                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="4d651-122">下表定義用來表示月份的格式類型。</span><span class="sxs-lookup"><span data-stu-id="4d651-122">The following table defines the format types used to represent months.</span></span>



| <span data-ttu-id="4d651-123">格式類型</span><span class="sxs-lookup"><span data-stu-id="4d651-123">Format type</span></span> | <span data-ttu-id="4d651-124">意義</span><span class="sxs-lookup"><span data-stu-id="4d651-124">Meaning</span></span>                                                                                                                                                                          |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d651-125">M</span><span class="sxs-lookup"><span data-stu-id="4d651-125">M</span></span>           | <span data-ttu-id="4d651-126">以月為單位的數位，不含前置零的數位月份。</span><span class="sxs-lookup"><span data-stu-id="4d651-126">Month as digits without leading zeros for single-digit months.</span></span>                                                                                                                   |
| <span data-ttu-id="4d651-127">MM</span><span class="sxs-lookup"><span data-stu-id="4d651-127">MM</span></span>          | <span data-ttu-id="4d651-128">以月為單位的數位，表示單一位數月份的前置零。</span><span class="sxs-lookup"><span data-stu-id="4d651-128">Month as digits with leading zeros for single-digit months.</span></span>                                                                                                                      |
| <span data-ttu-id="4d651-129">MMM</span><span class="sxs-lookup"><span data-stu-id="4d651-129">MMM</span></span>         | <span data-ttu-id="4d651-130">依[地區設定 \_ SABBREVMONTHNAME \* ](locale-sabbrev-constants.md)值指定的縮寫月份，例如英文 (美國) 的「11月」。</span><span class="sxs-lookup"><span data-stu-id="4d651-130">Abbreviated month as specified by a [LOCALE\_SABBREVMONTHNAME\*](locale-sabbrev-constants.md) value, for example, "Nov" in English (United States).</span></span>                             |
| <span data-ttu-id="4d651-131">MMMM</span><span class="sxs-lookup"><span data-stu-id="4d651-131">MMMM</span></span>        | <span data-ttu-id="4d651-132">依[地區設定 \_ SMONTHNAME \* ](locale-smonthname-constants.md)值指定的月份，例如 "十一月" 代表英文 (美國) ，而 "Noviembre" 表示西班牙文 (西班牙) 。</span><span class="sxs-lookup"><span data-stu-id="4d651-132">Month as specified by a [LOCALE\_SMONTHNAME\*](locale-smonthname-constants.md) value, for example, "November" for English (United States), and "Noviembre" for Spanish (Spain).</span></span> |



 

<span data-ttu-id="4d651-133">下表定義用來代表年份的格式類型。</span><span class="sxs-lookup"><span data-stu-id="4d651-133">The following table defines the format types used to represent years.</span></span>



| <span data-ttu-id="4d651-134">格式類型</span><span class="sxs-lookup"><span data-stu-id="4d651-134">Format type</span></span> | <span data-ttu-id="4d651-135">意義</span><span class="sxs-lookup"><span data-stu-id="4d651-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d651-136">y</span><span class="sxs-lookup"><span data-stu-id="4d651-136">y</span></span>           | <span data-ttu-id="4d651-137">只以最後一個位數表示的年份。</span><span class="sxs-lookup"><span data-stu-id="4d651-137">Year represented only by the last digit.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="4d651-138">yy</span><span class="sxs-lookup"><span data-stu-id="4d651-138">yy</span></span>          | <span data-ttu-id="4d651-139">只以最後兩位數表示的年份。</span><span class="sxs-lookup"><span data-stu-id="4d651-139">Year represented only by the last two digits.</span></span> <span data-ttu-id="4d651-140">會為單一位數年份新增前置零。</span><span class="sxs-lookup"><span data-stu-id="4d651-140">A leading zero is added for single-digit years.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="4d651-141">yyyy</span><span class="sxs-lookup"><span data-stu-id="4d651-141">yyyy</span></span>        | <span data-ttu-id="4d651-142">以完整四或五位數表示的年份，取決於所使用的行事曆。</span><span class="sxs-lookup"><span data-stu-id="4d651-142">Year represented by a full four or five digits, depending on the calendar used.</span></span> <span data-ttu-id="4d651-143">泰國曆和韓文日曆有五位數年份。</span><span class="sxs-lookup"><span data-stu-id="4d651-143">Thai Buddhist and Korean calendars have five-digit years.</span></span> <span data-ttu-id="4d651-144">"Yyyy" 模式顯示這兩個行事曆的五位數，以及所有其他支援行事曆的四個數字。</span><span class="sxs-lookup"><span data-stu-id="4d651-144">The "yyyy" pattern shows five digits for these two calendars, and four digits for all other supported calendars.</span></span> <span data-ttu-id="4d651-145">具有單一位數或兩位數年份的行事曆（例如日文天皇紀元）會以不同方式表示。</span><span class="sxs-lookup"><span data-stu-id="4d651-145">Calendars that have single-digit or two-digit years, such as for the Japanese Emperor era, are represented differently.</span></span> <span data-ttu-id="4d651-146">單一位數年份會以前置零表示，例如 "03"。</span><span class="sxs-lookup"><span data-stu-id="4d651-146">A single-digit year is represented with a leading zero, for example, "03".</span></span> <span data-ttu-id="4d651-147">兩位數年份會以兩位數表示，例如 "13"。</span><span class="sxs-lookup"><span data-stu-id="4d651-147">A two-digit year is represented with two digits, for example, "13".</span></span> <span data-ttu-id="4d651-148">不會顯示任何額外的前置零。</span><span class="sxs-lookup"><span data-stu-id="4d651-148">No additional leading zeros are displayed.</span></span> |
| <span data-ttu-id="4d651-149">yyyyy</span><span class="sxs-lookup"><span data-stu-id="4d651-149">yyyyy</span></span>       | <span data-ttu-id="4d651-150">行為與 "yyyy" 相同。</span><span class="sxs-lookup"><span data-stu-id="4d651-150">Behaves identically to "yyyy".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="4d651-151">下表定義用來表示句號或紀元的格式類型。</span><span class="sxs-lookup"><span data-stu-id="4d651-151">The following table defines the format types used to represent a period or era.</span></span>



| <span data-ttu-id="4d651-152">格式類型</span><span class="sxs-lookup"><span data-stu-id="4d651-152">Format type</span></span> | <span data-ttu-id="4d651-153">意義</span><span class="sxs-lookup"><span data-stu-id="4d651-153">Meaning</span></span>                                                                                                                                                                              |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d651-154">g、gg</span><span class="sxs-lookup"><span data-stu-id="4d651-154">g, gg</span></span>       | <span data-ttu-id="4d651-155">依 CAL SERASTRING 值所指定格式化的 Period/紀元字串 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4d651-155">Period/era string formatted as specified by the CAL\_SERASTRING value.</span></span> <span data-ttu-id="4d651-156">如果沒有相關聯的紀元或句號字串，則會忽略日期字串中的 "g" 和 "gg" 格式圖片。</span><span class="sxs-lookup"><span data-stu-id="4d651-156">The "g" and "gg" format pictures in a date string are ignored if there is no associated era or period string.</span></span> |



 

 

 




