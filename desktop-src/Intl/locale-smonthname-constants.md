---
description: 地區設定 \_ SMONTHNAME \* 常數
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: LOCALE_SMONTHNAME * 常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691079"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="2c9af-103">地區設定 \_ SMONTHNAME \* 常數</span><span class="sxs-lookup"><span data-stu-id="2c9af-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="2c9af-104">本主題定義 NLS 所使用的地區設定 \_ SMONTHNAME \* 常數。</span><span class="sxs-lookup"><span data-stu-id="2c9af-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c9af-105">值</span><span class="sxs-lookup"><span data-stu-id="2c9af-105">Value</span></span></th>
<th><span data-ttu-id="2c9af-106">意義</span><span class="sxs-lookup"><span data-stu-id="2c9af-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c9af-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="2c9af-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="2c9af-108">1月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-108">Native long name for January.</span></span> <span data-ttu-id="2c9af-109">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2c9af-110">使用 LOCALE_SMONTHNAME \* 常數來呼叫 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> 或 <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> 函式會傳回月份名稱的獨立或 nominative 形式。</span><span class="sxs-lookup"><span data-stu-id="2c9af-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="2c9af-111">若要取得 month 格式的月份名稱，應用程式會使用 ddMMMM 的日期圖片來呼叫 <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> 或 <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> ，並從抓取的字串開頭移除兩個數字。</span><span class="sxs-lookup"><span data-stu-id="2c9af-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c9af-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="2c9af-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="2c9af-113">二月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-113">Native long name for February.</span></span> <span data-ttu-id="2c9af-114">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-115">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c9af-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="2c9af-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="2c9af-117">三月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-117">Native long name for March.</span></span> <span data-ttu-id="2c9af-118">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-119">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c9af-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="2c9af-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="2c9af-121">四月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-121">Native long name for April.</span></span> <span data-ttu-id="2c9af-122">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-123">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c9af-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="2c9af-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="2c9af-125">可能的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-125">Native long name for May.</span></span> <span data-ttu-id="2c9af-126">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-127">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c9af-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="2c9af-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="2c9af-129">六月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-129">Native long name for June.</span></span> <span data-ttu-id="2c9af-130">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-131">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c9af-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="2c9af-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="2c9af-133">七月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-133">Native long name for July.</span></span> <span data-ttu-id="2c9af-134">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-135">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c9af-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="2c9af-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="2c9af-137">八月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-137">Native long name for August.</span></span> <span data-ttu-id="2c9af-138">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-139">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c9af-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="2c9af-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="2c9af-141">9月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-141">Native long name for September.</span></span> <span data-ttu-id="2c9af-142">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-143">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c9af-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="2c9af-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="2c9af-145">十月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-145">Native long name for October.</span></span> <span data-ttu-id="2c9af-146">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-147">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c9af-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="2c9af-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="2c9af-149">11月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-149">Native long name for November.</span></span> <span data-ttu-id="2c9af-150">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-151">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c9af-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="2c9af-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="2c9af-153">12月的原生完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2c9af-153">Native long name for December.</span></span> <span data-ttu-id="2c9af-154">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-155">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c9af-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="2c9af-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="2c9af-157">第13個月的原生名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="2c9af-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="2c9af-158">此字串允許的最大字元數為80，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="2c9af-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="2c9af-159">請參閱 LOCALE_SMONTHNAME1 的注意事項。</span><span class="sxs-lookup"><span data-stu-id="2c9af-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




