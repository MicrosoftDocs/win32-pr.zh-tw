---
title: 介面指標和介面
description: 介面指標和介面
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa23d53f529c43fa7529d657108cc75cb6a23b15
ms.sourcegitcommit: d482e4276cc06515e9fade2f253a257ffc418ce5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2019
ms.locfileid: "106965963"
---
# <a name="interface-pointers-and-interfaces"></a><span data-ttu-id="791f5-103">介面指標和介面</span><span class="sxs-lookup"><span data-stu-id="791f5-103">Interface Pointers and Interfaces</span></span>

<span data-ttu-id="791f5-104">介面實的實例實際上是指向方法指標陣列的指標，也就是參考介面中指定之所有方法的實作為函式資料表。</span><span class="sxs-lookup"><span data-stu-id="791f5-104">An instance of an interface implementation is actually a pointer to an array of pointers to methods - that is, a function table that refers to an implementation of all of the methods specified in the interface.</span></span> <span data-ttu-id="791f5-105">具有多個介面的物件可以提供一個以上的函式資料表指標。</span><span class="sxs-lookup"><span data-stu-id="791f5-105">Objects with multiple interfaces can provide pointers to more than one function table.</span></span> <span data-ttu-id="791f5-106">任何具有可存取陣列之指標的程式碼都可以呼叫該介面中的方法。</span><span class="sxs-lookup"><span data-stu-id="791f5-106">Any code that has a pointer through which it can access the array can call the methods in that interface.</span></span>

<span data-ttu-id="791f5-107">確切地說，這個多個間接取值並不方便，因此在介面函式資料表中，另一個物件必須用來呼叫其方法的指標，就只會被稱為 *介面指標*。</span><span class="sxs-lookup"><span data-stu-id="791f5-107">Speaking precisely about this multiple indirection is inconvenient, so instead, the pointer to the interface function table that another object must have to call its methods is called simply an *interface pointer*.</span></span> <span data-ttu-id="791f5-108">您可以使用 Visual C++ (或其他支援 COM) 的物件導向語言，手動在 C 應用程式中建立函式資料表或幾乎自動建立。</span><span class="sxs-lookup"><span data-stu-id="791f5-108">You can manually create function tables in a C application or almost automatically by using Visual C++ (or other object-oriented languages that support COM).</span></span>

