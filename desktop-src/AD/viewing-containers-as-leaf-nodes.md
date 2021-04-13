---
title: 以分葉節點形式來查看容器
description: Active Directory Domain Services 中的任何物件都可以是其他物件的容器。
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- 以分葉節點形式來查看容器
- 容器廣告，作為分葉節點來查看
- 分葉廣告，以分葉節點形式來查看容器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314599"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="589bb-106">以分葉節點形式來查看容器</span><span class="sxs-lookup"><span data-stu-id="589bb-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="589bb-107">Active Directory Domain Services 中的任何物件都可以是其他物件的容器。</span><span class="sxs-lookup"><span data-stu-id="589bb-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="589bb-108">這可能會讓使用者介面雜亂，因此可以宣告特定類別的物件只在使用者介面中顯示為分葉。</span><span class="sxs-lookup"><span data-stu-id="589bb-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="589bb-109">**TreatAsLeaf** 屬性是單一值的顯示規範屬性，可判斷該類別的物件是否應該只顯示為分葉物件。</span><span class="sxs-lookup"><span data-stu-id="589bb-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="589bb-110">這個屬性是布林值，如果 **為 TRUE**，表示類別的物件應該只顯示為分葉元素。</span><span class="sxs-lookup"><span data-stu-id="589bb-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="589bb-111">如果 **為 FALSE**，表示類別的物件可以顯示為容器或分葉。</span><span class="sxs-lookup"><span data-stu-id="589bb-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="589bb-112">如同所有顯示規範屬性， **treatAsLeaf** 屬性是根據每個地區設定來設定，因此此屬性可以視需要當地語系化。</span><span class="sxs-lookup"><span data-stu-id="589bb-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="589bb-113">例如，英文地區設定 (0409) 顯示規範的 **使用者顯示** 預設會將 **treatAsLeaf** 屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="589bb-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="589bb-114">這會導致使用者介面將所有 **使用者** 物件顯示為分葉物件。</span><span class="sxs-lookup"><span data-stu-id="589bb-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="589bb-115">**若要設定 **treatAsLeaf** 屬性的值**</span><span class="sxs-lookup"><span data-stu-id="589bb-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="589bb-116">系結至所需的地區設定中所需的顯示內容。</span><span class="sxs-lookup"><span data-stu-id="589bb-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="589bb-117">如需詳細資訊和程式碼範例，請參閱 [DisplaySpecifiers 容器](displayspecifiers-container.md)。</span><span class="sxs-lookup"><span data-stu-id="589bb-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="589bb-118">使用 [**IADs：:P**](/windows/desktop/api/iads/nf-iads-iads-put) 的錯誤方法，將 **treatAsLeaf** 屬性設定為 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="589bb-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="589bb-119">若要認可目錄的變更，請呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="589bb-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 