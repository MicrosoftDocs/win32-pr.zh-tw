---
description: 非同步回呼方法
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: 非同步回呼方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967073"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="70a20-103">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="70a20-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="70a20-104">媒體基礎使用回呼介面提供一致的方式來執行非同步方法。</span><span class="sxs-lookup"><span data-stu-id="70a20-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="70a20-105">本節說明如何執行回呼介面，以及如何撰寫使用此介面的非同步方法。</span><span class="sxs-lookup"><span data-stu-id="70a20-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="70a20-106">其中包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="70a20-106">It contains the following topics.</span></span>



| <span data-ttu-id="70a20-107">主題</span><span class="sxs-lookup"><span data-stu-id="70a20-107">Topic</span></span>                                                                                | <span data-ttu-id="70a20-108">描述</span><span class="sxs-lookup"><span data-stu-id="70a20-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70a20-109">呼叫非同步方法</span><span class="sxs-lookup"><span data-stu-id="70a20-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="70a20-110">如何在媒體基礎中呼叫非同步方法。</span><span class="sxs-lookup"><span data-stu-id="70a20-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="70a20-111">執行非同步回呼</span><span class="sxs-lookup"><span data-stu-id="70a20-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="70a20-112">如何在 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面中執行回呼方法。</span><span class="sxs-lookup"><span data-stu-id="70a20-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="70a20-113">支援多個回呼</span><span class="sxs-lookup"><span data-stu-id="70a20-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="70a20-114">如何支援相同 c + + 類別內的多個回呼。</span><span class="sxs-lookup"><span data-stu-id="70a20-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="70a20-115">工作佇列</span><span class="sxs-lookup"><span data-stu-id="70a20-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="70a20-116">工作佇列可提供有效的方式，讓您在另一個執行緒上執行非同步作業。</span><span class="sxs-lookup"><span data-stu-id="70a20-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="70a20-117">撰寫非同步方法</span><span class="sxs-lookup"><span data-stu-id="70a20-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="70a20-118">如何在媒體基礎中執行非同步方法。</span><span class="sxs-lookup"><span data-stu-id="70a20-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="70a20-119">自訂非同步結果物件</span><span class="sxs-lookup"><span data-stu-id="70a20-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="70a20-120">如何提供 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的自訂執行。</span><span class="sxs-lookup"><span data-stu-id="70a20-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="70a20-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="70a20-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70a20-122">**IMFAsyncCallback 介面**</span><span class="sxs-lookup"><span data-stu-id="70a20-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="70a20-123">**IMFAsyncResult 介面**</span><span class="sxs-lookup"><span data-stu-id="70a20-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="70a20-124">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="70a20-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



