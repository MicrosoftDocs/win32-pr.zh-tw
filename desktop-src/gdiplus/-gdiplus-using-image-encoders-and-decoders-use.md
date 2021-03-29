---
description: Windows GDI + 提供 Image 類別和 Bitmap 類別，可將影像儲存在記憶體中，並在記憶體中處理影像。
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: 使用影像編碼器和解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112936"
---
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="af0be-103">使用影像編碼器和解碼器</span><span class="sxs-lookup"><span data-stu-id="af0be-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="af0be-104">Windows GDI + 提供 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 類別和 [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 類別，可將影像儲存在記憶體中，並在記憶體中處理影像。</span><span class="sxs-lookup"><span data-stu-id="af0be-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="af0be-105">GDI + 會將影像以映射編碼器的協助寫入磁片檔案，並從磁片檔案載入映射，並提供映射解碼器的協助。</span><span class="sxs-lookup"><span data-stu-id="af0be-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="af0be-106">編碼器會將 **影像** 或 **點陣圖** 物件中的資料轉譯為指定的磁片檔案格式。</span><span class="sxs-lookup"><span data-stu-id="af0be-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="af0be-107">解碼器會將磁片檔中的資料轉譯成 **影像** 和 **點陣圖** 物件所需的格式。</span><span class="sxs-lookup"><span data-stu-id="af0be-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="af0be-108">GDI + 擁有內建的編碼器和支援下列檔案類型的解碼器：</span><span class="sxs-lookup"><span data-stu-id="af0be-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="af0be-109">BMP</span><span class="sxs-lookup"><span data-stu-id="af0be-109">BMP</span></span>
-   <span data-ttu-id="af0be-110">GIF</span><span class="sxs-lookup"><span data-stu-id="af0be-110">GIF</span></span>
-   <span data-ttu-id="af0be-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="af0be-111">JPEG</span></span>
-   <span data-ttu-id="af0be-112">PNG</span><span class="sxs-lookup"><span data-stu-id="af0be-112">PNG</span></span>
-   <span data-ttu-id="af0be-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="af0be-113">TIFF</span></span>

<span data-ttu-id="af0be-114">GDI + 也有內建的支援下列檔案類型的解碼器：</span><span class="sxs-lookup"><span data-stu-id="af0be-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="af0be-115">WMF</span><span class="sxs-lookup"><span data-stu-id="af0be-115">WMF</span></span>
-   <span data-ttu-id="af0be-116">EMF</span><span class="sxs-lookup"><span data-stu-id="af0be-116">EMF</span></span>
-   <span data-ttu-id="af0be-117">圖示</span><span class="sxs-lookup"><span data-stu-id="af0be-117">ICON</span></span>

<span data-ttu-id="af0be-118">下列主題會更詳細地討論編碼器和解碼器：</span><span class="sxs-lookup"><span data-stu-id="af0be-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="af0be-119">列出已安裝的編碼器</span><span class="sxs-lookup"><span data-stu-id="af0be-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="af0be-120">列出已安裝的解碼器</span><span class="sxs-lookup"><span data-stu-id="af0be-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="af0be-121">正在抓取編碼器的類別識別碼</span><span class="sxs-lookup"><span data-stu-id="af0be-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="af0be-122">判斷編碼器所支援的參數</span><span class="sxs-lookup"><span data-stu-id="af0be-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="af0be-123">將 BMP 影像轉換為 PNG 影像</span><span class="sxs-lookup"><span data-stu-id="af0be-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="af0be-124">設定 JPEG 壓縮等級</span><span class="sxs-lookup"><span data-stu-id="af0be-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="af0be-125">轉換 JPEG 影像而不遺失資訊</span><span class="sxs-lookup"><span data-stu-id="af0be-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="af0be-126">建立和儲存多框架影像</span><span class="sxs-lookup"><span data-stu-id="af0be-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="af0be-127">從 Multiple-Frame 影像複製個別的框架</span><span class="sxs-lookup"><span data-stu-id="af0be-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



