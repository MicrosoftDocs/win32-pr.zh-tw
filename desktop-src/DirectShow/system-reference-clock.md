---
description: 系統參考時鐘
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: 系統參考時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909486"
---
# <a name="system-reference-clock"></a><span data-ttu-id="ca6a2-103">系統參考時鐘</span><span class="sxs-lookup"><span data-stu-id="ca6a2-103">System Reference Clock</span></span>

<span data-ttu-id="ca6a2-104">系統參考時鐘物件會執行傳回系統時間的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="ca6a2-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="ca6a2-105">如果圖形中沒有任何篩選器提供參考時鐘，則篩選圖形管理員會使用此元件來同步處理圖形。</span><span class="sxs-lookup"><span data-stu-id="ca6a2-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="ca6a2-106">藉由呼叫 **CoCreateInstance** 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="ca6a2-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="ca6a2-107">標籤</span><span class="sxs-lookup"><span data-stu-id="ca6a2-107">Label</span></span> | <span data-ttu-id="ca6a2-108">值</span><span class="sxs-lookup"><span data-stu-id="ca6a2-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca6a2-109">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="ca6a2-109">Class Identifier</span></span> | <span data-ttu-id="ca6a2-110">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="ca6a2-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="ca6a2-111">介面</span><span class="sxs-lookup"><span data-stu-id="ca6a2-111">Interfaces</span></span>       | <span data-ttu-id="ca6a2-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)、 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)、 [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="ca6a2-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ca6a2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca6a2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca6a2-114">DirectShow 物件</span><span class="sxs-lookup"><span data-stu-id="ca6a2-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="ca6a2-115">參考時鐘</span><span class="sxs-lookup"><span data-stu-id="ca6a2-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="ca6a2-116">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="ca6a2-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



