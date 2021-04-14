---
title: 管理記憶體配置
description: 管理記憶體配置
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383010"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="9d6ae-103">管理記憶體配置</span><span class="sxs-lookup"><span data-stu-id="9d6ae-103">Managing Memory Allocation</span></span>

<span data-ttu-id="9d6ae-104">在 COM 中，許多（如果不是大多數）介面方法是由一個程式設計組織所撰寫，並由另一個程式碼所撰寫的程式碼所呼叫。</span><span class="sxs-lookup"><span data-stu-id="9d6ae-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="9d6ae-105">這些函式的許多參數和傳回值都是可透過傳值方式傳遞的類型。</span><span class="sxs-lookup"><span data-stu-id="9d6ae-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="9d6ae-106">不過，有時候必須傳遞資料結構，而不是這種情況，因此呼叫端和呼叫都必須有相容的配置和取消配置原則。</span><span class="sxs-lookup"><span data-stu-id="9d6ae-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="9d6ae-107">COM 會定義記憶體配置的通用慣例，因為它比定義個案規則更合理，因此 COM 遠端程序呼叫的執行可以正確地管理記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d6ae-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="9d6ae-108">COM 介面的方法一律會藉由呼叫 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)介面中找到的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)函式，來提供介面指標的記憶體管理，而所有其他 COM 介面都會從該介面衍生。</span><span class="sxs-lookup"><span data-stu-id="9d6ae-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="9d6ae-109"> (參閱 [管理參考計數的規則](rules-for-managing-reference-counts.md) ，以取得詳細資訊。 ) </span><span class="sxs-lookup"><span data-stu-id="9d6ae-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="9d6ae-110">本節只會說明如何針對未以傳值方式傳遞的參數配置記憶體（不是介面指標），還會描述更常見的專案，例如字串、結構指標等等。</span><span class="sxs-lookup"><span data-stu-id="9d6ae-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="9d6ae-111">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="9d6ae-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9d6ae-112">OLE 記憶體配置器</span><span class="sxs-lookup"><span data-stu-id="9d6ae-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="9d6ae-113">記憶體管理規則</span><span class="sxs-lookup"><span data-stu-id="9d6ae-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="9d6ae-114">調試記憶體配置</span><span class="sxs-lookup"><span data-stu-id="9d6ae-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 