---
description: 本主題說明 Windows 檔案總管中稱為內容視圖的新視圖，它會顯示每個專案最相關的內容。
title: 依檔案類型或種類的內容視圖
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693548"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="41ef4-103">依檔案類型或種類的內容視圖</span><span class="sxs-lookup"><span data-stu-id="41ef4-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="41ef4-104">本主題說明 Windows 檔案總管中稱為內容視圖的新視圖，它會顯示每個專案最相關的內容。</span><span class="sxs-lookup"><span data-stu-id="41ef4-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="41ef4-105">專案可以使用一組登錄機碼來定義屬性清單，以及 Shell 用於內容視圖的版面配置。</span><span class="sxs-lookup"><span data-stu-id="41ef4-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="41ef4-106">Shell 會使用專案的 [關聯陣列](fa-perceivedtypes.md)來抓取登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="41ef4-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="41ef4-107">內容視圖的運作方式為何？</span><span class="sxs-lookup"><span data-stu-id="41ef4-107">How Does the Content View Work?</span></span>

<span data-ttu-id="41ef4-108">在 Windows 7 和更新版本中，內容視圖會使用調整大小邏輯，以在視窗大小減少時卸載屬性，以確保最重要的屬性仍然具有可清楚讀取的空間。</span><span class="sxs-lookup"><span data-stu-id="41ef4-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="41ef4-109">下列螢幕擷取畫面說明包含音樂、圖片和檔的搜尋結果內容視圖。</span><span class="sxs-lookup"><span data-stu-id="41ef4-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![包含音樂、圖片和檔的搜尋結果內容視圖](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="41ef4-111">某些 Shell 資料來源預設會使用內容視圖，但使用者可以按一下 [Windows 檔案總管] 中的 [ **View Control** ] 按鈕，以選取內容視圖。</span><span class="sxs-lookup"><span data-stu-id="41ef4-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="41ef4-112">Shell 資料來源會擴充 Shell 命名空間，並公開資料存放區中的專案。</span><span class="sxs-lookup"><span data-stu-id="41ef4-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="41ef4-113">您可以使用通訊協定處理常式，利用 Windows Search 系統為數據存放區中的專案編制索引。</span><span class="sxs-lookup"><span data-stu-id="41ef4-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="41ef4-114">如何執行內容視圖</span><span class="sxs-lookup"><span data-stu-id="41ef4-114">How to Implement the Content View</span></span>

<span data-ttu-id="41ef4-115">註冊新的 [檔案類型](fa-file-types.md) 或 [通訊協定處理常式](../search/-search-3x-wds-extidx-prot-implementing.md)時，您可以使用兩種不同方法的其中一種來利用內容視圖。</span><span class="sxs-lookup"><span data-stu-id="41ef4-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="41ef4-116">您可以使用現有的屬性集和版面配置模式，也可以建立自己的組合。</span><span class="sxs-lookup"><span data-stu-id="41ef4-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="41ef4-117">您可以使用登錄專案，將您的檔案類型或專案與預先定義的 [種類](../properties/building-property-handlers-user-friendly-kind-names.md)產生關聯，這是您可以將它視為內容類別別的屬性。</span><span class="sxs-lookup"><span data-stu-id="41ef4-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="41ef4-118">藉由將您的檔案類型或專案與這些種類的某些專案產生關聯，您就可以自動繼承該種類的內容視圖配置模式和屬性清單。</span><span class="sxs-lookup"><span data-stu-id="41ef4-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="41ef4-119">Windows 會定義下列種類的內容視圖配置模式和屬性清單：檔、電子郵件、資料夾、音樂、圖片和一般。</span><span class="sxs-lookup"><span data-stu-id="41ef4-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="41ef4-120">建議您這樣的關聯類型。</span><span class="sxs-lookup"><span data-stu-id="41ef4-120">This type of association is encouraged.</span></span> <span data-ttu-id="41ef4-121">它可讓您提供使用者預期類似專案的一致體驗。</span><span class="sxs-lookup"><span data-stu-id="41ef4-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="41ef4-122">如需詳細資訊，請參閱 [檔](fa-file-types.md) 類型和 [種類名稱](../properties/building-property-handlers-user-friendly-kind-names.md) ，以及 [如何針對檔案類型或專案註冊屬性的唯一內容集和配置模式](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md)。</span><span class="sxs-lookup"><span data-stu-id="41ef4-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41ef4-123">其他資源</span><span class="sxs-lookup"><span data-stu-id="41ef4-123">Additional Resources</span></span>

-   <span data-ttu-id="41ef4-124">如需屬性參考 [檔，請參閱 system.string](../properties/props-system-kind.md)和 [system. KindText](../properties/props-system-kindtext.md)。</span><span class="sxs-lookup"><span data-stu-id="41ef4-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="41ef4-125">如需 PropList 參考檔，請參閱 [PropList. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)和 [PropList. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md)。</span><span class="sxs-lookup"><span data-stu-id="41ef4-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41ef4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="41ef4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ef4-127">應用程式註冊</span><span class="sxs-lookup"><span data-stu-id="41ef4-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="41ef4-128">檔案類型</span><span class="sxs-lookup"><span data-stu-id="41ef4-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="41ef4-129">檔案關聯的運作方式</span><span class="sxs-lookup"><span data-stu-id="41ef4-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="41ef4-130">檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="41ef4-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="41ef4-131">檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="41ef4-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="41ef4-132">程式設計識別碼</span><span class="sxs-lookup"><span data-stu-id="41ef4-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="41ef4-133">認知類型</span><span class="sxs-lookup"><span data-stu-id="41ef4-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="41ef4-134">關聯陣列</span><span class="sxs-lookup"><span data-stu-id="41ef4-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
