---
description: 翻頁是多媒體、動畫和遊戲軟體的關鍵;這與您可以使用一張紙來進行動畫的方式類似。
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: " (Direct3D 9 的頁面翻轉和後臺緩衝) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107001645"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="34ecf-103"> (Direct3D 9 的頁面翻轉和後臺緩衝) </span><span class="sxs-lookup"><span data-stu-id="34ecf-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="34ecf-104">翻頁是多媒體、動畫和遊戲軟體的關鍵;這與您可以使用一張紙來進行動畫的方式類似。</span><span class="sxs-lookup"><span data-stu-id="34ecf-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="34ecf-105">在每個頁面上，演出者會稍微變更圖，因此當您在工作表之間快速切換時，繪圖就會顯示為動畫。</span><span class="sxs-lookup"><span data-stu-id="34ecf-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="34ecf-106">軟體中的頁面翻轉與此程式類似。</span><span class="sxs-lookup"><span data-stu-id="34ecf-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="34ecf-107">Direct3D 會透過交換鏈（這是裝置的屬性）來實行頁面翻轉功能。</span><span class="sxs-lookup"><span data-stu-id="34ecf-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="34ecf-108">一開始，您可以設定一系列的 Direct3D 緩衝區，以將演出者的紙張翻轉到下一頁。</span><span class="sxs-lookup"><span data-stu-id="34ecf-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="34ecf-109">第一個緩衝區稱為色彩前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="34ecf-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="34ecf-110">它背後的緩衝區稱為回緩衝區。</span><span class="sxs-lookup"><span data-stu-id="34ecf-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="34ecf-111">您的應用程式會寫入背景緩衝區，然後翻轉色彩前端緩衝區，讓背景緩衝區顯示在畫面上。</span><span class="sxs-lookup"><span data-stu-id="34ecf-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="34ecf-112">當系統顯示影像時，您的軟體會再次寫入至背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="34ecf-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="34ecf-113">只要您要製作動畫，程式就會繼續進行，讓您有效率地製作影像動畫。</span><span class="sxs-lookup"><span data-stu-id="34ecf-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="34ecf-114">Direct3D 可讓您輕鬆地設定翻頁的配置，從簡單的雙重緩衝配置 (具有一個背景緩衝區的彩色前端緩衝區) 到更複雜的配置，還有額外的背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="34ecf-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34ecf-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="34ecf-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34ecf-116">Direct3D 表面</span><span class="sxs-lookup"><span data-stu-id="34ecf-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="34ecf-117">什麼是交換鏈？ (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="34ecf-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



