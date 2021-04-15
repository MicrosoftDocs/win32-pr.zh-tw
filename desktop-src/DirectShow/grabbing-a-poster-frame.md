---
description: 抓取海報框架
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: 抓取海報框架
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467935"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="dfdbf-103">抓取海報框架</span><span class="sxs-lookup"><span data-stu-id="dfdbf-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="dfdbf-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="dfdbf-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dfdbf-105">本文說明如何使用由[DirectShow 編輯服務](directshow-editing-services.md)提供的媒體偵測器[ (MediaDet) ](media-detector--mediadet.md)物件，顯示數位媒體檔案中的海報框架。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="dfdbf-106">媒體偵測器是協助程式物件，可從媒體來源檔案取得格式資訊。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="dfdbf-107">它也可以從來源檔案中的影片資料流程抓取點陣圖影像。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="dfdbf-108">假設檔案是可搜尋的，您可以從檔案中的任何時間點取得映射。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="dfdbf-109">傳回的影像一律採用24位 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="dfdbf-110">媒體偵測器不是篩選準則，而且應用程式不需要使用篩選圖形管理員或建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="dfdbf-111">就內部而言，媒體偵測器會建立包含 [**範例捕獲篩選器**](sample-grabber-filter.md)的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="dfdbf-112">為了取得點陣圖，媒體偵測器會搜尋並暫停篩選圖形，然後從範例捕獲篩選器抓取點陣圖。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="dfdbf-113">應用程式會透過 [**IMediaDet**](imediadet.md) 介面與媒體偵測器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="dfdbf-114">媒體偵測器是在協助程式物件內封裝篩選圖形的絕佳範例，以便保護應用程式不受圖形相關的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="dfdbf-115">媒體偵測器會以兩種模式運作。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="dfdbf-116">當您第一次建立時，媒體偵測器會處於「資訊收集」模式。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="dfdbf-117">您可以指定媒體檔案的名稱，並取得檔案中每個資料流程的相關資訊，例如格式類型、畫面播放速率或持續時間。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="dfdbf-118">如果檔案包含影片串流，您可以將媒體偵測器切換為「點陣圖抓取」模式，並從來源取出點陣圖。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="dfdbf-119">不過，一旦您這麼做，就無法將媒體偵測器切換回其原始模式;它會永久連接到該影片串流。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="dfdbf-120">若要使用另一個資料流程或另一個檔案，您必須建立媒體偵測器的新實例。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="dfdbf-121">本教學課程中的程式碼範例會使用 ATL **CComPtr** 類別，此類別會自動管理參考計數。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="dfdbf-122">如果您想要使用原始介面指標，請記得在完成時釋放每個介面。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="dfdbf-123">此外，為了簡潔起見，程式碼範例會省略應用程式應該執行的大部分錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="dfdbf-124">在工作程式碼中，一律檢查 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dfdbf-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="dfdbf-125">本教學課程包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="dfdbf-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="dfdbf-126">步驟1：建立 Windows Framework</span><span class="sxs-lookup"><span data-stu-id="dfdbf-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="dfdbf-127">步驟2：新增功能表命令以抓取海報畫面</span><span class="sxs-lookup"><span data-stu-id="dfdbf-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="dfdbf-128">步驟3：執行 Frame-Grabbing 函式</span><span class="sxs-lookup"><span data-stu-id="dfdbf-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="dfdbf-129">步驟4：在工作區上繪製點陣圖</span><span class="sxs-lookup"><span data-stu-id="dfdbf-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="dfdbf-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="dfdbf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfdbf-131">使用 DirectShow 編輯服務</span><span class="sxs-lookup"><span data-stu-id="dfdbf-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



