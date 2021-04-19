---
title: 原生 Active Accessibility 實作為
description: 執行 IAccessible 介面的使用者介面元素，就是提供原生的實作為。
ms.assetid: 36a5c0cd-53f0-433e-8932-da7d1de177dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5f6e6b6152c2f5e5c41a6a2b7cd3f84a3fce373
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967825"
---
# <a name="native-active-accessibility-implementation"></a><span data-ttu-id="266ae-103">原生 Active Accessibility 實作為</span><span class="sxs-lookup"><span data-stu-id="266ae-103">Native Active Accessibility Implementation</span></span>

<span data-ttu-id="266ae-104">執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的使用者介面元素，就是提供 *原生的實* 作為。</span><span class="sxs-lookup"><span data-stu-id="266ae-104">User interface elements that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface are said to provide a *native implementation*.</span></span> <span data-ttu-id="266ae-105">雖然將 **IAccessible** (或任何其他元件物件模型的開發成本 (COM) 介面) 可能很高，但其優點是對用戶端公開的資訊有完整的控制權。</span><span class="sxs-lookup"><span data-stu-id="266ae-105">Although the development cost for implementing **IAccessible** (or any other Component Object Model (COM) interface) can be high, the benefit is complete control over the information exposed to clients.</span></span>

<span data-ttu-id="266ae-106">如果您的應用程式使用自訂控制項或 Oleacc.dll 無法 proxy 的其他控制項，您將需要提供原生執行。</span><span class="sxs-lookup"><span data-stu-id="266ae-106">If your application uses custom controls or other controls that cannot be proxied by Oleacc.dll, you will need to provide a native implementation.</span></span>

 

 




