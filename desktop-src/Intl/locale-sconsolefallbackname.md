---
description: 地區設定 \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985183"
---
# <a name="locale_sconsolefallbackname"></a><span data-ttu-id="58853-103">地區設定 \_ SCONSOLEFALLBACKNAME</span><span class="sxs-lookup"><span data-stu-id="58853-103">LOCALE\_SCONSOLEFALLBACKNAME</span></span>

<span data-ttu-id="58853-104">**Windows Vista 和更新版本：** 用於主控台顯示的慣用地區設定。</span><span class="sxs-lookup"><span data-stu-id="58853-104">**Windows Vista and later:** Preferred locale to use for console display.</span></span> <span data-ttu-id="58853-105">此字串允許的最大字元數為85，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="58853-105">The maximum number of characters allowed for this string is 85, including a terminating null character.</span></span>

> [!Note]  
> <span data-ttu-id="58853-106">一般情況下，應用程式不應該直接使用地區設定 \_ SCONSOLEFALLBACKNAME 資料。</span><span class="sxs-lookup"><span data-stu-id="58853-106">In general, applications should not make direct use of LOCALE\_SCONSOLEFALLBACKNAME data.</span></span> <span data-ttu-id="58853-107">若要判斷要在主控台視窗中使用哪些語言資源，應用程式應該呼叫 [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) 或 [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)。</span><span class="sxs-lookup"><span data-stu-id="58853-107">To determine what language resources to use in a console window, an application should call either [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="58853-108">這些函式會在選擇可在主控台中辨認的語言時，使用主控台回溯資料作為一個因素，但不是唯一的行列式。</span><span class="sxs-lookup"><span data-stu-id="58853-108">These functions use the console fallback data as a factor in choosing a language that is legible in the console, but it is not the sole determinant.</span></span> <span data-ttu-id="58853-109">特別是，主控台只會顯示單一字碼頁的字元。</span><span class="sxs-lookup"><span data-stu-id="58853-109">In particular, the console is limited to displaying characters from a single code page.</span></span> <span data-ttu-id="58853-110">例如，希臘文 (希臘) 的 el-GR 是有效的主控台語言，但如果目前的主控台字碼頁是拉丁-1 (字碼頁 1252) 則主控台會以一系列字元找不到的符號來顯示希臘文文字。</span><span class="sxs-lookup"><span data-stu-id="58853-110">For example, el-GR for Greek (Greece) is a valid console language, but if the current console code page is Latin-1 (code page 1252) the console displays Greek text mostly as a series of character-not-found symbols.</span></span>

 

<span data-ttu-id="58853-111">如果主控台中支援對應到此地區設定的語言，則此值與 [地區設定 \_ SNAME](locale-sname.md)的值相同，也就是，地區設定本身可以用來顯示主控台。</span><span class="sxs-lookup"><span data-stu-id="58853-111">If the language corresponding to this locale is supported in the console, the value is the same as that for [LOCALE\_SNAME](locale-sname.md), that is, the locale itself can be used for console display.</span></span> <span data-ttu-id="58853-112">不過，主控台無法顯示只能使用 [Uniscribe](uniscribe.md)轉譯的語言。</span><span class="sxs-lookup"><span data-stu-id="58853-112">However, the console cannot display languages that can be rendered only with [Uniscribe](uniscribe.md).</span></span> <span data-ttu-id="58853-113">例如，主控台無法顯示阿拉伯文或不同的印度語言。</span><span class="sxs-lookup"><span data-stu-id="58853-113">For example, the console cannot display Arabic or the various Indic languages.</span></span> <span data-ttu-id="58853-114">因此， \_ 對應于這些語言之地區設定的地區設定 SCONSOLEFALLBACKNAME 值，與地區設定 SNAME 的值不同 \_ 。</span><span class="sxs-lookup"><span data-stu-id="58853-114">Therefore, the LOCALE\_SCONSOLEFALLBACKNAME value for locales corresponding to these languages is different from the value for LOCALE\_SNAME.</span></span>

<span data-ttu-id="58853-115">針對預先定義的地區設定，如果 fallback 值與地區設定本身的值不同，則會使用中性地區設定的值。</span><span class="sxs-lookup"><span data-stu-id="58853-115">For predefined locales, if the fallback value is different from the value for the locale itself, the value for the neutral locale is used.</span></span> <span data-ttu-id="58853-116">特定地區設定會與語言和國家/地區相關聯，而中性地區設定會與語言相關聯，但不會與任何國家/地區相關聯。</span><span class="sxs-lookup"><span data-stu-id="58853-116">A specific locale is associated with both a language and a country/region, while a neutral locale is associated with a language but is not associated with any country/region.</span></span> <span data-ttu-id="58853-117">例如，ar-SA 會回復為 "en"，而不是 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="58853-117">For example, ar-SA falls back to "en", not to "en-US".</span></span> <span data-ttu-id="58853-118">使用中性地區設定的這項原則會針對預先定義的地區設定一致地執行，強烈建議自訂地區設定。</span><span class="sxs-lookup"><span data-stu-id="58853-118">This policy of using neutral locales is implemented consistently for predefined locales and is strongly recommended for custom locales.</span></span> <span data-ttu-id="58853-119">不過，不會強制執行此原則。</span><span class="sxs-lookup"><span data-stu-id="58853-119">However, the policy is not enforced.</span></span> <span data-ttu-id="58853-120">若為自訂地區設定，您的應用程式可以使用特定的地區設定，而不是使用中性地區設定做為回復。</span><span class="sxs-lookup"><span data-stu-id="58853-120">For a custom locale, your application can use a specific locale instead of a neutral locale as a fallback.</span></span>

> [!Note]  
> <span data-ttu-id="58853-121">[呼叫「地區設定名稱](calling-the--locale-name--functions.md)」函式中所述的任何函式都不接受中性地區設定做為輸入。</span><span class="sxs-lookup"><span data-stu-id="58853-121">None of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs.</span></span> <span data-ttu-id="58853-122">因此，地區設定 \_ SCONSOLEFALLBACKNAME 資料的使用非常有限。</span><span class="sxs-lookup"><span data-stu-id="58853-122">Thus LOCALE\_SCONSOLEFALLBACKNAME data is of very limited use.</span></span> <span data-ttu-id="58853-123">尤其是， [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 都不接受中性地區設定做為輸入。</span><span class="sxs-lookup"><span data-stu-id="58853-123">In particular, neither [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) nor [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) accepts neutral locales as inputs.</span></span>

 

 

 



