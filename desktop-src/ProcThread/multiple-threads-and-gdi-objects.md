---
description: 為了增強效能，圖形裝置介面 (GDI) 物件 (例如，調色板、裝置內容、區域和類似的) 都不會序列化。
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: 多執行緒和 GDI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985448"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="3a133-103">多執行緒和 GDI 物件</span><span class="sxs-lookup"><span data-stu-id="3a133-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="3a133-104">為了增強效能，圖形裝置介面 (GDI) 物件 (例如，調色板、裝置內容、區域和類似的) 都不會序列化。</span><span class="sxs-lookup"><span data-stu-id="3a133-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="3a133-105">如果有多個執行緒共用這些物件的進程，這會造成潛在的危險。</span><span class="sxs-lookup"><span data-stu-id="3a133-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="3a133-106">例如，如果某個執行緒在另一個執行緒正在使用 GDI 物件時刪除該物件，則結果為無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="3a133-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="3a133-107">您可以避免這種危險，只是不共用 GDI 物件。</span><span class="sxs-lookup"><span data-stu-id="3a133-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="3a133-108">如果無法避免共用 (或希望) ，應用程式必須提供自己的機制來同步存取。</span><span class="sxs-lookup"><span data-stu-id="3a133-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="3a133-109">如需同步處理存取的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。</span><span class="sxs-lookup"><span data-stu-id="3a133-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



