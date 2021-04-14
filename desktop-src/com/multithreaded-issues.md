---
title: 多執行緒問題
description: 多執行緒問題
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372702"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="73525-103">多執行緒問題</span><span class="sxs-lookup"><span data-stu-id="73525-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="73525-104">OLE 提供多執行緒應用程式的支援，可讓應用程式從多個執行緒進行 OLE 呼叫。</span><span class="sxs-lookup"><span data-stu-id="73525-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="73525-105">此多執行緒支援稱為「單元模型」，因此使用多個執行緒的所有 OLE 元件都必須遵循此模型。</span><span class="sxs-lookup"><span data-stu-id="73525-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="73525-106">單元模型要求 (使用 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)將介面指標封送處理，並線上程之間傳遞時 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) 。</span><span class="sxs-lookup"><span data-stu-id="73525-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73525-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="73525-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73525-108">進程、執行緒和單元</span><span class="sxs-lookup"><span data-stu-id="73525-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




