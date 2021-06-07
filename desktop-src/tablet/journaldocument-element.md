---
description: 筆記本便箋 XML 檔案中的最上層元素。
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: JournalDocument 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432170"
---
# <a name="journaldocument-element"></a><span data-ttu-id="9e93a-103">JournalDocument 元素</span><span class="sxs-lookup"><span data-stu-id="9e93a-103">JournalDocument Element</span></span>

<span data-ttu-id="9e93a-104">筆記本便箋 XML 檔案中的最上層元素。</span><span class="sxs-lookup"><span data-stu-id="9e93a-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="9e93a-105">定義</span><span class="sxs-lookup"><span data-stu-id="9e93a-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="9e93a-106">父項目</span><span class="sxs-lookup"><span data-stu-id="9e93a-106">Parent Elements</span></span>

<span data-ttu-id="9e93a-107">無。</span><span class="sxs-lookup"><span data-stu-id="9e93a-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9e93a-108">子元素</span><span class="sxs-lookup"><span data-stu-id="9e93a-108">Child Elements</span></span>

[<span data-ttu-id="9e93a-109">**信箋**</span><span class="sxs-lookup"><span data-stu-id="9e93a-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="9e93a-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="9e93a-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="9e93a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9e93a-111">Attributes</span></span>



| <span data-ttu-id="9e93a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9e93a-112">Attribute</span></span>             | <span data-ttu-id="9e93a-113">類型</span><span class="sxs-lookup"><span data-stu-id="9e93a-113">Type</span></span>                      | <span data-ttu-id="9e93a-114">必要</span><span class="sxs-lookup"><span data-stu-id="9e93a-114">Required</span></span> | <span data-ttu-id="9e93a-115">描述</span><span class="sxs-lookup"><span data-stu-id="9e93a-115">Description</span></span>                                                      | <span data-ttu-id="9e93a-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="9e93a-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="9e93a-117">**版本**</span><span class="sxs-lookup"><span data-stu-id="9e93a-117">**Version**</span></span>           | <span data-ttu-id="9e93a-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="9e93a-118">**xs:string**</span></span>             | <span data-ttu-id="9e93a-119">必要</span><span class="sxs-lookup"><span data-stu-id="9e93a-119">Required</span></span> | <span data-ttu-id="9e93a-120">XML 檔案中表示的日誌檔版本。</span><span class="sxs-lookup"><span data-stu-id="9e93a-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="9e93a-121">1.0</span><span class="sxs-lookup"><span data-stu-id="9e93a-121">1.0</span></span>                       |
| <span data-ttu-id="9e93a-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="9e93a-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="9e93a-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="9e93a-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="9e93a-124">必要</span><span class="sxs-lookup"><span data-stu-id="9e93a-124">Required</span></span> | <span data-ttu-id="9e93a-125">筆記本檔的預設頁面寬度。</span><span class="sxs-lookup"><span data-stu-id="9e93a-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="9e93a-126">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="9e93a-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="9e93a-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="9e93a-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="9e93a-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="9e93a-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="9e93a-129">必要</span><span class="sxs-lookup"><span data-stu-id="9e93a-129">Required</span></span> | <span data-ttu-id="9e93a-130">筆記本檔頁面的預設高度。</span><span class="sxs-lookup"><span data-stu-id="9e93a-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="9e93a-131">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="9e93a-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="9e93a-132">項目資訊</span><span class="sxs-lookup"><span data-stu-id="9e93a-132">Element Information</span></span>



|  <span data-ttu-id="9e93a-133">元素</span><span class="sxs-lookup"><span data-stu-id="9e93a-133">Element</span></span>     | <span data-ttu-id="9e93a-134">值</span><span class="sxs-lookup"><span data-stu-id="9e93a-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="9e93a-135">項目類型</span><span class="sxs-lookup"><span data-stu-id="9e93a-135">Element type</span></span> | <span data-ttu-id="9e93a-136">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="9e93a-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="9e93a-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e93a-137">Namespace</span></span>    | <span data-ttu-id="9e93a-138">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="9e93a-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="9e93a-139">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="9e93a-139">Schema name</span></span>  | <span data-ttu-id="9e93a-140">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="9e93a-140">Journal Reader</span></span>                             |



 

 

 



