---
title: 系結控制碼的類型
description: 系結控制碼可以是自動、隱含或明確。
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021810"
---
# <a name="types-of-binding-handles"></a><span data-ttu-id="adfdf-103">系結控制碼的類型</span><span class="sxs-lookup"><span data-stu-id="adfdf-103">Types of Binding Handles</span></span>

<span data-ttu-id="adfdf-104">系結控制碼可以是自動、隱含或明確。</span><span class="sxs-lookup"><span data-stu-id="adfdf-104">Binding handles can be automatic, implicit, or explicit.</span></span> <span data-ttu-id="adfdf-105">它們在應用程式對系結程式上的控制程度不同。</span><span class="sxs-lookup"><span data-stu-id="adfdf-105">They differ in the amount of control the application has over the binding process.</span></span> <span data-ttu-id="adfdf-106">顧名思義，自動系結會處理自動化系結。</span><span class="sxs-lookup"><span data-stu-id="adfdf-106">As the name suggests, automatic binding handles automate binding.</span></span> <span data-ttu-id="adfdf-107">用戶端和伺服器應用程式不需要程式碼來處理系結程式。</span><span class="sxs-lookup"><span data-stu-id="adfdf-107">The client and server applications do not need code to handle the binding process.</span></span> <span data-ttu-id="adfdf-108">隱含系結控制碼可讓用戶端程式在系結髮生之前設定系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="adfdf-108">Implicit binding handles allow client programs to configure the binding handle before the binding takes place.</span></span> <span data-ttu-id="adfdf-109">在用戶端建立系結之後，RPC 執行時間程式庫會處理其餘部分。</span><span class="sxs-lookup"><span data-stu-id="adfdf-109">After the client establishes a binding, the RPC run-time library handles the rest.</span></span> <span data-ttu-id="adfdf-110">明確系結控制碼可將系結程式的完整控制權移至用戶端和伺服器程式的原始程式碼中。</span><span class="sxs-lookup"><span data-stu-id="adfdf-110">Explicit binding handles move complete control over the binding process into the source code of the client and the server programs.</span></span> <span data-ttu-id="adfdf-111">使用此控制項會增加複雜度。</span><span class="sxs-lookup"><span data-stu-id="adfdf-111">With this control comes increased complexity.</span></span> <span data-ttu-id="adfdf-112">您的應用程式必須呼叫 RPC 函數來管理系結。</span><span class="sxs-lookup"><span data-stu-id="adfdf-112">Your application must call RPC functions to manage the binding.</span></span> <span data-ttu-id="adfdf-113">它不會自動發生。</span><span class="sxs-lookup"><span data-stu-id="adfdf-113">It does not happen automatically.</span></span> <span data-ttu-id="adfdf-114">建議使用明確的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="adfdf-114">Explicit binding handles are recommended.</span></span>

<span data-ttu-id="adfdf-115">下圖說明自動、隱含和明確系結控制碼之間的差異。</span><span class="sxs-lookup"><span data-stu-id="adfdf-115">The following diagram illustrates the differences between automatic, implicit, and explicit binding handles.</span></span>

![自動、隱含和明確系結控制碼之間的差異](images/bhand.png)

<span data-ttu-id="adfdf-117">此外，每個系結控制碼都是基本或自訂的。</span><span class="sxs-lookup"><span data-stu-id="adfdf-117">In addition, every binding handle is either primitive or custom.</span></span> <span data-ttu-id="adfdf-118">下列主題將討論每種類型的系結控制碼：</span><span class="sxs-lookup"><span data-stu-id="adfdf-118">Each type of binding handle is discussed in the following topics:</span></span>

-   [<span data-ttu-id="adfdf-119">自動系結控制碼</span><span class="sxs-lookup"><span data-stu-id="adfdf-119">Automatic Binding Handles</span></span>](automatic-binding-handles.md)
-   [<span data-ttu-id="adfdf-120">隱含系結控制碼</span><span class="sxs-lookup"><span data-stu-id="adfdf-120">Implicit Binding Handles</span></span>](implicit-binding-handles.md)
-   [<span data-ttu-id="adfdf-121">明確的系結控制碼</span><span class="sxs-lookup"><span data-stu-id="adfdf-121">Explicit Binding Handles</span></span>](explicit-binding-handles.md)
-   [<span data-ttu-id="adfdf-122">基本和自訂系結控制碼</span><span class="sxs-lookup"><span data-stu-id="adfdf-122">Primitive and Custom Binding Handles</span></span>](primitive-and-custom-binding-handles.md)

 

 




