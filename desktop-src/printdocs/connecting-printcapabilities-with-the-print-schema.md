---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 2f6c51a3-003c-4d68-9e4d-9be5d325a477
title: 將 PrintCapabilities 與列印架構連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2f5a34421dba2402bce1d6699f208fd58c799
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106979858"
---
# <a name="connecting-printcapabilities-with-the-print-schema"></a><span data-ttu-id="232f7-104">將 PrintCapabilities 與列印架構連接</span><span class="sxs-lookup"><span data-stu-id="232f7-104">Connecting PrintCapabilities with the Print Schema</span></span>

<span data-ttu-id="232f7-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="232f7-105">This topic is not current.</span></span> <span data-ttu-id="232f7-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="232f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="232f7-107">一般 PrintCapabilities 架構涵蓋各種元素類型的結構、用途和使用。</span><span class="sxs-lookup"><span data-stu-id="232f7-107">The general PrintCapabilities Schema covers the structure, purpose, and use of the various element types.</span></span> <span data-ttu-id="232f7-108">它會指定名稱屬性，用來定義每個元素類型的特定實例。</span><span class="sxs-lookup"><span data-stu-id="232f7-108">It specifies the name attribute that is used to define specific instances of each element type.</span></span> <span data-ttu-id="232f7-109">它會指定 PrintCapabilities 作者可以使用 Print Schema 關鍵字所定義之專案的實例，或者，只要這些私用定義的實例定義在明確識別為其本身的命名空間中，就可能會引入自己的私用實例。</span><span class="sxs-lookup"><span data-stu-id="232f7-109">It specifies that PrintCapabilities authors may use instances of elements defined by the Print Schema Keywords, or they may introduce their own privately-defined instances, as long as these privately-defined instances are defined in a namespace that is clearly identified as their own.</span></span> <span data-ttu-id="232f7-110"> (PrintCapabilities 作者也可以使用先前在另一個私用命名空間中定義的實例。 ) </span><span class="sxs-lookup"><span data-stu-id="232f7-110">(PrintCapabilities authors may also use instances previously defined in another private namespace.)</span></span>

<span data-ttu-id="232f7-111">列印架構關鍵字檔會定義每個專案類型的特定實例，可用於 PrintCapabilities 檔和 PrintTickets 中。</span><span class="sxs-lookup"><span data-stu-id="232f7-111">The Print Schema Keywords document defines the specific instances of each element type available for use in PrintCapabilities documents and in PrintTickets.</span></span> <span data-ttu-id="232f7-112">它也記載了其用途和使用方式。</span><span class="sxs-lookup"><span data-stu-id="232f7-112">It also documents their purpose and usage.</span></span> <span data-ttu-id="232f7-113">列印架構關鍵字檔也會定義數個元素類型的實例，如下所示：</span><span class="sxs-lookup"><span data-stu-id="232f7-113">The Print Schema Keywords document also defines instances of several element types, as follows:</span></span>

-   <span data-ttu-id="232f7-114">位於 PrintCapabilities 檔根目錄的屬性和子屬性實例</span><span class="sxs-lookup"><span data-stu-id="232f7-114">Property and subproperty instances that reside at the root of the PrintCapabilities document</span></span>

    -   <span data-ttu-id="232f7-115">這些元素說明裝置的各種層面和功能，並提供描述裝置的常見詞彙。</span><span class="sxs-lookup"><span data-stu-id="232f7-115">These elements describe the various aspects and capabilities of the device, and provide a common vocabulary for describing devices.</span></span>

-   <span data-ttu-id="232f7-116">屬於 Feature 元素子系的屬性和子屬性實例</span><span class="sxs-lookup"><span data-stu-id="232f7-116">Property and subproperty instances that are children of Feature elements</span></span>

    -   <span data-ttu-id="232f7-117">這些元素會描述與特定功能相關的各種層面。</span><span class="sxs-lookup"><span data-stu-id="232f7-117">These elements describe various aspects related to a specific Feature.</span></span>

