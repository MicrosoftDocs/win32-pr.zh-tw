---
title: 動態輔助類別
description: 類似于結構化和抽象物件類別，輔助類別是由 Active Directory 架構中的 classSchema 物件所定義。
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- 動態輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462876"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="2b0e5-104">動態輔助類別</span><span class="sxs-lookup"><span data-stu-id="2b0e5-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="2b0e5-105">類似于結構化和抽象物件類別，輔助類別是由 Active Directory 架構中的 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 物件所定義。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="2b0e5-106">如需詳細資訊，請參閱 [結構化、抽象概念和輔助類別](structural-abstract-and-auxiliary-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="2b0e5-107">此架構定義會指定類別的各種特性，包括與類別相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="2b0e5-108">不同于結構化類別，您無法建立輔助類別的實例，就像您可以使用結構化類別一樣。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="2b0e5-109">相反地，您可以使用輔助類別來擴充與另一個結構化、抽象或輔助物件類別相關聯的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="2b0e5-110">在 Windows 2000 的初始版本中，Active Directory Domain Services 提供將輔助類別靜態連結至另一個物件類別之 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 定義的支援。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="2b0e5-111">以這種方式使用輔助類別時，物件類別的每個實例都支援輔助類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="2b0e5-112">**Windows 2000 伺服器和較早版本：** Active Directory Domain Services 不會提供將輔助類別動態連結至個別物件的支援，而不是只支援整個物件類別。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="2b0e5-113">此外，附加至物件實例的輔助類別，之後無法從實例中移除。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="2b0e5-114">**Windows Server 2003：** 當樹系中的所有網域控制站都執行 Windows Server 2003 且樹系功能模式為 Windows Server 2003 時，就會支援動態輔助類別。</span><span class="sxs-lookup"><span data-stu-id="2b0e5-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="2b0e5-115">如需輔助類別的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="2b0e5-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="2b0e5-116">動態連結的輔助類別</span><span class="sxs-lookup"><span data-stu-id="2b0e5-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="2b0e5-117">靜態連結的輔助類別</span><span class="sxs-lookup"><span data-stu-id="2b0e5-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="2b0e5-118">判斷與物件實例相關聯的類別</span><span class="sxs-lookup"><span data-stu-id="2b0e5-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="2b0e5-119">將輔助類別加入至物件實例</span><span class="sxs-lookup"><span data-stu-id="2b0e5-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="2b0e5-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span><span class="sxs-lookup"><span data-stu-id="2b0e5-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 