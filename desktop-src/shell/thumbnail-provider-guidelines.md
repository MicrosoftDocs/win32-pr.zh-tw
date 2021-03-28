---
description: 當您提供縮圖時，應遵循下列指導方針。
title: 縮圖處理常式指導方針
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: 9763c9cb859df3530766b6e65f9dce4f7de87fd2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/11/2020
ms.locfileid: "104093539"
---
# <a name="thumbnail-handler-guidelines"></a><span data-ttu-id="76010-103">縮圖處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="76010-103">Thumbnail Handler Guidelines</span></span>

<span data-ttu-id="76010-104">當您提供縮圖時，應遵循下列指導方針。</span><span class="sxs-lookup"><span data-stu-id="76010-104">When you provide a thumbnail, the following guidelines should be followed.</span></span>

-   <span data-ttu-id="76010-105">提供可在32位色彩中以256x256 圖元解析度顯示的縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-105">Provide thumbnails that display well at a resolution of 256x256 pixels in 32-bit color.</span></span> <span data-ttu-id="76010-106">如果沒有已註冊的預覽處理常式，Windows Vista 讀取窗格會使用此大小的縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-106">A thumbnail of this size is be used by the Windows Vista reading pane in the absence of a registered preview handler.</span></span> <span data-ttu-id="76010-107">不過，預覽處理常式是慣用的選項，應盡可能提供。</span><span class="sxs-lookup"><span data-stu-id="76010-107">However, a preview handler is the preferred option and should be provided whenever possible.</span></span>
-   <span data-ttu-id="76010-108">當您建立多個不同大小的影像時，請裁剪頁面、框架或影像，不要從較大的影像建立較大的影像。</span><span class="sxs-lookup"><span data-stu-id="76010-108">When you create multiple images of different sizes, do not create the smaller images from the larger by cropping the page, frame, or image.</span></span> <span data-ttu-id="76010-109">縮小整個影像。</span><span class="sxs-lookup"><span data-stu-id="76010-109">Scale down the entire image.</span></span>
-   <span data-ttu-id="76010-110">不要一次顯示多個頁面、框架或影像;只需要使用一個。</span><span class="sxs-lookup"><span data-stu-id="76010-110">Do not show multiple pages, frames, or images at once; just use one.</span></span> <span data-ttu-id="76010-111">如果檔是由數個頁面所組成，例如文字檔或包含數個工作表的試算表，則 [頁首] 頁面通常是最佳選擇，但不論您使用哪一種，都只能使用。</span><span class="sxs-lookup"><span data-stu-id="76010-111">If a document consists of several pages, such as a text document or a spreadsheet that consists of several worksheets, the cover page is often the best choice, but regardless of which you use, only use one.</span></span> <span data-ttu-id="76010-112">請勿匯總不同的頁面，以提供整齊的外觀。</span><span class="sxs-lookup"><span data-stu-id="76010-112">Do not aggregate different pages, which gives a cluttered look.</span></span>
-   <span data-ttu-id="76010-113">Windows Vista 負責相應減少或縮小取樣影像。</span><span class="sxs-lookup"><span data-stu-id="76010-113">Windows Vista is responsible for scaling down or down sampling images.</span></span> <span data-ttu-id="76010-114">如果您的處理常式要求的影像數目超過可用的數量，請提供您最接近的大小。</span><span class="sxs-lookup"><span data-stu-id="76010-114">If your handler is asked for a larger image than you have available, provide the closest size you have.</span></span> <span data-ttu-id="76010-115">請勿嘗試動態調整您自己的影像大小。</span><span class="sxs-lookup"><span data-stu-id="76010-115">Do not attempt to dynamically resize your own image.</span></span>
-   <span data-ttu-id="76010-116">一律會從您的處理常式傳回縮圖影像，而不是執行特殊邏輯來傳回傳統圖示。</span><span class="sxs-lookup"><span data-stu-id="76010-116">Always return a thumbnail image from your handler instead of performing special logic to return traditional icons.</span></span> <span data-ttu-id="76010-117">在特定大小下，Windows Vista 會自動顯示傳統圖示來取代縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-117">Below a certain size, Windows Vista automatically displays a traditional icon in place of the thumbnail.</span></span> <span data-ttu-id="76010-118">如需詳細資訊，請參閱 [縮圖處理常式](thumbnail-providers.md)的 *縮圖快取和大小調整* 區段。</span><span class="sxs-lookup"><span data-stu-id="76010-118">See the *Thumbnail Cache and Sizing* section of [Thumbnail Handlers](thumbnail-providers.md) for more details.</span></span>
-   <span data-ttu-id="76010-119">一律傳回具有頁面、框架或影像外觀比例的縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-119">Always return a thumbnail with the aspect ratio of the page, frame, or image.</span></span> <span data-ttu-id="76010-120">請勿使用 Alpha 來完成正方形。</span><span class="sxs-lookup"><span data-stu-id="76010-120">Do not use alpha to complete a square.</span></span> <span data-ttu-id="76010-121">Windows Vista 負責正確定位非方形的影像。</span><span class="sxs-lookup"><span data-stu-id="76010-121">Windows Vista is responsible for correctly positioning a non-square image.</span></span>
-   <span data-ttu-id="76010-122">請勿將裝飾新增至縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-122">Do not add adornments to your thumbnails.</span></span> <span data-ttu-id="76010-123">Windows Vista 會在適當的情況下自動套用陰影和其他裝飾。</span><span class="sxs-lookup"><span data-stu-id="76010-123">Windows Vista automatically applies drop shadows and other adornments where appropriate.</span></span> <span data-ttu-id="76010-124">它也會針對特定檔案類型（例如圖片或影片）套用特殊裝飾。</span><span class="sxs-lookup"><span data-stu-id="76010-124">It also applies special adornments for specific file types such as pictures or videos.</span></span>
-   <span data-ttu-id="76010-125">請勿覆迭縮圖上的檔案類型或應用程式資訊。</span><span class="sxs-lookup"><span data-stu-id="76010-125">Do not overlay file type or application information on your thumbnail.</span></span> <span data-ttu-id="76010-126">Windows Vista 會在影像的右下角顯示類型重迭。</span><span class="sxs-lookup"><span data-stu-id="76010-126">Windows Vista displays a type overlay for you in the lower right corner of the image.</span></span> <span data-ttu-id="76010-127">這項重迭是以認知型別為基礎，但可以針對個別檔案類型進行設定。</span><span class="sxs-lookup"><span data-stu-id="76010-127">This overlay is based on perceived type but can be set for individual file types.</span></span>
-   <span data-ttu-id="76010-128">為了獲得更好的效能，當您的縮圖是以檔案內容為基礎時（例如檔頁面），儲存預覽影像時儲存預覽影像 (，因此可能會變更) 而不是即時計算。</span><span class="sxs-lookup"><span data-stu-id="76010-128">For better performance, when your thumbnail is based on file content—a page of a document, for example—store the preview image when the file is saved (and therefore probably changed) instead of calculating it in real time.</span></span> <span data-ttu-id="76010-129">如果計算需要海量儲存體 (超過一或兩秒) ，就應該執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="76010-129">This should be done if the calculation is memory-intensive (more than one or two seconds).</span></span> <span data-ttu-id="76010-130">如果未這麼做，則顯示大量檔案的 views （這些檔案的縮圖會由不同的處理常式處理）將需要一些時間才會顯示—這是不良的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="76010-130">If this is not done, views showing a large number of files whose thumbnails are handled by different handlers is going to take some time to display—a bad user experience.</span></span> <span data-ttu-id="76010-131">Windows Vista 會快取縮圖，並參考上次修改時間，以判斷是否應該更新縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-131">Windows Vista caches thumbnails and refers to the last modified time to determine whether a thumbnail should be updated.</span></span>
-   <span data-ttu-id="76010-132">請注意，即使提供者可供使用，Explorer 也可以選擇不顯示縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-132">Be aware that Explorer may choose not to display a thumbnail even if a provider is available.</span></span> <span data-ttu-id="76010-133">例如，已封存至磁帶的檔案將不會重新叫用以取得其縮圖。</span><span class="sxs-lookup"><span data-stu-id="76010-133">For example, a file that has been archived to tape will not be recalled to obtain its thumbnail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76010-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="76010-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76010-135">縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="76010-135">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="76010-136">建立縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="76010-136">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> </dl>

 

 



