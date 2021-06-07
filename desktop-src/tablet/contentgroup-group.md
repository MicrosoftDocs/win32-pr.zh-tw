---
description: 定義在筆記本便箋中包含一組分組內容的群組。
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: ContentGroup 群組
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432610"
---
# <a name="contentgroup-group"></a><span data-ttu-id="40af0-103">ContentGroup 群組</span><span class="sxs-lookup"><span data-stu-id="40af0-103">ContentGroup Group</span></span>

<span data-ttu-id="40af0-104">定義在筆記本便箋中包含一組分組內容的群組。</span><span class="sxs-lookup"><span data-stu-id="40af0-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="40af0-105">定義</span><span class="sxs-lookup"><span data-stu-id="40af0-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="40af0-106">子元素</span><span class="sxs-lookup"><span data-stu-id="40af0-106">Child Elements</span></span>

[<span data-ttu-id="40af0-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="40af0-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="40af0-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="40af0-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="40af0-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="40af0-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="40af0-110">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="40af0-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="40af0-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="40af0-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="40af0-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="40af0-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="40af0-113">**旗標**</span><span class="sxs-lookup"><span data-stu-id="40af0-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="40af0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="40af0-114">Attributes</span></span>



| <span data-ttu-id="40af0-115">屬性</span><span class="sxs-lookup"><span data-stu-id="40af0-115">Attribute</span></span>  | <span data-ttu-id="40af0-116">類型</span><span class="sxs-lookup"><span data-stu-id="40af0-116">Type</span></span>                      | <span data-ttu-id="40af0-117">必要</span><span class="sxs-lookup"><span data-stu-id="40af0-117">Required</span></span> | <span data-ttu-id="40af0-118">描述</span><span class="sxs-lookup"><span data-stu-id="40af0-118">Description</span></span>                                                                                        | <span data-ttu-id="40af0-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="40af0-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="40af0-120">**離開**</span><span class="sxs-lookup"><span data-stu-id="40af0-120">**Left**</span></span>   | <span data-ttu-id="40af0-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="40af0-121">**xs:integer**</span></span>            | <span data-ttu-id="40af0-122">必要</span><span class="sxs-lookup"><span data-stu-id="40af0-122">Required</span></span> | <span data-ttu-id="40af0-123">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="40af0-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="40af0-124">任何整數。</span><span class="sxs-lookup"><span data-stu-id="40af0-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="40af0-125">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="40af0-125">**Top**</span></span>    | <span data-ttu-id="40af0-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="40af0-126">**xs:integer**</span></span>            | <span data-ttu-id="40af0-127">必要</span><span class="sxs-lookup"><span data-stu-id="40af0-127">Required</span></span> | <span data-ttu-id="40af0-128">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="40af0-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="40af0-129">任何整數。</span><span class="sxs-lookup"><span data-stu-id="40af0-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="40af0-130">**寬度**</span><span class="sxs-lookup"><span data-stu-id="40af0-130">**Width**</span></span>  | <span data-ttu-id="40af0-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="40af0-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="40af0-132">必要</span><span class="sxs-lookup"><span data-stu-id="40af0-132">Required</span></span> | <span data-ttu-id="40af0-133">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="40af0-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="40af0-134">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="40af0-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="40af0-135">**高度**</span><span class="sxs-lookup"><span data-stu-id="40af0-135">**Height**</span></span> | <span data-ttu-id="40af0-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="40af0-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="40af0-137">必要</span><span class="sxs-lookup"><span data-stu-id="40af0-137">Required</span></span> | <span data-ttu-id="40af0-138">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="40af0-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="40af0-139">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="40af0-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="40af0-140">類型資訊</span><span class="sxs-lookup"><span data-stu-id="40af0-140">Type Information</span></span>



|  <span data-ttu-id="40af0-141">元素</span><span class="sxs-lookup"><span data-stu-id="40af0-141">Element</span></span>     | <span data-ttu-id="40af0-142">值</span><span class="sxs-lookup"><span data-stu-id="40af0-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="40af0-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="40af0-143">Namespace</span></span>   | <span data-ttu-id="40af0-144">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="40af0-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="40af0-145">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="40af0-145">Schema name</span></span> | <span data-ttu-id="40af0-146">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="40af0-146">Journal Reader</span></span>                             |



 

 

 