-   <span data-ttu-id="232f7-118">屬於 Option 元素子系的屬性和子屬性實例</span><span class="sxs-lookup"><span data-stu-id="232f7-118">Property and subproperty instances that are children of Option elements</span></span>

    -   <span data-ttu-id="232f7-119">這些元素會描述裝置的各個層面和功能，而這些功能相依于特定功能所選的選項。</span><span class="sxs-lookup"><span data-stu-id="232f7-119">These elements describe the various aspects and capabilities of the device that are dependent on the Option selected for a specific Feature.</span></span> <span data-ttu-id="232f7-120">這些可能會由位於 PrintCapabilities 檔根目錄的屬性實例取代，但在某些情況下可提供額外的便利性。</span><span class="sxs-lookup"><span data-stu-id="232f7-120">These could be replaced by Property instances located at the root of the PrintCapabilities document, but offer additional convenience in some cases.</span></span> <span data-ttu-id="232f7-121">如需詳細資訊，請參閱 [加入屬性實例](adding-property-instances.md)。</span><span class="sxs-lookup"><span data-stu-id="232f7-121">For more information, see [Adding Property Instances](adding-property-instances.md).</span></span>

<!-- -->

-   <span data-ttu-id="232f7-122">ScoredProperty 實例</span><span class="sxs-lookup"><span data-stu-id="232f7-122">ScoredProperty instances</span></span>

    -   <span data-ttu-id="232f7-123">ScoredProperty 實例會定義用來定義選項特性的語言。</span><span class="sxs-lookup"><span data-stu-id="232f7-123">ScoredProperty instances define the language that is used to characterize an Option.</span></span> <span data-ttu-id="232f7-124">在 Print Schema 關鍵字中定義的 ScoredProperty 實例，可讓許多不同的合作物件為許多不同的合作物件撰寫的選項實例，讓許多裝置都能成為可攜性，並可供任何其他設備磁碟機或 PrintCapabilities 或 PrintTicket 提供者瞭解。</span><span class="sxs-lookup"><span data-stu-id="232f7-124">The ScoredProperty instances defined in the Print Schema Keywords make it possible for Option instances written by many different parties for many devices to be portable, and to be understood by any other device driver or PrintCapabilities or PrintTicket provider.</span></span>

-   <span data-ttu-id="232f7-125">ScoredProperty 值實例</span><span class="sxs-lookup"><span data-stu-id="232f7-125">ScoredProperty Value instances</span></span>

    -   <span data-ttu-id="232f7-126">針對提供 ScoredProperty 實例的相同原因，提供這些值實例。</span><span class="sxs-lookup"><span data-stu-id="232f7-126">These Value instances are provided for the same reason that ScoredProperty instances are provided.</span></span>

-   <span data-ttu-id="232f7-127">功能實例</span><span class="sxs-lookup"><span data-stu-id="232f7-127">Feature instances</span></span>

    -   <span data-ttu-id="232f7-128">每個選項都必須屬於特定功能，因此需要定義功能本身。</span><span class="sxs-lookup"><span data-stu-id="232f7-128">Each Option must belong to a specific Feature, thereby requiring the Feature itself to be defined.</span></span>

-   <span data-ttu-id="232f7-129">ParameterDef 實例</span><span class="sxs-lookup"><span data-stu-id="232f7-129">ParameterDef instances</span></span>

    -   <span data-ttu-id="232f7-130">列印架構關鍵字提供的 ParameterDef 實例也會針對其中包含的每個屬性定義一個值。</span><span class="sxs-lookup"><span data-stu-id="232f7-130">A Print Schema Keywords-supplied ParameterDef instance also defines a Value for each Property contained in it.</span></span> <span data-ttu-id="232f7-131">PrintCapabilities 提供者可自由修改可變更之屬性實例的值實例。</span><span class="sxs-lookup"><span data-stu-id="232f7-131">The PrintCapabilities provider is free to modify the Value instances for those Property instances that can be changed.</span></span> <span data-ttu-id="232f7-132">如需可以變更哪些屬性實例，以及哪些 (無法變更) 的詳細資訊，請參閱 [ParameterDef 和 ParameterInit 元素](parameterdef-and-parameterinit-elements.md)。</span><span class="sxs-lookup"><span data-stu-id="232f7-132">For information about which Property instances can be changed, and which cannot be changed (are immutable), see [ParameterDef and ParameterInit Elements](parameterdef-and-parameterinit-elements.md).</span></span>

