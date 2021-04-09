---
description: 本主題定義 (資料類型 CALID) 的行事曆識別碼，用來指定不同的行事曆。
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: 行事曆識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690255"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="c3b43-103">行事曆識別碼</span><span class="sxs-lookup"><span data-stu-id="c3b43-103">Calendar Identifiers</span></span>

<span data-ttu-id="c3b43-104">本主題定義 (資料類型 CALID) 的行事曆識別碼，用來指定不同的行事曆。</span><span class="sxs-lookup"><span data-stu-id="c3b43-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="c3b43-105">當您使用下列 NLS 函數和回呼函式時，您的應用程式可以使用這些識別碼，這些函數具有採用 CALID 資料類型的參數：</span><span class="sxs-lookup"><span data-stu-id="c3b43-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="c3b43-106">**ConvertSystemTimeToCalDateTime**</span><span class="sxs-lookup"><span data-stu-id="c3b43-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="c3b43-107">**EnumCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="c3b43-108">**EnumCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="c3b43-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="c3b43-109">**EnumCalendarInfoExEx**</span><span class="sxs-lookup"><span data-stu-id="c3b43-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="c3b43-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3b43-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="c3b43-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3b43-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="c3b43-112">**GetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="c3b43-113">**GetCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="c3b43-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="c3b43-114">**GetCalendarSupportedDateRange**</span><span class="sxs-lookup"><span data-stu-id="c3b43-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="c3b43-115">**IsCalendarLeapYear**</span><span class="sxs-lookup"><span data-stu-id="c3b43-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="c3b43-116">**SetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="c3b43-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="c3b43-117">以下是定義的值。</span><span class="sxs-lookup"><span data-stu-id="c3b43-117">The following values are defined.</span></span> <span data-ttu-id="c3b43-118">所有其他值都是保留的。</span><span class="sxs-lookup"><span data-stu-id="c3b43-118">All other values are reserved.</span></span> <span data-ttu-id="c3b43-119">這些值無法彼此結合。</span><span class="sxs-lookup"><span data-stu-id="c3b43-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="c3b43-120">行事曆識別碼</span><span class="sxs-lookup"><span data-stu-id="c3b43-120">Calendar identifier</span></span>

<span data-ttu-id="c3b43-121">意義</span><span class="sxs-lookup"><span data-stu-id="c3b43-121">Meaning</span></span>

<span data-ttu-id="c3b43-122">1</span><span class="sxs-lookup"><span data-stu-id="c3b43-122">1</span></span>

<span data-ttu-id="c3b43-123">CAL \_ 西曆</span><span class="sxs-lookup"><span data-stu-id="c3b43-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="c3b43-124">西曆 (當地語系化) </span><span class="sxs-lookup"><span data-stu-id="c3b43-124">Gregorian (localized)</span></span>

<span data-ttu-id="c3b43-125">2</span><span class="sxs-lookup"><span data-stu-id="c3b43-125">2</span></span>

<span data-ttu-id="c3b43-126">CAL \_ \_ 美國西曆</span><span class="sxs-lookup"><span data-stu-id="c3b43-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="c3b43-127">西曆 (的英文字串一律) </span><span class="sxs-lookup"><span data-stu-id="c3b43-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="c3b43-128">3</span><span class="sxs-lookup"><span data-stu-id="c3b43-128">3</span></span>

<span data-ttu-id="c3b43-129">CAL \_ 日本</span><span class="sxs-lookup"><span data-stu-id="c3b43-129">CAL\_JAPAN</span></span>

<span data-ttu-id="c3b43-130">日文天皇紀元</span><span class="sxs-lookup"><span data-stu-id="c3b43-130">Japanese Emperor Era</span></span>

<span data-ttu-id="c3b43-131">4</span><span class="sxs-lookup"><span data-stu-id="c3b43-131">4</span></span>

<span data-ttu-id="c3b43-132">CAL \_ 臺灣</span><span class="sxs-lookup"><span data-stu-id="c3b43-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="c3b43-133">臺灣日曆</span><span class="sxs-lookup"><span data-stu-id="c3b43-133">Taiwan calendar</span></span>

<span data-ttu-id="c3b43-134">5</span><span class="sxs-lookup"><span data-stu-id="c3b43-134">5</span></span>

<span data-ttu-id="c3b43-135">CAL \_ 韓國</span><span class="sxs-lookup"><span data-stu-id="c3b43-135">CAL\_KOREA</span></span>

<span data-ttu-id="c3b43-136">韓文 Tangun 紀元</span><span class="sxs-lookup"><span data-stu-id="c3b43-136">Korean Tangun Era</span></span>

<span data-ttu-id="c3b43-137">6</span><span class="sxs-lookup"><span data-stu-id="c3b43-137">6</span></span>

