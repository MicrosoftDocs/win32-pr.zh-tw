---
title: 多執行緒 OpenGL 繪圖策略
description: GDI 不支援多個執行緒。
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- Windows 上的 OpenGL，多執行緒繪圖
- 多執行緒 OpenGL 繪圖 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300631"
---
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="df817-105">多執行緒 OpenGL 繪圖策略</span><span class="sxs-lookup"><span data-stu-id="df817-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="df817-106">GDI 不支援多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="df817-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="df817-107">您必須針對每個執行緒使用不同的裝置內容和不同的轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="df817-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="df817-108">這通常會限制使用多個執行緒搭配執行 OpenGL 應用程式之單一處理器系統的效能優勢。</span><span class="sxs-lookup"><span data-stu-id="df817-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="df817-109">不過，有一些方法可搭配單一處理器系統使用執行緒，以大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="df817-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="df817-110">例如，您可以使用個別的執行緒，將 OpenGL 轉譯呼叫傳遞給專用的立體硬體。</span><span class="sxs-lookup"><span data-stu-id="df817-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="df817-111">對稱式多重處理 (SMP) 系統可大幅受益于使用多個執行緒。</span><span class="sxs-lookup"><span data-stu-id="df817-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="df817-112">最簡單的策略是針對每個處理器使用個別的執行緒，以處理個別視窗中的 OpenGL 轉譯。</span><span class="sxs-lookup"><span data-stu-id="df817-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="df817-113">例如，在飛行模擬應用程式中，您可以使用不同的處理器和執行緒來呈現前端、背面和側邊。</span><span class="sxs-lookup"><span data-stu-id="df817-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="df817-114">執行緒只能有一個目前的現用轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="df817-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="df817-115">當您使用多個執行緒和多個轉譯內容時，必須小心同步處理其使用方式。</span><span class="sxs-lookup"><span data-stu-id="df817-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="df817-116">例如，在所有線程完成繪製之後，只能使用一個執行緒來呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) 。</span><span class="sxs-lookup"><span data-stu-id="df817-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 




