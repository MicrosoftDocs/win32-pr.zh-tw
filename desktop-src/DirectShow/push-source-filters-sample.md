---
description: 推送來源篩選範例
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: 推送來源篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509994"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="92007-103">推送來源篩選範例</span><span class="sxs-lookup"><span data-stu-id="92007-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="92007-104">Description</span><span class="sxs-lookup"><span data-stu-id="92007-104">Description</span></span>

<span data-ttu-id="92007-105">此範例包含一組三個來源篩選器，可提供下列來源資料作為影片串流：</span><span class="sxs-lookup"><span data-stu-id="92007-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="92007-106">CPushSourceBitmap：從目前目錄載入的單一點陣圖 () </span><span class="sxs-lookup"><span data-stu-id="92007-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="92007-107">CPushSourceBitmapSet：從目前目錄載入 (點陣圖集合) </span><span class="sxs-lookup"><span data-stu-id="92007-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="92007-108">CPushSourceDesktop：目前桌面映射的複本 (僅限 GDI) </span><span class="sxs-lookup"><span data-stu-id="92007-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="92007-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="92007-109">Usage</span></span>

<span data-ttu-id="92007-110">若要使用篩選，請將它載入至 GraphEdit 並轉譯其輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="92007-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="92007-111">這會連接影片轉譯器 (可能會有色彩空間轉換器篩選) 並可讓您顯示輸出。</span><span class="sxs-lookup"><span data-stu-id="92007-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="92007-112">如果您想要將輸出轉譯成 AVI 檔案，請載入 AVI Mux、載入檔案寫入器篩選器、提供輸出名稱給檔案寫入器，然後轉譯 PushSource 濾波器的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="92007-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="92007-113">您也可以載入和連接影片壓縮機、影片效果等等。</span><span class="sxs-lookup"><span data-stu-id="92007-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="92007-114">Desktop capture 篩選不支援硬體重迭，因此它不會將轉譯的影片捕獲到重迭表面或透過硬體重迭顯示的資料指標。</span><span class="sxs-lookup"><span data-stu-id="92007-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="92007-115">它會使用 GDI 將目前的桌面影像轉換為點陣圖，並以媒體範例形式傳遞至輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="92007-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="92007-116">下載範例</span><span class="sxs-lookup"><span data-stu-id="92007-116">Downloading the Sample</span></span>

<span data-ttu-id="92007-117">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="92007-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="92007-118">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ PushSource。</span><span class="sxs-lookup"><span data-stu-id="92007-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92007-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="92007-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92007-120">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="92007-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



