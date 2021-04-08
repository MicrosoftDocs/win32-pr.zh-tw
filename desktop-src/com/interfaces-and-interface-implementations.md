---
title: 介面和介面的實現
description: COM 會在介面定義和其實作為之間進行基本的區別。
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8df92ac8b851925d82a4b03505fa4c5ab3dc39
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2020
ms.locfileid: "104023145"
---
# <a name="interfaces-and-interface-implementations"></a><span data-ttu-id="d57e8-103">介面和介面的實現</span><span class="sxs-lookup"><span data-stu-id="d57e8-103">Interfaces and Interface Implementations</span></span>

<span data-ttu-id="d57e8-104">COM 會在介面定義和其實作為之間進行基本的區別。</span><span class="sxs-lookup"><span data-stu-id="d57e8-104">COM makes a fundamental distinction between interface definitions and their implementations.</span></span>

<span data-ttu-id="d57e8-105">*介面* 實際上是由一組相關的函式原型所組成的合約，其使用方式是已定義的，但其執行不是。</span><span class="sxs-lookup"><span data-stu-id="d57e8-105">An *interface* is actually a contract that consists of a group of related function prototypes whose usage is defined but whose implementation is not.</span></span> <span data-ttu-id="d57e8-106">這些函數原型相當於 c + + 程式設計中的純虛擬基類。</span><span class="sxs-lookup"><span data-stu-id="d57e8-106">These function prototypes are equivalent to pure virtual base classes in C++ programming.</span></span> <span data-ttu-id="d57e8-107">介面定義會指定介面的成員函式，稱為 *方法*、其傳回類型、參數的數目和類型，以及它們必須做的動作。</span><span class="sxs-lookup"><span data-stu-id="d57e8-107">An interface definition specifies the interface's member functions, called *methods*, their return types, the number and types of their parameters, and what they must do.</span></span> <span data-ttu-id="d57e8-108">沒有與介面相關聯的執行。</span><span class="sxs-lookup"><span data-stu-id="d57e8-108">There is no implementation associated with an interface.</span></span>

<span data-ttu-id="d57e8-109">*介面實* 作為程式設計師提供的程式碼，用來執行介面定義中指定的動作。</span><span class="sxs-lookup"><span data-stu-id="d57e8-109">An *interface implementation* is the code a programmer supplies to carry out the actions specified in an interface definition.</span></span> <span data-ttu-id="d57e8-110">程式設計人員可以在以物件為基礎的應用程式中使用的許多介面，都包含在 COM 程式庫中。</span><span class="sxs-lookup"><span data-stu-id="d57e8-110">Implementations of many of the interfaces a programmer can use in an object-based application are included in the COM libraries.</span></span> <span data-ttu-id="d57e8-111">不過，程式設計人員可以自由地忽略這些實作為並撰寫自己的。</span><span class="sxs-lookup"><span data-stu-id="d57e8-111">However, programmers are free to ignore these implementations and write their own.</span></span> <span data-ttu-id="d57e8-112">當建立物件的實例時，介面的執行會與物件產生關聯，而該執行會提供物件所提供的服務。</span><span class="sxs-lookup"><span data-stu-id="d57e8-112">An interface implementation is to be associated with an object when an instance of that object is created, and the implementation provides the services that the object offers.</span></span>

