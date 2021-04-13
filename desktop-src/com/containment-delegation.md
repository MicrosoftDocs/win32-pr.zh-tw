---
title: 內含專案/委派
description: COM 中物件重複使用最常見的機制是內含專案/委派。
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311295"
---
# <a name="containmentdelegation"></a><span data-ttu-id="55c21-103">內含專案/委派</span><span class="sxs-lookup"><span data-stu-id="55c21-103">Containment/Delegation</span></span>

<span data-ttu-id="55c21-104">COM 中物件重複使用最常見的機制是內含專案 */委派*。</span><span class="sxs-lookup"><span data-stu-id="55c21-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="55c21-105">這種重複使用方式是在大部分物件導向語言和系統中的熟悉概念。</span><span class="sxs-lookup"><span data-stu-id="55c21-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="55c21-106">外部物件（需要利用內建物件）可作為內建物件的物件用戶端。</span><span class="sxs-lookup"><span data-stu-id="55c21-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="55c21-107">外部物件「包含」內建物件，當外部物件需要內建物件的服務時，外部物件會明確地將執行委派給內建物件的方法。</span><span class="sxs-lookup"><span data-stu-id="55c21-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="55c21-108">也就是說，外部物件會使用內建物件的服務來自行執行。</span><span class="sxs-lookup"><span data-stu-id="55c21-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="55c21-109">外部和內建物件不需要支援相同的介面，不過，它一定會合理地包含物件，該物件會執行外部物件不會執行外部物件的介面，並執行外部物件的方法，就像呼叫內建物件中的對應方法一樣。</span><span class="sxs-lookup"><span data-stu-id="55c21-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="55c21-110">但是，如果外部物件和內建物件的複雜性有很大的差異，則外部物件可以藉由將呼叫委派給內建物件中所執行的介面方法，來執行其介面的某些方法。</span><span class="sxs-lookup"><span data-stu-id="55c21-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="55c21-111">執行外部物件的內含專案很簡單。</span><span class="sxs-lookup"><span data-stu-id="55c21-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="55c21-112">外部物件會建立它需要作為任何其他用戶端使用的內建物件。</span><span class="sxs-lookup"><span data-stu-id="55c21-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="55c21-113">這並不是新的，程式就像 c + + 物件，它本身也包含 c + + 字串物件，它會使用它來執行特定的字串函式，即使外部物件不會被視為本身右邊的字串物件。</span><span class="sxs-lookup"><span data-stu-id="55c21-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="55c21-114">然後，使用其對內建物件的指標，在外部物件中呼叫方法時，會產生對內建物件方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="55c21-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55c21-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="55c21-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55c21-116">彙總</span><span class="sxs-lookup"><span data-stu-id="55c21-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




