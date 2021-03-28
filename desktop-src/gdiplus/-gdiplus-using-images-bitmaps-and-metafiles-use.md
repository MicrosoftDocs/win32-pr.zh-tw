---
description: Windows GDI + 提供的影像類別可使用 (點陣圖) 和向量影像 (中繼檔) 。
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: 使用影像、點陣圖和中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026588"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="dc812-103">使用影像、點陣圖和中繼檔</span><span class="sxs-lookup"><span data-stu-id="dc812-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="dc812-104">Windows GDI + 提供的 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 類別可使用 (點陣圖) 和向量影像 (中繼檔) 。</span><span class="sxs-lookup"><span data-stu-id="dc812-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="dc812-105">[**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)類別和 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile)類別都是繼承自 **Image** 類別。</span><span class="sxs-lookup"><span data-stu-id="dc812-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="dc812-106">**Bitmap** 類別藉由提供載入、儲存和操作點陣影像的其他方法，來擴充 **Image** 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="dc812-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="dc812-107">**中繼檔** 類別藉由提供記錄和檢查向量影像的其他方法，來擴充 **Image** 類別的功能。</span><span class="sxs-lookup"><span data-stu-id="dc812-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="dc812-108">下列主題會更詳細地討論 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)、 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)和 [**中繼檔**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) 類別：</span><span class="sxs-lookup"><span data-stu-id="dc812-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="dc812-109">載入和顯示點陣圖</span><span class="sxs-lookup"><span data-stu-id="dc812-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="dc812-110">載入和顯示中繼檔</span><span class="sxs-lookup"><span data-stu-id="dc812-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="dc812-111">錄製中繼檔</span><span class="sxs-lookup"><span data-stu-id="dc812-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="dc812-112">裁剪和縮放影像</span><span class="sxs-lookup"><span data-stu-id="dc812-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="dc812-113">旋轉、反映及扭曲影像</span><span class="sxs-lookup"><span data-stu-id="dc812-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="dc812-114">在縮放期間使用插補模式控制影像品質</span><span class="sxs-lookup"><span data-stu-id="dc812-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="dc812-115">建立縮圖影像</span><span class="sxs-lookup"><span data-stu-id="dc812-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="dc812-116">使用快取點陣圖改善效能</span><span class="sxs-lookup"><span data-stu-id="dc812-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="dc812-117">藉由避免自動調整來改善效能</span><span class="sxs-lookup"><span data-stu-id="dc812-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="dc812-118">讀取和寫入中繼資料</span><span class="sxs-lookup"><span data-stu-id="dc812-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