<span data-ttu-id="232f7-133">請務必注意，PrintCapabilities 架構不會命名任何選項實例。</span><span class="sxs-lookup"><span data-stu-id="232f7-133">It is important to note the PrintCapabilities Schema does not name any Option instances.</span></span> <span data-ttu-id="232f7-134">選項實例的特性僅由其整體 ScoredProperty 實例所組成。</span><span class="sxs-lookup"><span data-stu-id="232f7-134">Option instances are characterized solely by their ScoredProperty instances taken as a whole.</span></span> <span data-ttu-id="232f7-135">常見的誤解是，使用 ' name ' 屬性定義選項來識別選項實例，但這是不正確的。</span><span class="sxs-lookup"><span data-stu-id="232f7-135">A common misconception is that using the 'name' attribute to define an Option identifies Option instances, but this is incorrect.</span></span> <span data-ttu-id="232f7-136">選項元素不需要為同一個選項實例的唯一，也不能使用 ' name ' 屬性來定義所需的選項。</span><span class="sxs-lookup"><span data-stu-id="232f7-136">Option elements are not required to be unique for sibling Option instances, nor is using the 'name' attribute to define an Option required.</span></span>

<span data-ttu-id="232f7-137">Print Schema 關鍵字檔會定義 PrintCapabilities 和 PrintTicket 架構中的所有實例名稱屬性所屬的標準命名空間。</span><span class="sxs-lookup"><span data-stu-id="232f7-137">The Print Schema Keywords document defines a standard namespace to which all instance name attributes in the PrintCapabilities and PrintTicket schemas belong.</span></span> <span data-ttu-id="232f7-138">專案類型所使用的所有元素類型標記和 XML 屬性也都屬於這個命名空間。</span><span class="sxs-lookup"><span data-stu-id="232f7-138">All element type tags and XML Attributes used by the element types also belong to this namespace.</span></span>

<span data-ttu-id="232f7-139">針對 PrintCapabilities 架構中定義的每個實例，PrintCapabilities 架構會同時指定名稱屬性和實例的位置。</span><span class="sxs-lookup"><span data-stu-id="232f7-139">For each instance defined in the PrintCapabilities Schema, the PrintCapabilities Schema specifies both the name attribute and the location of the instance.</span></span> <span data-ttu-id="232f7-140">在 PrintCapabilities 檔或 PrintTicket 中使用這個實例時，提供者和用戶端都必須保留這兩者。</span><span class="sxs-lookup"><span data-stu-id="232f7-140">The provider and client must preserve both when using this instance in their PrintCapabilities document or PrintTicket.</span></span>

<span data-ttu-id="232f7-141">Print Schema 關鍵字檔會將某些實例指定為強制性。</span><span class="sxs-lookup"><span data-stu-id="232f7-141">The Print Schema Keywords document designates some instances as mandatory.</span></span> <span data-ttu-id="232f7-142">這些實例必須出現在每個 PrintCapabilities 檔中，而且必須使用有效值正確地初始化。</span><span class="sxs-lookup"><span data-stu-id="232f7-142">These instances must appear in every PrintCapabilities document and must be properly initialized with valid Values.</span></span> <span data-ttu-id="232f7-143">列印架構關鍵字中未指定為強制的所有實例都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="232f7-143">All instances in the Print Schema Keywords that are not designated as mandatory are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="232f7-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="232f7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="232f7-145">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="232f7-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



