---
description: 此頁面會列出一些通常是使用 XPS 檔 API 來執行的程式設計工作。
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: 一般 XPS 檔程式設計工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996727"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="5da9b-103">一般 XPS 檔程式設計工作</span><span class="sxs-lookup"><span data-stu-id="5da9b-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="5da9b-104">此頁面會列出一些通常是使用 XPS 檔 API 來執行的程式設計工作。</span><span class="sxs-lookup"><span data-stu-id="5da9b-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="5da9b-105">一般 XPS 檔工作</span><span class="sxs-lookup"><span data-stu-id="5da9b-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="5da9b-106">下列程式碼範例說明在使用 xps 檔 API 來處理 XPS OM 時，通常會執行的一些程式設計工作。</span><span class="sxs-lookup"><span data-stu-id="5da9b-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="5da9b-107">初始化 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5da9b-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="5da9b-108">建立空白的 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5da9b-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="5da9b-109">將 XPS 檔讀入 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5da9b-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="5da9b-110">流覽 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5da9b-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="5da9b-111">將文字寫入至 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5da9b-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="5da9b-112">在 XPS OM 中繪製圖形</span><span class="sxs-lookup"><span data-stu-id="5da9b-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="5da9b-113">以 XPS OM 放置影像</span><span class="sxs-lookup"><span data-stu-id="5da9b-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="5da9b-114">將 XPS OM 寫入 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="5da9b-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="5da9b-115">列印 XPS OM</span><span class="sxs-lookup"><span data-stu-id="5da9b-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="5da9b-116">使用 XPS OM 集合介面</span><span class="sxs-lookup"><span data-stu-id="5da9b-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="5da9b-117">免責聲明</span><span class="sxs-lookup"><span data-stu-id="5da9b-117">Disclaimer</span></span>

<span data-ttu-id="5da9b-118">程式碼範例的目的不是完整且正常運作的程式。</span><span class="sxs-lookup"><span data-stu-id="5da9b-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="5da9b-119">例如，此頁面所參考的程式碼範例不會執行參數檢查、錯誤檢查或錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="5da9b-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="5da9b-120">使用這些範例作為起點，然後新增建立健全的應用程式所需的程式碼。</span><span class="sxs-lookup"><span data-stu-id="5da9b-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="5da9b-121">如需 **HRESULT** 傳回值和錯誤處理策略的詳細資訊，請參閱 [COM 中的錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="5da9b-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="5da9b-122">在可以使用 XPS OM 介面之前，必須線上程中初始化 COM，如下列範例程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="5da9b-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="5da9b-123">為了清楚起見，這些程式碼範例會使用非常簡單的 XPS OM，它對您的應用程式而言可能不夠複雜。</span><span class="sxs-lookup"><span data-stu-id="5da9b-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="5da9b-124">在此情況下，將內容新增至頁面的程式碼範例中，會將頁面的視覺元素直接新增至頁面的視覺物件清單;不過，在實務上，您可能會想要將視覺物件分組為 canvas 物件，以便將多個物件視為群組來處理。</span><span class="sxs-lookup"><span data-stu-id="5da9b-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="5da9b-125">因此，若要啟用多個頁面大小的相同內容支援，您可以將頁面的視覺內容分組成單一畫布物件，然後將轉換套用至畫布，以將其調整為目前的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="5da9b-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5da9b-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="5da9b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5da9b-127">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="5da9b-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="5da9b-128">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5da9b-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