<span data-ttu-id="d57e8-113">例如，名為 IStack 的假設介面可能會定義兩個方法，名為 Push 和 Pop，指定連續呼叫 Pop 方法會以反向順序傳回先前傳遞給 Push 方法的值。</span><span class="sxs-lookup"><span data-stu-id="d57e8-113">For example, a hypothetical interface named IStack might define two methods, named Push and Pop, specifying that successive calls to the Pop method return, in reverse order, values previously passed to the Push method.</span></span> <span data-ttu-id="d57e8-114">此介面定義不會指定如何在程式碼中執行函數。</span><span class="sxs-lookup"><span data-stu-id="d57e8-114">This interface definition would not specify how the functions are to be implemented in code.</span></span> <span data-ttu-id="d57e8-115">在執行介面時，程式設計人員可能會將堆疊實作為陣列，並以存取該陣列的方式來執行 Push 和 Pop 方法，而另一位程式設計人員可能會使用連結的清單，並據此執行方法。</span><span class="sxs-lookup"><span data-stu-id="d57e8-115">In implementing the interface, one programmer might implement the stack as an array and implement the Push and Pop methods in such a way as to access that array, while another programmer might use a linked list and would implement the methods accordingly.</span></span> <span data-ttu-id="d57e8-116">無論推送和 Pop 方法的特定執行方式為何，IStack 介面指標的記憶體內標記法，以及用戶端所使用的，都完全由介面定義來決定。</span><span class="sxs-lookup"><span data-stu-id="d57e8-116">Regardless of a particular implementation of the Push and Pop methods, the in-memory representation of a pointer to an IStack interface, and therefore its use by a client, is completely determined by the interface definition.</span></span>

<span data-ttu-id="d57e8-117">簡單物件只支援單一介面。</span><span class="sxs-lookup"><span data-stu-id="d57e8-117">Simple objects support only a single interface.</span></span> <span data-ttu-id="d57e8-118">更複雜的物件（例如内嵌物件）通常支援數個介面。</span><span class="sxs-lookup"><span data-stu-id="d57e8-118">More complicated objects, such as embeddable objects, typically support several interfaces.</span></span> <span data-ttu-id="d57e8-119">用戶端只能透過其中一個介面的指標存取 COM 物件，而後者可讓用戶端呼叫任何組成該介面的方法。</span><span class="sxs-lookup"><span data-stu-id="d57e8-119">Clients have access to a COM object only through a pointer to one of its interfaces, which, in turn, allows the client to call any of the methods that make up that interface.</span></span> <span data-ttu-id="d57e8-120">這些方法會決定用戶端如何使用物件的資料。</span><span class="sxs-lookup"><span data-stu-id="d57e8-120">These methods determine how a client can use the object's data.</span></span>

<span data-ttu-id="d57e8-121">介面會定義物件與其用戶端之間的合約。</span><span class="sxs-lookup"><span data-stu-id="d57e8-121">Interfaces define a contract between an object and its clients.</span></span> <span data-ttu-id="d57e8-122">合約會指定必須與每個介面相關聯的方法，以及每個方法的行為在輸入和輸出方面必須有何關聯性。</span><span class="sxs-lookup"><span data-stu-id="d57e8-122">The contract specifies the methods that must be associated with each interface and what the behavior of each of the methods must be in terms of input and output.</span></span> <span data-ttu-id="d57e8-123">合約通常不會定義如何在介面中執行方法。</span><span class="sxs-lookup"><span data-stu-id="d57e8-123">The contract generally does not define how to implement the methods in an interface.</span></span> <span data-ttu-id="d57e8-124">合約的另一個重要層面是，如果物件支援介面，則必須以某種方式支援該介面的所有方法。</span><span class="sxs-lookup"><span data-stu-id="d57e8-124">Another important aspect of the contract is that if an object supports an interface, it must support all of that interface's methods in some way.</span></span> <span data-ttu-id="d57e8-125">並非所有方法都必須執行某些動作。</span><span class="sxs-lookup"><span data-stu-id="d57e8-125">Not all of the methods in an implementation need to do something.</span></span> <span data-ttu-id="d57e8-126">如果物件不支援方法所隱含的函式，則其實作為簡單的傳回，或可能會傳回有意義的錯誤訊息，但這些方法必須存在。</span><span class="sxs-lookup"><span data-stu-id="d57e8-126">If an object does not support the function implied by a method, its implementation may be a simple return or perhaps the return of a meaningful error message—but the methods must exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d57e8-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d57e8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d57e8-128">COM 物件和介面</span><span class="sxs-lookup"><span data-stu-id="d57e8-128">COM Objects and Interfaces</span></span>](com-objects-and-interfaces.md)
</dt> </dl>

 

 




