---
title: 多步驟格式轉換
description: 多步驟格式轉換
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- 音訊壓縮管理員 (的) 、轉換資料
- " (音效壓縮管理員) 、轉換資料"
- 進行中的範例，轉換資料
- 轉換資料
- acmFormatSuggest 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932270"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="c5a4b-108">多步驟格式轉換</span><span class="sxs-lookup"><span data-stu-id="c5a4b-108">Multistep Format Conversion</span></span>

<span data-ttu-id="c5a4b-109">在單一步驟中，無法將資料從一種格式轉換成另一種格式。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="c5a4b-110">例如，應用程式可能需要將16位、44-kHz 身歷聲資料轉換為 11-kHz mono ADPCM。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="c5a4b-111">如果壓縮程式或解壓縮程式無法直接執行這項轉換，應用程式可能會以兩個步驟來嘗試。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="c5a4b-112">這通常表示在兩個 PCM 格式之間進行一次轉換，然後再轉換成最終的格式類型。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="c5a4b-113">若要使用兩個步驟進行轉換，請使用 [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) 函式來尋找符合 ADPCM 格式的 PCM 格式。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="c5a4b-114">然後使用兩個轉換資料流程來執行轉換。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="c5a4b-115">例如，執行一個從16位、44-kHz 身歷聲 PCM 到16位、11-kHz mono 的轉換，然後從16位、11-kHz mono 轉換為 11-kHz mono ADPCM。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="c5a4b-116">多步驟轉換也會在來源或目的地格式不是 PCM 時進行。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="c5a4b-117">如果來源格式不是 PCM，則在轉換之前，應該將它變更為 PCM 格式。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="c5a4b-118">如果目的地格式不是 PCM，則來源必須轉換成中繼 PCM 格式，然後轉換成最終目的地格式。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="c5a4b-119">當來源和目的地格式都是 PCM 格式時，最直接的轉換會發生。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="c5a4b-120">如果來源或目的地的格式不是 PCM，轉換可能需要額外的步驟。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="c5a4b-121">如果來源和目的地格式都不是 PCM，轉換通常需要一個以上的步驟，而在某些情況下，可能無法進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c5a4b-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




