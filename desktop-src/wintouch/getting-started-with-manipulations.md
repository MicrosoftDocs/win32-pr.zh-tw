---
title: 操作
description: 本節說明 Windows Touch 的物件操作。
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch，操作
- 操作，關於
- 操作，手勢差異
- 手勢、操作差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300187"
---
# <a name="manipulations"></a><span data-ttu-id="82c3b-107">操作</span><span class="sxs-lookup"><span data-stu-id="82c3b-107">Manipulations</span></span>

<span data-ttu-id="82c3b-108">本節說明 Windows Touch 的物件操作。</span><span class="sxs-lookup"><span data-stu-id="82c3b-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="82c3b-109">操作總覽</span><span class="sxs-lookup"><span data-stu-id="82c3b-109">Manipulation Overview</span></span>

<span data-ttu-id="82c3b-110">要考慮操作的一個便利方式，就是將它們視為手勢的超集合。</span><span class="sxs-lookup"><span data-stu-id="82c3b-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="82c3b-111">您可以使用筆勢進行哪些動作，您可以利用更多的彈性，並使用操作來提供更精細的精確度。</span><span class="sxs-lookup"><span data-stu-id="82c3b-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="82c3b-112">操作和手勢之間的差異最好以簡單的範例來示範。</span><span class="sxs-lookup"><span data-stu-id="82c3b-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="82c3b-113">您可以展開物件，並使用操作將它轉譯;使用手勢時，您一次只能進行一個動作。</span><span class="sxs-lookup"><span data-stu-id="82c3b-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="82c3b-114">這項功能可以即時操作物件，藉由啟用更真實的體驗，讓應用程式更直覺化。</span><span class="sxs-lookup"><span data-stu-id="82c3b-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="82c3b-115">操作 Api 是用來針對已啟用觸控功能的應用程式，簡化對物件的轉換作業。</span><span class="sxs-lookup"><span data-stu-id="82c3b-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="82c3b-116">操作是在 Windows 7 中透過操作 COM 物件來執行。</span><span class="sxs-lookup"><span data-stu-id="82c3b-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="82c3b-117">藉由使用操作，開發人員可以更輕鬆地支援慣性 (物件物理) ，而且可以在與其他應用程式一致的方式中，輕鬆地執行物件的轉換。</span><span class="sxs-lookup"><span data-stu-id="82c3b-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="82c3b-118">下列各節說明您可以執行操作的各種方式。</span><span class="sxs-lookup"><span data-stu-id="82c3b-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="82c3b-119">區段</span><span class="sxs-lookup"><span data-stu-id="82c3b-119">Section</span></span>                                                                                            | <span data-ttu-id="82c3b-120">描述</span><span class="sxs-lookup"><span data-stu-id="82c3b-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82c3b-121">將操作支援新增至非受控碼</span><span class="sxs-lookup"><span data-stu-id="82c3b-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="82c3b-122">說明如何執行 [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents)介面的事件接收，以及將事件處理常式新增至您的程式碼。</span><span class="sxs-lookup"><span data-stu-id="82c3b-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="82c3b-123">Advanced 操作</span><span class="sxs-lookup"><span data-stu-id="82c3b-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="82c3b-124">說明如何執行複雜的操作。</span><span class="sxs-lookup"><span data-stu-id="82c3b-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="82c3b-125">單一手指旋轉</span><span class="sxs-lookup"><span data-stu-id="82c3b-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="82c3b-126">說明如何使用資料透視點和操作處理器來旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="82c3b-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="82c3b-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="82c3b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c3b-128">操作和慣性</span><span class="sxs-lookup"><span data-stu-id="82c3b-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




