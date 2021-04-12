---
title: 公開自訂消費者介面元素的快捷方式
description: 本章節描述應用程式開發人員可用來公開特定種類之自訂使用者介面專案的快捷方式。
ms.assetid: 024e1bfd-8cc2-4839-82ae-bd05dfec6449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f5fe1943f6a7b6a44bef2e9243d1da6d55f970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372505"
---
# <a name="shortcuts-for-exposing-custom-user-interface-elements"></a><span data-ttu-id="ce022-103">公開自訂消費者介面元素的快捷方式</span><span class="sxs-lookup"><span data-stu-id="ce022-103">Shortcuts for Exposing Custom User Interface Elements</span></span>

<span data-ttu-id="ce022-104">本章節描述應用程式開發人員可用來公開特定種類之自訂使用者介面專案的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ce022-104">This section describes shortcuts that application developers can use to expose certain kinds of custom user interface elements.</span></span> <span data-ttu-id="ce022-105">本節所述的技巧可簡化 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的執行，或提供替代方式來公開資訊，而不需執行 **IAccessible**。</span><span class="sxs-lookup"><span data-stu-id="ce022-105">The techniques described in this section either simplify the implementation of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface, or provide an alternative to exposing information without implementing **IAccessible**.</span></span>

> [!Note]  
> <span data-ttu-id="ce022-106">在嘗試本節所述的技術之前，您應該考慮使用某種形式的動態注釋 (直接、值對應或伺服器) 。</span><span class="sxs-lookup"><span data-stu-id="ce022-106">You should consider using some form of Dynamic Annotation (Direct, Value Map, or Server) before attempting the techniques described in this section.</span></span> <span data-ttu-id="ce022-107">如需詳細資訊，請參閱 [動態批註 API](dynamic-annotation-api.md)。</span><span class="sxs-lookup"><span data-stu-id="ce022-107">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="ce022-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="ce022-108">In this section</span></span>

-   [<span data-ttu-id="ce022-109">根據系統控制項公開控制項</span><span class="sxs-lookup"><span data-stu-id="ce022-109">Exposing Controls Based on System Controls</span></span>](exposing-controls-based-on-system-controls.md)
-   [<span data-ttu-id="ce022-110">Owner-Drawn 控制項加上標籤</span><span class="sxs-lookup"><span data-stu-id="ce022-110">Labeling Owner-Drawn Controls</span></span>](labeling-owner-drawn-controls.md)

 

 




