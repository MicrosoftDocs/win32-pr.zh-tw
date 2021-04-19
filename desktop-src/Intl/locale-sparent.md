---
description: 地區設定 \_ SPARENT
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35a774c6a7f8eea631a2d6579b97058b30acdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975226"
---
# <a name="locale_sparent"></a><span data-ttu-id="e634f-103">地區設定 \_ SPARENT</span><span class="sxs-lookup"><span data-stu-id="e634f-103">LOCALE\_SPARENT</span></span>

<span data-ttu-id="e634f-104">**Windows Vista 和更新版本：** 資源載入器所使用的備用地區設定。</span><span class="sxs-lookup"><span data-stu-id="e634f-104">**Windows Vista and later:** Fallback locale, used by the resource loader.</span></span> <span data-ttu-id="e634f-105">此字串允許的最大字元數為85，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="e634f-105">The maximum number of characters allowed for this string is 85, including a terminating null character.</span></span>

<span data-ttu-id="e634f-106">地區設定具有特定地區設定的父系為中性地區設定的階層。</span><span class="sxs-lookup"><span data-stu-id="e634f-106">Locales have a hierarchy in which the parent of a specific locale is a neutral locale.</span></span> <span data-ttu-id="e634f-107">特定地區設定會與語言和國家/地區相關聯，而中性地區設定會與語言相關聯，但不會與任何國家/地區相關聯。</span><span class="sxs-lookup"><span data-stu-id="e634f-107">A specific locale is associated with both a language and a country/region, while a neutral locale is associated with a language but is not associated with any country/region.</span></span> <span data-ttu-id="e634f-108">當特定地區設定的資源無法使用時，會使用父地區設定來決定要嘗試的第一個回復。</span><span class="sxs-lookup"><span data-stu-id="e634f-108">The parent locale is used to decide the first fallback to be tried when a resource for a specific locale is not available.</span></span> <span data-ttu-id="e634f-109">例如，"en-us" (0x0409) 的父地區設定為 "en" (0x0009) 。</span><span class="sxs-lookup"><span data-stu-id="e634f-109">For example, the parent locale for "en-US" (0x0409) is "en" (0x0009).</span></span> <span data-ttu-id="e634f-110">當資源無法用於特定的 "en-us" 地區設定時，資源載入器會切換回使用可用於中性 "en" 地區設定的資源。</span><span class="sxs-lookup"><span data-stu-id="e634f-110">When a resource is not available for the specific "en-US" locale, the resource loader falls back to use the resource that is available for the neutral "en" locale.</span></span> <span data-ttu-id="e634f-111">如需資源載入器回溯策略的進一步詳細資料，請參閱 [消費者介面語言管理](user-interface-language-management.md) 。</span><span class="sxs-lookup"><span data-stu-id="e634f-111">See [User Interface Language Management](user-interface-language-management.md) for further details of the resource loader fallback strategy.</span></span>

<span data-ttu-id="e634f-112">這個模式在預先定義的地區設定中是一致的。</span><span class="sxs-lookup"><span data-stu-id="e634f-112">This pattern is consistent for predefined locales.</span></span> <span data-ttu-id="e634f-113">不過，父地區設定並不是由地區設定名稱的任何操作所決定。</span><span class="sxs-lookup"><span data-stu-id="e634f-113">However, the parent locale is not determined by any manipulation of the locale name.</span></span> <span data-ttu-id="e634f-114">也就是說， [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 不會剖析字串（例如 "en-us"）以取得值 "en"。</span><span class="sxs-lookup"><span data-stu-id="e634f-114">That is, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) and [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) do not parse a string such as "en-US" to get the value "en".</span></span> <span data-ttu-id="e634f-115">相反地，他們會查看儲存的地區設定資料。</span><span class="sxs-lookup"><span data-stu-id="e634f-115">Instead, they look at the stored locale data.</span></span> <span data-ttu-id="e634f-116">針對預先定義的地區設定，此值會遵循預期的模式，在此模式中，特定地區設定的父系是對應的中性地區設定，而中性地區設定的父系是不變的地區設定。</span><span class="sxs-lookup"><span data-stu-id="e634f-116">For predefined locales, the value follows the expected pattern, in which the parent of a specific locale is the corresponding neutral locale and the parent of a neutral locale is the invariant locale.</span></span> <span data-ttu-id="e634f-117">雖然建議自訂地區設定遵循類似的策略來定義其父地區設定，但這並不會強制執行。</span><span class="sxs-lookup"><span data-stu-id="e634f-117">While it is recommended that custom locales follow a similar strategy in terms of defining their parent locale, this is not enforced.</span></span> <span data-ttu-id="e634f-118">執行自訂地區設定的應用程式可以指定較不明顯的適當父系。</span><span class="sxs-lookup"><span data-stu-id="e634f-118">The application implementing a custom locale can specify a less obviously appropriate parent.</span></span>

> [!Note]  
> <span data-ttu-id="e634f-119">由於 [呼叫「地區設定名稱](calling-the--locale-name--functions.md) 」函式中所述的任何函式都不接受中性地區設定做為輸入，因此此地區設定 \_ SPARENT 資料的用途有限。</span><span class="sxs-lookup"><span data-stu-id="e634f-119">Since none of the functions described in [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md) accept neutral locales as inputs, this LOCALE\_SPARENT data is of very limited use.</span></span> <span data-ttu-id="e634f-120">尤其是， [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 都不接受中性地區設定做為輸入。</span><span class="sxs-lookup"><span data-stu-id="e634f-120">In particular, neither [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) nor [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) accepts neutral locales as inputs.</span></span>

 

 

 



