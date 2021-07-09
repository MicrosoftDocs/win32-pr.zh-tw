---
description: 取得 Option 元素的相關資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549376"
---
# <a name="option"></a><span data-ttu-id="e3e6a-105">選項</span><span class="sxs-lookup"><span data-stu-id="e3e6a-105">Option</span></span>

<span data-ttu-id="e3e6a-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-106">This topic is not current.</span></span> <span data-ttu-id="e3e6a-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3e6a-108">Option 元素包含與此選項相關聯的所有屬性和 ScoredProperty 元素。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-108">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="e3e6a-109">元素標記</span><span class="sxs-lookup"><span data-stu-id="e3e6a-109">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="e3e6a-110">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="e3e6a-110">XML Attributes</span></span>

<span data-ttu-id="e3e6a-111">下表列出可能與此元素相關的 XML 屬性。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="e3e6a-112">XML 屬性</span><span class="sxs-lookup"><span data-stu-id="e3e6a-112">XML Attribute</span></span>          | <span data-ttu-id="e3e6a-113">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e3e6a-113">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e6a-114">約束</span><span class="sxs-lookup"><span data-stu-id="e3e6a-114">constrained</span></span><br/> | <span data-ttu-id="e3e6a-115">PrintCapabilities 檔的這個屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-115">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="e3e6a-116">這個屬性會指出選項是否可供選取或使用。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-116">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="e3e6a-117">這個 XML 屬性可以設定為下列其中一個值： None、PrintTicketSettings、AdminSetting 或 DeviceSettings。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-117">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="e3e6a-118">查看 [XML 屬性](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="e3e6a-118">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="e3e6a-119">NAME</span><span class="sxs-lookup"><span data-stu-id="e3e6a-119">name</span></span><br/>        | <span data-ttu-id="e3e6a-120">保存選項的名稱，也就是標準選項或私用定義的選項。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-120">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="e3e6a-121">這種方式會使用 XML 屬性來區分選項實例。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-121">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="e3e6a-122">如需詳細資訊，請參閱 [XML 屬性](xml-attributes.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-122">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="e3e6a-123">項目資訊</span><span class="sxs-lookup"><span data-stu-id="e3e6a-123">Element Information</span></span>

<span data-ttu-id="e3e6a-124">下表列出可能是這個專案之父代的元素、可能是這個專案之子系的專案，以及專案本身的任何限制。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-124">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="e3e6a-125">類別</span><span class="sxs-lookup"><span data-stu-id="e3e6a-125">Category</span></span>                   | <span data-ttu-id="e3e6a-126">詳細資料</span><span class="sxs-lookup"><span data-stu-id="e3e6a-126">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e6a-127">父元素</span><span class="sxs-lookup"><span data-stu-id="e3e6a-127">Parent elements</span></span><br/> | <span data-ttu-id="e3e6a-128">功能</span><span class="sxs-lookup"><span data-stu-id="e3e6a-128">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e3e6a-129">子元素</span><span class="sxs-lookup"><span data-stu-id="e3e6a-129">Child elements</span></span><br/>  | <span data-ttu-id="e3e6a-130">*屬性* (零或多個) </span><span class="sxs-lookup"><span data-stu-id="e3e6a-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="e3e6a-131">*ScoredProperty* (零或多個用於具有 XML 屬性 ' name ' 的選項;一或多個選項用於未使用 XML 屬性 ' name ' 的選項 \*) </span><span class="sxs-lookup"><span data-stu-id="e3e6a-131">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="e3e6a-132">\* 只有在列印架構中定義的公用選項才能有 ' name ' 屬性，例如 DocumentNUp) </span><span class="sxs-lookup"><span data-stu-id="e3e6a-132">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="e3e6a-133">這個元素</span><span class="sxs-lookup"><span data-stu-id="e3e6a-133">This element</span></span><br/>    | <span data-ttu-id="e3e6a-134">不允許任何字元資料。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-134">No character data is permitted.</span></span><br/> <span data-ttu-id="e3e6a-135">不允許重複的子同級。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-135">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="e3e6a-136">設定相依性</span><span class="sxs-lookup"><span data-stu-id="e3e6a-136">Configuration Dependencies</span></span>

<span data-ttu-id="e3e6a-137">Option definition 元素可能沒有任何設定相依性。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-137">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="e3e6a-138">專案使用方式</span><span class="sxs-lookup"><span data-stu-id="e3e6a-138">Element Usage</span></span>

<span data-ttu-id="e3e6a-139">Option 元素的目的是要說明裝置設定屬性（由功能元素代表）可以假設的其中一個狀態。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-139">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="e3e6a-140">每個選項專案定義都包含一或多個 ScoredProperty 元素，這些元素會描述該選項的內建或基本特性。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-140">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="e3e6a-141">為了促進可攜性和保存意圖，列印架構會定義許多常見的功能元素，以及每項功能的各種選項元素。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-141">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="e3e6a-142">因此，在您建立自己的選項定義之前，請務必先使用列印架構定義的選項元素（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-142">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="e3e6a-143">瞭解定義 Option 元素的程式，可提供 PrintCapabilities 檔和 PrintTickets 在 Microsoft .NET Framework 3.0 版和 Windows Vista 列印架構中的使用方式的實用深入解析。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-143">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="e3e6a-144">範例</span><span class="sxs-lookup"><span data-stu-id="e3e6a-144">Example</span></span>

<span data-ttu-id="e3e6a-145">下列範例會定義選項的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-145">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="e3e6a-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3e6a-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e6a-147">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="e3e6a-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