<span data-ttu-id="c3b43-138">CAL \_ 回曆</span><span class="sxs-lookup"><span data-stu-id="c3b43-138">CAL\_HIJRI</span></span>

<span data-ttu-id="c3b43-139">阿拉伯 (阿拉伯陰曆) </span><span class="sxs-lookup"><span data-stu-id="c3b43-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="c3b43-140">7</span><span class="sxs-lookup"><span data-stu-id="c3b43-140">7</span></span>

<span data-ttu-id="c3b43-141">CAL \_ 泰文</span><span class="sxs-lookup"><span data-stu-id="c3b43-141">CAL\_THAI</span></span>

<span data-ttu-id="c3b43-142">泰文</span><span class="sxs-lookup"><span data-stu-id="c3b43-142">Thai</span></span>

<span data-ttu-id="c3b43-143">8</span><span class="sxs-lookup"><span data-stu-id="c3b43-143">8</span></span>

<span data-ttu-id="c3b43-144">CAL \_ 希伯來文</span><span class="sxs-lookup"><span data-stu-id="c3b43-144">CAL\_HEBREW</span></span>

<span data-ttu-id="c3b43-145">希伯來文 (陰曆) </span><span class="sxs-lookup"><span data-stu-id="c3b43-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="c3b43-146">9</span><span class="sxs-lookup"><span data-stu-id="c3b43-146">9</span></span>

<span data-ttu-id="c3b43-147">CAL \_ 西曆 \_ （ \_ 法文）</span><span class="sxs-lookup"><span data-stu-id="c3b43-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="c3b43-148">Gregorian Middle East French</span><span class="sxs-lookup"><span data-stu-id="c3b43-148">Gregorian Middle East French</span></span>

<span data-ttu-id="c3b43-149">10</span><span class="sxs-lookup"><span data-stu-id="c3b43-149">10</span></span>

<span data-ttu-id="c3b43-150">CAL \_ 西曆 \_ 阿拉伯</span><span class="sxs-lookup"><span data-stu-id="c3b43-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="c3b43-151">Gregorian Arabic</span><span class="sxs-lookup"><span data-stu-id="c3b43-151">Gregorian Arabic</span></span>

<span data-ttu-id="c3b43-152">11</span><span class="sxs-lookup"><span data-stu-id="c3b43-152">11</span></span>

<span data-ttu-id="c3b43-153">CAL \_ 西曆 \_ XLIT \_ 英文</span><span class="sxs-lookup"><span data-stu-id="c3b43-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="c3b43-154">西曆（英文）</span><span class="sxs-lookup"><span data-stu-id="c3b43-154">Gregorian transliterated English</span></span>

<span data-ttu-id="c3b43-155">12</span><span class="sxs-lookup"><span data-stu-id="c3b43-155">12</span></span>

<span data-ttu-id="c3b43-156">CAL \_ 西曆 \_ XLIT \_ 法文</span><span class="sxs-lookup"><span data-stu-id="c3b43-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="c3b43-157">西曆（法文）</span><span class="sxs-lookup"><span data-stu-id="c3b43-157">Gregorian transliterated French</span></span>

<span data-ttu-id="c3b43-158">23</span><span class="sxs-lookup"><span data-stu-id="c3b43-158">23</span></span>

<span data-ttu-id="c3b43-159">CAL \_ UMALQURA</span><span class="sxs-lookup"><span data-stu-id="c3b43-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="c3b43-160">**Windows Vista 和更新版本：** (阿拉伯文陰曆) 行事曆的 Um Al</span><span class="sxs-lookup"><span data-stu-id="c3b43-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="c3b43-161">識別碼 CAL \_ 西曆 \_ XLIT \_ 法文和 CAL UMALQURA 之間的編號間隔是刻意的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3b43-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="c3b43-162">CAL UMALQURA 的指示項 \_ 是23，不是13。</span><span class="sxs-lookup"><span data-stu-id="c3b43-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="c3b43-163">此外， [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) 和 [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) 可讓您使用值列舉所有行事 \_ \_ 歷來要求所有適用行事曆的列舉。</span><span class="sxs-lookup"><span data-stu-id="c3b43-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="c3b43-164">值</span><span class="sxs-lookup"><span data-stu-id="c3b43-164">Value</span></span>

<span data-ttu-id="c3b43-165">意義</span><span class="sxs-lookup"><span data-stu-id="c3b43-165">Meaning</span></span>

<span data-ttu-id="c3b43-166">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="c3b43-166">0xffffffff</span></span>

<span data-ttu-id="c3b43-167">列舉 \_ 所有行事 \_ 曆</span><span class="sxs-lookup"><span data-stu-id="c3b43-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="c3b43-168">所有適用于指定地區設定的行事曆</span><span class="sxs-lookup"><span data-stu-id="c3b43-168">All applicable calendars for the specified locale</span></span>



 

 

 
