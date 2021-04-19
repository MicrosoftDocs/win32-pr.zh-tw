---
title: 結構化儲存體序列化屬性集格式
description: 持續性屬性集會提供將資料儲存在檔案系統實體內的選項。 建議您在建立和管理它們時，使用屬性和屬性集中所述的 IPropertySetStorage 和 IPropertyStorage 介面。
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- 結構化儲存體 Strctd Stg.、基礎、序列化屬性集格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea03d5ccab337897be801840080e83a6fa86880
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967273"
---
# <a name="structured-storage-serialized-property-set-format"></a><span data-ttu-id="806d3-105">結構化儲存體序列化屬性集格式</span><span class="sxs-lookup"><span data-stu-id="806d3-105">Structured Storage Serialized Property Set Format</span></span>

<span data-ttu-id="806d3-106">持續性屬性集會提供將資料儲存在檔案系統實體內的選項。</span><span class="sxs-lookup"><span data-stu-id="806d3-106">Persistent property sets provide an option to store data within file system entities.</span></span> <span data-ttu-id="806d3-107">建議您在建立和管理它們時，使用 [屬性和屬性集中](properties-and-property-sets.md)所述的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面。</span><span class="sxs-lookup"><span data-stu-id="806d3-107">It is recommended that, to create and manage them, you use the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interfaces described in [Properties and Property Sets](properties-and-property-sets.md).</span></span>

<span data-ttu-id="806d3-108">屬性集是由值的標記區段所組成，而且區段是由格式識別碼 (FMTID) 來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="806d3-108">Property sets are composed of a tagged section of values, with the section uniquely identified by a format identifier (FMTID).</span></span> <span data-ttu-id="806d3-109">每個屬性都是由屬性識別碼和代表值的類型指標所組成。</span><span class="sxs-lookup"><span data-stu-id="806d3-109">Every property consists of a property identifier and a type indicator that represents a value.</span></span> <span data-ttu-id="806d3-110">儲存在屬性集中的每個值都有唯一的屬性識別碼，可區分屬性。</span><span class="sxs-lookup"><span data-stu-id="806d3-110">Each value stored in a property set has a unique property identifier that distinguishes the property.</span></span> <span data-ttu-id="806d3-111">類型指標描述值中的資料標記法。</span><span class="sxs-lookup"><span data-stu-id="806d3-111">The type indicator describes the representation of the data in the value.</span></span>

