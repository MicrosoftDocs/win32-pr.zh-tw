---
description: MPEG-2 Demux Run-Time 模式
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: MPEG-2 Demux Run-Time 模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109645"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="c9ae8-103">MPEG-2 Demux Run-Time 模式</span><span class="sxs-lookup"><span data-stu-id="c9ae8-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="c9ae8-104">[Mpeg-2 信號](mpeg-2-demultiplexer.md) ( "demux" ) 可以在 push 模式或 pull 模式下運作。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="c9ae8-105">在推送模式中，資料來自即時來源，例如網路廣播。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="c9ae8-106">在提取模式中，資料來自本機檔案。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="c9ae8-107">在 Windows XP 和更新版本中，提取模式僅適用于程式串流。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="c9ae8-108">在舊版平臺上，使用 [Mpeg-2 分隔](mpeg-2-splitter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="c9ae8-109">推送模式適用于所有平臺，適用于程式資料流程和傳輸串流。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="c9ae8-110">因此，demux 支援三種可能的模式：提取模式的程式資料流程、推入模式中的程式資料流程，以及推送模式的傳輸資料流程。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="c9ae8-111">Demux 會決定在執行時間使用的模式。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="c9ae8-112">當輸入連接或第一個輸出 pin 已設定時（以先發生者為准），會決定模式：</span><span class="sxs-lookup"><span data-stu-id="c9ae8-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="c9ae8-113">當輸入 pin 連接：在 Windows XP 和更新版本上，demux 會查詢 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的上游篩選;如果上游篩選器公開該介面，demux 會在提取模式中為程式資料流程設定本身。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="c9ae8-114">否則，demux 會使用 push 模式，而媒體類型會判斷 (程式資料流程或傳輸資料流程) 的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="c9ae8-115">如需輸入類型清單，請參閱 [**Mpeg-2 信號的媒體類型**](mpeg-2-demultiplexer-media-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="c9ae8-116">當第一個輸出 pin 設定時：如果您建立輸出釘選並查詢它以進行 [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)，demux 會為推送模式中的傳輸資料流程設定本身。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="c9ae8-117">如果您查詢 [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap)的 pin，demux 會為程式資料流程設定本身，也會在推送模式中設定。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="c9ae8-118">針對其他介面進行的任何後續查詢都會失敗，因為 demux 無法一次以兩種模式運作。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="c9ae8-119">一旦 demux 為特定模式設定本身，它就會維持在該模式中。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="c9ae8-120">若要使用不同的模式，您必須建立 demux 的新實例。</span><span class="sxs-lookup"><span data-stu-id="c9ae8-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9ae8-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="c9ae8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9ae8-122">使用 MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="c9ae8-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



