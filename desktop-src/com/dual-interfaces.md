---
title: COM)  (的雙重介面
description: 雙重介面
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024204"
---
# <a name="dual-interfaces"></a><span data-ttu-id="efe4f-103">雙重介面</span><span class="sxs-lookup"><span data-stu-id="efe4f-103">Dual Interfaces</span></span>

<span data-ttu-id="efe4f-104">OLE Automation 可讓物件以兩種方式公開一組方法：透過 **IDispatch** 介面，以及透過直接的 OLE VTable 系結。</span><span class="sxs-lookup"><span data-stu-id="efe4f-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="efe4f-105">目前提供的大部分工具都使用 **IDispatch** ，並提供屬性和方法晚期繫結的支援。</span><span class="sxs-lookup"><span data-stu-id="efe4f-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="efe4f-106">VTable 系結會提供更高的效能，因為這種方法是直接呼叫，而不是透過 **IDispatch：： Invoke** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="efe4f-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="efe4f-107">**IDispatch** 提供晚期繫結支援，其中直接 VTable 系結可提供顯著的效能提升。這兩種技術在不同的情況下都很重要，而且很重要。</span><span class="sxs-lookup"><span data-stu-id="efe4f-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="efe4f-108">藉由將介面標記為 \[ [](/windows/desktop/Midl/dual) \] 類型程式庫中的雙重介面，可以透過 **IDispatch** 使用 OLE Automation 介面，也可以直接系結至該介面。</span><span class="sxs-lookup"><span data-stu-id="efe4f-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="efe4f-109">因此，容器可以選擇最適當的技巧。</span><span class="sxs-lookup"><span data-stu-id="efe4f-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="efe4f-110">強烈建議針對控制項和容器使用雙重介面。</span><span class="sxs-lookup"><span data-stu-id="efe4f-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 