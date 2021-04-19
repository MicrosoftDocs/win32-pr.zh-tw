---
title: " (舊版 Windows 環境功能的認知類型) "
description: PerceivedType 是將索引中的專案分類的屬性。
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966903"
---
# <a name="perceived-types-legacy-windows-environment-features"></a><span data-ttu-id="64c39-103"> (舊版 Windows 環境功能的認知類型) </span><span class="sxs-lookup"><span data-stu-id="64c39-103">Perceived Types (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="64c39-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="64c39-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="64c39-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="64c39-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="64c39-106">`PerceivedType` 是在索引中分類專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="64c39-106">`PerceivedType` is a property that classifies an item in the index.</span></span> <span data-ttu-id="64c39-107">此分類與 [Advanced Query 語法](-search-2x-wds-aqsreference.md) 所使用的「種類」分類不同，但同樣可讓使用者精簡其搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="64c39-107">This classification is different from the "kind" classification used by the [Advanced Query Syntax](-search-2x-wds-aqsreference.md) but similarly lets users refine their search results.</span></span> <span data-ttu-id="64c39-108">AQS 種類可讓使用者在 PerceivedType 屬性讓使用者篩選其結果集時，限制其搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="64c39-108">The AQS kind lets users limit their search query while the PerceivedType property lets users filter their result set.</span></span>

## <a name="types"></a><span data-ttu-id="64c39-109">類型</span><span class="sxs-lookup"><span data-stu-id="64c39-109">Types</span></span>

<span data-ttu-id="64c39-110">使用 PerceivedType 屬性來分類您的檔案類型，讓使用者可以依類型篩選其搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="64c39-110">Use the PerceivedType property to classify your file type so that users can filter their search results by type.</span></span> <span data-ttu-id="64c39-111">輸出必須是下列其中一個字串：</span><span class="sxs-lookup"><span data-stu-id="64c39-111">The output must be one of the following strings:</span></span>

-   <span data-ttu-id="64c39-112">連絡人</span><span class="sxs-lookup"><span data-stu-id="64c39-112">contact</span></span>
-   <span data-ttu-id="64c39-113">通訊</span><span class="sxs-lookup"><span data-stu-id="64c39-113">communications</span></span>
-   <span data-ttu-id="64c39-114">通訊/電子郵件</span><span class="sxs-lookup"><span data-stu-id="64c39-114">communications/email</span></span>
-   <span data-ttu-id="64c39-115">通訊/行事曆</span><span class="sxs-lookup"><span data-stu-id="64c39-115">communications/calendar</span></span>
-   <span data-ttu-id="64c39-116">通訊/工作</span><span class="sxs-lookup"><span data-stu-id="64c39-116">communications/task</span></span>
-   <span data-ttu-id="64c39-117">通訊/im</span><span class="sxs-lookup"><span data-stu-id="64c39-117">communications/im</span></span>
-   <span data-ttu-id="64c39-118">文件</span><span class="sxs-lookup"><span data-stu-id="64c39-118">document</span></span>
-   <span data-ttu-id="64c39-119">document/note</span><span class="sxs-lookup"><span data-stu-id="64c39-119">document/note</span></span>
-   <span data-ttu-id="64c39-120">document/text</span><span class="sxs-lookup"><span data-stu-id="64c39-120">document/text</span></span>
-   <span data-ttu-id="64c39-121">檔/試算表</span><span class="sxs-lookup"><span data-stu-id="64c39-121">document/spreadsheet</span></span>
-   <span data-ttu-id="64c39-122">檔/簡報</span><span class="sxs-lookup"><span data-stu-id="64c39-122">document/presentation</span></span>
-   <span data-ttu-id="64c39-123">music</span><span class="sxs-lookup"><span data-stu-id="64c39-123">music</span></span>
-   <span data-ttu-id="64c39-124">images</span><span class="sxs-lookup"><span data-stu-id="64c39-124">images</span></span>
-   <span data-ttu-id="64c39-125">影像/圖片</span><span class="sxs-lookup"><span data-stu-id="64c39-125">images/picture</span></span>
-   <span data-ttu-id="64c39-126">影像/影片</span><span class="sxs-lookup"><span data-stu-id="64c39-126">images/video</span></span>
-   <span data-ttu-id="64c39-127">folder</span><span class="sxs-lookup"><span data-stu-id="64c39-127">folder</span></span>
-   <span data-ttu-id="64c39-128">程式</span><span class="sxs-lookup"><span data-stu-id="64c39-128">program</span></span>

<span data-ttu-id="64c39-129">例如，當您想要為新的圖片檔案類型建立篩選增益集時，您需要在您的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面中執行下列程式：</span><span class="sxs-lookup"><span data-stu-id="64c39-129">For example, when you want to create a filter add-in for a new picture file type, you need to implement the following in your [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface:</span></span>

-   <span data-ttu-id="64c39-130">**GetChunk** 傳回包含下列內容的 FULLPROPSPEC： D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span><span class="sxs-lookup"><span data-stu-id="64c39-130">**GetChunk** to return a FULLPROPSPEC that includes: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType</span></span>
-   <span data-ttu-id="64c39-131">**GetValue** 傳回包含： VT \_ LPWSTR = "images/PICTURE" 的 PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="64c39-131">**GetValue** to return a PROPVARIANT that includes: VT\_LPWSTR = "images/picture"</span></span>

## <a name="related-topics"></a><span data-ttu-id="64c39-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="64c39-132">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64c39-133">**參考**</span><span class="sxs-lookup"><span data-stu-id="64c39-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64c39-134">開發 IFilter 增益集</span><span class="sxs-lookup"><span data-stu-id="64c39-134">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="64c39-135">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="64c39-135">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="64c39-136">進階查詢語法</span><span class="sxs-lookup"><span data-stu-id="64c39-136">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="64c39-137">SchemaTable</span><span class="sxs-lookup"><span data-stu-id="64c39-137">SchemaTable</span></span>](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
