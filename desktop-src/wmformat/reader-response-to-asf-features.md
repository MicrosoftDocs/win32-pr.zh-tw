---
title: ASF 功能的讀取器回應
description: ASF 功能的讀取器回應
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media 格式 SDK，讀取器回應 ASF 功能
- Advanced Systems Format (ASF) ，讀取器對功能的回應
- ASF (Advanced 系統格式) ，讀取器回應功能
- 對 ASF 功能的讀取器回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967420"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="21416-107">ASF 功能的讀取器回應</span><span class="sxs-lookup"><span data-stu-id="21416-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="21416-108">大部分的特殊 ASF 檔案功能都可以在檔案中設定，以與設計用來處理它們的自訂播放應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="21416-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="21416-109">不過，某些功能在 reader 物件中有內建支援。</span><span class="sxs-lookup"><span data-stu-id="21416-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="21416-110">讀取器物件會自動從以位元速率互斥的集合中選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="21416-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="21416-111">這種特殊案例稱為 (MBR) 的多重位元速率。</span><span class="sxs-lookup"><span data-stu-id="21416-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="21416-112">讀取器選取的資料流程是以資料流程的位元速率為基礎。</span><span class="sxs-lookup"><span data-stu-id="21416-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="21416-113">資料流程號碼和將其加入至互斥物件的順序與自動選取無關。</span><span class="sxs-lookup"><span data-stu-id="21416-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="21416-114">如果檔案包含多個以位元速率互斥的資料流程集合，則讀取器會根據可用頻寬的最佳使用方式來選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="21416-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="21416-115">以語言為基礎的相互排除是在播放之前使用輸出設定來設定。</span><span class="sxs-lookup"><span data-stu-id="21416-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="21416-116">如果您結合了語言和以位速率為基礎的相互排除，您應該依語言將以位速率為基礎的互斥資料流程分組，然後讓群組依語言相互排斥。</span><span class="sxs-lookup"><span data-stu-id="21416-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="21416-117">讀取器會先檢查語言，然後判斷要使用的位元速率。</span><span class="sxs-lookup"><span data-stu-id="21416-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="21416-118">資料流程優先順序是使用記錄的陣列設定。</span><span class="sxs-lookup"><span data-stu-id="21416-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="21416-119">陣列中的記錄依優先權的遞減順序排列。</span><span class="sxs-lookup"><span data-stu-id="21416-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="21416-120">陣列中的最後一個資料流程是讀取器將卸載的第一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="21416-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21416-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="21416-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21416-122">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="21416-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="21416-123">**互斥**</span><span class="sxs-lookup"><span data-stu-id="21416-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="21416-124">**資料流程優先順序**</span><span class="sxs-lookup"><span data-stu-id="21416-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




