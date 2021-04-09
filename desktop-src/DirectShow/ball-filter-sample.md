---
description: 球形濾波器範例
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: 球形濾波器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846731"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="c5316-103">球形濾波器範例</span><span class="sxs-lookup"><span data-stu-id="c5316-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="c5316-104">Description</span><span class="sxs-lookup"><span data-stu-id="c5316-104">Description</span></span>

<span data-ttu-id="c5316-105">球形濾波器是一個影片來源篩選器，可產生彈跳球的影像。</span><span class="sxs-lookup"><span data-stu-id="c5316-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="c5316-106">此範例說明格式的協商，以及使用來源篩選基類 [**CSource**](csource.md) 和 [**CSourceStream**](csourcestream.md)。</span><span class="sxs-lookup"><span data-stu-id="c5316-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="c5316-107">Fball 和 Fball 中的程式碼會管理篩選介面。</span><span class="sxs-lookup"><span data-stu-id="c5316-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="c5316-108">這兩個檔案大約包含來源篩選器所需的最少程式碼。</span><span class="sxs-lookup"><span data-stu-id="c5316-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="c5316-109">球形和球 .cpp 檔案包含彈跳球的程式碼。</span><span class="sxs-lookup"><span data-stu-id="c5316-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="c5316-110">此篩選器具有單一輸出圖釘，可提供影片串流，以顯示在框架中跳動的球。</span><span class="sxs-lookup"><span data-stu-id="c5316-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="c5316-111">球濾波器也接受來自下游篩選的品質管制要求，其說明簡單的品質管理原則。</span><span class="sxs-lookup"><span data-stu-id="c5316-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="c5316-112">此篩選準則會針對該目的來實行 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="c5316-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c5316-113">下載範例</span><span class="sxs-lookup"><span data-stu-id="c5316-113">Downloading the Sample</span></span>

<span data-ttu-id="c5316-114">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c5316-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="c5316-115">此範例安裝在下列路徑下： \[ *SDK 根* \] \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 球。</span><span class="sxs-lookup"><span data-stu-id="c5316-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5316-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5316-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5316-117">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="c5316-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



