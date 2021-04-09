---
title: '媒體範例 (Windows Media Format 11 SDK) '
description: 媒體範例
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK，媒體範例
- Windows Media Format SDK，範例
- Advanced Systems Format (ASF) 、媒體範例
- ASF (Advanced 系統格式) 、媒體範例
- Advanced Systems Format (ASF) 、範例
- ASF (Advanced Systems Format) ，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933858"
---
# <a name="media-samples-windows-media-format-11-sdk"></a><span data-ttu-id="b3cab-109">媒體範例 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="b3cab-109">Media Samples (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="b3cab-110">媒體範例（或範例）是數位媒體資料的區塊。</span><span class="sxs-lookup"><span data-stu-id="b3cab-110">A media sample, or sample, is a block of digital media data.</span></span> <span data-ttu-id="b3cab-111">範例是讀取和寫入 Windows Media 格式 SDK 的物件所操作的基本單位。</span><span class="sxs-lookup"><span data-stu-id="b3cab-111">A sample is the basic unit that is manipulated by the reading and writing objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="b3cab-112">個別範例的內容是由與範例相關聯的媒體類型所決定。</span><span class="sxs-lookup"><span data-stu-id="b3cab-112">The contents of an individual sample are dictated by the media type associated with the sample.</span></span> <span data-ttu-id="b3cab-113">在影片中，每個範例都代表一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="b3cab-113">For video, each sample represents a single frame.</span></span> <span data-ttu-id="b3cab-114">若是音訊，個別樣本中的資料量是在用來建立 ASF 檔案的設定檔中設定。</span><span class="sxs-lookup"><span data-stu-id="b3cab-114">For audio, the amount of data in an individual sample is set in the profile used to create the ASF file.</span></span>

<span data-ttu-id="b3cab-115">範例可以包含未壓縮的資料，也可以包含壓縮的資料，在這種情況下，它們稱為 *串流範例*。</span><span class="sxs-lookup"><span data-stu-id="b3cab-115">Samples can contain uncompressed data, or they can contain compressed data, in which case they are called *stream samples*.</span></span> <span data-ttu-id="b3cab-116">建立 ASF 檔案時，您會將範例傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="b3cab-116">When creating an ASF file, you pass samples to the writer.</span></span> <span data-ttu-id="b3cab-117">寫入器會以適當的編解碼器來協調範例的壓縮，並將壓縮的資料排列在 ASF 檔案的 [資料] 區段中。</span><span class="sxs-lookup"><span data-stu-id="b3cab-117">The writer coordinates compression of the samples with the appropriate codec and arranges the compressed data in the data section of the ASF file.</span></span> <span data-ttu-id="b3cab-118">在播放時，讀取器會讀取壓縮的資料，並將其解壓縮，並提供重新重建的未壓縮資料作為輸出範例。</span><span class="sxs-lookup"><span data-stu-id="b3cab-118">On playback, the reader reads the compressed data, decompresses it, and provides the reconstructed uncompressed data as output samples.</span></span>

<span data-ttu-id="b3cab-119">Windows Media 格式 SDK 所使用的所有範例都會封裝在由 SDK 執行時間元件自動設定其記憶體的緩衝區物件中。</span><span class="sxs-lookup"><span data-stu-id="b3cab-119">All samples used by the Windows Media Format SDK are encapsulated in buffer object whose memory is allocated automatically by the SDK run-time components.</span></span> <span data-ttu-id="b3cab-120">您也可以視需要使用寫入器和讀取器的 advanced 功能來配置自己的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b3cab-120">You can also allocate your own buffers if you need to, using advanced features of the writer and reader.</span></span>

<span data-ttu-id="b3cab-121">**注意** 此 SDK 中使用「詞彙範例」來參考媒體範例，而非音訊範例。</span><span class="sxs-lookup"><span data-stu-id="b3cab-121">**Note** The term sample is used in this SDK to refer to a media sample, not an audio sample.</span></span> <span data-ttu-id="b3cab-122">在音訊編碼中，範例是指單一編碼的音訊值。</span><span class="sxs-lookup"><span data-stu-id="b3cab-122">In audio encoding, a sample refers to a single encoded audio value.</span></span> <span data-ttu-id="b3cab-123">一般而言，編碼的音訊品質是以每秒的樣本數來指定。</span><span class="sxs-lookup"><span data-stu-id="b3cab-123">Typically, the quality of encoded audio is specified by a number of samples per second.</span></span> <span data-ttu-id="b3cab-124">例如，CD 品質音效會記錄在每秒44100個樣本。</span><span class="sxs-lookup"><span data-stu-id="b3cab-124">For example, CD quality sound is recorded at 44,100 samples per second.</span></span> <span data-ttu-id="b3cab-125">此值通常會以 Hz 標記法縮寫，因此每秒44100個樣本會是 44100 Hz 或 44.1 kHz。</span><span class="sxs-lookup"><span data-stu-id="b3cab-125">This value is commonly abbreviated with the Hz notation, so 44,100 samples per second would be 44,100 Hz or 44.1 kHz.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3cab-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3cab-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3cab-127">**概念**</span><span class="sxs-lookup"><span data-stu-id="b3cab-127">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="b3cab-128">**INSSBuffer 介面**</span><span class="sxs-lookup"><span data-stu-id="b3cab-128">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="b3cab-129">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="b3cab-129">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




