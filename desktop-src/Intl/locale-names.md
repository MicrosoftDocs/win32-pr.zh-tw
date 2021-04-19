---
description: 地區設定名稱是根據 RFC 4646 (Windows Vista 和更新版本) 的語言標記慣例，並以地區設定 SNAME 來表示 \_ 。
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: 地區設定名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9808db94615cba4416c12995b9c969eaaf5a3fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985671"
---
# <a name="locale-names"></a><span data-ttu-id="f43b1-103">地區設定名稱</span><span class="sxs-lookup"><span data-stu-id="f43b1-103">Locale Names</span></span>

<span data-ttu-id="f43b1-104">[地區](locales-and-languages.md)設定名稱是根據 RFC 4646 (Windows Vista 和更新版本) 的語言標記慣例，並以[地區設定 \_ SNAME](locale-sname.md)來表示。</span><span class="sxs-lookup"><span data-stu-id="f43b1-104">A [locale](locales-and-languages.md) name is based on the language tagging conventions of RFC 4646 (Windows Vista and later), and is represented by [LOCALE\_SNAME](locale-sname.md).</span></span> <span data-ttu-id="f43b1-105">一般而言， `<language>-<REGION>` 會使用此模式。</span><span class="sxs-lookup"><span data-stu-id="f43b1-105">Generally, the pattern `<language>-<REGION>` is used.</span></span> <span data-ttu-id="f43b1-106">在這裡，language 是小寫的 ISO 639 語言代碼。</span><span class="sxs-lookup"><span data-stu-id="f43b1-106">Here, language is a lowercase ISO 639 language code.</span></span> <span data-ttu-id="f43b1-107">如果有的話，會使用 ISO 639-1 中的代碼。</span><span class="sxs-lookup"><span data-stu-id="f43b1-107">The codes from ISO 639-1 are used when available.</span></span> <span data-ttu-id="f43b1-108">否則，會使用 ISO 639-2/T 中的代碼。</span><span class="sxs-lookup"><span data-stu-id="f43b1-108">Otherwise, codes from ISO 639-2/T are used.</span></span> <span data-ttu-id="f43b1-109">區域指定大寫的 ISO 3166-1 國家/地區識別碼。</span><span class="sxs-lookup"><span data-stu-id="f43b1-109">REGION specifies an uppercase ISO 3166-1 country/region identifier.</span></span> <span data-ttu-id="f43b1-110">例如，英文 (美式的地區設定名稱) 為 "en-us"，而迪維 () 馬爾地夫的地區設定名稱是 "dv-MV"。</span><span class="sxs-lookup"><span data-stu-id="f43b1-110">For example, the locale name for English (United States) is "en-US" and the locale name for Divehi (Maldives) is "dv-MV".</span></span>

> [!Note]  
> <span data-ttu-id="f43b1-111">固定的 [地區設定 \_ 名稱 \_ 最大 \_ 長度](locale-name-constants.md) 會提供地區設定名稱的最大長度。</span><span class="sxs-lookup"><span data-stu-id="f43b1-111">The constant [LOCALE\_NAME\_MAX\_LENGTH](locale-name-constants.md) gives the maximum length of a locale name.</span></span> <span data-ttu-id="f43b1-112">它包含結束的 null 字元的空間。</span><span class="sxs-lookup"><span data-stu-id="f43b1-112">It includes space for a terminating null character.</span></span>

 

<span data-ttu-id="f43b1-113">如果地區設定是中性地區設定 (沒有任何區域) ，地區設定 [ \_ SNAME](locale-sname.md) 值會遵循此模式 `<language>` 。</span><span class="sxs-lookup"><span data-stu-id="f43b1-113">If the locale is a neutral locale (no region), the [LOCALE\_SNAME](locale-sname.md) value follows the pattern `<language>`.</span></span> <span data-ttu-id="f43b1-114">如果這是腳本很重要的中性地區設定，則模式為 `<language>-<Script>` 。</span><span class="sxs-lookup"><span data-stu-id="f43b1-114">If it is a neutral locale for which the script is significant, the pattern is `<language>-<Script>`.</span></span>

<span data-ttu-id="f43b1-115">如果您必須使用不同的腳本，從相同語言和區域的另一個地區設定來區分地區設定，則地區設定 \_ SNAME 值會遵循此模式 `<language>-<Script>-<REGION>` ，其中腳本是首字母的 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) 腳本。</span><span class="sxs-lookup"><span data-stu-id="f43b1-115">If a locale must be distinguished from another locale for the same language and region using a different script, the LOCALE\_SNAME value follows the pattern `<language>-<Script>-<REGION>`, where Script is an initial-uppercase [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) script code.</span></span> <span data-ttu-id="f43b1-116">例如， \_ 特定地區設定烏茲別克 (拉丁，烏茲別克) 的地區設定 SNAME 值為 "uz-Latn-uz"。</span><span class="sxs-lookup"><span data-stu-id="f43b1-116">For example, the LOCALE\_SNAME value for the specific locale Uzbek (Latin, Uzbekistan) is "uz-Latn-UZ".</span></span> <span data-ttu-id="f43b1-117">當語言通常只會在一個腳本中寫入時，不會包含腳本元件。</span><span class="sxs-lookup"><span data-stu-id="f43b1-117">The script component is not included in cases where a language is commonly written in only one script.</span></span>

