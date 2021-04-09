---
description: 直接裝載
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: 直接裝載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688507"
---
# <a name="directly-hosting-a-dmo"></a><span data-ttu-id="3d2b7-103">直接裝載</span><span class="sxs-lookup"><span data-stu-id="3d2b7-103">Directly Hosting a DMO</span></span>

<span data-ttu-id="3d2b7-104">本章節描述應用程式如何做為 a 的直接用戶端。</span><span class="sxs-lookup"><span data-stu-id="3d2b7-104">This section describes how an application can act as the direct client of a DMO.</span></span> <span data-ttu-id="3d2b7-105">應用程式會將輸入傳遞給 SQL-DMO，而是會建立輸出，而應用程式會使用輸出來呈現、進一步處理或其他任何東西。</span><span class="sxs-lookup"><span data-stu-id="3d2b7-105">The application delivers input to the DMO, the DMO creates output, and the application uses the output for rendering, further processing, or anything else.</span></span> <span data-ttu-id="3d2b7-106">應用程式會負責問題，例如記憶體配置、時間和同步處理，以及執行緒。</span><span class="sxs-lookup"><span data-stu-id="3d2b7-106">The application is responsible for issues such as memory allocation, timing and synchronization, and threading.</span></span> <span data-ttu-id="3d2b7-107">這些需求會視應用程式的本質而定。</span><span class="sxs-lookup"><span data-stu-id="3d2b7-107">These requirements will depend on the nature of the application.</span></span>

<span data-ttu-id="3d2b7-108">如果您要撰寫的元件是應用程式和 (SQL-DMO 之間的層級（例如，裝載 SQL-DMO) 的 ActiveX 控制項），本節中的資訊也適用。</span><span class="sxs-lookup"><span data-stu-id="3d2b7-108">The information in this section also applies if you are writing a component that acts as a layer between an application and a DMO (for example, an ActiveX Control that hosts a DMO).</span></span> <span data-ttu-id="3d2b7-109">此外，如果您要撰寫一節，請閱讀本節，因為它描述了您的</span><span class="sxs-lookup"><span data-stu-id="3d2b7-109">In addition, you should read this section if you are writing a DMO, because it describes the functionality that your DMO must implement.</span></span>

<span data-ttu-id="3d2b7-110">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="3d2b7-110">This section contains the following topics:</span></span>

-   [<span data-ttu-id="3d2b7-111">設定中的媒體類型</span><span class="sxs-lookup"><span data-stu-id="3d2b7-111">Setting Media Types on a DMO</span></span>](setting-media-types-on-a-dmo.md)
-   [<span data-ttu-id="3d2b7-112">處理 SQL-DMO 中的資料</span><span class="sxs-lookup"><span data-stu-id="3d2b7-112">Processing Data in a DMO</span></span>](processing-data-in-a-dmo.md)
-   [<span data-ttu-id="3d2b7-113">就地處理</span><span class="sxs-lookup"><span data-stu-id="3d2b7-113">In-Place Processing</span></span>](in-place-processing.md)
-   [<span data-ttu-id="3d2b7-114">選用資料流程</span><span class="sxs-lookup"><span data-stu-id="3d2b7-114">Optional Streams</span></span>](optional-streams.md)
-   [<span data-ttu-id="3d2b7-115">執行 IMediaBuffer</span><span class="sxs-lookup"><span data-stu-id="3d2b7-115">Implementing IMediaBuffer</span></span>](implementing-imediabuffer.md)

## <a name="related-topics"></a><span data-ttu-id="3d2b7-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d2b7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d2b7-117">使用 DMOs</span><span class="sxs-lookup"><span data-stu-id="3d2b7-117">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



