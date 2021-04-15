---
description: 提供 VMR-7 的自訂 Allocator-Presenter
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: 提供 VMR-7 的自訂 Allocator-Presenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554893"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a><span data-ttu-id="7cc0d-103">提供 VMR-7 的自訂 Allocator-Presenter</span><span class="sxs-lookup"><span data-stu-id="7cc0d-103">Supplying a Custom Allocator-Presenter for VMR-7</span></span>

<span data-ttu-id="7cc0d-104">配置器-展示者負責配置 DirectDraw 表面，並呈現影片框架以供轉譯。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-104">The allocator-presenter is responsible for allocating DirectDraw surfaces and presenting the video frames for rendering.</span></span> <span data-ttu-id="7cc0d-105">在大部分的案例中，預設配置器的功能會比應用程式的需求還多。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-105">In the vast majority of scenarios, the functionality of the default allocator-presenter will be more than sufficient for an application's needs.</span></span> <span data-ttu-id="7cc0d-106">但是，藉由插入自訂配置器提供者，應用程式可以直接存取影片位，並且完全控制轉譯流程。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-106">But by plugging in a custom allocator-presenter, an application can obtain direct access to the video bits and completely control the rendering process.</span></span> <span data-ttu-id="7cc0d-107">這項增強功能的代價是，應用程式必須處理額外的 DirectDraw 介面管理複雜性。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-107">The trade-off for this increased power is that the application must handle the added complexity of DirectDraw surface management.</span></span>

![使用自訂配置器-展示者](images/custom-ap.png)

<span data-ttu-id="7cc0d-109">上圖顯示 VMR 和配置器展示者所使用的通訊介面。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-109">The preceding figure shows the communication interfaces used by the VMR and the allocator-presenter.</span></span> <span data-ttu-id="7cc0d-110">覆寫所有預設配置和呈現功能的自訂配置器呈現者，必須執行 [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) 和 [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) 介面，也可以選擇 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-110">A custom allocator-presenter that overrides all of the default allocation and presentation functionality must implement the [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) and [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) interfaces, and optionally, [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol).</span></span>

<span data-ttu-id="7cc0d-111">為了取代預設配置器-展示者，應用程式會呼叫 [**IVMRSurfaceAllocatorNotify：： AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) 方法，並將指標傳遞給新的配置器-展示者。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-111">To replace the default allocator-presenter, an application calls the [**IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) method and passes in a pointer to the new allocator-presenter.</span></span> <span data-ttu-id="7cc0d-112">為了回應此呼叫，VMR 會呼叫配置器展示者的 [**IVMRSurfaceAllocator：： AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) 方法，以提供 VMR 的 [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-112">In response to this call, the VMR will call the allocator-presenter's [**IVMRSurfaceAllocator::AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) method to provide the pointer to the VMR's [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) interface.</span></span> <span data-ttu-id="7cc0d-113">配置器呈現者在使用 [**IVMRSurfaceAllocatorNotify：： NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) 方法將事件傳遞給 VMR 時，會使用這個介面指標。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-113">The allocator-presenter will use this interface pointer when passing events to the VMR with the [**IVMRSurfaceAllocatorNotify::NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) method.</span></span>

<span data-ttu-id="7cc0d-114">作為替代方案，應用程式可以使用它自己的配置器展示者和預設配置器-展示者。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-114">As an alternate solution, an application can use both its own allocator-presenter and the default allocator-presenter.</span></span> <span data-ttu-id="7cc0d-115">在此案例中，自訂配置器展示者只會處理需要自訂功能的呼叫，並將其餘的呼叫從 VMR 傳遞至預設配置器-展示者。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-115">In this scenario, the custom allocator-presenter handles only those calls where custom functionality is needed, and passes the rest of the calls from the VMR through to the default allocator-presenter.</span></span> <span data-ttu-id="7cc0d-116">在許多情況下，只需要覆寫 [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) 介面。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-116">In many cases, it is only necessary to override the [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) interface.</span></span>

![使用兩個配置器-展示者](images/custom-ap2.png)

<span data-ttu-id="7cc0d-118">若要同時使用自訂配置器提供者和預設配置器-展示者，應用程式會先呼叫 [**IVMRSurfaceAllocatorNotify：： AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) ，以提供指向新配置器的指標。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-118">To use both a custom allocator-presenter and the default allocator-presenter, an application would first call [**IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) to provide a pointer to the new allocator-presenter.</span></span> <span data-ttu-id="7cc0d-119">這會導致預設配置器-展示者終結，因此應用程式必須在 VMR 上呼叫 **QueryInterface** 並要求 [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) 介面，以建立另一個實例。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-119">This causes the default allocator-presenter to be destroyed, so the application must create another instance of it by calling **QueryInterface** on the VMR and requesting the [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) interface.</span></span> <span data-ttu-id="7cc0d-120">如上圖所示，自訂配置器呈現者會覆寫 [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) 介面方法，並只會將 **IVMRSurfaceAllocator** 介面的所有呼叫都傳遞至預設的實值。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-120">As shown in the preceding figure, the custom allocator-presenter overrides the [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) interface methods, and simply passes all calls to the **IVMRSurfaceAllocator** interface through to the default implementation.</span></span> <span data-ttu-id="7cc0d-121">此圖也會顯示在配置器上執行的 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="7cc0d-121">The figure also shows the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface as being implemented on the allocator-presenter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cc0d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="7cc0d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc0d-123">提供 VMR-9 的自訂 Allocator-Presenter</span><span class="sxs-lookup"><span data-stu-id="7cc0d-123">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[<span data-ttu-id="7cc0d-124">VMR Renderless 播放模式 (自訂配置器-展示者) </span><span class="sxs-lookup"><span data-stu-id="7cc0d-124">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



