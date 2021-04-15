---
title: 保留模式與立即模式
description: 圖形 Api 可以分為保留模式 Api 和立即模式 Api。
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104556319"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="32345-103">保留模式與立即模式</span><span class="sxs-lookup"><span data-stu-id="32345-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="32345-104">圖形 Api 可以分為 *保留模式* api 和 *立即模式* api。</span><span class="sxs-lookup"><span data-stu-id="32345-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="32345-105">Direct2D 是立即模式的 API。</span><span class="sxs-lookup"><span data-stu-id="32345-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="32345-106">Windows Presentation Foundation (WPF) 是保留模式 API 的範例。</span><span class="sxs-lookup"><span data-stu-id="32345-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="32345-107">保留模式 API 是宣告式。</span><span class="sxs-lookup"><span data-stu-id="32345-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="32345-108">應用程式會從圖形基本專案（例如圖形和線條）來建立場景。</span><span class="sxs-lookup"><span data-stu-id="32345-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="32345-109">圖形程式庫會將場景的模型儲存在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="32345-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="32345-110">為了繪製框架，圖形程式庫會將場景轉換成一組繪圖命令。</span><span class="sxs-lookup"><span data-stu-id="32345-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="32345-111">在框架之間，圖形程式庫會將場景保留在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="32345-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="32345-112">為了變更轉譯的內容，應用程式會發出命令以更新場景，例如，加入或移除圖形。</span><span class="sxs-lookup"><span data-stu-id="32345-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="32345-113">然後，程式庫會負責重繪場景。</span><span class="sxs-lookup"><span data-stu-id="32345-113">The library is then responsible for redrawing the scene.</span></span>

![顯示保留模式圖形的圖表。](images/graphics06.png)

<span data-ttu-id="32345-115">立即模式 API 是程式性的。</span><span class="sxs-lookup"><span data-stu-id="32345-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="32345-116">每次繪製新的框架時，應用程式就會直接發出繪製命令。</span><span class="sxs-lookup"><span data-stu-id="32345-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="32345-117">圖形程式庫不會在畫面格之間儲存場景模型。</span><span class="sxs-lookup"><span data-stu-id="32345-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="32345-118">相反地，應用程式會持續追蹤場景。</span><span class="sxs-lookup"><span data-stu-id="32345-118">Instead, the application keeps track of the scene.</span></span>

![顯示立即模式圖形的圖表。](images/graphics07.png)

<span data-ttu-id="32345-120">保留模式 Api 可能更容易使用，因為 API 會為您執行更多工作，例如初始化、狀態維護和清除。</span><span class="sxs-lookup"><span data-stu-id="32345-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="32345-121">另一方面，它們通常較不具彈性，因為 API 會有自己的場景模型。</span><span class="sxs-lookup"><span data-stu-id="32345-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="32345-122">此外，保留模式 API 可能具有較高的記憶體需求，因為它需要提供一般用途的場景模型。</span><span class="sxs-lookup"><span data-stu-id="32345-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="32345-123">使用立即模式 API，您可以執行目標優化。</span><span class="sxs-lookup"><span data-stu-id="32345-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="32345-124">下一個</span><span class="sxs-lookup"><span data-stu-id="32345-124">Next</span></span>

[<span data-ttu-id="32345-125">您的第一個 Direct2D 計畫</span><span class="sxs-lookup"><span data-stu-id="32345-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 