<span data-ttu-id="791f5-109">使用 C 和 c + +) 固有的適當編譯器支援 (，用戶端可以透過其名稱（而不是其在陣列中的位置）來呼叫介面方法。</span><span class="sxs-lookup"><span data-stu-id="791f5-109">With appropriate compiler support (which is inherent in C and C++), a client can call an interface method through its name, not its position in the array.</span></span> <span data-ttu-id="791f5-110">因為介面是一種型別，所以編譯器會提供方法的名稱，可以檢查參數的類型，並傳回每個介面方法呼叫的值。</span><span class="sxs-lookup"><span data-stu-id="791f5-110">Because an interface is a type, the compiler, given the names of methods, can check the types of parameters and return values of each interface method call.</span></span> <span data-ttu-id="791f5-111">相反地，如果用戶端使用以位置為基礎的呼叫配置，則即使是在 C 或 c + + 中，也無法使用這類的類型檢查。</span><span class="sxs-lookup"><span data-stu-id="791f5-111">In contrast, if a client uses a position-based calling scheme, such type-checking is not available, even in C or C++.</span></span>

<span data-ttu-id="791f5-112">每個介面都是一組功能的不可變合約。</span><span class="sxs-lookup"><span data-stu-id="791f5-112">Each interface is an immutable contract of a functional group of methods.</span></span> <span data-ttu-id="791f5-113">您在執行時間使用全域唯一的介面識別碼（ (IID) ）參考介面。</span><span class="sxs-lookup"><span data-stu-id="791f5-113">You reference an interface at run time with a globally unique interface identifier (IID).</span></span> <span data-ttu-id="791f5-114">這個 IID 是 COM 所支援的全域唯一識別碼 (GUID) 的特定實例，可讓用戶端精確地要求物件是否支援介面的語法，而不會產生不必要的額外負荷，也不會造成系統中可能發生的混淆，因為系統不會產生具有相同名稱的多個相同介面版本。</span><span class="sxs-lookup"><span data-stu-id="791f5-114">This IID, which is a specific instance of a globally unique identifier (GUID) supported by COM, allows a client to ask an object precisely whether it supports the semantics of the interface, without unnecessary overhead and without the confusion that could arise in a system from having multiple versions of the same interface with the same name.</span></span>

<span data-ttu-id="791f5-115">總而言之，請務必瞭解 COM 介面是什麼，而不是：</span><span class="sxs-lookup"><span data-stu-id="791f5-115">To summarize, it is important to understand what a COM interface is, and is not:</span></span>

-   <span data-ttu-id="791f5-116">COM 介面與 c + + 類別不同。</span><span class="sxs-lookup"><span data-stu-id="791f5-116">A COM interface is not the same as a C++ class.</span></span> <span data-ttu-id="791f5-117">純虛擬定義不會執行任何工作。</span><span class="sxs-lookup"><span data-stu-id="791f5-117">The pure virtual definition carries no implementation.</span></span> <span data-ttu-id="791f5-118">如果您是 c + + 程式設計人員，您可以將介面的實作為類別來定義，但這會落在未指定 COM 的 [執行詳細資料] 標題下方。</span><span class="sxs-lookup"><span data-stu-id="791f5-118">If you are a C++ programmer, you can define your implementation of an interface as a class, but this falls under the heading of implementation details, which COM does not specify.</span></span> <span data-ttu-id="791f5-119">必須建立物件的實例，這個實例必須要有介面才能實際存在。</span><span class="sxs-lookup"><span data-stu-id="791f5-119">An instance of an object that implements an interface must be created for the interface actually to exist.</span></span> <span data-ttu-id="791f5-120">此外，不同的物件類別可能會以不同的方式來執行介面，但前提是該行為符合介面定義。</span><span class="sxs-lookup"><span data-stu-id="791f5-120">Furthermore, different object classes may implement an interface differently yet be used interchangeably in binary form, as long as the behavior conforms to the interface definition.</span></span>
-   <span data-ttu-id="791f5-121">COM 介面不是物件。</span><span class="sxs-lookup"><span data-stu-id="791f5-121">A COM interface is not an object.</span></span> <span data-ttu-id="791f5-122">這只是一組相關的函式，而且是用戶端和物件用來進行通訊的二進位標準。</span><span class="sxs-lookup"><span data-stu-id="791f5-122">It is simply a related group of functions and is the binary standard through which clients and objects communicate.</span></span> <span data-ttu-id="791f5-123">只要它可以提供介面方法的指標，就可以使用任何內部狀態標記法來執行物件。</span><span class="sxs-lookup"><span data-stu-id="791f5-123">As long as it can provide pointers to interface methods, the object can be implemented in any language with any internal state representation.</span></span>
-   <span data-ttu-id="791f5-124">COM 介面是強型別。</span><span class="sxs-lookup"><span data-stu-id="791f5-124">COM interfaces are strongly typed.</span></span> <span data-ttu-id="791f5-125">每個介面都有它自己的介面識別碼 (GUID) ，這樣可以消除任何其他命名配置可能發生重複的可能性。</span><span class="sxs-lookup"><span data-stu-id="791f5-125">Every interface has its own interface identifier (a GUID), which eliminates the possibility of duplication that could occur with any other naming scheme.</span></span>
-   <span data-ttu-id="791f5-126">COM 介面是不可變的。</span><span class="sxs-lookup"><span data-stu-id="791f5-126">COM interfaces are immutable.</span></span> <span data-ttu-id="791f5-127">您無法定義新版本的舊介面，並為其指定相同的識別碼。</span><span class="sxs-lookup"><span data-stu-id="791f5-127">You cannot define a new version of an old interface and give it the same identifier.</span></span> <span data-ttu-id="791f5-128">新增或移除介面或變更語義的方法，會建立新的介面，而不是新的舊介面版本。</span><span class="sxs-lookup"><span data-stu-id="791f5-128">Adding or removing methods of an interface or changing semantics creates a new interface, not a new version of an old interface.</span></span> <span data-ttu-id="791f5-129">因此，新的介面無法與舊的介面發生衝突。</span><span class="sxs-lookup"><span data-stu-id="791f5-129">Therefore, a new interface cannot conflict with an old interface.</span></span> <span data-ttu-id="791f5-130">不過，物件可以同時支援多個介面，且可以公開具有不同識別碼之介面的後續修訂介面。</span><span class="sxs-lookup"><span data-stu-id="791f5-130">However, objects can support multiple interfaces simultaneously and can expose interfaces that are successive revisions of an interface, with different identifiers.</span></span> <span data-ttu-id="791f5-131">因此，每個介面都是個別的合約，而全系統物件則不需要擔心它們所呼叫的介面版本是否為它們所預期的版本。</span><span class="sxs-lookup"><span data-stu-id="791f5-131">Thus, each interface is a separate contract, and systemwide objects need not be concerned about whether the version of the interface they are calling is the one they expect.</span></span> <span data-ttu-id="791f5-132"> (IID 的介面識別碼) 明確且唯一地定義介面合約。</span><span class="sxs-lookup"><span data-stu-id="791f5-132">The interface ID (IID) defines the interface contract explicitly and uniquely.</span></span>

## <a name="related-topics"></a><span data-ttu-id="791f5-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="791f5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="791f5-134">COM 物件和介面</span><span class="sxs-lookup"><span data-stu-id="791f5-134">COM Objects and Interfaces</span></span>](com-objects-and-interfaces.md)
</dt> </dl>

 

 




