---
description: 建立時間軸物件
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: 建立時間軸物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973345"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="f2fd9-103">建立時間軸物件</span><span class="sxs-lookup"><span data-stu-id="f2fd9-103">Creating Timeline Objects</span></span>

<span data-ttu-id="f2fd9-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f2fd9-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f2fd9-105">本文中顯示的範例程式碼會以空白的時間軸開始，但如果您載入現有的專案，而且想要在其中新增物件，則適用相同的步驟。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="f2fd9-106">若要在時間軸中建立任何類型的物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="f2fd9-107">例如，下列程式碼會建立新的群組：</span><span class="sxs-lookup"><span data-stu-id="f2fd9-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="f2fd9-108">第二個參數是 [**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="f2fd9-109">它會指定要建立的時間軸物件類型，例如群組或曲目。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="f2fd9-110">**CreateEmptyNode** 方法會建立物件，並傳回物件的 [**IAMTimelineObj**](iamtimelineobj.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="f2fd9-111">此外，它也會遞增 **IAMTimelineObj** 介面上的參考計數，因此您必須在使用完畢之後釋放介面。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="f2fd9-112">請勿呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="f2fd9-113">相反地，請一律使用 **CreateEmptyNode** 來建立時間軸物件，因為它會初始化要在時間軸中使用的新物件。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="f2fd9-114">[**IAMTimelineObj**](iamtimelineobj.md)介面是泛型介面。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="f2fd9-115">它提供所有類型時程表物件通用的方法。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="f2fd9-116">每種類型的物件也會公開其他介面。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="f2fd9-117">例如，群組會公開 [**IAMTimelineGroup**](iamtimelinegroup.md) 介面，以及其他群組。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="f2fd9-118">您可以藉由呼叫 **QueryInterface** 來取得其他介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="f2fd9-119">建立物件之後，它還不是時間軸的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="f2fd9-120">將物件加入至時間軸的方法取決於物件類型。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="f2fd9-121">下一節說明如何將群組、組合和追蹤新增至時間軸。</span><span class="sxs-lookup"><span data-stu-id="f2fd9-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2fd9-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="f2fd9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2fd9-123">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="f2fd9-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
