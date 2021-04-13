---
description: 傾印篩選範例
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: 傾印篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510265"
---
# <a name="dump-filter-sample"></a><span data-ttu-id="df552-103">傾印篩選範例</span><span class="sxs-lookup"><span data-stu-id="df552-103">Dump Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="df552-104">Description</span><span class="sxs-lookup"><span data-stu-id="df552-104">Description</span></span>

<span data-ttu-id="df552-105">傾印篩選器是轉譯器篩選器，可將其接收的媒體範例寫入文字檔。</span><span class="sxs-lookup"><span data-stu-id="df552-105">The Dump Filter is a renderer filter that writes the media samples it receives to a text file.</span></span>

<span data-ttu-id="df552-106">此範例說明如何使用基底篩選類別 [**CBaseFilter**](cbasefilter.md) 和轉譯的輸入針腳類別 [**CRenderedInputPin**](crenderedinputpin.md)。</span><span class="sxs-lookup"><span data-stu-id="df552-106">This sample illustrates how to use the base filter class [**CBaseFilter**](cbasefilter.md) and the rendered input pin class [**CRenderedInputPin**](crenderedinputpin.md).</span></span> <span data-ttu-id="df552-107">它也會示範如何執行 [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) 介面。</span><span class="sxs-lookup"><span data-stu-id="df552-107">It also demonstrates how to implement the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface.</span></span> <span data-ttu-id="df552-108">傾印篩選器具有單一輸入 pin，會將它直接接收的每個範例寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="df552-108">The Dump filter has a single input pin, which writes every sample that it receives directly to a file.</span></span>

## <a name="usage"></a><span data-ttu-id="df552-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="df552-109">Usage</span></span>

<span data-ttu-id="df552-110">此篩選是實用的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="df552-110">This filter is a useful debugging tool.</span></span> <span data-ttu-id="df552-111">例如，您可以驗證轉換篩選的結果（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="df552-111">For example, you can verify, bit by bit, the results of a transform filter.</span></span> <span data-ttu-id="df552-112">您可以使用 GraphEdit 來手動建立圖形，並將傾印篩選連接到轉換篩選器或任何其他輸出的輸出。</span><span class="sxs-lookup"><span data-stu-id="df552-112">You can build a graph manually by using GraphEdit, and connect the Dump filter to the output of a transform filter or any other output pin.</span></span> <span data-ttu-id="df552-113">您也可以連接到 t-sql 篩選器，並將傾印篩選放在 t-sql 篩選器的一個階段，並將一般輸出放在另一個階段，以在即時案例中監視結果。</span><span class="sxs-lookup"><span data-stu-id="df552-113">You can also connect a tee filter and put the Dump filter on one leg of the tee filter and the typical output on another leg to monitor the results in a real-time scenario.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="df552-114">下載範例</span><span class="sxs-lookup"><span data-stu-id="df552-114">Downloading the Sample</span></span>

<span data-ttu-id="df552-115">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="df552-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="df552-116">此範例安裝在下列路徑下： *\[ SDK 根 \]* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ 傾印。</span><span class="sxs-lookup"><span data-stu-id="df552-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Dump.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df552-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="df552-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df552-118">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="df552-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



