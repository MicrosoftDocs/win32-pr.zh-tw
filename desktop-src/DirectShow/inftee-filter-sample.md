---
description: InfTee 篩選範例
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: InfTee 篩選範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972118"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="c2187-103">InfTee 篩選範例</span><span class="sxs-lookup"><span data-stu-id="c2187-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="c2187-104">Description</span><span class="sxs-lookup"><span data-stu-id="c2187-104">Description</span></span>

<span data-ttu-id="c2187-105">InfTee 篩選器提供了 DirectShow [無限釘](infinite-pin-tee-filter.md) 選篩選準則的範例執行。</span><span class="sxs-lookup"><span data-stu-id="c2187-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="c2187-106">篩選器具有一個輸入的 pin 和動態的輸出圖釘數目。</span><span class="sxs-lookup"><span data-stu-id="c2187-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="c2187-107">所有傳送至篩選器的媒體範例都會從所有輸出圖釘同時傳遞。</span><span class="sxs-lookup"><span data-stu-id="c2187-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="c2187-108">此篩選器會出現在 GraphEdit 的「範例無限 Pin 碼 t」名稱底下，以與 DirectShow 中提供的標準無限 Pin 指標篩選準則區別。</span><span class="sxs-lookup"><span data-stu-id="c2187-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="c2187-109">使用方式</span><span class="sxs-lookup"><span data-stu-id="c2187-109">Usage</span></span>

<span data-ttu-id="c2187-110">因為此篩選不會變更其所接收的資料，所以所有的 pin 都必須同意相同的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c2187-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="c2187-111">在連接過程中，篩選器可能會重新連接某些 pin，以使媒體類型相符。</span><span class="sxs-lookup"><span data-stu-id="c2187-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="c2187-112">到達輸入 pin 的資料在傳送至輸出圖釘之前，不會先複製。</span><span class="sxs-lookup"><span data-stu-id="c2187-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="c2187-113">篩選準則也可確保將資料傳遞至下游篩選器，以保證這兩個輸出都會收到及時的服務。</span><span class="sxs-lookup"><span data-stu-id="c2187-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="c2187-114">尤其是，如果其中一個輸出可以在 [**COutputQueue：： Receive**](coutputqueue-receive.md) 成員函式中封鎖，則 t 會將執行緒旋轉以傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="c2187-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="c2187-115">如果沒有可傳遞範例的執行緒，則傳遞範例至 t 輸入 pin 的執行緒可能會將資料傳遞至下游篩選;屆時，它可能會封鎖，並保留其他下游篩選的資料很長一段時間。</span><span class="sxs-lookup"><span data-stu-id="c2187-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c2187-116">下載範例</span><span class="sxs-lookup"><span data-stu-id="c2187-116">Downloading the Sample</span></span>

<span data-ttu-id="c2187-117">若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c2187-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="c2187-118">此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 篩選 \\ InfTee。</span><span class="sxs-lookup"><span data-stu-id="c2187-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2187-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2187-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2187-120">DirectShow 範例</span><span class="sxs-lookup"><span data-stu-id="c2187-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



