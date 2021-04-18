---
title: 呈現時間
description: 呈現時間
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media Format SDK，簡報時間
- Advanced Systems Format (ASF) ，簡報時間
- ASF (Advanced Systems Format) ，簡報時間
- 展示時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301732"
---
# <a name="presentation-time"></a><span data-ttu-id="2eca9-107">呈現時間</span><span class="sxs-lookup"><span data-stu-id="2eca9-107">Presentation Time</span></span>

<span data-ttu-id="2eca9-108">呈現時間是從 ASF 檔案中第一個資料流程的第一個範例測量時間。</span><span class="sxs-lookup"><span data-stu-id="2eca9-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="2eca9-109">這項測量，以及此 SDK 的物件所使用的大部分其他時間測量值為 100-毫微秒單位。</span><span class="sxs-lookup"><span data-stu-id="2eca9-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="2eca9-110">簡報時間很重要，因為它們可讓檔案中的各種資料流程進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="2eca9-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="2eca9-111">您必須為您傳遞至寫入器的每個輸入範例提供呈現時間。</span><span class="sxs-lookup"><span data-stu-id="2eca9-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="2eca9-112">ASF 檔案的 [資料] 區段中的每個資料物件都有相關聯的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="2eca9-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="2eca9-113">讀取器取出的每個輸出範例也都有呈現時間。</span><span class="sxs-lookup"><span data-stu-id="2eca9-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2eca9-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="2eca9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eca9-115">**概念**</span><span class="sxs-lookup"><span data-stu-id="2eca9-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="2eca9-116">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="2eca9-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="2eca9-117">**媒體範例**</span><span class="sxs-lookup"><span data-stu-id="2eca9-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 




