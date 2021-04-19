---
description: Windows Installer 會保留關係資料庫中安裝的所有相關資訊。 您可以使用轉換和合併來修改此資料庫，因此也可以進行安裝。
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: 合併和轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990459"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="3de80-104">合併和轉換</span><span class="sxs-lookup"><span data-stu-id="3de80-104">Merges and Transforms</span></span>

<span data-ttu-id="3de80-105">Windows Installer 會保留關係資料庫中安裝的所有相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3de80-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="3de80-106">您可以使用轉換和合併來修改此資料庫，因此也可以進行安裝。</span><span class="sxs-lookup"><span data-stu-id="3de80-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="3de80-107">轉換</span><span class="sxs-lookup"><span data-stu-id="3de80-107">Transforms</span></span>

<span data-ttu-id="3de80-108">[資料庫轉換](database-transforms.md)會新增或取代原始資料庫中的元素。</span><span class="sxs-lookup"><span data-stu-id="3de80-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="3de80-109">例如，轉換可以將應用程式使用者介面中的所有文字從法文變更為英文。</span><span class="sxs-lookup"><span data-stu-id="3de80-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="3de80-110">轉換的主要用途包括：</span><span class="sxs-lookup"><span data-stu-id="3de80-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="3de80-111">針對特定使用者群組自訂基底安裝套件。</span><span class="sxs-lookup"><span data-stu-id="3de80-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="3de80-112">轉換可以用來封裝不同使用者群組所需的單一基底套件的各種自訂。</span><span class="sxs-lookup"><span data-stu-id="3de80-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="3de80-113">例如，在財務與員工支援部門需要不同安裝特定產品的組織中，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="3de80-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="3de80-114">單一系統管理安裝點上的所有人都可以使用產品的基底套件，並個別將適當的自訂散發給每個使用者群組。</span><span class="sxs-lookup"><span data-stu-id="3de80-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="3de80-115">跨語言同步處理應用程式。</span><span class="sxs-lookup"><span data-stu-id="3de80-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="3de80-116">轉換適用于將封裝撰寫于在撰寫期間以廣泛分隔的位置進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="3de80-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="3de80-117">例如，如果第一次為英文版或法文版應用程式的英文版進行升級，則可以將轉換套用至升級的英文版，以將其轉換為升級的法文版。</span><span class="sxs-lookup"><span data-stu-id="3de80-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="3de80-118">您可以將多個轉換套用至基底套件，然後在安裝期間即時套用。</span><span class="sxs-lookup"><span data-stu-id="3de80-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="3de80-119">這會擴充安裝程式的功能，以建立自訂套件，並提供一種機制，可有效率地將最適當的安裝指派給不同的使用者群組。</span><span class="sxs-lookup"><span data-stu-id="3de80-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="3de80-120">修補應用程式。</span><span class="sxs-lookup"><span data-stu-id="3de80-120">Patching applications.</span></span>

    <span data-ttu-id="3de80-121">轉換可以用來將次要修正套用至不保證進行重大升級的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3de80-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="3de80-122">如需修補程式的詳細資訊，請參閱 [修補套件](patch-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="3de80-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="3de80-123">合併</span><span class="sxs-lookup"><span data-stu-id="3de80-123">Merges</span></span>

<span data-ttu-id="3de80-124">合併會將兩個資料庫結合成一個資料庫，並加入（而不是取代）資訊。</span><span class="sxs-lookup"><span data-stu-id="3de80-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="3de80-125">如果兩個資料庫中都有相同的資訊，就會發生合併衝突。</span><span class="sxs-lookup"><span data-stu-id="3de80-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="3de80-126">合併適用于開發小組，因為它們允許將大型應用程式分割成可稍後輕易的元件。</span><span class="sxs-lookup"><span data-stu-id="3de80-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="3de80-127">例如，您可以個別開發新元件的安裝資料庫元素，稍後再合併到主要安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="3de80-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="3de80-128">如需詳細資訊，請參閱 [合併模組](merge-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="3de80-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="3de80-129">開發小組可能會以下列方式套用合併作業：</span><span class="sxs-lookup"><span data-stu-id="3de80-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="3de80-130">個別分組，並在大型應用程式的不同元件上同時運作。</span><span class="sxs-lookup"><span data-stu-id="3de80-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="3de80-131">每個開發群組接著會在資料庫中填入本身元件的安裝資訊，而不需要擔心應用程式的其他元件。</span><span class="sxs-lookup"><span data-stu-id="3de80-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="3de80-132">完成元件的開發之後，即可將該元件的資料庫合併到整個應用程式的主要安裝資料庫中。</span><span class="sxs-lookup"><span data-stu-id="3de80-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 



