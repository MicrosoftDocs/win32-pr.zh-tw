---
title: 計數器、查詢和效能測量
description: 下列各節說明在效能測試和改進（例如查詢、計數器、計時和 predication）中使用的功能。
ms.assetid: C7AEF1A0-36FB-4026-9CCF-ED0206961A58
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf316978f3dd0928692f378dd8d72b8453ad0aae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105057"
---
# <a name="counters-queries-and-performance-measurement"></a><span data-ttu-id="2c372-103">計數器、查詢和效能測量</span><span class="sxs-lookup"><span data-stu-id="2c372-103">Counters, Queries and Performance Measurement</span></span>

<span data-ttu-id="2c372-104">下列各節說明在效能測試和改進（例如查詢、計數器、計時和 predication）中使用的功能。</span><span class="sxs-lookup"><span data-stu-id="2c372-104">The following sections describe features for use in performance testing and improvement, such as queries, counters, timing, and predication.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c372-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="2c372-105">In this section</span></span>



| <span data-ttu-id="2c372-106">主題</span><span class="sxs-lookup"><span data-stu-id="2c372-106">Topic</span></span>                                                                                                 | <span data-ttu-id="2c372-107">描述</span><span class="sxs-lookup"><span data-stu-id="2c372-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c372-108">資料流程-輸出計數器、UAV 計數器、查詢和 Predication</span><span class="sxs-lookup"><span data-stu-id="2c372-108">Stream-Output Counters, UAV Counters, Queries, and Predication</span></span>](counters-and-queries.md)<br/> | <span data-ttu-id="2c372-109">串流輸出和 UAV 計數器會在與 Direct3D 11 類似的方法中，在 Direct3D 12 中運作，不過現在計數器的記憶體必須由應用程式佈建，驅動程式並不會這麼做。</span><span class="sxs-lookup"><span data-stu-id="2c372-109">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="2c372-110">Direct3D 12 中的查詢與 Direct3D 11 中的查詢更加不同，另外還新增了一些程式來移除某些查詢類型的需求。</span><span class="sxs-lookup"><span data-stu-id="2c372-110">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span><br/> |
| [<span data-ttu-id="2c372-111">計時</span><span class="sxs-lookup"><span data-stu-id="2c372-111">Timing</span></span>](timing.md)<br/>                                                                       | <span data-ttu-id="2c372-112">本節涵蓋查詢時間戳記，以及校準 GPU 和 CPU 時間戳計數器。</span><span class="sxs-lookup"><span data-stu-id="2c372-112">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="2c372-113">預測</span><span class="sxs-lookup"><span data-stu-id="2c372-113">Predication</span></span>](predication.md)<br/>                                                             | <span data-ttu-id="2c372-114">Predication 是一項功能，可啟用 GPU 而非 CPU 來決定不繪製、複製或分派物件。</span><span class="sxs-lookup"><span data-stu-id="2c372-114">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span><br/>                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="2c372-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c372-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c372-116">Direct3D 12 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2c372-116">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





