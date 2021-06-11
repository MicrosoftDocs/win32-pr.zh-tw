---
description: 瞭解 Microsoft 媒體基礎中的媒體範例。 媒體範例是一個物件，其中包含零或多個緩衝區的已排序清單。
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: '媒體範例 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989153"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="cebb2-104">媒體範例 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="cebb2-104">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="cebb2-105">媒體範例是一個物件，其中包含零或多個緩衝區的已排序清單。</span><span class="sxs-lookup"><span data-stu-id="cebb2-105">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="cebb2-106">媒體範例會公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面。</span><span class="sxs-lookup"><span data-stu-id="cebb2-106">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="cebb2-107">一個範例中包含的資料量，取決於建立範例的元件，以及緩衝區中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="cebb2-107">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="cebb2-108">針對未壓縮的影片，範例通常會保留單一的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="cebb2-108">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="cebb2-109">若是未壓縮的音訊，資料量可能會有所不同，但通常音訊框架不會跨越兩個樣本。</span><span class="sxs-lookup"><span data-stu-id="cebb2-109">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="cebb2-110">針對壓縮的資料，可能不適用這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="cebb2-110">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="cebb2-111">基於效率的原因，單一範例可能包含多個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cebb2-111">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="cebb2-112">例如，在 ASF 檔案中，影片框架通常會分散在多個 ASF 封包中。</span><span class="sxs-lookup"><span data-stu-id="cebb2-112">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="cebb2-113">媒體來源可能會將封包讀取至多個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cebb2-113">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="cebb2-114">來源只會將所有緩衝區放入一個範例中，而不是將每個片段複製到一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cebb2-114">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="cebb2-115">下游元件接著可以決定是否要將較小的緩衝區複製到一個連續的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cebb2-115">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="cebb2-116">一般而言，如果您要撰寫管線元件，則應該假設任何範例可能包含一個以上的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cebb2-116">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="cebb2-117">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="cebb2-117">This section contains the following topics.</span></span>



| <span data-ttu-id="cebb2-118">主題</span><span class="sxs-lookup"><span data-stu-id="cebb2-118">Topic</span></span>                                                        | <span data-ttu-id="cebb2-119">描述</span><span class="sxs-lookup"><span data-stu-id="cebb2-119">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cebb2-120">使用媒體範例</span><span class="sxs-lookup"><span data-stu-id="cebb2-120">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="cebb2-121">描述媒體範例的一般行為。</span><span class="sxs-lookup"><span data-stu-id="cebb2-121">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="cebb2-122">影片範例</span><span class="sxs-lookup"><span data-stu-id="cebb2-122">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="cebb2-123">描述專門針對用來保存未壓縮影片畫面的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 執行。</span><span class="sxs-lookup"><span data-stu-id="cebb2-123">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cebb2-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="cebb2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cebb2-125">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="cebb2-125">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="cebb2-126">媒體基礎基本</span><span class="sxs-lookup"><span data-stu-id="cebb2-126">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



