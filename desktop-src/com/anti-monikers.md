---
title: 反標記
description: OLE 會提供一種特殊類型的標記來執行，稱為反標記。
ms.assetid: 3b52d3bd-8375-4463-a0e3-5117fa96a1c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d69c461268b486a040b36f59108bc8e8379656
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021587"
---
# <a name="anti-monikers"></a><span data-ttu-id="61b6c-103">反標記</span><span class="sxs-lookup"><span data-stu-id="61b6c-103">Anti-Monikers</span></span>

<span data-ttu-id="61b6c-104">OLE 會提供一種特殊類型的標記來執行，稱為 *反標記*。</span><span class="sxs-lookup"><span data-stu-id="61b6c-104">OLE provides an implementation of a special type of moniker called an *anti-moniker*.</span></span> <span data-ttu-id="61b6c-105">您可以在建立新的「標記」類別時使用這個標記。</span><span class="sxs-lookup"><span data-stu-id="61b6c-105">You use this moniker in the creation of new moniker classes.</span></span> <span data-ttu-id="61b6c-106">您可以使用它做為它所組成之標記的反向，有效地取消該標記，與「...」運算子在檔案系統命令中的目錄層級上移動的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="61b6c-106">You use it as the inverse of the moniker that it is composed onto, effectively canceling that moniker, in much the same way that the ".." operator moves up a directory level in a file system command.</span></span>

<span data-ttu-id="61b6c-107">必須有反標記可供使用，因為一旦建立複合的標記，就無法刪除部分的標記（例如，物件移動）。</span><span class="sxs-lookup"><span data-stu-id="61b6c-107">It is necessary to have an anti-moniker available, because once a composite moniker is created, it is not possible to delete parts of the moniker if, for example, an object moves.</span></span> <span data-ttu-id="61b6c-108">相反地，您可以使用反標記來移除複合標記中的一或多個專案。</span><span class="sxs-lookup"><span data-stu-id="61b6c-108">Instead, you use an anti-moniker to remove one or more entries from a composite moniker.</span></span>

<span data-ttu-id="61b6c-109">反標記是明確要作為反向使用的標記類別。</span><span class="sxs-lookup"><span data-stu-id="61b6c-109">Anti-monikers are a moniker class explicitly intended for use as an inverse.</span></span> <span data-ttu-id="61b6c-110">COM 會定義名為 [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) 的函式，此函式會傳回反標記。</span><span class="sxs-lookup"><span data-stu-id="61b6c-110">COM defines the named [**CreateAntiMoniker**](/windows/desktop/api/Objbase/nf-objbase-createantimoniker) function, which returns an anti-moniker.</span></span> <span data-ttu-id="61b6c-111">您通常會使用這個函數來執行 [**IMoniker：：反向**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) 方法。</span><span class="sxs-lookup"><span data-stu-id="61b6c-111">You generally use this function to implement the [**IMoniker::Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) method.</span></span>

<span data-ttu-id="61b6c-112">反標記只是對這些標記類型的反向，這些類型是實為了將反標記視為反向的。</span><span class="sxs-lookup"><span data-stu-id="61b6c-112">An anti-moniker is only an inverse for those types of monikers that are implemented to treat anti-monikers as an inverse.</span></span> <span data-ttu-id="61b6c-113">例如，如果您想要移除複合標記的最後一個部分，則不應建立反標記，並將它撰寫至複合結尾。</span><span class="sxs-lookup"><span data-stu-id="61b6c-113">For example, if you want to remove the last piece of a composite moniker, you should not create an anti-moniker and compose it to the end of the composite.</span></span> <span data-ttu-id="61b6c-114">您無法確定複合的最後一個部分會將反標記視為反向。</span><span class="sxs-lookup"><span data-stu-id="61b6c-114">You cannot be sure that the last piece of the composite considers an anti-moniker to be its inverse.</span></span> <span data-ttu-id="61b6c-115">相反地，您應該在複合的標記上呼叫 [**IMoniker：： Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) ，並指定 **FALSE** 做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="61b6c-115">Instead, you should call [**IMoniker::Enum**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-enum) on the composite moniker, specifying **FALSE** as the first parameter.</span></span> <span data-ttu-id="61b6c-116">這會建立一個列舉值，以反向順序傳回元件的名字。</span><span class="sxs-lookup"><span data-stu-id="61b6c-116">This creates an enumerator that returns the component monikers in reverse order.</span></span> <span data-ttu-id="61b6c-117">您可以使用列舉值來取出複合的最後片段，並在該名字標記上呼叫 [**反向**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) 。</span><span class="sxs-lookup"><span data-stu-id="61b6c-117">Use the enumerator to retrieve the last piece of the composite, and call [**Inverse**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-inverse) on that moniker.</span></span> <span data-ttu-id="61b6c-118">**反向** 傳回的標記是您需要移除複合最後一部分的結果。</span><span class="sxs-lookup"><span data-stu-id="61b6c-118">The moniker returned by **Inverse** is what you need to remove the last piece of the composite.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61b6c-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="61b6c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61b6c-120">類別名字標記</span><span class="sxs-lookup"><span data-stu-id="61b6c-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="61b6c-121">複合的名字</span><span class="sxs-lookup"><span data-stu-id="61b6c-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="61b6c-122">檔案名字</span><span class="sxs-lookup"><span data-stu-id="61b6c-122">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="61b6c-123">專案的名字</span><span class="sxs-lookup"><span data-stu-id="61b6c-123">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="61b6c-124">指標標記</span><span class="sxs-lookup"><span data-stu-id="61b6c-124">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




