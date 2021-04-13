---
description: 影片轉譯器中的來源和目標矩形
ms.assetid: fdddbffb-c44f-4364-9e2e-b721ba39c74f
title: 影片轉譯器中的來源和目標矩形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556aea6aad22e5ea6df61c74ed0a46d2e3984d67
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510129"
---
# <a name="source-and-target-rectangles-in-video-renderers"></a><span data-ttu-id="dbca5-103">影片轉譯器中的來源和目標矩形</span><span class="sxs-lookup"><span data-stu-id="dbca5-103">Source and Target Rectangles in Video Renderers</span></span>

<span data-ttu-id="dbca5-104">影片媒體類型的 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)、 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)和 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構中有三種大小。</span><span class="sxs-lookup"><span data-stu-id="dbca5-104">There are three sizes found in the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structures of video media types.</span></span> <span data-ttu-id="dbca5-105">本文將說明它們是什麼，以及它們的運作方式。</span><span class="sxs-lookup"><span data-stu-id="dbca5-105">This article explains what they are and how they work.</span></span>

<span data-ttu-id="dbca5-106">首先，這些結構的 **bmiHeader** 成員會有大小。</span><span class="sxs-lookup"><span data-stu-id="dbca5-106">First, there is a size in the **bmiHeader** member of these structures.</span></span> <span data-ttu-id="dbca5-107">**BmiHeader** 成員是具有自己的寬度和高度成員（ **bmiHeader. biWidth** 和 **BmiHeader. biHeight**）的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。</span><span class="sxs-lookup"><span data-stu-id="dbca5-107">The **bmiHeader** member is a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure with its own width and height members, **bmiHeader.biWidth** and **bmiHeader.biHeight**.</span></span>

<span data-ttu-id="dbca5-108">其次，這些結構的 **rcSource** 成員中有一個矩形;最後，這些結構的 **rcTarget** 成員中有一個矩形。</span><span class="sxs-lookup"><span data-stu-id="dbca5-108">Second, there is a rectangle in the **rcSource** member of these structures; and last, there is a rectangle in the **rcTarget** member of these structures.</span></span>

<span data-ttu-id="dbca5-109">假設您有兩個篩選器，A 和 B，這些篩選器會彼此連接 (左邊、上游、右邊的 B，或具有特定影片媒體類型的下游) 。</span><span class="sxs-lookup"><span data-stu-id="dbca5-109">Assume you have two filters, A and B, and that these filters are connected to each other (A on the left, or upstream, and B on the right, or downstream) with a certain video media type.</span></span>

<span data-ttu-id="dbca5-110">在篩選 A 和 B 之間傳遞的緩衝區大小 (**bmiHeader. biWidth**、 **bmiHeader. biHeight**) 。</span><span class="sxs-lookup"><span data-stu-id="dbca5-110">The buffers that pass between filters A and B have the size (**bmiHeader.biWidth**, **bmiHeader.biHeight**).</span></span> <span data-ttu-id="dbca5-111">篩選 A 應該採用 **rcSource** 決定的部分輸入影片，並延展該影片以填滿緩衝區的 **rcTarget** 部分。</span><span class="sxs-lookup"><span data-stu-id="dbca5-111">Filter A should take a portion of its input video determined by **rcSource** and stretch that video to fill the **rcTarget** portion of the buffer.</span></span> <span data-ttu-id="dbca5-112">所要使用之輸入影片的部分是根據 **rcSource** 與 (**biWidth** 的比較方式，也就是篩選 A 和 B 原本連接的媒體類型的 **biHeight**) 大小。</span><span class="sxs-lookup"><span data-stu-id="dbca5-112">The portion of the input video to use is based on how **rcSource** compares to the (**biWidth**, **biHeight**) size of the media type that filters A and B originally connected with.</span></span> <span data-ttu-id="dbca5-113">如果 **rcSource** 是空的，則篩選 A 會使用其整個輸入影片。</span><span class="sxs-lookup"><span data-stu-id="dbca5-113">If **rcSource** is empty, filter A uses its entire input video.</span></span> <span data-ttu-id="dbca5-114">如果 **rcTarget** 是空的，則篩選會填滿整個輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbca5-114">If **rcTarget** is empty, filter A fills the entire output buffer.</span></span>

