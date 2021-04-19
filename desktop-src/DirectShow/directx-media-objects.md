---
description: DirectX 媒體物件
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: DirectX 媒體物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "107001775"
---
# <a name="directx-media-objects"></a><span data-ttu-id="bb8d7-103">DirectX 媒體物件</span><span class="sxs-lookup"><span data-stu-id="bb8d7-103">DirectX Media Objects</span></span>

> [!Note]  
> <span data-ttu-id="bb8d7-104">DMOs 已被 [媒體基礎轉換](/windows/desktop/medfound/media-foundation-transforms) (MFTs) 取代。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-104">DMOs have been superseded by [Media Foundation Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs).</span></span> <span data-ttu-id="bb8d7-105">仍支援 SQL-DMO 介面。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-105">The DMO interfaces are still supported.</span></span> <span data-ttu-id="bb8d7-106">但是，如果您要撰寫自訂編解碼器或音訊/視頻處理外掛程式，您應該考慮將它實作為 MFT。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-106">However, if you are writing a custom codec or audio/video processing plug-in, you should consider implementing it as an MFT.</span></span>

 

<span data-ttu-id="bb8d7-107"> (DMOs) 的 DirectX 媒體物件是以 COM 為基礎的資料串流元件。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-107">DirectX Media Objects (DMOs) are COM-based data-streaming components.</span></span> <span data-ttu-id="bb8d7-108">在某些方面，DMOs 類似于 Microsoft DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-108">In some respects, DMOs are similar to Microsoft DirectShow filters.</span></span> <span data-ttu-id="bb8d7-109">就像 DirectShow 篩選器一樣，DMOs 會取得輸入資料並使用它來產生輸出資料。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-109">Like DirectShow filters, DMOs take input data and use it to produce output data.</span></span> <span data-ttu-id="bb8d7-110">不過， (Api) 的應用程式開發介面，比適用于 DirectShow 的相對應 Api 簡單得多。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-110">However, the application programming interfaces (APIs) for DMOs are much simpler than the corresponding APIs for DirectShow.</span></span> <span data-ttu-id="bb8d7-111">因此，DMOs 比較容易建立、測試和使用。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-111">As a result, DMOs are easier to create, test, and use.</span></span> <span data-ttu-id="bb8d7-112">DMOs 可用於許多案例：</span><span class="sxs-lookup"><span data-stu-id="bb8d7-112">DMOs can be used in many scenarios:</span></span>

-   <span data-ttu-id="bb8d7-113">以 DirectShow 為基礎的應用程式可以使用 DMOs，透過稱為「的 DirectShow [包裝](dmo-wrapper-filter.md) 函式」篩選器。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-113">Applications based on DirectShow can use DMOs through a DirectShow filter called the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="bb8d7-114">篩選和 DMOs 之間的差異對應用程式而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-114">The distinction between filters and DMOs is transparent to the application.</span></span> <span data-ttu-id="bb8d7-115">應用程式不會直接呼叫 SQL-DMO Api。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-115">The application does not directly call the DMO APIs.</span></span>
-   <span data-ttu-id="bb8d7-116">以 Microsoft DirectSound 為基礎的應用程式可以使用 [音訊效果 DMOs]。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-116">Applications based on Microsoft DirectSound can use audio effect DMOs.</span></span> <span data-ttu-id="bb8d7-117">同樣地，較高層級的 DirectSound Api 會將應用程式防護為低層級的 SQL-DMO Api。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-117">Again, the application is shielded from the low-level DMO APIs by the higher-level DirectSound APIs.</span></span>
-   <span data-ttu-id="bb8d7-118">應用程式可以直接使用 DMOs。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-118">Applications can use DMOs directly.</span></span>

<span data-ttu-id="bb8d7-119">因此，藉由撰寫一組，您可以建立可在各種應用程式中使用的元件。</span><span class="sxs-lookup"><span data-stu-id="bb8d7-119">Thus, by writing a DMO, you create a component that can be used in a wide range of applications.</span></span> <span data-ttu-id="bb8d7-120">本檔包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="bb8d7-120">This documentation contains the following sections:</span></span>

-   [<span data-ttu-id="bb8d7-121">關於 DMOs</span><span class="sxs-lookup"><span data-stu-id="bb8d7-121">About DMOs</span></span>](about-dmos.md)
-   [<span data-ttu-id="bb8d7-122">使用 DMOs</span><span class="sxs-lookup"><span data-stu-id="bb8d7-122">Using DMOs</span></span>](using-dmos.md)
-   [<span data-ttu-id="bb8d7-123">撰寫 SQL-DMO</span><span class="sxs-lookup"><span data-stu-id="bb8d7-123">Writing a DMO</span></span>](writing-a-dmo.md)
-   [<span data-ttu-id="bb8d7-124">媒體參數</span><span class="sxs-lookup"><span data-stu-id="bb8d7-124">Media Parameters</span></span>](media-parameters.md)
-   [<span data-ttu-id="bb8d7-125">SQL-DMO 參考</span><span class="sxs-lookup"><span data-stu-id="bb8d7-125">DMO Reference</span></span>](dmo-reference.md)

## <a name="related-topics"></a><span data-ttu-id="bb8d7-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb8d7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8d7-127">DirectShow</span><span class="sxs-lookup"><span data-stu-id="bb8d7-127">DirectShow</span></span>](directshow.md)
</dt> </dl>

 

 
