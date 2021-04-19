---
title: 簡單元素
description: 簡單元素是與其他元素共用 IAccessible 物件的 UI 元素，而且會依賴該 IAccessible 物件 (通常是其父) 來公開其屬性。
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969483"
---
# <a name="simple-elements"></a><span data-ttu-id="8b652-103">簡單元素</span><span class="sxs-lookup"><span data-stu-id="8b652-103">Simple Elements</span></span>

<span data-ttu-id="8b652-104">*簡單元素* 是與其他元素共用 [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)物件的 UI 元素，而且會依賴該 **IAccessible** 物件 (通常是其父) 來公開其屬性。</span><span class="sxs-lookup"><span data-stu-id="8b652-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="8b652-105">為了區分共用 **IAccessible** 物件的元素，伺服器會為每個簡單專案指派一個唯一的正數子識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b652-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="8b652-106">這項指派是依每個實例的介面來完成，因此識別碼在該內容中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8b652-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="8b652-107">許多實作為順序指派這些識別碼，從1開始。</span><span class="sxs-lookup"><span data-stu-id="8b652-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="8b652-108">此配置不允許簡單的元素擁有自己的子系。</span><span class="sxs-lookup"><span data-stu-id="8b652-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="8b652-109">簡單元素也稱為 *子* 系。</span><span class="sxs-lookup"><span data-stu-id="8b652-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="8b652-110">若要唯一識別和公開，簡單元素需要 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件和子系識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b652-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="8b652-111">因此，當與 **IAccessible** 物件通訊時，用戶端必須提供適當的子系識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b652-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="8b652-112">特殊的識別碼（ **CHILDID \_ SELF**）可以用來參考可存取的物件本身，而不是它的其中一個子系。</span><span class="sxs-lookup"><span data-stu-id="8b652-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="8b652-113">在簡單元素之間共用的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 物件通常會對應至使用者介面中的一般父物件。</span><span class="sxs-lookup"><span data-stu-id="8b652-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="8b652-114">例如，系統清單方塊會針對整體清單方塊和每個清單方塊專案的簡單元素公開可存取物件。</span><span class="sxs-lookup"><span data-stu-id="8b652-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="8b652-115">在此情況下，清單方塊的 **IAccessible** 物件也是清單專案的父代或容器。</span><span class="sxs-lookup"><span data-stu-id="8b652-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="8b652-116">如需可存取物件的詳細資訊，請參閱 [可存取的物件](accessible-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="8b652-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 




