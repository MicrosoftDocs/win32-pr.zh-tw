---
title: 建立 Proxy 物件
description: 除了設計可執行 IAccessible 屬性和方法的類別之外，伺服器開發人員也可能需要設計 proxy 物件來監視可存取物件的存留期。
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671903"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="99efd-103">建立 Proxy 物件</span><span class="sxs-lookup"><span data-stu-id="99efd-103">Creating Proxy Objects</span></span>

<span data-ttu-id="99efd-104">除了設計可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性和方法的類別之外，伺服器開發人員也可能需要設計 *proxy* 物件來監視可存取物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="99efd-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="99efd-105">如果應用程式中的可存取物件可在應用程式執行時使用，則您不需要建立 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="99efd-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="99efd-106">如果可以在應用程式執行時終結可存取的物件，則您必須建立 proxy 物件。</span><span class="sxs-lookup"><span data-stu-id="99efd-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99efd-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="99efd-107">In this section</span></span>

-   [<span data-ttu-id="99efd-108">什麼是 Proxy 物件？</span><span class="sxs-lookup"><span data-stu-id="99efd-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="99efd-109">為何需要 Proxy 物件</span><span class="sxs-lookup"><span data-stu-id="99efd-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="99efd-110">Proxy 物件的設計考慮</span><span class="sxs-lookup"><span data-stu-id="99efd-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 




