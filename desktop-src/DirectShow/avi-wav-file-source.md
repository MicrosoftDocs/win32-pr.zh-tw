---
description: AVI/WAV 檔案來源
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: AVI/WAV 檔案來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971294"
---
# <a name="aviwav-file-source"></a><span data-ttu-id="add86-103">AVI/WAV 檔案來源</span><span class="sxs-lookup"><span data-stu-id="add86-103">AVI/WAV File Source</span></span>

<span data-ttu-id="add86-104">(已淘汰。</span><span class="sxs-lookup"><span data-stu-id="add86-104">(Deprecated.</span></span> <span data-ttu-id="add86-105">若是 AVI 和 WAV 檔案，請使用檔案 [來源 (Async) ](file-source--async--filter.md) 和 [AVI 分隔器](avi-splitter-filter.md) 或 [WAVE](wave-parser-filter.md)剖析器。 ) </span><span class="sxs-lookup"><span data-stu-id="add86-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="add86-106">AVI/WAV 檔案來源篩選器會讀取 AVI 和 WAV 來源檔案，並針對檔案類型產生適當的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="add86-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="add86-107">針對 WAV 檔案，此篩選會建立音訊輸出針腳，以產生可連接到音訊轉譯篩選器或仲介音訊轉換篩選器的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="add86-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="add86-108">對於 AVI 檔案，此篩選會建立影片輸出圖釘，它會產生適合 AVI 編解碼器篩選器的壓縮 AVI 資料流程，而音訊輸出圖釘則會產生適合音訊轉譯篩選或中間音訊轉換篩選的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="add86-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="add86-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="add86-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add86-110">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="add86-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



