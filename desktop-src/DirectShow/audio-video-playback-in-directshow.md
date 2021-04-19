---
description: 本教學課程說明如何撰寫可播放媒體檔案的 DirectShow 應用程式。
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: 在 DirectShow 播放音訊/影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973543"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="212ba-103">在 DirectShow 播放音訊/影片</span><span class="sxs-lookup"><span data-stu-id="212ba-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="212ba-104">本教學課程說明如何撰寫可播放媒體檔案的 DirectShow 應用程式。</span><span class="sxs-lookup"><span data-stu-id="212ba-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="212ba-105">閱讀本教學課程之前，您可能想要閱讀下列主題：</span><span class="sxs-lookup"><span data-stu-id="212ba-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="212ba-106">DirectShow 應用程式程式設計簡介</span><span class="sxs-lookup"><span data-stu-id="212ba-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="212ba-107">如何播放檔案</span><span class="sxs-lookup"><span data-stu-id="212ba-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="212ba-108">關於 DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="212ba-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="212ba-109">關於篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="212ba-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="212ba-110">本節內容</span><span class="sxs-lookup"><span data-stu-id="212ba-110">In this section</span></span>

-   [<span data-ttu-id="212ba-111">步驟1：宣告 DShowPlayer 類別</span><span class="sxs-lookup"><span data-stu-id="212ba-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="212ba-112">步驟2：宣告 CVideoRenderer 和衍生類別</span><span class="sxs-lookup"><span data-stu-id="212ba-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="212ba-113">步驟3：建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="212ba-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="212ba-114">步驟4：新增影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="212ba-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="212ba-115">步驟5：新增影片功能</span><span class="sxs-lookup"><span data-stu-id="212ba-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="212ba-116">步驟6：處理圖形事件</span><span class="sxs-lookup"><span data-stu-id="212ba-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="212ba-117">步驟7：傳輸控制項</span><span class="sxs-lookup"><span data-stu-id="212ba-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="212ba-118">DirectShow 播放範例</span><span class="sxs-lookup"><span data-stu-id="212ba-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="212ba-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="212ba-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="212ba-120">使用 DirectShow</span><span class="sxs-lookup"><span data-stu-id="212ba-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



