---
title: 類別、物件和介面
description: 類別、物件和介面
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104463905"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="6a267-103">類別、物件和介面</span><span class="sxs-lookup"><span data-stu-id="6a267-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="6a267-104">在 c + + 程式設計語言中， *類別* 是由 *屬性* (或成員資料) 和 *方法*)  (或成員函式所組成。</span><span class="sxs-lookup"><span data-stu-id="6a267-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="6a267-105">這些屬性是資料元素，例如結構中所包含的專案。</span><span class="sxs-lookup"><span data-stu-id="6a267-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="6a267-106">這些方法會用於各種用途，例如初始化、指派、作業和資料存取。</span><span class="sxs-lookup"><span data-stu-id="6a267-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="6a267-107">使用類別宣告的方式，與使用結構宣告的方式相同。</span><span class="sxs-lookup"><span data-stu-id="6a267-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="6a267-108">當您定義類別 *物件* 時，會為類別配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="6a267-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="6a267-109">每個類別物件都有其屬性的資料區域，以及它所支援之方法的指標資料表。</span><span class="sxs-lookup"><span data-stu-id="6a267-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="6a267-110">在 OLE 中，物件是由資料和方法所組成，就像在 c + + 中一樣。</span><span class="sxs-lookup"><span data-stu-id="6a267-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="6a267-111">不過，OLE 物件會遵守更嚴格的規則。</span><span class="sxs-lookup"><span data-stu-id="6a267-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="6a267-112">資料完全是內部的。</span><span class="sxs-lookup"><span data-stu-id="6a267-112">The data is strictly internal.</span></span> <span data-ttu-id="6a267-113">物件只會公開介面。</span><span class="sxs-lookup"><span data-stu-id="6a267-113">An object only exposes interfaces.</span></span> <span data-ttu-id="6a267-114">*介面* 是一組物件的相關方法。</span><span class="sxs-lookup"><span data-stu-id="6a267-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="6a267-115">每個物件都可以支援多個介面。</span><span class="sxs-lookup"><span data-stu-id="6a267-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="6a267-116">所有 OLE 介面都支援 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。</span><span class="sxs-lookup"><span data-stu-id="6a267-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




