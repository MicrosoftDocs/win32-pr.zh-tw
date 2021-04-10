---
description: 日本曆的紀元處理方式
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: 日本曆的紀元處理方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851811"
---
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="d211a-103">日本曆的紀元處理方式</span><span class="sxs-lookup"><span data-stu-id="d211a-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="d211a-104">許多行事曆都有紀元，例如 AD/BC 或 CE/BCE。</span><span class="sxs-lookup"><span data-stu-id="d211a-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="d211a-105">在日文日曆中，年份會以 nengō（年份數目和紀元名稱的組合）來描述。</span><span class="sxs-lookup"><span data-stu-id="d211a-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="d211a-106">例如，2009是 Heisei 21。</span><span class="sxs-lookup"><span data-stu-id="d211a-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="d211a-107">在過去，日文紀元名稱經常變更，但現在日文的紀元只會在每個英制上變更。</span><span class="sxs-lookup"><span data-stu-id="d211a-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="d211a-108">在過去，Windows 和 Microsoft .NET 在此原則下支援四個新式的紀元： Meiji、Taishō、Shōwa 和 Heisei。</span><span class="sxs-lookup"><span data-stu-id="d211a-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="d211a-109">有了 Windows 7、Windows Server 2008 R2 和 .NET Framework 4，Microsoft 就能辨識未來可能會加入額外的紀元。</span><span class="sxs-lookup"><span data-stu-id="d211a-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="d211a-110">在這些版本的 Windows 上，紀中繼資料會儲存在登錄中的機碼底下：</span><span class="sxs-lookup"><span data-stu-id="d211a-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="d211a-111">HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Nls 行事 \\ 曆 \\ 日文 \\ 紀元</span><span class="sxs-lookup"><span data-stu-id="d211a-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="d211a-112">如有必要，您可以透過一般的 Windows Update 程式，將額外的紀元新增至該索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d211a-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="d211a-113">您可以使用登錄編輯程式 (Regedit.exe) 來查看此機碼。</span><span class="sxs-lookup"><span data-stu-id="d211a-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="d211a-114">Windows 7 隨附的金鑰和值的範例如下：</span><span class="sxs-lookup"><span data-stu-id="d211a-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="d211a-115">每個紀元值的名稱都是紀元開始于西曆的日期。</span><span class="sxs-lookup"><span data-stu-id="d211a-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="d211a-116">值包含日文的紀元名稱、日文的縮寫名稱、英文的名稱，以及英文的縮寫名稱：</span><span class="sxs-lookup"><span data-stu-id="d211a-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="d211a-117">"YYYY MM DD" = "JE \_ AJE \_ EE \_ AEE"</span><span class="sxs-lookup"><span data-stu-id="d211a-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="d211a-118">"YYYY MM DD" 是年、月、日、年是4位數、日是2位數，且月份也是2位數的紀元開始日期。</span><span class="sxs-lookup"><span data-stu-id="d211a-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="d211a-119">以空格分隔日期的每個部分。</span><span class="sxs-lookup"><span data-stu-id="d211a-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="d211a-120">「JE」是紀元的日文名稱，後面接著底線。</span><span class="sxs-lookup"><span data-stu-id="d211a-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="d211a-121">"AJE" 是紀元的縮寫名稱，以日文為開頭，後面接著底線。</span><span class="sxs-lookup"><span data-stu-id="d211a-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="d211a-122">"EE" 是日文紀元的英文名稱，後面接著底線。</span><span class="sxs-lookup"><span data-stu-id="d211a-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="d211a-123">"AEE" 是日文紀元的縮寫英文名稱。</span><span class="sxs-lookup"><span data-stu-id="d211a-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="d211a-124">應用程式開發人員的其中一個考慮是，Windows Update 或其他方式將額外的紀元新增至其他紀元的可能性。</span><span class="sxs-lookup"><span data-stu-id="d211a-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="d211a-125">在這種情況下，應用程式可能會遇到日文行事曆預期的四個紀元。</span><span class="sxs-lookup"><span data-stu-id="d211a-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="d211a-126">針對測試用途，測試人員可能會在登錄中加入額外的紀元;不過，這應該限制為僅測試電腦，因為它會影響整部電腦的行為。</span><span class="sxs-lookup"><span data-stu-id="d211a-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="d211a-127">以下是可用於測試的這類金鑰範例。</span><span class="sxs-lookup"><span data-stu-id="d211a-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="d211a-128">您可以使用登錄編輯程式來進行這種變更。</span><span class="sxs-lookup"><span data-stu-id="d211a-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="d211a-129"> (此範例僅供測試使用，且不適合用來預測未來的任何新增專案。 ) </span><span class="sxs-lookup"><span data-stu-id="d211a-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="d211a-130">請注意，這只會影響執行 Windows 7 和更新版本或 .NET Framework 4 和更新版本的機器。</span><span class="sxs-lookup"><span data-stu-id="d211a-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="d211a-131">應用程式開發人員可以使用這類額外的測試紀元來測試其應用程式，以確保其應用程式在未來的時間加入額外的紀元時仍能繼續運作。</span><span class="sxs-lookup"><span data-stu-id="d211a-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d211a-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="d211a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d211a-133">正在抓取時間和日期資訊</span><span class="sxs-lookup"><span data-stu-id="d211a-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="d211a-134">行事曆識別碼</span><span class="sxs-lookup"><span data-stu-id="d211a-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 



