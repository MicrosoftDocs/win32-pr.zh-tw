---
title: 元件類別管理員執行
description: 當可用的元件數目增加時，管理這些元件會變得越來越困難。 就它們公開的介面以及它們所執行的工作而言，許多元件都提供類似的功能。
ms.assetid: c2c67129-bf19-465b-8354-193922aeafaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2414567beba159c05ea08b3561f0a97ddda1cb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932566"
---
# <a name="component-categories-manager-implementation"></a><span data-ttu-id="79837-104">元件類別管理員執行</span><span class="sxs-lookup"><span data-stu-id="79837-104">Component Categories Manager Implementation</span></span>

<span data-ttu-id="79837-105">當可用的元件數目增加時，管理這些元件會變得越來越困難。</span><span class="sxs-lookup"><span data-stu-id="79837-105">As the number of available components grows, it becomes increasingly difficult to manage these components.</span></span> <span data-ttu-id="79837-106">就它們公開的介面以及它們所執行的工作而言，許多元件都提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="79837-106">In terms of the interfaces they expose as well as the tasks they perform, many components offer similar functionality.</span></span>

<span data-ttu-id="79837-107">通常必須列舉可在特定內容中使用的元件。</span><span class="sxs-lookup"><span data-stu-id="79837-107">It is often necessary to enumerate the components that can be used in a certain context.</span></span> <span data-ttu-id="79837-108">例如，OLE 複合檔案中使用的 [ **插入物件** ] 對話方塊，以及用於 ole 控制項的 [ **插入控制項** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="79837-108">Examples of this are the **Insert Object** dialog box used in OLE compound documents and the **Insert Control** dialog box used in OLE controls.</span></span> <span data-ttu-id="79837-109">這些對話方塊會列出所有符合 (或宣告來滿足複合檔案或控制項之介面合約) 的所有元件。</span><span class="sxs-lookup"><span data-stu-id="79837-109">These dialog boxes list all components that fulfill (or claim to fulfill) the interface contracts for compound documents or controls.</span></span> <span data-ttu-id="79837-110">這些現有的類別 (OLE 檔，OLE 控制項) 不代表確切的介面簽章。</span><span class="sxs-lookup"><span data-stu-id="79837-110">These existing categories (OLE document, OLE control) do not imply an exact interface signature.</span></span> <span data-ttu-id="79837-111">OLE 檔必須公開一組特定的核心介面 (例如 [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) 或 [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)) 但也可以公開其他介面，例如 [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)。</span><span class="sxs-lookup"><span data-stu-id="79837-111">OLE documents have to expose a certain set of core interfaces (for example, [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) or [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)) but can also expose additional interfaces such as [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink).</span></span>

<span data-ttu-id="79837-112">在過去，已標記元件，方法是新增人類可讀取的名稱 ( 「可插入」、「控制項」等等) 作為 **HKEY \_ 類別 \_ 根目錄 \\ CLSID \\ {...}** 的子機碼</span><span class="sxs-lookup"><span data-stu-id="79837-112">In the past, components have been tagged by adding a human-readable name ("Insertable", "Control", and so on) as a subkey to the **HKEY\_CLASSES\_ROOT\\CLSID\\{...}**</span></span> <span data-ttu-id="79837-113">對應至元件的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="79837-113">registry key corresponding to the component.</span></span> <span data-ttu-id="79837-114">這適用于類別的集中定義，但在許多獨立的合作物件定義新類別時，會產生風險名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="79837-114">This works well for a central definition of categories but risks name collisions when many independent parties define new categories.</span></span> <span data-ttu-id="79837-115">在 COM 的其他區域中，提供可延伸命名空間的解決方案是使用全域唯一識別碼 (Guid) 。</span><span class="sxs-lookup"><span data-stu-id="79837-115">As in other areas of COM, the solution to providing an extensible namespace lies in the use of globally unique identifiers (GUIDs).</span></span> <span data-ttu-id="79837-116">與其使用人類看得懂的名稱， (CATID) 的唯一數目會指派給每個類別。</span><span class="sxs-lookup"><span data-stu-id="79837-116">Instead of using a human-readable name, a unique number (CATID) is assigned to each category.</span></span>

<span data-ttu-id="79837-117">現有分類的另一項限制是僅限於表示元件本身的功能。</span><span class="sxs-lookup"><span data-stu-id="79837-117">Another limitation with the existing categorization is that it is limited to expressing the capabilities of the component itself.</span></span> <span data-ttu-id="79837-118">許多元件需要容器的特定功能。</span><span class="sxs-lookup"><span data-stu-id="79837-118">Many components require certain capabilities from the containers.</span></span> <span data-ttu-id="79837-119">將這類元件插入容器時，插入可能會失敗或非預期的行為，即使元件符合其中一個類別所隱含的合約也一樣。</span><span class="sxs-lookup"><span data-stu-id="79837-119">When such a component is inserted into a container, the insertion can fail or behave unexpectedly, even though the component fulfills the contracts implied by one of its categories.</span></span> <span data-ttu-id="79837-120">若要列舉在某些情況下可以成功使用的元件，必須考慮元件和容器的功能。</span><span class="sxs-lookup"><span data-stu-id="79837-120">To enumerate the components that can be used successfully in certain situations, the capabilities of both the component and the container must be considered.</span></span>

<span data-ttu-id="79837-121">基於這些考慮，已對現有的分類進行下列變更：</span><span class="sxs-lookup"><span data-stu-id="79837-121">Because of these considerations, the following changes were made to the existing categorization:</span></span>

-   <span data-ttu-id="79837-122">類別是使用全域唯一識別碼的 Catid 來表示。</span><span class="sxs-lookup"><span data-stu-id="79837-122">Categories are indicated by using CATIDs that are globally unique identifiers.</span></span>
-   <span data-ttu-id="79837-123">在 **HKEY \_ 類別 \_ 根 \\ CLSID** 登錄機碼的 **元件** 子機碼底下，已開發兩個不同的子機碼：「實作為類別」和「必要類別」。</span><span class="sxs-lookup"><span data-stu-id="79837-123">Under the **Components** subkey of the **HKEY\_CLASSES\_ROOT\\CLSID** registry key, two separate subkeys, "Implemented Categories" and "Required Categories", were developed.</span></span> <span data-ttu-id="79837-124">這些子機碼包含元件所提供的 Catid 清單，或元件的容器必須提供的清單。</span><span class="sxs-lookup"><span data-stu-id="79837-124">These subkeys contain the lists of CATIDs that are provided by the component or that the container of the component must provide.</span></span>

<span data-ttu-id="79837-125">為了簡化元件類別的管理，類別會列在登錄： **HKEY \_ 類別的 \_ 根 \\ 元件類別** 的集中位置。</span><span class="sxs-lookup"><span data-stu-id="79837-125">To ease managing the component categories, categories are listed in a central place in the registry: **HKEY\_CLASSES\_ROOT\\Component Categories**.</span></span> <span data-ttu-id="79837-126">此索引鍵會列出已安裝的類別及其 CATID 以及當地語系化、人們看得懂的名稱。</span><span class="sxs-lookup"><span data-stu-id="79837-126">This key lists the installed categories both with their CATID and with localized, human-readable names.</span></span>

<span data-ttu-id="79837-127">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="79837-127">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="79837-128">依元件功能分類</span><span class="sxs-lookup"><span data-stu-id="79837-128">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
-   [<span data-ttu-id="79837-129">依容器功能分類</span><span class="sxs-lookup"><span data-stu-id="79837-129">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
-   [<span data-ttu-id="79837-130">元件類別管理員</span><span class="sxs-lookup"><span data-stu-id="79837-130">The Component Categories Manager</span></span>](the-component-categories-manager.md)
-   [<span data-ttu-id="79837-131">預設類別和關聯</span><span class="sxs-lookup"><span data-stu-id="79837-131">Default Classes and Associations</span></span>](default-classes-and-associations.md)
-   [<span data-ttu-id="79837-132">定義元件類別</span><span class="sxs-lookup"><span data-stu-id="79837-132">Defining Component Categories</span></span>](defining-component-categories.md)
-   [<span data-ttu-id="79837-133">將圖示與類別產生關聯</span><span class="sxs-lookup"><span data-stu-id="79837-133">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)

 

 




