---
title: 專案的名字
description: 另一個已執行 OLE 的標記類別是專案標記，可用來識別包含在另一個物件中的物件。
ms.assetid: ddcf3669-4ad0-4a4e-80a6-eb78058cff09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b692502ba44519a2c51a661ef62a51e133ac04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967395"
---
# <a name="item-monikers"></a><span data-ttu-id="5118d-103">專案的名字</span><span class="sxs-lookup"><span data-stu-id="5118d-103">Item Monikers</span></span>

<span data-ttu-id="5118d-104">另一個已執行 OLE 的標記類別是 *專案標記*，可用來識別包含在另一個物件中的物件。</span><span class="sxs-lookup"><span data-stu-id="5118d-104">Another OLE-implemented moniker class is the *item moniker*, which can be used to identify an object contained in another object.</span></span> <span data-ttu-id="5118d-105">其中一種包含的物件是內嵌在複合檔案中的 OLE 物件。</span><span class="sxs-lookup"><span data-stu-id="5118d-105">One type of contained object is an OLE object embedded in a compound document.</span></span> <span data-ttu-id="5118d-106">複合檔案可以藉由將任意名稱（例如 "embedobj1"、"embedobj2" 等等）指派給每一個，來識別它所包含的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="5118d-106">A compound document could identify the embedded objects it contains by assigning each one an arbitrary name, such as "embedobj1," "embedobj2," and so forth.</span></span> <span data-ttu-id="5118d-107">另一種類型的包含物件是檔中的使用者選取專案，例如試算表中的資料格範圍，或文字檔中的字元範圍。</span><span class="sxs-lookup"><span data-stu-id="5118d-107">Another type of contained object is a user selection in a document, such as a range of cells in a spreadsheet or a range of characters in a text document.</span></span> <span data-ttu-id="5118d-108">包含選取專案的物件稱為 *虛擬物件* ，因為它不會被視為相異物件，直到使用者標示選取範圍為止。</span><span class="sxs-lookup"><span data-stu-id="5118d-108">An object that consists of a selection is called a *pseudo-object* because it isn't treated as a distinct object until a user marks the selection.</span></span> <span data-ttu-id="5118d-109">試算表可能會使用名稱（例如 "1A： 7F"）來識別儲存格範圍，而文字處理檔可能會使用書簽的名稱來識別字元範圍。</span><span class="sxs-lookup"><span data-stu-id="5118d-109">A spreadsheet might identify a cell range using a name such as "1A:7F," while a word processing document might identify a range of characters using the name of a bookmark.</span></span>

<span data-ttu-id="5118d-110">專案的標記主要適用于串連或 *組成* 的另一個標記，以識別容器。</span><span class="sxs-lookup"><span data-stu-id="5118d-110">An item moniker is useful primarily when concatenated, or *composed*, with another moniker, one that identifies the container.</span></span> <span data-ttu-id="5118d-111">通常會建立專案的名字標記，然後將它組成 (例如) 檔案的標記，以建立與物件之完整路徑相等的專案。</span><span class="sxs-lookup"><span data-stu-id="5118d-111">An item moniker is usually created and then composed onto (for example) a file moniker to create the equivalent of a complete path to the object.</span></span> <span data-ttu-id="5118d-112">例如，您可以撰寫檔案標記 "c： \\ work \\report.doc" (它會識別容器物件) 具有專案標記 "embedobj1" (這會識別容器內的物件，) 可 \\ \\ \\ 唯一識別特定檔案中的特定物件。</span><span class="sxs-lookup"><span data-stu-id="5118d-112">For example, you can compose the file moniker "c:\\work\\report.doc" (which identifies the container object) with the item moniker "embedobj1" (which identifies an object within the container) to form the moniker "c:\\work\\report.doc\\embedobj1," which uniquely identifies a particular object within a particular file.</span></span> <span data-ttu-id="5118d-113">您也可以串連其他專案的專案識別碼，以識別深層嵌套的物件。</span><span class="sxs-lookup"><span data-stu-id="5118d-113">You can also concatenate additional item monikers to identify deeply nested objects.</span></span> <span data-ttu-id="5118d-114">例如，如果 "embedobj1" 是試算表物件的名稱，若要在該試算表物件中識別特定範圍的資料格，您可以附加另一個專案的標記，以建立相當於 "c： \\ work \\report.doc\\ Embedobj1 \\ 1a： 7F" 的標記。</span><span class="sxs-lookup"><span data-stu-id="5118d-114">For example, if "embedobj1" is the name of a spreadsheet object, to identify a certain range of cells in that spreadsheet object you could append another item moniker to create a moniker that would be the equivalent of "c:\\work\\report.doc\\embedobj1\\1A:7F."</span></span>

