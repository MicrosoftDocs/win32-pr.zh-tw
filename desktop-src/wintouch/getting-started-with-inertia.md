---
title: 慣性
description: 本節說明 Windows Touch 的慣性。
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch，慣性
- 慣性，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020933"
---
# <a name="inertia"></a><span data-ttu-id="9819b-105">慣性</span><span class="sxs-lookup"><span data-stu-id="9819b-105">Inertia</span></span>

<span data-ttu-id="9819b-106">本節說明 Windows Touch 的慣性。</span><span class="sxs-lookup"><span data-stu-id="9819b-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="9819b-107">包含在 Windows 7 中的慣性 API，藉由提供簡單的物理模型，在 Windows Touch 應用程式中啟用一致的物件行為。</span><span class="sxs-lookup"><span data-stu-id="9819b-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="9819b-108">您可以使用慣性處理器（封裝功能的類別）來啟用慣性。</span><span class="sxs-lookup"><span data-stu-id="9819b-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="9819b-109">慣性處理器的運作方式，是在物件操作完成時處理傳遞給它的事件，並以與其他應用程式一致的方式處理物件軌跡。</span><span class="sxs-lookup"><span data-stu-id="9819b-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="9819b-110">請注意，慣性處理器與操作處理器緊密結合，以簡化對使用操作的應用程式加入慣性支援。</span><span class="sxs-lookup"><span data-stu-id="9819b-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="9819b-111">事實上，慣性處理器會引發操作處理器所執行的相同事件。</span><span class="sxs-lookup"><span data-stu-id="9819b-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="9819b-112">下一節將說明如何開始使用慣性。</span><span class="sxs-lookup"><span data-stu-id="9819b-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="9819b-113">區段</span><span class="sxs-lookup"><span data-stu-id="9819b-113">Section</span></span>                                                                      | <span data-ttu-id="9819b-114">描述</span><span class="sxs-lookup"><span data-stu-id="9819b-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9819b-115">慣性機制</span><span class="sxs-lookup"><span data-stu-id="9819b-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="9819b-116">說明慣性計算的基本概念。</span><span class="sxs-lookup"><span data-stu-id="9819b-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="9819b-117">處理非受控碼中的慣性</span><span class="sxs-lookup"><span data-stu-id="9819b-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="9819b-118">說明如何使用 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面處理非受控碼中的慣性。</span><span class="sxs-lookup"><span data-stu-id="9819b-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9819b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9819b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9819b-120">操作和慣性</span><span class="sxs-lookup"><span data-stu-id="9819b-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




