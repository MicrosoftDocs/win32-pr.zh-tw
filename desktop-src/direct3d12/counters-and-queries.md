---
title: 計數器、查詢和 predication
description: 串流輸出和 UAV 計數器會在與 Direct3D 11 類似的方法中，在 Direct3D 12 中運作，不過現在計數器的記憶體必須由應用程式佈建，驅動程式並不會這麼做。
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548450"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="3e2b0-103">計數器、查詢和 predication</span><span class="sxs-lookup"><span data-stu-id="3e2b0-103">Counters, queries, and predication</span></span>

<span data-ttu-id="3e2b0-104">本主題涵蓋資料流程輸出計數器、UAV 計數器、查詢和 predication。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="3e2b0-105">串流輸出和 UAV 計數器會在與 Direct3D 11 類似的方法中，在 Direct3D 12 中運作，不過現在計數器的記憶體必須由應用程式佈建，驅動程式並不會這麼做。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="3e2b0-106">Direct3D 12 中的查詢與 Direct3D 11 中的查詢更加不同，另外還新增了一些程式來移除某些查詢類型的需求。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e2b0-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="3e2b0-107">In this section</span></span>



| <span data-ttu-id="3e2b0-108">主題</span><span class="sxs-lookup"><span data-stu-id="3e2b0-108">Topic</span></span>                                                           | <span data-ttu-id="3e2b0-109">描述</span><span class="sxs-lookup"><span data-stu-id="3e2b0-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e2b0-110">串流輸出計數器</span><span class="sxs-lookup"><span data-stu-id="3e2b0-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="3e2b0-111">資料流程輸出是 GPU 將頂點寫入緩衝區的能力。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="3e2b0-112">資料流程輸出計數器會監視進度。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="3e2b0-113">UAV 計數器</span><span class="sxs-lookup"><span data-stu-id="3e2b0-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="3e2b0-114">UAV 計數器可以用來將32位不可部分完成的計數器與未排序的存取權 (UAV) 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="3e2b0-115">查詢</span><span class="sxs-lookup"><span data-stu-id="3e2b0-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="3e2b0-116">在 Direct3D 12 中，查詢會分組為稱為查詢堆積的查詢陣列。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="3e2b0-117">查詢堆積有一種類型，可定義可搭配該堆積使用的有效查詢類型。</span><span class="sxs-lookup"><span data-stu-id="3e2b0-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3e2b0-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e2b0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e2b0-119">效能測量</span><span class="sxs-lookup"><span data-stu-id="3e2b0-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





