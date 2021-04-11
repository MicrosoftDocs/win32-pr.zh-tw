---
description: 非同步篩選範例
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: 非同步篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025780"
---
# <a name="async-filter-sample"></a><span data-ttu-id="3415b-103">非同步篩選範例</span><span class="sxs-lookup"><span data-stu-id="3415b-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="3415b-104">Description</span><span class="sxs-lookup"><span data-stu-id="3415b-104">Description</span></span>

<span data-ttu-id="3415b-105">非同步篩選範例是支援漸進式下載的檔案讀取器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3415b-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="3415b-106">此範例篩選準則會執行 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 和 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) 介面。</span><span class="sxs-lookup"><span data-stu-id="3415b-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="3415b-107">它支援 MPEG 檔案，但非 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="3415b-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="3415b-108">使用方式</span><span class="sxs-lookup"><span data-stu-id="3415b-108">Usage</span></span>

<span data-ttu-id="3415b-109">此範例包含示範篩選的小型命令列應用程式 Memfile.exe。</span><span class="sxs-lookup"><span data-stu-id="3415b-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="3415b-110">命令列引數會指定媒體檔案和位元速率（以每秒 kb 數為單位）。</span><span class="sxs-lookup"><span data-stu-id="3415b-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="3415b-111">應用程式會以指定的速率將檔案讀取到記憶體中，然後播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="3415b-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="3415b-112">若要這樣做，它會建立篩選的實例、將篩選準則加入至篩選圖形，然後轉譯篩選的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="3415b-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="3415b-113">在命令列輸入：</span><span class="sxs-lookup"><span data-stu-id="3415b-113">At the command line, type:</span></span>

<span data-ttu-id="3415b-114">**Memfile 檔案名位元速率**</span><span class="sxs-lookup"><span data-stu-id="3415b-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="3415b-115">非同步範例篩選不支援 AVI 檔案，因為它無法連接到 [Avi 分隔](avi-splitter-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="3415b-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="3415b-116">非同步篩選的輸出圖釘會建議 \_ \_ 媒體類型的媒體類型，並 MEDIASUBTYPE Null。</span><span class="sxs-lookup"><span data-stu-id="3415b-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="3415b-117">AVI 分隔器篩選器上的輸入 pin 不接受 MEDIASUBTYPE \_ Null，且不會建議任何類型。</span><span class="sxs-lookup"><span data-stu-id="3415b-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="3415b-118">因此，pin 連接會失敗。</span><span class="sxs-lookup"><span data-stu-id="3415b-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="3415b-119">可以增強非同步篩選，以 \_ 在適當時提供 MEDIASUBTYPE Avi。</span><span class="sxs-lookup"><span data-stu-id="3415b-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="3415b-120">例如，它可以檢查檔案格式，或使用副檔名。</span><span class="sxs-lookup"><span data-stu-id="3415b-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3415b-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="3415b-121">Downloading the Sample</span></span>

<span data-ttu-id="3415b-122">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3415b-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="3415b-123">此範例安裝在下列路徑下： \[ *SDK 根* \] \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 非同步。</span><span class="sxs-lookup"><span data-stu-id="3415b-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3415b-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="3415b-124">Related topics</span></span>



[<span data-ttu-id="3415b-125">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="3415b-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



