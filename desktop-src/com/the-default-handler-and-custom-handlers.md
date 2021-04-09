---
title: 預設處理常式和自訂處理常式
description: 預設處理常式和自訂處理常式
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932037"
---
# <a name="the-default-handler-and-custom-handlers"></a><span data-ttu-id="efe79-103">預設處理常式和自訂處理常式</span><span class="sxs-lookup"><span data-stu-id="efe79-103">The Default Handler and Custom Handlers</span></span>

<span data-ttu-id="efe79-104">大部分的應用程式會使用預設處理常式（OLE 提供的實值）做為處理常式。</span><span class="sxs-lookup"><span data-stu-id="efe79-104">The default handler, an implementation provided by OLE, is used by most applications as the handler.</span></span> <span data-ttu-id="efe79-105">當預設處理常式的功能不足時，應用程式會執行自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="efe79-105">An application implements a custom handler when the default handler's capabilities are insufficient.</span></span> <span data-ttu-id="efe79-106">自訂處理常式可以完全取代預設處理常式，或使用它在適當情況下提供的部分功能。</span><span class="sxs-lookup"><span data-stu-id="efe79-106">A custom handler can either completely replace the default handler or use parts of the functionality it provides where appropriate.</span></span> <span data-ttu-id="efe79-107">在後者的情況下，應用程式處理常式會實作為由新控制項物件和預設處理常式組成的匯總物件。</span><span class="sxs-lookup"><span data-stu-id="efe79-107">In the latter case, the application handler is implemented as an aggregate object composed of a new control object and the default handler.</span></span> <span data-ttu-id="efe79-108">組合應用程式/預設處理常式也稱為同 *進程處理* 程式。</span><span class="sxs-lookup"><span data-stu-id="efe79-108">Combination application/default handlers are also known as *in-process handlers*.</span></span> <span data-ttu-id="efe79-109">*遠端處理處理常式* 用於未在系統登錄中指派 CLSID 或沒有指定處理常式的物件。</span><span class="sxs-lookup"><span data-stu-id="efe79-109">The *remoting handler* is used for objects that are not assigned a CLSID in the system registry or that have no specified handler.</span></span> <span data-ttu-id="efe79-110">這些物件類型的處理常式所需的全部都是在整個進程界限之間傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="efe79-110">All that is required from a handler for these types of objects is that they pass information across the process boundary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efe79-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="efe79-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efe79-112">物件處理常式</span><span class="sxs-lookup"><span data-stu-id="efe79-112">Object Handlers</span></span>](object-handlers.md)
</dt> </dl>

 

 