<span data-ttu-id="dbca5-115">例如，假設篩選 A 正在接收 160 x 120 圖元的影片資料。</span><span class="sxs-lookup"><span data-stu-id="dbca5-115">For example, assume filter A is receiving video data that is 160 x 120 pixels.</span></span> <span data-ttu-id="dbca5-116">也假設篩選 A 使用下列媒體類型連接至篩選 B。</span><span class="sxs-lookup"><span data-stu-id="dbca5-116">Assume also that filter A is connected to filter B with the following media type.</span></span>

-   <span data-ttu-id="dbca5-117"> (**biWidth**、 **biHeight**) ：320、240</span><span class="sxs-lookup"><span data-stu-id="dbca5-117">(**biWidth**, **biHeight**): 320, 240</span></span>
-   <span data-ttu-id="dbca5-118">**rcSource**： (0、0、0、0) </span><span class="sxs-lookup"><span data-stu-id="dbca5-118">**rcSource**: (0, 0, 0, 0)</span></span>
-   <span data-ttu-id="dbca5-119">**rcTarget**： (0、0、0、0) </span><span class="sxs-lookup"><span data-stu-id="dbca5-119">**rcTarget**: (0, 0, 0, 0)</span></span>

<span data-ttu-id="dbca5-120">這表示篩選 A 會以 x 和 y 方向的2來延展所收到的影片，並填滿 320 x 240 輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbca5-120">This means that filter A will stretch the video it receives by 2 in both the x and y directions, and fill a 320 x 240 output buffer.</span></span>

<span data-ttu-id="dbca5-121">另一個範例是，假設篩選 A 正在接收 160 x 120 video 資料，而且它是以下列媒體類型連接至篩選 B。</span><span class="sxs-lookup"><span data-stu-id="dbca5-121">As another example, assume filter A is receiving 160 x 120 video data, and that it is connected to filter B with the following media type.</span></span>

-   <span data-ttu-id="dbca5-122"> (**biWidth**、 **biHeight**) ：320、240</span><span class="sxs-lookup"><span data-stu-id="dbca5-122">(**biWidth**, **biHeight**): 320, 240</span></span>
-   <span data-ttu-id="dbca5-123">**rcSource**： (0、0、160、240) </span><span class="sxs-lookup"><span data-stu-id="dbca5-123">**rcSource**: (0, 0, 160, 240)</span></span>
-   <span data-ttu-id="dbca5-124">**rcTarget**： (0、0、0、0) </span><span class="sxs-lookup"><span data-stu-id="dbca5-124">**rcTarget**: (0, 0, 0, 0)</span></span>

<span data-ttu-id="dbca5-125">**RcSource** 成員相對於連接的緩衝區大小320，240。</span><span class="sxs-lookup"><span data-stu-id="dbca5-125">The **rcSource** member is relative to the connected buffer size of 320, 240.</span></span> <span data-ttu-id="dbca5-126">因為指定的 **rcSource** (0，0、160、240) 是緩衝區的左邊半部，篩選 A 會採用其輸入影片的左邊半部，或 (0、0、80、120) 部分，並將影片延展至 (320、240)  (x 方向的4，以及 y 方向的2，) 並填滿 320 x 240 輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbca5-126">Because the specified **rcSource** (0, 0, 160, 240) is the left half of the buffer, filter A will take the left half of its input video, or the (0, 0, 80, 120) portion, and stretch the video to a size of (320, 240) (by 4 in the x direction, and by 2 in the y direction) and filling the 320 x 240 output buffer.</span></span>

