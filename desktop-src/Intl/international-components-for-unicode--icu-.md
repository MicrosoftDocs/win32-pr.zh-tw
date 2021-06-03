---
description: Unicode (ICU) 的國際元件是一組成熟、廣泛使用的開放原始碼全球化 Api。
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Unicode 的國際元件 (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349987"
---
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="b3064-103">Unicode 的國際元件 (ICU)</span><span class="sxs-lookup"><span data-stu-id="b3064-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="b3064-104">Unicode (ICU) 的國際元件是一組成熟、廣泛使用的開放原始碼全球化 Api。</span><span class="sxs-lookup"><span data-stu-id="b3064-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="b3064-105">ICU 利用 Unicode 的廣泛通用地區設定資料存放庫 (CLDR) 作為其資料庫，提供軟體應用程式的全球化支援。</span><span class="sxs-lookup"><span data-stu-id="b3064-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="b3064-106">ICU 具有廣泛的可攜性，讓應用程式在所有平臺上都有相同的結果。</span><span class="sxs-lookup"><span data-stu-id="b3064-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="b3064-107">ICU 所提供全球化 API 服務的重點</span><span class="sxs-lookup"><span data-stu-id="b3064-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="b3064-108">**字碼頁轉換**：將文字資料轉換成 Unicode 和幾乎任何其他字元集或編碼。</span><span class="sxs-lookup"><span data-stu-id="b3064-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="b3064-109">在數十年的過程中，ICU 的轉換資料表是以 IBM 收集的字元集資料為基礎，而且是最完整的可用位置。</span><span class="sxs-lookup"><span data-stu-id="b3064-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="b3064-110">定 **序**：根據特定語言、區域或國家/地區的慣例和標準來比較字串。</span><span class="sxs-lookup"><span data-stu-id="b3064-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="b3064-111">ICU 的定序是以 Unicode 定序演算法和 CLDR 的地區設定專屬比較規則為基礎。</span><span class="sxs-lookup"><span data-stu-id="b3064-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="b3064-112">**格式**：根據所選地區設定的慣例來格式化數位、日期、時間和貨幣數量。</span><span class="sxs-lookup"><span data-stu-id="b3064-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="b3064-113">這包括將月份和日名稱轉譯為選取的語言、選擇適當的縮寫、正確地排序欄位等等。這種資料也來自一般地區設定資料存放庫。</span><span class="sxs-lookup"><span data-stu-id="b3064-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="b3064-114">**時間計算**：提供多種類型的行事曆給傳統西曆以外的時間。</span><span class="sxs-lookup"><span data-stu-id="b3064-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="b3064-115">提供一組完整的時區計算 Api。</span><span class="sxs-lookup"><span data-stu-id="b3064-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="b3064-116">**Unicode 支援**： ICU 緊密地追蹤 unicode 標準，可讓您輕鬆存取所有的 unicode 字元屬性、unicode 正規化、案例折迭，以及 [unicode 標準](https://www.unicode.org/)所指定的其他基本作業。</span><span class="sxs-lookup"><span data-stu-id="b3064-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="b3064-117">**正則運算式**： ICU 的正則運算式完全支援 Unicode，同時提供極具競爭力的效能。</span><span class="sxs-lookup"><span data-stu-id="b3064-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="b3064-118">**雙向**：支援處理包含由左到右混合的文字 (英文) ，以及由右至左 (阿拉伯文或希伯來文) 資料。</span><span class="sxs-lookup"><span data-stu-id="b3064-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="b3064-119">如需詳細資訊，您可以造訪 ICU 網站： <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="b3064-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="b3064-120">概觀</span><span class="sxs-lookup"><span data-stu-id="b3064-120">Overview</span></span>

<span data-ttu-id="b3064-121">在 Windows 10 Creators Update 中，ICU 已整合至 Windows，讓 C Api 和資料可供公開存取。</span><span class="sxs-lookup"><span data-stu-id="b3064-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3064-122">Windows 中的 ICU 版本只會公開 C Api。</span><span class="sxs-lookup"><span data-stu-id="b3064-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="b3064-123">它不會公開任何 c + + Api。</span><span class="sxs-lookup"><span data-stu-id="b3064-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="b3064-124">可惜的是，因為 c + + 缺乏穩定的 ABI，所以無法公開 c + + Api。</span><span class="sxs-lookup"><span data-stu-id="b3064-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="b3064-125">如需有關 ICU C Api 的檔，請參閱這裡的官方 ICU 檔頁面： <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="b3064-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="b3064-126">Windows 中 ICU 文件庫的變更歷程記錄</span><span class="sxs-lookup"><span data-stu-id="b3064-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="b3064-127">版本 1703 (建立者更新) </span><span class="sxs-lookup"><span data-stu-id="b3064-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="b3064-128">在此版本中，會先將 ICU 程式庫新增至 Windows 10 作業系統。</span><span class="sxs-lookup"><span data-stu-id="b3064-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="b3064-129">它已新增為：</span><span class="sxs-lookup"><span data-stu-id="b3064-129">It was added as:</span></span>
- <span data-ttu-id="b3064-130">兩個系統 Dll：</span><span class="sxs-lookup"><span data-stu-id="b3064-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="b3064-131">**icuuc.dll** (這是 ICU 的「一般」程式庫) </span><span class="sxs-lookup"><span data-stu-id="b3064-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="b3064-132">**icuin.dll** (這是 ICU 「國際化」程式庫) </span><span class="sxs-lookup"><span data-stu-id="b3064-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="b3064-133">Windows 10 SDK 中有兩個標頭檔：</span><span class="sxs-lookup"><span data-stu-id="b3064-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="b3064-134">**icucommon。h**</span><span class="sxs-lookup"><span data-stu-id="b3064-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="b3064-135">**icui18n。h**</span><span class="sxs-lookup"><span data-stu-id="b3064-135">**icui18n.h**</span></span>
- <span data-ttu-id="b3064-136">Windows 10 SDK 中有兩個匯入程式庫：</span><span class="sxs-lookup"><span data-stu-id="b3064-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="b3064-137">**icuuc .lib**</span><span class="sxs-lookup"><span data-stu-id="b3064-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="b3064-138">**icuin .lib**</span><span class="sxs-lookup"><span data-stu-id="b3064-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="b3064-139">版本 1709 (秋季建立者更新) </span><span class="sxs-lookup"><span data-stu-id="b3064-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="b3064-140">已加入合併的標頭檔（ **icu. h**），其中包含上述兩個標頭檔的內容 (icucommon 和 icui18n) ，而且也會將的型別變更 `UCHAR` 為 `char16_t` 。</span><span class="sxs-lookup"><span data-stu-id="b3064-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="b3064-141">1903版 (2019 更新) </span><span class="sxs-lookup"><span data-stu-id="b3064-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="b3064-142">已加入新的組合 DLL **icu.dll**，其中包含 "common" 和 "國際化" 程式庫。</span><span class="sxs-lookup"><span data-stu-id="b3064-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="b3064-143">此外，已將新的匯入程式庫新增至 Windows 10 SDK： **icu.**.。</span><span class="sxs-lookup"><span data-stu-id="b3064-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="b3064-144">接下來，將不會在舊的標頭中加入新的 Api (icucommon .h 和 icui18n) 或舊的匯入程式庫 (icuuc .lib 和 icuin .lib) 。</span><span class="sxs-lookup"><span data-stu-id="b3064-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="b3064-145">新的 Api 只會加入至合併的標頭 (icu. h) 和合併的匯入程式庫 (icu...... a) 。</span><span class="sxs-lookup"><span data-stu-id="b3064-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="b3064-146">開始使用</span><span class="sxs-lookup"><span data-stu-id="b3064-146">Getting Started</span></span>

<span data-ttu-id="b3064-147">需要遵循三個主要步驟： (Windows 10 Creators Update 或更高版本) </span><span class="sxs-lookup"><span data-stu-id="b3064-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="b3064-148">您的應用程式必須以 Windows 10 1703 版 (建立者更新) 或更高版本為目標。</span><span class="sxs-lookup"><span data-stu-id="b3064-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="b3064-149">加入標頭：</span><span class="sxs-lookup"><span data-stu-id="b3064-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="b3064-150">在 Windows 10 1709 版和更新版本上，您應該改為包含合併的標頭：</span><span class="sxs-lookup"><span data-stu-id="b3064-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="b3064-151">連結至這兩個程式庫：</span><span class="sxs-lookup"><span data-stu-id="b3064-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="b3064-152">icuuc .lib</span><span class="sxs-lookup"><span data-stu-id="b3064-152">icuuc.lib</span></span>
   -   <span data-ttu-id="b3064-153">icuin .lib</span><span class="sxs-lookup"><span data-stu-id="b3064-153">icuin.lib</span></span>

   <span data-ttu-id="b3064-154">在 Windows 10 1903 版和更新版本上，您應該改用組合的程式庫：</span><span class="sxs-lookup"><span data-stu-id="b3064-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="b3064-155">icu. .lib</span><span class="sxs-lookup"><span data-stu-id="b3064-155">icu.lib</span></span>

</dl>

<span data-ttu-id="b3064-156">然後，您可以從您想要的這些程式庫呼叫任何 ICU C API。</span><span class="sxs-lookup"><span data-stu-id="b3064-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="b3064-157"> (不會公開任何 c + + Api。 ) </span><span class="sxs-lookup"><span data-stu-id="b3064-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3064-158">如果您使用舊版的匯入程式庫（icuuc .lib 和 icuin），請確定它們列在 [其他相依性連結器] 設定中的 [] 程式庫之前（例如 onecoreuap .lib 或 >windowsapp）， (查看下圖) 。</span><span class="sxs-lookup"><span data-stu-id="b3064-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="b3064-159">否則，連結器會連結至 icu，這會導致在執行時間嘗試載入 icu.dll。</span><span class="sxs-lookup"><span data-stu-id="b3064-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="b3064-160">只有從1903版開始才會出現該 DLL。</span><span class="sxs-lookup"><span data-stu-id="b3064-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="b3064-161">因此，如果使用者在1903版的 Windows 電腦上升級 Windows 10 SDK，應用程式將無法載入並執行。</span><span class="sxs-lookup"><span data-stu-id="b3064-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="b3064-162">如需 Windows 中 ICU 文件庫的歷程記錄，請參閱 [windows 中 icu 文件庫的變更歷程記錄](#history-of-changes-to-the-icu-library-in-windows)。</span><span class="sxs-lookup"><span data-stu-id="b3064-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![icu 範例](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="b3064-164">這是 [所有平臺] 的設定。</span><span class="sxs-lookup"><span data-stu-id="b3064-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="b3064-165">針對要使用 ICU 的 Win32 應用程式，他們必須先呼叫 [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 。</span><span class="sxs-lookup"><span data-stu-id="b3064-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span> <span data-ttu-id="b3064-166">在 Windows 10 1903 版和更新版本上，可以使用合併的 ICU 程式庫 (icu.dll/icu.lib) ，您可以使用合併的程式庫省略 CoInitializeEx 呼叫。</span><span class="sxs-lookup"><span data-stu-id="b3064-166">On Windows 10 version 1903 and above, where the combined ICU library (icu.dll/icu.lib) is available, you can omit the CoInitializeEx call by using the combined library.</span></span>
> - <span data-ttu-id="b3064-167">並非 ICU Api 所傳回的所有資料都會與 Windows 作業系統一致，因為此對齊工作仍在進行中。</span><span class="sxs-lookup"><span data-stu-id="b3064-167">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="b3064-168">ICU 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="b3064-168">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="b3064-169">範例程式碼片段</span><span class="sxs-lookup"><span data-stu-id="b3064-169">Example code snippet</span></span>

<span data-ttu-id="b3064-170">以下範例說明如何在 c + + UWP 應用程式中使用 ICU Api。</span><span class="sxs-lookup"><span data-stu-id="b3064-170">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="b3064-171"> (它不是完整的獨立應用程式，而只是呼叫 ICU 方法的範例。 ) </span><span class="sxs-lookup"><span data-stu-id="b3064-171">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="b3064-172">下列小型範例假設有方法 **ErrorMessage** 和 **OutputMessage** 會以某種方式將字串輸出至使用者。</span><span class="sxs-lookup"><span data-stu-id="b3064-172">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