<span data-ttu-id="806d3-112">當您使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面時，您不需要處理 COM 序列化的屬性集格式結構。</span><span class="sxs-lookup"><span data-stu-id="806d3-112">When you use the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) and [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interfaces, you do not have to handle the COM serialized property set format structure.</span></span> <span data-ttu-id="806d3-113">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="806d3-113">For more information, see the listed topics:</span></span>

<span data-ttu-id="806d3-114">屬性集內的所有資料元素都會儲存在 Intel 表示中， (也就是以位元組由小到大的順序) 。</span><span class="sxs-lookup"><span data-stu-id="806d3-114">All data elements within a property set are stored in Intel representation (that is, in little-endian byte order).</span></span>

<span data-ttu-id="806d3-115">COM 會定義屬性集的標準、序列化資料格式。</span><span class="sxs-lookup"><span data-stu-id="806d3-115">COM defines a standard, serialized data format for property sets.</span></span> <span data-ttu-id="806d3-116">處理序列化格式，而不是使用介面時，屬性集會具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="806d3-116">When handling the serialized format, and not with the interfaces, property sets have the following characteristics:</span></span>

-   <span data-ttu-id="806d3-117">屬性集可讓不同的應用程式建立自己的獨立屬性集來提供應用程式。</span><span class="sxs-lookup"><span data-stu-id="806d3-117">Property sets allow for different applications to create their own independent property sets to serve the application.</span></span>
-   <span data-ttu-id="806d3-118">屬性集可以儲存在單一 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例或包含多個資料流程的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中。</span><span class="sxs-lookup"><span data-stu-id="806d3-118">Property sets can be stored in a single [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) instance or in an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instance that contains multiple streams.</span></span> <span data-ttu-id="806d3-119">屬性集只是另一種資料類型，可儲存在記憶體中或磁片上儲存體的許多不同形式。</span><span class="sxs-lookup"><span data-stu-id="806d3-119">Property sets are simply another data type that can be stored in many different forms of an in-memory or on-disk storage.</span></span> <span data-ttu-id="806d3-120">如需建立儲存物件之字串名稱的詳細資訊和建議慣例，請參閱 [存放裝置物件命名慣例](storage-object-naming-conventions.md)。</span><span class="sxs-lookup"><span data-stu-id="806d3-120">For more information and recommended conventions for creating the string name for the storage object, see [Storage Object Naming Conventions](storage-object-naming-conventions.md).</span></span>
-   <span data-ttu-id="806d3-121">屬性集允許包含說明內容的顯示名稱字典。</span><span class="sxs-lookup"><span data-stu-id="806d3-121">Property sets allow for a dictionary of display names to be included that describe the contents.</span></span> <span data-ttu-id="806d3-122">建議使用一組選擇屬性名稱的慣例。</span><span class="sxs-lookup"><span data-stu-id="806d3-122">A set of conventions for choosing property names is recommended.</span></span> <span data-ttu-id="806d3-123">如需此選擇性字典的詳細資訊，請參閱 [保留的屬性識別碼](reserved-property-identifiers.md)，包括 [屬性識別碼 0](/windows/desktop/Stg/reserved-property-identifiers)。</span><span class="sxs-lookup"><span data-stu-id="806d3-123">For more information about this optional dictionary, see [Reserved Property Identifiers](reserved-property-identifiers.md), including [Property ID 0](/windows/desktop/Stg/reserved-property-identifiers).</span></span>

<span data-ttu-id="806d3-124">屬性集資料流程分為三個主要部分：</span><span class="sxs-lookup"><span data-stu-id="806d3-124">The property set stream is divided into three major parts:</span></span>

-   <span data-ttu-id="806d3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="806d3-125">Header</span></span>
-   <span data-ttu-id="806d3-126">FORMATID/位移配對</span><span class="sxs-lookup"><span data-stu-id="806d3-126">FORMATID/offset pair</span></span>
-   <span data-ttu-id="806d3-127">包含實際屬性集值的區段</span><span class="sxs-lookup"><span data-stu-id="806d3-127">Section containing the actual property set values</span></span>

<span data-ttu-id="806d3-128">屬性集資料流程的整體長度必須小於或等於256K。</span><span class="sxs-lookup"><span data-stu-id="806d3-128">The overall length of the property set stream must be less than or equal to 256K.</span></span> <span data-ttu-id="806d3-129">下列章節、 [屬性集標頭](property-set-header.md)、 [格式識別碼/位移](format-identifier-offset-pair.md)組和 [區段](section.md) (包括 [屬性識別碼/位移](property-identifiers-offset-pairs.md) 組) ，以及支援的主題，描述構成屬性集資料格式的個別元件。</span><span class="sxs-lookup"><span data-stu-id="806d3-129">The following sections, [Property Set Header](property-set-header.md), [Format Identifier/Offset Pair](format-identifier-offset-pair.md), and [Section](section.md) (including [Property Identifiers/Offset Pairs](property-identifiers-offset-pairs.md)), with supporting topics, describe the individual components that compose the property-set data format.</span></span>

> [!Note]  
> <span data-ttu-id="806d3-130">本檔先前的版本描述了屬性集資料流程的延伸模組，並允許一個以上的區段，但是已經修改為可提供屬性資料流程中的一個區段。</span><span class="sxs-lookup"><span data-stu-id="806d3-130">Previous versions of this document described extensions to the property set stream with more than one section allowed, but that has been revised to provide for one section in the property stream.</span></span> <span data-ttu-id="806d3-131">其中一個例外狀況是 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="806d3-131">The one exception is [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span>

 

 

 