---
description: 使用永久性地區設定資料
ms.assetid: f62402d6-31de-4ff7-9538-7925a007a089
title: 使用永久性地區設定資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4fe4990da53e4db9f71b2feffbd9eb40aedee9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852960"
---
# <a name="using-persistent-locale-data"></a><span data-ttu-id="4f6f9-103">使用永久性地區設定資料</span><span class="sxs-lookup"><span data-stu-id="4f6f9-103">Using Persistent Locale Data</span></span>

<span data-ttu-id="4f6f9-104">全球化應用程式通常會保存或傳輸資料，例如，時間和日期。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-104">A globalized application often persists or transmits data, for example, time and date.</span></span> <span data-ttu-id="4f6f9-105">當您決定應用程式應該如何處理資料持續性時，請記住，從電腦到電腦或應用程式執行之間的資料並不一定相同。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-105">When deciding how your application should handle data persistence, remember that data is not guaranteed to be the same from computer to computer or between runs of the application.</span></span> <span data-ttu-id="4f6f9-106">這適用于隨附于 Windows 和[自訂地區](custom-locales.md)設定的兩種[地區](locales-and-languages.md)設定。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-106">This is true for both [locales](locales-and-languages.md) that ship with Windows and [custom locales](custom-locales.md).</span></span>

<span data-ttu-id="4f6f9-107">應用程式的設計必須考慮各種可能發生的地區設定相關資料變更。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-107">Design of the application must take into account a variety of locale-related data changes that can occur.</span></span> <span data-ttu-id="4f6f9-108">例如：</span><span class="sxs-lookup"><span data-stu-id="4f6f9-108">For example:</span></span>

-   <span data-ttu-id="4f6f9-109">貨幣符號可以隨著國家採用歐元而變更。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-109">Currency symbols can change as countries adopt the Euro.</span></span>
-   <span data-ttu-id="4f6f9-110">區域喜好設定可以變更。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-110">Regional preferences can change.</span></span> <span data-ttu-id="4f6f9-111">例如，d/m/y 格式可能會變更為特定地區設定的 m/d/y 格式。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-111">For example, the format d/m/y might change to the format m/d/y for a particular locale.</span></span>
-   <span data-ttu-id="4f6f9-112">由於拼寫 reforms，可能會變更日名稱的拼寫。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-112">The spelling of day names can change due to spelling reforms.</span></span> <span data-ttu-id="4f6f9-113">此外，也可以變更月份或日期名稱的大小寫。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-113">Additionally, casing can change for month or day names.</span></span>

## <a name="use-locale-independent-formats-for-storage-and-data-interchange"></a><span data-ttu-id="4f6f9-114">使用 Locale-Independent 格式進行儲存體和資料交換</span><span class="sxs-lookup"><span data-stu-id="4f6f9-114">Use Locale-Independent Formats for Storage and Data Interchange</span></span>

<span data-ttu-id="4f6f9-115">保存資料的應用程式應該使用與地區設定無關的儲存和資料交換格式。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-115">An application that persists data should use locale-independent formats for storage and data interchange.</span></span> <span data-ttu-id="4f6f9-116">範例有硬式編碼或標準格式;非變異地區設定的 [地區設定 \_ 名稱不 \_ 變](locale-name-constants.md); 以及二進位儲存格式。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-116">Examples are hard-coded or standard formats; the invariant locale [LOCALE\_NAME\_INVARIANT](locale-name-constants.md); and binary storage formats.</span></span>

<span data-ttu-id="4f6f9-117">如果需要持續性排序資料，應用程式必須使用 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) 函數。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-117">If persistent sorting data is required, the application must use the [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) function.</span></span> <span data-ttu-id="4f6f9-118">請記住，不變的格式不會針對地區設定和行事歷數據進行 [排序](sorting.md)，因此不會維持不變。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-118">Remember that an invariant format does not remain invariant for [sorting](sorting.md), only for locale and calendar data.</span></span>

## <a name="use-the-user-default-locale-for-data-presentation"></a><span data-ttu-id="4f6f9-119">使用資料呈現的使用者預設地區設定</span><span class="sxs-lookup"><span data-stu-id="4f6f9-119">Use the User Default Locale for Data Presentation</span></span>

<span data-ttu-id="4f6f9-120">若要呈現持續性資料，最適合讓應用程式使用使用者預設地區設定來重新格式化資料。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-120">To present persistent data, it is best for the application to reformat the data using the user default locale.</span></span> <span data-ttu-id="4f6f9-121">使用此地區設定可允許使用者覆寫。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-121">Use of this locale allows user overrides.</span></span> <span data-ttu-id="4f6f9-122">如需詳細資訊，請參閱 [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)。</span><span class="sxs-lookup"><span data-stu-id="4f6f9-122">For more information, see [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f6f9-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f6f9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f6f9-124">使用國家語言支援</span><span class="sxs-lookup"><span data-stu-id="4f6f9-124">Using National Language Support</span></span>](using-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="4f6f9-125">自訂地區設定</span><span class="sxs-lookup"><span data-stu-id="4f6f9-125">Custom Locales</span></span>](custom-locales.md)
</dt> <dt>

[<span data-ttu-id="4f6f9-126">排序</span><span class="sxs-lookup"><span data-stu-id="4f6f9-126">Sorting</span></span>](sorting.md)
</dt> </dl>

 

 



