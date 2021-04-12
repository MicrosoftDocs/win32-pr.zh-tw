---
title: '控制項 (COM) '
description: 控制項
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316975"
---
# <a name="controls-com"></a><span data-ttu-id="ce268-103">控制項 (COM) </span><span class="sxs-lookup"><span data-stu-id="ce268-103">Controls (COM)</span></span>

<span data-ttu-id="ce268-104">ActiveX 控制項其實只是 OLE 物件的另一個詞彙，也是更明確的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ce268-104">An ActiveX control is really just another term for OLE object or more specifically, COM object.</span></span> <span data-ttu-id="ce268-105">換句話說，一個控制項至少是一個支援 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面且也可自行註冊的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ce268-105">In other words, a control, at the very least, is some COM object that supports the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface and is also self-registering.</span></span> <span data-ttu-id="ce268-106">透過 [**IUnknown：： QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) ，容器可以管理控制項的存留期，也可以根據可用的介面，以動態方式探索控制項功能的完整範圍。</span><span class="sxs-lookup"><span data-stu-id="ce268-106">Through [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) a container can manage the lifetime of the control as well as dynamically discover the full extent of a control's functionality based on the available interfaces.</span></span> <span data-ttu-id="ce268-107">如此一來，控制項就可以在必要時執行幾乎不需要的功能，而不是支援大量不會執行任何動作的介面。</span><span class="sxs-lookup"><span data-stu-id="ce268-107">This allows a control to implement as little functionality as it needs to, instead of supporting a large number of interfaces that actually don't do anything.</span></span> <span data-ttu-id="ce268-108">簡單來說，這種不超過 **IUnknown** 的基本需求，可讓任何控制項盡可能輕量。</span><span class="sxs-lookup"><span data-stu-id="ce268-108">In short, this minimal requirement for nothing more than **IUnknown** allows any control to be as lightweight as it can.</span></span>

<span data-ttu-id="ce268-109">簡單地說，除了 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 和自我註冊以外，還有其他控制項的需求。</span><span class="sxs-lookup"><span data-stu-id="ce268-109">In short, other than [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and self-registration, there are no other requirements for a control.</span></span> <span data-ttu-id="ce268-110">不過，有一些慣例應該遵循介面的支援，其方式就是由控制項提供給容器的各項功能。</span><span class="sxs-lookup"><span data-stu-id="ce268-110">There are, however, conventions that should be followed about what the support of an interface means in terms of functionality provided to the container by the control.</span></span> <span data-ttu-id="ce268-111">接著，本節會說明控制項實際支援介面的意義，以及控制項在支援方法、屬性和事件時，應提供作為基準的方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="ce268-111">This section then describes what it means for a control to actually support an interface, as well as methods, properties, and events that a control should provide as a baseline if it has occasion to support methods, properties, and events.</span></span>

<span data-ttu-id="ce268-112">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="ce268-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ce268-113">控制項的自我註冊</span><span class="sxs-lookup"><span data-stu-id="ce268-113">Self Registration for Controls</span></span>](self-registration-for-controls.md)
-   [<span data-ttu-id="ce268-114">介面的支援代表</span><span class="sxs-lookup"><span data-stu-id="ce268-114">What Support for an Interface Means</span></span>](what-support-for-an-interface-means.md)
-   [<span data-ttu-id="ce268-115">持續性介面</span><span class="sxs-lookup"><span data-stu-id="ce268-115">Persistence Interfaces</span></span>](persistence-interfaces.md)
-   [<span data-ttu-id="ce268-116">控制項介面中的選擇性方法</span><span class="sxs-lookup"><span data-stu-id="ce268-116">Optional Methods in Control Interfaces</span></span>](optional-methods-in-control-interfaces.md)
-   [<span data-ttu-id="ce268-117">Class Factory 選項</span><span class="sxs-lookup"><span data-stu-id="ce268-117">Class Factory Options</span></span>](class-factory-options.md)
-   [<span data-ttu-id="ce268-118">透過 IDispatch 公開屬性</span><span class="sxs-lookup"><span data-stu-id="ce268-118">Exposing Properties through IDispatch</span></span>](properties.md)
-   [<span data-ttu-id="ce268-119">透過 IDispatch 公開方法</span><span class="sxs-lookup"><span data-stu-id="ce268-119">Exposing Methods through IDispatch</span></span>](exposing-methods-through-idispatch.md)
-   [<span data-ttu-id="ce268-120">控制項中的事件</span><span class="sxs-lookup"><span data-stu-id="ce268-120">Events in Controls</span></span>](events-in-controls.md)
-   [<span data-ttu-id="ce268-121">屬性頁</span><span class="sxs-lookup"><span data-stu-id="ce268-121">Property Pages</span></span>](property-pages.md)
-   [<span data-ttu-id="ce268-122">控制項的環境屬性</span><span class="sxs-lookup"><span data-stu-id="ce268-122">Ambient Properties for Controls</span></span>](ambient-properties-for-controls.md)
-   [<span data-ttu-id="ce268-123">使用容器的功能</span><span class="sxs-lookup"><span data-stu-id="ce268-123">Using the Container's Functionality</span></span>](using-the-container-s-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="ce268-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce268-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce268-125">ActiveX 控制項和控制項容器指導方針</span><span class="sxs-lookup"><span data-stu-id="ce268-125">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




