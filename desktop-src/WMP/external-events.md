---
title: 外來事件
description: 外來事件
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player 的外觀、外來事件
- 外觀，外來事件
- 事件，外部
- 撰寫適用于外觀的程式碼，外來事件
- 外來事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965815"
---
# <a name="external-events"></a><span data-ttu-id="d17e3-108">外來事件</span><span class="sxs-lookup"><span data-stu-id="d17e3-108">External Events</span></span>

<span data-ttu-id="d17e3-109">當使用者按一下按鈕或按下按鍵時，您可以使用事件處理常式來回應其輸入。</span><span class="sxs-lookup"><span data-stu-id="d17e3-109">When users click a button or press a key, you can respond to their input with event handlers.</span></span> <span data-ttu-id="d17e3-110">事件處理常式是每次觸發事件時執行的程式碼區段。</span><span class="sxs-lookup"><span data-stu-id="d17e3-110">An event handler is a section of code that runs whenever the event is triggered.</span></span>

<span data-ttu-id="d17e3-111">面板元素支援下列事件：</span><span class="sxs-lookup"><span data-stu-id="d17e3-111">The following events are supported by skin elements:</span></span>

-   <span data-ttu-id="d17e3-112">**載入**</span><span class="sxs-lookup"><span data-stu-id="d17e3-112">**load**</span></span>
-   <span data-ttu-id="d17e3-113">**close**</span><span class="sxs-lookup"><span data-stu-id="d17e3-113">**close**</span></span>
-   <span data-ttu-id="d17e3-114">**調整**</span><span class="sxs-lookup"><span data-stu-id="d17e3-114">**resize**</span></span>
-   <span data-ttu-id="d17e3-115">**計時 器**</span><span class="sxs-lookup"><span data-stu-id="d17e3-115">**timer**</span></span>
-   <span data-ttu-id="d17e3-116">**點擊**</span><span class="sxs-lookup"><span data-stu-id="d17e3-116">**click**</span></span>
-   <span data-ttu-id="d17e3-117">**dblclick**</span><span class="sxs-lookup"><span data-stu-id="d17e3-117">**dblclick**</span></span>
-   <span data-ttu-id="d17e3-118">**error**</span><span class="sxs-lookup"><span data-stu-id="d17e3-118">**error**</span></span>
-   <span data-ttu-id="d17e3-119">**mousedown**</span><span class="sxs-lookup"><span data-stu-id="d17e3-119">**mousedown**</span></span>
-   <span data-ttu-id="d17e3-120">**mouseup**</span><span class="sxs-lookup"><span data-stu-id="d17e3-120">**mouseup**</span></span>
-   <span data-ttu-id="d17e3-121">**mousemove**</span><span class="sxs-lookup"><span data-stu-id="d17e3-121">**mousemove**</span></span>
-   <span data-ttu-id="d17e3-122">**上方**</span><span class="sxs-lookup"><span data-stu-id="d17e3-122">**mouseover**</span></span>
-   <span data-ttu-id="d17e3-123">**mouseout**</span><span class="sxs-lookup"><span data-stu-id="d17e3-123">**mouseout**</span></span>
-   <span data-ttu-id="d17e3-124">**keypress**</span><span class="sxs-lookup"><span data-stu-id="d17e3-124">**keypress**</span></span>
-   <span data-ttu-id="d17e3-125">**keydown**</span><span class="sxs-lookup"><span data-stu-id="d17e3-125">**keydown**</span></span>
-   <span data-ttu-id="d17e3-126">**keyup**</span><span class="sxs-lookup"><span data-stu-id="d17e3-126">**keyup**</span></span>

<span data-ttu-id="d17e3-127">如需特定事件的詳細資訊，請參閱 [外觀程式設計參考](skin-programming-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="d17e3-127">See the [Skin Programming Reference](skin-programming-reference.md) for more details about specific events.</span></span>

<span data-ttu-id="d17e3-128">一般的外部事件處理常式會將事件命名，並定義將執行的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d17e3-128">A typical external event handler would name the event and define the code that will run.</span></span> <span data-ttu-id="d17e3-129">例如，如果您想要建立程式碼來啟動 Windows Media Player 當使用者按一下按鈕時，您會將下列程式程式碼放在按鈕程式碼中。</span><span class="sxs-lookup"><span data-stu-id="d17e3-129">For example, if you want to create code to start Windows Media Player when the user clicks on a button, you would put the following line in your button code.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



<span data-ttu-id="d17e3-130">這會播放名為 laure 的檔案。</span><span class="sxs-lookup"><span data-stu-id="d17e3-130">This will play the file named laure.wma.</span></span> <span data-ttu-id="d17e3-131">請注意，您會將 "on" 這個字新增至特定事件。</span><span class="sxs-lookup"><span data-stu-id="d17e3-131">Note that you add the word "on" to specific events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d17e3-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="d17e3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d17e3-133">**處理事件**</span><span class="sxs-lookup"><span data-stu-id="d17e3-133">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




