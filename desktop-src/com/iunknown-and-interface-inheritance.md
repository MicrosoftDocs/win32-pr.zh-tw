---
title: IUnknown 和介面繼承
description: IUnknown 和介面繼承
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966272"
---
# <a name="iunknown-and-interface-inheritance"></a><span data-ttu-id="61048-103">IUnknown 和介面繼承</span><span class="sxs-lookup"><span data-stu-id="61048-103">IUnknown and Interface Inheritance</span></span>

<span data-ttu-id="61048-104">COM 中的繼承不表示程式碼重複使用。</span><span class="sxs-lookup"><span data-stu-id="61048-104">Inheritance in COM does not mean code reuse.</span></span> <span data-ttu-id="61048-105">因為沒有任何與介面相關聯的執行，所以介面繼承不表示程式碼繼承。</span><span class="sxs-lookup"><span data-stu-id="61048-105">Because no implementations are associated with interfaces, interface inheritance does not mean code inheritance.</span></span> <span data-ttu-id="61048-106">這表示，只有與介面相關聯的合約會以 c + + 純虛擬基類方式繼承，並修改（藉由加入新的方法或進一步限定允許的方法使用方式）。</span><span class="sxs-lookup"><span data-stu-id="61048-106">It means only that the contract associated with an interface is inherited in a C++ pure-virtual base-class fashion and modified — either by adding new methods or by further qualifying the allowed usage of methods.</span></span> <span data-ttu-id="61048-107">COM 中沒有選擇性繼承。</span><span class="sxs-lookup"><span data-stu-id="61048-107">There is no selective inheritance in COM.</span></span> <span data-ttu-id="61048-108">如果某個介面繼承自另一個介面，則會包含其他介面所定義的所有方法。</span><span class="sxs-lookup"><span data-stu-id="61048-108">If one interface inherits from another, it includes all the methods that the other interface defines.</span></span>

<span data-ttu-id="61048-109">預先定義的 COM 介面會謹慎使用繼承。</span><span class="sxs-lookup"><span data-stu-id="61048-109">Inheritance is used sparingly in the predefined COM interfaces.</span></span> <span data-ttu-id="61048-110">所有預先定義的介面 (以及您定義的任何自訂介面) 都會從重要的介面 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)繼承其定義，其中包含三個重要的方法： [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))、 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。</span><span class="sxs-lookup"><span data-stu-id="61048-110">All predefined interfaces (and any custom interfaces you define) inherit their definitions from the important interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), which contains three vital methods: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref), and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="61048-111">所有 COM 物件都必須執行 **IUnknown** 介面，因為它提供了使用 **QueryInterface** 的方法，可在物件支援的不同介面之間自由移動，以及使用 **AddRef** 和 **Release** 來管理其存留期的方法。</span><span class="sxs-lookup"><span data-stu-id="61048-111">All COM objects must implement the **IUnknown** interface because it provides the means, using **QueryInterface**, to move freely between the different interfaces that an object supports as well as the means to manage its lifetime by using **AddRef** and **Release**.</span></span>

<span data-ttu-id="61048-112">在建立支援 [匯總](aggregation.md)的物件時，您必須為所有介面和獨立 **IUnknown** 介面各執行一組 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)函數。</span><span class="sxs-lookup"><span data-stu-id="61048-112">In creating an object that supports [aggregation](aggregation.md), you would need to implement one set of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) functions for all interfaces as well as a stand-alone **IUnknown** interface.</span></span> <span data-ttu-id="61048-113">在任何情況下，任何物件實作項都會執行 **IUnknown** 方法。</span><span class="sxs-lookup"><span data-stu-id="61048-113">In any case, any object implementor will implement **IUnknown** methods.</span></span> <span data-ttu-id="61048-114">如需詳細資訊，請參閱 [使用和執行 IUnknown](using-and-implementing-iunknown.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="61048-114">See the section [Using and Implementing IUnknown](using-and-implementing-iunknown.md) for more information.</span></span>

<span data-ttu-id="61048-115">雖然有一些介面除了 [**iunknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)之外還會從第二個介面繼承其定義，但大部分只會繼承 **iunknown** 介面方法。</span><span class="sxs-lookup"><span data-stu-id="61048-115">While there are a few interfaces that inherit their definitions from a second interface in addition to [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), the majority simply inherit the **IUnknown** interface methods.</span></span> <span data-ttu-id="61048-116">這使得大部分的介面相對較簡潔，而且容易封裝。</span><span class="sxs-lookup"><span data-stu-id="61048-116">This makes most interfaces relatively compact and easy to encapsulate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61048-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="61048-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61048-118">COM 物件和介面</span><span class="sxs-lookup"><span data-stu-id="61048-118">COM Objects and Interfaces</span></span>](com-objects-and-interfaces.md)
</dt> </dl>

 

 