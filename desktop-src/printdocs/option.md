---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982818"
---
# <a name="option"></a><span data-ttu-id="5a338-104">選項</span><span class="sxs-lookup"><span data-stu-id="5a338-104">Option</span></span>

<span data-ttu-id="5a338-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="5a338-105">This topic is not current.</span></span> <span data-ttu-id="5a338-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="5a338-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a338-107">Option 元素包含與此選項相關聯的所有屬性和 ScoredProperty 元素。</span><span class="sxs-lookup"><span data-stu-id="5a338-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5a338-108">元素標記</span><span class="sxs-lookup"><span data-stu-id="5a338-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="5a338-109">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="5a338-109">XML Attributes</span></span>

<span data-ttu-id="5a338-110">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="5a338-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5a338-111">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="5a338-111">XML Attribute</span></span>          | <span data-ttu-id="5a338-112">詳細資料</span><span class="sxs-lookup"><span data-stu-id="5a338-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a338-113">約束</span><span class="sxs-lookup"><span data-stu-id="5a338-113">constrained</span></span><br/> | <span data-ttu-id="5a338-114">PrintCapabilities 檔的這個屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="5a338-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="5a338-115">這個屬性會指出選項是否可供選取或使用。</span><span class="sxs-lookup"><span data-stu-id="5a338-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="5a338-116">這個 XML 屬性可以設定為下列其中一個值： None、PrintTicketSettings、AdminSetting 或 DeviceSettings。</span><span class="sxs-lookup"><span data-stu-id="5a338-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="5a338-117">查看 [XML 屬性](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="5a338-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="5a338-118">NAME</span><span class="sxs-lookup"><span data-stu-id="5a338-118">name</span></span><br/>        | <span data-ttu-id="5a338-119">保存選項的名稱，也就是標準選項或私用定義的選項。</span><span class="sxs-lookup"><span data-stu-id="5a338-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="5a338-120">這種方式會使用 XML 屬性來區分選項實例。</span><span class="sxs-lookup"><span data-stu-id="5a338-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="5a338-121">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="5a338-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5a338-122">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5a338-122">Element Information</span></span>

<span data-ttu-id="5a338-123">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="5a338-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="5a338-124">類別</span><span class="sxs-lookup"><span data-stu-id="5a338-124">Category</span></span>                   | <span data-ttu-id="5a338-125">詳細資料</span><span class="sxs-lookup"><span data-stu-id="5a338-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a338-126">父元素</span><span class="sxs-lookup"><span data-stu-id="5a338-126">Parent elements</span></span><br/> | <span data-ttu-id="5a338-127">功能</span><span class="sxs-lookup"><span data-stu-id="5a338-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5a338-128">子元素</span><span class="sxs-lookup"><span data-stu-id="5a338-128">Child elements</span></span><br/>  | <span data-ttu-id="5a338-129">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="5a338-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="5a338-130">*ScoredProperty* (零或多個用於具有 XML 屬性 ' name ' 的選項;一或多個選項用於未使用 XML 屬性 ' name ' 的選項 \*) </span><span class="sxs-lookup"><span data-stu-id="5a338-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="5a338-131">\* 只有在列印架構中定義的公用選項才能有 ' name ' 屬性，例如 DocumentNUp) </span><span class="sxs-lookup"><span data-stu-id="5a338-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="5a338-132">這個元素</span><span class="sxs-lookup"><span data-stu-id="5a338-132">This element</span></span><br/>    | <span data-ttu-id="5a338-133">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="5a338-133">No character data is permitted.</span></span><br/> <span data-ttu-id="5a338-134">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="5a338-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5a338-135">設定相依性</span><span class="sxs-lookup"><span data-stu-id="5a338-135">Configuration Dependencies</span></span>

<span data-ttu-id="5a338-136">Option definition 元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="5a338-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="5a338-137">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="5a338-137">Element Usage</span></span>

<span data-ttu-id="5a338-138">Option 元素的目的是要說明裝置設定屬性（由功能元素代表）可以假設的其中一個狀態。</span><span class="sxs-lookup"><span data-stu-id="5a338-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="5a338-139">每個選項專案定義都包含一或多個 ScoredProperty 元素，這些元素會描述該選項的內建或基本特性。</span><span class="sxs-lookup"><span data-stu-id="5a338-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="5a338-140">為了促進可攜性和保存意圖，列印架構會定義許多常見的功能元素，以及每項功能的各種選項元素。</span><span class="sxs-lookup"><span data-stu-id="5a338-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="5a338-141">因此，在您建立自己的選項定義之前，請務必先使用列印架構定義的選項元素（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="5a338-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="5a338-142">瞭解定義 Option 元素的程式，可提供 PrintCapabilities 檔和 PrintTickets 在 Microsoft .NET Framework 3.0 版和 Windows Vista 列印架構中的使用方式的實用深入解析。</span><span class="sxs-lookup"><span data-stu-id="5a338-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="5a338-143">範例</span><span class="sxs-lookup"><span data-stu-id="5a338-143">Example</span></span>

<span data-ttu-id="5a338-144">下列範例會定義選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a338-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="5a338-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a338-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a338-146">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="5a338-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




