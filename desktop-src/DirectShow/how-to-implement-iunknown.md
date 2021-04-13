---
description: 如何執行 IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: 如何執行 IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509786"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="ecbe0-103">如何執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecbe0-103">How to Implement IUnknown</span></span>

<span data-ttu-id="ecbe0-104">Microsoft DirectShow 是以元件物件模型 (COM) 為基礎。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="ecbe0-105">如果您撰寫自己的篩選準則，則必須將它實作為 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="ecbe0-106">DirectShow 基類提供可從中進行此作業的架構。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="ecbe0-107">不需要使用基類，但可以簡化開發流程。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="ecbe0-108">本文說明 COM 物件的一些內部詳細資料，以及它們在 DirectShow 基類中的實作為。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="ecbe0-109">本文假設您已瞭解如何程式設計 COM 用戶端應用程式（亦即，您瞭解 **IUnknown** 中的方法），但不會假設任何先前的開發 com 物件體驗。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="ecbe0-110">DirectShow 處理許多開發 COM 物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="ecbe0-111">如果您有開發 COM 物件的經驗，請參閱 [使用 CUnknown](using-cunknown.md)的章節，其中描述 [**CUnknown**](cunknown.md) 基類。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="ecbe0-112">COM 是一種規格，不是實作為。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="ecbe0-113">它會定義元件必須遵循的規則;讓這些規則生效，讓開發人員得以運用。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="ecbe0-114">在 DirectShow 中，所有物件都衍生自一組 c + + 基類。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="ecbe0-115">基底類別的函式和方法會執行大部分的 COM "簿記" 工作，例如保留一致的參考計數。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="ecbe0-116">藉由從基類衍生您的篩選，您就可以繼承類別的功能。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="ecbe0-117">若要有效地使用基類，您需要先瞭解它們如何實行 COM 規格。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="ecbe0-118">本文包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="ecbe0-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="ecbe0-119">IUnknown 的運作方式</span><span class="sxs-lookup"><span data-stu-id="ecbe0-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="ecbe0-120">使用 CUnknown</span><span class="sxs-lookup"><span data-stu-id="ecbe0-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="ecbe0-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ecbe0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecbe0-122">DirectShow 和 COM</span><span class="sxs-lookup"><span data-stu-id="ecbe0-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



