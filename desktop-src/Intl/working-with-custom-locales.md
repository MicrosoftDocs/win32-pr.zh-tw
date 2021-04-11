---
description: 本主題提供一些指示，說明如何處理應用程式中的自訂地區設定。
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: 使用自訂地區設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943718"
---
# <a name="working-with-custom-locales"></a><span data-ttu-id="8e48c-103">使用自訂地區設定</span><span class="sxs-lookup"><span data-stu-id="8e48c-103">Working with Custom Locales</span></span>

<span data-ttu-id="8e48c-104">本主題提供一些指示，說明如何處理應用程式中的 [自訂地區](custom-locales.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="8e48c-104">This topic provides some instructions for handling [custom locales](custom-locales.md) in your applications.</span></span> <span data-ttu-id="8e48c-105">因為您的應用程式不會控制作業系統上是否已安裝自訂地區設定，所以最好以這些考慮來準備所有的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="8e48c-105">It is best to prepare all your source code with these considerations in mind, as your application does not control whether custom locales are installed on the operating system.</span></span>

## <a name="handle-locale_stime-constant-correctly"></a><span data-ttu-id="8e48c-106">正確處理地區設定 \_ STIME 常數</span><span class="sxs-lookup"><span data-stu-id="8e48c-106">Handle LOCALE\_STIME Constant Correctly</span></span>

<span data-ttu-id="8e48c-107">如果您的繼承應用程式使用 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 取得 [地區設定 \_ STIME](locale-stime-constants.md)所指出的過時時間分隔符號，則應用程式可能無法剖析時間格式。</span><span class="sxs-lookup"><span data-stu-id="8e48c-107">If you have an older application that uses [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to obtain the obsolete time separator indicated by [LOCALE\_STIME](locale-stime-constants.md), the application can fail to parse the time format.</span></span> <span data-ttu-id="8e48c-108">請記住，以分鐘為單位分隔小時的字元與從秒分隔分鐘的字元不同。</span><span class="sxs-lookup"><span data-stu-id="8e48c-108">Remember that the character that separates hours from minutes is distinct from the character that separates minutes from seconds.</span></span>

> [!Note]  
> <span data-ttu-id="8e48c-109">當您針對自訂地區設定進行程式設計時，請記住它們不尋常。</span><span class="sxs-lookup"><span data-stu-id="8e48c-109">When programming for custom locales, remember that they are unusual.</span></span> <span data-ttu-id="8e48c-110">所有適用于 NLS 的欄位幾乎都必須處理不尋常的行為。</span><span class="sxs-lookup"><span data-stu-id="8e48c-110">Virtually every field available to NLS has to cope with unusual behavior.</span></span> <span data-ttu-id="8e48c-111">例如，時間格式 12H34 ' 12 ' ' 是合法的，而且通常是可理解的。</span><span class="sxs-lookup"><span data-stu-id="8e48c-111">For example, the time format 12H34'12'' is legitimate and generally understandable.</span></span> <span data-ttu-id="8e48c-112">但許多應用程式也會對可能會中斷緩衝區長度或顯示欄位的時間分隔符號提出假設。</span><span class="sxs-lookup"><span data-stu-id="8e48c-112">Yet many applications make assumptions about the time separators that can break buffer lengths or display fields.</span></span>

 

## <a name="distinguish-among-supplemental-locales"></a><span data-ttu-id="8e48c-113">區分補充地區設定</span><span class="sxs-lookup"><span data-stu-id="8e48c-113">Distinguish Among Supplemental Locales</span></span>

<span data-ttu-id="8e48c-114">所有補充地區設定都使用地區設定[識別碼](locale-identifiers.md)的[地區設定 \_ 自訂 \_ 未指定](locale-custom-constants.md)常數。</span><span class="sxs-lookup"><span data-stu-id="8e48c-114">All supplemental locales use the [LOCALE\_CUSTOM\_UNSPECIFIED](locale-custom-constants.md) constant for the [locale identifier](locale-identifiers.md).</span></span> <span data-ttu-id="8e48c-115">[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)無法區別補充的地區設定，但 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)可能是因為它使用地區設定 [名稱](locale-names.md)，而非地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e48c-115">As a rule, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) cannot distinguish among supplemental locales, but [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) can because it uses [locale names](locale-names.md) instead of locale identifiers.</span></span> <span data-ttu-id="8e48c-116">只有當該地區設定是目前選取的使用者地區設定時，您的應用程式才能取得特定補充地區設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e48c-116">Your application can retrieve information about a particular supplemental locale only when that locale is the currently selected user locale.</span></span> <span data-ttu-id="8e48c-117">然後，應用程式可以呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 並傳遞常數 [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md) 作為地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e48c-117">Then, the application can call [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and pass the constant [LOCALE\_USER\_DEFAULT](locale-user-default.md) as the locale identifier.</span></span>

## <a name="handle-replacement-locales"></a><span data-ttu-id="8e48c-118">處理取代地區設定</span><span class="sxs-lookup"><span data-stu-id="8e48c-118">Handle Replacement Locales</span></span>

<span data-ttu-id="8e48c-119">若要保留 Windows 的可靠性，請記住，您的應用程式所支援的取代地區設定無法修改取代地區設定的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e48c-119">To preserve the reliability of Windows, remember that a replacement locale supported by your application cannot modify the locale identifier of the replaced locale.</span></span> <span data-ttu-id="8e48c-120">取代地區設定都不能修改 Windows 的排序屬性。</span><span class="sxs-lookup"><span data-stu-id="8e48c-120">Neither can a replacement locale modify the sorting properties of Windows.</span></span>

<span data-ttu-id="8e48c-121">雖然取代地區設定可以變更預設行事曆，但它必須將原始預設值保留在可用行事曆清單中的某個位置。</span><span class="sxs-lookup"><span data-stu-id="8e48c-121">Although a replacement locale can change the default calendar, it must retain the original default somewhere in the list of available calendars.</span></span> <span data-ttu-id="8e48c-122">例如，泰文 (泰國) 地區設定會使用泰文曆日曆作為預設值。</span><span class="sxs-lookup"><span data-stu-id="8e48c-122">For example, the Thai (Thailand) locale uses the Thai Buddhist calendar as the default.</span></span> <span data-ttu-id="8e48c-123">系統管理員可以建立使用西曆當地語系化日曆的取代地區設定。</span><span class="sxs-lookup"><span data-stu-id="8e48c-123">An administrator can create a replacement locale that uses the Gregorian localized calendar.</span></span> <span data-ttu-id="8e48c-124">不過，可用的行事曆清單會繼續包含泰國曆日曆的專案。</span><span class="sxs-lookup"><span data-stu-id="8e48c-124">However, the list of available calendars continues to contain an entry for the Thai Buddhist calendar.</span></span>

<span data-ttu-id="8e48c-125">針對取代地區設定，您的應用程式通常應該查閱地區設定特定資訊，而不是根據特定地區設定的知識來嘗試「快捷方式」。</span><span class="sxs-lookup"><span data-stu-id="8e48c-125">For replacement locales, your application should generally consult locale-specific information instead of attempting a "shortcut" based on knowledge of a certain locale.</span></span> <span data-ttu-id="8e48c-126">例如，當 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) 將目前的地區設定視為英文 (美國) 時，實際上可能是應允許生效的取代地區設定。</span><span class="sxs-lookup"><span data-stu-id="8e48c-126">For example, when [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) retrieves the current locale as English (United States), it might actually be a replacement locale that should be allowed to take effect.</span></span>

