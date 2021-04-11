---
description: Windows Vista 引進了大量的函式，這些函式會使用地區設定名稱，而非地區設定識別碼。
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: 呼叫「地區設定名稱」函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58c15d2d9fe7721eb162f8c7cf96084bd4afa2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690252"
---
# <a name="calling-the-locale-name-functions"></a><span data-ttu-id="ff675-103">呼叫「地區設定名稱」函數</span><span class="sxs-lookup"><span data-stu-id="ff675-103">Calling the "Locale Name" Functions</span></span>

<span data-ttu-id="ff675-104">Windows Vista 引進了大量的函式，這些函式會使用 [地區設定名稱](locale-names.md) ，而非 [地區設定識別碼](locale-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="ff675-104">Windows Vista introduces a large number of functions that use [locale names](locale-names.md) instead of [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="ff675-105">這些新函式為 [補充地區](custom-locales.md)設定提供良好的支援，而其中有幾個可提供較舊的 NLS 函式中未提供的額外功能。</span><span class="sxs-lookup"><span data-stu-id="ff675-105">These new functions provide good support for [supplemental locales](custom-locales.md), and several of them provide additional functionality not available in the older NLS functions.</span></span> <span data-ttu-id="ff675-106">其中一些（例如新的列舉函式）也表示設計改進。</span><span class="sxs-lookup"><span data-stu-id="ff675-106">Some of them, such as the new enumeration functions, also represent design improvements.</span></span>

> [!Note]  
> <span data-ttu-id="ff675-107">只在 Windows Vista 和更新版本上執行的應用程式應該使用「地區設定名稱」功能，以喜好設定使用地區設定識別碼的 NLS 函數。</span><span class="sxs-lookup"><span data-stu-id="ff675-107">Applications that are intended to run only on Windows Vista and later should use the "locale name" functions in preference to the NLS functions that use locale identifiers.</span></span>

 

<span data-ttu-id="ff675-108">下表列出地區設定名稱函式，以及它們可以取代的舊版函式。</span><span class="sxs-lookup"><span data-stu-id="ff675-108">The following table lists the locale name functions along with the older functions that they can replace.</span></span>



| <span data-ttu-id="ff675-109">使用地區設定名稱的函式</span><span class="sxs-lookup"><span data-stu-id="ff675-109">Functions using locale names</span></span>                                     | <span data-ttu-id="ff675-110">使用地區設定識別碼的函式</span><span class="sxs-lookup"><span data-stu-id="ff675-110">Functions using locale identifiers</span></span>                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff675-111">**CompareStringEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-111">**CompareStringEx**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)                       | [<span data-ttu-id="ff675-112">**CompareString**</span><span class="sxs-lookup"><span data-stu-id="ff675-112">**CompareString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                                                         |
| [<span data-ttu-id="ff675-113">**EnumCalendarInfoExEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-113">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)             | <span data-ttu-id="ff675-114">[**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)、 [ **EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)</span><span class="sxs-lookup"><span data-stu-id="ff675-114">[**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)</span></span> |
| [<span data-ttu-id="ff675-115">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-115">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)               | <span data-ttu-id="ff675-116">[**EnumDateFormats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa)、 [ **EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)</span><span class="sxs-lookup"><span data-stu-id="ff675-116">[**EnumDateFormats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)</span></span>     |
| [<span data-ttu-id="ff675-117">**EnumSystemLocalesEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-117">**EnumSystemLocalesEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)               | [<span data-ttu-id="ff675-118">**EnumSystemLocales**</span><span class="sxs-lookup"><span data-stu-id="ff675-118">**EnumSystemLocales**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesa)                                                 |
| [<span data-ttu-id="ff675-119">**EnumTimeFormatsEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-119">**EnumTimeFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsex)                   | [<span data-ttu-id="ff675-120">**EnumTimeFormats**</span><span class="sxs-lookup"><span data-stu-id="ff675-120">**EnumTimeFormats**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsa)                                                     |
| [<span data-ttu-id="ff675-121">**FindNLSStringEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-121">**FindNLSStringEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)                       | [<span data-ttu-id="ff675-122">**FindNLSString**</span><span class="sxs-lookup"><span data-stu-id="ff675-122">**FindNLSString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)                                                         |
| [<span data-ttu-id="ff675-123">**GetCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-123">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)                   | [<span data-ttu-id="ff675-124">**GetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="ff675-124">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)                                                     |
| [<span data-ttu-id="ff675-125">**GetCurrencyFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-125">**GetCurrencyFormatEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformatex)               | [<span data-ttu-id="ff675-126">**GetCurrencyFormat**</span><span class="sxs-lookup"><span data-stu-id="ff675-126">**GetCurrencyFormat**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformata)                                                 |
| [<span data-ttu-id="ff675-127">**GetDateFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-127">**GetDateFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)                       | [<span data-ttu-id="ff675-128">**GetDateFormat**</span><span class="sxs-lookup"><span data-stu-id="ff675-128">**GetDateFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)                                                         |
| [<span data-ttu-id="ff675-129">**GetDurationFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-129">**GetDurationFormatEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)               | [<span data-ttu-id="ff675-130">**GetDurationFormat**</span><span class="sxs-lookup"><span data-stu-id="ff675-130">**GetDurationFormat**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)                                                 |
| [<span data-ttu-id="ff675-131">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-131">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)                       | [<span data-ttu-id="ff675-132">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="ff675-132">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)                                                         |
| [<span data-ttu-id="ff675-133">**GetNLSVersionEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-133">**GetNLSVersionEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex)                       | [<span data-ttu-id="ff675-134">**GetNLSVersion**</span><span class="sxs-lookup"><span data-stu-id="ff675-134">**GetNLSVersion**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getnlsversion)                                                         |
| [<span data-ttu-id="ff675-135">**GetNumberFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-135">**GetNumberFormatEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getnumberformatex)                   | [<span data-ttu-id="ff675-136">**GetNumberFormat**</span><span class="sxs-lookup"><span data-stu-id="ff675-136">**GetNumberFormat**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getnumberformata)                                                     |
| [<span data-ttu-id="ff675-137">**GetSystemDefaultLocaleName**</span><span class="sxs-lookup"><span data-stu-id="ff675-137">**GetSystemDefaultLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) | [<span data-ttu-id="ff675-138">**GetSystemDefaultLCID**</span><span class="sxs-lookup"><span data-stu-id="ff675-138">**GetSystemDefaultLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid)                                           |
| [<span data-ttu-id="ff675-139">**GetTimeFormatEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-139">**GetTimeFormatEx**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)                       | [<span data-ttu-id="ff675-140">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="ff675-140">**GetTimeFormat**</span></span>](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                                         |
| [<span data-ttu-id="ff675-141">**GetUserDefaultLocaleName**</span><span class="sxs-lookup"><span data-stu-id="ff675-141">**GetUserDefaultLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)     | [<span data-ttu-id="ff675-142">**GetUserDefaultLCID**</span><span class="sxs-lookup"><span data-stu-id="ff675-142">**GetUserDefaultLCID**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)                                               |
| [<span data-ttu-id="ff675-143">**IsValidLocaleName**</span><span class="sxs-lookup"><span data-stu-id="ff675-143">**IsValidLocaleName**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)                   | [<span data-ttu-id="ff675-144">**IsValidLocale**</span><span class="sxs-lookup"><span data-stu-id="ff675-144">**IsValidLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isvalidlocale)                                                         |
| [<span data-ttu-id="ff675-145">**LCMapStringEx**</span><span class="sxs-lookup"><span data-stu-id="ff675-145">**LCMapStringEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)                           | [<span data-ttu-id="ff675-146">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="ff675-146">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                                                             |



 

## <a name="example"></a><span data-ttu-id="ff675-147">範例</span><span class="sxs-lookup"><span data-stu-id="ff675-147">Example</span></span>

<span data-ttu-id="ff675-148">下列範例顯示如何使用以地區設定名稱為基礎的多個函式 [： NLS：以名稱為基礎的 Api 範例](nls--name-based-apis-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="ff675-148">An example showing the use of several functions based on locale names can be found in [NLS: Name-based APIs Sample](nls--name-based-apis-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff675-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff675-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff675-150">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="ff675-150">Using National Language Support</span></span>](using-national-language-support.md)
</dt> </dl>

 

 
