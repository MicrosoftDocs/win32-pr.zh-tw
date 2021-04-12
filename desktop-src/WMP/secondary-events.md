---
title: 次要事件
description: 次要事件
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Windows Media Player 的外觀，次要事件
- 外觀，次要事件
- 事件，次要
- 撰寫適用于面板的程式碼，次要事件
- 次要事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462384"
---
# <a name="secondary-events"></a><span data-ttu-id="1fb50-108">次要事件</span><span class="sxs-lookup"><span data-stu-id="1fb50-108">Secondary Events</span></span>

<span data-ttu-id="1fb50-109">您可以判斷觸發特定事件時，所發生的其他事件。</span><span class="sxs-lookup"><span data-stu-id="1fb50-109">You can determine what other events are taking place when a specific event is triggered.</span></span> <span data-ttu-id="1fb50-110">例如，按一下滑鼠按鍵時，您可能會想要知道 ALT 鍵是否同時關閉。</span><span class="sxs-lookup"><span data-stu-id="1fb50-110">For example, when a mouse button is clicked, you may want to know whether the ALT key was down at the same time.</span></span>

## <a name="event-attributes"></a><span data-ttu-id="1fb50-111">事件屬性</span><span class="sxs-lookup"><span data-stu-id="1fb50-111">Event Attributes</span></span>

<span data-ttu-id="1fb50-112">以下是支援的事件屬性：</span><span class="sxs-lookup"><span data-stu-id="1fb50-112">The following event attributes are supported for skins:</span></span>

-   <span data-ttu-id="1fb50-113">**altKey**</span><span class="sxs-lookup"><span data-stu-id="1fb50-113">**altKey**</span></span>
-   <span data-ttu-id="1fb50-114">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="1fb50-114">**button**</span></span>
-   <span data-ttu-id="1fb50-115">**clientX**</span><span class="sxs-lookup"><span data-stu-id="1fb50-115">**clientX**</span></span>
-   <span data-ttu-id="1fb50-116">**clientY**</span><span class="sxs-lookup"><span data-stu-id="1fb50-116">**clientY**</span></span>
-   <span data-ttu-id="1fb50-117">**ctrlKey**</span><span class="sxs-lookup"><span data-stu-id="1fb50-117">**ctrlKey**</span></span>
-   <span data-ttu-id="1fb50-118">**fromElement**</span><span class="sxs-lookup"><span data-stu-id="1fb50-118">**fromElement**</span></span>
-   <span data-ttu-id="1fb50-119">**offsetX**</span><span class="sxs-lookup"><span data-stu-id="1fb50-119">**offsetX**</span></span>
-   <span data-ttu-id="1fb50-120">**offsetY**</span><span class="sxs-lookup"><span data-stu-id="1fb50-120">**offsetY**</span></span>
-   <span data-ttu-id="1fb50-121">**screenX**</span><span class="sxs-lookup"><span data-stu-id="1fb50-121">**screenX**</span></span>
-   <span data-ttu-id="1fb50-122">**screenY**</span><span class="sxs-lookup"><span data-stu-id="1fb50-122">**screenY**</span></span>
-   <span data-ttu-id="1fb50-123">**shiftKey**</span><span class="sxs-lookup"><span data-stu-id="1fb50-123">**shiftKey**</span></span>
-   <span data-ttu-id="1fb50-124">**srcElement**</span><span class="sxs-lookup"><span data-stu-id="1fb50-124">**srcElement**</span></span>
-   <span data-ttu-id="1fb50-125">**toElement**</span><span class="sxs-lookup"><span data-stu-id="1fb50-125">**toElement**</span></span>
-   <span data-ttu-id="1fb50-126">**x**</span><span class="sxs-lookup"><span data-stu-id="1fb50-126">**x**</span></span>
-   <span data-ttu-id="1fb50-127">**y**</span><span class="sxs-lookup"><span data-stu-id="1fb50-127">**y**</span></span>
-   <span data-ttu-id="1fb50-128">**keyCode**</span><span class="sxs-lookup"><span data-stu-id="1fb50-128">**keyCode**</span></span>

<span data-ttu-id="1fb50-129">如需這些屬性的詳細資訊，請參閱 [外觀程式設計參考](skin-programming-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="1fb50-129">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="using-secondary-events"></a><span data-ttu-id="1fb50-130">使用次要事件</span><span class="sxs-lookup"><span data-stu-id="1fb50-130">Using Secondary Events</span></span>

<span data-ttu-id="1fb50-131">您只能處理 JScript 程式碼中的事件屬性。</span><span class="sxs-lookup"><span data-stu-id="1fb50-131">You can only process event attributes in JScript code.</span></span> <span data-ttu-id="1fb50-132">您必須使用下列語法：</span><span class="sxs-lookup"><span data-stu-id="1fb50-132">You must use the following syntax:</span></span>


```C++
event.eventattributename
```



<span data-ttu-id="1fb50-133">*eventattributename* 是事件屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="1fb50-133">*eventattributename* is the name of the event attribute.</span></span> <span data-ttu-id="1fb50-134">例如，若要判斷在 click 事件期間是否按下 ALT 鍵，您可以在 JScript 程式碼中使用下列幾行：</span><span class="sxs-lookup"><span data-stu-id="1fb50-134">For example, to determine whether the ALT key was pressed during a click event, you could use the following lines in your JScript code:</span></span>


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a><span data-ttu-id="1fb50-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fb50-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fb50-136">**處理事件**</span><span class="sxs-lookup"><span data-stu-id="1fb50-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




