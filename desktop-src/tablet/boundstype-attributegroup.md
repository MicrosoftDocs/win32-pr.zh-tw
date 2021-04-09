---
description: 定義日誌 XML 檔案中各種專案所使用的屬性群組。 它包含屬性，用來定義檔中專案的左邊、頂端、高度和寬度)  (範圍。
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: BoundsType 屬性群組
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689231"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="be021-104">BoundsType 屬性群組</span><span class="sxs-lookup"><span data-stu-id="be021-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="be021-105">定義日誌 XML 檔案中各種專案所使用的屬性群組。</span><span class="sxs-lookup"><span data-stu-id="be021-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="be021-106">它包含屬性，用來定義檔中專案的左邊、頂端、高度和寬度)  (範圍。</span><span class="sxs-lookup"><span data-stu-id="be021-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="be021-107">定義</span><span class="sxs-lookup"><span data-stu-id="be021-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="be021-108">子元素</span><span class="sxs-lookup"><span data-stu-id="be021-108">Child Elements</span></span>

<span data-ttu-id="be021-109">無。</span><span class="sxs-lookup"><span data-stu-id="be021-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="be021-110">屬性</span><span class="sxs-lookup"><span data-stu-id="be021-110">Attributes</span></span>



| <span data-ttu-id="be021-111">屬性</span><span class="sxs-lookup"><span data-stu-id="be021-111">Attribute</span></span>  | <span data-ttu-id="be021-112">類型</span><span class="sxs-lookup"><span data-stu-id="be021-112">Type</span></span>                      | <span data-ttu-id="be021-113">必要</span><span class="sxs-lookup"><span data-stu-id="be021-113">Required</span></span> | <span data-ttu-id="be021-114">描述</span><span class="sxs-lookup"><span data-stu-id="be021-114">Description</span></span>                                                                                        | <span data-ttu-id="be021-115">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="be021-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="be021-116">**離開**</span><span class="sxs-lookup"><span data-stu-id="be021-116">**Left**</span></span>   | <span data-ttu-id="be021-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="be021-117">**xs:integer**</span></span>            | <span data-ttu-id="be021-118">必要</span><span class="sxs-lookup"><span data-stu-id="be021-118">Required</span></span> | <span data-ttu-id="be021-119">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="be021-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="be021-120">任何整數。</span><span class="sxs-lookup"><span data-stu-id="be021-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="be021-121">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="be021-121">**Top**</span></span>    | <span data-ttu-id="be021-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="be021-122">**xs:integer**</span></span>            | <span data-ttu-id="be021-123">必要</span><span class="sxs-lookup"><span data-stu-id="be021-123">Required</span></span> | <span data-ttu-id="be021-124">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="be021-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="be021-125">任何整數。</span><span class="sxs-lookup"><span data-stu-id="be021-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="be021-126">**寬度**</span><span class="sxs-lookup"><span data-stu-id="be021-126">**Width**</span></span>  | <span data-ttu-id="be021-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="be021-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="be021-128">必要</span><span class="sxs-lookup"><span data-stu-id="be021-128">Required</span></span> | <span data-ttu-id="be021-129">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="be021-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="be021-130">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="be021-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="be021-131">**高度**</span><span class="sxs-lookup"><span data-stu-id="be021-131">**Height**</span></span> | <span data-ttu-id="be021-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="be021-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="be021-133">必要</span><span class="sxs-lookup"><span data-stu-id="be021-133">Required</span></span> | <span data-ttu-id="be021-134">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="be021-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="be021-135">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="be021-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="be021-136">類型資訊</span><span class="sxs-lookup"><span data-stu-id="be021-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="be021-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="be021-137">Namespace</span></span>   | <span data-ttu-id="be021-138">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="be021-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="be021-139">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="be021-139">Schema name</span></span> | <span data-ttu-id="be021-140">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="be021-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="be021-141">備註</span><span class="sxs-lookup"><span data-stu-id="be021-141">Remarks</span></span>

<span data-ttu-id="be021-142">**左邊** 和 **頂端** 可以是負數，因為來源是由邊界（而非頁面）所定義。</span><span class="sxs-lookup"><span data-stu-id="be021-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




