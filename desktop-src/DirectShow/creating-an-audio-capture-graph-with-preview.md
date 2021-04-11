---
description: 使用預覽建立音訊捕獲圖形
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: 使用預覽建立音訊捕獲圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103936012"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="8f7c5-103">使用預覽建立音訊捕獲圖形</span><span class="sxs-lookup"><span data-stu-id="8f7c5-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="8f7c5-104">[建立音訊捕獲圖形](creating-an-audio-capture-graph.md)中所述的篩選圖形只會執行 Capture，沒有預覽。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="8f7c5-105">若要同時預覽和捕捉，則篩選圖形必須使用 [無限 Pin 指標篩選](infinite-pin-tee-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="8f7c5-106">此篩選器有一個輸入 pin，並會視需要建立多個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="8f7c5-107"> (其開頭為一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-107">(It starts with one output pin.</span></span> <span data-ttu-id="8f7c5-108">每次連接輸出釘選時，它會建立另一個。 ) 無限 Pin 的 t a t t t a t t 篩選準則會透過其所有輸出接點，傳遞每個接收到的樣本（未變更）。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="8f7c5-109">將音訊捕獲篩選器連線到無限釘選，然後將無限的釘選到多工器和 [DirectSound 轉譯器篩選器](directsound-renderer-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="8f7c5-110">如同之前一樣，將多工器連接到檔案寫入器。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="8f7c5-111">下圖說明 AVI 檔案產生的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![具有預覽的音訊捕獲圖表](images/audio-capture-graph.png)

<span data-ttu-id="8f7c5-113">因為 DirectSound 轉譯器是預設的音訊轉譯器，所以您可以直接在無限釘選的輸出圖釘上呼叫 [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) 方法。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="8f7c5-114">篩選圖形管理員會使用 [智慧型連接](intelligent-connect.md) 來建立轉譯器、將它新增至篩選圖形，以及連接釘選。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="8f7c5-115">如果您從麥克風捕獲音訊，並從同一部電腦上的喇叭進行預覽，您可能會建立音訊意見反應。</span><span class="sxs-lookup"><span data-stu-id="8f7c5-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8f7c5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f7c5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f7c5-117">音訊捕獲</span><span class="sxs-lookup"><span data-stu-id="8f7c5-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



