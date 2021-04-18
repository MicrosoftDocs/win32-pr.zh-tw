---
title: 重複使用物件
description: 重複使用物件
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: 917c90b6ed4af323fedada331211b40396876424
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/08/2020
ms.locfileid: "104507853"
---
# <a name="reusing-objects"></a><span data-ttu-id="f2697-103">重複使用物件</span><span class="sxs-lookup"><span data-stu-id="f2697-103">Reusing Objects</span></span>

<span data-ttu-id="f2697-104">任何物件模型的重要目標，是要讓物件作者能夠重複使用，並將其他人所提供的物件，擴充為其本身的實作為片段。</span><span class="sxs-lookup"><span data-stu-id="f2697-104">An important goal of any object model is to enable object authors to reuse and extend objects provided by others as pieces of their own implementations.</span></span> <span data-ttu-id="f2697-105">在 Microsoft Visual C++ 和其他語言中執行這項作業的其中一種方式，是使用「 *執行繼承*」，這可讓物件繼承 ( 「子類別」 ) 其他物件的部分函數，同時覆寫其他函式。</span><span class="sxs-lookup"><span data-stu-id="f2697-105">One way to do this in Microsoft Visual C++ and other languages is by using *implementation inheritance*, which allows an object to inherit ("subclass") some of its functions from another object while overriding other functions.</span></span>

<span data-ttu-id="f2697-106">使用傳統的實作為繼承的全系統物件互動問題，就是不清楚地定義在執行階層中的物件之間的合約 (介面) 。</span><span class="sxs-lookup"><span data-stu-id="f2697-106">The problem for systemwide object interaction using traditional implementation inheritance is that the contract (the interface) between objects in an implementation hierarchy is not clearly defined.</span></span> <span data-ttu-id="f2697-107">事實上，它是隱含且不明確的。</span><span class="sxs-lookup"><span data-stu-id="f2697-107">In fact, it is implicit and ambiguous.</span></span> <span data-ttu-id="f2697-108">當父系或子物件變更其執行時，相關元件的行為可能會變成未定義或 unstably。</span><span class="sxs-lookup"><span data-stu-id="f2697-108">When the parent or child object changes its implementation, the behavior of related components might become undefined or unstably implemented.</span></span> <span data-ttu-id="f2697-109">在任何單一的應用程式中，只要是可同時更新所有元件的單一工程小組來管理，這不一定是主要的考慮。</span><span class="sxs-lookup"><span data-stu-id="f2697-109">In any single application, where the implementation can be managed by a single engineering team that updates all of the components at the same time, this is not always a major concern.</span></span> <span data-ttu-id="f2697-110">在某個小組元件的環境中，透過以黑色的方式重複使用其他小組所建立的其他元件，這類不穩定危及重複使用。</span><span class="sxs-lookup"><span data-stu-id="f2697-110">In an environment where the components of one team are built through black-box reuse of other components built by other teams, this type of instability jeopardizes reuse.</span></span> <span data-ttu-id="f2697-111">此外，執行繼承通常只能在進程界限內運作。</span><span class="sxs-lookup"><span data-stu-id="f2697-111">Additionally, implementation inheritance usually works only within process boundaries.</span></span> <span data-ttu-id="f2697-112">如此一來，在許多工程團隊所建立的軟體元件所組成的大型、不斷演進的系統中，傳統的執行繼承就不切實際。</span><span class="sxs-lookup"><span data-stu-id="f2697-112">This makes traditional implementation inheritance impractical for large, evolving systems composed of software components built by many engineering teams.</span></span>

<span data-ttu-id="f2697-113">建立可重複使用之元件的關鍵是能夠將物件視為不透明的方塊。</span><span class="sxs-lookup"><span data-stu-id="f2697-113">The key to building reusable components is to be able to treat the object as an opaque box.</span></span> <span data-ttu-id="f2697-114">這表示，嘗試重複使用另一個物件的程式碼，並不知道任何內容，也不需要知道所使用元件的內部結構或實作為。</span><span class="sxs-lookup"><span data-stu-id="f2697-114">This means that the piece of code attempting to reuse another object knows nothing, and needs to know nothing, about the internal structure or implementation of the component being used.</span></span> <span data-ttu-id="f2697-115">換句話說，嘗試重複使用元件的程式碼取決於物件的行為，而不是其實際執行。</span><span class="sxs-lookup"><span data-stu-id="f2697-115">In other words, the code attempting to reuse a component depends on the behavior of the object and not its exact implementation.</span></span>

<span data-ttu-id="f2697-116">為了達到黑箱的重複利用性，COM 採用其他既定的重複利用機制，例如內含專案 */委派* 和 *匯總*。</span><span class="sxs-lookup"><span data-stu-id="f2697-116">To achieve black-box reusability, COM adopts other established reusability mechanisms such as *containment/delegation* and *aggregation*.</span></span>

> [!NOTE]  
> <span data-ttu-id="f2697-117">為了方便起見，要重複使用的物件稱為 *內建物件* ，而使用該內建物件的物件則是 *外部物件*。</span><span class="sxs-lookup"><span data-stu-id="f2697-117">For convenience, the object being reused is called the *inner object* and the object making use of that inner object is the *outer object*.</span></span>

 

<span data-ttu-id="f2697-118">在這兩種機制中，請務必記住外部物件對其用戶端的外觀。</span><span class="sxs-lookup"><span data-stu-id="f2697-118">It is important to remember in both these mechanisms how the outer object appears to its clients.</span></span> <span data-ttu-id="f2697-119">至於用戶端，這兩個物件都會執行用戶端可以取得指標的任何介面。</span><span class="sxs-lookup"><span data-stu-id="f2697-119">As far as the clients are concerned, both objects implement any interfaces to which the client can get a pointer.</span></span> <span data-ttu-id="f2697-120">用戶端會將外部物件視為不透明的方塊，因此不會在意外部 objectâ的內部結構，也不需要在意。」用戶端只在意行為。</span><span class="sxs-lookup"><span data-stu-id="f2697-120">The client treats the outer object as an opaque box and therefore does not care, nor does it need to care, about the internal structure of the outer objectâ€”the client cares only about behavior.</span></span>

<span data-ttu-id="f2697-121">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="f2697-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f2697-122">內含專案/委派</span><span class="sxs-lookup"><span data-stu-id="f2697-122">Containment/Delegation</span></span>](containment-delegation.md)
-   [<span data-ttu-id="f2697-123">彙總</span><span class="sxs-lookup"><span data-stu-id="f2697-123">Aggregation</span></span>](aggregation.md)

 

 