<span data-ttu-id="f43b1-118">地區設定的排序次序會使用 [排序次序識別碼](sort-order-identifiers.md)來指定，例如，排序 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="f43b1-118">Sort orders for locales are designated using [sort order identifiers](sort-order-identifiers.md), for example, SORT\_DEFAULT.</span></span> <span data-ttu-id="f43b1-119">為了區分相同語言和區域的兩個或多個排序次序，地區設定名稱會遵循此模式 `<language>-<REGION>\_<sort order>` 。</span><span class="sxs-lookup"><span data-stu-id="f43b1-119">To distinguish two or more sort orders for the same language and region, the locale name follows the pattern `<language>-<REGION>\_<sort order>`.</span></span> <span data-ttu-id="f43b1-120">如果您必須區分腳本和排序次序，則名稱會遵循模式 `<language>-<Script>-<REGION>\_<sort order>` 。</span><span class="sxs-lookup"><span data-stu-id="f43b1-120">If you must distinguish both script and sort order, the name follows the pattern `<language>-<Script>-<REGION>\_<sort order>`.</span></span> <span data-ttu-id="f43b1-121">預設的排序次序絕對不會明確指定，只會指定替代的排序次序。</span><span class="sxs-lookup"><span data-stu-id="f43b1-121">The default sort order is never explicitly specified, only the alternative sort order.</span></span> <span data-ttu-id="f43b1-122">例如，匈牙利文 () 匈牙利預設值為 [排序] 預設值， \_ 或指定的數位相等排序 [匈牙利文] \_ \_ 預設值為 [hu-hu]。</span><span class="sxs-lookup"><span data-stu-id="f43b1-122">For example, Hungarian (Hungary) with either SORT\_DEFAULT or the numerically equivalent SORT\_HUNGARIAN\_DEFAULT is designated "hu-HU".</span></span> <span data-ttu-id="f43b1-123">使用排序次序排序匈牙利文的匈牙利文 (匈牙利) \_ 匈牙利文 \_ 技術是指定為 "HU-hu \_ technl"。</span><span class="sxs-lookup"><span data-stu-id="f43b1-123">Hungarian (Hungary) with sort order SORT\_HUNGARIAN\_TECHNICAL is designated "hu-HU\_technl".</span></span>

<span data-ttu-id="f43b1-124">若為 [取代地區](custom-locales.md)設定，地區設定名稱必須與要取代之地區設定的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="f43b1-124">For a [replacement locale](custom-locales.md), the locale name must be the same as the name for the locale being replaced.</span></span> <span data-ttu-id="f43b1-125">針對補充地區設定，地區設定名稱應遵循或的模式 `<language>-<REGION>-x-<custom>` `<language>-<Script>-<REGION>-x-<custom>` ，其中 `<custom>` 是補充地區設定特有的英數位元字串。</span><span class="sxs-lookup"><span data-stu-id="f43b1-125">For a supplemental locale, the locale name should follow the pattern of `<language>-<REGION>-x-<custom>` or `<language>-<Script>-<REGION>-x-<custom>`, where `<custom>` is an alphanumeric string specific to the supplemental locale.</span></span> <span data-ttu-id="f43b1-126">例如，稱為 >fabricam.com 的公司專屬的補充地區設定可能稱為「en-us->fabricam.com」。</span><span class="sxs-lookup"><span data-stu-id="f43b1-126">For example, a supplemental locale specific to a company called Fabricam might be called "en-US-x-fabricam".</span></span>

<span data-ttu-id="f43b1-127">應用程式可以使用 [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) 和 [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) 函數來取得目前的地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="f43b1-127">An application can retrieve the current locale names by using the [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) and [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) functions.</span></span> <span data-ttu-id="f43b1-128">雖然每個執行緒都可以使用 [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) 來取得和設定本身的地區設定識別碼，並使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)進行設定，但沒有類似的函數可依名稱取得和設定地區設定。</span><span class="sxs-lookup"><span data-stu-id="f43b1-128">While each thread can retrieve and set its own locale identifier with [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) and set it with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale), there are no analogous functions to get and set locale by name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f43b1-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="f43b1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f43b1-130">地區設定和語言</span><span class="sxs-lookup"><span data-stu-id="f43b1-130">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="f43b1-131">自訂地區設定</span><span class="sxs-lookup"><span data-stu-id="f43b1-131">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="f43b1-132">地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="f43b1-132">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="f43b1-133">排序次序識別碼</span><span class="sxs-lookup"><span data-stu-id="f43b1-133">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> </dl>

 

 



