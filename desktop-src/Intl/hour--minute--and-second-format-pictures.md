---
description: 本主題說明用來撰寫時間字串格式圖片的字串格式類型。 每個格式圖片都包含每個格式類型的一個字串組合。
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Hour、Minute 和 Second 格式的圖片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027576"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="eaa19-104">Hour、Minute 和 Second 格式的圖片</span><span class="sxs-lookup"><span data-stu-id="eaa19-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="eaa19-105">本主題說明用來撰寫時間字串格式圖片的字串格式類型。</span><span class="sxs-lookup"><span data-stu-id="eaa19-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="eaa19-106">每個格式圖片都包含每個格式類型的一個字串組合。</span><span class="sxs-lookup"><span data-stu-id="eaa19-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="eaa19-107">在格式類型中，字母 "m"、"s" 和 "t" 必須是小寫，而且字母 "h" 必須是小寫，以表示12小時制或大寫 ( "H" ) 表示24小時制。</span><span class="sxs-lookup"><span data-stu-id="eaa19-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="eaa19-108">單引號可以用來標示應該完全依照指定顯示的字元。</span><span class="sxs-lookup"><span data-stu-id="eaa19-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="eaa19-109">如果應用程式必須顯示單引號，則應該在資料列中放入兩個單引號。</span><span class="sxs-lookup"><span data-stu-id="eaa19-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="eaa19-110">例如，' abc ' ' bar ' 會顯示為 "abc'bar"。</span><span class="sxs-lookup"><span data-stu-id="eaa19-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="eaa19-111">下表定義用來表示小時的格式類型。</span><span class="sxs-lookup"><span data-stu-id="eaa19-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="eaa19-112">String</span><span class="sxs-lookup"><span data-stu-id="eaa19-112">String</span></span> | <span data-ttu-id="eaa19-113">意義</span><span class="sxs-lookup"><span data-stu-id="eaa19-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="eaa19-114">h</span><span class="sxs-lookup"><span data-stu-id="eaa19-114">h</span></span>      | <span data-ttu-id="eaa19-115">單一位數的小時內不含前置零的小時 (12 小時制) 。</span><span class="sxs-lookup"><span data-stu-id="eaa19-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="eaa19-116">hh</span><span class="sxs-lookup"><span data-stu-id="eaa19-116">hh</span></span>     | <span data-ttu-id="eaa19-117">以前置零表示單一位數小時的小時 (12 小時制) 。</span><span class="sxs-lookup"><span data-stu-id="eaa19-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="eaa19-118">H</span><span class="sxs-lookup"><span data-stu-id="eaa19-118">H</span></span>      | <span data-ttu-id="eaa19-119">單一位數的小時內不含前置零的小時 (24 小時制) 。</span><span class="sxs-lookup"><span data-stu-id="eaa19-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="eaa19-120">HH</span><span class="sxs-lookup"><span data-stu-id="eaa19-120">HH</span></span>     | <span data-ttu-id="eaa19-121">以前置零表示單一位數小時的小時 (24 小時制) 。</span><span class="sxs-lookup"><span data-stu-id="eaa19-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="eaa19-122">下表定義用來代表分鐘的格式類型。</span><span class="sxs-lookup"><span data-stu-id="eaa19-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="eaa19-123">String</span><span class="sxs-lookup"><span data-stu-id="eaa19-123">String</span></span> | <span data-ttu-id="eaa19-124">意義</span><span class="sxs-lookup"><span data-stu-id="eaa19-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="eaa19-125">m</span><span class="sxs-lookup"><span data-stu-id="eaa19-125">m</span></span>      | <span data-ttu-id="eaa19-126">單一位數分鐘沒有前置零的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="eaa19-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="eaa19-127">mm</span><span class="sxs-lookup"><span data-stu-id="eaa19-127">mm</span></span>     | <span data-ttu-id="eaa19-128">在單一位數分鐘內使用前置零的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="eaa19-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="eaa19-129">下表定義用來代表秒鐘的格式類型。</span><span class="sxs-lookup"><span data-stu-id="eaa19-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="eaa19-130">String</span><span class="sxs-lookup"><span data-stu-id="eaa19-130">String</span></span> | <span data-ttu-id="eaa19-131">意義</span><span class="sxs-lookup"><span data-stu-id="eaa19-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="eaa19-132">s</span><span class="sxs-lookup"><span data-stu-id="eaa19-132">s</span></span>      | <span data-ttu-id="eaa19-133">單一位數秒沒有前置零的秒數。</span><span class="sxs-lookup"><span data-stu-id="eaa19-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="eaa19-134">ss</span><span class="sxs-lookup"><span data-stu-id="eaa19-134">ss</span></span>     | <span data-ttu-id="eaa19-135">以前置零表示的秒數（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="eaa19-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="eaa19-136">下表定義用來表示時間標記的格式類型。</span><span class="sxs-lookup"><span data-stu-id="eaa19-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="eaa19-137">String</span><span class="sxs-lookup"><span data-stu-id="eaa19-137">String</span></span> | <span data-ttu-id="eaa19-138">意義</span><span class="sxs-lookup"><span data-stu-id="eaa19-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="eaa19-139">t</span><span class="sxs-lookup"><span data-stu-id="eaa19-139">t</span></span>      | <span data-ttu-id="eaa19-140">一個字元的時間標記字串。</span><span class="sxs-lookup"><span data-stu-id="eaa19-140">One-character time marker string.</span></span><br /><span data-ttu-id="eaa19-141">**注意：** 不建議將此格式用於某些語言，例如日文 (日本) 。</span><span class="sxs-lookup"><span data-stu-id="eaa19-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="eaa19-142">使用此格式，應用程式一律會使用時間標記字串中的第一個字元（由 [LOCALE_S1159](locale-s1159.md) (AM) 和 [LOCALE_S2359](locale-s2359.md) (PM) 。</span><span class="sxs-lookup"><span data-stu-id="eaa19-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="eaa19-143">因此，應用程式可以使用 AM 和 PM 所用的相同字串來建立不正確的格式。</span><span class="sxs-lookup"><span data-stu-id="eaa19-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="eaa19-144">tt</span><span class="sxs-lookup"><span data-stu-id="eaa19-144">tt</span></span>     | <span data-ttu-id="eaa19-145">多字元的時間標記字串。</span><span class="sxs-lookup"><span data-stu-id="eaa19-145">Multi-character time marker string.</span></span> |