<span data-ttu-id="5118d-115">結合檔案的標記時，專案的標記會形成完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="5118d-115">When combined with a file moniker, an item moniker forms a complete path.</span></span> <span data-ttu-id="5118d-116">專案的名字標記會將路徑名稱的概念延伸到檔案系統之外，並定義路徑名稱來識別個別物件，而不只是檔案。</span><span class="sxs-lookup"><span data-stu-id="5118d-116">Item monikers thus extend the notion of path names beyond the file system, defining path names to identify individual objects, not just files.</span></span>

<span data-ttu-id="5118d-117">專案的名字和檔案的名字之間有顯著的差異。</span><span class="sxs-lookup"><span data-stu-id="5118d-117">There is a significant difference between an item moniker and a file moniker.</span></span> <span data-ttu-id="5118d-118">檔案標記中包含的路徑對了解檔案系統的任何人都有意義，而專案標記中包含的部分路徑只對特定的容器有意義。</span><span class="sxs-lookup"><span data-stu-id="5118d-118">The path contained in a file moniker is meaningful to anyone who understands the file system, while the partial path contained in an item moniker is meaningful only to a particular container.</span></span> <span data-ttu-id="5118d-119">每個人都知道 "c： \\ work \\report.doc" 的參考，但只有一個特定的容器物件知道 "1A： 7F" 的參考。</span><span class="sxs-lookup"><span data-stu-id="5118d-119">Everyone knows what "c:\\work\\report.doc" refers to, but only one particular container object knows what "1A:7F" refers to.</span></span> <span data-ttu-id="5118d-120">一個容器無法解讀另一個應用程式所建立的專案標記;唯一知道專案標記所參考之物件的容器是一開始將專案標記指派給物件的容器。</span><span class="sxs-lookup"><span data-stu-id="5118d-120">One container cannot interpret an item moniker created by another application; the only container that knows which object is referred to by an item moniker is the container that assigned the item moniker to the object in the first place.</span></span> <span data-ttu-id="5118d-121">基於這個理由，藉由檔案和專案標記的組合所命名的物件來源，不僅必須實 [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)，也不能用來系結檔案的名字標記，還可以 [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) 在檔案內容中，協助將專案標記的名稱解析為適當的物件。</span><span class="sxs-lookup"><span data-stu-id="5118d-121">For this reason, the source of the object named by the combination of a file and item moniker must not only implement [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile), to facilitate binding the file moniker, but also [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer) to facilitate resolving the name of the item moniker into the appropriate object, in the context of a file.</span></span>

<span data-ttu-id="5118d-122">使用標記的優點是，只要專案的名字標記是複合專案的一部分，使用「標記」（item）來尋找物件的使用者就不需要瞭解專案標記中包含的名稱。</span><span class="sxs-lookup"><span data-stu-id="5118d-122">The advantage of monikers is that someone using a moniker to locate an object doesn't need to understand the name contained within the item moniker, as long as the item moniker is part of a composite.</span></span> <span data-ttu-id="5118d-123">一般情況下，專案的標記本身本身並不合理。</span><span class="sxs-lookup"><span data-stu-id="5118d-123">Generally, it would not make sense for an item moniker to exist on its own.</span></span> <span data-ttu-id="5118d-124">相反地，您會將專案標記撰寫至檔案的標記。</span><span class="sxs-lookup"><span data-stu-id="5118d-124">Instead, you would compose an item moniker onto a file moniker.</span></span> <span data-ttu-id="5118d-125">然後，您會在複合上呼叫 [**IMoniker：： BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) ，以系結其內的個別名字，並解讀名稱。</span><span class="sxs-lookup"><span data-stu-id="5118d-125">You would then call [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on the composite, which binds the individual monikers within it, interpreting the names.</span></span>

<span data-ttu-id="5118d-126">為了建立專案的「名字標記」物件，並將其指標傳回至「標記提供者」，OLE 提供 helper 函數 [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)。</span><span class="sxs-lookup"><span data-stu-id="5118d-126">To create an item moniker object and return its pointer to the moniker provider, OLE provides the helper function [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker).</span></span> <span data-ttu-id="5118d-127">此函式會建立專案的標記物件，並將其指標傳回給提供者。</span><span class="sxs-lookup"><span data-stu-id="5118d-127">This function creates an item moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5118d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="5118d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5118d-129">反標記</span><span class="sxs-lookup"><span data-stu-id="5118d-129">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="5118d-130">類別名字標記</span><span class="sxs-lookup"><span data-stu-id="5118d-130">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="5118d-131">複合的名字</span><span class="sxs-lookup"><span data-stu-id="5118d-131">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="5118d-132">檔案名字</span><span class="sxs-lookup"><span data-stu-id="5118d-132">File Monikers</span></span>](file-monikers.md)
</dt> <dt>

[<span data-ttu-id="5118d-133">指標標記</span><span class="sxs-lookup"><span data-stu-id="5118d-133">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




