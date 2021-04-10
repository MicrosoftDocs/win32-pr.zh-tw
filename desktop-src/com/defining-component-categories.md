---
title: 定義元件類別
description: 定義元件類別
ms.assetid: 2d67a998-5200-4285-bd99-48cf59683569
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4609654827789949705a2f32803c154152d3f9c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184184"
---
# <a name="defining-component-categories"></a><span data-ttu-id="e5fdf-103">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="e5fdf-103">Defining Component Categories</span></span>

<span data-ttu-id="e5fdf-104">元件類別定義的作者會建立唯一的 GUID (與定義一起發行的 CATID) 。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-104">The author of a component category definition creates a unique GUID (the CATID) that is published along with the definition.</span></span> <span data-ttu-id="e5fdf-105">其他合作物件知道此類型的定義，而且可以據此使用其支援的類別。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-105">Other parties know the definition of this type and can make use of its supported classes accordingly.</span></span> <span data-ttu-id="e5fdf-106">如同介面的方法簽章，在安裝之後，不應該修改分類的語法。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-106">Like the method signature of an interface, a category's semantics should not be modified after being installed.</span></span> <span data-ttu-id="e5fdf-107">藉由引進具有修訂之語義的新分類識別碼，最好是維持類別的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-107">It is better to maintain backward compatibility of the category by introducing a new category identifier with revised semantics.</span></span>

<span data-ttu-id="e5fdf-108">因為介面識別碼 (IID) 和元件類別識別碼 (CATID) 存在於不同的命名空間中，所以看起來像是可以針對 IID 和 CATID 使用相同的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-108">Because interface identifiers (IID) and component category identifiers (CATID) exist in different namespaces, it seems as if it would be possible to use the same GUID for both an IID and a CATID.</span></span> <span data-ttu-id="e5fdf-109">不過，由於 Iid 通常用於介面之 proxy/stub 伺服器的 CLSID，因此可能會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-109">However, since IIDs are often used for the CLSID of the interface's proxy/stub server, there is the potential for conflict.</span></span> <span data-ttu-id="e5fdf-110">因此，請不要對 IID 和 CATID 使用相同的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e5fdf-110">Therefore, do not use the same GUID for an IID and CATID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5fdf-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e5fdf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5fdf-112">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="e5fdf-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-113">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="e5fdf-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-114">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="e5fdf-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-115">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="e5fdf-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="e5fdf-116">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="e5fdf-116">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