<span data-ttu-id="dbca5-127">現在假設篩選 A 呼叫 [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md)，且傳回的媒體範例有附加的媒體類型，表示篩選 B 希望篩選 a 提供不同于先前提供的大小或影片類型。</span><span class="sxs-lookup"><span data-stu-id="dbca5-127">Now assume that filter A calls [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md), and the media sample returned has a media type attached to it, signifying that filter B wants filter A to provide a different size or kind of video than it has previously been providing.</span></span> <span data-ttu-id="dbca5-128">假設新的媒體類型為：</span><span class="sxs-lookup"><span data-stu-id="dbca5-128">Assume the new media type is:</span></span>

-   <span data-ttu-id="dbca5-129"> (**biWidth**、 **biHeight**) ：640、480</span><span class="sxs-lookup"><span data-stu-id="dbca5-129">(**biWidth**, **biHeight**): 640, 480</span></span>
-   <span data-ttu-id="dbca5-130">**rcSource**： (0、0、160、120) </span><span class="sxs-lookup"><span data-stu-id="dbca5-130">**rcSource**: (0, 0, 160, 120)</span></span>
-   <span data-ttu-id="dbca5-131">**rcTarget**： (0、0、80、60) </span><span class="sxs-lookup"><span data-stu-id="dbca5-131">**rcTarget**: (0, 0, 80, 60)</span></span>

<span data-ttu-id="dbca5-132">這表示媒體範例有一個大小為 640 x 480 的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbca5-132">This means that the media sample has a buffer that is 640 x 480 in size.</span></span> <span data-ttu-id="dbca5-133">**RcSource** 成員相對於原始的連線媒體類型 (320、240) 不 (640、480) 的新媒體類型，因此 **rcSource** 指定要使用輸入影片的左上角 (25% ) 。</span><span class="sxs-lookup"><span data-stu-id="dbca5-133">The **rcSource** member is relative to the original connected media type (320, 240) not to the new media type of (640, 480), so **rcSource** specifies that the top-left corner (25%) of the input video is to be used.</span></span> <span data-ttu-id="dbca5-134">這部分的輸入影片會置於左上角 (80、60) 圖元（640 x 480 輸出緩衝區），如 (0、0、80、60) 的 **rcTarget** 所指定。</span><span class="sxs-lookup"><span data-stu-id="dbca5-134">This portion of the input video is placed in the top-left (80, 60) pixels of the 640 x 480 output buffer, as specified by **rcTarget** of (0, 0, 80, 60).</span></span> <span data-ttu-id="dbca5-135">由於篩選 A 會接收 160 x 120 影片，因此輸入影片的左上角是 (80、60) 片段、相同大小的輸出點陣圖，且不需要延展。</span><span class="sxs-lookup"><span data-stu-id="dbca5-135">Because filter A is receiving 160 x 120 video, the top-left corner of the input video is an (80, 60) piece, the same size of the output bitmap, and no stretching is required.</span></span>

<span data-ttu-id="dbca5-136">篩選準則將不會在輸出緩衝區的其他圖元內放置任何資料，而且不會讓這些位保持不變。</span><span class="sxs-lookup"><span data-stu-id="dbca5-136">Filter A will place no data in the other pixels of the output buffer, and will leave those bits untouched.</span></span> <span data-ttu-id="dbca5-137">**RcSource** 成員系結于篩選 A 和 B 之間原始連線媒體類型的 **biWidth** 和 **biHeight** ，而 **rcTarget** 則是由媒體範例的新 **biWidth** 和 **biHeight** 所限制。</span><span class="sxs-lookup"><span data-stu-id="dbca5-137">The **rcSource** member is bounded by the **biWidth** and **biHeight** of the original connected media type between filters A and B, and **rcTarget** is bounded by the new **biWidth** and **biHeight** of the media sample.</span></span> <span data-ttu-id="dbca5-138">在上述範例中， **rcSource** 無法超出 (0、0、320、240) 的界限，而且 **rcTarget** 無法超出 (0、0、640、480) 的範圍。</span><span class="sxs-lookup"><span data-stu-id="dbca5-138">In the preceding example, **rcSource** could not go outside the boundaries of (0, 0, 320, 240) and **rcTarget** could not go outside the boundaries of (0, 0, 640, 480).</span></span>

 

 



