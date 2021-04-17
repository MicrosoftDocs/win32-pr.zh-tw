---
description: DirectShow 應用程式程式設計簡介
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: DirectShow 應用程式程式設計簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385673"
---
# <a name="introduction-to-directshow-application-programming"></a><span data-ttu-id="45049-103">DirectShow 應用程式程式設計簡介</span><span class="sxs-lookup"><span data-stu-id="45049-103">Introduction to DirectShow Application Programming</span></span>

<span data-ttu-id="45049-104">本文介紹 DirectShow 中使用的基本術語和概念。</span><span class="sxs-lookup"><span data-stu-id="45049-104">This article introduces the basic terminology and concepts that are used in DirectShow.</span></span> <span data-ttu-id="45049-105">閱讀本節之後，您就可以開始撰寫您的第一個 DirectShow 應用程式。</span><span class="sxs-lookup"><span data-stu-id="45049-105">After reading this section, you will be ready to write your first DirectShow application.</span></span>

<span data-ttu-id="45049-106">**篩選和篩選圖形**</span><span class="sxs-lookup"><span data-stu-id="45049-106">**Filters and Filter Graphs**</span></span>

<span data-ttu-id="45049-107">DirectShow 的建立區塊是稱為 *篩選器* 的軟體元件。</span><span class="sxs-lookup"><span data-stu-id="45049-107">The building block of DirectShow is a software component called a *filter*.</span></span> <span data-ttu-id="45049-108">篩選器是一種軟體元件，可在多媒體串流上執行某些作業。</span><span class="sxs-lookup"><span data-stu-id="45049-108">A filter is a software component that performs some operation on a multimedia stream.</span></span> <span data-ttu-id="45049-109">例如，DirectShow 篩選器可以</span><span class="sxs-lookup"><span data-stu-id="45049-109">For example, DirectShow filters can</span></span>

-   <span data-ttu-id="45049-110">讀取檔案</span><span class="sxs-lookup"><span data-stu-id="45049-110">read files</span></span>
-   <span data-ttu-id="45049-111">從影片捕獲裝置取得影片</span><span class="sxs-lookup"><span data-stu-id="45049-111">get video from a video capture device</span></span>
-   <span data-ttu-id="45049-112">解碼各種不同的串流格式，例如 MPEG-1 video</span><span class="sxs-lookup"><span data-stu-id="45049-112">decode various stream formats, such as MPEG-1 video</span></span>
-   <span data-ttu-id="45049-113">將資料傳遞至圖形或音效卡</span><span class="sxs-lookup"><span data-stu-id="45049-113">pass data to the graphics or sound card</span></span>

<span data-ttu-id="45049-114">篩選器會接收輸入並產生輸出。</span><span class="sxs-lookup"><span data-stu-id="45049-114">Filters receive input and produce output.</span></span> <span data-ttu-id="45049-115">例如，如果篩選器會解碼 MPEG-2 影片，則輸入為 MPEG 編碼的資料流程，而輸出是一系列未壓縮的影片框架。</span><span class="sxs-lookup"><span data-stu-id="45049-115">For example, if a filter decodes MPEG-1 video, the input is the MPEG-encoded stream and the output is a series of uncompressed video frames.</span></span>

<span data-ttu-id="45049-116">在 DirectShow 中，應用程式會將篩選鏈連接在一起，以執行任何工作，讓某個篩選的輸出變成另一個篩選的輸入。</span><span class="sxs-lookup"><span data-stu-id="45049-116">In DirectShow, an application performs any task by connecting chains of filters together, so that the output from one filter becomes the input for another.</span></span> <span data-ttu-id="45049-117">一組連接的篩選稱為 *篩選圖形*。</span><span class="sxs-lookup"><span data-stu-id="45049-117">A set of connected filters is called a *filter graph*.</span></span> <span data-ttu-id="45049-118">例如，下圖顯示用來播放 AVI 檔案的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="45049-118">For example, the following diagram shows a filter graph for playing an AVI file.</span></span>

![用來播放 avi 檔案的篩選圖形](images/avi-filter-graph.png)

<span data-ttu-id="45049-120">檔案來源篩選器會從硬碟讀取 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="45049-120">The File Source filter reads the AVI file from the hard disk.</span></span> <span data-ttu-id="45049-121">AVI 分隔器篩選器會將檔案剖析成兩個數據流：壓縮的影片資料流程和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="45049-121">The AVI Splitter filter parses the file into two streams, a compressed video stream and an audio stream.</span></span> <span data-ttu-id="45049-122">AVI 解壓縮程式篩選器會解碼影片畫面。</span><span class="sxs-lookup"><span data-stu-id="45049-122">The AVI Decompressor filter decodes the video frames.</span></span> <span data-ttu-id="45049-123">影片轉譯器篩選器會使用 DirectDraw 或 GDI 來繪製畫面上顯示的畫面格。</span><span class="sxs-lookup"><span data-stu-id="45049-123">The Video Renderer filter draws the frames to the display, using DirectDraw or GDI.</span></span> <span data-ttu-id="45049-124">預設 DirectSound 裝置篩選器會使用 DirectSound 播放音訊串流。</span><span class="sxs-lookup"><span data-stu-id="45049-124">The Default DirectSound Device filter plays the audio stream, using DirectSound.</span></span>

