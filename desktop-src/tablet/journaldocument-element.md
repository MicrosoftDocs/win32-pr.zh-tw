---
description: 筆記本便箋 XML 檔案中的最上層元素。
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: JournalDocument 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514108"
---
# <a name="journaldocument-element"></a><span data-ttu-id="5f5bf-103">JournalDocument 元素</span><span class="sxs-lookup"><span data-stu-id="5f5bf-103">JournalDocument Element</span></span>

<span data-ttu-id="5f5bf-104">筆記本便箋 XML 檔案中的最上層元素。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="5f5bf-105">定義</span><span class="sxs-lookup"><span data-stu-id="5f5bf-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="5f5bf-106">父項目</span><span class="sxs-lookup"><span data-stu-id="5f5bf-106">Parent Elements</span></span>

<span data-ttu-id="5f5bf-107">無。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5f5bf-108">子元素</span><span class="sxs-lookup"><span data-stu-id="5f5bf-108">Child Elements</span></span>

[<span data-ttu-id="5f5bf-109">**信箋**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="5f5bf-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="5f5bf-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5f5bf-111">Attributes</span></span>



| <span data-ttu-id="5f5bf-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5f5bf-112">Attribute</span></span>             | <span data-ttu-id="5f5bf-113">類型</span><span class="sxs-lookup"><span data-stu-id="5f5bf-113">Type</span></span>                      | <span data-ttu-id="5f5bf-114">必要</span><span class="sxs-lookup"><span data-stu-id="5f5bf-114">Required</span></span> | <span data-ttu-id="5f5bf-115">描述</span><span class="sxs-lookup"><span data-stu-id="5f5bf-115">Description</span></span>                                                      | <span data-ttu-id="5f5bf-116">可能的值</span><span class="sxs-lookup"><span data-stu-id="5f5bf-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5f5bf-117">**版本**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-117">**Version**</span></span>           | <span data-ttu-id="5f5bf-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-118">**xs:string**</span></span>             | <span data-ttu-id="5f5bf-119">必要</span><span class="sxs-lookup"><span data-stu-id="5f5bf-119">Required</span></span> | <span data-ttu-id="5f5bf-120">XML 檔案中表示的日誌檔版本。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="5f5bf-121">1.0</span><span class="sxs-lookup"><span data-stu-id="5f5bf-121">1.0</span></span>                       |
| <span data-ttu-id="5f5bf-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="5f5bf-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5f5bf-124">必要</span><span class="sxs-lookup"><span data-stu-id="5f5bf-124">Required</span></span> | <span data-ttu-id="5f5bf-125">筆記本檔的預設頁面寬度。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="5f5bf-126">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="5f5bf-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="5f5bf-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5f5bf-129">必要</span><span class="sxs-lookup"><span data-stu-id="5f5bf-129">Required</span></span> | <span data-ttu-id="5f5bf-130">筆記本檔頁面的預設高度。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="5f5bf-131">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="5f5bf-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="5f5bf-132">項目資訊</span><span class="sxs-lookup"><span data-stu-id="5f5bf-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="5f5bf-133">項目類型</span><span class="sxs-lookup"><span data-stu-id="5f5bf-133">Element type</span></span> | <span data-ttu-id="5f5bf-134">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="5f5bf-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="5f5bf-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="5f5bf-135">Namespace</span></span>    | <span data-ttu-id="5f5bf-136">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="5f5bf-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="5f5bf-137">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="5f5bf-137">Schema name</span></span>  | <span data-ttu-id="5f5bf-138">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="5f5bf-138">Journal Reader</span></span>                             |



 

 

 



