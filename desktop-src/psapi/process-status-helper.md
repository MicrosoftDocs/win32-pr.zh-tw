---
title: 進程狀態 API
description: 取得處理常式、模組 (可執行檔或 Dll) 和設備磁碟機的相關資訊。 收集記憶體使用量資料。 取得實際對應至進程內容的記憶體數量快照集。
ms.assetid: 512c3f0f-b1b5-43a0-9460-eb668315d6f4
keywords:
- 進程狀態 API
- 進程狀態協助程式
- PSAPI.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a2234ee53acda22df6b6be6267815ba68090be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023949"
---
# <a name="process-status-api"></a><span data-ttu-id="08b8b-108">進程狀態 API</span><span class="sxs-lookup"><span data-stu-id="08b8b-108">Process Status API</span></span>

<span data-ttu-id="08b8b-109">進程狀態應用程式開發介面 (PSAPI.DLL) 是協助程式程式庫，可讓您更輕鬆地取得處理常式和設備磁碟機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08b8b-109">The process status application programming interface (PSAPI) is a helper library that makes it easier for you to obtain information about processes and device drivers.</span></span> <span data-ttu-id="08b8b-110">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="08b8b-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="08b8b-111">關於 PSAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="08b8b-111">About PSAPI</span></span>](about-psapi.md)
-   [<span data-ttu-id="08b8b-112">使用 PSAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="08b8b-112">Using PSAPI</span></span>](using-psapi.md)
-   [<span data-ttu-id="08b8b-113">PSAPI.DLL 參考</span><span class="sxs-lookup"><span data-stu-id="08b8b-113">PSAPI Reference</span></span>](psapi-reference.md)

<span data-ttu-id="08b8b-114">這些函數可在 Psapi.dll 中取得。</span><span class="sxs-lookup"><span data-stu-id="08b8b-114">These functions are available in Psapi.dll.</span></span>

<span data-ttu-id="08b8b-115">相同的資訊通常可透過登錄中的效能資料取得。</span><span class="sxs-lookup"><span data-stu-id="08b8b-115">The same information is generally available through the performance data in the registry.</span></span> <span data-ttu-id="08b8b-116">如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="08b8b-116">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

 

 