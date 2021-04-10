---
description: WMContainer 物件提供對剖析和寫入 Advanced 系統格式 (ASF) 檔的低層級控制。
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: WMContainer ASF 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944381"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="2ed3b-103">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="2ed3b-103">WMContainer ASF Components</span></span>

<span data-ttu-id="2ed3b-104">WMContainer 物件提供對剖析和寫入 Advanced 系統格式 (ASF) 檔的低層級控制。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="2ed3b-105">[管線層 ASF 元件](pipeline-layer-asf-components.md)會在內部使用 WMContainer 物件。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="2ed3b-106">大部分的應用程式都應該使用管線元件，而不是使用 WMContainer 物件。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="2ed3b-107">只有當您需要對剖析和寫入 ASF 檔案的低層級控制時，才能使用 WMContainer。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="2ed3b-108">WMContainer 層包含下列物件：</span><span class="sxs-lookup"><span data-stu-id="2ed3b-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="2ed3b-109">ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="2ed3b-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="2ed3b-110">ASF ContentInfo 物件</span><span class="sxs-lookup"><span data-stu-id="2ed3b-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="2ed3b-111">ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="2ed3b-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="2ed3b-112">ASF 多工器</span><span class="sxs-lookup"><span data-stu-id="2ed3b-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="2ed3b-113">ASF 索引子</span><span class="sxs-lookup"><span data-stu-id="2ed3b-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="2ed3b-114">下列主題包含有關使用 WMContainer 來讀取或寫入 ASF 檔案的逐步指示。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="2ed3b-115">教學課程：使用 WMContainer 物件讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="2ed3b-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="2ed3b-116">教學課程：使用 WMContainer 物件複製 ASF 資料流程</span><span class="sxs-lookup"><span data-stu-id="2ed3b-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="2ed3b-117">教學課程：使用 WMContainer 物件撰寫 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="2ed3b-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="2ed3b-118">關於 WM 容器</span><span class="sxs-lookup"><span data-stu-id="2ed3b-118">About WM Container</span></span>

<span data-ttu-id="2ed3b-119">WMContainer 物件會直接與 ASF 檔案物件互動。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="2ed3b-120">下圖顯示 ASF 檔案結構和對應的 WMContainer 物件。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![顯示 asf 檔案結構和對應的 media foundation 物件的圖表](images/asf-components01.png)

<span data-ttu-id="2ed3b-122">除了分隔器和多工器之外，每個物件都支援剖析 (讀取) 和寫入 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="2ed3b-123">分隔器只會用來讀取 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="2ed3b-124">多工器只用于撰寫新的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="2ed3b-125">WMContainer 物件所執行的所有作業都是同步的，這表示它們會封鎖呼叫執行緒。</span><span class="sxs-lookup"><span data-stu-id="2ed3b-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ed3b-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ed3b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed3b-127">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="2ed3b-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



