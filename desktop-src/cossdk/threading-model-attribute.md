---
description: COM + 會為您管理執行緒。 每個 COM 元件都有一個 >threadingmodel 屬性，您可以在開發元件時指定此屬性。 這個屬性會決定如何將元件物件指派給執行緒，以便執行方法。
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: 執行緒模型屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385894"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="f9fee-105">執行緒模型屬性</span><span class="sxs-lookup"><span data-stu-id="f9fee-105">Threading Model Attribute</span></span>

<span data-ttu-id="f9fee-106">COM + 會為您管理執行緒。</span><span class="sxs-lookup"><span data-stu-id="f9fee-106">COM+ manages threads for you.</span></span> <span data-ttu-id="f9fee-107">每個 COM 元件都有一個 **>threadingmodel** 屬性，您可以在開發元件時指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="f9fee-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="f9fee-108">這個屬性會決定如何將元件的物件指派給執行方法的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f9fee-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="f9fee-109">您可以使用 [元件服務] 系統管理工具，以滑鼠右鍵按一下 [ **元件** ] 資料夾中的元件，按一下 [ **屬性**]，然後按一下 [ **並行** 存取] 索引標籤，以查看執行緒模型屬性。在 **執行緒模型** 下，可能的值如下所示：</span><span class="sxs-lookup"><span data-stu-id="f9fee-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="f9fee-110">**主執行緒單元**</span><span class="sxs-lookup"><span data-stu-id="f9fee-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="f9fee-111">**單一線程單元**</span><span class="sxs-lookup"><span data-stu-id="f9fee-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="f9fee-112">**自由執行緒單元**</span><span class="sxs-lookup"><span data-stu-id="f9fee-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="f9fee-113">**中立的單元**</span><span class="sxs-lookup"><span data-stu-id="f9fee-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="f9fee-114">**任何單元**</span><span class="sxs-lookup"><span data-stu-id="f9fee-114">**Any Apartment**</span></span>

<span data-ttu-id="f9fee-115">COM + 的慣用執行緒模型是 [中性的單元](neutral-apartments.md)。</span><span class="sxs-lookup"><span data-stu-id="f9fee-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="f9fee-116">但是，如果您未指定元件的執行緒模型，COM + 會使用主執行緒的單元（預設值）。</span><span class="sxs-lookup"><span data-stu-id="f9fee-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="f9fee-117">如需詳細資訊，請參閱 [選擇執行緒模型](/windows/desktop/com/choosing-the-threading-model)。</span><span class="sxs-lookup"><span data-stu-id="f9fee-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="f9fee-118">下表顯示 COM + 中各單元的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="f9fee-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="f9fee-119">型號</span><span class="sxs-lookup"><span data-stu-id="f9fee-119">Model</span></span>                     | <span data-ttu-id="f9fee-120">公寓</span><span class="sxs-lookup"><span data-stu-id="f9fee-120">Apartment</span></span>                                                 | <span data-ttu-id="f9fee-121">免費</span><span class="sxs-lookup"><span data-stu-id="f9fee-121">Free</span></span>                               | <span data-ttu-id="f9fee-122">兩者</span><span class="sxs-lookup"><span data-stu-id="f9fee-122">Both</span></span>                               | <span data-ttu-id="f9fee-123">中性</span><span class="sxs-lookup"><span data-stu-id="f9fee-123">Neutral</span></span>                      | <span data-ttu-id="f9fee-124">未指定</span><span class="sxs-lookup"><span data-stu-id="f9fee-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="f9fee-125">單一執行緒，非主要</span><span class="sxs-lookup"><span data-stu-id="f9fee-125">Single-threaded, not main</span></span> | <span data-ttu-id="f9fee-126">在目前的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-126">Created in current apartment</span></span>                              | <span data-ttu-id="f9fee-127">在多執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="f9fee-128">在目前的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-128">Created in current apartment</span></span>       | <span data-ttu-id="f9fee-129">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-129">Created in neutral apartment</span></span> | <span data-ttu-id="f9fee-130">在主執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="f9fee-131">單一執行緒、主要</span><span class="sxs-lookup"><span data-stu-id="f9fee-131">Single-threaded, main</span></span>     | <span data-ttu-id="f9fee-132">在目前的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-132">Created in current apartment</span></span>                              | <span data-ttu-id="f9fee-133">在多執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="f9fee-134">在目前的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-134">Created in current apartment</span></span>       | <span data-ttu-id="f9fee-135">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-135">Created in neutral apartment</span></span> | <span data-ttu-id="f9fee-136">在目前的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-136">Created in current apartment</span></span>       |
| <span data-ttu-id="f9fee-137">多執行緒</span><span class="sxs-lookup"><span data-stu-id="f9fee-137">Multithreaded</span></span>             | <span data-ttu-id="f9fee-138">在主機單一執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="f9fee-139">在多執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="f9fee-140">在多執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="f9fee-141">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-141">Created in neutral apartment</span></span> | <span data-ttu-id="f9fee-142">在主執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="f9fee-143">STA 執行緒上的中性 () </span><span class="sxs-lookup"><span data-stu-id="f9fee-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="f9fee-144">在主機單一執行緒的單元中為此執行緒建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="f9fee-145">在多執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="f9fee-146">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-146">Created in neutral apartment</span></span>       | <span data-ttu-id="f9fee-147">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-147">Created in neutral apartment</span></span> | <span data-ttu-id="f9fee-148">在主執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="f9fee-149">MTA 執行緒上的中性 () </span><span class="sxs-lookup"><span data-stu-id="f9fee-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="f9fee-150">在主機單一執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="f9fee-151">在多執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="f9fee-152">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-152">Created in neutral apartment</span></span>       | <span data-ttu-id="f9fee-153">在中立的單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-153">Created in neutral apartment</span></span> | <span data-ttu-id="f9fee-154">在主執行緒單元中建立</span><span class="sxs-lookup"><span data-stu-id="f9fee-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f9fee-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="f9fee-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9fee-156">**>threadingmodel**</span><span class="sxs-lookup"><span data-stu-id="f9fee-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