## <a name="customize-calendars"></a><span data-ttu-id="8e48c-127">自訂行事曆</span><span class="sxs-lookup"><span data-stu-id="8e48c-127">Customize Calendars</span></span>

<span data-ttu-id="8e48c-128">您的應用程式可以針對西曆自訂日期和月份名稱，但不能針對非西曆行事曆。</span><span class="sxs-lookup"><span data-stu-id="8e48c-128">Your applications can customize day and month names for Gregorian calendars, but not for non-Gregorian calendars.</span></span> <span data-ttu-id="8e48c-129">同樣地，NLS 不支援建立使用者定義的自訂行事曆。</span><span class="sxs-lookup"><span data-stu-id="8e48c-129">Similarly, NLS does not support creation of user-defined custom calendars.</span></span> <span data-ttu-id="8e48c-130">如需詳細資訊，請參閱 [日期和行事曆](date-and-calendar.md)。</span><span class="sxs-lookup"><span data-stu-id="8e48c-130">For more information, see [Date and Calendar](date-and-calendar.md).</span></span>

## <a name="handle-sorting-sequences"></a><span data-ttu-id="8e48c-131">處理排序次序</span><span class="sxs-lookup"><span data-stu-id="8e48c-131">Handle Sorting Sequences</span></span>

<span data-ttu-id="8e48c-132">補充地區設定可以使用任何 Microsoft 定義的排序次序。</span><span class="sxs-lookup"><span data-stu-id="8e48c-132">A supplemental locale can use any Microsoft-defined sorting sequence.</span></span> <span data-ttu-id="8e48c-133">取代地區設定必須使用與其所取代之地區設定相同的排序次序。</span><span class="sxs-lookup"><span data-stu-id="8e48c-133">A replacement locale must use the same sorting sequence as the locale it replaces.</span></span> <span data-ttu-id="8e48c-134">NLS 不支援建立使用者定義的排序次序。</span><span class="sxs-lookup"><span data-stu-id="8e48c-134">NLS does not support the creation of user-defined sorting sequences.</span></span> <span data-ttu-id="8e48c-135">如需詳細資訊，請參閱 [在您的應用程式中處理排序](handling-sorting-in-your-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="8e48c-135">For more information, see [Handling Sorting in Your Applications](handling-sorting-in-your-applications.md).</span></span>

## <a name="localize-custom-locale-information"></a><span data-ttu-id="8e48c-136">將自訂地區設定資訊當地語系化</span><span class="sxs-lookup"><span data-stu-id="8e48c-136">Localize Custom Locale Information</span></span>

<span data-ttu-id="8e48c-137">NLS 不提供當地語系化自訂地區設定資訊的機制。</span><span class="sxs-lookup"><span data-stu-id="8e48c-137">NLS does not provide a mechanism for localizing custom locale information.</span></span> <span data-ttu-id="8e48c-138">因此，用來做為自訂地區設定之地區設定識別碼的常數 [地區設定 \_ SLANGUAGE](locale-slanguage.md) 或 [地區設定 \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) 一律會抓取與 [地區設定 \_ SNATIVELANGNAME](locale-snative-constants.md) 或 [地區設定 \_ SNATIVELANGUAGENAME](locale-snative-constants.md)相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="8e48c-138">Thus the constant [LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) used as a locale identifier for a custom locale always retrieves values associated with [LOCALE\_SNATIVELANGNAME](locale-snative-constants.md) or [LOCALE\_SNATIVELANGUAGENAME](locale-snative-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e48c-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e48c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e48c-140">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="8e48c-140">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="8e48c-141">自訂地區設定</span><span class="sxs-lookup"><span data-stu-id="8e48c-141">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="8e48c-142">日期和行事曆</span><span class="sxs-lookup"><span data-stu-id="8e48c-142">Date and Calendar</span></span>](date-and-calendar.md)
</dt> <dt>

[<span data-ttu-id="8e48c-143">處理應用程式中的排序</span><span class="sxs-lookup"><span data-stu-id="8e48c-143">Handling Sorting in Your Applications</span></span>](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



