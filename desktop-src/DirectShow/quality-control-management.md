---
description: Quality-Control 管理
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control 管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971090"
---
# <a name="quality-control-management"></a><span data-ttu-id="17bb9-103">Quality-Control 管理</span><span class="sxs-lookup"><span data-stu-id="17bb9-103">Quality-Control Management</span></span>

<span data-ttu-id="17bb9-104">品質控制是一種機制，可透過篩選圖形來調整資料流程的速率，以回應執行時間效能。</span><span class="sxs-lookup"><span data-stu-id="17bb9-104">Quality control is a mechanism for adjusting the rate of data flow through the filter graph in response to run-time performance.</span></span> <span data-ttu-id="17bb9-105">如果轉譯器篩選器收到太多資料或太少資料，它可能會傳送 *品質訊息*。</span><span class="sxs-lookup"><span data-stu-id="17bb9-105">If a renderer filter is receiving too much data or too little data, it can send a *quality message*.</span></span> <span data-ttu-id="17bb9-106">品質訊息會要求資料速率的調整。</span><span class="sxs-lookup"><span data-stu-id="17bb9-106">The quality message requests an adjustment in the data rate.</span></span> <span data-ttu-id="17bb9-107">根據預設，品質訊息會從轉譯器行進上游，直到到達可回應 (（如果有任何) ）的篩選器為止。</span><span class="sxs-lookup"><span data-stu-id="17bb9-107">By default, quality messages travel upstream from the renderer until they reach a filter that can respond (if any).</span></span> <span data-ttu-id="17bb9-108">應用程式也可以執行自訂的品質管制員。</span><span class="sxs-lookup"><span data-stu-id="17bb9-108">An application can also implement a custom quality manager.</span></span> <span data-ttu-id="17bb9-109">在此情況下，轉譯器會將品質訊息直接傳遞至應用程式的品質管制員。</span><span class="sxs-lookup"><span data-stu-id="17bb9-109">In that case, the renderer passes quality messages directly to the application's quality manager.</span></span>

<span data-ttu-id="17bb9-110">本文包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="17bb9-110">This article contains the following topics.</span></span>

-   [<span data-ttu-id="17bb9-111">品質訊息</span><span class="sxs-lookup"><span data-stu-id="17bb9-111">Quality Messages</span></span>](quality-messages.md)
-   [<span data-ttu-id="17bb9-112">預設品質控制項</span><span class="sxs-lookup"><span data-stu-id="17bb9-112">Default Quality Control</span></span>](default-quality-control.md)

## <a name="related-topics"></a><span data-ttu-id="17bb9-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="17bb9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17bb9-114">篩選開發人員的資料流程</span><span class="sxs-lookup"><span data-stu-id="17bb9-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="17bb9-115">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="17bb9-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



