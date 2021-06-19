---
description: 瞭解如何使用影像、點陣圖和中繼檔。 Windows GDI + 提供的影像類別可使用 (點陣圖) 和向量影像 (中繼檔) 。
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: 使用影像、點陣圖和中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395533"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="58136-104">使用影像、點陣圖和中繼檔</span><span class="sxs-lookup"><span data-stu-id="58136-104">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="58136-105">Windows GDI + 提供的 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 類別可使用 (點陣圖) 和向量影像 (中繼檔) 。</span><span class="sxs-lookup"><span data-stu-id="58136-105">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="58136-106">[**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)類別和 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)類別都是繼承自 **Image** 類別。</span><span class="sxs-lookup"><span data-stu-id="58136-106">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="58136-107">**Bitmap** 類別藉由提供載入、儲存和操作點陣影像的其他方法，來擴充 **Image** 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="58136-107">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="58136-108">**中繼檔** 類別藉由提供記錄和檢查向量影像的其他方法，來擴充 **Image** 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="58136-108">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="58136-109">下列主題會更詳細地討論 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)、 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)和 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別：</span><span class="sxs-lookup"><span data-stu-id="58136-109">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="58136-110">載入和顯示點陣圖</span><span class="sxs-lookup"><span data-stu-id="58136-110">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="58136-111">載入和顯示中繼檔</span><span class="sxs-lookup"><span data-stu-id="58136-111">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="58136-112">錄製中繼檔</span><span class="sxs-lookup"><span data-stu-id="58136-112">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="58136-113">裁剪和縮放影像</span><span class="sxs-lookup"><span data-stu-id="58136-113">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="58136-114">旋轉、反映及扭曲影像</span><span class="sxs-lookup"><span data-stu-id="58136-114">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="58136-115">在縮放期間使用插補模式控制影像品質</span><span class="sxs-lookup"><span data-stu-id="58136-115">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="58136-116">建立縮圖影像</span><span class="sxs-lookup"><span data-stu-id="58136-116">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="58136-117">使用快取點陣圖改善效能</span><span class="sxs-lookup"><span data-stu-id="58136-117">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="58136-118">藉由避免自動調整來改善效能</span><span class="sxs-lookup"><span data-stu-id="58136-118">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="58136-119">讀取和寫入中繼資料</span><span class="sxs-lookup"><span data-stu-id="58136-119">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



