---
title: 音訊重新取樣
description: 音訊重新取樣
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK，音訊重新取樣
- Windows Media Format SDK，重新取樣音訊
- Advanced Systems Format (ASF) 、音訊重新取樣
- ASF (Advanced 系統格式) 、音訊重新取樣
- Advanced Systems Format (ASF) 、重新取樣音訊
- ASF (Advanced 系統格式) 、重新取樣音訊
- 音訊重新取樣
- 重新取樣音訊，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300824"
---
# <a name="audio-resampling"></a><span data-ttu-id="9086d-111">音訊重新取樣</span><span class="sxs-lookup"><span data-stu-id="9086d-111">Audio Resampling</span></span>

<span data-ttu-id="9086d-112">音訊編解碼器的每個壓縮格式都有特定的取樣率和樣本大小。</span><span class="sxs-lookup"><span data-stu-id="9086d-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="9086d-113">這些不需要符合輸入格式或輸出格式的設定。</span><span class="sxs-lookup"><span data-stu-id="9086d-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="9086d-114">如果輸入格式的設定與設定檔中所描述的壓縮格式不同，寫入器會在編碼過程中重新取樣音訊，以符合壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="9086d-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="9086d-115">寫入器只接受某些格式做為輸入。</span><span class="sxs-lookup"><span data-stu-id="9086d-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="9086d-116">當您列舉壓縮音訊串流的輸入格式時，所有取出的格式都可以重新取樣，以符合設定檔中的格式。</span><span class="sxs-lookup"><span data-stu-id="9086d-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="9086d-117">讀取壓縮的音訊時，讀取器會重新取樣內容，以符合輸出格式。</span><span class="sxs-lookup"><span data-stu-id="9086d-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="9086d-118">您必須使用讀取器列舉的其中一個輸出格式，以保證音訊可以重新取樣為輸出格式設定。</span><span class="sxs-lookup"><span data-stu-id="9086d-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="9086d-119">每次重新取樣可能會影響音訊品質。</span><span class="sxs-lookup"><span data-stu-id="9086d-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="9086d-120">可能的話，您應該使用輸入和輸出格式搭配符合壓縮格式的設定。</span><span class="sxs-lookup"><span data-stu-id="9086d-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9086d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9086d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9086d-122">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="9086d-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="9086d-123">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="9086d-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="9086d-124">**使用輸出**</span><span class="sxs-lookup"><span data-stu-id="9086d-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




