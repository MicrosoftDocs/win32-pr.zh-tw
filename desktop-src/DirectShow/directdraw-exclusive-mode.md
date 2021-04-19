---
description: DirectDraw 獨佔模式
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: DirectDraw 獨佔模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991615"
---
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="d7cd5-103">DirectDraw 獨佔模式</span><span class="sxs-lookup"><span data-stu-id="d7cd5-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="d7cd5-104">本主題僅適用于 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="d7cd5-105">在 VMR-9 中，您可以藉由提供專屬的獨佔模式配置器-展示者來啟用獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="d7cd5-106">如果您使用 [**IVMRSurfaceAllocatorNotify9：： AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) 方法，這會相當簡單。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="d7cd5-107">VMR9Allocator 範例會示範如何執行自訂配置器-展示者。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="d7cd5-108">在 DirectDraw 獨佔模式中，應用程式會獨佔控制圖形硬體。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="d7cd5-109">這對於遊戲等應用程式或可能是全螢幕的影片應用程式很有用。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="d7cd5-110">一般來說，VMR 會建立 DirectDraw 物件，並將合作層級設定為 [一般]。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="d7cd5-111">不過，若要在 DirectDraw 獨佔模式中執行 VMR，應用程式本身必須建立 DirectDraw 物件和主要介面，然後呼叫 **SetCooperativeLevel** 以指定獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="d7cd5-112">VMR 具有特殊的配置器提供者，可讓它在 DirectDraw 獨佔模式中執行。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="d7cd5-113">若要將 VMR 設定為使用此配置器-展示者：</span><span class="sxs-lookup"><span data-stu-id="d7cd5-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="d7cd5-114">使用 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法，建立篩選圖形並將 VMR 新增至其中。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="d7cd5-115">如需程式碼範例，請參閱 [VMR 無視窗模式](vmr-windowless-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="d7cd5-116">建立專屬模式配置器-展示者：</span><span class="sxs-lookup"><span data-stu-id="d7cd5-116">Create the Exclusive Mode allocator-presenter:</span></span>
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  <span data-ttu-id="d7cd5-117">設定新的配置器-展示者：</span><span class="sxs-lookup"><span data-stu-id="d7cd5-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="d7cd5-118">將新的配置器呈現者插入 VMR 中。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="d7cd5-119">以一般方式建立篩選圖形的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="d7cd5-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7cd5-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7cd5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7cd5-121">作業的 VMR 模式</span><span class="sxs-lookup"><span data-stu-id="d7cd5-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 