<span data-ttu-id="45049-125">應用程式不需要管理此資料流程。</span><span class="sxs-lookup"><span data-stu-id="45049-125">The application does not have to manage all of this data flow.</span></span> <span data-ttu-id="45049-126">相反地，篩選是由稱為「篩選圖形管理員」的高階元件所控制。</span><span class="sxs-lookup"><span data-stu-id="45049-126">Instead, the filters are controlled by a high-level component called the Filter Graph Manager.</span></span> <span data-ttu-id="45049-127">應用程式會進行高階 API 呼叫（例如「執行」 (以透過圖形移動資料) 或「停止」 (以停止) 資料的流程。</span><span class="sxs-lookup"><span data-stu-id="45049-127">The application makes high-level API calls such as "Run" (to move data through the graph) or "Stop" (to stop the flow of data).</span></span> <span data-ttu-id="45049-128">如果您需要更充分掌控資料流程作業，您可以直接透過 COM 介面存取篩選。</span><span class="sxs-lookup"><span data-stu-id="45049-128">If you require more control over the stream operations, you can access the filters directly through COM interfaces.</span></span> <span data-ttu-id="45049-129">篩選圖形管理員也會將事件通知傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="45049-129">The Filter Graph Manager also passes event notifications to the application.</span></span>

<span data-ttu-id="45049-130">篩選圖形管理員也提供另一個用途：它會透過將篩選連接在一起，提供應用程式建立篩選圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="45049-130">The Filter Graph Manager serves another purpose as well: It provides methods for the application to build the filter graph, by connecting the filters together.</span></span> <span data-ttu-id="45049-131"> (DirectShow 也提供可簡化此程式的各種 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="45049-131">(DirectShow also provides various helper objects that simplify this process.</span></span> <span data-ttu-id="45049-132">這些會在檔中完整說明。 ) </span><span class="sxs-lookup"><span data-stu-id="45049-132">These are thoroughly described in the documentation.)</span></span>

<span data-ttu-id="45049-133">**撰寫 DirectShow 應用程式**</span><span class="sxs-lookup"><span data-stu-id="45049-133">**Writing a DirectShow Application**</span></span>

<span data-ttu-id="45049-134">大致上，有三個可供任何 DirectShow 應用程式執行的工作。</span><span class="sxs-lookup"><span data-stu-id="45049-134">In broad terms, there are three tasks that any DirectShow application must perform.</span></span> <span data-ttu-id="45049-135">如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="45049-135">These are illustrated in the following diagram.</span></span>

![典型的 directshow 應用程式](images/fgm.png)

1.  <span data-ttu-id="45049-137">應用程式會建立篩選圖形管理員的實例。</span><span class="sxs-lookup"><span data-stu-id="45049-137">The application creates an instance of the Filter Graph Manager.</span></span>
2.  <span data-ttu-id="45049-138">應用程式會使用篩選圖形管理員來建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="45049-138">The application uses the Filter Graph Manager to build a filter graph.</span></span> <span data-ttu-id="45049-139">圖形中的一組確切篩選器將視應用程式而定。</span><span class="sxs-lookup"><span data-stu-id="45049-139">The exact set of filters in the graph will depend on the application.</span></span>
3.  <span data-ttu-id="45049-140">應用程式會使用篩選圖形管理員來控制篩選圖形，並透過篩選來串流資料。</span><span class="sxs-lookup"><span data-stu-id="45049-140">The application uses the Filter Graph Manager to control the filter graph and stream data through the filters.</span></span> <span data-ttu-id="45049-141">在整個過程中，應用程式也會回應篩選圖形管理員的事件。</span><span class="sxs-lookup"><span data-stu-id="45049-141">Throughout this process, the application will also respond to events from the Filter Graph Manager.</span></span>

<span data-ttu-id="45049-142">處理完成時，應用程式會釋放篩選圖形管理員和所有篩選。</span><span class="sxs-lookup"><span data-stu-id="45049-142">When processing is completed, the application releases the Filter Graph Manager and all of the filters.</span></span>

<span data-ttu-id="45049-143">DirectShow 是以 COM 為基礎;篩選圖形管理員和篩選器都是 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="45049-143">DirectShow is based on COM; the Filter Graph Manager and the filters are all COM objects.</span></span> <span data-ttu-id="45049-144">開始程式設計 DirectShow 之前，您應該先對 COM 用戶端程式設計有大致的瞭解。</span><span class="sxs-lookup"><span data-stu-id="45049-144">You should have a general understanding of COM client programming before you begin programming DirectShow.</span></span> <span data-ttu-id="45049-145">有許多關於 COM 程式設計的書籍都可供使用。</span><span class="sxs-lookup"><span data-stu-id="45049-145">Many books about COM programming are available.</span></span>

<span data-ttu-id="45049-146">若要開始使用 DirectShow，請閱讀文章 [如何播放](how-to-play-a-file.md)檔案，該檔案提供簡單的主控台應用程式來播放影片檔案。</span><span class="sxs-lookup"><span data-stu-id="45049-146">To get started with DirectShow, read the article [How To Play a File](how-to-play-a-file.md), which presents a simple console application to play a video file.</span></span> <span data-ttu-id="45049-147">[關於 directshow](about-directshow.md)的章節會更詳細地說明 directshow 架構，而[使用 directshow](using-directshow.md)的區段會檢查 directshow 所支援的主要案例，例如捕捉、影片編輯、DVD 播放和電視。</span><span class="sxs-lookup"><span data-stu-id="45049-147">The section [About DirectShow](about-directshow.md) explains the DirectShow architecture in more detail, while the section [Using DirectShow](using-directshow.md) examines the major scenarios that are supported by DirectShow, such as capture, video editing, DVD playback, and television.</span></span>

 

 



