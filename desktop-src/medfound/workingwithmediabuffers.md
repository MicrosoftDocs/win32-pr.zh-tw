---
description: 使用 SQL-DMO 媒體緩衝區
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: 使用 SQL-DMO 媒體緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998562"
---
# <a name="working-with-dmo-media-buffers"></a><span data-ttu-id="58feb-103">使用 SQL-DMO 媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="58feb-103">Working with DMO Media Buffers</span></span>

<span data-ttu-id="58feb-104">輸入資料會使用媒體緩衝區傳遞給編解碼器 DMOs。</span><span class="sxs-lookup"><span data-stu-id="58feb-104">Input data is passed to the codec DMOs using media buffers.</span></span> <span data-ttu-id="58feb-105">媒體緩衝區是實 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="58feb-105">A media buffer is an object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="58feb-106">您可以針對此用途來執行類別，或者，如果您在應用程式中使用 Windows Media Format SDK，則可以使用該 SDK 中定義的緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="58feb-106">You can implement a class for this purpose or, if you are using the Windows Media Format SDK in your application, you can use the buffer objects that are defined in that SDK.</span></span>

<span data-ttu-id="58feb-107">如果您要執行自己的緩衝區類別，請小心處理緩衝區記憶體的處理方式。</span><span class="sxs-lookup"><span data-stu-id="58feb-107">If you implement your own buffer class, be careful about how the buffer memory is handled.</span></span> <span data-ttu-id="58feb-108">當您傳遞輸入範例時，會保留緩衝區的參考，直到完成樣本為止。</span><span class="sxs-lookup"><span data-stu-id="58feb-108">When you pass an input sample, the DMO keeps a reference to the buffer until it is finished with the sample.</span></span> <span data-ttu-id="58feb-109">您可以立即釋出 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 介面的參考，但無法知道編解碼器不再需要它的參考。</span><span class="sxs-lookup"><span data-stu-id="58feb-109">You can immediately release your reference to the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface, but you have no way of knowing when the codec no longer needs its reference.</span></span> <span data-ttu-id="58feb-110">若要確定當物件刪除時，記憶體會釋出，您應該執行類別，使其在內部為緩衝區配置和釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="58feb-110">To be certain that the memory is freed when the object deletes itself, you should implement your class so that it allocates and frees the memory for the buffer internally.</span></span>

<span data-ttu-id="58feb-111">由於 DMOs 會在未知的期間內保留緩衝區的參考，因此使用有限的緩衝區集區並不是很簡單的事。</span><span class="sxs-lookup"><span data-stu-id="58feb-111">Because the DMOs keep references to buffers for an unknown period of time, it is not a trivial matter to use a limited pool of buffers.</span></span> <span data-ttu-id="58feb-112">最簡單的解決方案是為每個範例配置新的緩衝區，雖然這樣做沒有效率。</span><span class="sxs-lookup"><span data-stu-id="58feb-112">The simplest solution is to allocate a new buffer for each sample, although doing so is inefficient.</span></span>

<span data-ttu-id="58feb-113">更好的解決方法是執行物件來管理緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="58feb-113">A better solution is to implement an object to manage a pool of buffers.</span></span> <span data-ttu-id="58feb-114">若要這樣做，請在 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer)執行的 **Release** 方法中撰寫程式碼，以呼叫緩衝區管理員的方法， (而不是在參考計數降至零時刪除本身) 。</span><span class="sxs-lookup"><span data-stu-id="58feb-114">To do this, write code in the **Release** method of your [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementation that calls a method of your buffer manager (instead of deleting itself) when the reference count drops to zero.</span></span> <span data-ttu-id="58feb-115">然後，緩衝區管理員可以維護已配置之緩衝區物件的指標清單。</span><span class="sxs-lookup"><span data-stu-id="58feb-115">The buffer manager can then maintain a list of pointers to allocated buffer objects.</span></span> <span data-ttu-id="58feb-116">在您的緩衝區管理員中建立方法，以檢查可用緩衝區清單並傳回指標，讓您的應用程式可以視需要存取緩衝區。</span><span class="sxs-lookup"><span data-stu-id="58feb-116">Create a method in your buffer manager to check the list of free buffers and return a pointer so that your application can access buffers when needed.</span></span> <span data-ttu-id="58feb-117">此方法應該視需要建立新的緩衝區，並將其新增至清單。</span><span class="sxs-lookup"><span data-stu-id="58feb-117">This method should create new buffers as needed and add them to the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58feb-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="58feb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58feb-119">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="58feb-119">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
