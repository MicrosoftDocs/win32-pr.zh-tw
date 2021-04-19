---
description: 詞彙 &\# 0034; language&\# 0034; 表示在讀出和寫入通訊中使用的屬性集合。
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: 地區設定和語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973899"
---
# <a name="locales-and-languages"></a><span data-ttu-id="15356-103">地區設定和語言</span><span class="sxs-lookup"><span data-stu-id="15356-103">Locales and Languages</span></span>

<span data-ttu-id="15356-104">「語言」一詞表示在讀出和寫入通訊中所使用的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="15356-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="15356-105">每種語言都有語言名稱和語言識別項，表示特定 [字碼頁](code-pages.md) (ANSI、DOS、Macintosh) 用來代表作業系統上語言的 [地理位置](table-of-geographical-locations.md) 。</span><span class="sxs-lookup"><span data-stu-id="15356-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="15356-106">中性語言會以名稱（例如 "en" 代表英文）表示。</span><span class="sxs-lookup"><span data-stu-id="15356-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="15356-107">有更多地理位置的特定語言可透過包含地區設定和國家/地區資訊的名稱來表示。</span><span class="sxs-lookup"><span data-stu-id="15356-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="15356-108">例如，地區設定英文 (美國) 的語言名稱為 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="15356-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="15356-109">「地區設定」是以值清單表示的語言相關使用者喜好設定資訊的集合。</span><span class="sxs-lookup"><span data-stu-id="15356-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="15356-110">Windows XP 支援150以上的地區設定，而 Windows Vista 支援大約200。</span><span class="sxs-lookup"><span data-stu-id="15356-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="15356-111">每個地區設定都是由語言和排序次序所定義，而且具有地區設定名稱和地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="15356-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="15356-112">德文 (德國) 的地區設定名稱範例是「de de \_ 電話簿」。</span><span class="sxs-lookup"><span data-stu-id="15356-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="15356-113">每個作業系統都至少有一個已安裝的地區設定，而且通常會有許多可供使用者選取的地區設定。</span><span class="sxs-lookup"><span data-stu-id="15356-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="15356-114">除了名稱和識別碼之外，每個地區設定都有與其相關聯的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="15356-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="15356-115">地區設定資訊 [常數](locale-information-constants.md)中會說明地區設定資訊類型。</span><span class="sxs-lookup"><span data-stu-id="15356-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="15356-116">作業系統會將地區設定指派給每個執行緒，一開始會指派 [地區設定 \_ 系統 \_ 預設值](locale-system-default.md)所定義的「系統預設地區設定」。</span><span class="sxs-lookup"><span data-stu-id="15356-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="15356-117">當安裝作業系統時，或當使用者使用主控台的 [地區及語言選項] 部分進行選取時，就會設定此地區設定。</span><span class="sxs-lookup"><span data-stu-id="15356-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="15356-118">在屬於使用者的進程中執行執行緒時，作業系統會將「使用者預設地區設定」指派給執行緒。</span><span class="sxs-lookup"><span data-stu-id="15356-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="15356-119">此地區設定是由 [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)所定義。</span><span class="sxs-lookup"><span data-stu-id="15356-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="15356-120">應用程式可以使用 [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) 函式來明確設定執行緒的地區設定，以覆寫其中一個預設值。</span><span class="sxs-lookup"><span data-stu-id="15356-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="15356-121">語言的執行需要對應的地區設定。</span><span class="sxs-lookup"><span data-stu-id="15356-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="15356-122">作業系統會藉由選取與特定語言版本相關聯之地區設定的資料（通常是最廣泛的地區設定），來實行中性語言。</span><span class="sxs-lookup"><span data-stu-id="15356-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="15356-123">從 Windows Vista 開始，特定語言有可能對應至補充地區設定，這是一種自訂地區設定。</span><span class="sxs-lookup"><span data-stu-id="15356-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="15356-124">因為補充地區設定全都共用單一地區設定識別碼，所以您的應用程式應該依名稱（而非依識別碼）來處理這些地區設定和對應的語言。</span><span class="sxs-lookup"><span data-stu-id="15356-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="15356-125">語言概念與地區設定概念密切相關，但這兩個詞彙不可互換。</span><span class="sxs-lookup"><span data-stu-id="15356-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="15356-126">一般來說，與 [多語系消費者介面](multilingual-user-interface.md) 相關的函式會處理語言，而 NLS 函式則是以地區設定為依據。</span><span class="sxs-lookup"><span data-stu-id="15356-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="15356-127">這一節涵蓋下列主題：</span><span class="sxs-lookup"><span data-stu-id="15356-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="15356-128">自訂地區設定</span><span class="sxs-lookup"><span data-stu-id="15356-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="15356-129">語言識別碼</span><span class="sxs-lookup"><span data-stu-id="15356-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="15356-130">語言名稱</span><span class="sxs-lookup"><span data-stu-id="15356-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="15356-131">地區設定識別碼</span><span class="sxs-lookup"><span data-stu-id="15356-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="15356-132">地區設定名稱</span><span class="sxs-lookup"><span data-stu-id="15356-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="15356-133">虛擬地區設定</span><span class="sxs-lookup"><span data-stu-id="15356-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="15356-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="15356-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15356-135">關於國家語言支援</span><span class="sxs-lookup"><span data-stu-id="15356-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="15356-136">字碼頁</span><span class="sxs-lookup"><span data-stu-id="15356-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="15356-137">地區設定資訊常數</span><span class="sxs-lookup"><span data-stu-id="15356-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="15356-138">多語系使用者介面</span><span class="sxs-lookup"><span data-stu-id="15356-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="15356-139">地理位置資料表</span><span class="sxs-lookup"><span data-stu-id="15356-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="15356-140">消費者介面語言管理</span><span class="sxs-lookup"><span data-stu-id="15356-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="15356-141">**SetThreadLocale**</span><span class="sxs-lookup"><span data-stu-id="15356-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



