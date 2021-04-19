---
description: 系統參考時鐘
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: 系統參考時鐘
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987703"
---
# <a name="system-reference-clock"></a><span data-ttu-id="df9b5-103">系統參考時鐘</span><span class="sxs-lookup"><span data-stu-id="df9b5-103">System Reference Clock</span></span>

<span data-ttu-id="df9b5-104">系統參考時鐘物件會執行傳回系統時間的參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="df9b5-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="df9b5-105">如果圖形中沒有任何篩選器提供參考時鐘，則篩選圖形管理員會使用此元件來同步處理圖形。</span><span class="sxs-lookup"><span data-stu-id="df9b5-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="df9b5-106">藉由呼叫 **CoCreateInstance** 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="df9b5-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df9b5-107">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="df9b5-107">Class Identifier</span></span> | <span data-ttu-id="df9b5-108">CLSID \_ SystemClock</span><span class="sxs-lookup"><span data-stu-id="df9b5-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="df9b5-109">介面</span><span class="sxs-lookup"><span data-stu-id="df9b5-109">Interfaces</span></span>       | <span data-ttu-id="df9b5-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)、 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)、 [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="df9b5-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df9b5-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="df9b5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df9b5-112">DirectShow 物件</span><span class="sxs-lookup"><span data-stu-id="df9b5-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="df9b5-113">參考時鐘</span><span class="sxs-lookup"><span data-stu-id="df9b5-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="df9b5-114">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="df9b5-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



