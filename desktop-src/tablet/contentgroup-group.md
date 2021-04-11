---
description: 定義在筆記本便箋中包含一組分組內容的群組。
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: ContentGroup 群組
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027110"
---
# <a name="contentgroup-group"></a><span data-ttu-id="aa2e8-103">ContentGroup 群組</span><span class="sxs-lookup"><span data-stu-id="aa2e8-103">ContentGroup Group</span></span>

<span data-ttu-id="aa2e8-104">定義在筆記本便箋中包含一組分組內容的群組。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="aa2e8-105">定義</span><span class="sxs-lookup"><span data-stu-id="aa2e8-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="aa2e8-106">子元素</span><span class="sxs-lookup"><span data-stu-id="aa2e8-106">Child Elements</span></span>

[<span data-ttu-id="aa2e8-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="aa2e8-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="aa2e8-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="aa2e8-110">**繪圖**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="aa2e8-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="aa2e8-112">**Image**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="aa2e8-113">**旗標**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="aa2e8-114">屬性</span><span class="sxs-lookup"><span data-stu-id="aa2e8-114">Attributes</span></span>



| <span data-ttu-id="aa2e8-115">屬性</span><span class="sxs-lookup"><span data-stu-id="aa2e8-115">Attribute</span></span>  | <span data-ttu-id="aa2e8-116">類型</span><span class="sxs-lookup"><span data-stu-id="aa2e8-116">Type</span></span>                      | <span data-ttu-id="aa2e8-117">必要</span><span class="sxs-lookup"><span data-stu-id="aa2e8-117">Required</span></span> | <span data-ttu-id="aa2e8-118">描述</span><span class="sxs-lookup"><span data-stu-id="aa2e8-118">Description</span></span>                                                                                        | <span data-ttu-id="aa2e8-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="aa2e8-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="aa2e8-120">**離開**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-120">**Left**</span></span>   | <span data-ttu-id="aa2e8-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-121">**xs:integer**</span></span>            | <span data-ttu-id="aa2e8-122">必要</span><span class="sxs-lookup"><span data-stu-id="aa2e8-122">Required</span></span> | <span data-ttu-id="aa2e8-123">從原點到專案之周框方塊中最左邊點的距離。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="aa2e8-124">任何整數。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="aa2e8-125">**前幾個**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-125">**Top**</span></span>    | <span data-ttu-id="aa2e8-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-126">**xs:integer**</span></span>            | <span data-ttu-id="aa2e8-127">必要</span><span class="sxs-lookup"><span data-stu-id="aa2e8-127">Required</span></span> | <span data-ttu-id="aa2e8-128">從原點到專案之周框方塊中最上方點的距離。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="aa2e8-129">任何整數。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="aa2e8-130">**寬度**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-130">**Width**</span></span>  | <span data-ttu-id="aa2e8-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa2e8-132">必要</span><span class="sxs-lookup"><span data-stu-id="aa2e8-132">Required</span></span> | <span data-ttu-id="aa2e8-133">元素周框方塊的寬度。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="aa2e8-134">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="aa2e8-135">**高度**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-135">**Height**</span></span> | <span data-ttu-id="aa2e8-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa2e8-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa2e8-137">必要</span><span class="sxs-lookup"><span data-stu-id="aa2e8-137">Required</span></span> | <span data-ttu-id="aa2e8-138">元素周框方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="aa2e8-139">任何非負整數。</span><span class="sxs-lookup"><span data-stu-id="aa2e8-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="aa2e8-140">類型資訊</span><span class="sxs-lookup"><span data-stu-id="aa2e8-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="aa2e8-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="aa2e8-141">Namespace</span></span>   | <span data-ttu-id="aa2e8-142">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="aa2e8-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="aa2e8-143">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="aa2e8-143">Schema name</span></span> | <span data-ttu-id="aa2e8-144">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="aa2e8-144">Journal Reader</span></span>                             |



 

 

 




